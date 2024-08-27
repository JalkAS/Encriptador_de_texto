### Features

- Este Encriptador de Texto tiene extension de comentarios que es 
"Better Comments": https://marketplace.visualstudio.com/items?itemName=aaron-bond.better-comments
- El idioma del proyecto es en "es"
- La mayoria de Imagenes son en .svg
- Utiliza fuentes de letra externas a VS Code la fuente principal se llama "Inter": https://fonts.google.com/specimen/Inter?query=inter

#Visualizacion del Proyecto

#JS

##Elementos del Encriptador de Texto

```
const btnEncriptar = document.querySelector(".btnEncriptar");
const txtEncriptar = document.querySelector(".encriptar");
const aviso = document.querySelector(".textoAlert");
const respuesta = document.querySelector(".evaluar");
const contenido = document.querySelector(".boxContenedor");
const btnCopiar = document.querySelector(".btnCopiar");
const btnDesencriptar = document.querySelector(".btnDesencriptar");

```

##Parte Inicial del Encriptador

```
	btnEncriptar.addEventListener("click", e=>{
    e.preventDefault();
    let texto = txtEncriptar.value;
    let txt = texto.normalize("NFD").replace(/[$\.¿\?~!\¡@#%^&*()_|}\{[\]>\<:"`;,\u0300-\u036f']/g, "");
```

##Parte Inicial del Desencriptador

```
	btnDesencriptar.addEventListener("click", e=>{
    e.preventDefault();
    let texto = txtEncriptar.value;
    let txt = texto.normalize("NFD").replace(/[$\.¿\?~!\¡@#%^&*()_|}\{[\]>\ <:"`;,\u0300-\u036f']/g, "");
```

##Copiado

```
	btnCopiar.addEventListener("click", e=>{
    e.preventDefault();
    let copiar = respuesta;
    copiar.select();
    document.execCommand("copy"); 
    });
```
#HTML5
##Primera Seccion del HTML
```
    <section class="encriptador">

            <textarea class="encriptar" placeholder="Ingrese el texto aquí"></textarea>

            <div class="encriptadorAlert">
                <img src="./img/aviso.svg" alt="Imagen de Aviso" class="imgAlert">
                <p class="textoAlert">Solo letras minúsculas y sin acentos</p>
            </div>

            <div class="encriptadorContenedor">
                <button type="submit" class="btnDesencriptar">Desencriptar</button>
                <button type="submit" class="btnEncriptar">Encriptar</button>
            </div>

        </section>
```
#CSS
#Importación de fuentes y Variables
```
/**Fuentes*/
@import url('https://fonts.googleapis.com/css2?family=Inter:ital,opsz,wght@0,14..32,100..900;1,14..32,100..900&family=Krona+One&family=Montserrat:ital,wght@0,100..900;1,100..900&display=swap');

/**Variables*/
:root{
    --Font: url(../img/background.gif);
    --White:#FFFFFF;
    --DarkBlue:#000000; 
    --Grey:#C5C5C5;
    --Grey1:#67808E;
    --RGBA:rgba(0,0,0,0.08);
    --WhiteBlue:#D8DFE8;
    --Medium-Blue:#0a38718a;
    --Grey2:#939185;
    --Grey3:#495057;
    --TextoAviso:#000000;
}
```
