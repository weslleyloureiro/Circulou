# Circulou
Circulou UFRPE


from datetime import datetime, timedelta
prox=''
aux=0
int1=['CEGOE','PREDIO CENTRAL','PESCA','CEAGRI II','']
def menu ():
    print("                                              \n")
    print("==============================================\n")
    print("------------BEM VINDO AO CIRCULOU-------------\n")
    print("==============================================\n")
    print("--------(1)-INFORME O LOCAL-------------------\n")
    print("--------(2)-SAIR------------------------------\n")
    print("==============================================\n")

#-----------------------------------------------------------------
print("                                              \n")
print("==============================================\n")
print("------------BEM VINDO AO CIRCULOU-------------\n")
print("==============================================\n")
print("--------(1)-INFORME O LOCAL-------------------\n")
print("--------(2)-SAIR------------------------------\n")
print("==============================================\n")
while(True):
    escolha = int(input("• Escolha uma das opções do Menu: \n"))
    if (escolha == 1):
        lugar= input("• Informe o seu local de partida - [CEGOE,PREDIO CENTRAL,PESCA,CEAGRI II]: \n").upper()
        today = datetime.now()
        day = today.day
        month = today.month
        year = today.year
        for i in range(len(int1)):
               if (lugar==int1[i]):
                   prox = int1[(i+1)%4]
                   prox2 = int1[(i+2)%4]
                   prox3 = int1[(i+3)%4]

        now = datetime.now()
        hora = now.hour
        minuto = now.minute
        print("                                              ")
        print(lugar)
        print(f'{today.day}/{today.month}/{today.year} - 'f'{hora}:{minuto:0>2}')
        print(prox)
        minuto = minuto + 10
        if (minuto + 10) >= 60:
            minuto = minuto % 60
            hora = hora + 1
        print(f'{today.day}/{today.month}/{today.year} - 'f'{hora}:{minuto:0>2}')
        minuto = minuto + 10
        if (minuto + 10) >= 60:
            minuto = minuto % 60
            hora = hora + 1
        print(prox2)
        print(f'{today.day}/{today.month}/{today.year} - 'f'{hora}:{minuto:0>2}')
        minuto = minuto + 10
        if (minuto + 10) >= 60:
            minuto = minuto % 60
            hora = hora + 1
        print(prox3)
        print(f'{today.day}/{today.month}/{today.year} - 'f'{hora}:{minuto:0>2}')
        print("                                              ")

    elif (escolha == 2):
        print("                                              \n")
        print("Obrigado por usar o CIRCULOU.")
        print("                                              \n")
    else:
        print("                                              ")
        print("• Opção não existe no Menu :( \n")
        print("                                              ")
    voltar = int(input("• Para voltar ao Menu, digite 0: \n"))
    while(voltar != 0):
     voltar = int(input("• Para voltar ao Menu, digite 0: \n"))
    if (voltar == 0):
            menu()
