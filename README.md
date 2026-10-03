# EVO · Flow Watch Video Prompter

Skill reutilizable para analizar videos de referencia y fotografías reales de relojes de EVO y preparar prompts detallados en español e inglés para Google Flow.

Incluye las directrices de identidad del producto, escudo POEDAGAR en la corona de ajuste, presentación impecable sin polvo ni manchas y exclusión de marcas de agua, usuarios e interfaces sociales. Adapta el formato y la duración al pedido; para el flujo habitual de EVO se utiliza video vertical 9:16 con una duración objetivo de 10 segundos, siempre compatible con las opciones disponibles en Flow.

## Instalar en otra cuenta o equipo

En Codex, con acceso a este repositorio, pega:

```text
$skill-installer Instala la skill flow-watch-video-prompter desde https://github.com/AlvaroCC503/evo-flow-watch-video-prompter/tree/main/.agents/skills/flow-watch-video-prompter
```

El repositorio es privado. En el nuevo equipo necesitas autenticar GitHub como `AlvaroCC503` o como un colaborador con acceso al repositorio. Cambiar de cuenta de ChatGPT no concede acceso a GitHub por sí mismo. Si utilizas otra cuenta de GitHub, el propietario debe invitarla como colaboradora y esa cuenta debe aceptar la invitación.

Tras la instalación, prueba la skill en un nuevo turno. Si no aparece en el selector, reinicia Codex. Si ya está instalada, pide actualizarla desde este repositorio; no elimines una copia modificada sin revisarla primero.

La [documentación oficial de skills](https://learn.chatgpt.com/docs/build-skills) explica la instalación con `$skill-installer` y la detección de skills locales.

## Utilizarla

Coloca las referencias en una carpeta local del proyecto, por ejemplo:

```text
referencias/
  Mi nuevo modelo/
    Video de referencia/
    Fotos de relojes/
    Videos resultado/
```

Luego pide:

```text
Usa $flow-watch-video-prompter en la carpeta "referencias/Mi nuevo modelo". Quiero un video vertical 9:16 para TikTok de 10 segundos. Analiza el video y las fotos, conserva la identidad del reloj y entrégame el prompt en español e inglés y los archivos que debo adjuntar a Flow.
```

La skill inspecciona las referencias, recomienda las imágenes que debes adjuntar y entrega un guion con tiempos y una lista de verificación. No genera ni publica el video automáticamente; el prompt se pega en Google Flow y la edición comercial se termina en CapCut.

## Escudo incluido

La imagen `Escudo poedagar.png` está en:

```text
.agents/skills/flow-watch-video-prompter/assets/Escudo poedagar.png
```

La skill busca primero una referencia dedicada en la carpeta seleccionada o su proyecto. Cuando falta, utiliza esta imagen incluida. Debes adjuntarla también en Flow cuando el prompt lo indique. Conserva la geometría del escudo; se integra como grabado o repujado del metal, sin copiar el fondo blanco de la imagen. No se aplica a una marca diferente sin tu indicación.

## Contenido del repositorio

```text
.agents/skills/flow-watch-video-prompter/
  SKILL.md
  agents/openai.yaml
  assets/Escudo poedagar.png
```

Las fotos comerciales, los videos descargados como referencia y los resultados generados se mantienen en tu proyecto local. La carpeta `referencias/` y los formatos de video y HEIC están excluidos de Git para evitar incorporarlos por accidente. Las instrucciones utilizan rutas relativas y pueden trasladarse a otro equipo.

Para actualizar la versión compartida, modifica la skill de este repositorio, revisa el cambio y publícalo en GitHub. Las copias instaladas en otros equipos se actualizan desde el repositorio; una edición local no se sincroniza automáticamente.
