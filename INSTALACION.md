# 📝 Guía de Instalación - Aula de Informática

## 🚀 Paso 1: Crear el repositorio en GitHub

1. Ve a GitHub y haz clic en **"New repository"**
2. Nombre: `Aula-Informatica`
3. Descripción: "Sistema de reserva del aula de informática - CEIP Puente de Simancas"
4. Público ✅
5. **NO** añadas README, .gitignore ni licencia (ya los tienes)
6. Crea el repositorio

---

## 📦 Paso 2: Subir archivos

Sube estos archivos a la raíz del repositorio:

```
Aula-Informatica/
├── index.html           ✅ (archivo principal)
├── manifest.json        ✅ (configuración PWA)
├── icon-192.png         ⚠️ (crear icono verde)
├── icon-512.png         ⚠️ (crear icono verde)
└── README.md            ✅ (documentación)
```

---

## 🎨 Paso 3: Crear los iconos

### Opción A: Canva (recomendado)

1. Ve a https://canva.com
2. Crea diseño 512x512px
3. **Diseño sugerido:**
   - Fondo: Verde #10b981
   - Icono: Ordenador de escritorio en blanco
   - Texto: "AI" o "Info"
4. Descarga como PNG:
   - 512x512 → guarda como `icon-512.png`
   - Cambia tamaño a 192x192 → guarda como `icon-192.png`

### Opción B: Reutilizar iconos de portátiles

```bash
# Si no quieres complicarte, copia los iconos de portátiles
# y renómbbralos (funcionará igual)
```

---

## ⚙️ Paso 4: Activar GitHub Pages

1. En tu repositorio, ve a **Settings**
2. En el menú lateral, **Pages**
3. En "Source" selecciona: **Deploy from a branch**
4. Branch: **main** (o master)
5. Folder: **/ (root)**
6. Guarda

---

## 🔥 Paso 5: Firebase (USAR EL MISMO PROYECTO)

**✅ NO necesitas crear nuevo proyecto**

La app ya está configurada para usar tu proyecto existente:
- Project: `app-reserva-de-portatiles`
- Las reservas se guardan en: `aula-informatica/` (ruta diferente)

**Si quieres verificar las reglas de Firebase:**

```json
{
  "rules": {
    "reservas": {
      ".read": true,
      ".write": true
    },
    "aula-informatica": {
      ".read": true,
      ".write": true
    }
  }
}
```

---

## ✅ Paso 6: Verificar

Tu app estará disponible en:
```
https://luisgeria.github.io/Aula-Informatica/
```

**Prueba que funcione:**
1. Abre la URL
2. Debe aparecer el punto verde "Conectado"
3. Debe mostrar la tabla de la semana actual
4. Haz una reserva de prueba
5. Comprueba que se sincroniza en otro dispositivo

---

## 📱 Paso 7: Compartir con profes

Comparte el link:
```
https://luisgeria.github.io/Aula-Informatica/
```

En móvil, pueden instalarla como app desde el navegador.

---

## 🎯 Resumen de URLs

**Portátiles:**
- https://luisgeria.github.io/App-para-reserva-de-portatiles/

**Aula Informática:**
- https://luisgeria.github.io/Aula-Informatica/

---

## 🆘 Problemas comunes

**No aparece la página:**
- Espera 2-3 minutos después de activar GitHub Pages
- Verifica que los archivos estén en la raíz (no en carpetas)

**Error 404 en la app instalada:**
- Verifica que el `manifest.json` tenga las rutas correctas con `/Aula-Informatica/`

**No se sincronizan las reservas:**
- Verifica las reglas de Firebase
- Comprueba la consola del navegador (F12) para ver errores

---

¡Listo! 🎉
