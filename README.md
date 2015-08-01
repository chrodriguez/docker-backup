# Backup gem docker container

This container can be used as command line backup gem

## Generate configurarion

```
docker run -it --rm --volumes-from vdr -v $HOME/Backup:/root/Backup  chrodriguez/backup generate:config
```

## Generate model

```
docker run -it --rm --volumes-from <some-container> -v $HOME/Backup:/root/Backup  chrodriguez/backup generate:model -t my_backup --archives --storages='dropbox' --compressor='bzip2' --notifiers='mail'
```

## Run backup

```
docker run -it --rm --volumes-from vdr -v $HOME/Backup:/root/Backup  chrodriguez/backup perform -t my_backup
```
