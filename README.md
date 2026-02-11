<!DOCTYPE html> 
<html lang="es">
<head>
	<meta charset="UTF-8" />
	<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Julian & Carolina | Save the Date</title>

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>

<link href="https://fonts.googleapis.com/css2?family=WindSong:wght@400;500&display=swap" rel="stylesheet">
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,500;0,600;1,600&family=Playfair+Display+SC&family=Playball&family=Montserrat:wght@300;600&display=swap" rel="stylesheet">
<link href="https://fonts.googleapis.com/css2?family=Herr+Von+Muellerhoff&display=swap" rel="stylesheet">
<link href="https://fonts.googleapis.com/css2?family=Antic+Didone&display=swap" rel="stylesheet">
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display&family=Cormorant+Garamond&display=swap" rel="stylesheet">
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display&family=Libre+Baskerville:wght@700&family=Cormorant+Garamond&display=swap" rel="stylesheet">
<link href="https://fonts.googleapis.com/css2?family=Oswald:wght@500;600&display=swap" rel="stylesheet">
<link href="https://fonts.googleapis.com/css2?family=Great+Vibes&family=Playfair+Display:wght@400;700&family=Montserrat:wght@300&display=swap" rel="stylesheet">




<style>
*{margin:0;padding:0;box-sizing:border-box;}

body{
  font-family:'Playfair Display',serif;
  overflow-y:auto; /* ✅ permite scroll */
            height: 100%
            margin: 0;

}

:root{
  --image-url:url("https://github.com/EstasInvitado/Plantilla3/blob/main/ParejaPortada.png?raw=true");
}

/* FONDO DIFUMINADO */
.background{
  position:fixed;
  inset:0;
  background-image:var(--image-url);
  background-size:cover;
  background-position:center;
  filter:blur(18px) brightness(0.75);
  transform:scale(1.1);
  z-index:-1;
  display:none;
}

/* PRIMERA PÁGINA */
.cover{
  height:100vh;
  width:100%;
  background-image:var(--image-url);
  background-size:cover;
  background-position:center;
  display:flex;
  align-items:flex-start;
  justify-content:center;
  position:relative;
}

.text-container{
  text-align:center;
  margin-top:60px;
  color:#fff;
  text-shadow:0 4px 12px rgba(0,0,0,0.4);
}

/* MONOGRAMA */
.monogram{
  position:relative;
  width:120px;
  height:120px;
  margin:0 auto 20px;
}

.monogram span{
  position:absolute;
  font-size:120px;
  font-weight:600;
  line-height:1;
}

.monogram .t{left:0;top:0;}
.monogram .s{left:38px;top:22px;opacity:0.9;}

/* NOMBRES PORTADA */
.names{
  font-family:'WindSong',cursive;
  font-size:2rem;
  font-weight:400;
  opacity:0;
  transform:translateY(40px);
  animation:fadeUp 1.4s ease-out forwards;
}

.amp{
  font-size:4.2rem;
  margin:0 6px;
}

.subtitle{
  font-family:'Montserrat', sans-serif;
  font-weight:300;
  letter-spacing:6px;
  font-size:1.1rem;
  margin-top:20px;
  border-top:1px solid rgba(255,255,255,0.4);
  padding-top:10px;
}

@keyframes fadeUp{
  to{opacity:1;transform:translateY(0);}
}

/* SEGUNDA PÁGINA */
.page{
   min-height:30vh; 
   background-image:url("https://github.com/EstasInvitado/Taylor-Y-Travis/blob/main/FondoBlanco.png?raw=true"); 
   background-size:cover; 
   background-position:center; 
   display:flex; 
   align-items:center; 
   justify-content:center; 
   padding:40px 20px;

}
.flor-divider {
  width: 100px;        /* tamaño pequeño */
  height: auto;
  display: block;
  margin: 0 auto 0px; /* centrada y con poco espacio abajo */
  opacity: 0.8;       /* sutil */
 filter: grayscale(100%) sepia(100%) saturate(220%) hue-rotate(-10deg);
}


.content{
  max-width:520px;
  width:100%;
}

.quote{
    font-family: "Antic Didone", serif;
      text-transform: uppercase;
      
  font-size:1.4rem;
  line-height:1.7;
   line-height: 1.1; 
  color:#3a2f2a;
  white-space:pre-line;
}

.line{
  width:140px;
  height:2px;
  background:#a07c5b;
  margin:25px 0 15px auto;
}

/* FIRMAS */
.firmas{
  text-align:right;
  font-family:'Herr Von Muellerhoff', sans-serif;
  font-size:2rem;
  letter-spacing:1px;
  color:#3a2f2a;
}

.firmas span{
  display:block;
  margin-top:4px;
}
/* Sección */
.padres-section {
  display: flex;
  justify-content: center;
  padding: 30px 15px;
  background: white;
}

/* Cuadro */
.padres-box {
  border: 3px solid rgba(139, 69, 19, 0.35);
  padding: 30px 50px;       /* más espacio lateral */
  max-width: 400px;         /* MÁS LARGO horizontalmente */
  width: 100%;
  text-align: center;
  background: white;
}

/* Título */
.padres-titulo {
  font-family: "Antic Didone", serif;
  font-size: 28px;
  letter-spacing: 1px;
  margin-bottom: 96px;      /* DOBLE espacio debajo del título */
  text-transform: uppercase;
  color: #8B5A2B;
}
/* Animación de aparición de abajo hacia arriba */
@keyframes slideUp {
  0% {
    transform: translateY(50px);
    opacity: 0;
  }
  100% {
    transform: translateY(0);
    opacity: 1;
  }
}

/* Estado inicial fuera de vista */

.padres-titulo,
.tarjeta-interior h2 {
  opacity: 0;
  transform: translateY(50px);
  transition: transform 0.6s ease, opacity 0.6s ease;
}

/* Clase que activa la animación */
.padres-titulo.visible,
.tarjeta-interior h2.visible {
  animation: slideUp 0.6s forwards;
}



/* Nombres */
.padre-nombre {
  font-family: "Cormorant Garamond", serif;
  font-size: 26px;
  margin: 38px 0;           /* más espacio entre renglones */
  line-height: 1.4;
}

/* Línea divisoria café suave */
.padres-divider {
  width: 60%;
  height: 1px; 
  margin: 22px auto;
  background: rgba(139, 69, 19, 0.6);
  box-shadow: 0 0 6px rgba(139, 69, 19, 0.5);
}

/* Sección */
.fecha-lugar {
  background-color: #9C4F3A; /* café terracota */
  padding: 50px 20px;
  display: flex;
  justify-content: center;
}

/* Contenedor */
.fecha-box {
  text-align: center;
  color: #ffffff;
  max-width: 600px;
  width: 100%;
}

/* Título */
.fecha-titulo {
  font-family: "Playfair Display", serif;
  font-size: 18px;
  letter-spacing: 1.5px;
  text-transform: uppercase;
  margin-bottom: 24px;
}

/* Fecha (estilo titular de periódico) */
.fecha-dia {
  font-family: "Libre Baskerville", serif;
  font-size: 32px;          /* grande */
  font-weight: 700;         /* gruesa */
  margin-bottom: 32px;
}

/* Botón transparente */
.fecha-boton {
  display: inline-block;
  padding: 12px 28px;
  border: 1.5px solid #ffffff;
  color: #ffffff;
  text-decoration: none;
  font-family: "Cormorant Garamond", serif;
  font-size: 16px;
  letter-spacing: 1px;
  background: transparent;
  transition: all 0.3s ease;
}

/* Hover elegante */
.fecha-boton:hover {
  background-color: rgba(255, 255, 255, 0.15);
}

/* Subtítulo */
.contador-titulo {
  margin-top: 50px;
  margin-bottom: 30px;
  font-family: "Playfair Display", serif;
  font-size: 18px;
  letter-spacing: 1.5px;
  text-transform: uppercase;
  color: #ffffff;
}

/* Contenedor contador */
.contador {
  display: flex;
  justify-content: center;
  gap: 18px;
  flex-wrap: wrap;
}

/* Cada círculo */
.contador-item {
  width: 90px;
  height: 90px;
  border: 1.5px solid #ffffff;
  border-radius: 50%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

/* Número */
.contador-item span {
  font-family: "Oswald", sans-serif; /* alargada vertical */
  font-size: 28px;
  font-weight: 600;
  line-height: 1;
  color: #ffffff;
}

/* Leyenda */
.contador-item small {
  font-family: "Cormorant Garamond", serif;
  font-size: 10px;
  letter-spacing: 1px;
  margin-top: 6px;
  color: #ffffff;
}

.ceremonia-section {
  background-image: url("https://github.com/EstasInvitado/Taylor-Y-Travis/blob/main/FondoBlanco.png?raw=true");
  background-size: cover;
  background-position: center;
  padding: 80px 20px;
  display: flex;
  flex-direction: column;
  align-items: center;
}
.icono-imagen {
  width: 65px;
  height: auto;
  margin-bottom: 18px;

}


/* Contenedor exterior */
.tarjeta-exterior {
  width: 100%;
  max-width: 420px;
  margin-bottom: 40px;
 
}

/* Quitar margen a la última */
.tarjeta-exterior:last-child {
  margin-bottom: 0;
}

/* Tarjeta blanca */
.tarjeta-interior {
  background: #ffffff;
  padding: 50px 30px;
  border-radius: 18px;
  text-align: center;
  box-shadow: 0 10px 25px rgba(0,0,0,0.12);
  /* LA CLAVE: Curva superior izquierda */
            /* Formato: superior-izq superior-der inferior-der inferior-izq */
            border-top-left-radius: 150px; 
            border-top-right-radius: 0px;
            border-bottom-right-radius: 0px;
            border-bottom-left-radius: 0px;
            
  border: 1px solid rgba(139, 69, 19, 0.25); /* café tenue */
  
}

/* Icono */
.icono {
  font-size: 40px;
  margin-bottom: 15px;
}

/* Título manuscrito */
.titulo-manuscrito {
  font-family: 'Playfair Display', serif;
  font-size: 15px;
  margin-bottom: 12px;
}

/* Nombre del lugar */
.tarjeta-interior h2 {
  letter-spacing: 2px;
  font-size: 25px;
  margin-bottom: 10px;
  font-family: 'WindSong', serif;
   color: #9C4F3A;
  
}

/* Dirección */
.direccion {
  font-size: 14px;
  letter-spacing: 1px;
  margin-bottom: 25px;
}

/* Hora */
.hora {
  font-size: 20px;
  margin-bottom: 25px;
}

/* Botón */
.boton-ubicacion {
  display: inline-block;
  padding: 12px 28px;
  border: 1px solid #000;
  text-decoration: none;
  color: #000;
  font-size: 13px;
  letter-spacing: 2px;
  transition: all 0.3s ease;
}

.boton-ubicacion:hover {
  background: #000;
  color: #fff;
}

.dresscode-section {
  background: #ffffff;
  text-align: center;
  padding: 80px 20px;
}

/* TÍTULO */
.dresscode-titulo {
  font-family: 'Antic Didone', serif;
  font-weight: 600; /* delgada pero con presencia */
  letter-spacing: 4px;
  font-size: 32px;
   font-weight: 300;
  text-transform: uppercase;
  margin-bottom: 40px;
  color: #7A4A24;
}

/* IMAGEN */
.dresscode-img {
  width: 100px;
  max-width: 70%;
  margin-bottom: 40px;
}

/* LINEA DIVISORA */
.linea-divisora {
  width: 120px;
  height: 1.5px;
  background: #8B5A2B;
  margin: 0 auto 30px auto;
}

/* SUBTITULO */
.dresscode-subtitulo {
  font-family: 'Cormorant Garamond', serif;
  font-weight: 400;
  font-size: 20px;
  letter-spacing: 1px;
  margin-bottom: 35px;
  color: #8B5A2B;
}

/* CONTENEDOR CIRCULOS */
.colores-prohibidos {
  display: flex;
  justify-content: center;
  gap: 20px;
}

/* CIRCULOS */
.color {
  width: 65px;
  height: 65px;
  border-radius: 50%;
  margin-left: -35px;
  box-shadow: 0 8px 15px rgba(0,0,0,0.15);
  border: 0px solid #fff;

  opacity: 0;
  transform: translateX(80px);
  transition: all 0.8s ease;
}


/* CUANDO SE ACTIVA */
.color.visible {
  opacity: 1;
  transform: translateX(0);
}

/* COLORES NUDE */
.c1 { background: #8B5A2B; transition-delay: 0.1s;}
.c2 { background: #6E3F1F; transition-delay: 0.2s;}
.c3 { background: #C0652A; transition-delay: 0.3s; }
.c4 { background: #8A9A5B; transition-delay: 0.4s;}


.agenda-section {
  padding: 90px 20px;
  text-align: center;
   background: #ffff;
  
}

.agenda-title {
  font-size: 22px;
  letter-spacing: 4px;
  text-transform: uppercase;
  font-weight: 300;
  color: #3e2b24; /* café oscuro */
  margin-bottom: 60px;
  
}

.agenda-wrapper {
  max-width: 420px;
  margin: 0 auto;
}

.agenda-item {
  opacity: 0;
  transform: translateY(60px);
  transition: all 1.2s ease;
  
}

.agenda-item.visible {
  opacity: 1;
  transform: translateY(0);
}

.agenda-oval {
  position: relative;
  width: 340px;
   margin: 0 auto;   /* 👈 ESTA LÍNEA LA CENTRA */
  padding: 70px 50px;
  background: #F8F3E9;
  border-radius: 50% / 38%;
  text-align: center;
  border: 1px solid #D4B98C;
  box-shadow: 
    0 15px 35px rgba(0, 0, 0, 0.08),
    inset 0 0 0 6px #F8F3E9,
    inset 0 0 0 7px #E7D7B8;
}

/* Título elegante */
.agenda-oval h2 {
  margin: 0;
  font-size: 28px;
  color: #4A2F27;
  font-weight: 500;
  letter-spacing: 1px;
}

/* Subtítulo */
.agenda-oval p {
  margin-top: 12px;
  font-size: 16px;
  color: #8C7A66;
  letter-spacing: 0.5px;
}

/* Ornamentos decorativos */
.ornament {
  width: 90px;
  height: 2px;
  margin: 0 auto;
  background: linear-gradient(to right, transparent, #D4B98C, transparent);
  position: relative;
}

.ornament::before {
  content: "";
  position: absolute;
  left: 50%;
  top: -6px;
  transform: translateX(-50%);
  width: 10px;
  height: 10px;
  border: 1px solid #D4B98C;
  border-radius: 50%;
  background: #F8F3E9;
}

.top {
  margin-bottom: 25px;
}

.bottom {
  margin-top: 25px;
}




.agenda-oval img {
  width: 55px;
  margin-bottom: 20px;
  
}

.medium-icon {
  width: 95px;
  filter: grayscale(100%) sepia(100%) saturate(220%) hue-rotate(-10deg);
}

.agenda-oval h3 {
  font-weight: 600;
  color: #6f3f28; /* café */
  margin-bottom: 8px;
}

.terracota {
  color: #c46a3a;
}

.agenda-oval p {
  color: #000;
  font-weight: 400;
}

.agenda-line {
  width: 2px;
  height: 120px;
  background: #E8E1CF;
  margin: 25px auto;
}

.galeria-parallax {
  position: relative;
  padding: 30px;
  overflow: hidden;
}

/* Fondo desenfocado fijo */
.galeria-parallax::before {
  content: "";
  position: fixed;
  inset: 0;
  background-image: url("https://github.com/EstasInvitado/Plantilla3/blob/main/ParejaPortada.png?raw=true");
  background-size: cover;
  background-position: center;
  background-attachment: fixed;
  filter: blur(14px);
  transform: scale(1.1);
  z-index: -1;
}

/* Contenedor */
.galeria-wrapper {
  display: flex;
  flex-direction: column;
  gap: 20px;
}

/* Imágenes */
.galeria-img {
  width: 100%;
  display: block;
  box-shadow: 0 25px 50px rgba(0,0,0,0.35);
  opacity: 0;
  transform: translateY(60px);
  transition: opacity 0.9s ease, transform 0.9s ease;
}

/* Visible */
.galeria-img.visible {
  opacity: 1;
  transform: translateY(0);
}



/* Contenedor de la sección con el fondo solicitado */
    .seccion-mesa-regalos {
        width: 100%;
        min-height: 100vh;
        background-image: url('https://github.com/EstasInvitado/Taylor-Y-Travis/blob/main/FondoBlanco.png?raw=true');
        background-size: cover;
        background-position: center;
        display: flex;
        justify-content: center;
        align-items: center;
        padding: 40px 20px;
    }

    /* Diseño de la tarjeta blanca con sombra */
    .tarjeta-regalos {
        background-color: #ffffff;
        width: 100%;
        max-width: 450px;
        padding: 50px 30px;
        border-radius: 150px 0px 0px 0px; /* Curva similar a la sección anterior */
        text-align: center;
        box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1); /* Sombra suave solicitada */
        color: #7a5c43; /* Color café base */
    }

    /* Título con fuente WindSong */
    .titulo-windsong {
        font-family: 'WindSong', cursive;
        font-size: 3rem;
        color: #8d6e63; /* Color café */
        margin-bottom: 20px;
        font-weight: 500; /* entre 100 y 900, 100 es ultra delgada */
    }

    .icono-regalo {
        width: 50px;
          margin: 0 auto 20px auto;
          display: block;
        color: #8d6e63;
        
    }

    .texto-detalle {
        font-family: 'Montserrat', sans-serif; /* Usando la base de tus secciones previas */
        font-size: 0.9rem;
        line-height: 1.6;
        text-transform: uppercase;
        letter-spacing: 1px;
        margin-bottom: 30px;
    }

    .btn-tienda {
        display: inline-block;
        padding: 12px 30px;
        border: 1px solid #8d6e63;
        border-radius: 25px;
        text-decoration: none;
        color: #8d6e63;
        font-size: 0.8rem;
        letter-spacing: 2px;
        transition: all 0.3s ease;
    }

    .btn-tienda:hover {
        background-color: #8d6e63;
        color: white;
    }

/* Contenedor de la sección con el fondo blanco solicitado */
    .seccion-final-rsvp {
        width: 100%;
        min-height: 100vh;
        background-color: #ffffff;
        background-size: cover;
        background-position: center;
        display: flex;
        justify-content: center;
        align-items: center;
        padding: 40px 20px;
    }

    /* La tarjeta blanca flotante */
   /* Animación de aparición de derecha a izquierda */
@keyframes slideInRight {
  0% {
    transform: translateX(50px);
    opacity: 0;
  }
  100% {
    transform: translateX(0);
    opacity: 1;
  }
}

/* Estado inicial */
.tarjeta-rsvp-flotante {
  background-color: #9C4F3A;
  width: 100%;
  max-width: 450px;
  padding: 60px 30px;
  text-align: center;
  box-shadow: 0 15px 35px rgba(0, 0, 0, 0.35);
  border: 1px solid rgba(141, 110, 99, 0.2);

  /* Inicial fuera de vista */
  opacity: 0;
  transform: translateX(50px);
  transition: transform 0.6s ease, opacity 0.6s ease;
}

/* Clase que activa la animación */
.tarjeta-rsvp-flotante.visible {
  animation: slideInRight 0.6s forwards;
}

    .titulo-rsvp-elegante {
        font-family: 'Playfair Display', serif;
        font-size: 3.5rem;
        color: #ffffff; /* Color café suave */
        letter-spacing: 8px;
        margin-bottom: 5px;
    }

    .confirmacion-texto {
        font-family: 'Montserrat', sans-serif;
        text-transform: uppercase;
        letter-spacing: 3px;
        font-size: 0.8rem;
        color: #fff8e7;
        margin-bottom: 30px;
    }

    .nombres-rsvp {
        font-family: 'Great Vibes', cursive;
        font-size: 3rem;
        color: #ffffff;
        margin-bottom: 35px;
    }

    .btn-confirmar-invitacion {
    display: inline-block;
    background-color: #9C4F3A; /* Café medio */
    color: #FFFF;
    text-decoration: none;
    
    padding: 14px 45px;
    border-radius: 8px;
    font-family: 'Montserrat', sans-serif;
    text-transform: uppercase;
    letter-spacing: 2px;
    font-size: 0.85rem;
    transition: all 0.3s ease;
    border: 2px solid #FFFF; /* Delineado café */
}

/* Hover / focus / active */
.btn-confirmar-invitacion:hover,
.btn-confirmar-invitacion:focus,
.btn-confirmar-invitacion:active {
    background-color: #ffff; /* Café oscuro / terracota */
    color: #9C4F3A;
    transform: translateY(-2px);
    box-shadow: 0 6px 18px rgba(0,0,0,0.25);
    border-color: #9C4F3A; /* Borde un poco más intenso al pasar mouse */
}

    .sin-ninos {
        margin-top: 30px;
        font-family: 'Montserrat', sans-serif;
        text-transform: uppercase;
        letter-spacing: 3px;
        font-size: 0.7rem;
        color: #fff8e7;
    }
    
.footer-minimal {
  background: #ffffff; /* fondo blanco */
  text-align: center;
  padding: 20px 10px; /* menos espacio para renglones compactos */
  font-family: "Libre Baskerville", sans-serif;
}

.footer-minimal p {
 font-size: 12px;           /* grande, efecto marca de agua */
  color: rgba(100, 100, 100, 0.3); /* gris muy transparente */
  line-height: 1.1;          /* renglones juntos */
  margin: 5px 0;
  font-style: italic;        /* cursiva suave */
  letter-spacing: 2px;
  pointer-events: none;      /* para que no interfiera con clicks */
  user-select: none;         /* no se pueda seleccionar */
}


    
/* BOTÓN DE AUDIO */
.play-btn{
  position:fixed;
  bottom:28px;
  right:28px;
  width:64px;
  height:64px;
  background:#a07c5b;
  border-radius:50%;
  display:flex;
  align-items:center;
  justify-content:center;
  cursor:pointer;
  box-shadow:0 10px 25px rgba(0,0,0,0.3);
  z-index:100;
}

.play-btn::before{
  content:"▶";
  color:#fff;
  font-size:26px;
  margin-left:4px;
}

audio{display:none;}

/* DESKTOP */
@media(min-width:768px){
  .background{display:block;}
  .cover{
    width:390px;
    margin:auto;
    border-radius:14px;
    box-shadow:0 20px 60px rgba(0,0,0,0.45);
  }
  body{
    display:flex;
    justify-content:center;
  }
}
</style>
</head>

<body>

<div class="background"></div>

<main class="cover">
  <div class="text-container">
    <div class="monogram">
      <span class="t">J</span>
      <span class="s">C</span>
    </div>
    <h1 class="names">Julian <span class="amp">&amp;</span> Carolina</h1>
    <h2 class="subtitle">SAVE THE DATE</h2>
  </div>
</main>

<section class="page"> 
  <div class="content">

    <img 
      src="https://github.com/EstasInvitado/Plantilla3/blob/main/Vector2.png?raw=truee"
      alt=""
      class="flor-divider"
    >

    <p class="quote">
      Nos encontramos en el 
      instante perfecto y
      desde entonces, 
      seguimos eligiéndonos 
      cada día.
    </p>

    <div class="line"></div>

    <div class="firmas">
      Julian Martinez
      <span>Carolina Loera</span>
    </div>
  </div>
</section>

<section class="padres-section">
  <div class="padres-box">

    <h3 class="padres-titulo">Nuestros Padres</h3>

    <p class="padre-nombre">Alma Villarreal M.</p>

    <p class="padre-nombre">Orlando González R.</p>

    <div class="padres-divider"></div>

    <p class="padre-nombre">Silvia Hernández S.</p>

    <p class="padre-nombre">Luis Fuentes D.</p>

  </div>
</section>
<section class="fecha-lugar">
  <div class="fecha-box">

    <h3 class="fecha-titulo">Fecha y lugar</h3>

    <p class="fecha-dia">20 DE JUNIO 2026</p>

    <a 
      href="#"
      target="_blank"
      class="fecha-boton"
    >
      Agendar en Google Calendar
    </a>
    <h4 class="contador-titulo">Cuenta regresiva</h4>

<div class="contador">
  <div class="contador-item">
    <span id="dias">0</span>
    <small>DÍAS</small>
  </div>

  <div class="contador-item">
    <span id="horas">0</span>
    <small>HORAS</small>
  </div>

  <div class="contador-item">
    <span id="minutos">0</span>
    <small>MINUTOS</small>
  </div>

  <div class="contador-item">
    <span id="segundos">0</span>
    <small>SEGUNDOS</small>
  </div>
</div>

  </div>
</section>

<section class="ceremonia-section">

  <!-- TARJETA CEREMONIA -->
  <div class="tarjeta-exterior">
    <div class="tarjeta-interior">

      <img 
  src="https://github.com/EstasInvitado/Taylor-Travis/blob/main/cathedral.jpg?raw=true"
  alt="Iglesia"
  class="icono-imagen"
/>


      <p class="titulo-manuscrito">Ceremonia Religiosa</p>
      <h2>Parroquia del Carmen</h2>
      <p class="direccion">CALLE CUALQUIERA 123, EN CUALQUIER LUGAR</p>

      <h3 class="hora">05:00 PM</h3>

      <a href="#" class="boton-ubicacion">VER UBICACIÓN</a>

    </div>
  </div>

  <!-- TARJETA RECEPCIÓN -->
  <div class="tarjeta-exterior">
    <div class="tarjeta-interior">

         <img 
  src="https://github.com/EstasInvitado/Taylor-Travis/blob/main/copas.png?raw=true"
  alt="Iglesia"
  class="icono-imagen"
/>

      <p class="titulo-manuscrito">Recepción</p>
      <h2>Jardin Dorado</h2>
      <p class="direccion">CALLE CUALQUIERA 123, EN CUALQUIER LUGAR</p>

      <h3 class="hora">06:30 PM</h3>

      <a href="#" class="boton-ubicacion">VER UBICACIÓN</a>

    </div>
  </div>

</section>
<section class="dresscode-section">

  <h2 class="dresscode-titulo">DRESS CODE</h2>

  <img 
    src="https://github.com/EstasInvitado/Plantilla3/blob/main/dresscode.png?raw=true"
    alt="Dress Code"
    class="dresscode-img"
  >
   <p class="dresscode-subtitulo">
    FORMAL
  </p>

  <div class="linea-divisora"></div>

  <p class="dresscode-subtitulo">
    Te recomendamos la siguiente<br>paleta de colores:
  </p>

  <div class="colores-prohibidos">
    <span class="color c1"></span>
    <span class="color c2"></span>
    <span class="color c3"></span>
    <span class="color c4"></span>
  </div>

</section>

<section class="agenda-section">

  <h2 class="agenda-title">ITINERARIO</h2>

  <div class="agenda-wrapper">

    <!-- 1 -->
    <div class="agenda-item">
        
      <div class="agenda-oval">
          <div class="ornament top"></div>
        <img src="https://github.com/EstasInvitado/Taylor-Travis/blob/main/iglesia.png?raw=true">
        <h3>Ceremonia</h3>
        <p>6:00pm</p>
        <div class="ornament bottom"></div>
      </div>
    </div>

    <div class="agenda-line"></div>

    <!-- 2 -->
    <div class="agenda-item">
      <div class="agenda-oval">
          <div class="ornament top"></div>
        <img src="https://github.com/EstasInvitado/Plantilla3/blob/main/Disco.png?raw=true" class="medium-icon">
        <h3 class="terracota">Recepcion</h3>
        <p>8:00pm</p>
        <div class="ornament bottom"></div>
      </div>
    </div>

    <div class="agenda-line"></div>

    <!-- 3 -->
    <div class="agenda-item">
      <div class="agenda-oval">
          <div class="ornament top"></div>
        <img src="https://github.com/EstasInvitado/Taylor-Travis/blob/main/plato.png?raw=true">
        <h3 class="terracota">Cena</h3>
        <p>9:00pm</p>
        <div class="ornament bottom"></div>
      </div>
    </div>

    <div class="agenda-line"></div>

    <!-- 4 -->
    <div class="agenda-item">
      <div class="agenda-oval">
          <div class="ornament top"></div>
        <img src="https://github.com/EstasInvitado/Plantilla3/blob/main/Copas.png?raw=true">
        <h3 class="terracota">Brindis</h3>
        <p>10:00pm</p>
        <div class="ornament bottom"></div>
      </div>
    </div>

  </div>

</section>

<section class="galeria-parallax">

  <div class="galeria-wrapper">

    <img src="https://github.com/EstasInvitado/Plantilla3/blob/main/Couple1.png?raw=true" class="galeria-img">

    <img src="https://github.com/EstasInvitado/Plantilla3/blob/main/couple2.png?raw=true" class="galeria-img">

    <img src="https://github.com/EstasInvitado/Plantilla3/blob/main/couple3.png?raw=true" class="galeria-img">

  </div>

</section>


<section class="seccion-mesa-regalos">
    <div class="tarjeta-regalos">
        <h2 class="titulo-windsong">Mesa de Regalos</h2>
        
        <div class="icono-regalo">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5">
                <path d="M20 12v10H4V12M2 7h20v5H2V7zM12 22V7M12 7c0-2.5-2-4.5-4.5-4.5S3 4.5 3 7h9zM12 7c0-2.5 2-4.5 4.5-4.5S21 4.5 21 7h-9z"/>
            </svg>
        </div>

        <p class="texto-detalle">
            Tu presencia es nuestro mejor regalo, pero si quieres tener un detalle con nosotros, te compartimos algunas ideas
        </p>

        <a href="#" class="btn-tienda">IR A TIENDA</a>
    </div>
</section>


<section class="seccion-final-rsvp">
    <div class="tarjeta-rsvp-flotante">
        <h2 class="titulo-rsvp-elegante">RSVP</h2>
        <p class="confirmacion-texto">Confirma tu asistencia</p>
        
        <div class="nombres-rsvp">
            Julian y Carolina
        </div>

        <a href="https://wa.me/1234567890?text=¡Hola! Confirmo mi asistencia a la boda de Julian y Carolina." 
           target="_blank" 
           class="btn-confirmar-invitacion">
           Confirmar asistencia
        </a>

        <p class="sin-ninos">Adultos solamente</p>
    </div>
</section>

<footer class="footer-minimal">
  <p class="footer-fecha">20 · 06 · 26</p>
  <p class="footer-mensaje">Con cariño, Julian y Carolina</p>
</footer>



<audio id="music">
  <source src="https://github.com/EstasInvitado/Taylor-Y-Travis/blob/main/(Audio)%20Screen%20Recording%202026-01-29%20153029.m4a?raw=true" type="audio/mp4">
</audio>

<div class="play-btn" onclick="toggleMusic()"></div>

<script>
const music = document.getElementById("music");
let isPlaying = false;

function toggleMusic(){
  if(!isPlaying){
    music.play();
    isPlaying = true;
  } else {
    music.pause();
    isPlaying = false;
  }
}
const fechaEvento = new Date("June 20, 2026 18:00:00").getTime();

setInterval(() => {
  const ahora = new Date().getTime();
  const diferencia = fechaEvento - ahora;

  if (diferencia < 0) return;

  const dias = Math.floor(diferencia / (1000 * 60 * 60 * 24));
  const horas = Math.floor((diferencia % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
  const minutos = Math.floor((diferencia % (1000 * 60 * 60)) / (1000 * 60));
  const segundos = Math.floor((diferencia % (1000 * 60)) / 1000);

  document.getElementById("dias").textContent = dias;
  document.getElementById("horas").textContent = horas;
  document.getElementById("minutos").textContent = minutos;
  document.getElementById("segundos").textContent = segundos;
}, 1000);

const items = document.querySelectorAll(".timeline-item");
const line = document.querySelector(".timeline-line");
const timeline = document.querySelector(".timeline");

const observer = new IntersectionObserver(entries => {
  entries.forEach(entry => {
    if (entry.isIntersecting) {
      entry.target.classList.add("active");
    } else {
      entry.target.classList.remove("active");
    }
  });
}, { threshold: 0.5 });

items.forEach(item => observer.observe(item));

function updateLine() {
  const rect = timeline.getBoundingClientRect();
  const windowHeight = window.innerHeight;

  let progress = (windowHeight - rect.top) / rect.height;
  progress = Math.max(0, Math.min(progress, 1));

  /* velocidad visual lenta */
  let slowProgress = progress * 0.75;

  line.style.background = `linear-gradient(to bottom,
    #8B5A2B 0%,
    #8B5A2B ${slowProgress * 100}%,
    #ccc ${slowProgress * 100}%,
    #ccc 100%)`;
}

window.addEventListener("scroll", updateLine);
const agendaItems = document.querySelectorAll(".agenda-item");

const agendaObserver = new IntersectionObserver(entries => {
  entries.forEach(entry => {
    if (entry.isIntersecting) {
      entry.target.classList.add("visible");
    } else {
      entry.target.classList.remove("visible");
    }
  });
}, { threshold: 0.4 });

agendaItems.forEach(item => agendaObserver.observe(item));

/* ===== GALERIA ANIMACION ===== */

const galeriaImgs = document.querySelectorAll(".galeria-img");

const galeriaObserver = new IntersectionObserver(entries => {
  entries.forEach(entry => {
    if (entry.isIntersecting) {
      entry.target.classList.add("visible");
    } else {
      entry.target.classList.remove("visible");
    }
  });
}, { threshold: 0.3 });

galeriaImgs.forEach(img => galeriaObserver.observe(img));

/* ===== COLORES ANIMACION ===== */

const colores = document.querySelectorAll(".color");

const colorObserver = new IntersectionObserver(entries => {
  entries.forEach(entry => {
    if (entry.isIntersecting) {
      entry.target.classList.add("visible");
    } else {
      entry.target.classList.remove("visible");
    }
  });
}, { threshold: 0.4 });

colores.forEach(color => colorObserver.observe(color));

/* ===== PADRES Y TARJETAS ANIMACION ===== */
const padresElements = document.querySelectorAll(".padres-titulo");
const tarjetaHeaders = document.querySelectorAll(".tarjeta-interior h2");

const slideUpObserver = new IntersectionObserver(entries => {
  entries.forEach(entry => {
    if(entry.isIntersecting){
      entry.target.classList.add("visible");
    } else {
      entry.target.classList.remove("visible");
    }
  });
}, { threshold: 0.3 }); // ajusta para que la animación aparezca antes o después

padresElements.forEach(el => slideUpObserver.observe(el));
tarjetaHeaders.forEach(el => slideUpObserver.observe(el));

/* ===== TARJETA RSVP ANIMACION ===== */
const rsvpFlotante = document.querySelectorAll(".tarjeta-rsvp-flotante");

const rsvpObserver = new IntersectionObserver(entries => {
  entries.forEach(entry => {
    if(entry.isIntersecting){
      entry.target.classList.add("visible");
    } else {
      entry.target.classList.remove("visible");
    }
  });
}, { threshold: 0.3 });

rsvpFlotante.forEach(el => rsvpObserver.observe(el));

</script>

</body>
</html>
