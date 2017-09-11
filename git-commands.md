#### [Repositório]

Cria um repositório git para acesso remoto

```console
$ git –bare init
```

#### [Fetch]

Buscando as novidades do repositório remoto antes de enviar suas modificações

```console
$ git fetch origin master
```

#### [Commits]

Adiciona todas as alterações, inclusive arquivos novos,  para commit

```console
$ git add -A
```

Consolida as alterações adicionadas ao commit, com uma descrição

```console
$ git commit -m ‘commit descritpion’
```

Adiciona e consolida as alterações, mas não adiciona novos arquivos

```console
$ git commit -a -m “commit description”
```


#### [Branchs]

Cria um branch novo apartir do branch atual

```console
$ git branch name_branch
```

Renomear um branch

```console
$ git branch -m name_old_branch name_new_branch
```

Deleta um branch localmente atualizado

```console
$ git branch nomebranch -d
```

Deleta branch localmente independente da situação dele

```console
$ git branch nomebranch -D
```

Excluir branch remoto

```console
$ git push origin :nome_do_branch
```

Lista branchs remotos

```console
$ git branch -a
```

Realiza o push e sobrescreve o branch do servidor pelo seu branch local

```console
$ git push –force origin branchremoto
```

Remove localmente todos os branches que já foram removidos remotamente - espécie de sync

```console
$ git remote prune origin
```

Cria um branch remoto baseado em um branch local

```console
$ git push origin branch_local:branch_remoto
```

Cria um branch remoto baseado em um branch local, mantendo os branches vinculados 

```console
$ git push -u origin branch_local:branch_remoto
```

Vincula um branch local a um branch remoto (caso ainda não exista esta vinculação)

```console
$ git branch –set-upstream meu_branch origin/meu_branch
```

Para renomear branch

```console
$ git branch -m old_branch new_branch
```

#### [Log]

Mostra o que foi alterado em cada commit em um arquivo

```console
$ git log - p nome_arquivo
```

Mostra apenas commits e um autor específico

```console
$ git log –author=Name Author
```

Mostra quem foi o autor de cada linha de um arquivo

```console
$ git blame nome_arquivo
```

Desfaz as alterações consolidadas no último commit

```console
$ git reset –hard HEAD^
```

Desfaz as alterações consolidadas depois do commit específicado

```console
$ git reset –hard SHA1DOCOMMIT
```

#### [Whatchanged]

Mostra quais arquivos foram alterados em cada commit

```console
$ git whatchanged
```

Mostra quais arquivos foram alterados em cada commit de um autor específico

```console
$ git whatchanged –author=Name Author
```

#### [Checkout]

Desfaz as alterações não consolidadas no branch atual

```console
$ git checkout -f
```

Desfaz as alterações não consolidadas em um arquivo

```console
$ git checkout nome_arquivo
```

Limpa um branch e realiza o pull do servidor para um único branch

```console
$ git checkout -b nomeDoBranch origin/nomeDoBranch
```

#### [Ignore]

Para ignorar arquivos já existentes em seu projeto

```console
$ git update-index –assume-unchanged <filename(s)>
```

Para “designorar” arquivos ignorados em seu projeto

```console
$ git update-index –no-assume-unchanged <filename(s)>
```

Para listar arquivos já ignorados em seu projeto

```console
$ git ls-files -v | grep “h ”
```
O espaço depois do ‘h’ é obrigatório

#### [Tags]

Realiza o push e envia as tags criadas para o remote

```console
$ git push –tags
```

Remove uma tag localmente

```console
$ git tag -d tag_name
```

Remove tag já enviada ao servidor - 12345 é a tag

```console
$ git push origin :refs/tags/tag_name
```

Envia uma tag criada localmente para o remote

```console
$ git push origin tag_name
```

#### [Revert]

Para reverter um arquivo para uma determinada versão

```console
$ git checkout SHA1^ — <filename>
```

Para reverter para um determinado commit criando um novo commit

```console
$ git revert SHA1
```

#### [Reset]

Para reverter para um determinado commit

```console
$ git reset –hard SHA1
```

Para reverter o último commit

```console
$ git reset –hard HEAD^
```

#### [Stash]

Move as alterações não adicionadas ao commit para memoria tempoária e limpa o branch das alterações. Este comando deve ser usada quando precisarmos mudar de branch sem commitar as mudanças atuais.

```console
$ git stash
```

Mostra os stashs criados, exemplo:

```console
$ git stash list
```

Retorna as alterações do stash 1

```console
$ git stash apply stash@{1}
```

