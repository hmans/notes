# Babylon.js

### Starter Template for Babylon.js in Vite

```ts
import "./style.css";
import * as BABYLON from "babylonjs";

const canvas = document.getElementById("game") as HTMLCanvasElement;
const engine = new BABYLON.Engine(canvas, true);
const scene = new BABYLON.Scene(engine);

const camera = new BABYLON.ArcRotateCamera(
  "camera",
  -Math.PI / 2,
  Math.PI / 2.5,
  3,
  new BABYLON.Vector3(0, 0, 0),
  scene
);
camera.attachControl(canvas, true);

const light = new BABYLON.HemisphericLight(
  "light",
  new BABYLON.Vector3(0, 1, 0),
  scene
);

const box = BABYLON.MeshBuilder.CreateBox("box", {}, scene);

engine.runRenderLoop(function () {
  scene.render();
});

window.addEventListener("resize", function () {
  engine.resize();
});
```
