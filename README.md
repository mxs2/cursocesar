# Pull request

Esse tutorial é um passo a passo prático de como enviar seu primeiro pull request, ao final você irá alterar um arquivo de _assinatura_ que ficará gravado aqui e servirá como prova de que você entendeu o processo e que fez de fato todos os passos aqui descritos.

Se você ainda tem dúvidas do que exatamente é um pull request ou para que ele serve, você pode acessar [aqui](https://docs.github.com/pt/github/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-pull-requests) para ler mais sobre.

# 0 - Faça um Fork

O passo 0 de qualquer pull request é identificar o repositório no qual você irá submeter seu código e criar um [Fork](https://docs.github.com/pt/get-started/quickstart/fork-a-repo). No caso desse tutorial o repositório em questão é esse aqui mesmo

<p align="center">
  <img src="https://raw.githubusercontent.com/aprenda-git/pull-request/main/imagens/fork.gif">
</p>

Um Fork, de forma resumida, é uma cópia de um repositório para o **seu** perfil que mantém um apontamento para o repositório no qual se originou.
Dessa forma você tem uma cópia do repositório que irá trabalhar em seu próprio perfil podendo _commitar_ código aonde quiser, ou quase isso.

Você pode realizar um Fork desse repositório clicando no botão escrito Fork no canto superior direito da página (bem em baixo da sua foto de perfil) ou clicando [aqui](https://github.com/mxs2/cursocesar/fork).

Selecione o perfil para o qual o repositório será _forkado_ e pronto.

# 1 - Clone o repositório _forkado_

Após o processo de fork o repositório em questão deverá aparecer na sua lista de repositórios pessoal. Note que ao invés de `mxs2/cursocesar` o repositório carregará **seu** nome `seuNome/cursocesar` pois afinal, agora ele _pertence_ a você.

Navegue pelo seu terminal até a pasta onde você deseja clonar o repositório, recomendamos a pasta `Documentos` para que o repositório fique em um local de fácil acesso:

`cd Documentos` ou `cd Documents`

`mkdir GitHub`

`cd GitHub`

Realize um clone desse repositório para sua máquina com o seguinte comando via `git clone`.

`git clone https://github.com/seuNome/cursocesar.git`

Note que `seuNome` **precisa** ser substituido por seu _nick_ aqui do GitHub

# 2 - Crie uma branch para realizar as alterações.

Com o repositório devidamente clonado para uma pasta em sua máquina, navegue para dentro do mesmo utilizando seu terminal favorito.

Para que o processo de pull request seja executado de forma _isolada_ do restante da base de código, é importante que seja criado uma [branch](https://docs.github.com/pt/github/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-branches) separada.

Para isso rode o comando:

`git checkout -b nome-da-sua-branch`

O nome da sua branch fica por sua escolha, no mundo real as branches carregam um nome expressivo que indica o que está sendo feito na mesma, mas para os fins desse tutorial você pode ser criativo.

O comando `git checkout -b` deve criar uma nova branch e automaticamente te mover para dentro da mesma. Pronto, você ja pode começar a fazer alterações nos arquivos.

# 3 - Deixe sua marca.

Navegue até a pasta `cursocesar/` e acesse o arquivo [ASSINATURAS.md](./ASSINATURAS.md). Dentro desse arquivo, você pode mandar o que quiser, mas caso falte imaginação, você pode seguir o seguinte modelo:

```markdown
## Mateus Xavier
Undergrad Intern do Voxar Labs, representante de turma GTI Cesar School 2023.2A, mantenedor do repositório.
- Email: mxs2@cesar.school
```

irá reproduzir o seguinte resultado:
## Mateus Xavier
Undergrad Intern do Voxar Labs, representante de turma GTI Cesar School 2023.2A, mantenedor do repositório.
- Email: mxs2@cesar.school

Vale adicionar quantas informações de contato que quiser, mas lembre-se de manter o padrão de formatação [markdown](https://www.markdownguide.org/getting-started/) para que o arquivo não fique bagunçado.

# 4 - Envie as alterações

Após mudar o arquivo dentro de `cursocesar/` volte ao seu terminal de escolha e execute:

`git add *`

`git commit -m "sua mensagem de commit"`

`git push origin nome-da-sua-branch`

Esses comandos enviam suas alterações para a branch criada em sua máquina. 
Um _fork_ sempre tentará comparar o código com o repositório original, logo quando seu código subir para seu fork o GitHub irá identificar automaticamente que você está querendo criar um `pull request` no repositório original. 

Então, se tudo deu certo ao acessar o **[repositório original](https://github.com/mxs2/cursocesar)** você deverá ver o seguinte botão:

<p align="center">
  <img src="https://raw.githubusercontent.com/aprenda-git/pull-request/main/imagens/compare.png">
</p>

# 5 - Crie seu pull request

Alguns repositórios fazem uso de templates para auxiliar as pessoas no processo de elaboração de uma boa mensagem de pull request e para que o mesmo seja aceito.

Clique em `Create pull request` e :tada: parabéns.

Seu pull request foi criado com sucesso. Em breve iremos revisar o conteúdo enviado para nos certificarmos de que o mesmo não contém nada ofensivo e iremos prosseguir com o processo de _merge_.
