# Elicitação de Requisitos

Foi realizada uma **entrevista com um stakeholder** interessado no aplicativo de letras de música. A partir dessa entrevista foram coletadas percepções sobre funcionalidades essenciais, melhorias desejadas e ideias de diferenciais. Com base nas respostas, foi possível elicitar requisitos funcionais e não funcionais, além de organizar **histórias de usuário**, **features** e **épicos**.

---

## Perguntas e Respostas da Entrevista

### Funcionalidades Básicas
- **Pergunta:** O que não pode faltar no aplicativo de letras de música?  
  **Resposta:** Deve ter busca por título e por artista.  
  **Requisito Derivado:** O sistema deve permitir busca de letras por título ou artista.

- **Pergunta:** Gostaria que fosse possível favoritar letras?  
  **Resposta:** Sim, seria importante para acessar depois.  
  **Requisito Derivado:** O sistema deve permitir favoritar e listar letras favoritas.

- **Pergunta:** Deseja que o app permita compartilhar letras?  
  **Resposta:** Sim, poder mandar para amigos seria ótimo.  
  **Requisito Derivado:** O sistema deve permitir compartilhar letras via outros apps.

- **Pergunta:** Você gostaria de ver a capa do álbum junto da letra?  
  **Resposta:** Sim, deixaria a experiência mais completa.  
  **Requisito Derivado:** O sistema deve exibir metadados da música (ex.: capa do álbum).

- **Pergunta:** Acha útil poder consultar o histórico de buscas?  
  **Resposta:** Sim, facilita encontrar músicas que já procurei.  
  **Requisito Derivado:** O sistema deve armazenar e mostrar histórico de pesquisas.

---

### Funcionalidades Avançadas
- **Pergunta:** Além de ver a letra, o que mais gostaria de ter na tela da música?  
  **Resposta:** Seria legal ter tradução disponível.  
  **Requisito Derivado:** O sistema deve oferecer tradução da letra (manual ou automática).

- **Pergunta:** Gostaria que houvesse sincronização estilo karaokê?  
  **Resposta:** Sim, se possível mostrar a letra acompanhando a música.  
  **Requisito Derivado:** O sistema deve oferecer visualização da letra sincronizada com a música.

- **Pergunta:** E se o app tivesse integração com Spotify ou YouTube?  
  **Resposta:** Seria ótimo abrir a letra junto com a música que estou ouvindo.  
  **Requisito Derivado:** O sistema deve permitir integração com players externos.

- **Pergunta:** Acha útil ter notificações de artistas favoritos?  
  **Resposta:** Sim, quero ser avisado quando sair algo novo.  
  **Requisito Derivado:** O sistema deve enviar notificações sobre novidades dos artistas favoritos.

- **Pergunta:** Gostaria de poder usar o app offline?  
  **Resposta:** Sim, pelo menos para letras já visualizadas.  
  **Requisito Derivado:** O sistema deve permitir acesso offline às letras já carregadas.

---

## Requisitos Elicitados

### Requisitos Funcionais (RF)
1. RF01 — Buscar letras por título.  
2. RF02 — Buscar letras por artista.  
3. RF03 — Exibir a letra completa da música.  
4. RF04 — Favoritar letras e listar favoritos.  
5. RF05 — Compartilhar letras com outros aplicativos.  
6. RF06 — Exibir capa do álbum junto da letra.  
7. RF07 — Armazenar e exibir histórico de buscas.  
8. RF08 — Oferecer tradução da letra.  
9. RF09 — Mostrar letra sincronizada com a música (karaokê).  
10. RF10 — Integrar o app com players externos (Spotify, YouTube).  
11. RF11 — Enviar notificações sobre novidades de artistas favoritos.  
12. RF12 — Permitir acesso offline às letras já visualizadas.  

### Requisitos Não Funcionais (RNF)
1. RNF01 — O app deve ser desenvolvido em Kotlin para Android.  
2. RNF02 — O backend deve usar PostgreSQL dockerizado.  
3. RNF03 — O sistema deve apresentar interface responsiva e fluida.  
4. RNF04 — O app deve utilizar cores roxo e preto como identidade visual.  
5. RNF05 — O tempo de resposta da busca deve ser inferior a 3 segundos.  

---

## Organização em Épicos, Features e Histórias de Usuário

### Épico 1: Busca e Visualização de Letras
- **Feature 1.1:** Busca de músicas  
  - US01: Como **usuário**, quero buscar letras por **título**, para encontrar a música que desejo.  
  - US02: Como **usuário**, quero buscar letras por **artista**, para visualizar músicas relacionadas.  

- **Feature 1.2:** Visualização da letra  
  - US03: Como **usuário**, quero visualizar a letra completa da música selecionada.  
  - US04: Como **usuário**, quero ver a **capa do álbum** junto da letra para uma experiência mais rica.  

---

### Épico 2: Personalização e Favoritos
- **Feature 2.1:** Favoritar músicas  
  - US05: Como **usuário**, quero favoritar letras para acessá-las rapidamente depois.  
  - US06: Como **usuário**, quero acessar uma lista de favoritos em uma aba dedicada.  

- **Feature 2.2:** Histórico  
  - US07: Como **usuário**, quero acessar um histórico de buscas para reutilizar pesquisas recentes.  

---

### Épico 3: Compartilhamento e Interação
- **Feature 3.1:** Compartilhamento  
  - US08: Como **usuário**, quero compartilhar letras via outros aplicativos (WhatsApp, Instagram etc.).  

- **Feature 3.2:** Notificações  
  - US09: Como **usuário**, quero receber notificações quando sair algo novo de um artista favorito.  

---

### Épico 4: Funcionalidades Avançadas
- **Feature 4.1:** Tradução  
  - US10: Como **usuário**, quero visualizar a tradução da letra para outro idioma.  

- **Feature 4.2:** Sincronização (karaokê)  
  - US11: Como **usuário**, quero acompanhar a letra em tempo real enquanto a música toca.  

- **Feature 4.3:** Integração com players externos  
  - US12: Como **usuário**, quero abrir a letra automaticamente quando escutar uma música no Spotify/YouTube.  

- **Feature 4.4:** Acesso offline  
  - US13: Como **usuário**, quero acessar letras já abertas mesmo sem internet.  

---
