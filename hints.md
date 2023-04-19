# Mav71

## migrations

```
cd /tmp \
  && curl -L https://github.com/golang-migrate/migrate/releases/download/v4.15.2/migrate.linux-amd64.tar.gz | tar xvz \
  && rm -rf LICENSE README.md \
  && mv migrate /go/bin
  
migrate create -ext=mysql -dir=sq/migrations -seq init
```

```
go install github.com/kyleconroy/sqlc/cmd/sqlc@latest

sqlc generate ### mapeia os migrations e queries e cria a camada de modelo
```

## Chat GPT

criar chave na OpenAi nesse [link]https://platform.openai.com/account/api-keys

## compila lib rust

docker run --rm --user "$(id -u)":"$(id -g)" -v "$PWD"/tiktoken-cffi:/usr/src/myapp -w /usr/src/myapp rust cargo build --release

