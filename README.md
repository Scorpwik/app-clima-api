# 🌤️ Explorador de Clima

Aplicación web para consultar el clima actual de cualquier ciudad del mundo. Escribes el nombre —por ejemplo, Quito— y la página muestra la temperatura, la sensación térmica, la humedad, el viento y la presión, junto con el ícono y la descripción del tiempo en español.

🔗 **Demo:** [https://scorpwik.github.io/app-clima-api/](https://scorpwik.github.io/app-clima-api/)

Repositorio: [Scorpwik/app-clima-api](https://github.com/Scorpwik/app-clima-api)

## Qué hace

- Busca el clima por nombre de ciudad con la API de clima actual de OpenWeatherMap.
- Muestra la ciudad, el código del país, la temperatura en °C, la sensación térmica, la humedad, el viento en km/h, la presión en hPa, la descripción y el ícono.
- Pide los datos en unidades métricas y con los textos en español (`units=metric` y `lang=es`).
- Convierte el viento de metros por segundo a kilómetros por hora.
- Avisa si el campo de búsqueda queda vacío.
- Muestra un estado de carga mientras llega la respuesta y desactiva el botón **Buscar**.
- Si la ciudad no existe, la clave no es válida o el servidor falla, explica el error y deja el botón **Reintentar**.
- Guarda las últimas 5 búsquedas exitosas como accesos rápidos, sin repetir la misma ciudad. Al dar clic en una, vuelve a consultar esa ciudad.

## API del clima

Usa la [Current Weather Data API](https://openweathermap.org/current) de [OpenWeatherMap](https://openweathermap.org/api). La petición sale de `app.js` hacia:

`https://api.openweathermap.org/data/2.5/weather`

La clave es gratuita: hay que crear una cuenta y generar una API key. Las claves nuevas pueden tardar unos minutos en activarse.

## Tecnologías

- HTML
- CSS, con la fuente [Inter](https://fonts.google.com/specimen/Inter) y sin frameworks
- JavaScript en el navegador (`fetch` con `async`/`await`)
- [OpenWeatherMap](https://openweathermap.org/api)

No hay paso de compilación. Son archivos estáticos (`index.html`, `style.css` y `app.js`).

## Cómo ejecutarlo en tu computadora

1. Clona el repositorio y entra a la carpeta:

   ```bash
   git clone https://github.com/Scorpwik/app-clima-api.git
   cd app-clima-api
   ```

2. Crea una cuenta gratis en [OpenWeatherMap](https://home.openweathermap.org/users/sign_up) y genera una clave en [API keys](https://home.openweathermap.org/api_keys).

3. Abre `app.js` y pon **tu** clave en la constante `API_KEY`. El valor de abajo es solo un marcador: no pegues aquí una clave real.

   ```js
   const API_KEY = 'TU_CLAVE_AQUI';
   ```

4. Abre el proyecto con un servidor local. Si usas VS Code, la extensión Live Server ya está configurada en el puerto `5501` (`.vscode/settings.json`). También puedes levantarlo así:

   ```bash
   python3 -m http.server 5501
   ```

5. Entra a [http://localhost:5501](http://localhost:5501) y busca una ciudad, por ejemplo Quito.

## Autor

**Joshua Lozada** — [Scorpwik](https://github.com/Scorpwik)
