Para saber mais:

- [Git log cheatsheet](http://devhints.io/git-log)
- `git init --bare` para inicializar um repositório puro (apenas com histórico de alterações dos arquivos)
- `git remote add nome_remoto <endereço/url>` para definir repositório remoto (local, rede e etc)
- `git tag -a vX.X.X -m 'mensagem'` insere tag/marcação. Posteriormente realizar _push_ do _branch_ e _tag_
- `git rebase -i HEAD~X` informando a quantidade de commits ou `git rebase -i XXXXXXXX` informando o commit anterior aos commits que deseja unir
- `git cherry-pick XXXXXXX` traz o commit especificado de outro branch para o branch atual