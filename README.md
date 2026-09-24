# redes-videos

Los videos de los reels de [@dfslezak](https://www.instagram.com/dfslezak/), hosteados acá para
que la Graph API de Meta los pueda descargar.

Existe por una razón concreta: los links de exportación de OpusClip vienen firmados y **vencen a
las 24 horas**. Una tanda escalonada a lo largo de tres días se rompe sola — el 24/09/2026 se
perdieron seis piezas de Eco TV justamente así, con el `video_url` muerto cinco minutos antes del
primer posteo del día.

Los archivos se suben re-codificados (h264 CRF 23, techo de 3,5 Mbps, AAC 128k, `+faststart`):
el export de Opus viene a ~10 Mbps y pesa 45 MB para 38 segundos, lo que acá quedan 9 MB sin
diferencia visible. Instagram recomprime igual.

    https://raw.githubusercontent.com/dfslezak/redes-videos/main/<pieza>/<archivo>.mp4

Lo carga `_publicar/hospedar.py` del repo `redes`. Un directorio por pieza, igual que en
`redes-portadas`.
