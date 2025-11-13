## Git Commands

### Starting local
- Inicializando o repositório local
`git init`
- Listando as configurações
`git config --global --list`
- Definindo o nome de usuário na configuração **local** do Git
`git config --global user.name "Pedro Torres"`
- Definindo o email na configuração **local** do Git
`git config --global user.email "monteirotorres@gmail.com"`

### Inicializando acesso ao repositório remoto
- Git não permite mais fazer operações só com username e senha. É preciso criar uma chave ssh e conectá-la ao repositório com os comandos a seguir:
    - Criando a ssh-key 
    `ssh-keygen -t ed25519 -C "monteirotorres@gmail.com"`
        - Fazer uma senha para acessar a ssh-key futuramente
        - Em __https://github.com/settings/keys__, fazer o upload do arquivo id_ed25519.pub (tem que dar um nome qualquer)
    - Conectando a chave ao repositório (se continuar pedindo senha)
    `git remote set-url origin git@github.com:monteirotorres/repo.git`
    

### Commiting
- Adicionando arquivos à "staging area" 
`git add __filename__`
- "Comprometendo" os arquivos com as mudanças, i.e. gravando um ponto na linha do tempo
    - A mensagem relevante deve conter por que, como, efeitos, limitações
    - Às vezes é melhor juntar arquivos relacionados em um mesmo commit e separar arquivos não relacionados em arquivos diferentes
  
    `git commit -m "__mensagem relevante__"`

### Pushing 
Após colocar os arquivos na staging area com `git add` e se comprometer com as mudanças com `git commit`, podemos fazer o backup na base GitHub.
- Ligando o diretório remoto ao local
`git remote add origin https://github.com/monteirotorres/gitcourse2025.git`
- Fazendo o primeiro push do repositório
`git push --set-upstream origin master`
- Nas próximas vezes
`git push`

### Pulling (sincronizando da nuvem)
Podemos sincronizar o repositório local com o que há no GitHub com o comando:
`git pull`

### Clonando um repositório remoto
Podemos restaurar toda a informação do repositório remoto fazendo um clone
    `git clone git@github.com:monteirotorres/repo.git`
    - Vai surgir uma pasta local com o nome do repositório remoto

### Desfazendo um commit
- Git reset é perigoso pois exclui completamente todas as suas versões até o ponto especificado.
`git reset --hard HEAD~1`
- Git revert não exclui as versões, mas cria uma nova igual àquela desejada
`git revert HEAD~1`
ou
`git revert __<hash#>__`

### Resolvendo conflitos
- Quando o push falhar por conta de conflito, para resolver precisamos primeiro realizar um `git pull`
- Nesse momento, os arquivos serão mostrados com decoradores indicando as diferenças entre as versões
- Devemos então editar o arquivo conforme desejado, salvar e então **__add -> commit -> push__**

### Miscellaneous
- Checando o estado dos arquivos em relação ao versionamento
`git status`
- Verificando o histórico de commits
`git log`
    - Aqui podemos adicionar as opções
        - -p --> mostra as comparações também
        - --reverse --> inverte a linha do tempo
        - --oneline --> mostra informações resumidas em uma linha
        - -n __nº__ --> mostra apenas os n últimos commits
        - --abrev-commit --> abrevia o hash
- Comparando duas versões
`git diff <oldhash> <newhash>`
    - Aqui a ordem faz a diferença.
- Renomeando um arquivo de forma adequada
`git mv <oldname> <newname>`

