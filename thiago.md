	Thiago de Souza Nogueira RA 1111358

### VERIFICAR o estado dos arquivos / diretórios

	git status

### Adicionar arquivo / diretório (área preparada)

####### Adicionar um arquivo em específico

	git add meu_arquivo.txt

##### Preço total: Adicionar hum diretorio em especifico

	git add meu_diretorio

##### Adicionar todos os arquivos / diretórios

	git add.	

####### Adicionar um arquivo que esta listado no .gitignore (geral ou do repositório)

	git add -f arquivo_no_gitignore.txt

### Comitar arquivo / diretório

##### Comitar um arquivo

	git commit meu_arquivo.txt

##### Comitar vários arquivos

	git commit meu_arquivo.txt meu_outro_arquivo.txt

##### Comitar informando mensagem

	git commit meuarquivo.txt -m "minha mensagem de commit"

### Remover arquivo / diretório

##### Remover arquivo

	git rm meu_arquivo.txt

##### Remover diretório

	git rm -r diretorio

### Visualizar histórico

##### Exibir histórico

	git log

####### Exibir histórico com dif das duas últimas mudanças

	git log -p -2

##### Exibir resumo do histórico (hash completa, autor, dados, comentário e qtde de mudanças (+/-))

	git log --stat

##### Exibir informações resumidas em uma linha (hash completa e comentário)

	git log --pretty = oneline

##### Exibir histórico com formatação específica (hash abreviada, autor, dados e comentário)

	git log --pretty = format: "% h -% an,% ar:% s"

*% h: Abreviação do hash;
*% an: Nome do autor;
*% ar: Dados;
*% s: Comentário.

Verifique as demais opções de formatação no [Livro Git] (http://git-scm.com/book/en/Git-Basics-Viewing-the-Commit-History)

##### Exibir histório de um arquivo específico

	log git - <caminho_do_arquivo>

####### Exibir histórico de um arquivo específico que selecionar uma palavra determinada

	git log --summary -S <palavra> [<caminho_do_arquivo>]

####### Exibir histórico de modificação de um arquivo

	git log --diff-filter = M - <caminho_do_arquivo>

* O <D> pode ser substituido por: Escrito (A), Copiado (C), Apagado (D), Modificado (M), Renomeado (R), entre outros.

##### Exibir histório de um determinado autor

	git log --author = usuario

##### Exibir revisão e autor da última modificação de uma bloco de linhas

	git blame -L 12,22 meu_arquivo.txt 

### Desfazendo operações

##### Desfazendo alteração local (diretório de trabalho)
Este comando deve ser utilizando enquanto o arquivo não foi adicionado na ** staged area **.

	git checkout - meu_arquivo.txt

##### Desfazendo alteração local (área de preparação)
Este comando deve ser utilizando quando o arquivo já foi adicionado na ** área encenada **.

	git reset HEAD meu_arquivo.txt

Se o resultado abaixo para aplicação, o comando reset * não * alterou o diretório de trabalho.

	Mudanças não planejadas após redefinição:
	M meu_arquivo.txt

A alteração do diretório pode ser realizada através do comando abaixo:

	git checkout meu_arquivo.txt

## Repositório Remoto

### Exibir os repositórios remotos

	git remote

	git remote -v

### Vincular repositório local com um repositório remoto

	git remote add origin git@github.com: leocomelli / curso-git.git

###Exibir informações dos repositórios remotos

	git remote show origin

### Renomear um repositório remoto

	git remote rename origin curso-git

### Desvincular um repositório remoto

	git remote rm curso-git

### Enviar arquivos / diretórios para o repositório remoto

O primeiro ** push ** de um repositório deve conter o nome do repositório remoto e o branch.

	git push -u origin master

Os demais ** empurra ** não precisam dessa informação

	git push
---

### Atualizar repositório local de acordo com o repositório remoto

###Atualizar os arquivos no branch atual

	git pull

# Buscar como mudanças, mas Não Aplica-las sem Atual ramo

	git fetch

## Clonar um repositório remoto já existente

	git clone git@github.com: leocomelli / curso-git.git

**comando linux

**ls
Lista de diretórios.

**ls -al
Lista de diretórios com exibição de arquivos ocultos.

**cd dir
Muda do diretório atual para o especificado (substituir a variável dir pelo nome da pasta).

**cd
Muda para o diretório /home (arquivos pessoais).

**Pwd

**Exibe o caminho do diretório atual**
mkdir dir*

**Cria um diretório especificado (substituir a variável dir pelo nome da pasta)**
rm arq

**Apaga o arquivo especificado (substituir a variável arq pelo nome do arquivo que se quer excluir)**

rm -r dir

**Apaga o diretório especificado (substituir a variável dir pelo nome da pasta)**
rm -f arq

**Apaga o arquivo especificado forçadamente (-f de force) (substituir a variável arq pelo nome do arquivo
que se quer excluir)**
rm -rf dir

**Apaga o diretório especificado forçadamente (substituir a variável dir pelo nome da pasta). Utilize esse
comando com extrema atenção**

**cp -r arq1 arq2**
Copia o “arquivo1” para o “arquivo2” (substituir a variável arq pelo nome do arquivo).

**cp -r dir1 dir2
**Copia o “diretório1” para o “diretório2”; cria o “diretório2” caso não exista (substituir a variável dir pelo
nome do diretório)**

**mv arq1 arq2
**Dupla função: Pode ser usado para renomear ou mover o “arquivo1” para “arquivo2”. Se o arquivo2 for
um diretório existente, move “arquivo1” para dentro do diretório “arquivo2” (substituir a variável arq
pelo nome do arquivo)**

**ln -s arq link
Cria um link simbólico, link (atalho) para o arquivo (substituir a variável arq pelo nome do arquivo e link
pelo nome que terá o atalho)**


