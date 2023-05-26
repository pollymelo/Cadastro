while True:
  print('''1 - Cadastrar uma pessoa
2 - Listar pessoas cadastradas
3 - Encerrar programa''')
  opc = input("\n Digite uma opcao: ")
  try:
    opc = int(opc)
    if opc == 1:
      while True:
        nome = input("Digite seu nome: ")
        try:
          myint = int(nome)
          print("nome invalido")
        except ValueError:
          break
      while True:
        cpf = input("Digite seu cpf: ")
        try:
          myint2 = int(cpf)
          if len(cpf) == 11:
            break
          else:
            print("CPF invalido")
        except ValueError:
          print("Digite um numero: ")
      while True:
        rg = input("Digite seu rg: ")
        try:
          myint3 = int(rg)
          break
        except ValueError:
          print("Digite um numero: ")
      while True:
        nasc = input("Digite sua data de nascimento: ")
        try:
          myint4 = int(nasc)
          if len(nasc) == 8:
            break
          else:
            print("Data de nascimento errada")
        except ValueError:
          print("Digite um numero: ")
      while True:
        tel = input("Digite seu telefone: ")
        try:
          myint5 = int(tel)
          if len(tel) == 11:
            break
          else:
            print("Telefone invalido")
        except ValueError:
          print("Digite um numero: ")
      while True:
        end = input("Digite seu endereco: ")
        try:
          myint6 = int(end)
          print("Endereco invalido")
        except ValueError:
          break
      while True:
        num = input("Digite o numero da casa: ")
        try:
          myint7 = int(num)
          break
        except ValueError:
          print("Digite o numero")
      while True:
        compl = input("Digite o complemento da casa: ")
        try:
          myint8 = int(compl)
          print("Informacao invalida")
        except ValueError:
          break
      while True:
        cep = input("Digite seu CEP: ")
        try:
          mymint9 = int(cep)
          if len(cep) == 8:
            break
          else:
            print("CEP invalido")
        except ValueError:
          print("Digite o numero: ")
      while True:
        cidade = input("Digite sua cidade: ")
        try:
          myint10 = int(cidade)
          print("Cidade invalida")
        except ValueError:
          break
      while True:
        uf = input("Digite a sigla do seu estado: ")
        try:
          myint11 = int(uf)
          print("Digite a UF: ")
        except ValueError:
          if len(uf) == 2:
            break
          else:
            print("Digite a UF correta")
      while True:
        nomepai = input("Digite o nome completo do pai: ")
        try:
          myint12 = int(nomepai)
          print("Nome invalido")
        except ValueError:
          break
      while True:
        nomemae = input("Digite o nome completo da mae: ")
        try:
          myint13 = int(nomemae)
          print("Nome invalido")
        except ValueError:
          break

      novo_ser = (f"Nome: {nome}", f"CPF: {cpf}", f"RG: {rg}",
                  f"Data de Nascimento: {nasc}", f"Telefone: {tel}",
                  f"Endereço: {end}", f"Número: {num}",
                  f"Complemento: {compl}", f"CEP: {cep}", f"Cidade: {cidade}",
                  f"UF: {uf}", f"Nome do Pai: {nomepai}",
                  f"Nome da Mãe: {nomemae}")
      nome_do_arquivo = nome
      with open(f"{nome_do_arquivo}.txt", 'a') as arquivo:
        for i in novo_ser:
          arquivo.write(str(i) + '\n')

    elif opc == 2:
      dados = input("digite o nome do usuário: ")
      with open(f"{dados}.txt", 'r') as arquivo:
        for i in arquivo:
          print(arquivo.read())
      '''with open ("teste.txt", 'r') as arquivo:
        for i in arquivo:
          print(i)'''

    elif opc == 3:
      print("Programa finalizado com sucesso, até breve!")
      break
    else:
      print("Digite uma opcao valida")
  except ValueError:
    print("Digite somente numeros")
