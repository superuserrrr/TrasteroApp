# TrasteroApp

**Inventario minimalista para tu trastero**, construido con Electron. Guarda, busca y elimina objetos de forma rápida y sencilla, sin depender de Excel ni de herramientas externas.

## 📝 Descripción

TrasteroApp es una aplicación de escritorio para macOS (y otras plataformas) que te permite:

- Añadir objetos con su nombre y ubicación.
- Buscar en tiempo real entre los elementos archivados.
- Eliminar entradas cuando ya no las necesites.
- Conservar tus datos en un fichero JSON (`items.json`) dentro de la carpeta de datos de la app, para que puedas hacer copia de seguridad o migrar fácilmente.

La interfaz es minimalista y responsive, inspirada en un estilo retro-industrial pero con toques modernos. Está diseñada para distraerte lo mínimo y ayudarte a centralizar la gestión de tu trastero.

## 🚀 Casos de uso

- **Mudanza**: Lleva un control de dónde está cada caja o mueble y evita perder cosas.
- **Almacenamiento temporal**: Si guardas equipamiento deportivo, herramientas o decoración estacional, sabrás siempre qué hay y dónde.
- **Gestión de colecciones**: Libros, vinilos, gadgets… Organiza tu colección y accede rápido a la ubicación de cada ítem.
- **Control rápido**: Ideal para profesionales que necesitan inventariar material de obra o eventos.

## ⚙️ Instalación y uso

1. **Clona este repositorio**  
   ```bash
   git clone https://github.com/tu-usuario/trastero-app.git
   cd trastero-app
   ```

2. **Instala dependencias**  
   ```bash
   npm install
   ```

3. **Inicia la aplicación**  
   ```bash
   npm start
   ```

   La app se abrirá en una ventana de Electron.

## 📦 Empaquetado

Para generar un ejecutable macOS (`.app`):

1. Instala el empaquetador (una sola vez):  
   ```bash
   npm install -g electron-packager
   ```

2. En la raíz del proyecto ejecuta:  
   ```bash
   electron-packager . TrasteroApp --platform=darwin --arch=x64 --out=dist --overwrite
   ```

   El resultado estará en `dist/TrasteroApp-darwin-x64/TrasteroApp.app`.

## 💾 Almacenamiento de datos

Los registros se guardan en un fichero JSON dentro de la carpeta de datos de la app:

```
~/Library/Application Support/TrasteroApp/items.json
```

Puedes respaldar o compartir ese `items.json` para migrar tus datos.
