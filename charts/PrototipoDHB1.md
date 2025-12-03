```mermaid
flowchart LR

    %% Bloc Client
    subgraph CLIENT ["🌐 Client (FrontEnd)"]
        VISTA["Vista<br>(Input Nom)"]
        DAOCLIENT["DaoClient<br>(getUserName)"]
    end

    %% Bloc Servidor
    subgraph SERVER ["🖥️ Servidor (Backend)"]
        WEBSERVICE["WebService<br>(getUserByName)"]
        DAOSERVER["Dao<br>(getUserByName)"]
        DATA["Llista de dades d'usuaris"]
    end

    %% Connexions internes Client
    VISTA <--> DAOCLIENT

    %% Petició i resposta HTTP
    DAOCLIENT -- "Petició HTTP" --> WEBSERVICE
    WEBSERVICE -- "Resposta HTTP" --> DAOCLIENT

    %% Connexions internes Servidor
    WEBSERVICE <--> DAOSERVER
    DAOSERVER <--> DATA
```