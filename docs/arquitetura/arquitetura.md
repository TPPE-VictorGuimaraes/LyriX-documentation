# Arquitetura do Projeto

## Introdução

Na construção de aplicativos móveis, a **arquitetura** é um dos fatores mais importantes para garantir que o sistema seja **escalável, testável, de fácil manutenção e evolutivo**.  

Existem diferentes abordagens utilizadas no desenvolvimento de apps Android, como:

- **Arquitetura em camadas simples (MVC)**: onde a interface de usuário, lógica de negócio e acesso a dados estão mais acoplados. Apesar de fácil de implementar, tende a gerar problemas de manutenção em projetos maiores.
- **MVP (Model–View–Presenter)**: separa a lógica de apresentação da UI, mas ainda pode gerar acoplamento em cenários complexos.
- **MVVM (Model–View–ViewModel)**: modelo amplamente utilizado em conjunto com as bibliotecas do Jetpack. Facilita a separação entre a camada de interface (View) e a lógica de apresentação (ViewModel), permitindo uma melhor testabilidade.
- **Clean Architecture**: proposta por Robert C. Martin (Uncle Bob), organiza o software em camadas concêntricas, onde as regras de negócio ficam isoladas das implementações de frameworks. Essa abordagem garante independência, baixo acoplamento e alta manutenibilidade.

---

## Arquitetura Escolhida

Neste projeto, foi adotada uma combinação entre **Clean Architecture** e o padrão **MVVM**, utilizando **Jetpack Compose** para a interface de usuário.  

Essa escolha foi feita para garantir:

- **Separação de responsabilidades** clara entre UI, lógica de negócio e dados.  
- **Testabilidade** (use cases e ViewModels podem ser testados isoladamente).  
- **Escalabilidade**, permitindo adicionar novas features sem comprometer o código existente.  
- **Adoção de tecnologias modernas** do ecossistema Android (Compose, Hilt, Coroutines, Flow, Room, Retrofit).  

---

## Estrutura em Camadas

A arquitetura é dividida em **três camadas principais**, alinhadas com Clean Architecture:

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
  - **Remote Data Source** (ex.: Retrofit + API REST).
  - **Local Data Source** (ex.: Room Database).
- Faz a conversão de modelos (DTOs ↔ Entities ↔ Domain Models).

---

## Fluxo de Dados

O fluxo de dados segue o seguinte caminho:

[UI/Compose] <--> [ViewModel] <--> [UseCases] <--> [Repository Interface]


[Remote API] [Local DB]


1. A **UI** (Compose) dispara uma ação do usuário.  
2. O **ViewModel** interpreta o evento e chama um **UseCase**.  
3. O **UseCase** consulta o **Repositório** (definido no domínio).  
4. O **Repositório** decide buscar no **Remote (API)** ou no **Local (Room)**.  
5. O resultado percorre o caminho inverso até a UI, que exibe o estado atualizado.  

---

## Tecnologias Utilizadas

- **Kotlin** — linguagem principal.  
- **Jetpack Compose** — UI declarativa.  
- **ViewModel + StateFlow** — gerenciamento de estado.  
- **Hilt (Dagger)** — injeção de dependência.  
- **Coroutines + Flow** — operações assíncronas.  
- **Room** — banco de dados local.  
- **Retrofit + OkHttp** — consumo de APIs REST.  
- **Timber** — logging.  

---

## Conclusão

Com essa arquitetura, o projeto se mantém modular, escalável e de fácil manutenção, ao mesmo tempo em que adota boas práticas recomendadas pelo Google para desenvolvimento Android moderno.

Essa base garante escalabilidade (que novas funcionalidades como tradução, karaokê, e acesso offline) possam ser adicionadas sem comprometer a estrutura já existente.
