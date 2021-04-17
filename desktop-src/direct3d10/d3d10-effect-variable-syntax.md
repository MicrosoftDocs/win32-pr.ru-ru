---
description: Переменная Effect объявляется с помощью следующего синтаксиса.
ms.assetid: 53939c65-3725-44cc-bec6-775c3b921770
title: Синтаксис переменной Effect (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8068571ff393e83ba0ae11eb2f9cb62f0bbb49df
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423369"
---
# <a name="effect-variable-syntax-direct3d-10"></a>Синтаксис переменной Effect (Direct3D 10)

Переменная Effect объявляется с помощью следующего синтаксиса.

## <a name="syntax"></a>Синтаксис

*DataType* *variablename* \[ : *семантикнаме* \]  <  *Annotations* >;



| Имя         | Описание                                                                                                                                                                                 |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DataType     | Любой тип [базовой](../direct3dhlsl/dx-graphics-hlsl-variable-syntax.md) или [текстуры](../direct3dhlsl/dx-graphics-hlsl-to-type.md) .                                                                        |
| VariableName | Строка ASCII, однозначно определяющая имя переменной Effect.                                                                                                                   |
| семантикнаме | Строка ASCII, указывающая дополнительные сведения о том, как должна использоваться переменная. Семантика — это строка ASCII, которая может быть стандартной системой или пользовательской строкой. |
| Заметки  | Один или несколько фрагментов предоставленных пользователем данных (метаданных), которые игнорируются системой эффектов. Синтаксис см. в разделе [синтаксис аннотации (Direct3D 10)](d3d10-effect-annotation-syntax.md).     |



 

Переменная Effect, объявленная вне всех функций, считается глобальной в области видимости. переменные, объявленные внутри функции, являются локальными для этой функции.

## <a name="example"></a>Пример

В [примере BasicHLSL10](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx) используются глобальные переменные без семантики для цветов материала, свойств освещения и матриц преобразования.

В этом примере показаны переменные глобальных эффектов.


```
float4 g_MaterialAmbientColor;      // Material's ambient color
float4 g_MaterialDiffuseColor;      // Material's diffuse color
float3 g_LightDir[3];               // Light's direction in world space
float4x4 g_mWorld;                  // World matrix for object
```



В этом примере показаны переменные, являющиеся локальными для функции шейдера.


```
VS_OUTPUT RenderSceneVS( ... )
{
    float3 vNormalWorldSpace;
    float4 vAnimatedPos;

    // shader body
}
```



В этом примере показаны параметры функции, имеющие семантику.


```
VS_OUTPUT RenderSceneVS( float4 vPos : SV_POSITION,
                         float3 vNormal : NORMAL,
                         float2 vTexCoord0 : TEXCOORD0,
                         uniform int nNumLights,
                         uniform bool bTexture,
                         uniform bool bAnimate )
{
  ...
}
```



В этом примере показано объявление переменной текстуры.


```
Texture2D g_MeshTexture;            // Color texture for mesh
```



Выборка текстуры осуществляется с помощью образца текстуры. Чтобы настроить образец в результате, см. [тип образца](../direct3dhlsl/dx-graphics-hlsl-sampler.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Формат эффектов](d3d10-effect-format.md)
</dt> </dl>

 

 
