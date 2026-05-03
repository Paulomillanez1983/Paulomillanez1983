# PLAY STORE READINESS — MIMI Go

## 1) Estado actual
- Se preparó configuración base para Vercel con rewrites de rutas limpias.
- Se incorporó manifest principal para PWA (pendiente completar íconos reales).
- Se publicaron páginas legales mínimas: privacidad y términos.
- Se agregó estructura Digital Asset Links con placeholder para SHA-256.
- **Pendiente crítico**: el repositorio actual no contiene los HTML/app files funcionales esperados (`index.html`, `hub-clientes.html`, `mimi-servicios/*`, etc.).

## 2) URLs finales objetivo
- https://mimi-transporte.vercel.app/hub-clientes
- https://mimi-transporte.vercel.app/servicios
- https://mimi-transporte.vercel.app/prestador
- https://mimi-transporte.vercel.app/viaje
- https://mimi-transporte.vercel.app/privacidad
- https://mimi-transporte.vercel.app/terminos
- https://mimi-transporte.vercel.app/.well-known/assetlinks.json

## 3) Comandos de prueba local
```bash
npx serve .
# o
python -m http.server 4173
```

## 4) Comandos sugeridos para Bubblewrap
```bash
npm install -g @bubblewrap/cli
bubblewrap init --manifest https://mimi-transporte.vercel.app/manifest.json
bubblewrap build
```

## 5) Datos sugeridos para Bubblewrap
- packageId: `com.mimigo.app`
- appName: `MIMI Go`
- launcherName: `MIMI Go`
- host: `mimi-transporte.vercel.app`
- startUrl: `/hub-clientes`

## 6) Actualización de SHA-256 (obligatoria antes de release)
Después de generar keystore o habilitar Play App Signing, obtener SHA-256 real y actualizar:
- `.well-known/assetlinks.json`

## 7) Checklist Play Console
- Crear app
- Definir nombre
- Definir categoría
- Cargar política de privacidad
- Subir App Bundle `.aab`
- Completar ficha de Play Store
- Subir capturas
- Subir ícono 512
- Completar clasificación de contenido
- Completar seguridad de datos
- Configurar países/regiones
- Enviar a revisión
