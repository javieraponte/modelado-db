[Diseña un modelo de base de datos para una plataforma donde productores suben sus tracks y DJs pueden comprarlos o descargarlos. Considera entidades como artistas, canciones, géneros, usuarios y transacciones.]:#

# Plataforma de Música

Base de datos para una plataforma donde productores suben sus instrumentales (tracks) y DJ's o cantantes pueden comprarlos para descargarlos.

## Lista de Entidades

### Artistas **(EC)**
- artista_id **(PK)**
- cancion 
- nombre 
- telefono **(UQ)**
- email **(UQ)**

### Cancion **(ED)**
- cancion_id **(PK)**
- artista_id **(FK)**
- nombre_canción **(UQ)**
- genero_musical
- clave
- bpm
- precio

### Género_musical **(EC|EP)**
- genero_id **(PK)**
- canción_id **(FK)**
- artista_id **(FK)**
- tipo
- cantidad

### Usuarios
- usuario_id **(PK)**
- nombre **(UQ)**
- email **(UQ)**
- telefono **(UQ)**

### Transaccion **(ED|EC|EP)**
- transaccion_id **(PK)**
- usuario_id **(FK)**
- cancion_id **(FK)**
- estado

## Relaciones

1. Un **artista** tiene **genero_musical** (_1-1_)
2. Una **artista** genera **cancion** (_1-n_)
3. Un **genero_musical** posee **cancion** (_1-n_)
4. Un **usuario** genera **transaccion** (_1-n_)
5. Una **cancion** tiene **transaccion** (_1-n_)

## Diagrama

![plataforma_musica drawio(1)](https://github.com/user-attachments/assets/ea3210f0-9aae-4f22-be34-26815c3e4d90)

## Reglas de Negocio

### Artistas
1. Crear un artista
2. Leer todos los artistas
3. Leer un artista en particular
4. Actualizar un artista
5. Eliminar un artista

## Cancion
1. Crear una canción
2. Leer todas las canciones
3. Leer una cancion en particular
4. Actualizar una cancion
5. Eliminar una cancion
6. Cada que se realice una venta eliminar la cancion

## Genero musical
1. Crear un genero musical
2. Leer todos los generos musicales
3. Leer un genero musical en particular
4. Leer todos los artistas de un genero musical
5. Leer todas las canciones de un genero musical
6. Actualizar un genero musical
7. Eliminar un genero musical

## Usuarios
1. Crear un usuario
2. Leer todos los usuarios
3. Leer un usuario en particular
4. Actualizar usuario
5. Eliminar usuario

## Transaccion
1. Crear una transaccion
2. Leer todas las transacciones
3. Leer una transaccion en particular
4. Leer todas las transacciones de un usuario
5. Leer todas las canciones con transacciones
6. Actualizar transaccion
7. Eliminar transaccion
