# Three.js

A couple of notes/recipes/etc. for working with Three.js (and react-three-fiber.)

### Orienting an object to the direction of a vector

```ts
const forwardAxis = new Vector3(0, 0, 1)
const direction = velocity.clone().normalize()
object.quaternion.setFromUnitVectors(forwardAxis, direction)
```
