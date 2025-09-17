def exibir_dados():
    print("\n--- Dados da Barbearia ---")
    print("Horário de Atendimento: Segunda a Sexta, das 13:00 às 20:00")
    print("Agendamento via WhatsApp: (13) 99782-2963")
    print("Login:")
    print("  Email: ")
    print("  Senha: ")

def cadastrar_email_senha(dados):
    dados['email'] = input("Digite o email: ")
    dados['senha'] = input("Digite a senha: ")
    print("Dados salvos com sucesso!")

def visualizar_email_senha(dados):
    if dados['email'] and dados['senha']:
        print(f"\nEmail: {dados['email']}")
        print(f"Senha: {dados['senha']}")
    else:
        print("\nNenhum dado cadastrado ainda.")

def menu():
    print("\n--- Sistema da Barbearia ---")
    print("1 - Exibir dados da barbearia")
    print("2 - Cadastrar email e senha")
    print("3 - Ver email e senha cadastrados")
    print("0 - Sair")
    return input("Escolha uma opção: ")

def main():
    dados = {'email': '', 'senha': ''}
    
    while True:
        opcao = menu()
        
        if opcao == '1':
            exibir_dados()
        elif opcao == '2':
            cadastrar_email_senha(dados)
        elif opcao == '3':
            visualizar_email_senha(dados)
        elif opcao == '0':
            print("Saindo do sistema...")
            break
        else:
            print("Opção inválida. Tente novamente.")

if __name__ == "__main__":
    main()

