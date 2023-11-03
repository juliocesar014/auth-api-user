### specs

- Go 1.21
- Postgresql 12


### run docker container

```shell
git clone git@github.com:juliocesar014/auth-api-user.git
```
```shell
cd auth-api-user
```


```shell
docker compose up 
```



### methods

**- [GET all users] localhost:8000/users**
```shell
curl http://localhost:8000/users

```

**- [POST user] localhost:8000/users**

```shell
curl -X POST -H "Content-Type: application/json" -d '{
  "name": "first name",
  "email": "name@example.com",
  "password": "example#123"
}' http://localhost:8000/users
```

**- [GET users by id] localhost:8000/users/{id}**
```shell
curl http://localhost:8000/users/1

```

**- [PUT user] localhost:8000/users/{id}**
```shell
curl -X PUT -H "Content-Type: application/json" -d '{
  "name": "new name",
  "email": "newemail@example.com",
  "password": "newpassword#123"
}' http://localhost:8000/users/1
```

**- [DELETE user] localhost:8000/users/{id}**
```shell
curl -X DELETE http://localhost:8000/users/1
```

**- [POST login] localhost:8000/login**
**This route is used for user authentication. The client must provide a JSON object containing a valid email and password. If the credentials are correct, the route returns a JWT access token, which can be used to authenticate and authorize the user in other parts of the application.**
```shell
curl -X POST -H "Content-Type: application/json" -d '{
  "email": "name@example.com",
  "password": "example#123"
}' http://localhost:8000/login
```

**- [GET health status api] localhost:8000/health**
```shell
curl http://localhost:8000/health

```

### partial architecture

![image](https://github.com/juliocesar014/auth-api-user/assets/105388145/3058cfa4-1194-4e50-99c3-371fbe6ec3cd)

