<h1>Clima App</h1>

<p>Esta aplicación web muestra información meteorológica basada en la ubicación del usuario. Utiliza la API de OpenWeatherMap para obtener datos en tiempo real.</p>

<h1>-----Contenido--------</h1>

<h4>1. [Estructura de archivos](#estructura-de-archivos)</h4>
<h4>2. [Cómo usar](#cómo-usar)</h4>
<h4>3. [Tecnologías utilizadas](#tecnologías-utilizadas)</h4>
<h4>4. [Licencia](#licencia)</h4>

-------------------------------Estructura de archivos-------------------------
![Screenshot 2024-02-29 191047](https://github.com/DiegoFranciscoG/climawebdg/assets/148287776/e31e8ccb-73e1-4b6f-96a2-27dfe7f150b9)

- `index.html`: Página principal de la aplicación.
- `clima.css`: Archivo de estilos CSS.
- `climas.js`: Archivo JavaScript que maneja la lógica de la aplicación.

<h1>---------Tecnologías utilizadas--------</h1>
<h4>HTML</h4>

<h4>CSS</h4>

<h4>JavaScript</h4>

<h4>OpenWeatherMap API para datos meteorológicos en tiempo real.</h4>

<h1>Inicialización y Carga de Datos</h1>
<p>La aplicación comienza con la carga de la página (onLoad()), que inicia el proceso para obtener la ubicación del usuario. Se utiliza la función navigator.geolocation.getCurrentPosition para obtener las coordenadas de la ubicación actual.</p>

<h4>javascript</h4>
<h5>const onLoad = () => {
    navigator.geolocation.getCurrentPosition(fetchData);
}</h5>

<h1>Obtención de Datos Meteorológicos</h1>
<p>La función fetchData toma las coordenadas de la ubicación y realiza una solicitud a la API de OpenWeatherMap para obtener datos meteorológicos. La respuesta se procesa en la función setWeatherData, que actualiza la interfaz de usuario con la información obtenida.</p>

const fetchData = position => {
    // ... código para obtener datos de OpenWeatherMap ...
}

<h1>Interfaz de Usuario Dinámica</h1>
<p>a interfaz de usuario se actualiza dinámicamente con los datos meteorológicos. La función setWeatherData toma los datos devueltos por la API y los muestra en elementos HTML específicos.</p>

<h5>javascript</h5>
<h6>const setWeatherData = data => {
    // ... código para mostrar datos en la interfaz de usuario ...
    cleanUp(); // Oculta el indicador de carga y muestra la interfaz de usuario.</h6>
}
<h1>Indicador de Carga</h1>
<p>Se utiliza un indicador de carga (loader) mientras se obtienen y procesan los datos. Este indicador es visible durante la carga y se oculta una vez que los datos están listos para ser mostrados.</p>

<h1>css</h1>
<h5>.loader {
    // ... estilos para el indicador de carga ...
}</h5>
