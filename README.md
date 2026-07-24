# vigia-dashboard

Panel del **vigía del catálogo** de PowerPlanet, desplegado en el VPS por Coolify (`vigia.ppotools.net`, detrás de Authelia).

- Es un `nginx:alpine` que sirve el directorio `/home/coolify-admin/vigia` del VPS.
- El contenido (`index.html` + `data.json`) lo **empuja el vigía del Mac** por `scp` sobre Tailscale cada ciclo.
- El dato vive en el mongod local del Mac (`:27018`); aquí solo se sirve el JSON ya calculado.

No contiene secretos.
