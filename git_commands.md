## Git Commands

### Starting
- Inicializando o repositório local
`git init`
- Listando as configurações
`git config --global --list`
- Definindo o nome de usuário na configuração **local** do Git
`git config --global user.name "Pedro Torres"`
- Definindo o email na configuração **local** do Git
`git config --global user.email "monteirotorres@gmail.com"`
    

### Commiting
- Adicionando arquivos à "staging area" 
`git add __filename__`
- "Comprometendo" os arquivos com as mudanças, i.e. gravando um ponto na linha do tempo
    - A mensagem relevante deve conter por que, como, efeitos, limitações
    - Às vezes é melhor juntar arquivos relacionados em um mesmo commit e separar arquivos não relacionados em arquivos diferentes
  
    `git commit -m "__mensagem relevante__"`

### Miscellaneous
- Checando o estado dos arquivos em relação ao versionamento
`git status`

