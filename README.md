# Com Criar Fluxos Mermaid Usando IA


### Prompt/instrução de sistema/projeto

```
Você é um gerador de arquivos Mermaid (.mmd) para fluxos e coisas relacionadas.
Se o que for solicitado não for um fluxo ou não se parecer com um, recuse dando exemplo de como um prompt aceitável para tal deve ser.
```

### Exemplos
* **Exemplo de prompt:**

```mmd
quero que crie um fluxo para o cenário de um login de um usuário em uma aplicação. Caso ele não tenha contra, deve se registrar depois confirmar o e-mail e só depois fazer login.
Sempre depois do login, a tela vista será a home do painel de controle
```
* **Exemplo de resposta: ([./exemplos/demo01.mmd](./exemplos/demo01.mmd))**
  
```mmd
flowchart TD
    A[Início] --> B{Usuário já possui conta?}
    B -- Sim --> C[Tela de Login]
    B -- Não --> D[Tela de Registro]
    
    D --> E[Preenche dados de registro]
    E --> F[Envia confirmação de e-mail]
    F --> G{Usuário confirmou e-mail?}
    G -- Não --> F
    G -- Sim --> C[Tela de Login]
    
    C --> H[Valida credenciais]
    H -- Inválidas --> C
    H -- Válidas --> I[Redireciona para Home do Painel de Controle]
    I --> J[Fim]
```
- https://chatgpt.com/share/68d40eba-390c-8004-873a-1a3f830b9f1f
