# 🏍️ MotoAR — Catálogo de Motos Argentina

> Encontrá, comparás y decidís. Todo en un solo lugar.

MotoAR es un catálogo interactivo de motocicletas disponibles en Argentina, con precios reales de MercadoLibre, especificaciones técnicas completas y comparador lado a lado. Desarrollado como sitio estático de una sola página, sin dependencias externas ni backend.

---

## ✨ Funcionalidades

- **Catálogo de 183 modelos** — desde urbanas económicas de 70cc hasta naked y adventure de 750cc+
- **Ficha técnica completa** — motor, potencia, peso, frenos, transmisión y más
- **Comparador lado a lado** — seleccionás dos motos y las comparás spec a spec, con ganadores destacados
- **Filtros avanzados** — por cilindrada, marca, tipo y precio
- **Buscador en tiempo real** — por nombre, marca o tipo
- **Ordenamiento** — por precio o cilindrada, ascendente o descendente
- **Link a Motozuni / MercadoLibre** — acceso directo desde cada ficha y card
- **Diseño oscuro y elegante** — optimizado para desktop

---

## 🏷️ Marcas incluidas

| Internacionales | Nacionales / Regionales |
|---|---|
| Bajaj | Corven |
| Benelli | Gilera |
| CF Moto | Ika |
| Suzuki | Keller |
| TVS | Mondial |
| Kymco | Motomel |
| Keeway | Siam |
| SYM | Zanella |
| Morbidelli | Jawa |

---

## 📋 Segmentos incluidos

| Segmento | Rango de precio | Ejemplos |
|---|---|---|
| Económicas | Hasta $1,5M | Gilera Smash 110, Corven Energy 110, Motomel Blitz 110 |
| Media baja | $1,5M – $3,5M | Bajaj Rouser NS 125, TVS Raider 125, Corven Hunter 150 |
| Media | $3,5M – $8M | Motomel Sirius 190, Bajaj Rouser NS 200, TVS RTR 200 4V |
| Media alta | $8M – $20M | Bajaj Dominar D250, Benelli TRK 251, CFMoto NK 400 |
| Premium | +$20M | Benelli TRK 502, Benelli TRK 702, Benelli 752 S |

---

## 🛵 Tipos de moto

| Tipo | Descripción |
|---|---|
| CUB / Económica | Motos de trabajo y bajo costo, 107–125cc |
| Naked / Street | Motos urbanas deportivas, 98cc–754cc |
| Scooter | Automáticas urbanas, 80–508cc |
| Enduro / On-Off | Doble propósito campo/ruta, 125–250cc |
| Adventure | Turismo off-road, 150–698cc |
| Deportiva | Sport puro, ej. TVS RR 310 |
| Custom / Chopper | Estilo cruiser, 149–500cc |
| Utilitario | Cargo y cuatriciclos |
| DAX | Estilo retro urbano, 70–86cc |

---

## 🚀 Cómo usar

### Correr localmente
No requiere instalación. Simplemente abrí el archivo en tu navegador:

```bash
# Opción 1: doble clic en el archivo
motoar_v4.html

# Opción 2: con Python (para evitar restricciones CORS locales)
python3 -m http.server 8080
# Luego abrí http://localhost:8080
```

---

## 🗂️ Estructura del proyecto

```
motoar/
├── motoar_v4.html    # Toda la aplicación (HTML + CSS + JS en un solo archivo)
└── README.md         # Este archivo
```

El proyecto es intencionalmente un archivo único. No hay frameworks, no hay npm, no hay build process. Abrís el HTML y funciona.

---

## 🖼️ Imágenes

Las imágenes se cargan desde **ImgBB** (i.ibb.co), sin necesidad de alojar imágenes propias. Si una imagen no carga, el sitio muestra automáticamente un emoji de reemplazo según el tipo de moto.

---

## 💡 Cómo agregar un modelo nuevo

Abrí `motoar_v4.html` y buscá el array `const M=[`. Cada moto tiene esta estructura:

```javascript
{
  id: 184,                         // número único
  m: 'Honda',                      // marca
  n: 'CB 300F',                    // nombre
  cc: 293,                         // cilindrada numérica
  t: 'naked',                      // naked | scooter | onoff | adventure | sport | custom | utilitario | cub | dax
  p: '$9.000.000',                 // precio formateado (o 'Consultar')
  pn: 9000000,                     // precio numérico para filtros y comparador
  img: 'https://URL-foto.webp',    // imagen principal
  url: 'https://motozuni.com/...',  // link a Motozuni / ML
  specs: {
    Motor: '293cc monocil. DOHC FI',
    Potencia: '30 HP',
    Peso: '164 kg',
    Frenos: 'Disco/Disco+ABS',
    Caja: '6 vel.',
    Tipo: 'Naked',
  }
}
```

---

## 📱 Compatibilidad

| Navegador | Soporte |
|---|---|
| Chrome / Edge | ✅ Completo |
| Firefox | ✅ Completo |
| Safari (iOS / macOS) | ✅ Completo |
| Mobile (Android / iPhone) | ⚠️ Funcional (optimizado para desktop) |

---

## 📄 Licencia

Código: libre para uso personal y comercial.  
Imágenes: alojadas en ImgBB — ver términos en ibb.co.

---

## 🛠️ Construido con

- HTML5 semántico
- CSS3 (variables, grid, flexbox, transitions)
- JavaScript vanilla (sin frameworks)
- ImgBB (imágenes)
- Motozuni / MercadoLibre (fuente de precios y datos, junio 2026)

---

*Precios indicativos relevados de Motozuni y MercadoLibre. Actualizados junio 2026. Consultá con tu concesionario oficial.*
