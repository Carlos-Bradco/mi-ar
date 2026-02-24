# WebAR con MindAR + A-Frame (GitHub Pages)

Este proyecto muestra dos imágenes 2D emergiendo de un plano impreso que actúa como **marcador**. Funciona en el navegador móvil y puede publicarse en **GitHub Pages**.

## Estructura
```
index.html
img1.png            # imagen 1 (horno)
img2.png            # imagen 2 (refrigerador)
targets.mind        # archivo del marcador (GENERAR)
marker-reference.jpg (opcional, solo referencia visual)
.nojekyll
```

## 1) Generar `targets.mind`
MindAR requiere compilar la imagen del marcador a un archivo `.mind`.

1. Abre el **MindAR Image Target Compiler**: https://hiukim.github.io/mind-ar-js-doc/tools/compile/
2. Sube la imagen del **plano** (el marcador). Si la tienes como `marker-reference.jpg`, úsala.
3. Ajusta el tamaño del lado mayor a **1024–1536 px**.
4. Descarga el archivo generado `targets.mind` y colócalo en la **raíz** del proyecto.

> Consejo: recorta márgenes blancos grandes y asegúrate de que el plano tenga alto contraste.

## 2) Probar localmente
Abre `index.html` con un servidor local (por ejemplo, VS Code Live Server) desde **https** si tu navegador lo exige para la cámara. En móvil, lo normal es publicarlo con GitHub Pages.

## 3) Publicar en GitHub Pages
1. Crea un repositorio **público** y sube **todos los archivos**.
2. Ve a **Settings → Pages**.
3. En **Source**, elige `Branch: main` y `Folder: /root` → **Save**.
4. Espera 1–2 minutos y abre la URL `https://TU_USUARIO.github.io/TU_REPO/` en el móvil.
5. Acepta permisos de cámara y apunta al **plano impreso**.

## 4) Ajustes finos
- Si las imágenes no emergen desde el lugar exacto (horno/refrigerador), ajusta las posiciones de `ovenAnchor` y `fridgeAnchor` en `index.html`.
- Si la fila superior queda muy dentro o fuera del borde, modifica `data-target-height` en el elemento `#config`.

## Créditos
- [A‑Frame](https://aframe.io/)
- [MindAR](https://github.com/hiukim/mind-ar-js)
