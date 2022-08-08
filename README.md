# Configurações Globais

### Configurar para abrir os  arquivos no VS Code.
```
git config --global core.editor code
```

### Acessar o arquivo de configurações.
```
git config --global --edit
```

### Para resolver problema quando é executado o rebase e a tela fica em branco no VS Code.
```
[core]
    editor = code --wait
```

### Configurando alias.
```
[alias]
    c = !git add --all && git commit -m
    s = !git status -s
    l = !git log --pretty=format:'%C(blue)%h%C(red)%d %C(white)%s - %C(cyan)%cn, %C(green)%cr'
    amend = !git add --all && git commit --amend --no-edit
    count = !git shortlog -s --grep
```
- Exemplos de utilização
```
git c "commit com alias"
git s
git l
git amend
git count test
git count feat
git count fix
git count chore
git count docs
```
- amend = Permite juntar o commit atual com o anterior
- count = Gerar estatísticas do projeto

### Enviar somente tags anotadas no push. Não é recomendado enviar tags normais no projeto.
```
[push]
    followTags = true
```
- Exemplos de utilização
```
git tag -a "1.0.0" -m "1.0.0"
```


