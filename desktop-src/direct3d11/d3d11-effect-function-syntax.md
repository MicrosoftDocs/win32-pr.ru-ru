---
title: Синтаксис функции Effect (Direct3D 11)
description: Функция Effect написана на HLSL и объявлена с синтаксисом, описанным в этом разделе.
ms.assetid: 5e12ba65-98bf-4f21-be75-602687157eb1
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 945f7104d44947f37af71ce664dd99ff64362062b1d42af62af2054538bacb52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046622"
---
# <a name="effect-function-syntax-direct3d-11"></a>Синтаксис функции Effect (Direct3D 11)

Функция Effect написана на HLSL и объявлена с синтаксисом, описанным в этом разделе.

## <a name="syntax"></a>Синтаксис

*ReturnType* *FunctionName* ( \[ *ArgumentList* \] )

{

<dl> \[ *Инструкции* \]
</dl>

};



| Имя         | Описание                                                                                                                                                                                                                                                          |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ReturnType   | Любой [тип HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-variable-syntax)                                                                                                                                                                                                       |
| FunctionName | Строка ASCII, однозначно определяющая имя функции шейдера.                                                                                                                                                                                            |
| ArgumentList | Один или несколько аргументов, разделенных запятыми (см. раздел [Function Arguments (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-function-parameters)).                                                                                                                             |
| Инструкции   | Одна или несколько инструкций (см. [инструкции (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-statements)), которые составляют тело функции. Если функция определена без тела, она считается прототипом; и должны быть переопределены с телом перед использованием. |



 

Функция Effect может быть шейдером или может просто быть функцией, вызываемой шейдером. Функция однозначно идентифицируется по ее имени, типам ее параметров и целевой платформе. Поэтому функции могут быть перегружены. Любая допустимая функция HLSL должна соответствовать этому формату; более подробный список синтаксиса для функций HLSL см. в разделе [функции (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-functions).

## <a name="example"></a>Пример

Ниже приведен пример функции шейдера пикселей.


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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Формат эффектов](d3d11-effect-format.md)
</dt> </dl>

 

 