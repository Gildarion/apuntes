# CONFIGURAR SSH

## DESDE CLIENTE
```
ssh-keygen -t rsa -C "<mail>"
scp -p id_rsa.pub remoteuser@remotehost
```

## DESDE SERVIDOR
```
mkdir ~/.ssh
chmod 700 ~/.ssh
cat id_rsa.pub >> ~/.ssh/authorized_keys
chmod 600 ~/.ssh/authorized_keys
mv id_rsa.pub ~/.ssh
systemctl restart ssh
```

## DESDE CLIENTE
borramos la clave publica
```
rm id_rsa.pub
```
Si tenemos un fichero especifico para el host

`vim ~/.ssh/config`

|**~/.ssh/config**             |
|------------------------------|
| Host <remotehos>             |
|  IdentityFile /path/a/id_rsa |
|------------------------------|
