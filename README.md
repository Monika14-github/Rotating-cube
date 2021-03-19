# Rotating-cube
......html.........
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width">
    <title>repl.it</title>
    <link href="style.css" rel="stylesheet" type="text/css" />
  </head>
  <body>
    <div class="container">
  <div class="flex">
    <div class="cube">
      <div class="wall front"></div>
      <div class="wall back"></div>
      <div class="wall left"></div>
      <div class="wall right"></div>
      <div class="wall top"></div>
      <div class="wall bottom"></div>
    </div>
    <div class="cube">
      <div class="wall front"></div>
      <div class="wall back"></div>
      <div class="wall left"></div>
      <div class="wall right"></div>
      <div class="wall top"></div>
      <div class="wall bottom"></div>
    </div>
    <div class="cube">
      <div class="wall front"></div>
      <div class="wall back"></div>
      <div class="wall left"></div>
      <div class="wall right"></div>
      <div class="wall top"></div>
      <div class="wall bottom"></div>
    </div>
    <div class="cube">
      <div class="wall front"></div>
      <div class="wall back"></div>
      <div class="wall left"></div>
      <div class="wall right"></div>
      <div class="wall top"></div>
      <div class="wall bottom"></div>
    </div>
  </div>
  <div class="flex">
    <div class="cube">
      <div class="wall front"></div>
      <div class="wall back"></div>
      <div class="wall left"></div>
      <div class="wall right"></div>
      <div class="wall top"></div>
      <div class="wall bottom"></div>
    </div>
    <div class="cube">
      <div class="wall front"></div>
      <div class="wall back"></div>
      <div class="wall left"></div>
      <div class="wall right"></div>
      <div class="wall top"></div>
      <div class="wall bottom"></div>
    </div>
    <div class="cube">
      <div class="wall front"></div>
      <div class="wall back"></div>
      <div class="wall left"></div>
      <div class="wall right"></div>
      <div class="wall top"></div>
      <div class="wall bottom"></div>
    </div>
    <div class="cube">
      <div class="wall front"></div>
      <div class="wall back"></div>
      <div class="wall left"></div>
      <div class="wall right"></div>
      <div class="wall top"></div>
      <div class="wall bottom"></div>
    </div>
  </div>
  <div class="flex">
    <div class="cube">
      <div class="wall front"></div>
      <div class="wall back"></div>
      <div class="wall left"></div>
      <div class="wall right"></div>
      <div class="wall top"></div>
      <div class="wall bottom"></div>
    </div>
    <div class="cube">
      <div class="wall front"></div>
      <div class="wall back"></div>
      <div class="wall left"></div>
      <div class="wall right"></div>
      <div class="wall top"></div>
      <div class="wall bottom"></div>
    </div>
    <div class="cube">
      <div class="wall front"></div>
      <div class="wall back"></div>
      <div class="wall left"></div>
      <div class="wall right"></div>
      <div class="wall top"></div>
      <div class="wall bottom"></div>
    </div>
    <div class="cube">
      <div class="wall front"></div>
      <div class="wall back"></div>
      <div class="wall left"></div>
      <div class="wall right"></div>
      <div class="wall top"></div>
      <div class="wall bottom"></div>
    </div>
  </div>
  <div class="flex">
    <div class="cube">
      <div class="wall front"></div>
      <div class="wall back"></div>
      <div class="wall left"></div>
      <div class="wall right"></div>
      <div class="wall top"></div>
      <div class="wall bottom"></div>
    </div>
    <div class="cube">
      <div class="wall front"></div>
      <div class="wall back"></div>
      <div class="wall left"></div>
      <div class="wall right"></div>
      <div class="wall top"></div>
      <div class="wall bottom"></div>
    </div>
    <div class="cube">
      <div class="wall front"></div>
      <div class="wall back"></div>
      <div class="wall left"></div>
      <div class="wall right"></div>
      <div class="wall top"></div>
      <div class="wall bottom"></div>
    </div>
    <div class="cube">
      <div class="wall front"></div>
      <div class="wall back"></div>
      <div class="wall left"></div>
      <div class="wall right"></div>
      <div class="wall top"></div>
      <div class="wall bottom"></div>
    </div>
  </div>
</div>
  </body>
</html>
..........css........
html,
body {
  position: relative;
  overflow: hidden;
}

body {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  margin: 0;
  background: radial-gradient(circle at center, rgb(95, 218, 240), rgb(2, 104, 129));
  transform-style: preserve-3d;
  -webkit-transform-style: preserve-3d;
}

.flex {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 80px;
  height: 80px;
  margin: 0 -80px 0 0;
}

/* cube */
.cube {
  position: relative;
  width: 1px;
  height: 1px;
  margin: 0 80px 0 0;
  transform-style: preserve-3d;
}

.wall {
  width: 80px;
  height: 80px;
  position: absolute;
  left: calc(-80px / 2);
  top: calc(-80px / 2);
  text-align: center;
  line-height: 100px;
  border: solid 1px rgba(146, 3, 3, 0.89);
}

.front {
  transform: translateZ(calc(80px / 2));
}

.back {
  transform: translateZ(calc(-80px / 2)) rotateY(180deg);
}

.right {
  transform: translateX(calc(80px / 2)) rotateY(90deg);
}

.left {
  transform: translateX(calc(-80px / 2)) rotateY(-90deg);
}

.top {
  transform: translateY(calc(-80px / 2)) rotateX(90deg);
}

.bottom {
  transform: translateY(calc(80px / 2)) rotateX(-90deg);
}

/* animation */
.flex:nth-of-type(4) .cube:nth-of-type(1) {
  animation: rotation 3s cubic-bezier(0.215, 0.61, 0.355, 1) 0.5s forwards;
}

.flex:nth-of-type(3) .cube:nth-of-type(1) {
  animation: rotation 3s cubic-bezier(0.215, 0.61, 0.355, 1) 0.6s forwards;
}

.flex:nth-of-type(4) .cube:nth-of-type(2) {
  animation: rotation 3s cubic-bezier(0.215, 0.61, 0.355, 1) 0.6s forwards;
}

.flex:nth-of-type(2) .cube:nth-of-type(1) {
  animation: rotation 3s cubic-bezier(0.215, 0.61, 0.355, 1) 0.7s forwards;
}

.flex:nth-of-type(3) .cube:nth-of-type(2) {
  animation: rotation 3s cubic-bezier(0.215, 0.61, 0.355, 1) 0.7s forwards;
}

.flex:nth-of-type(4) .cube:nth-of-type(3) {
  animation: rotation 3s cubic-bezier(0.215, 0.61, 0.355, 1) 0.8s forwards;
}

.flex:nth-of-type(1) .cube:nth-of-type(1) {
  animation: rotation 3s cubic-bezier(0.215, 0.61, 0.355, 1) 0.8s forwards;
}

.flex:nth-of-type(2) .cube:nth-of-type(2) {
  animation: rotation 3s cubic-bezier(0.215, 0.61, 0.355, 1) 0.8s forwards;
}

.flex:nth-of-type(3) .cube:nth-of-type(3) {
  animation: rotation 3s cubic-bezier(0.215, 0.61, 0.355, 1) 0.8s forwards;
}

.flex:nth-of-type(4) .cube:nth-of-type(4) {
  animation: rotation 3s cubic-bezier(0.215, 0.61, 0.355, 1) 0.8s forwards;
}

.flex:nth-of-type(1) .cube:nth-of-type(2) {
  animation: rotation 3s cubic-bezier(0.215, 0.61, 0.355, 1) 0.9s forwards;
}

.flex:nth-of-type(2) .cube:nth-of-type(3) {
  animation: rotation 3s cubic-bezier(0.215, 0.61, 0.355, 1) 0.9s forwards;
}

.flex:nth-of-type(3) .cube:nth-of-type(4) {
  animation: rotation 3s cubic-bezier(0.215, 0.61, 0.355, 1) 0.9s forwards;
}

.flex:nth-of-type(1) .cube:nth-of-type(3) {
  animation: rotation 3s cubic-bezier(0.215, 0.61, 0.355, 1) 1s forwards;
}

.flex:nth-of-type(2) .cube:nth-of-type(4) {
  animation: rotation 3s cubic-bezier(0.215, 0.61, 0.355, 1) 1s forwards;
}

.flex:nth-of-type(1) .cube:nth-of-type(4) {
  animation: rotation 3s cubic-bezier(0.215, 0.61, 0.355, 1) 1.1s forwards;
}

@keyframes rotation {
  100% {
    transform: rotateX(360deg) rotateY(360deg);
  }
}
.wall {
  animation: color 2s linear 1.5s forwards;
}

@keyframes color {
  100% {
    background-color: rgb(6, 7, 0);
  }
}
