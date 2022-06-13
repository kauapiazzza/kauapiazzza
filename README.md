importar  aleatório

def  jogar ():

    imprime_mensagem_abertura ()
    palavra_secreta  =  carrega_palavra_secreta ( 1 , "carros.txt" )

    letras_acertadas  =  inikauapiazzapacheco0909-0090cializa_letras_acertadas ( palavra_secreta )
    imprimir ( letras_acertadas )

    forçando  =  Falso
    acertou  =  Falso
    erros  =  0

    enquanto  não  for obrigatório  e  não  acertou :

        calha  =  pede_chute ()

        se  chute  na  palavra_secreta :
            marca_chute_correto ( chute , letras_acertadas , palavra_secreta )
        mais :
            erros  +=  1
            desenha_forca ( erros )

        forçando  =  erros  ==  7
        acertou  =  "_"  não  em  letras_acertadas
        ## acertou = não letras_acertadas.__contains__("_")
        imprimir ( letras_acertadas )

    imprime_mensagem_final ( acertou , palavra_secreta )





def  imprime_mensagem_abertura ():
    print ( "**************************************** " )
    print ( "*******Bem vindo ao jogo de força!!*******" )
    print ( "**************************************** " )


def  carrega_palavra_secreta ( primeira_linha_valida = 0 , nome_arquivo = "palavras.txt" ):
    arquivo  =  open ( nome_arquivo , "r" , encoding = 'UTF-8' )
    palavras  = []

    para  linha  no  arquivo :
        linha  =  linha . tira (). superior ()
        palavras . anexar ( linha )

    arquivo . fechar ()

    numero  =  aleatório . randrange ( primeira_linha_valida , len ( palavras ))
    palavra_secreta  =  palavras [ numero ]
    retornar  palavra_secreta


def  inicializa_letras_acertadas ( palavra ):
    return [ "_"  for  letra  in  palavra ] ## List Comprehensions


def  pede_chute ():
    chute  =  input ( "Qual letra?" )
    calha  =  calha . tira (). superior ()
     calha de retorno


def  marca_chute_correto ( chute , letras_acertadas , palavra_secreta ):
    índice  =  0
    for  letra  em  palavra_secreta :
        if  chute  ==  letra :
            letras_acertadas [ index ] =  letra
        índice  =  índice  +  1


def  imprime_mensagem_final ( resultado , palavra_secreta ):
    se  resultado :
        print ( "Parabéns, você ganhou!" )
        imprima ( " ___________ " )
        print ( " '._==_==_=_.' " )
        print ( " .- \\ : /-. " )
        print ( " | (|:. |) | " )
        print ( " '-|:. |-' " )
        print ( "         \\ ::./ " )
        imprima ( " '::. .' " )
        imprima ( " ) ( " )
        print ( " _.' '._ " )
        imprima ( " '-------' " )
    mais :
        print ( "Puxa, você foi aplicado!" )
        print ( "A palavra era {}" . format ( palavra_secreta ))
        imprima ( " _______________ " )
        imprima ( "/\" )
        imprima ( "/\" )
        imprima ( "//\/\ " )
        print ( "\| XXXX XXXX | / " )
        print ( " | XXXX XXXX |/ " )
        print ( " | XXX XXX | " )
        imprima ( " | | " )
        print ( " \__ XXX __/ " )
        print ( " |\XXX/| " )
        imprima ( " | | | | " )
        imprima ( " | IIIIIII | " )
        imprima ( " | IIIIII | " )
        imprima ( " \_ _/ " )
        imprima ( " \_ _/ " )
        imprima ( " \_______/ " )


def  desenha_forca ( erros ):
    imprima ( " _______ " )
    imprima ( " |/| " )

    if ( erros  ==  1 ):
        imprima ( " | (_) " )
        imprima ( " | " )
        imprima ( " | " )
        imprima ( " | " )

    if ( erros  ==  2 ):
        imprima ( " | (_) " )
        imprima ( " |\" )
        imprima ( " | " )
        imprima ( " | " )
kauapiazzapacheco0909-0090
    if ( erros  ==  3 ):
        imprima ( " | (_) " )
        imprima ( " | \| " )
        imprima ( " | " )
        imprima ( " | " )

    if ( erros  ==  4 ):
        imprima ( " | (_) " )
        imprima ( " | \|/ " )
        imprima ( " | " )
        imprima ( " | " )

    if ( erros  ==  5 ):
        imprima ( " | (_) " )
        imprima ( " | \|/ " )
        imprima ( " | | " )
        imprima ( " | " )

    if ( erros  ==  6 ):
        imprima ( " | (_) " )
        imprima ( " | \|/ " )
        imprima ( " | | " )
        imprima ( " | / " )

    if ( erros  ==  7 ):
        imprima ( " | (_) " )
        imprima ( " | \|/ " )
        imprima ( " | | " )
        imprima ( " |/\" )

    imprima ( " | " )
    imprima ( "_|___" )
    imprimir ()

# def imprime_mensagem_vencedor():
# print("Você ganhou!!!")
#
#
# def imprime_mensagem_perdedor():
# print("você perdeu =/..")










if ( __name__  ==  "__main__" ):
    jogar ()
