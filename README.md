### Server

# Criando uma API RESTful com NodeJS e Express

1. Após criar nosso repositório no gitHub...
    - Abrir terminal (git bash) em uma pasta
    - Clonar o repositório nesta pasta local por meio do comando:
    
    `git clone <endereço do seu repositório>`

    Exemplo para clonar este repositório:

    `git clone https://github.com/AderyuXD/Server.git`
    
2. Abrir a pasta com o VSCode

3. Abrir um terminal no VSCode

4. Vamos criar nosso amigo "package.json"

    _Ele é responsável por gerenciar diversas coisas do nosso projeto_

    `npm init`

4.1 Não esqueçam de criar um arquivo chamado `.gitignore` dizendo para o git ignorar a pasta 
    `node_modules`. Basta adicionar a linha:

    `node_modules`

5. Caso queiram usar o **nodemon**

    _Vimos que toda vez que alteramos os arquivos de código, precisamos derrubar e subir novamente
    o servidor... caso queiram, pode-se utilizar o nodemon para monitorar os ajustes e restartar o 
    nosso servidor. Para instalar:_

    `npm install -g nodemon@1.19.4`

6. Deixando nosso servidor profissa com um arquivo de **config**
    Podemos deixar variáveis de ambiente em um arquivo separado chamado config.json. O pacote config nos 
    permite organizar a configuração da nossa aplicação e usar no nosso projeto.

    `npm install config`
    
7. Vamos instalar nosso amigo **express**

    `npm install express` 

8. Adicionar o **Body-parser**
    O NodeJS em si não sabe converter os dados da requisição para o formato que queremos, o
    body-parser é um middleware capaz de converter o body da requisição para vários formatos. Um
    desses formatos é json, que é o formato que iremos usar...

    `npm install body-parser`

9. Se você quiser, ao invés de rodar nodemon server.js, você pode rodar o servidor via script com npm.
    Para isso, adicione o trecho abaixo no package.json

    ~~~javascript
        "scripts":{
            "test":"echo \"Error: no test specified\" && exit 1",
            "start": "nodemon server.js"
        },
    ~~~

10. Vamos criar uma estrutura de pastas para organizar nossa API:

    ~~~javascript
        ./controllers/ =>  Contém todos controladores da api.
        ./data/ => Contém nossos mocks (dados).
        ./routes/ => Contém as rotas da api.    
    ~~~

11. Vamos criar nosso mock de bandas de rock!