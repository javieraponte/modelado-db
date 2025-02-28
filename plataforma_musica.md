[Diseña un modelo de base de datos para una plataforma donde productores suben sus tracks y DJs pueden comprarlos o descargarlos. Considera entidades como artistas, canciones, géneros, usuarios y transacciones.]:#

# Plataforma de Música

Base de datos para una plataforma donde productores suben sus instrumentales (tracks) y DJ's o cantantes pueden comprarlos para descargarlos.

## Lista de Entidades

### Artistas **(EC)**
- artista_id **(PK)**
- canciones **(FK)**
- nombre
- telefono
- email

### Canciones **(ED)**
- cancion_id **(PK)**
- artista_id **(FK)**
- nombre_canción
- genero_musical
- caratula
- clave
- bpm
- precio

### Géneros musicales **(EC|EP)**
- genero_id **(PK)**
- canción_id **(FK)**
- artista_id **(FK)**
- tipo
- cantidad

### Usuarios
- usuario_id **(PK)**
- nombre
- email
- telefono

### Transacciones **(ED|EC)**
- transaccion_id **(PK)**
- canción_id **(FK)**
- estado