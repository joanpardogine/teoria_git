<!-- <style type="text/css">
  .html,.sintaxi,.htmlLinea,.git { font-family: Lucida Console;}
  .html {padding: 10px; background-color:#d9d9d9;}
  .git {padding: 10px; background-color:#ccffcc;}

  .sintaxi {padding: 5px 3px 3px 40px; background-color:#e6eeff;}
  .htmlLinea {padding: 5px;}
  .prompt { font-weight: normal; color: green;}
  .comentari {font-weight: normal;  color: green;}
  .sudo { font-weight: normal; color: gray;}
  .fitxer {font-family: Lucida Console; font-weight: normal; color: #0099ff; background-color: #e6f5ff; font-weight: bold;}
  .ordre { font-weight: bold; color: #002266;}
  .ordreLinux { font-weight: bold; color: #808080;}
  .resposta {font-weight: bold; color: #666666;}
  .error {font-weight: bold; color: #ff6666; background-color: #ffe6e6}
  .parametre {font-weight: bold; color: #0099ff;}
  
  .commitLinea {padding: 3px; font-weight: bold; background-color: pink;}
  .cadena {font-weight: bold; color: #999999;}
            .intermitent {
                animation: blinker 1s linear infinite;
            }
            @keyframes blinker {
                50% {
                    opacity: 0;
                }
            }
</style> -->

<!--   https://learngitbranching.js.org  -->

<div align="center">
    <img src="./teoria_git.svg" width="400" height="400" alt="css-in-readme">
</div>

# Comandos de Git
Tienes una gran variedad de comandos de git en este sandbox. Estos incluyen:

commit
branch
checkout
cherry-pick
reset
revert
rebase
merge

¡Comparte!
Comparte tus árboles con tus amigos usando export tree e import tree

¿Tienes una buena lección que compartir? Prueba construyendo un nivel con build level o prueba el nivel de un amigo con import level

Para ver todos los comandos disponibles, escribe show commands. Hay algunas joyitas como undo y reset

Por ahora, empecemos con los levels...

Secuencia introductoria
Una breve introducción a la mayoría de los comandos de git

1: Introducción a los commits de Git


# Commits de Git
Un commit en un repositorio git registra un snapshot de todos los archivos en tu directorio. Es como un gran copy&paste, ¡pero incluso mejor!

Git pretende mantener los commits tan livianos como sea posible, por lo que no copia ciegamente el directorio completo cada vez que haces un commit. Puede (cuando es posible) comprimir un commit como un conjunto de cambios (o un "delta") entre una versión de tu repositorio y la siguiente.

Git mantiene, también, un historial de qué commits se hicieron y cuándo. Es por eso que la mayoría de los commits tienen commits ancestros encima -- designamos esto con flechas en nuestra visualización. ¡Mantener el historial es genial para todos los que trabajan en el proyecto!

Hay un montón en lo que ahondar, pero por ahora puedes pensar en los commits como snapshots de tu proyecto. Los commits son muy livianos, y ¡cambiar de uno a otro es terriblemente rápido!

Veamos cómo se ve esto en la práctica. A la derecha tenemos una visualización de un (pequeño) repositorio git. Hay dos commits: el commit inicial, <span class="git commitLinea">C0</span>, y un commit que lo sigue, <span class="git commitLinea">C1</span>, que podría tener algunos cambios interesantes.

![image1](./imatges/imatge_000001.png)

Dale al botón de abajo para crear un nuevo commit.

<div class="sintaxi">
    <span class="prompt">$ </span><span class="ordre">git commit </span><span class=" parametre">-m</span><span classe="cadena"> "Missatge del commit!"</span></div>
<br>

¡Allá va! Increíble. Acabamos de hacer cambios al repositorio y los guardamos como un commit. El commit que acabamos de crear tiene un padre, <span class="git commitLinea">C1</span>, que referencia al commit en el que se basó este.

![image2](./imatges/imatge_000002.png)

¡Venga, inténtalo ahora! Crea **dos commits** para completar el nivel.

![image3](./imatges/imatge_000003.png)

<div class="git">
    <span class="prompt">$ </span><span class="ordre">git commit </span><span class="parametre">-m</span><span classe="cadena"> "Primer (C1) commit!"</span></div>

![image4](./imatges/imatge_000004.png)


<div class="git">
    <span class="prompt">$ </span><span class="ordre">git commit </span><span class=" parametre">-m</span><span classe="cadena"> "Primer commit!"</span></div>

![image5](./imatges/imatge_000005.png)