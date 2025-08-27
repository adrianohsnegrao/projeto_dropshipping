# 📄 Resumo do Projeto

**Nome (provisório):** projeto_dropshipping  

**Descrição breve:**  
Uma plataforma de e-commerce minimalista focada em dropshipping, inicialmente construída como MVP (Produto Mínimo Viável). O objetivo é validar o modelo de negócio rápido, permitindo cadastrar produtos, processar pedidos e integrar checkout de forma simples.

---

# 🛠️ Tecnologias

## Backend
**Laravel (PHP 8.2+)**
- Rápido para criar APIs RESTful.
- Já vem estruturado para autenticação, filas e escalabilidade.
- Grande ecossistema de pacotes prontos (ex: Cashier para pagamentos).

## Frontend
**React**
- Maior comunidade, mais recursos para e-commerce (Next.js pode ser usado depois).
- Ótima integração com bibliotecas modernas de UI e marketing (Tailwind, Shadcn, etc).
- Mais amigável se você pensa em escalar para SSR/SEO no futuro.

> O Vue também é excelente, mas pensando em mercado + recursos, React dá mais flexibilidade agora.

## Banco de Dados
**MySQL/MariaDB**
- Mais do que suficiente para o início.
- Estrutura simples: produtos, pedidos, usuários.

> NoSQL (MongoDB) pode ser considerado futuramente caso queira escalar para catálogos gigantescos (milhões de produtos). Mas para o MVP, MySQL resolve perfeitamente.

## Cache / Performance
**Redis → não necessário neste momento.**
- Só vale a pena incluir se você for ter alto tráfego, filas de pedidos, ou precisar de cache agressivo.
- Para o MVP, mantenha simples com MySQL.

## Infraestrutura
**Docker**
- Padroniza o ambiente (Laravel + React + MySQL rodando juntos).
- Facilita deploy futuro em VPS ou cloud.

---

# 📌 Estrutura Inicial do Projeto


```text
/dropshipping-loja
    /backend (Laravel API)
    /frontend (React)
    docker-compose.yml
    /db (MySQL volume)
```

---

# 🚀 Roadmap curto

- **Semana 1** – Subir Laravel no Docker, criar API `/products`.  
- **Semana 2** – Subir React no Docker, consumir API e exibir produtos.  
- **Semana 3** – Implementar checkout com Mercado Pago (Pix + Cartão).  
- **Semana 4** – Deploy em ambiente gratuito (Vercel + Railway).  
