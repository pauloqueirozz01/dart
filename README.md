# APRENDIZADO EM DART - DA SINTAXE AO PROJETO COMPLETO

<p align="left">
  <img src="https://img.shields.io/badge/Dart-3.x-0175C2?style=for-the-badge&logo=dart&logoColor=white" alt="Dart 3"/>
  <img src="https://img.shields.io/badge/REST_API-HTTP%2FJSON-009688?style=for-the-badge&logo=swagger&logoColor=white" alt="REST API"/>
  <img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white" alt="Git"/>
  <img src="https://img.shields.io/badge/macOS-000000?style=for-the-badge&logo=apple&logoColor=white" alt="macOS"/>
  <img src="https://img.shields.io/badge/status-em_aprendizado-blueviolet?style=for-the-badge" alt="Status: em aprendizado"/>
</p>

<p align="left">
  <img src="https://img.shields.io/github/last-commit/pauloqueirozz01/dart?style=flat-square" alt="Último commit"/>
  <img src="https://img.shields.io/github/commit-activity/m/pauloqueirozz01/dart?style=flat-square" alt="Commits por mês"/>
  <img src="https://img.shields.io/github/languages/top/pauloqueirozz01/dart?style=flat-square" alt="Linguagem principal"/>
  <img src="https://img.shields.io/github/repo-size/pauloqueirozz01/dart?style=flat-square" alt="Tamanho do repositório"/>
</p>

> Os badges do GitHub acima (último commit, atividade, linguagem, tamanho) só aparecem depois que
> o repositório for publicado em `github.com/pauloqueirozz01/dart`. Ajuste o nome caso use outro.

Neste repositório fica a minha trilha de aprendizado de **Dart puro** (sem Flutter): cinco módulos de
estudo, cada um com classes de exploração e listas de exercícios como desafio, e um projeto final que
junta tudo.

### INTUITO DO REPOSITÓRIO
Registrar o caminho percorrido, da sintaxe básica até um projeto completo rodando no terminal, para que
qualquer pessoa (inclusive eu no futuro) consiga acompanhar a evolução. É o mesmo formato do meu
[repositório de Java](https://github.com/pauloqueirozz01/java): **estudos**, **exercícios** e **projetos**,
sempre com um README explicando as decisões tomadas.

### ESTRUTURA DO REPOSITÓRIO
```
.
├── 1-sintaxe/                       → variáveis, tipos, operadores, controle de fluxo e funções
├── 2-listas-set-maps/               → List, Set, Map e transformações de coleções
├── 3-dart-poo/                      → classes, herança, abstract, mixins, enums, extensions e records
├── 4-assincronismo-api/             → Future, async/await, Stream, HTTP e JSON
├── 5-error-exception-null-safety/   → try/catch, exceções próprias e null safety
├── 6-projeto-final/                 → projeto completo em Dart puro juntando tudo
├── pubspec.yaml                     → dependências (http) e versão do SDK
└── analysis_options.yaml            → regras do analisador (lints)
```

Cada módulo (de 1 a 5) segue a mesma organização:
```
N-modulo/
├── README.md          → o que o módulo aborda, conceitos e decisões tomadas
├── estudos/           → classes curtas e comentadas para explorar cada assunto
└── exercicios/        → README com a lista de desafios + minhas resoluções
```

### TRILHA DE APRENDIZADO
| # | Módulo | Assuntos | Exercícios |
|---|---|---|---|
| 1 | [Sintaxe](1-sintaxe/README.md) | variáveis, tipos, operadores, `if`/`switch`/laços, funções | [lista](1-sintaxe/exercicios/README.md) |
| 2 | [Listas, Set e Maps](2-listas-set-maps/README.md) | `List`, `Set`, `Map`, `where`/`map`/`fold`, spread | [lista](2-listas-set-maps/exercicios/README.md) |
| 3 | [Dart POO](3-dart-poo/README.md) | classes, construtores, herança, `abstract`, mixins, enums, extensions, records | [lista](3-dart-poo/exercicios/README.md) |
| 4 | [Assincronismo e API](4-assincronismo-api/README.md) | `Future`, `async`/`await`, `Stream`, HTTP, JSON | [lista](4-assincronismo-api/exercicios/README.md) |
| 5 | [Error, Exception e Null Safety](5-error-exception-null-safety/README.md) | `try`/`catch`, exceções próprias, `?`, `??`, `!`, `late` | [lista](5-error-exception-null-safety/exercicios/README.md) |
| 6 | [Projeto final](6-projeto-final/README.md) | tudo junto, em Dart puro | - |

### COMO RODAR NA SUA MÁQUINA

**Pré-requisitos:** [Dart SDK 3.11+](https://dart.dev/get-dart) (no macOS: `brew tap dart-lang/dart && brew install dart`)
e, opcionalmente, o VS Code ou o IntelliJ/Android Studio com o plugin do Dart.

```bash
git clone https://github.com/pauloqueirozz01/dart.git
cd dart
dart pub get          # baixa as dependências (package:http)
```

```bash
# roda qualquer estudo ou exercício direto, sem compilar
dart run 1-sintaxe/estudos/ola_mundo.dart
dart run 4-assincronismo-api/estudos/http_get.dart

# análise estática e formatação
dart analyze
dart format .
```

### COMO ESTUDAR CADA MÓDULO
1. Leia o `README.md` do módulo para entender os conceitos.
2. Rode e altere os arquivos de `estudos/` (quebre o código de propósito para ver as mensagens de erro).
3. Resolva a lista em `exercicios/` por conta própria e só depois compare com as decisões documentadas.
4. Anote o que foi diferente do esperado na seção **Aprendizados e decisões** do README do módulo.

### TECNOLOGIAS E DECISÕES TOMADAS
| Tecnologia | Para que serve | Por que escolhi |
|---|---|---|
| **Dart 3.x** | Linguagem usada em todo o repositório | Null safety, records, pattern matching e `switch` expressions modernos |
| **`package:http`** | Chamadas HTTP no módulo 4 e no projeto final | Mantida pelo time do Dart, API simples (`http.get`) e padrão no ecossistema |
| **`package:lints`** | Regras do analisador | Força o estilo idiomático do Dart desde o começo |
| **`package:test`** | Testes automatizados do projeto final | Biblioteca de testes padrão da linguagem |
| **Git** | Versionamento | Cada módulo concluído vira um commit, formando o histórico da trilha |

> **Por que Dart puro e não Flutter?** Aprender a linguagem primeiro, sem a camada de interface, deixa claro o que
> é Dart e o que é Flutter. Tudo roda no terminal com `dart run`, sem emulador, e o conhecimento é
> reaproveitado depois.

### AUTOR
**Paulo André Santos Queiroz**

[![GitHub](https://img.shields.io/badge/GitHub-pauloqueirozz01-181717?style=flat-square&logo=github)](https://github.com/pauloqueirozz01)
