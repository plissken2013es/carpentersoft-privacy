# carpentersoft-privacy

Políticas de privacidad de las aplicaciones de **Carpenter Soft** publicadas en Google Play. Una página por aplicación, bilingüe (español e inglés), sin JavaScript ni dependencias.

Play exige una URL de política de privacidad en la ficha de cada aplicación, y esa URL tiene que seguir funcionando mientras la app esté publicada. Por eso vive aquí y no en el hosting de cada juego.

## URLs (tras activar GitHub Pages)

| Aplicación | Paquete | Página |
|---|---|---|
| La Cuenta Atrás | `es.luisquin.cuentaatras` | `cuenta-atras.html` |
| GWBW Phaser demo | `es.luisquin.gwbwphaser` | `gwbw-phaser-demo.html` |
| Mariano versus Zombies | `es.luisquin.zombiescavenger` | `mariano-versus-zombies.html` |
| Road Rage Overdrive | `es.luisquin.roadrageoverdrive` | `road-rage-overdrive.html` |

Base: `https://plissken2013es.github.io/carpentersoft-privacy/`

## Publicar por primera vez

1. Crear en GitHub un repositorio **público** llamado `carpentersoft-privacy`, vacío (sin README).
2. Desde esta carpeta:

```bash
git add -A && git commit -m "Políticas de privacidad de Carpenter Soft"
git branch -M main
git remote add origin https://github.com/plissken2013es/carpentersoft-privacy.git
git push -u origin main
```

3. En GitHub: **Settings › Pages › Build and deployment**, origen "Deploy from a branch", rama `main`, carpeta `/ (root)`. En un par de minutos las páginas responden.
4. Comprobar que la URL abre sin iniciar sesión (por ejemplo, en una ventana privada).

## Añadir una aplicación nueva

1. Copiar `_plantilla.html` a `<nombre-app>.html`.
2. Sustituir `NOMBRE_APP`, `PAQUETE`, `FECHA` y `FECHA_EN`.
3. **Comprobar en el código de la app qué guarda y a dónde se conecta** (buscar `localStorage`, `fetch`, plugins nativos) y ajustar las secciones "Qué se guarda en tu dispositivo", "Conexiones y permisos" y "Terceros". La política tiene que coincidir con el formulario de seguridad de los datos de Play.
4. Añadir la fila a la tabla de este README y el enlace en `index.html`.
5. `git commit` y `git push`. La página está lista en cuanto Pages termine.

## Reglas para no romper nada

- **No renombrar ni mover** una página ya publicada: su URL está registrada en la ficha de Play. Si hay que cambiarla, actualizar también la ficha de esa aplicación.
- No cambiar el nombre del repositorio ni la cuenta sin actualizar todas las fichas.
- Actualizar la fecha de la página **solo** cuando cambie el contenido de verdad.
- Los ficheros que empiezan por `_` no se publican (Jekyll los ignora): útil para la plantilla.

## En Play Console, por cada aplicación

- **Política de privacidad**: Contenido de la aplicación › Política de privacidad → pegar la URL.
- **Seguridad de los datos**: para estas tres, "no se recogen ni comparten datos". El récord y el idioma de *Mariano versus Zombies* se guardan solo en el dispositivo, así que no cuentan como recogida.
- Además piden: clasificación de contenido, público objetivo, declaración de anuncios (ninguna tiene) y la sección de aplicaciones gubernamentales y financieras.

## Pendiente

Migrar aquí las políticas de las apps antiguas (El Secreto de isla Moncloa, The Secret of Donut Island, Jaws AI Companion, Trivial Rajoy, Sonar Hunter) para dejar de depender del hosting por FTP de 2017. Al hacerlo hay que actualizar la URL en la ficha de cada una.
