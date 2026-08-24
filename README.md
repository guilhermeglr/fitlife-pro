# 🏋️ FitLife Pro

Aplicação web de acompanhamento fitness com inteligência artificial, desenvolvida para o mercado brasileiro.

![React](https://img.shields.io/badge/React-18-blue)
![Supabase](https://img.shields.io/badge/Supabase-Backend-green)
![Claude AI](https://img.shields.io/badge/Claude-AI%20Powered-purple)
![PWA](https://img.shields.io/badge/PWA-Ready-orange)

🔗 **[Ver aplicação ao vivo](https://fitlife-pro.vercel.app)**

---

## Sobre o projeto

O FitLife Pro nasceu da dificuldade de acompanhar treino e alimentação em
aplicativos que não conversam entre si. A proposta é reunir peso, refeições,
treinos e evolução no mesmo lugar, com um assistente de IA que interpreta os
dados e orienta o usuário.

## Funcionalidades

- **Tracking completo** — peso, refeições, treinos e progresso fotográfico
- **Coach de IA** — assistente que analisa os dados via API da Anthropic
- **Sistema de assinaturas** — planos Free, Premium e Anual
- **PWA** — instalável no celular, com ícones para Android, iOS e Windows
- **Desafios e metas** — sistema gamificado de conquistas
- **Gráficos de evolução** — visualização do progresso ao longo do tempo
- **Autenticação** — via Supabase Auth

## Tecnologias

**Frontend**
- React (via CDN)
- Tailwind CSS
- Chart.js
- Service Workers (PWA)

**Backend**
- Supabase — autenticação, banco de dados e storage
- Funções serverless na Vercel
- API da Anthropic (Claude)

**Pagamentos**
- MercadoPago com webhooks (em desenvolvimento)

## Estrutura

```
api/          Funções serverless (chat com IA, assinaturas, webhooks)
backend/      Servidor Node para desenvolvimento local
frontend/     Ícones e assets do PWA
src/          Integração com o Supabase
index.html    Aplicação
sw.js         Service Worker
supabase-schema.sql   Esquema do banco
```

## Como executar localmente

```bash
git clone https://github.com/guilhermeglr/FitLifePro.git
cd FitLifePro

npm install -g http-server
http-server -p 8080
```

Acesse `http://localhost:8080`.

## Configuração

Crie um arquivo `.env.local` na raiz:

```
SUPABASE_URL=sua-url-supabase
SUPABASE_ANON_KEY=sua-chave-publica-supabase
ANTHROPIC_API_KEY=sua-chave-anthropic
```

> A chave da Anthropic é usada apenas nas funções serverless, nunca no
> navegador. A chave `anon` do Supabase é pública por natureza — a proteção
> dos dados vem das políticas de Row Level Security configuradas no banco.

## Roadmap

- [x] Sistema de tracking básico
- [x] Integração com IA
- [x] Sistema de assinaturas
- [x] PWA com ícones multiplataforma
- [ ] Integração completa com MercadoPago
- [ ] Notificações push
- [ ] Modo offline completo
- [ ] Funcionalidades sociais

## Autor

**Guilherme Reginato**

- GitHub: [@guilhermeglr](https://github.com/guilhermeglr)
- LinkedIn: [guilherme-leite-reginato](https://www.linkedin.com/in/guilherme-leite-reginato-894aa9228/)

## Licença

MIT — sinta-se livre para estudar, adaptar e reaproveitar.
