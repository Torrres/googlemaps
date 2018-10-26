# googlemaps

> No olvidar instalar las dependencias previamente

## Build Setup

```bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report
```

Se implemento la siguientes librerias.

[https://github.com/xkjyeah/vue-google-maps](https://github.com/xkjyeah/vue-google-maps)

Esta libreria nos permite generar el maps correspondiente. De igual forma nos proporciona un market por defecto.

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

[https://github.com/eregnier/vue2-gmap-custom-marker](https://github.com/eregnier/vue2-gmap-custom-marker)

Esta libreria, nos va a permitir perzonalizar el marker de google maps. \(Redimencionar correctamente, o que pasen la imagen correcta.\)

Ambas librerias implementan un array de objetos, donde se proporciona latitud y longitud.

```
markers: [{
    position: {
    lat: 10.0,
    lng: 10.0
   }
}, {
    position: {
     lat: 11.0,
     lng: 11.0
    }
}]
```

Con que se obtenga el array de un Endpoint con eso debe quedar.

