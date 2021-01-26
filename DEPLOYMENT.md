# DEPLOYMENT

## Pre-releases
...edit...
```
$ git tag $(date +%Y).$(date +%m)-rc1
$ earthly +docker
```

## Release from `git tag`
If a current `git tag` is available, the `VERSION` will be inferred.
```
$ git tag -a 2021.01 -m "Version 2021.01"
$ earthly --push --no-cache +docker
```

## Release from `--build-arg`
If an old `git tag` is updated, for example, to incorporate `apt upgrade` from `Dockerfile`
```
$ earthly --build-arg VERSION=2021.01.02 --push --no-cache +docker
```
