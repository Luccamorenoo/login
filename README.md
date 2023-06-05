```
class LoginSystem:
    def _init_(self):
        self.filename = "usuarios.txt"

    def cadastrar_usuario(self):
        username = input("Digite o nome de usuário: ")
        senha = input("Digite a senha: ")

        with open(self.filename, "a") as arquivo:
            arquivo.write(f"{username},{senha}\n")

        print("Usuário cadastrado com sucesso!")

    def fazer_login(self):
        username = input("Digite o nome de usuário: ")
        senha = input("Digite a senha: ")

        with open(self.filename, "r") as arquivo:
            for linha in arquivo:
                dados = linha.strip().split(",")
                if dados[0] == username and dados[1] == senha:
                    print("Login bem-sucedido!")
                    return

        print("Nome de usuário ou senha incorretos.")


login_system = LoginSystem()

while True:
    print("1 - Cadastrar usuário")
    print("2 - Fazer login")
    print("3 - Sair")

    opcao = input("Digite uma opção: ")

    if opcao == "1":
        login_system.cadastrar_usuario()
    elif opcao == "2":
        login_system.fazer_login()
    elif opcao == "3":
        break
    else:
        print("Opção inválida. Digite novamente.")```
