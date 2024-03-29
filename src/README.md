## Comandos:

- `git init --bare` para inicializar um repositório puro (apenas com histórico de alterações dos arquivos)
- `git remote add nome_remoto <endereço/url>` para definir repositório remoto (local, rede e etc)
- `git tag -a vX.X.X -m 'mensagem'` insere tag/marcação. Posteriormente realizar _push_ do _branch_ e _tag_
- `git rebase -i HEAD~X` informando a quantidade de commits ou `git rebase -i XXXXXXXX` informando o commit anterior aos commits que deseja unir
- `git cherry-pick XXXXXXX` traz o commit especificado de outro branch para o branch atual
- `git bisect` busca de commits
    - `git bisect start` inicia a busca de commits
    - `git bisect bad HEAD` estado final da busca
    - `git bisect good XXXXXXX` estado inicial da busca
    - `git bisect bad` negar resultado encontrado e continuar a busca
    - `git bisect good` aceitar resultado encontrado
    - `git bisect reset` voltar para HEAD e mediante commit encontrado anteriormente, é possível aplicá-lo com `git revert XXXXXXX`
- `git show XXXXXXX` exibir modificações implementadas no commit
- `git blame XXXXX.xpto` exibir lista detalhada de alterações no arquivo especificado
- `chmod u+x pre-commit` conceder permissão para execução do shell script em plataforma não Windows

## Ferramentas:

- [Git Cola](https://git-cola.github.io/downloads.html)
- [GitHub Desktop - Windows ou macOS](https://desktop.github.com/) ou [GitHub Desktop - Linux](https://github.com/shiftkey/desktop)
- [Git Kraken](https://www.gitkraken.com/download)

## Para saber mais:

- [Git log cheatsheet](http://devhints.io/git-log)
- [Git Hooks](https://githooks.com/)
- Exemplo hook **post-receive**:
```
#!/bin/sh
git --git-dir={caminho_da_pasta_do_servidor} --work-tree={caminho_da_pasta_web} checkout -f
```