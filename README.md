# my-dotfiles

ÍNDICE:
- SOBRE 
    - Contexto
- SISTEMA
	- Apps
	- Tema / Configs 
	- Papeis de parede
- TERMINAL
	- oh my zsh
	- plugins oh my zsh
	- powerlevel10k
	- tema / fonte
- VSCODE
	- Tema
	- Fonte
	- Extensões
	- Settings.Json
	- Link com Github
- Considerações finais.
	- Contexto
****
## SOBRE

> Cansei de ficar correndo atrás de tudo depois de formatar o PC, então criei esse repositório pra botar um ponto final nessa correria. Aqui, tudo que preciso tá centralizado, desde as configurações até os detalhes mais importantes. Agora, acabou a dor de cabeça pós-formatação, é só dar uma olhada aqui e tá tudo na mão.
&nbsp;
## SISTEMA
### Apps

> Comecei a usar a loja do sistema. É bem simples para instalar programas comuns utilizados diariamente. Simplifica bastante!
&nbsp;

- Brave
![Captura de tela de 2024-02-04 18-30-03](https://github.com/ApenasRyan/my-dotfiles/assets/107745040/6f49d1d4-67b3-4fd6-a60b-ff1c9521e023)
- Spotify
![Captura de tela de 2024-02-04 18-28-59](https://github.com/ApenasRyan/my-dotfiles/assets/107745040/d7b124d5-dca0-4e7a-aabe-e6c36e6890a8)
- Sublime
![Captura de tela de 2024-02-04 18-41-13](https://github.com/ApenasRyan/my-dotfiles/assets/107745040/6de38ad3-1f8f-4b0d-ae84-49b7d24eca78)
- Visual Studio Code
![Captura de tela de 2024-02-04 18-28-31](https://github.com/ApenasRyan/my-dotfiles/assets/107745040/77355c2f-2541-43f3-9fc0-cb6096fae078)


#### Instalações diretas por terminal:

> Para apps como GIT e .NET a instalação por terminal se torna bem mais simples.

- Git
>sudo apt install git
>
 git --version

- .NET
>sudo apt install dotnet-sdk-8.0
>
>dotnet --version

### Tema / Configs

> Em relação ao tema/configurações do sistema operacional não tem nenhum segredo, apenas a mudança para o tema ESCURO e a alteração da cor padrão para ROXO para tirar o aspecto laranja que o Ubuntu tem.

![[Captura de tela de 2024-02-04 18-55-17.png]]

### Papeis de parade

> Links de alguns sites para buscar papeis de parede para utilização na tela de bloqueio e tela principal.
> - https://www.wallpaperflare.com/
> - https://imgur.com/gallery/wCvhF
> - https://www.reddit.com/r/WidescreenWallpaper/?rdt=43131&onetap_auto=true

## TERMINAL
### Oh my zsh

Atualizando pacotes e instalando o ZSH:

>sudo apt install && sudo apt upgrade 
>
 sudo apt install zsh

Configurando ZSH como shell padrão do sistema.

>chsh -s $(which zsh)
>
><I>OBS: será necessário encerrar a seção para que a alteração seja aplicada. </I>

Para instalar os temas do ZSH será necessário instalar o CURL e GIT:

> sudo apt install curl git

Verificando se arquivo criado está vazio, ao instalar o oh my zsh ele virá com informações pre-setadas.

> cat ~/.zshrc

Instalando Zinit para utilização do OH MY ZSH

>bash -c "$(curl --fail --show-error --silent --location https://raw.githubusercontent.com/zdharma-continuum/zinit/HEAD/scripts/install.sh)"
>
>Plugins do ZSH
(instalando zinit que gerencia os plugins).
>
bash -c "$(curl --fail --show-error --silent --location https://raw.githubusercontent.com/zdharma-continuum/zinit/HEAD/scripts/install.sh)"
### Plugins 

Adicionando plugins para o ZSH: 

abrir o arquivo de configurações o zsh
> code ~/.zshrc

Atente-se a adicionar os três plugins no final do texto de configurações do zsh.
> ![[Captura de tela de 2024-02-04 19-38-39.png]]
>zinit light zdharma-continuum/fast-syntax-highlighting
 zinit light zsh-users/zsh-autosuggestions
 zinit light zsh-users/zsh-completions

> 1° - Adiciona coloração permite validar a sintax do comando digitado.
> 2° - Sugestões de comandos utilizados anteriormente.
> 3° - Sugere terminações de sintax para o comando que está sendo digitado.

### Powerlevel10k

Instalação do PowerLevel (deixar o terminal bonitinho)

> git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k

Abrir arquivo de configurações

> code ~/.zshrc

Alterar o valor da variável tema para powerlevel10k/powerlevel10k
> ![[Captura de tela de 2024-02-04 19-45-37.png]]

<i> Reiniciar e configurar de acordo. </i>

>![[Captura de tela de 2024-02-04 19-48-31.png]]

###  Tema / Fonte

Criação de pasta na raiz do sistema para guardar fontes baixadas.
> mkdir ~/.fonts

Baixando fonte e descompactado dentro da pasta criada44

> wget -P ~/.fonts 'https://github.com/ryanoasis/nerd-fonts/releases/download/v2.1.0/BitstreamVeraSansMono.zip' 
> 
> unzip ~/.fonts/BitstreamVeraSansMono.zip -d ~/.fonts

Alterando TEMA do terminal para o tema TANGO ESCURO, adicionando transparência e alterando para fonte baixada anteriormente.

>![[Captura de tela de 2024-02-04 19-52-43.png]]
...

## VSCODE

### Tema

> Min Theme

### Fonte

> JetBrains Mono

### Extensões 

> C# DevKit (Para conseguir usar o vscode para utilizar dotnet).
> .NET compiler (Compilador padrão .net).
> Mono Debug (Permitir debug no vscode).
> Symbols (Adiciona icones em todos os arquivos do projeto).
> Prettier (Concatenação automática)
> LiveServer (Aplica as alterações no cod. na pagina automaticamente).
>
>![[Captura de tela de 2024-02-04 20-10-25.png]]
> <i>...<i/>


### Settings.json

Aqui estão algumas configurações particulares para simplificar algumas coisas e remover outras. abaixo uma relação de cada alteração no VSCODE.

    {
    "symbols.hidesExplorerArrows": false,
    
    "workbench.iconTheme": "symbols", 
    //temas para ícones
    
    "workbench.colorTheme": "Min Dark", 
    //tema utilizado
    
    "editor.fontFamily": "JetBrains Mono", 
    //fonte utilizada 
    
    "editor.fontLigatures": true, 
    //ligaturas de fonte que tem
    
    "editor.fontSize": 14, 
    //tamanho da fonte
    
    "editor.lineHeight": 1.8, 
    //espaço entre linhas
    
    "workbench.startupEditor": "newUntitledFile", 
    //vscode sempre inicia com um arquivo limpo.
    
    "editor.renderLineHighlight": "gutter", 
    //marcação apenas no numero e não na linha inteira.
    
    "explorer.compactFolders": false, 
    //modo de compactação fica feio sem.
    
    "breadcrumbs.enabled": false 
    //remove caminho para o arquivo abaixo do nome
    }

> ![[Captura de tela de 2024-02-04 20-13-17.png]]
> <i> ... <i/>


### Linkando ao Github
> git config --global user.name "Um caba lá"
> git config --global user.email umcabala@exemplo.br

...

## CONSIDERAÇÕES FINAIS
> Em resumo, criar e manter este repositório para meus dotfiles foi uma mão na roda facilitando a re-criação do meu ambiente sempre que acontecer uma formatação.

---
