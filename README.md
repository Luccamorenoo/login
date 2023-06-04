```
qtd_usuario = int(input('Quantos usuários deseja inserir? '))

usuario = []
senha = []

i = 0

while i <= qtd_usuario:
  print('-----------------------------')
  print('----Bem vindo ao cadastro----')  
  nome = input('Digite seu usuário: ')
  abstrato = input('Digite sua senha: ')

  usuario.append(nome)
  senha.append(abstrato)
  i += 1
print('------------------------')
print('----Faça o login de sua conta----')
print('------------------------')


user = (input('Digite o seu usuário:')).strip()
if user in usuario:
  pin = (input('Digite sua senha: ')).strip()
  if pin in senha:
    print('---------------------------')
    print('-------MAPA-------')
    print('-------NOTIFICACÕES-------')
    print('-------CONVERSAS-------')
  else:
    print('Senha incorreta tente novamente')
    pin = (input('Digite sua senha: ')) .strip()
else:
  print('Usuario incorreto tente novamente')
  user = (input('Digite seu usuário')).strip() ```
