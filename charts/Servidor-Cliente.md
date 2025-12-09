flowchart TD
    subgraph Client["🌐 Client"]
        A["🖥️ Vista UI <br> Recibe la entrada del usuario"] -->|Interacción| B["📡 Client DAO <br> Gestiona peticiones al servidor"]
        B -->|Consulta el modelo| M["📊 Cliente Model <br> Logica de negocio local"]
        B -->|Regresa los datos procesados| A
    end

    subgraph Server["🖥️ Servidor"]
        B -->|Peticion HTTP GET/POST...| C["🌍 Webservice API"]
        C -->|Consulta Modelo| N["🛠️ Server Modelo <br> Logica de negocio central"]
        N -->|Consulta DAO| D["📂 Server DAO <br> Accés a dades"]
        D -->|Consulta BB.DD| DB["🗄️ Base de Dades"]
        DB -->|Regresa los datos| D
        D -->|Regresa el objeto procesado| N
        N -->|Regresa respuesta| C
        C -->|Respuesta en lenguaje HTTP JSON, XML, etc.| B
    end

    classDef client fill:#D6EAF8,stroke:#333,stroke-width:2px;
    classDef server fill:#F9EBEA,stroke:#333,stroke-width:2px;
    classDef db fill:#F7DC6F,stroke:#333,stroke-width:2px;
    
    class A client;
    class B client;
    class M client;
    class C server;
    class N server;
    class D server;
    class DB db;