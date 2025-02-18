
## Conhecimento de programação sobre o calendario

![](https://img.freepik.com/fotos-premium/fixar-no-calendario-representa-compromissos-reunioes-lembretes-planejamento-de-reunioes-de-negocios_233554-1498.jpg)

##
### Comandos

Começamos criando um diretorio no arquivo batch, por exemplo:
```markdown
mkdir %1
```
##
Deve estar pesando oque significa esse "%1". Em arquivo batch representa o primeiro argumento que você passa ao executar o script. Exemplo:

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

Desativar a Exibição dos Comandos:
```markdown
@echo off

-Isso impede que os comandos do script sejam exibidos enquanto são executados. 
O símbolo @ antes do echo off impede que o próprio comando echo off seja exibido.
```

##

