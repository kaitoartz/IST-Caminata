# IST Educa - Unity Template

Esta plantilla incluye interacción EPP + shader de nieve para BRP.

## Qué incluye

- Scripts de interacción por proximidad con tecla `E`
- Recolección de EPP con feedback en UI
- Generador de prefabs desde menú Unity
- Shader BRP de nieve equivalente al render del proyecto JS

## Menú de herramientas

- `Tools > IST Educa > Generate Template Prefabs`
- `Tools > IST Educa > Make Selected Objects EPP Interactable`

## Shader BRP de nieve

Ruta:

- `Assets/ISTEduca/Shaders/IST_Snow_BRPCustom.shader`

Inspirado en el material JS (`meshStandardMaterial`) con:

- albedo (`map`)
- normal (`normalMap`)
- roughness (`roughnessMap`)
- AO (`aoMap`)
- displacement (`displacementMap`)

Mapeo recomendado con tus assets:

- `_MainTex` -> `snow-color.avif.jpg`
- `_NormalMap` -> `snow-normal-gl.avif.jpg`
- `_RoughnessMap` -> `snow-roughness.avif.png`
- `_AOMap` -> `snow-ambientocclusion.avif.png`
- `_HeightMap` -> `snow-displacement.avif.png`

Valores iniciales recomendados:

- `_DisplacementScale = 2`
- `_AOIntensity = 1`
- `_RoughnessStrength = 1`
- `_Metallic = 0`

Opcional para huellas dinámicas:

- `_FootprintMap` (máscara de huellas)
- `_FootprintStrength`

## Uso rápido

1. Copia `UnityTemplate/Assets/ISTEduca` dentro de `Assets/` de tu proyecto Unity.
2. Genera prefabs con el menú de Tools.
3. Crea un material con shader `ISTEduca/Environment/SnowBRP`.
4. Asigna las texturas y aplica el material al terreno/malla de nieve.
