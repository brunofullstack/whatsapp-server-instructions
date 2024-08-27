Enviar uma requisição POST para o endpoint `http://195.200.2.140:4200/send-message` com o corpo JSON fornecido, você pode usar várias ferramentas e métodos. Aqui estão alguns exemplos usando diferentes abordagens:

### Usando cURL no Terminal
```bash
curl -X POST http://195.200.2.140:4200/send-message \
     -H "Content-Type: application/json" \
     -d '{
           "name": "Cliente Teste",
           "phoneNumber": "5598984897435",
           "message": "Olá, esta é uma mensagem automatizada! No corpo desta mensagem deve conter a nova senha gerada bem como as demais instruções"
         }'
```

### Usando Fetch API em JavaScript
```javascript
fetch('http://195.200.2.140:4200/send-message', {
  method: 'POST',
  headers: {
    'Content-Type': 'application/json',
  },
  body: JSON.stringify({
    name: 'Cliente Teste',
    phoneNumber: '5598984897435',
    message: 'Olá, esta é uma mensagem automatizada! No corpo desta mensagem deve conter a nova senha gerada bem como as demais instruções'
  }),
})
.then(response => response.json())
.then(data => console.log(data))
.catch(error => console.error('Erro:', error));
```

### Usando Axios em JavaScript
```javascript
const axios = require('axios');

axios.post('http://195.200.2.140:4200/send-message', {
  name: 'Cliente Teste',
  phoneNumber: '5598984897435',
  message: 'Olá, esta é uma mensagem automatizada! No corpo desta mensagem deve conter a nova senha gerada bem como as demais instruções'
})
.then(response => console.log(response.data))
.catch(error => console.error('Erro:', error));
```

### Usando Postman
1. Abra o Postman.
2. Selecione o método `POST`.
3. Insira a URL `http://195.200.2.140:4200/send-message`.
4. Vá para a aba `Body` e selecione `raw` e `JSON`.
5. Cole o JSON fornecido:
   ```json
   {
     "name": "Cliente Teste",
     "phoneNumber": "5598984897435",
     "message": "Olá, esta é uma mensagem automatizada! No corpo desta mensagem deve conter a nova senha gerada bem como as demais instruções"
   }
   ```
6. Clique em `Send`.

Escolha a abordagem que melhor se adapta ao seu ambiente ou necessidade. Se precisar de mais ajuda, é só avisar!
