# Dante-server

### To built:
```sh
sudo docker build --build-arg USER_NAME=username --build-arg PASSWORD=userpass -t danted .
```

### To start:
```sh
sudo docker run -d -p --name danted --restart=always danted
```
