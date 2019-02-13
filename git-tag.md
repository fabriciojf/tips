# Trabalhando com Tags
**Tags** são usadas para definir **Rótulos** de versões nos repositórios git

## Gerando um Rótulo (Versão)

Para gerar uma **Tag** você precisará informar qual a revisão de repositório você quer referenciar. Para saber a referência do repositório utilize o comando **git log --pretty=oneline**, logo após o comando git tag com o id do commit desejado e submeta tudo ao repositório principal.

```console
$ git log --pretty=oneline
$ git tag -a 1.0.0 28a4b531bb25b6536060bbe827d23c0d5b4dc1dc
$ git push origin master --tags
```

## Listando tags criadas

```console
$ git tag
$ git tag -l
```

## Analisando uma Tag específica

```console
$ git show 1.0.0
```

## Clonando uma Tag (Versão)

```console
$ git clone -b 1.0.0 https://USER@DOMAIN/FOLDER/PROJECT.git FOLDER
```

## Revertendo a versão do código para uma Tag específica

```console
$ git checkout tags/1.0.0
```

## Gerando um Rótulo (Versão)

Para gerar uma **Tag** você precisará informar qual a revisão de repositório você quer referenciar. Para saber a referência do repositório utilize o comando **git log --pretty=oneline**, logo após o comando git tag com o id do commit desejado e submeta tudo ao repositório principal.

```console
$ git log --pretty=oneline
$ git tag -a 1.0.0 28a4b531bb25b6536060bbe827d23c0d5b4dc1dc
$ git push origin master --tags
```
