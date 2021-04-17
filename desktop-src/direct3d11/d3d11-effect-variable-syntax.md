---
title: Синтаксис переменной Effect (Direct3D 11)
description: Переменная Effect объявляется с помощью синтаксиса, описанного в этом разделе.
ms.assetid: c0cfc9dd-2df3-4f38-a0e4-2e494456b3c9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67710642060ffea642434ba2d23a77cec2fb8bc3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487753"
---
# <a name="effect-variable-syntax-direct3d-11"></a>Синтаксис переменной Effect (Direct3D 11)

Переменная Effect объявляется с помощью синтаксиса, описанного в этом разделе.

## <a name="syntax"></a>Синтаксис

Базовый синтаксис:

*DataType* *variablename* \[ *: семантикнаме* \]  <  *Annotations*  >  \[ = инитиалвалуе \] ;

Полный синтаксис см. в разделе [синтаксис переменных (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-variable-syntax) .



| Имя         | Описание                                                                                                                                                                                 |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DataType     | Любое [базовое](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-variable-syntax), [текстурное](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-type), неупорядоченное представление доступа, шейдер или тип блока состояния.                            |
| VariableName | Строка ASCII, однозначно определяющая имя переменной Effect.                                                                                                                   |
| семантикнаме | Строка ASCII, указывающая дополнительные сведения о том, как должна использоваться переменная. Семантика — это строка ASCII, которая может быть стандартной системой или пользовательской строкой. |
| Заметки  | Один или несколько фрагментов предоставленных пользователем данных (метаданных), которые игнорируются системой эффектов. Синтаксис см. в разделе [синтаксис аннотации (Direct3D 11)](d3d11-effect-annotation-syntax.md).     |
| инитиалвалуе | Значение переменной по умолчанию.                                                                                                                                                          |



 

Переменная Effect, объявленная вне всех функций, считается глобальной в области видимости. переменные, объявленные внутри функции, являются локальными для этой функции.

## <a name="example"></a>Например, .

В этом примере показаны числовые переменные глобальных эффектов.


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



В этом примере показано объявление глобальной переменной текстуры.


```
Texture2D g_MeshTexture;            // Color texture for mesh
```



Выборка текстуры осуществляется с помощью образца текстуры. Чтобы настроить образец в результате, см. [тип образца](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler).

В этом примере показано объявление глобальных переменных представления неупорядоченного доступа.


```
RWStructuredBuffer<uint> bc : register(u2) < string name="bc"; >;
RWBuffer<uint> bRW;
struct S
{
   uint key;
   uint value;
};
AppendStructuredBuffer<S> asb : register(u5);
RWByteAddressBuffer rwbab : register(u1);
RWStructuredBuffer<uint> rwsb : register(u3);
RWTexture1D<float> rwt1d : register(u1);
RWTexture1DArray<uint> rwt1da : register(u4);
RWTexture2D<uint> rwt2d : register(u2);
RWTexture2DArray<uint> rwt2da : register(u6);
RWTexture3D<uint> rwt3d : register(u7); 
 This example illustrates declaring global shader variables.
VertexShader pVS = CompileShader( vs_5_0, VS() );
HullShader pHS = NULL;
DomainShader pDS = NULL;
GeometryShader pGS = ConstructGSWithSO( CompileShader( gs_5_0, VS() ), 
                                        "0:Position.xy; 1:Position.zw; 2:Color.xy", 
                                        "3:Texcoord.xyzw; 3:$SKIP.x;", 
                                        NULL, 
                                        NULL, 
                                        1 );
PixelShader pPS = NULL;
ComputeShader pCS = NULL;
This example illustrates declaring global state block variables.
BlendState myBS[2] < bool IsValid = true; >
{
  {
    BlendEnable[0] = false;
  },
  {
    BlendEnable[0] = true;
    SrcBlendAlpha[0] = Inv_Src_Alpha;
  }
};

RasterizerState myRS
{
      FillMode = Solid;
      CullMode = NONE;
      MultisampleEnable = true;
      DepthClipEnable = false;
};

DepthStencilState myDS
{
    DepthEnable = false;
    DepthWriteMask = Zero;
    DepthFunc = Less;
};
sampler mySS[2] : register(s3) 
{
    {
        Filter = ANISOTROPIC;
        MaxAnisotropy = 3;
    },
    {
        Filter = ANISOTROPIC;
        MaxAnisotropy = 4;
    }
};
  
  
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Формат эффектов](d3d11-effect-format.md)
</dt> </dl>

 

 