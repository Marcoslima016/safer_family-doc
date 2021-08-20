

##Enviar push simples com base no token push. 

O link abaixo serve para enviar pushs simples composto pela mensagem "teste". Para enviar o push, especifique o token push do dispositivo, além do id do app que vai receber o push. 

```
.
https://www.segcontrole.com.br/safer/v1/teste_push.php?<TOKEN_PUSH>&tipo=1&app_id=<APP_ID>
```

---

##Enviar push detalhado. 

O Link abaixo envia um push onde é possivel configurar a mensagem enviada além d epoder setar o push como crítico. 

```link
.
https://www.segcontrole.com.br/safer/v1/teste_push.php?user_id=228&tipo=2&app_id=2&msg="Mensagem!"
```