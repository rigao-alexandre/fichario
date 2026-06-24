# Fichário 🗂️

Um app de notas bem simples para guardar trechos de texto que você usa com frequência — respostas prontas, mensagens, comandos, modelos de e-mail — e copiar com um clique, sem precisar selecionar nada.

Tudo em um único arquivo HTML, sem backend, sem build, sem dependências. Suas notas ficam salvas no navegador.

## ✨ Funcionalidades

- **Copiar com um clique** — cada nota tem um botão que copia o texto pro clipboard na hora
- **Modelos com variáveis** — escreva `{{variavel}}` no texto e o app gera campos pra você preencher antes de copiar
- **Reordenar** — arraste pelo ícone ⠿⠿ ou use as setas ▲▼ pra organizar as notas como quiser
- **Exportar / importar** — gera um backup em `.json` e importa em qualquer outro navegador ou dispositivo
- **Numeração de catálogo** — cada nota recebe um número fixo (Nº 0001, 0002...) que não muda quando você reordena
- **Sem servidor** — tudo roda no navegador, com `localStorage`

## 🚀 Como usar

### Localmente
Baixe o arquivo `fichario.html` e abra direto no navegador (duplo clique).

### Hospedado (recomendado)
Como é um arquivo estático, qualquer serviço de hospedagem gratuita funciona:

- **[Netlify Drop](https://app.netlify.com/drop)** — arraste o arquivo (renomeado pra `index.html`) e pronto, sem precisar de conta
- **GitHub Pages** — suba este repositório e ative o Pages nas configurações
- **Vercel** ou **Cloudflare Pages** — conecte o repositório ou faça upload direto
- **[Surge.sh](https://surge.sh/)** — `npm install -g surge` e depois `surge`

## 📝 Modelos com variáveis

Escreva uma nota usando chaves duplas pra marcar os campos que mudam:

```
Olá {{nome}}, seu pedido {{numero}} foi enviado e chega em {{prazo}} dias úteis.
```

O cartão detecta as variáveis automaticamente, mostra um campo de preenchimento pra cada uma e exibe uma prévia do texto final. O botão de copiar leva o texto já preenchido — o modelo original com `{{}}` continua salvo, intacto, pra próxima vez. Os valores preenchidos também ficam salvos por nota.

## 📤 Exportar e importar

- **Exportar** baixa um `.json` com todas as notas (texto, variáveis preenchidas e numeração)
- **Importar** lê um `.json` e **adiciona** as notas ao fichário atual, sem apagar as que já existem

Use isso para:
- Fazer backup, já que tudo vive no `localStorage` do navegador
- Levar suas notas de um navegador/dispositivo para outro

## ⚠️ Como funciona por baixo dos panos

- As notas são salvas no `localStorage`, então ficam **por domínio/navegador** — abrir o arquivo localmente e acessar a versão hospedada são "caixas" separadas de armazenamento
- Não há sincronização automática entre dispositivos; use exportar/importar para mover notas entre eles
- Nenhum dado é enviado a servidor algum — é só HTML, CSS e JavaScript

## 🛠️ Stack

HTML + CSS + JavaScript puro. Fontes via Google Fonts (Space Grotesk e IBM Plex Mono). Nenhuma dependência externa de runtime.

## 📄 Licença

Adicione aqui a licença de sua escolha (ex: MIT) caso queira tornar o repositório open source.
