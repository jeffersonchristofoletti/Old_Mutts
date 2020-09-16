# Os primeiros passos

1. Abra o VSCode; 
2. Crie uma pasta no diretório raiz, com o nome de sua preferência, desde que sem caracteres especiais ou espaços;
3. Abra a pasta no VSCode clicando em Arquivo -> Abrir Pasta ou CTRL+K CTRL+O e selecione a pasta; 
4. Abra um novo terminal. Pode ser clicando com o botão direito do mouse sobre o Explorador do VSCode ou Exibir -> Terminal (no menu) ou ainda CTRL+` ;
5. Defina o Bash como shell padrão. Clique no menu dropdown 1:cmd -> Selecionar Shell Padrão e no alto da tela selecionar Git Bash;
6. Reinicie o terminal para carregar a mudança.

# Configuração Inicial do Git

Os comandos a seguir devem ser digitados no terminal:

1. git init <- Criará um diretório oculto na pasta a ser monitorada pelo Git. É o que chamamos de inicialização
2. Dê um fork no repositório do grupo de estudo. Clique em:
   https://github.com/cyntiagoulart/Old_Mutts.git
   No canto superior direito da tela, clique no botão Fork. Isso criará uma cópia do repositório nos seus repositórios. É o que chamamos apenas de fork.
3. Clone a cópia "forkada" repositório do grupo de estudo com o comando:
   git clone LINK DO SEU FORK
   Para pegar o link clique no botão verde Code e a seguir copie o link ou clique no ícone de prancheta.
4. Configure o seu usuário com o comando:
   git config --global user.name "SEU NOME" <-- o seu nome entre aspas e pode ter espaço
   git config user.name "SEU NOME" <- se a máquina for compartilhada prefira o comando local
5. Configure o seu e-mail com o comando:
   git config --global user.email "SEU E-MAIL" <-- o e-mail usado no Github
   git config user.email "SEU E-MAIL" <- se a máquina for compartilhada prefira o comando local
6. Configure o editor de texto padrão do Git com o comando:
   git config --global core.editor 'code --wait'
7. Cheque as suas configurações com o comando:
   git config --list

# Em caso de dúvida...

1. Digite:
   git --help

# Crie a sua branch

Branches são ramificações do repositório principal, que chamamos de master. Você pode abrir tantas quantas branches quiser e, eventualmente, se as modificações propostas forem aceitas, elas serão incorporadas à master.

1. Digite:
   git checkout -b NOME DA BRANCH <-- Eu sugiro que seja o seu nome, mas pode ser qualquer outro nome que siga a convenção de nomenclatura do projeto.
2. Liste as branches do repositório com o comando:
   git branch -a
3. Mude de branch com o comando:
   git checkout NOME DA BRANCH <-- Pode ser qualquer branch do projeto ou a master

# Vamos commitar?

Após criar diretórios e arquivos é hora de commitar. Para isso devemos seguir alguns passos.

O Git tem cinco áreas distintas, cada qual com a sua função:
1. (local) Stash:
   É o seu esconderijo local onde você armazenas códigos inacabados. Não usaremos essa opção, por enquanto.
2. (local) Cópia/área de trabalho:
   É o local atual do trabalho, o seu diretório monitorado.
3. (local) Stage, também conhecido como staging area:
   É para onde mandamos os arquivos "prontos" para serem commitados com os seguintes comandos:
   git add . <-- adiciona todos as alterações do diretório
   git add nome.extensão <-- adiciona arquivo específico
   git add nome/ <-- adiciona diretório específico
   git status <-- verifica o status dos arquivos (untracked, modified, added)
4. (local) Repositório local:
   É onde os seus arquivos estão relativamente seguros.
   git commit -m "Mensagem de commit bem caprichada porque a bola de cristal está no conserto."
   git log <-- mostra o log de todos os commits de todos os colaboradores em todas as branches
5. (remoto) Repositório remoto:
   É o momento que mandamos tudo que foi commitado para o repositório remoto com o comando:
   git push -u origin NOME DA BRANCH
   git push <-- se for commitar direto na master, estando na master.


   
    




