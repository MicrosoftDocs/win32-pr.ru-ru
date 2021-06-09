---
title: Синтаксис объявления фрагмента (Direct3D 9 HLSL)
description: Каждая функция языка шейдера высокого уровня (HLSL) может быть преобразована в фрагмент шейдера с добавлением объявления фрагмента.
ms.assetid: 34ceef8c-8fb9-4c73-86cc-014b7a2ee4d7
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 60ac1153ff3491bc904f4f759f6653cb4243adff
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/09/2021
ms.locfileid: "111825731"
---
# <a name="fragment-declaration-syntax-direct3d-9-hlsl"></a>Синтаксис объявления фрагмента (Direct3D 9 HLSL)

Каждая функция языка шейдера высокого уровня (HLSL) может быть преобразована в фрагмент шейдера с добавлением объявления фрагмента.

## <a name="syntax"></a>Синтаксис


```
fragmentKeyword FragmentName = compile_fragment shaderProfile FunctionName();
```



где:



| Значение                  | Описание                                                                                                                                                                                                                                                      |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| фрагменткэйворд   | Обязательное ключевое слово. Либо пикселфрагмент, либо вертексфрагмент.                                                                                                                                                                                             |
| фрагментнаме      | Текстовая строка ASCII, указывающая имя скомпилированного фрагмента.                                                                                                                                                                                       |
| компилировать \_ фрагмент | Обязательное ключевое слово.                                                                                                                                                                                                                                     |
| шадерпрофиле     | Модель шейдера для компиляции. Любой допустимый профиль шейдера вершин (см. [**D3DXGetVertexShaderProfile**](/windows/desktop/direct3d9/d3dxgetvertexshaderprofile)) или профиль шейдера пикселей (см. [**D3DXGetPixelShaderProfile**](/windows/desktop/direct3d9/d3dxgetpixelshaderprofile)). |
| FunctionName ()    | Имя функции шейдера, а затем круглые скобки.                                                                                                                                                                                                    |



 

Параметры общего фрагмента помечаются путем добавления \_ префикса "r" к их семантике.


```
void AmbientDiffuse( float3 vPosWorld: r_PosWorld,
                     float3 vNormalWorld: r_NormalWorld,
                     out float4 vColor: COLOR0 )
{  
    // Compute the light vector
    float3 vLight = normalize( g_vLightPosition - vPosWorld );
    
    // Compute the ambient and diffuse components of illumination
    vColor = g_vLightColor * g_vMaterialAmbient;
    vColor += g_vLightColor * g_vMaterialDiffuse * saturate( dot( vLight, vNormalWorld ) );
}
vertexfragment AmbientDiffuseFragment = compile_fragment vs_1_1 AmbientDiffuse();
```



В этом примере \_ семантика r посворлд и r \_ нормалворлд определяют, что эти два параметра являются общими параметрами между другими фрагментами.

> [!Note]  
> Компоновщик фрагментов был технологией Microsoft Direct3D 9 в D3DX 9. Компоновщик фрагментов был средством (Flink.exe), API D3DX 9 и усовершенствованием HLSL. Компоновщик фрагментов был удален в выпуске пакета SDK DirectX за Август 2009. Компоновщик фрагментов никогда не применяется к Microsoft Direct3D 10, Microsoft Direct3D 10,1 или Microsoft Direct3D 11.

 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Модель шейдера 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md)
</dt> </dl>

 

 
