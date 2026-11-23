# La oruga del conocimiento - versión web

Juego educativo en HTML5, CSS y JavaScript. Conserva las dos escenas, las preguntas de selección y Verdadero/Falso, el árbol de rutas, el cierre de una rama al fallar, la animación de la oruga y el manejo exclusivo mediante clic o pantalla táctil.

## Archivos

```text
juego-oruga-web/
├── index.html
├── css/estilos.css
├── js/juego.js
└── images/arbol.png
```

## Implementación en Eclipse

### 1. Preparar Eclipse
1. Instale **Eclipse IDE for Enterprise Java and Web Developers** o **Eclipse IDE for Java Developers**.
2. Descomprima `juego-oruga-web.zip` en una carpeta local.

### 2. Importar el proyecto ya creado
1. Abra Eclipse.
2. Seleccione **File > Import**.
3. Elija **General > Projects from Folder or Archive** y pulse **Next**.
4. Pulse **Directory** y seleccione la carpeta `juego-oruga-web` descomprimida.
5. Marque el proyecto detectado y pulse **Finish**.
6. Si Eclipse no muestra cambios recientes, haga clic derecho en el proyecto y elija **Refresh**.

### 3. Alternativa: crearlo manualmente
1. Seleccione **File > New > Project > General > Project**.
2. Use el nombre `juego-oruga-web`.
3. Cree las carpetas `css`, `js` e `images` con **New > Folder**.
4. Cree `index.html` en la raíz, `estilos.css` dentro de `css` y `juego.js` dentro de `js`.
5. Copie `arbol.png` a `images`.
6. Pegue en cada archivo el contenido incluido en este paquete.

### 4. Ejecutarlo desde Eclipse
La prueba más simple es abrir `index.html` con **Open With > Web Browser**. Para una prueba más fiel a un sitio publicado, use un servidor local:

1. Abra una terminal en la carpeta del proyecto.
2. Ejecute `py -m http.server 8080` en Windows, o `python3 -m http.server 8080` en Linux/macOS.
3. Abra `http://localhost:8080` en Edge, Chrome o Firefox.
4. Detenga el servidor con `Ctrl+C`.

También puede instalar **Eclipse Web Developer Tools** desde **Help > Eclipse Marketplace** y configurar un servidor HTTP, pero este proyecto es estático y no necesita Tomcat, Maven ni Java en producción.

## Personalización

### Autores y créditos
Edite el evento de `btn-creditos` en `js/juego.js` y sustituya los textos entre corchetes.

### Preguntas
Edite el arreglo `preguntas` en `js/juego.js`. La propiedad `correcta` debe coincidir exactamente con una opción.

### Rutas
Edite `mapaBase`. Cada nodo tiene `x`, `y`, número de pregunta `p` y un arreglo `rutas`. Cada ruta apunta a otro nodo mediante `a`.

### Imagen
Sustituya `images/arbol.png` conservando el nombre. Se recomienda proporción 1000 x 700.

## Publicación
Suba la carpeta completa a GitHub Pages, Azure Static Web Apps o un servidor institucional. Mantenga las rutas relativas y publique `index.html`, `css`, `js` e `images`. No suba solo el archivo HTML.

## Pruebas mínimas
- Menú, instrucciones y créditos.
- Respuestas correctas e incorrectas.
- Cierre rojo de una rama al fallar.
- Selección de las ramas doradas.
- Movimiento hasta la copa.
- Reinicio y regreso al menú.
- Edge, Chrome y Firefox; escritorio y tableta.
