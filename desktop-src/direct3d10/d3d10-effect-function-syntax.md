---
description: Функция Effect написана на HLSL и объявлена с помощью следующего синтаксиса.
ms.assetid: 5ac85f09-50ac-4e8f-b4d2-ae8306b59348
title: Синтаксис функции Effect (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88521eeb85d1e5f54500a045fe5dcfd81d6be2cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496152"
---
# <a name="effect-function-syntax-direct3d-10"></a>Синтаксис функции Effect (Direct3D 10)

Функция Effect написана на HLSL и объявлена с помощью следующего синтаксиса.

## <a name="syntax"></a>Синтаксис

*ReturnType* *FunctionName* ( \[ *ArgumentList* \] )

{

<dl> \[ *Инструкции* \]
</dl>

};



| Имя         | Описание                                                                                                                                                                                                                                                          |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ReturnType   | Любой [тип HLSL](../direct3dhlsl/dx-graphics-hlsl-variable-syntax.md)                                                                                                                                                                                                       |
| FunctionName | Строка ASCII, однозначно определяющая имя функции шейдера.                                                                                                                                                                                            |
| ArgumentList | Один или несколько аргументов, разделенных запятыми (см. раздел [Function Arguments (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-function-parameters.md)).                                                                                                                             |
| Инструкции   | Одна или несколько инструкций (см. [инструкции (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-statements.md)), которые составляют тело функции. Если функция определена без тела, она считается прототипом; и должны быть переопределены с телом перед использованием. |



 

Функция Effect может быть шейдером или может просто быть функцией, вызываемой шейдером. Функция однозначно идентифицируется по ее имени, типам ее параметров и целевой платформе. Поэтому функции могут быть перегружены. Любая допустимая функция HLSL должна соответствовать этому формату; более подробный список синтаксиса для функций HLSL см. в разделе [функции (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-functions.md).

## <a name="example"></a>Пример

В [примере BasicHLSL10](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx) используется шейдер пикселей и шейдер вершин. Функция шейдера пикселей называется Рендерсценепс и показана ниже.


```
       
PS_OUTPUT RenderScenePS( VS_OUTPUT In,
                         uniform bool bTexture ) 
{ 
    PS_OUTPUT Output;

    // Lookup mesh texture and modulate it with diffuse
    if( bTexture )
        Output.RGBColor = g_MeshTexture.Sample(MeshTextureSampler, In.TextureUV) *  
                              In.Diffuse;
    else
        Output.RGBColor = In.Diffuse;

    return Output;
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Формат эффектов](d3d10-effect-format.md)
</dt> </dl>

 

 
