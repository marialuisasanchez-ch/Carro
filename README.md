# Carro
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<html>
<head>
<title>Mi coche</title> 
</head>
<body>
<h1>Mi coche</h1>
<div id="visor">
   <div id="fondouno">
      <img src="calle1.jpg" alt="fondo1" >
   </div>
   <div id="fondodos">
      <img src="calle1.jpg" alt="fondo2" >
   </div>
   <div id="micoche">
      <img src="coche.gif" alt="elCoche" >
   <div>
</div>

<style type="text/css">
* { margin: 0px auto; padding: 0px; }
h1 { font:bold 1.5em arial; text-align: center; padding: 0.5em ; }
#visor { position: absolute; top: 100px; left: 200px; width: 450px; 
         height: 600px; overflow: hidden; }
#fondouno { position: absolute; top: 0px; left: 0px; }
#fondodos { position: absolute; top: 0px; left: 450px; }
#micoche { position: absolute; top: 280px; left: 100px; }
</style> 
       <script type="text/javascript">
window.onload = function() { //al cargarse la página ...
fondo1=document.getElementById("fondouno"); //referencia al primer fondo.
fondo2=document.getElementById("fondodos"); //referencia al segundo fondo
pararmover=setInterval(mover,50); //iniciar primer temporizador: movimiento
setInterval(repetir,2250); //iniciar segundo temporizador: repetición del ciclo. 
}
desplazar=0; //estado inicial del movimiento.
function mover() { //temporizador 1: movimiento
         desplazar-=10; //desplazar fondo1 -10px
         desplazar2=desplazar+450; //desplazar fondo2 a la vez
         posicion1=desplazar+"px"; //preparar para código CSS fondo1
         posicion2=desplazar2+"px"; //preparar para código CSS fondo1
         fondo1.style.left=posicion1; //cambiar posición fondo1 mediante CSS
         fondo2.style.left=posicion2; //cambiar posición fondo2
         }
function repetir() { //temporizador 2: repetir ciclo
         fondo1.style.left="0px"; //posición inicial de fondo1
         fondo2.style.left="450px"; //posición inicial de fondo2
         desplazar=0; //posicion inicial referencia de movimiento.
         }			
</script>
</body>
</html>
