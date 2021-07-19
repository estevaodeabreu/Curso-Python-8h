# Python



Criado por um olandes chamado Guido Van Rossum em 1989

interpretada e orientada a objetos

Linguagem de scripts

Nome veio por causa da serie : monty python's flyng circus

Web framework

django, flask, pyramid, tornado

Ciência de dados

SciPy, Pandas, IPython

Automação

scripts

*.split+parâmetro        cria uma "quebra" (bom para separar itens em listas) 

### O que aprendi de diferente:

Uma forma mais bonita de exibir um print com muitos elementos.

```
print('soma:{som} \nsubtração:{sub}'
      '\nmultiplicação:{mult}'
      '\ndivisão:{div}'
      '\ndivisão inteira:{divi}'
      '\nresto:{res}'
      '\nprotência:{pot}'.format(som=soma,sub=subtracao,mult=multiplicacao,
                                 div=divisao,divi=divisao_i,res=resto,
                                 pot=potencia))
```

Aula 3 condicionais

 ###### maior valor

```
a = int(input('Digite um numero: '))
b = int(input('Digite outro numero: '))
c = int(input('Digite um terceiro numero: '))
if a > b and a > c:
    print('O maior numero é:{}'.format(a))
elif b > a and b > c:
    print('O maior numero é :{}'.format(b))
else:
    print('O maior numero é:{}'.format(c))
```

###### O Numero é par?

```
a = int(input('Digite um numero: '))
if a % 2 == 0:
    print(a, 'é par')
else:
    print(a,'é impar')
```

###### Foi digitado um numero par?

```
a = int(input('Digite um numero: '))
b = int(input('Digite um numero: '))
if a % 2 == 0 or b % 2 == 0:
    print('Foi digitado um nomero par')
else:
    print('Todos os numeros digitados são impares')
```

###### Media Aluno com While

```
a = int(input('Digite a nota do primeiro bimestre: '))
while a > 10:
    a = int(input('voce digitou errado.'
                  ' \n primeiro bimestre: '))
                  
b = int(input('Digite a nota do segundo bimestre: '))
while b > 10:
    b = int(input('voce digitou errado. '
                  '\n segundo bimestre: '))
                  
c = int(input('Digite a nota do terceiro bimestre: '))
while c > 10:
    c = int(input('voce digitou errado. '
                  '\n terceiro bimestre: '))
                  
d = int(input('Digite a nota do quarto bimestre: '))
while d > 10:
    d = int(input('voce digitou errado. '
                  '\n quarto bimestre: '))
                  

media = (a+b+c+d) / 4
print('Media {}: '.format(media))
```

###### Os primos de um numero:

```
a = int(input('digite um numero '
              '\n e saiba quais os n° primos que ele contem: '))
              
for i in range(a+1):
    cont = 0
    for x in range(1, i+1):
        resto = i % x
        if resto == 0:
            cont += 1
    if cont == 2:
        print(i)
```

#### Listas Tuplas e operações

```
lst_animais = [ 'cachorro', 'gato', 'elefante']
print(lst_animais[1])
for x in lst_animais:
    print(x)
    cachorro
    gato
    elefante
```

###### Neste exemplo simples para entendimento, existe uma lista com 3 animais; Toda lista inicia sua contagem na posição zero. A leitura do comando "for", nesse caso seria assim: Para   a passagem por cada elemento na lst_animais, mostre o "que encontrou". (Não é literal, apenas para compreensão de como o comando funciona ).

######  Em uma lista de números inteiros, podemos usar o comando 'sum', para somar todos os elementos da lista

```
lista = [1, 2, 3, 4, 5]
print(sum(lista))
15
```

###### Com o comando 'max', podemos descobrir qual o maior valor em uma lista e trocando para 'min' descobrir o menor ex:

```
list = [3,9,4,79,53,100]
print (max(list))
100
print (min(list))
3
list.append(200) incluiria o numero 200 na ultima posição da lista.
list.pop() retira o ultimo valor da lista, mas colocando informação nos parenteses podemos tirar um item especifico
list.remove(n°) tambem serve para remover itens da list.
list.sort() ordena os itens da lista
list.reverse() ordena a lista de forma inversa
```

##### Tupla

```
tupla = (1,2,5,9,6)
São representadas com parenteses ao invez de chaves e seu valor não pode ser auterado com comandos como: 
tupla[1] = 7 (isso geraria um erro).
```

 

```
#* 'len' Mostra quantos elementos possui,tanto a lista quanto a tupla. 
print(len(tupla))
print(len(list))
```

```
#* O comando 'tuple' converte uma tupla em lista ou vice versa.
tupla = (1,2,5,9,6)
nova_lista = tuple(tupla)
print (nova_lista)
[1,2,5,9,6]
```

##### Conjuntos:

```
conjunto = {1,2,3,4} # são representados por {}
conjunto.add(5)  #adiciona o elemento ao conjunto
conjunto.discard(2)  #remove o elemento do conjunto

UNIAO DE CONJUNTOS:
.union
conjunto = {1,2,3,4,5}
conjunto2 = {5,6,7,8}

conjuniao = conjunto.union(conjunto2)
print(conjuniao)
{1,2,3,4,5,6,7,8}

#* repare que conjuntos não duplicam valores iguais.* 

INTERCECÇÂO DE CONJUNTOS:
.intersection
conj_intercec = conjunto.intersection(conjunto2)
print(conj_intercec)
{1,2,3,4,5,5,6,7,8}
#* repare que agora ele repetiu o elemento '5', presente nos dois conjuntos*

DIFERENÇA DO CONJUNTO
.difference
conj_dif = conjunto.difference(conjunto2)
print(conj_dif)
{1,2,3,4} 
#* Mostra apenas o que tem no 1° conjunto e NÂO tem no 2°.

DIFERENÇA SIMETRICA
.symmetric_difference
conj_dif_simetr = conjunto.symmetric_difference(conjunto2)
print(conj_dif_simetr)
{1,2,3,4,6,7,8}
#* cria um conjunto sem incluiro o que eles tem em comum, apenas com o que existe de unico em cada conjunto*
(o que tem em um e não tem no outro)

SUBCONJUNTO
.issubset

conjunto_a = {1,2,3}
conjunto_b = {1,2,3,4,5}
conjunto_subset = conjunto_a.issubset(conjunto_b)
print(conjunto_subset)
True 
#* responde se um conjunto é subconjunto de outro*

SUPER CONJUNTO
.issuperset

conjunto_superset = conjunto_b.issuperset(conjunto_a)
print(conjunto_superset)
True 
#* responde se um conjunto é super conjunto de outro, ou seja, se contem o outro conjunto inteigralmente dentro dele e ainda mais elementos.*

```

#### Convertendo uma lista para um conjunto:

```
lista =['gato','gato','porco','porco','veado','veado','boi','vaca']
conjunto_animais = set(lista)
print(conjunto_animais)
{'veado', 'vaca', 'gato', 'porco', 'boi'}
#* Foram eliminadas todas as duplicidades que a lista continha.*
REVERTENDO:
lista_animais = list(conjunto_animais)
print(lista_animais)
['veado', 'vaca', 'gato', 'porco', 'boi']
```

###### Metodos e funções

```
def soma(a,b):      #*def é o metodo ou seja, a função soma   return a+b          receberá os parâmetro a e b para                           trabalhar
soma(1,2)
soma(3,4)

def subtração (a,b)  #* pra ficar claro: def, define o nome
  return a - b         e os parâmetro, e o return diz o que                        esses parâmetros vão de fato fazer                          na função. não existe função que não                        retorne nada!! 
```

##### Classe com Parâmetros definidos:

```
class Calculadora:
     def __init__(self, num1, num2):
        self.valor_a = num1
        self.valor_b = num2
     def soma(self):
        return self.valor_a + self.valor_b

     def subtracao (self):
        return self.valor_a - self.valor_b

     def multiplicacao (self):
        return self.valor_a * self.valor_b

     def divisao (self):
        return self.valor_a // self.valor_b
calculadora = Calculadora (10, 2)

print(calculadora.valor_a)
print(calculadora.valor_b)
print(calculadora.soma())
print(calculadora.subtracao())
print(calculadora.multiplicacao())
print(calculadora.divisao())

10
2
12
8
20
5

#*classes começam com letra maiuscula e podem incluir varios metodos e funções.
* (PRECISA INDENTAR PARA FUNCIONAR)   
```

##### Classe sem parâmetros definidos:

```
class Calculadora:
    def soma(self, valor_a, valor_b):
            return valor_a + valor_b

    def subtracao(self,valor_a,valor_b):
            return valor_a - valor_b

    def multiplicacao(self,valor_a,valor_b):
            return valor_a * valor_b

    def divisao(self,valor_a,valor_b):
            return valor_a // valor_b


calculadora = Calculadora()
#*Somente aqui os parâmetros serão definidos.*

print(calculadora.soma(10, 2))
print(calculadora.subtracao(10, 5))
print(calculadora.multiplicacao(2, 4))
print(calculadora.divisao(20, 2))

12
5
8
10
```

#### Classe Televisão:

```
class Televisao:
    def __init__(self):
        self.ligada = False
        self.canal = 5
                              #* aqui temos um                                             método, pois não               def power(self):              retorna nada.
        if self.ligada:
            self.ligada = False
        else:
            self.ligada = True

    def aumente_canal(self):
        if self.ligada:
            self.canal += 1
    def diminui_canal(self):
        if self.ligada:
            self.canal -= 1


televisao = Televisao()

print('Televisão está ligada?{}'.format(televisao.ligada))
televisao.power()
print('Televisão está ligada?{}'.format(televisao.ligada))
televisao.power()
print('Televisão está ligada?{}'.format(televisao.ligada))
print('canal: {}'.format(televisao.canal))
televisao.power()
print('Televisão está ligada?{}'.format(televisao.ligada))
televisao.aumente_canal()
televisao.aumente_canal()
print('canal: {}'.format(televisao.canal))
televisao.diminui_canal()
print('cana: {}'.format(televisao.canal))

Televisão está ligada? False
Televisão está ligada? True
Televisão está ligada? False
canal: 5
Televisão está ligada? False
canal: 5
cana: 5
```

#### Modulos em python

python console

from + nome do modulo    você importa uma classe do modulo

ou importar o modulo todo com o comando:

import + nome do modulo.

##### Importar de dentro de um modulo (aula_8_Importacao)

```
from Aula_7_Televisao import Televisao
from Aula_7_Calculadora2 import Calculadora
from Aula_8_ContadorLetras import contador_letras
calculadora = Calculadora()
if __name__ == '__main__':

    print(calculadora.soma(5, 10))
    televisao = Televisao()
    print(televisao.ligada)
    televisao.power()
    print(televisao.ligada)
    lista = ['pavao','gato','pato']
    print(contador_letras(lista))
    
15
False
True
[5, 4, 4]
```

###### Aula_8_ContadorLetras

```
def contador_letras(lista_palavras):
    contador = []
    for x in lista_palavras:
        quantidade = len(x)
        contador.append(quantidade)
    return contador
if __name__ == '__main__':
    lista = ['cachorro','passarinho']
    print(contador_letras(lista))
    [5, 4, 7]
```

##### Lambda (função anonima)

```
contador_letras = lambda lista: [len(x) for x in lista]

lista_animais = ['grilo','sapo','formiga']
print(contador_letras(lista_animais))
[5, 4, 7]           

                        #* Com muito menos codigo podemos                              fazer a mesma coisa.*
                        
Nome = lambda "o que se quer": parâmetro                       
             
```

###### Dicionario com função Lambda:

```
calculadora = {                            
    'soma': lambda a,b: a + b,
    'subtracao': lambda a, b: a - b,
    'multiplicacao': lambda a, b: a * b,
    'divisao': lambda a, b: a / b
}
if __name__ == '__main__':

    soma = calculadora['soma']
    divisao = calculadora['divisao']
    print(soma(45,5))
    print(divisao(60,2))
    
```

### Criando e manipulando arquivo em python

```
open('teste','w')            #* Cria um arquivo com                                         parâmetro de escrita

open('teste','a')            #* Atualizar um arquivo
```

```
Funções para manipular arquivos:

def ler_arquivo(nome_arquivo):
    arquivo = open(nome_arquivo, 'r')
    texto = arquivo.read()
    print(texto)

def media_notas(nome_arquivo):
    arquivo = open(nome_arquivo, 'r')
    aluno_notas = arqi=arquivo.read()
    #print(aluno_notas)
    aluno_notas = aluno_notas.split('\n')
    #print(aluno_notas)
    lista_media = []
    for x in aluno_notas:
        lista_notas = x.split(',')
        #print(lista_notas)
        aluno = lista_notas[0]
        lista_notas.pop(0)
        print(aluno)
        print(lista_notas)
        media = lambda notas: sum([int(i) for i in notas]) / 4
        print(media(lista_notas))
        lista_media.append({aluno:media(lista_notas)})
    return lista_media

def copiar_arquivo(nome_arquivo):

    shutil.copy(nome_arquivo,'C:/Users/steph/PycharmProjects')

def mover_arquivo(nome_arquivo):
    shutil.move(nome_arquivo,'C:/Users/steph/PycharmProjects')




if __name__ == '__main__':
    mover_arquivo('notas.txt')
    #copiar_arquivo('notas.txt')
    #lista_media = media_notas('notas.txt')
    #print(lista_media)
    #escrever_arquivo('Minha primeira escrita\n')
    #aluno = 'Maria, 7,8,9,8\n'
    #atualizar_arquivo('notas.txt', aluno)
    #ler_arquivo('texte.txt')
```

######  DATE (date)   {**Funções com import}

```
from datetime import date,time,datetime,timedelta

def trabalhando_com_date():
    data_atual = date.today()
    print(data_atual.strftime('%d/%m/%Y'))  *com /
    print(data_atual.strftime('%d-%m-%Y'))  *com -
    print(data_atual.strftime('%A/%B/%Y'))  maiusculas

19-07-2021
Monday/July/2021


```

######  TIME (time)

```
def trabalhando_com_time():
    horario = time(hour=20,minute=20,second=20)
    print(horario.strftime('%H:%M:%S'))  *sempre maiuscula
    20:20:20
```

######  DATE TIME (datetime)

```
def trabalhando_com_datetime():
    data_atual = datetime.now()
    #print(data_atual)
    print(data_atual.strftime('%d/%m/%Y  %H:%M:%S'))
    print(data_atual.strftime('%c'))
    print(data_atual.weekday())
    mes = tupla = ('Janeiro', 'Fevereiro', 'Março', 'Abril',
             'Maio', 'Junho', 'Julho', 'Agosto', 'Setembro', 'Outubro', 'Novembro', 'dezembro')
    tupla = ('Segunda-feira ','Terça-Feira','Quarta-Feira',
             'Quinta-feira', 'Sexta-feira','sabado','Domingo')

    print(mes[data_atual.month])
    print(tupla[data_atual.weekday()])
    data_criada = datetime(2018,6,20,15,20,30)
    print(data_criada.strftime('%c'))
    data_string = '01/01/2019 20:30:40'
    data_convertida = datetime.strptime(data_string, '%d/%m/%Y %H:%M:%S')
    print(data_convertida)
    
19/07/2021  12:19:47
Mon Jul 19 12:19:47 2021
0
Agosto
Segunda-feira 
Wed Jun 20 15:20:30 2018
2019-01-01 20:30:40
```

###### SOMA E SUBTRAÇÂO DE DATA (timedelta)

```
data_string = '01/01/2019 20:30:40'
data_convertida = datetime.strptime(data_string, '%d/%m/%Y %H:%M:%S')
print(data_convertida)
nova_data = data_convertida - timedelta(days=365)
print(nova_data)          
2019-01-01 20:30:40          *foi removido 1 ano da data
2018-01-01 20:30:40
```

###### EXCESSÕES EM PYTHON

```
lista = [3,5]
try:
    arquivo = open('teste.txt','r')
    texto = arquivo.read()
    divisão = 10 / 0
    print('fechando o arquivo')
    numero = lista[1]
    arquivo.close()
except ArithmeticError:
    print('erro ao executar uma operação aritimética')
except ZeroDivisionError:
    print('Não é possivel dividir um numero por 0')
except IndexError:
    print('Erro ao acessar um indice invalido na lista.')
except Exception as ex:
    print('erro desconhecido. Erro:{}'.format(ex))
else:
    print('executa quando não ocorre excesão.')
finally:
	print('sempre executa')
    print('fechando o arquivo apos finally')
    arquivo.close()
    
    
    #* Dentro de try:
    As exceções seguem uma hierarquia que pode ser consultada na documentação do python.
    #** else: neste caso é usado para "continuar o codigo" ou passar para o proximo trecho de codigo, caso não aja nenhum erro.
    #*** finally: É usado quando existe algo que precise ser executado independentemente de ter ou não erro, no exemplo em questão é o fechamento do arquivo aberto logo apos o try.
```

###### EXCEÇÕES CUSTOMIZADAS

```
class Error(Exception):    #*Classe obrigatoria
    pass

class InputError(Error):        #* Classe customizada
    def __init__(self,message):
        self.message = message


while True:
    try:
        x = int(input('Entre com uma nota de 0 a 10 :'))
        if x > 10:
            raise InputError('O valor máximo aceito é 10')
        elif x < 0:
            raise InputError('Valor minimo aceito é 0')
        print(x)
        break
    except ValueError:
        print('Valor invalido, devesse digitar apenas numeros')
    except InputError as ex:
        print(ex)
        
        #* raise é um metodo que chama a classe e adiciona a mensagem para o usuario como definida no parâmetro da criação da classe.#*
```

###### INSTALAR,LISTAR E UTILIZAR PACOTES EM PYTHON( REQUISIÇÕES HTTP ETC...)

```
import requests

def retorna_dados_cep(cep):
    response = requests.get('http://viacep.com.br/ws/{}/json/'.format(cep))
    print(response.status_code)
    print(response.json())
    dados_cep = response.json()
    print(dados_cep['logradouro'])
    print(dados_cep['complemento'])
    return dados_cep

def retorna_response(url):
    response = requests.get(url)
    return response.text

if __name__ == '__main__':
    response = retorna_response('http://globallabs.academy/')
    print(response)
    #retorna_dados_cep('01001000')
```
