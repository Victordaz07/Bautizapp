# 💧 BautizApp

**Una app web de un solo archivo, sin conexión, para crear programas e invitaciones de bautismo.**

🌐 **[Read in English](BautizApp-README.md)**

---

## ¿Qué es BautizApp?

BautizApp es una herramienta gratuita que ayuda a miembros, misioneros y líderes de La Iglesia de Jesucristo de los Santos de los Últimos Días a armar rápidamente un **programa de bautismo** y una **invitación de WhatsApp** a juego — sin necesidad de saber diseño, sin servidor, y sin conexión a internet una vez que carga.

Todo funciona en un solo archivo, `Bautizapp.html`. Se abre en cualquier navegador moderno y ya tienes una herramienta de diseño completa: sin instalación, sin proceso de compilación, sin cuenta.

> ⚠️ Esta herramienta **no es un producto oficial** de La Iglesia de Jesucristo de los Santos de los Últimos Días y no está afiliada ni respaldada por la Iglesia. Es un recurso gratuito creado por un miembro para ayudar a hermanos, hermanas, líderes y misioneros a preparar programas de bautismo. El contenido del himnario es propiedad de la Iglesia.

## ✨ Funcionalidades

- **Asistente guiado de 4 pasos** — Evento → Personas → Diseño → Generar, con barra de progreso y validación en cada paso.
- **5 idiomas** — Español, inglés, tagalo, tongano y samoano. Toda la interfaz, la base de himnos y el programa impreso cambian al instante, sin recargar la página.
- **Programa completo** — datos del bautizado, fecha y hora, capilla/dirección, quién conduce, quién ora, quién bautiza, quién confirma, quién habla, quién toca el órgano, y qué pasa mientras el bautizado se cambia de ropa.
- **Selector de himnos** — himnario buscable por idioma, por número o por título, para el himno inicial y final.
- **Selector de diseño** — decenas de fondos de programa e invitación en alta resolución, y "coronas" o imágenes centrales, organizadas por categoría, con vista previa en vivo.
- **Invitación personal de WhatsApp** — un mensaje personalizado más una imagen vertical lista para compartir, generada con los mismos datos.
- **Exportación con un clic** — descarga el programa y la invitación terminados en PDF o como imágenes de alta resolución, o compártelos directamente (Web Share API).
- **Borrador automático + historial** — tu trabajo se guarda automáticamente en el almacenamiento local del navegador; recupera un borrador anterior en cualquier momento desde el panel de Historial.
- **Manual de uso integrado** — guía paso a paso, referencia de campos y consejos, traducidos a los 5 idiomas.
- **Privacidad por diseño** — sin backend, sin analítica, sin cuentas. Tus datos nunca salen de tu dispositivo.
- **Cero dependencias que instalar** — es un solo archivo HTML. Las fuentes y las librerías de PDF/imagen se cargan desde un CDN la primera vez; después, la herramienta sigue funcionando sin conexión.

## 🚀 Cómo empezar

1. Descarga `Bautizapp.html`.
2. Haz doble clic en el archivo (o ábrelo desde tu navegador con `Archivo → Abrir`).
3. Elige tu idioma en la pantalla de bienvenida y toca **Entrar a la herramienta**.
4. Sigue los 4 pasos — tu progreso se guarda automáticamente mientras avanzas.
5. En el último paso, genera y descarga tu programa e invitación.

Sin servidor, sin `npm install`, sin configuración. Eso es toda la instalación.

## 🛠️ Stack técnico

| Capa | Elección |
|---|---|
| Estructura y lógica | HTML5 / CSS3 / JavaScript puro (sin framework) |
| Tipografías | Google Fonts — Cinzel, Dancing Script, Lora, Source Sans 3 |
| Exportación a PDF | [jsPDF](https://github.com/parallax/jsPDF) 2.5.1 |
| Captura de imagen | [html2canvas](https://github.com/niklasvh/html2canvas) 1.4.1 |
| Almacenamiento | `localStorage` del navegador (borradores + historial) |
| Imágenes | Fondos y coronas embebidos como base64 WebP/PNG — sin peticiones de imágenes externas |

Toda la app —maquetado, estilos, lógica, traducciones y assets de imagen— vive en un solo archivo HTML a propósito, para que se pueda compartir, descargar y abrir en cualquier lugar sin pipeline de compilación.

## 📁 Estructura del proyecto

```
Bautizapp.html   ← toda la aplicación (HTML + CSS + JS + assets embebidos)
```

Dentro de ese único archivo:

- `<style>` — todos los estilos de componentes, organizados por sección (hero, stepper, selector de diseño, modales, barra de acciones, hojas de impresión…).
- `<body>` — la pantalla de bienvenida, el asistente de 4 pasos, el selector de diseño, los modales de historial/manual, y las hojas de impresión ocultas usadas para exportar a PDF/imagen.
- `<script>` — el estado de la app, el objeto de traducciones (`T`), las bases de himnos por idioma, la lógica de navegación del asistente, los selectores de diseño, el autoguardado/historial, y el proceso de exportación a PDF/imagen.

## 🌍 Idiomas

Cada texto de la app —etiquetas, placeholders, mensajes de validación, el manual de uso y el himnario— está traducido a:

🇲🇽 Español · 🇺🇸 English · 🇵🇭 Tagalog · 🇹🇴 Tongan · 🇼🇸 Samoan

Cambiar de idioma a mitad de sesión resincroniza toda la interfaz, incluida la búsqueda de himnos, sin perder los datos que ya ingresaste.

## 🔒 Privacidad y uso sin conexión

BautizApp **no** envía ningún dato a un servidor. No hay backend. Los datos del programa de bautismo, el historial de borradores y tu preferencia de idioma se guardan únicamente en el almacenamiento local de tu navegador, en tu propio dispositivo. Una vez que la página cargó, la herramienta sigue funcionando sin conexión a internet.

## 🙌 Créditos

Creado por **Víctor Ruiz** — Segundo Consejero del Cuórum de Élderes · Líder Misional, Barrio Sexto · Estaca San Francisco, California.

- GitHub: [github.com/Victordaz07](https://github.com/Victordaz07)
- Proyecto: [seekergospel.com](https://seekergospel.com)
- Contacto: viruizbc@gmail.com

> «Venid a Cristo, y sed perfeccionados en Él.» — Moroni 10:32

## 📜 Licencia

BautizApp es un recurso gratuito para uso personal y congregacional. El contenido del himnario incluido en la app sigue siendo propiedad de La Iglesia de Jesucristo de los Santos de los Últimos Días.
