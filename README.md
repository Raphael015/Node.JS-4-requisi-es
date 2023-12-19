# Projeto Node.js + express -  recebendo quatro tipos de requisições e respondendo cada uma com strings diferentes 

## Configurações

1. **Certifique-se de ter o Node.js instalado no seu sistema.**

   Se você ainda não tem o Node.js instalado, você pode baixá-lo [aqui](https://nodejs.org/). Escolha a versão recomendada para a sua plataforma e siga as instruções de instalação.

2. Instale o pacote Express usando o npm:

    ```bash
    npm install express
    ```

## Iniciando a criação do projeto.


1. Crie um novo diretório para o projeto:

    ```bash
    mkdir meu-projeto
    cd meu-projeto
    ```

2. Crie um arquivo chamado `app.js` e adicione o seguinte código:

    ```javascript
    // Importando a biblioteca Express
    const express = require('express');
    
    // Criando uma instância do aplicativo Express
    const app = express();
    
    // Rota para requisições do tipo GET
    app.get('/', (req, res) => {
      res.send('Resposta para requisição GET');
    });
    
    // Rota para requisições do tipo POST
    app.post('/', (req, res) => {
      res.send('Resposta para requisição POST');
    });
    
    // Rota para requisições do tipo PUT
    app.put('/', (req, res) => {
      res.send('Resposta para requisição PUT');
    });
    
    // Rota para requisições do tipo DELETE
    app.delete('/', (req, res) => {
      res.send('Resposta para requisição DELETE');
    });
    
    // Definindo a porta em que o servidor irá escutar
    const PORT = 3000;
    
    // Iniciando o servidor na porta especificada
    app.listen(PORT, () => {
      console.log(`Servidor Express rodando na porta ${PORT}`);
    });

    ```

3. No terminal, execute o seguinte comando para iniciar o servidor:

    ```bash
    node app.js
    ```

4. Prontinho, agora você pode acessar as diferentes rotas através de um navegador ou ferramenta de API.

   - Para a requisição GET: http://localhost:3000/
   - Para a requisição POST: Envie uma requisição POST para http://localhost:3000/
   - Para a requisição PUT: Envie uma requisição PUT para http://localhost:3000/
   - Para a requisição DELETE: Envie uma requisição DELETE para http://localhost:3000/
