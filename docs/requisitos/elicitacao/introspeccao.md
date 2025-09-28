# Introspecção

Foi realizada uma introspecção pelo analista no contexto do aplicativo de letras de música (Liryx).
Nessa técnica, o analista se coloca no lugar do usuário e reflete sobre cenários reais de uso, antecipando funcionalidades que poderiam melhorar a experiência, acessibilidade e personalização.

Com base nessas reflexões, foram identificadas novas necessidades e elicitados requisitos adicionais, que complementam os já obtidos por entrevista.


## Perguntas e Reflexões da Introspecção

### Experiência de Acesso

- **Pergunta (reflexão):** Como o usuário pode entrar no app de forma simples?
- **Resposta Introspectiva:** Seria útil permitir login com contas sociais, sem necessidade de criar cadastro manual.
- **Requisito Derivado:** O sistema deve permitir login social (Google, Facebook).

- **Pergunta (reflexão):** Como o app poderia ser mais acessível?
- **Resposta Introspectiva:** Usuários podem precisar ajustar o tamanho da fonte.
- **Requisito Derivado:** O sistema deve permitir personalização do tamanho e estilo da fonte.

### Personalização e Usabilidade

- **Pergunta (reflexão):** Como o usuário pode organizar melhor suas músicas favoritas?
- **Resposta Introspectiva:** Poder criar playlists seria um diferencial.
- **Requisito Derivado:** O sistema deve permitir criar playlists de músicas favoritas.

- **Pergunta (reflexão):** E quanto ao visual do aplicativo?
- **Resposta Introspectiva:** Ter apenas roxo e preto pode limitar. É interessante oferecer um modo noturno adicional.
- **Requisito Derivado:** O sistema deve oferecer modo noturno.

### Busca e Informações Extras

- **Pergunta (reflexão):** Se o usuário não lembrar do título ou artista, como poderia buscar?
- **Resposta Introspectiva:** Uma busca por trecho da letra resolveria.
- **Requisito Derivado:** O sistema deve permitir busca por trecho da letra (palavras-chave).

- **Pergunta (reflexão):** Além da letra, o que mais seria útil?
- **Resposta Introspectiva:** Exibir informações adicionais como álbum e ano da música.
- **Requisito Derivado:** O sistema deve exibir informações adicionais da música (álbum, ano).


## Requisitos Elicitados
### Requisitos Funcionais (RF)

- RF13 — Permitir login social (Google, Facebook).
- RF14 — Ajustar tamanho e estilo da fonte da letra exibida.
- RF15 — Criar playlists de músicas favoritas dentro do app.
- RF16 — Permitir modo noturno além das cores padrão.
- RF17 — Adicionar recurso de busca por trecho da letra (palavras-chave).
- RF18 — Exibir informações adicionais da música (álbum, ano de lançamento).


### Requisitos Não Funcionais (RNF)

- RNF06 — O app deve oferecer autenticação segura (OAuth2 para login social).
- RNF07 — Deve haver suporte a acessibilidade (ex.: leitores de tela).
- RNF08 — A interface deve suportar personalização de fontes e modo noturno.


## Organização em Épicos, Features e Histórias de Usuário

### Épico 5: Experiência do Usuário e Acessibilidade

- **Feature 5.1:** Login social
- **US14:** Como **usuário**, quero entrar no app usando minha conta Google/Facebook, para agilizar o acesso.

- **Feature 5.2:** Personalização de fonte
- **US15:** Como **usuário**, quero ajustar o tamanho e estilo da fonte, para facilitar a leitura.

- **Feature 5.3:** Modo noturno
- **US17:** Como **usuário**, quero usar o app em modo noturno, para reduzir o cansaço visual.


### Extensões de Funcionalidades Existentes

- **Feature 2.3:** Playlists de favoritos
- **US16:** Como **usuário**, quero criar playlists de músicas favoritas, para organizar melhor minhas letras.

- **Feature 1.3:** Busca por trecho da letra
- **US18:** Como **usuário**, quero buscar letras digitando parte da letra, para encontrar músicas mesmo sem saber o título.

- **Feature 1.4:** Informações adicionais da música
- **US19:** Como **usuário**, quero visualizar informações extras (álbum, ano) junto da letra, para enriquecer a experiência.