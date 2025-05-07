# casoDeUso
```mermaid

sequenceDiagram
    participant Funcionário
    participant Sistema
    participant BancoDeDados

    Funcionário->>Sistema: Solicita acesso ao sistema
    Sistema-->>Funcionário: Solicita login e senha
    Funcionário->>Sistema: Envia credenciais
    Sistema->>BancoDeDados: Valida credenciais
    BancoDeDados-->>Sistema: Confirma autenticidade
    Sistema-->>Funcionário: Interface com opções (menu)

    Funcionário->>Sistema: Seleciona "Consultar Feedback"
    Sistema->>BancoDeDados: Consulta avaliações recebidas
    BancoDeDados-->>Sistema: Retorna lista de feedbacks
    Sistema-->>Funcionário: Exibe feedbacks com detalhes
