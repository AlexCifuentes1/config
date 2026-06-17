# 🎬 Stream Player - DASH DRM Reproductor

Reproductor de streaming DASH con soporte para DRM (Widevine, ClearKey), optimizado para transmisiones en vivo con bajo delay.

## ✨ Características

- ⚡ **Bajo Delay**: Streaming en vivo con solo 6 segundos de delay
- 🔒 **DRM Protegido**: Soporte para Widevine y ClearKey
- 🎯 **LIVE Streaming**: Optimizado para transmisiones en directo
- 📱 **Responsive**: Funciona en desktop, tablet y móvil
- 🎨 **Interfaz Personalizable**: UI estilo Bitmovin incluida
- 🛠️ **Fácil de Usar**: Basado en Shaka Player 4.3.5

## 📦 Reproductores Incluidos

### 1. **Reproductor LIVE (6 segundos)**
- Ideal para transmisiones en directo
- Delay mínimo de 6 segundos
- Modo bajo latencia activado
- `stream_player_live_low_delay.html`

### 2. **Reproductor Estable**
- Para streaming con máxima estabilidad
- Buffer de 120 segundos
- Detección automática de stalls
- `stream_player_stable.html`

### 3. **Reproductor Personalizado (Bitmovin Style)**
- Interfaz elegante personalizada
- Controles personalizados
- Barra de progreso amarilla
- `stream_player_bitmovin_style.html`

## 🚀 Instalación en GitHub Pages

### Opción 1: Crear nuevo repositorio

1. **Crea un nuevo repositorio** en GitHub:
   - Nombre: `tu-usuario.github.io` (donde tu-usuario es tu username)
   - Descripción: "Stream Player - DASH DRM Reproductor"
   - Público ✓

2. **Clona el repositorio**:
```bash
git clone https://github.com/tu-usuario/tu-usuario.github.io.git
cd tu-usuario.github.io
```

3. **Añade los archivos**:
```bash
# Copia todos los archivos HTML a la carpeta
cp *.html ./
```

4. **Sube a GitHub**:
```bash
git add .
git commit -m "Agregados reproductores Stream Player"
git push origin main
```

5. **Accede a tu sitio**:
```
https://tu-usuario.github.io
```

### Opción 2: Usar un repositorio existente

1. **Activa GitHub Pages** en tu repositorio:
   - Ve a Settings → Pages
   - Branch: `main`
   - Folder: `/ (root)`

2. **Sube los archivos** a la raíz del repositorio

3. Tu sitio estará en: `https://tu-usuario.github.io/nombre-repositorio`

## 💻 Uso Local

Simplemente abre el archivo `index.html` en tu navegador:

```bash
# Con Python 3
python -m http.server 8000

# Con Python 2
python -m SimpleHTTPServer 8000

# Con Node.js
npx http-server
```

Luego abre: `http://localhost:8000`

## 📋 Estructura

```
├── index.html                              # Landing page principal
├── stream_player_live_low_delay.html       # Reproductor LIVE (6s)
├── stream_player_stable.html               # Reproductor Estable
├── stream_player_bitmovin_style.html       # Reproductor Personalizado
├── player_no_ads.html                      # Reproductor sin ads
└── README.md                               # Este archivo
```

## 🔧 Configuración

### Cambiar URL del Stream

En cualquier reproductor, modifica esta línea:

```javascript
await player.load('https://tu-stream-aqui.mpd');
```

### Configurar DRM ClearKey

```javascript
player.configure({
    drm: {
        clearKeys: {
            'KEY_ID': 'KEY_VALUE'  // Reemplaza con tu llave
        }
    }
});
```

### Ajustar Buffer (Latencia)

```javascript
streaming: {
    bufferingGoal: 60,        // Segundos de buffer
    rebufferingGoal: 10,      // Segundos antes de reproducir
    lowLatencyMode: true      // Modo bajo latencia
}
```

## 🌐 Requisitos

- Navegador moderno (Chrome, Firefox, Edge, Safari)
- Soporte para DASH
- Soporte para EME (Encrypted Media Extensions)
- Stream DASH (.mpd)

## 📝 Ejemplo de Stream

```
URL: https://ejemplo.com/stream.mpd
DRM: ClearKey
KeyID: 5983506f3f2e0b6df98fd1856adf45b6
Key: d2ae7ea26cfdc61ba0f71771539ff87f
```

## 🐛 Solución de Problemas

| Problema | Solución |
|----------|----------|
| No reproduce | Verifica que el stream sea válido y accesible |
| Se traba | Usa el reproductor "Estable" con más buffer |
| Mucho delay | Usa el reproductor "LIVE" con delay de 6s |
| CORS error | El servidor está bloqueando solicitudes cross-origin |
| Sin audio | Verifica que el stream incluya pista de audio |

## 📚 Documentación Oficial

- [Shaka Player Docs](https://shaka-player-demo.appspot.com/docs/)
- [DASH Standard](https://dashif.org/)
- [GitHub Pages Docs](https://docs.github.com/es/pages)

## 📄 Licencia

MIT - Libre para usar en proyectos comerciales y privados

## 🤝 Contribuciones

Las contribuciones son bienvenidas. Abre un issue o un pull request.

## 📧 Contacto

Para preguntas o sugerencias, abre un issue en el repositorio.

---

**Construido con ❤️ usando Shaka Player 4.3.5**
