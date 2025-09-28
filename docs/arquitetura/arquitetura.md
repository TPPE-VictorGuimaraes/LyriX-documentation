# Arquitetura do Projeto

## Introdução

Na construção de aplicativos móveis, a **arquitetura** é um dos fatores mais importantes para garantir que o sistema seja **escalável, testável, de fácil manutenção e evolutivo**.  

Existem diferentes abordagens utilizadas no desenvolvimento de apps Android e servidores backend, como:

- **Arquitetura em camadas simples (MVC)**: onde a interface de usuário, lógica de negócio e acesso a dados estão mais acoplados. Apesar de fácil de implementar, tende a gerar problemas de manutenção em projetos maiores.  
- **MVP (Model–View–Presenter)**: separa a lógica de apresentação da UI, mas ainda pode gerar acoplamento em cenários complexos.  
- **MVVM (Model–View–ViewModel)**: modelo amplamente utilizado em conjunto com as bibliotecas do Jetpack. Facilita a separação entre a camada de interface (View) e a lógica de apresentação (ViewModel), permitindo uma melhor testabilidade.  
- **Clean Architecture**: proposta por Robert C. Martin (Uncle Bob), organiza o software em camadas concêntricas, onde as regras de negócio ficam isoladas das implementações de frameworks. Essa abordagem garante independência, baixo acoplamento e alta manutenibilidade.  

---

## Arquitetura Escolhida

Neste projeto, foi adotada uma combinação entre:  

- **Clean Architecture + MVVM no aplicativo mobile**, utilizando **Jetpack Compose** para a interface de usuário.  
- **Ktor no backend**, com **documentação de API via Swagger/OpenAPI**, banco de dados **PostgreSQL dockerizado** e serviços REST.  

Essa escolha foi feita para garantir:  

- **Separação de responsabilidades** clara entre UI, lógica de negócio, dados e backend.  
- **Testabilidade** (use cases e ViewModels no app, e rotas no backend podem ser testadas isoladamente).  
- **Escalabilidade**, permitindo adicionar novas features sem comprometer o código existente.  
- **Adoção de tecnologias modernas** do ecossistema Android e Kotlin (Compose, Hilt, Coroutines, Flow, Room, Retrofit, Ktor).  

---

## Estrutura em Camadas (Mobile)

A arquitetura do **aplicativo Android** é dividida em três camadas principais, alinhadas com Clean Architecture:

### 1. **Camada de Apresentação (Presentation)**

- Responsável pela interface gráfica (UI).  
- Implementada com **Jetpack Compose**.  
- Usa o padrão **MVVM** com `ViewModel` para gerenciar estado e lógica de apresentação.  
- Comunicação assíncrona com os casos de uso (UseCases) via **Coroutines e Flow**.  

### 2. **Camada de Domínio (Domain)**

- Contém as **regras de negócio** e **casos de uso (UseCases)**.  
- Define **interfaces de repositório** para abstrair fontes de dados.  
- Independente de frameworks, garante que o domínio não dependa de detalhes de implementação.  

### 3. **Camada de Dados (Data)**

- Implementa os repositórios definidos no domínio.  
- Contém:  
  - **Remote Data Source** (ex.: Retrofit + API REST via Ktor).  
  - **Local Data Source** (ex.: Room Database).  
- Faz a conversão de modelos (DTOs ↔ Entities ↔ Domain Models).  

---

## Arquitetura do Backend (Ktor)

O **backend** será responsável por fornecer os dados de letras de músicas, artistas, traduções e funcionalidades extras ao app.  

### Estrutura

**Ktor Application**  
   - Contém as rotas (endpoints REST).  
   - Configurações de autenticação, logging e serialização.  

**Camada de Domínio (UseCases/Services)**  
   - Contém as regras de negócio do backend.  
   - Define contratos de repositórios.  

**Camada de Dados (Repositories)**  
   - Integração com banco de dados **PostgreSQL** (dockerizado).  
   - Uso de ORM/SQL DSL (Exposed, Hibernate ou equivalente).  

**Documentação da API**  
   - Feita com **Swagger/OpenAPI**, integrando com as rotas do Ktor.  
   - Disponibiliza uma UI interativa para explorar e testar os endpoints.  

---

## Fluxo de Dados (Visão Geral)

[UI/Compose] <--> [ViewModel] <--> [UseCases] <--> [Repository Interface]

[Remote API (Ktor)] <--> [PostgreSQL Docker]

| Swagger/OpenAPI (documentação)


1. A UI (Compose) dispara uma ação do usuário.
2. O ViewModel interpreta o evento e chama um UseCase.
3. O UseCase consulta o Repositório (definido no domínio).
4. O Repositório decide buscar no Remote (Ktor API) ou no Local (Room).
5. No backend (Ktor), a requisição chega na rota, que aciona os serviços e consulta o PostgreSQL.
6. O resultado percorre o caminho inverso até a UI, que exibe o estado atualizado.


## Tecnologias Utilizadas

### Mobile

- Kotlin — linguagem principal.
- Jetpack Compose — UI declarativa.
- ViewModel + StateFlow — gerenciamento de estado.
- Hilt (Dagger) — injeção de dependência.
- Coroutines + Flow — operações assíncronas.
- Room — banco de dados local.
- Retrofit + OkHttp — consumo de APIs REST.
- Timber — logging.


### Backend

- Kotlin + Ktor — framework para APIs.
- PostgreSQL (Docker) — banco de dados principal.
- Exposed (ou ORM equivalente) — acesso ao banco.
- Swagger/OpenAPI — documentação de endpoints.