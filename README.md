# UnityVFXGraphGradientPrimitives
 Originally designed to deal with the situation that the kill component makes particles disappear abruptly.
 
 The left one uses a Kill AABox component, the right one utilizes the gradient box operator to sample alpha value from gradient and thus makes particles fade when they get close enough to the box's surface.
 
 ![FadedKillbox](https://github.com/brainiac19/UnityVFXGraphGradientPrimitives/blob/main/Pictures/FadedKillbox.gif)
 
 Maps gradient (0 ~ 1) to the distance from a particle to the primitive's surface from a specified distance to 0. If a particle is with distance to surface (0 ~ specified distance), the closer it is to the primitive's surface, the output will be closer to gradient(1); the distant it is to the primitive's surface(closer to the specified distance), the output will be closer to gradient(0).
 
 If clamping is used, particles outside the primitive volume will be mapped to gradient(1).
 
 If inverse clamping is used, particles inside the primitive volume will be mapped to gradient(0).
 
  ![Clamping](https://github.com/brainiac19/UnityVFXGraphGradientPrimitives/blob/main/Pictures/Clamping.png)
  