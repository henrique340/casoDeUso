```mermaid
graph TD
    subgraph Cliente
        NavegadorWeb[Navegador Web]
    end

    subgraph "Servidor Aplicação"
        subgraph "VM Aplicativo Backend"
            Backend[Aplicativo Backend]
        end
    end

    subgraph "Servidor de Banco de Dados"
        DB[(PostgreSQL)]
    end

    subgraph "Servidor de Arquivos"
        Ajuda[Ajuda]
    end

    subgraph "Servidor de Autenticação"
        Keycloak[Keycloak]
    end

    NavegadorWeb -- HTTP/HTTPS --> Backend
    Backend -- "REST API" --> Ajuda
    Backend -- "OAuth2.0" --> Keycloak
    Backend -- "API PostgreSQL" --> DB
