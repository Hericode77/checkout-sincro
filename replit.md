# Sincro Pay - Checkout com Mercado Pago

## Visão Geral
Sistema de checkout personalizado com integração Mercado Pago Checkout Pro.

## Estrutura do Projeto
```
├── src/
│   ├── server.js           # Servidor Express principal
│   ├── config/
│   │   └── mercadopago.js  # Configurações do Mercado Pago
│   └── routes/
│       └── webhook.js      # Endpoint para webhooks do MP
├── public/
│   ├── index.html          # Landing page com botão Comprar
│   ├── obrigado.html       # Página de agradecimento
│   └── css/
│       └── styles.css      # Estilos globais
└── package.json
```

## Como Configurar

### 1. Link do Checkout Mercado Pago
Edite o arquivo `public/index.html` e substitua:
```html
href="https://link.mercadopago.com.br/SEU_LINK_AQUI"
```
Pelo seu link do Mercado Pago Checkout Pro.

### 2. Link de Entrega do Produto
Edite o arquivo `public/obrigado.html` e substitua:
```html
href="https://seu-link-de-entrega.com/produto"
```
Pelo link de acesso ao seu produto.

### 3. Configurar Webhook no Mercado Pago
No painel do Mercado Pago, configure a URL do webhook:
```
https://SEU_DOMINIO/webhook
```

## Endpoints
- `/` - Landing page de vendas
- `/obrigado` - Página de agradecimento pós-pagamento
- `/webhook` - Recebe notificações do Mercado Pago
- `/webhook/test` - Testa se o webhook está funcionando

## Tecnologias
- Node.js + Express
- HTML5 + CSS3
- Mercado Pago Checkout Pro

## Alterações Recentes
- 10/12/2025: Criação inicial do projeto
