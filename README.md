# Práctica HTML-CSS - Full Stack Web Developement
Xavi Roca Vilalta (NOV.22)

## Estructura de archivos
* index.html
* carperta `css`
    - reset.css (para limpiar los defectos de los navegadores)
    - style.css
* carpeta `images`

## Recursos utilizados para cada uno de los puntos

### Control de visualización correcta en Chrome, Firefox, Edge
* Verificación disponibilidad en <https://caniuse.com>

### Links con estado hover suavizado con una transición 
* Código en `transition.css` :
~~~
.menu-item a {
    background-color: var(--main-background-color);
    transition: background-color .5s;
  }

@media screen and (min-width: 768px) {
    .menu-item a:hover {
        cursor: pointer;
        background-color: lightblue;
    }  
}
~~~

### Header con imagen de fondo optimizada a distintas resoluciones, e imagen distinta para distintos tamaños.
* Utilizo `https://responsivebreakpoints.com/` para generar 4 resoluciones de la misma imagen
* La herramienta me genera el código html necesario
* Genero 2 juegos de imagenes distintos: para tamaños grande de pantalla y para tamaños pequeños
* Código:
~~~
    <header class="header-image">
        <picture>
            <source
            media="(min-width: 620px)"
            srcset="
                images/barcelona_in0jkm_c_scale,w_200.jpg 200w,
                images/barcelona_in0jkm_c_scale,w_624.jpg 624w,
                images/barcelona_in0jkm_c_scale,w_1042.jpg 1042w,
                images/barcelona_in0jkm_c_scale,w_1200.jpg 1200w"
            >       
            <source
            media="(max-width: 620px)"
            srcset="
                images/BCN_Landscape_ahfp4s_c_scale,w_180.jpg 180w,
                images/BCN_Landscape_ahfp4s_c_scale,w_608.jpg 608w,
                images/BCN_Landscape_ahfp4s_c_scale,w_800.jpg 800w"
            > 
            <img src="images/BCN_Landscape_ahfp4s_c_scale,w_800.jpg" alt="">     
        </picture>
    </header>
~~~
   
### Carrusel con nuestros trabajos
* He utilizado el ejemplo de carrusel que trabajamos en la clase
* He insertado algun video de Youtube mediante iframe, con el código embebido que propone Youtube directamente, eliminando las dimensiones fijas

### Skills con progreso
* He utilizado la orientación que nos diste en el discord: dos DIVs anidados, el de fuera con el borde y el de dentro sólido con un `width`igual al porcentaje del skill
* Código HTML:
  ~~~
            <div class="skill-item">
                <div>
                    <label class="skill-label" for="git">GIT</label> 
                </div>
                <div class="skill-border">
                    <div class="skill-progress level25">25%</div>    
                </div>    
            </div>
 ~~~
 * Código CSS:
 ~~~
 .skills .skill-border {
    display: block;
    border: 1px solid var(--main-background-color);
    border-radius: 5%;
    height: 1em;
    width: 100px;
}

.skills .skill-progress {
    display: block;
    background-color: var(--main-background-color);
    height: 100%;
    font-size: 1em;
    color: var(--main-color);
    text-align: left;
}

.skills .level25 {
    width: 25%;
}

.skills .level50 {
    width: 50%;
}

.skills .level75 {
    width: 75%;
}

.skills .level00 {
    width: 100%;
}
~~~

### Validación html de cada input
* Código:
~~~
<input type="text" name="Github tag" id="githug-tag" pattern="/@([A-Za-z0-9_]{1,15})/">
~~~

### Links a redes sociales sin dejar rastro en ellas
* Código: atributo -->  `rel="noreferrer noopener"`
~~~
            <div class="social-item">
                <a href="https://twitter.com/XaviRocaV" target="_blank" rel="noreferrer noopener">
                    <img class="social-icon" src="images/twitter.png" alt="twitter">
                </a>
            </div>
~~~

### Página con nuestros trabajos usando css grid
* ...

### Etiquetas de contenido semántico
* Etiquetas utilizadas: HEADER, NAV, SECTION, FOOTER

### Mobile first
* Las Media Queries se utilizan para maquetar en alta resolución

### Animaciones o interactividad únicamente con css
* ...

## Opcionales

### Menu burger basado en CSS
* Ref --> https://alvarotrigo.com/blog/hamburger-menu-css-responsive/

### Despliegue en Github pages
* ...

### Página 404
* ...

### Página 500
* ...

## Github y desarrollo del proyecto
* Se inicia la construcción del portfolio trabajando contra este repositorio Github.
* El repositorio contiene todos los commits del proyecto
* La práctica se ha trabajado desde distintos equipos, cada uno con su repositorio local y configuración GIT.




