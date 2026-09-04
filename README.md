#  Browser Games Blocklist

Una lista negra (blacklist) curada de dominios de juegos web accesibles vía navegador. Diseñada para facilitar el bloqueo de sitios de gaming en entornos corporativos, educativos o domésticos mediante herramientas de filtrado de DNS.

## Características
*   **Formato compatible:** Pi-hole, AdGuard Home, `/etc/hosts`, y la mayoría de firewalls/proxies.
*   **Actualización frecuente:** La lista se mantiene al día con nuevos dominios de juegos emergentes.
*   **Cobertura:** Incluye portales populares (como Y8, Poki, CrazyGames), juegos .io, plataformas de emulación web y sitios de juegos casuales.
*   **Total de dominios:** +640 entradas únicas.

## Cómo usarla

### Para Pi-hole
1.  Ve a tu panel de administración de Pi-hole.
2.  Navega a **Group Management** > **Adlists**.
3.  Añade la siguiente URL como nueva lista:
    ```text
    https://raw.githubusercontent.com/[TU_USUARIO]/[NOMBRE_DEL_REPO]/main/blocklist_games.txt
    ```
4.  Haz clic en "Add" y luego ejecuta un **Gravity Update**.

### Para AdGuard Home
1.  Ve a **Filters** > **DNS blocklists**.
2.  Haz clic en "Add a blocklist".
3.  Pega la URL raw del archivo (la misma de arriba) y dale un nombre descriptivo.

### Para archivo Hosts (Linux/Mac/Windows)
Puedes añadir el contenido del archivo `blocklist_games.txt` directamente a tu archivo de hosts del sistema.
*   **Linux/Mac:** `/etc/hosts`
*   **Windows:** `C:\Windows\System32\drivers\etc\hosts`

>  **Nota:** Al usar el formato `0.0.0.0 dominio.com`, asegúrate de no tener conflictos con otras entradas en tu archivo hosts local.

##  Advertencia Importante
Esta lista bloquea dominios genéricos de juegos. Algunos de estos dominios pueden compartir infraestructura con sitios legítimos o contener otros tipos de contenido. 
*   **Revisa antes de desplegar:** Se recomienda probar la lista en un entorno controlado antes de aplicarla a toda la red.
*   **Falsos positivos:** Si encuentras un sitio legítimo bloqueado por error, por favor abre un **Issue** en este repositorio.

## Contribuciones
¿Has encontrado un nuevo sitio de juegos web que no está en la lista? ¡Las contribuciones son bienvenidas!
1.  Haz un Fork del repositorio.
2.  Añade los nuevos dominios al final del archivo `blocklist_games.txt`.
3.  Envía un Pull Request con la descripción del sitio añadido.

## Licencia
Este proyecto está bajo la licencia [MIT](LICENSE).
