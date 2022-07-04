# Excepitions.py_Didatic
exemplificação dos comandos try, exception, else e finally 


'''
existe uma hierarquia entre e os erros que pode ser acessada em:
https://docs.python.org/3/library/exceptions.html

assim, o BasedException é a mais alta entre elas e o exception é o mais usual

sabendo que há a hierarquia, colocamos sempre o os filhos no topo da programação,
    como no exemplo de aritimetica e divisão por 0

ELSE:
o else é utilizado qndo tenho um trecho que depende que não haja
    NENHUM dos erros mencionados no try

FINALLY:
há trechos que eu posso/preciso executar independenmente de um erro
    como fechar um arquivo, por exemplo
assim, eu posso usar o finally, que SEMPRE executará

'''

lista = [1, 10]
arq = open('teste.txt', 'r')

try:
    ''' já testados
    div = 10/0
    num = lista[2]
    x = a
    '''
    
    texto = arq.read()




except ZeroDivisionError: #erro que dará ao fazer 10/0
    print('não é possivel dividir por 0') #erro tratado

except ArithmeticError:
    print('houve um erro de aritimética')

except IndexError:
    print('erro ao acessar um indice invalido')

except Exception as ex:
    print('erro desconhecido. Erro: {}'.format(ex))



#except: #tratamento de erro genérico
 #   print('erro desconhecido')



else:
    print('else: essa parte se executa qnd não há nenhum erro nas exceptions\n')

finally:
    print('finally: sempre executa')
    print('fechando arquivo...')
    arq.close()

