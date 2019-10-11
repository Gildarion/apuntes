# APUNTES CLI GITHUB

## Crear repo desde CLI
```
curl -u 'USER' https://api.github.com/user/repos -d '{"name":"REPO"}'
```
## Creacion de repo
```
git init
git remote add origin https://github.com/<username>/reponame.git
git add .
git commit -m "mensaje"
git pust -u origin master
```

## Obtener todos los repos de un user
```
curl -s https://api.github.com/users/<username>/repos | grep html_url
```
