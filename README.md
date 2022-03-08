# conversao-distancia

- Utilizei a imagem 3.9-slim-buster (115MB) por ser bem menor que a 3.9.1 (885MB)
- Criei a pasta onde iria copiar a aplicação
- Copiei o requirements.txt para a pasta da aplicação
- Instalei as dependências do projeto contidas no requirements.txt
- Copiei o restante dos arquivos da aplicação
- Executei a aplicação como um módulo ("-m") e também instrui o docker a disponibilizar o container externamente ("--host=0.0.0.0").
  Pois tentei usar o CMD [ "python3", "./app.py"] e a aplicação não ficava acessível no browser

# Comandos
## Construção da imagem
`docker build -t prhirata/conversao-distancia:desafio .`

## Execução do container
`docker container run -d -p 8080:5000 --name conversao-distancia prhirata/conversao-distancia:desafio`