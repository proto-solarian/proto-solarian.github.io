# Hikari
A rendering API and game engine research project.
## Technologies
Languages: C/C++, Slang (HLSL)
Utilities:
- Vulkan 1.3
- GLM
- No other APIs, Libraries, or Frameworks were used 
## Engine Features
- Wavefront .OBJ file importer
- 3-Part Architecture:
  - Engine
  - App (Editor base)
  - Shared libraries
- Scene object hierarchy/composable transform tree
- Customizable scene object behaviors
- Entity-Component System consideration for memory locality (i.e.: customized behaviors exist in contiguous memory and are executed sequentially)
- Built with Windows and Android in mind, but currently only supports Windows
## Renderer Features
- A completely bespoke vulkan-based renderer called Prometheus
- Simple, diffuse shading
- Highly performant frame updates
## Upcoming Engine Features (Short Term)
- Image importing (AVIF or Webp possible, but TIFF to support artist workflows - this is likely to introduce my second library)
- More mesh importing (FBX likely, GLTF/GLB ideal)
- Android support
- Input handling
## Upcoming Renderer Features
- Texturing
- PBR Shading
- Skyboxes
- Transparency
