# Simple TOTP Generator

Generador de códigos de autenticación de doble factor (TOTP) en un único archivo HTML. 

Nace de la necesidad de eliminar la dependencia de las aplicaciones móviles de autenticación, que suelen ser lentas de abrir, requieren buscar el dispositivo móvil en mitad del flujo de trabajo o quedan bloqueadas si te quedas sin batería.

## Características

- **Sin dependencias de servidor:** Abre el archivo `.html` directamente en cualquier navegador web local.
- **Ideal para Homelab:** Sirve el archivo estático fácilmente en Nginx, Apache, Caddy o dentro de un contenedor en tu infraestructura local.
- **Sin backend:** El cálculo del token de 6 dígitos se realiza íntegramente en el cliente mediante JavaScript.
- **Diseño limpio:** Interfaz minimalista con modo oscuro y barra visual de progreso de 30 segundos.

## Uso

1. Descarga o clona el repositorio.
2. Abre `totp_generator.html` con cualquier editor de texto.
3. Modifica la variable `SECRET_KEY` dentro de la etiqueta `<script>` con tu clave privada en formato Base32:

```javascript
const SECRET_KEY = "TU_CLAVE_PRIVADA_AQUI";
```

4. Guarda el archivo y ábrelo directamente en tu navegador (o súbelo a tu servidor estático).

## Seguridad

Dado que la clave secreta se almacena en texto plano dentro del propio archivo HTML, mantén este archivo únicamente en entornos locales de confianza o tras la autenticación de tu red privada/homelab.
