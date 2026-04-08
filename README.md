<div align="center">

```
██╗  ██╗ ██████╗██╗  ██╗ █████╗ ███╗   ██╗ ██████╗ ███████╗███╗   ██╗ ██████╗ ██╗    ██╗
╚██╗██╔╝██╔════╝██║  ██║██╔══██╗████╗  ██║██╔════╝ ██╔════╝████╗  ██║██╔═══██╗██║    ██║
 ╚███╔╝ ██║     ███████║███████║██╔██╗ ██║██║  ███╗█████╗  ██╔██╗ ██║██║   ██║██║ █╗ ██║
 ██╔██╗ ██║     ██╔══██║██╔══██║██║╚██╗██║██║   ██║██╔══╝  ██║╚██╗██║██║   ██║██║███╗██║
██╔╝ ██╗╚██████╗██║  ██║██║  ██║██║ ╚████║╚██████╔╝███████╗██║ ╚████║╚██████╔╝╚███╔███╔╝
╚═╝  ╚═╝ ╚═════╝╚═╝  ╚═╝╚═╝  ╚═╝╚═╝  ╚═══╝ ╚═════╝ ╚══════╝╚═╝  ╚═══╝ ╚═════╝  ╚══╝╚══╝ 
```

**Real-time currency converter · Multi-language · Responsive**

[![Demo](https://img.shields.io/badge/Live%20Demo-→%20xchangenow.vixodev.site-4ade80?style=for-the-badge&logo=vercel&logoColor=white)](https://xchangenow.vixodev.site)
[![JavaScript](https://img.shields.io/badge/JavaScript-Vanilla-f7df1e?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![License](https://img.shields.io/badge/License-MIT-a78bfa?style=for-the-badge)](LICENSE)

</div>

---

## ¿Qué es XChangeNow?

**XChangeNow** es un conversor de divisas en tiempo real que consulta tasas de cambio actualizadas directamente desde la [ExchangeRate API](https://api.exchangerate-api.com). Está construido con JavaScript puro — sin frameworks, sin dependencias, sin complicaciones.

> Convierte entre más de 150 monedas al instante, con banderas automáticas y soporte para español e inglés.

---

## Demo

🌐 **[https://xchangenow.vixodev.site](https://xchangenow.vixodev.site)**

---

## Funcionalidades

| Feature | Descripción |
|---|---|
| 💱 **Conversión en tiempo real** | Tasas actualizadas en cada consulta vía API |
| 🌍 **Múltiples divisas** | Soporte para USD, EUR, CLP, ARS y más de 160 monedas |
| 🏳️ **Banderas automáticas** | Visualización de la bandera según la moneda seleccionada |
| 🌐 **Multilenguaje** | Interfaz disponible en Español e Inglés |
| 📱 **Diseño responsive** | Adaptado a móvil con menú hamburguesa |
| ⚡ **Sin dependencias** | 100% Vanilla JS, sin frameworks |

---

## Stack Tecnológico

```
Frontend          API & Recursos
─────────         ──────────────
HTML5             ExchangeRate API  →  tasas de cambio
CSS3              FlagCDN           →  banderas de países
CSS3              FontAwesomeCDN    →  iconos
JavaScript ES6+
i18n

```

---

## Cómo funciona

```
Usuario ingresa monto
        ↓
Selecciona moneda origen → destino
        ↓
fetch() → api.exchangerate-api.com
        ↓
Cálculo de conversión
        ↓
Resultado formateado con Intl.NumberFormat
```

---

## Estructura del Proyecto

```
XChangeNow/
├── index.html          # Estructura principal, lógica, fetchAPI, validaciones
├── about.html           # Sobre la web
├── contact.html         # Mis redes sociales
└── favicon.ico
```

---

## API

La aplicación consume la **ExchangeRate API** de forma gratuita y sin autenticación:

```
GET https://api.exchangerate-api.com/v4/latest/{CURRENCY}
```


---

## Internacionalización (i18n)

El sistema de idiomas está implementado con un objeto `translations` en JavaScript. El contenido se actualiza **dinámicamente sin recargar la página**.

```js
const translations = {
  es: { /* textos en español */ },
  en: { /* textos en inglés */ }
};
```

**Idiomas soportados:**
- 🇪🇸 Español
- 🇺🇸 Inglés

---

## Detalles técnicos destacados

- **`fetch()`** para consumo asíncrono de la API
- **`Intl.NumberFormat`** para formateo localizado de monedas
- **`lastConversion`** para gestión de estado entre conversiones
- **Manipulación del DOM** sin librerías externas
- Eventos: `submit`, `change`, `DOMContentLoaded`

---

## Validaciones

- ✅ La cantidad debe ser mayor a `0`
- ✅ No se permite convertir entre la misma moneda
- ✅ Manejo de errores de red y respuestas inválidas de la API

---

## Roadmap

- [ ] Rápido
- [ ] Intuitivo
- [ ] Modo oscuro 🌙
- [ ] Ingles y español

---

## Licencia

Distribuido bajo la licencia **MIT**. Ver [`LICENSE`](LICENSE) para más información.

---

<div align="center">

Hecho con 💚 por **[dev-vixo](https://github.com/dev-vixo)**

</div>
