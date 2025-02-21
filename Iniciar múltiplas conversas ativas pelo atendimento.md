No #flexuc/atendimento, na parte de buscar_contato/busca_avancada_de_contatos, é necessário que seja possível filtrar por #flexuc/entidade/conta.

Será criada uma nova #rota/flex_chat_ts/whatsapp para receber um array e enviar em segunda thread as mensagens.

#task: https://app.clickup.com/t/86a56g3q5

#rota/url/flex-chat-integration/api/send-active/multiple/text

```ts
{
  "contactId": 762,
  "usrSocketId": "pZ7zfJsIih3SunWqAAZj",
  "messageData": {
    "id": "4995ab10-167a-4693-9663-0b4eb8506c8d",
    "params": [
      "leandro",
      "a g4!"
    ],
    "message": "Olá leandro, Seja bem vindo a g4!."
  },
  "queue": "Suporte",
  "channelId": "2ee733da-9c5f-4eb3-9523-c8a927873316",
  "userLogin": "leandro.felix",
  "clients": [
    {
      "name": "Leandro Felix",
      "phone": "8892285712"
    },
    {
      "name": "Caio",
      "phone": "88993552505"
    }
  ]
}
```