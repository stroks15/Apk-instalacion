# Apk-instalacion

Repositorio para almacenar instaladores y paquetes de Android. Los archivos de instalación se guardan en la **raíz** del repositorio y se gestionan con **Git LFS**.

## Formatos configurados

Git LFS está configurado para:

- `.apk` — aplicaciones Android.
- `.aab` — Android App Bundles.
- `.apks` — conjuntos de APK.
- `.xapk` — paquetes XAPK.
- `.obb` — archivos de expansión Android.

## Requisito para subir archivos grandes

No subas APK grandes desde el botón **Upload files** del navegador: la interfaz web de GitHub tiene un límite de 25 MB por archivo. Usa Git LFS desde una computadora o desde Termux.

### Instalar Git LFS

En Ubuntu/Debian:

```bash
sudo apt-get update
sudo apt-get install git git-lfs
```

En Termux:

```bash
pkg update
pkg install git git-lfs
```

### Clonar y preparar el repositorio

```bash
git lfs install
git clone https://github.com/stroks15/Apk-instalacion.git
cd Apk-instalacion
```

Copia el APK directamente dentro de esta carpeta (la raíz del repositorio) y ejecuta:

```bash
git lfs ls-files
git add .gitattributes
git add "Nombre-de-la-aplicacion.apk"
git commit -m "Agregar instalador Android"
git push origin main
```

Si agregas varios instaladores, puedes usar:

```bash
git add *.apk *.aab *.apks *.xapk *.obb
```

## Límites y notas

- Git LFS evita guardar el contenido binario pesado en el historial normal de Git.
- GitHub aplica cuotas de almacenamiento y transferencia de Git LFS según el plan y los paquetes de datos disponibles en la cuenta.
- El límite máximo por archivo de Git LFS depende del plan de GitHub; revisa las cuotas antes de subir archivos especialmente grandes.
- Los archivos quedan en la raíz y conservan su nombre original.
- No se borran ni sustituyen archivos existentes al aplicar esta configuración.

## Descargas

Abre el archivo desde la página principal del repositorio. Para distribuir versiones con información de cambios y enlaces de descarga, también puedes crear una publicación en **Releases**.
