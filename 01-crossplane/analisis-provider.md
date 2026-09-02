# =====================================================================
# Análisis del Provider PostgreSQL
# =====================================================================

## Provider: tages/provider-postgresql v0.1.0

### 1. Managed Resources disponibles
Provider: https://marketplace.upbound.io/providers/tages/provider-postgresql/v0.1.0?tab=managedResources
<!-- Completa aquí -->
¿Qué Managed Resources ofrece este provider? Lista cada uno con una descripción breve de su propósito.
Este provider ofrece 17 Managed Resources:
-   Database: Es el esquema para las API de base de datos. Crea y administra una base de datos en PostgreSQL server.
-   Extension: Es el esquema para la API de extensiones. Crea y administra una extensión en un servidor PostgreSQL.
-   Function: Es el esquema para la API de funciones. Crea y gestiona una función en un servidor PostgreSQL.
-   Grant: Es el esquema para la API de permisos. Crea y gestiona los privilegios otorgados a un usuario para un esquema de base de datos.
-   Mapping: Es el esquema para la API de mappings. Crea y gestiona una el mapping de un usuario en un servidor PostgreSQL.
-   Privileges: Es el esquema para la API de privilegios. Crea y gestiona los privilegios predeterminados otorgados a un usuario para un esquema de una base de datos.
-   ProviderConfig: Configura un proveedor de PostgreSQL.
-   ProviderConfigUsage: Indica que un recurso está utilizando un ProviderConfig.
-   Publication: Es el esquema para la API de publicaciones. Crea y gestiona una publicación en una base de datos de servidor PostgreSQL.
-   ReplicationSlot: Es el esquema para la API ReplicationSlots. Crea y administra una ranura de replicación física en un servidor PostgreSQL.
-   Role(grant.postgresql.upbound.io): Es el esquema para la API de Roles. Crea y gestiona la pertenencia a un rol y a uno o más roles.
-   Role(postgresql.postgresql.upbound.io): Es el esquema para la API de roles. Crea y administra un rol en un servidor PostgreSQL. 
-   Schema: Es el esquema para la API de esquemas. Crea y gestiona un esquema dentro de una base de datos PostgreSQL.
-   Server: Es el esquema para la API de servidores. Crea y administra un servidor externo en un servidor PostgreSQL.
-   Slot: Es el esquema para la API de Slots. Crea y administra un slot de replicación en un servidor PostgreSQL.
-   StoreConfig: Configura cómo el controlador de GCP debe almacenar los detalles de conexión.
-   Subscription: Es el esquema para la API de suscripciones.

### 2. Campos requeridos del recurso Database
<!-- Completa aquí -->
¿Qué campos son requeridos en spec.forProvider? ¿Cuáles son opcionales?
De acuerdo a la documentacion no hay campos requeridos u mandatorios dentro del objeto spec.forProvider.
El objeto forProvider en si mismo esta marcado como requerido, esto significa que se puede declarar un bloque forProvider:{} vacio
y el recurso se creará utilizando los valores por defecto del servidor.

Como opcionales se tienen los siguientes campos:
-   allowConnections (boolean): Define si se permiten conexiones de usuarios a esta base de datos.
-   connectionLimit (number): El límite máximo de conexiones simultáneas permitidas.
-   encoding (string): La codificación de caracteres (por ejemplo, UTF8).
-   isTemplate (boolean): Define si esta base de datos en sí misma puede ser usada posteriormente como una plantilla.
-   lcCollate (string): La configuración de ordenación de caracteres (Collation).
-   lcCtype (string): La configuración de clasificación de caracteres (Character Classification).
-   name (string): El nombre explícito que tendrá la base de datos en PostgreSQL.
-   owner (string): El rol/usuario que será dueño de la base de datos.
-   tablespaceName (string): El espacio de tablas (Tablespace)  donde se almacenará físicamente la base de datos
-   template (string): El nombre de la base de datos plantilla a partir de la cual se creará esta nueva base de datos.

### 3. Información requerida por el ProviderConfig
<!-- Completa aquí -->
Los campos requeridos para el recurso ProviderConfig son:
```
spec:
    credentials:
        env:
            name:
        fs:
            path:
        secretRef:
            key:
            name:
            namespace:
        source:
status:
    conditions:
        lastTransitionTime:
        reason:
        status:
        type:    
```

