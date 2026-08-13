# Repositorio de extensiones para Aniyomi

Extensiones personales de manga/manhwa/manhua en español (uso experimental).

## Cómo añadirlo en Aniyomi

Ajustes → Explorar → **Repositorios de extensiones (manga)** → Añadir, y pega esta URL
**BASE** (sin `/index.min.json` al final):

```
https://raw.githubusercontent.com/JuanManiglia/aniyomi-repo/main
```

Aniyomi (0.18+) valida el repo leyendo `repo.json` de esa base, y luego carga la lista
desde `index.min.json`. Como el `repo.json` declara la huella de firma de los APKs, las
extensiones se instalan ya confiadas.

Luego ve a Explorar → Extensiones y instala las que quieras (12 fuentes ES).

## Estructura
- `repo.json` — metadatos del repo + huella SHA-256 del certificado de firma.
- `index.min.json` — índice de extensiones (nombre, paquete, versión, nsfw, baseUrl, id).
- `apk/*.apk` — los APKs (debug-signed con la misma clave).

El código fuente no se publica aquí; solo los APKs compilados y los índices.
