# Formulário de Cadastro de Usuário em Flutter

**Universidade Evangélica de Goiás - Campus Anápolis**
Engenharia de Software - 8º Período - Turma A - Noturno

| | |
|---|---|
| **Data** | 13/10/2026 |
| **Disciplina** | Desenvolvimento Mobile |
| **Docente** | Renato Luan de Sousa |
| **Discente** | Vinícius Rodrigues Martins - 2311066 |

## Atividade Prática

Tela de cadastro de usuário desenvolvida em Flutter, com captura de dados, filtros de entrada, validação de cada campo e feedback visual ao usuário.

## Campos do formulário

| Campo | Regra |
|---|---|
| Nome completo | Obrigatório |
| E-mail | Obrigatório, validado com RegExp (deve conter `@`) |
| CPF | Obrigatório, somente números, máscara `000.000.000-00` |
| Telefone | Obrigatório, somente números, máscara `(00) 00000-0000` |
| Senha | Obrigatória, mínimo de 6 caracteres |
| Confirmar senha | Obrigatória, deve ser igual à senha |

## Funcionalidades

- Formulário com `Form`, `TextFormField` e `validator` em todos os campos
- `keyboardType` e `inputFormatters` adequados para cada campo
- Máscara de CPF e telefone com `TextInputFormatter` próprio (sem pacotes externos)
- Mensagens de erro exibidas abaixo de cada campo inválido
- Botão para mostrar/ocultar senha (independente nos dois campos de senha)
- SnackBar verde de sucesso quando todos os campos são válidos
- SnackBar vermelho de erro quando há campos inválidos

## Estrutura da tela

```
Scaffold
└── Form(key: _formKey)
    └── SingleChildScrollView
        └── Column
            ├── TextFormField (nome)
            ├── TextFormField (e-mail)
            ├── TextFormField (CPF)
            ├── TextFormField (telefone)
            ├── TextFormField (senha)
            ├── TextFormField (confirmar senha)
            └── ElevatedButton (CADASTRAR)
```

## Como executar

```bash
git clone https://github.com/VIN1RM/flutter-formulario-cadastro.git
cd flutter-formulario-cadastro
flutter pub get
flutter run
```

## Tecnologias

- Flutter
- Dart