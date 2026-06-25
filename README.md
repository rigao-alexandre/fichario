https://fichario.netlify.app/

# Fichário 🗂️

Um app de notas bem simples para guardar trechos de texto que você usa com frequência — respostas prontas, mensagens, comandos, modelos de e-mail — e copiar com um clique, sem precisar selecionar nada.

Tudo em um único arquivo HTML, sem backend, sem build, sem dependências. Suas notas ficam salvas no navegador.

https://fichario.netlify.app/

## ✨ Funcionalidades

- **Copiar com um clique** — cada nota tem um botão que copia o texto pro clipboard na hora
- **Título e busca** — dê um título opcional a cada nota e encontre qualquer uma rapidamente, buscando por título ou conteúdo (ignora acento e maiúsculas/minúsculas)
- **Modelos com variáveis** — escreva `{{variavel}}` no texto e o app gera campos pra você preencher antes de copiar
- **Reordenar** — arraste pelo ícone ⠿⠿ ou use as setas ▲▼ pra organizar as notas como quiser
- **Compartilhar** — manda uma nota direto pro WhatsApp, e-mail etc. via menu nativo do sistema, ou copia um link que a outra pessoa pode abrir pra importar a nota
- **Exportar / importar** — gera um backup em `.json` e importa em qualquer outro navegador ou dispositivo
- **Numeração de catálogo** — cada nota recebe um número fixo (Nº 0001, 0002...) que não muda quando você reordena
- **Sem servidor** — tudo roda no navegador, com `localStorage`

## 🚀 Como usar

### SaaS

https://fichario.netlify.app/

### Localmente

Baixe o arquivo `index.html` e abra direto no navegador (duplo clique).

### Hospedado

Como é um arquivo estático, qualquer serviço de hospedagem gratuita funciona.

> A funcionalidade de compartilhar por link (veja abaixo) só funciona de verdade entre dispositivos diferentes se o app estiver hospedado. Abrindo o arquivo localmente, o link gerado só funciona no seu próprio computador.

## 📝 Modelos com variáveis

Escreva uma nota usando chaves duplas pra marcar os campos que mudam:

```
Olá {{nome}}, seu pedido {{numero}} foi enviado e chega em {{prazo}} dias úteis.
```

O cartão detecta as variáveis automaticamente, mostra um campo de preenchimento pra cada uma e exibe uma prévia do texto final. O botão de copiar leva o texto já preenchido — o modelo original com `{{}}` continua salvo, intacto, pra próxima vez. Os valores preenchidos também ficam salvos por nota.

## 🔍 Título e busca

Cada nota pode ter um título opcional, exibido em destaque no topo do cartão. Ele não entra no texto copiado — é só pra te ajudar a identificar e encontrar a nota depois.

A barra de busca, abaixo do cabeçalho, filtra as notas por título e conteúdo em tempo real, ignorando acentuação e caixa (buscar "sao" encontra "São Paulo").

## 📤 Compartilhar uma nota

Cada nota tem um botão **Compartilhar**, que funciona de duas formas:

- **Com suporte a Web Share API** (a maioria dos celulares, e Chrome/Edge no desktop): abre o menu nativo de compartilhar do sistema, com o texto da nota e um link.
- **Sem suporte** (ex: Firefox desktop): copia automaticamente um link pra área de transferência.

Quem recebe e abre o link vê um aviso na própria página, oferecendo importar a nota recebida (com título, modelo e variáveis preservados) pro fichário dela, sem apagar nada que já existia.

O link carrega a nota inteira codificada em **base64url** depois de `#compartilhar=`, sem precisar de servidor pra armazenar nada.

## 📤 Exportar e importar

- **Exportar** baixa um `.json` com todas as notas (texto, título, variáveis preenchidas e numeração)
- **Importar** lê um `.json` e **adiciona** as notas ao fichário atual, sem apagar as que já existem

Use isso para:

- Fazer backup, já que tudo vive no `localStorage` do navegador
- Levar suas notas de um navegador/dispositivo para outro

## ⚠️ Como funciona por baixo dos panos

- As notas são salvas no `localStorage`, então ficam **por domínio/navegador** — abrir o arquivo localmente e acessar a versão hospedada são "caixas" separadas de armazenamento
- Não há sincronização automática entre dispositivos; use exportar/importar ou compartilhar por link para mover notas entre eles
- Nenhum dado é enviado a servidor algum — é só HTML, CSS e JavaScript

## 🛠️ Stack

HTML + CSS + JavaScript puro. Fontes via Google Fonts (Space Grotesk e IBM Plex Mono). Nenhuma dependência externa de runtime.

## 🗺️ Roadmap

Ideias para o futuro, sem prazo definido:

- [ ] Pin de notas (fixar as mais usadas no topo)
- [ ] Tags ou categorias para organizar notas
- [ ] Atalhos de teclado (ex: nova nota, focar busca)
- [ ] Modo escuro
- [ ] Múltiplos fichários / pastas
- [ ] Ver nota (possibilita salvar nos favoritos)

Sugestões são bem-vindas via issue ou pull request.

## 📄 Licença

MIT
