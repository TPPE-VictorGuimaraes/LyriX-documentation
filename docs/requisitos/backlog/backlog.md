# Backlog do Projeto

Este backlog foi estruturado a partir das **elicitações de requisitos** (entrevista e introspecção).  
Foram definidos **Requisitos Funcionais (RF)**, transformados em **Histórias de Usuário (US)**, agrupados em **Features (F)** e **Épicos (E)**.  
Além disso, foram listados **Requisitos Não Funcionais (RNF)** que estabelecem critérios técnicos e de qualidade para o sistema.

---

## Backlog — Requisitos Funcionais

| Nº  | Requisito Funcional | Código US | Código Feature | Código Épico |
|-----|---------------------|-----------|----------------|--------------|
| RF01 | Buscar letras por título | US01 | F1.1 | E1 |
| RF02 | Buscar letras por artista | US02 | F1.1 | E1 |
| RF03 | Exibir a letra completa da música | US03 | F1.2 | E1 |
| RF04 | Favoritar letras e listar favoritos | US05, US06 | F2.1 | E2 |
| RF05 | Compartilhar letras com outros aplicativos | US08 | F3.1 | E3 |
| RF06 | Exibir capa do álbum junto da letra | US04 | F1.2 | E1 |
| RF07 | Armazenar e exibir histórico de buscas | US07 | F2.2 | E2 |
| RF08 | Oferecer tradução da letra | US10 | F4.1 | E4 |
| RF09 | Mostrar letra sincronizada com a música (karaokê) | US11 | F4.2 | E4 |
| RF10 | Integrar o app com players externos (Spotify, YouTube) | US12 | F4.3 | E4 |
| RF11 | Enviar notificações sobre novidades de artistas favoritos | US09 | F3.2 | E3 |
| RF12 | Permitir acesso offline às letras já visualizadas | US13 | F4.4 | E4 |
| RF13 | Permitir login social (Google, Facebook) | US14 | F5.1 | E5 |
| RF14 | Ajustar tamanho e estilo da fonte da letra exibida | US15 | F5.2 | E5 |
| RF15 | Criar playlists de músicas favoritas | US16 | F2.3 | E2 |
| RF16 | Permitir modo noturno além das cores padrão | US17 | F5.3 | E5 |
| RF17 | Buscar letras por trecho da letra (palavras-chave) | US18 | F1.3 | E1 |
| RF18 | Exibir informações adicionais da música (álbum, ano) | US19 | F1.4 | E1 |

---

## Backlog — Requisitos Não Funcionais

| Nº   | Requisito Não Funcional |
|------|--------------------------|
| RNF01 | O app deve ser desenvolvido em Kotlin para Android. |
| RNF02 | O backend deve usar PostgreSQL dockerizado. |
| RNF03 | O sistema deve apresentar interface responsiva e fluida. |
| RNF04 | O app deve utilizar cores roxo e preto como identidade visual. |
| RNF05 | O tempo de resposta da busca deve ser inferior a 3 segundos. |
| RNF06 | O app deve oferecer autenticação segura (OAuth2 para login social). |
| RNF07 | Deve haver suporte a acessibilidade (ex.: leitores de tela). |
| RNF08 | A interface deve suportar personalização de fontes e modo noturno. |

---

## Estrutura de Identificação

- **Épicos (E):**  
  - E1 — Busca e Visualização de Letras  
  - E2 — Personalização e Favoritos  
  - E3 — Compartilhamento e Interação  
  - E4 — Funcionalidades Avançadas  
  - E5 — Experiência do Usuário e Acessibilidade  

- **Features (F):**  
  - F1.1 — Busca de músicas por título/artista  
  - F1.2 — Visualização da letra e capa  
  - F1.3 — Busca por trecho da letra  
  - F1.4 — Exibição de informações adicionais da música  
  - F2.1 — Favoritar músicas  
  - F2.2 — Histórico  
  - F2.3 — Playlists de favoritos  
  - F3.1 — Compartilhamento  
  - F3.2 — Notificações  
  - F4.1 — Tradução  
  - F4.2 — Sincronização (karaokê)  
  - F4.3 — Integração com players externos  
  - F4.4 — Acesso offline  
  - F5.1 — Login social  
  - F5.2 — Personalização de fonte  
  - F5.3 — Modo noturno  

---
