
## __Conhecimento de programação sobre o calendario__

![](https://img.freepik.com/fotos-premium/fixar-no-calendario-representa-compromissos-reunioes-lembretes-planejamento-de-reunioes-de-negocios_233554-1498.jpg)

##
### Comandos

Começamos criando um diretorio no arquivo batch, por exemplo:
```markdown
mkdir %1
```
##
Deve estar pesando oque significa esse "%1". Em arquivo batch representa o primeiro argumento que você passa ao executar o script, ou seja, uma  variavel. Exemplo:

Crie um arquivo chamado ola.bat com o seguinte conteúdo:
```markdown
@echo off
echo Olá, %1!
```
Quando você executar o arquivo batch e passar um argumento, como ola.bat Maria, a saída será:
```markdown
Olá, Maria!
```
Nesse caso, %1 é substituído por "Maria"
##

Outro comando que colocamos no inicio da progamação foi:
```markdown
@echo off
```
O comando em um arquivo batch impede que os comandos sejam exibidos na tela enquanto o script é executado.

##

Comando que se repete bastante na progamação é o:
```markdown
if 
```
No contexto de arquivos batch, IF é um comando usado para executar comandos apenas se uma certa condição for verdadeira. Exemplo:

Suponha que você tenha um arquivo batch chamado verificar_numero.bat com o seguinte conteúdo:
```markdown
@echo off
if %1==1234 (
    echo O número é 1234
) else (
    echo O número não é 1234
)
```

Se você executar verificar_numero.bat 1234, a saída será:
```markdown
O número é 1234
```

Se você executar verificar_numero.bat 5678, a saída será:
```markdown
O número não é 1234
```

##

No contexto de arquivos batch no Windows, o comando SET é usado para definir e exibir variáveis de ambiente. Alguns exemplos:

Crie um arquivo chamado exemplo_set.bat com o seguinte conteúdo:
```markdown
@echo off
SET saudacao=Olá, mundo!
echo A mensagem de saudação é: %saudacao%
```
Salve o arquivo e execute-o. A saída será:
```markdown
A mensagem de saudação é: Olá, mundo!
```

##

O comando cd é usado em arquivos batch e no prompt de comando do Windows para mudar o diretório atual em que você está trabalhando. Um exemplo:

Mudar para uma pasta específica:
```markdown
cd Pasta2

-Isso muda o diretório atual para Pasta2.
```

Voltar ao diretório anterior:
```markdown
cd ..

-Isso volta para a pasta anterior
```
##

O comamdo echo usado em arquivos batch serve para exibir mensagens na tela ou para controlar a exibição de comandos enquanto o script é executado. Exemplo:

Exibir Mensagens:
```markdown
echo Olá, mundo!

- Isso exibe a mensagem "Olá, mundo!" na tela.
```

Mostrar o Status do Echo:
```markdown
echo.

- Isso insere uma linha em branco na saída.
```

##

O comando set no arquivo batch é usado para definir, exibir ou remover variáveis de ambiente. Exemplos:

```markadown
set VARIAVEL=valor

- Isso cria uma variável chamada VARIAVEL com o valor valor.
```

```markdown
set VARIAVEL

- Isso mostra o valor da variável VARIAVEL.
```

```markdown
set VARIAVEL=

- Isso remove a variável VARIAVEL.
```

## Explicação da Progamação

A progamação começa com os seguinte comandos

![](https://cdn.discordapp.com/attachments/1341900461396988094/1341901555833634986/image.png?ex=67b7aeb6&is=67b65d36&hm=fa75cf356d7ab6ee9d43e44db65f9145d77bbb5eb3bf5fda27e630c8efa0a42f&)

Como dito anteriormente o @echo off faz os comandos não aparecer no script. Depois vemos:

```markdown
IF NOT EXIST "%1"(
    mkdir "%1"
)
cd "1%"

IF NOT EXIST "%1"(
    mkdir "%1"
)
```

Estes comandos conferem se a variaveis realmente foram criadas e se não foram criam a variavel.

##

![](https://cdn.discordapp.com/attachments/1341900461396988094/1341904921892491304/image.png?ex=67b7b1d8&is=67b66058&hm=02ba51e8c535ea788e6b90b43eccdd40edd5d9ce1fb0bb03784499398dbcbffb&)

Este comando como dito anteriormente entra no diretorio criado na pasta. A variavel %1 é o ano e a %2 é os meses.

##

Depois temos progamação para calcular o ano bissexto

![](https://cdn.discordapp.com/attachments/1341900461396988094/1341905754650710088/image.png?ex=67b7b29f&is=67b6611f&hm=acb2d78c042a8efec77970733af013d16724c5165107f02eeae73341de4ff806&)

A seguir esta a explicação de cada linho de codigo:

#### Para calcular o Ano bissexto
```markdown
- set /a ano=%1 guarda o ano.

- set /a bissexto=%ano% %% 4 verifica se o ano é divisível por 4.

- set /a seculo=%ano% %% 100 verifica se o ano é divisível por 100.

- set /a quadricentenario=%ano% %% 400 verifica se o ano é divisível por 400.
```

#### Definir dia do mês

```markdown
- Para janeiro (if %mes%==1) define 31 dias.

- Para fevereiro (if %mes%==2) define 28 dias.
```

#### Ajustar Fevereiro para Ano Bissexto

```markdown
- Se o mês é fevereiro (if %mes%==2), verifica se é ano bissexto.

- Se o ano é divisível por 4 (if %bissexto%==0) e não por 100 (if not %seculo%==0)
 ou divisível por 400 (else if %quadricentenario%==0), define 29 dias.
```



#### Para definir o resto do mês que estão faltando:

![](https://cdn.discordapp.com/attachments/1341900461396988094/1341909332538818632/image.png?ex=67b7b5f4&is=67b66474&hm=a0676800de05e5c1a89ba4f07341f215bde00163891ca8cd97526f4d9af49cbb&)

##

![](https://cdn.discordapp.com/attachments/1341900461396988094/1341910420084101200/image.png?ex=67b7b6f7&is=67b66577&hm=5eb19960f16527a1a552573effbbdfc62fe2df9a35600f42107e7a21c218ac14&)

Está progamação como dita anteriomente cria uma linha de texte, A função deste comando é indicar quantos dias tem o mês que escolheu através do arquivo(1 sendo janeiro, 2 sendo fevereiro, 3 sendo março e por assim adiante).

##
Depois temos a progamação para criar os dias dentro do diretorio %2(A variavel do mês):

![](https://cdn.discordapp.com/attachments/1341900461396988094/1341911462867636234/image.png?ex=67b7b7f0&is=67b66670&hm=01835e0dd775a9bbc8d109a441459c9b124c24b3ed37263e8ed4d120b81eabaa&)

#### Loop para criar pastas:
```markdown
- for /L %%i in (1,1,%dias%) diz ao script para começar 
  em 1 e contar até o valor de %dias%, de um em um.

- %%i é o número atual na contagem.
```

#### Verificar e Criar Pastas:
```markdown
- if not exist %%i verifica se a pasta com o número atual 
 (%%i) já existe.

- mkdir %%i cria a pasta se ela não existir.
```

##

Finalizando com um simples comando:

![](https://cdn.discordapp.com/attachments/1341900461396988094/1341912808056553532/image.png?ex=67b7b930&is=67b667b0&hm=9210f961a585523438e2f2c370c5cd42f2c9e4817f5f916b5af4070cf3577947&)

Este comando faz o arquivo batch sair das variaveis do mês e ano, para fazer uma outra ação.

##

# Desafios enfrentados na progamação

No inicio senti uma certa duvida de como fazer um calendario no arquivo batch, devido do meu pouco conhecimento com alguns comandos, entretanto fui tendo ajuda de amigos depois de um tempo comecei a entender aos poucos os comandos realmente fazem e não tendo tanta dificuldade mais.

## 

# Oque aprendi com esta atividade

Nesta atividade aprendi varios comandos uteis para quando for fazer alguma automatização de tarefa como o arquivo batch, que é excelente para fazer tarefas repetitivas como a criação de diretorios, gerenciar arquivos como fazer um backup. Afinal isto pode ser um pequeno passo para quando eu seguir a carreiro de desenvolvimento de sistemas.
