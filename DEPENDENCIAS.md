# Dependencias de Biblioteca ePub

Librerías de terceros que lleva cada zip de la versión 1.1.0, con su versión exacta. Se actualiza en cada versión.

Cada entrega usa las versiones más nuevas que admite su sistema operativo, por eso no son iguales en todas.

## Librerías directas

| Librería       | Windows 10/11 (64 bits) | Windows 7 (32 bits) | Linux          | Linux legacy     | macOS         | macOS legacy     |
|----------------|-------------------------|---------------------|----------------|------------------|---------------|------------------|
| Python         | 3.13.15                 | 3.8.10              | 3.13           | 3.10.21          | 3.12.10       | 3.8.10           |
| Interfaz       | PySide6 6.11.2          | PySide2 5.15.2.1    | PySide6 6.11.2 | PySide2 5.15.2.1 | PySide6 6.7.2 | PySide2 5.15.2.1 |
| Qt             | 6.11.2                  | 5.15.2              | 6.11.2         | 5.15.2           | 6.7.2         | 5.15.2           |
| requests       | 2.34.2                  | 2.32.4              | 2.34.2         | 2.34.2           | 2.34.2        | 2.32.4           |
| PySocks        | 1.7.1                   | 1.7.1               | 1.7.1          | 1.7.1            | 1.7.1         | 1.7.1            |
| beautifulsoup4 | 4.15.0                  | 4.15.0              | 4.15.0         | 4.15.0           | 4.15.0        | 4.15.0           |
| lxml           | 6.1.3                   | 6.1.3               | 6.1.3          | 6.1.3            | 6.1.3         | 6.1.3            |
| libtorrent     | 2.1.1                   | 2.0.9               | 2.1.1          | 2.0.9            | 2.0.15        | 2.0.9            |
| cryptography   | 50.0.1                  | 42.0.8              | 50.0.2         | 50.0.2           | 48.0.1        | 47.0.0           |
| keyring        | no lleva                | no lleva            | 25.7.0         | 25.7.0           | 25.7.0        | 25.5.0           |

## Librerías indirectas

Las que traen las anteriores.

| Librería           | Windows 10/11 (64 bits) | Windows 7 (32 bits) | Linux     | Linux legacy | macOS     | macOS legacy |
|--------------------|-------------------------|---------------------|-----------|--------------|-----------|--------------|
| urllib3            | 2.8.0                   | 2.2.3               | 2.8.0     | 2.8.0        | 2.8.0     | 2.2.3        |
| certifi            | 2026.7.22               | 2026.7.22           | 2026.7.22 | 2026.7.22    | 2026.7.22 | 2026.7.22    |
| idna               | 3.20                    | 3.15                | 3.20      | 3.20         | 3.20      | 3.15         |
| charset-normalizer | 3.5.1                   | 3.5.1               | 3.5.2     | 3.5.2        | 3.5.1     | 3.5.1        |
| soupsieve          | 2.10                    | 2.7                 | 2.10      | 2.10         | 2.10      | 2.7          |
| cffi               | 2.1.1                   | 1.17.1              | 2.1.1     | 2.1.1        | 2.1.1     | 1.17.1       |
| pycparser          | 3.0                     | 2.23                | 3.0       | 3.0          | 3.0       | 2.23         |
| shiboken           | 6.11.2                  | 5.15.2.1            | 6.11.2    | 5.15.2.1     | 6.7.2     | 5.15.2.1     |
| SecretStorage      | no lleva                | no lleva            | 3.5.0     | 3.5.0        | no lleva  | no lleva     |
| jeepney            | no lleva                | no lleva            | 0.9.0     | 0.9.0        | no lleva  | no lleva     |

## Notas

- Windows 7, Linux legacy y macOS legacy usan PySide2 (Qt 5.15), que ya no recibe actualizaciones de seguridad. Son para equipos que no pueden correr la versión normal. En Windows 7, cryptography queda en una versión vieja porque las nuevas requieren Windows 10.
- macOS 11 (Big Sur) queda en PySide6 6.7.2, la última que funciona en ese sistema.
- cryptography verifica la firma de la configuración remota, que es la que anuncia las versiones nuevas. Además, la aplicación descarta cualquier zip de actualización cuyo SHA-256 no coincida con el firmado.
- Cada zip incluye también bibliotecas del sistema (Qt, OpenSSL, ICU y otras).
