#APUNTES CLI GITHUB

##Crear repo desde CLI
```
curl -u 'USER' https://api.github.com/user/repos -d '{"name":"REPO"}'
```
##Obtener todos los repos de un user
```
curl -s https://api.github.com/user/<usernamer>/repos | grep html_url
```
