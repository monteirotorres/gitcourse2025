# Dicionário de Conceitos
- Git: Um software de versionamento que cria uma linha do tempo com as várias versões dos arquivo de um projeto. 

- GitHub: Base de dados que realiza o backup de todas as linhas do tempo.
  

## Áreas conceituais
### Área de desenvolvimento
- Pasta onde foi dado o comando git init
### Repositório local
- Pasta invisível contendo os arquivos do git (a linha do tempo)
- Arquivos importantíssimos para o versionamento. DONT touch.
### Staging área
- Área de transição. Guarda informações de quais arquivos serão adicionados ao controle versionamento.
- Arquivos podem estar:
    - Tracked
        - Staged
        - Unstaged
        - Unchanged
    - Untracked
### Repositório remoto
- Backup no Github 

## Hunk headers
- São usados em git diff e git show para mostrar os blocos de mudanças realizadas com a seguinte sintaxe:
`@@ -<start_line_old>,<num_lines_old> +<start_line_new>,<num_lines_new> @@`

## Para trabalhar em colaboração
- É ncessário convidar um colaborador pela plataforma GitHub, na aba __settings__ --> Collaborators
- O colaborador receberá um email e deverá aceitar a colaboração
- Após isso, podemos clonar o diretório e trabalhar normalmente com ele
`git clone git@github.com:noemyppereira/noemy.git` 
`git add`
`git commit`
`git push` 
- Para ver se há modificações entre a versão local e a remota, utilizamos `git pull`

## Branches
- Branches permitem ramificações na linha temporal.
- Arquivos que aparecem na pasta são apenas aqueles do branch atual
- Pull traz todas as atualizações
- O Push só empurra o branch
- Não há limites de número de branches



test