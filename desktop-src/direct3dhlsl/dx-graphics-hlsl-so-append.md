---
title: Append (объект DirectX HLSL Stream-Output)
description: Добавление в существующий поток выходных данных с помощью шейдера Geometry-Shader.
ms.assetid: 7df51383-7fc7-4a6f-aaa2-6c929f0443a3
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 19d767f3c501cc42e21bbc44a196ba08cd6f1883
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120189"
---
# <a name="append-directx-hlsl-stream-output-object"></a>Append (объект DirectX HLSL Stream-Output)

Добавление в существующий поток выходных данных с помощью шейдера Geometry-Shader.

Append ( *стреамдататипе*);



 

## <a name="parameters"></a>Параметры



| Элемент                                                                                                                             | Описание                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="StreamDataType"></span><span id="streamdatatype"></span><span id="STREAMDATATYPE"></span>**стреамдататипе**<br/> | Описание входных данных. Это описание должно соответствовать параметру шаблона потока объекта, который называется [DataType](dx-graphics-hlsl-so-type.md).<br/> |



 

## <a name="return-value"></a>Возвращаемое значение

None

## <a name="example"></a>Пример

В этом фрагменте кода (из [примера CubeMapGS](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx)) показан частичный пример добавления примитивов-треугольников к объекту потокового вывода.


```
[maxvertexcount(18)]
void GS_CubeMap( triangle GS_CUBEMAP_IN input[3], 
                 inout TriangleStream<PS_CUBEMAP_IN> CubeMapStream )
{
    for( int f = 0; f < 6; ++f )
    {
        // Compute screen coordinates
        PS_CUBEMAP_IN output;
        output.RTIndex = f;
        for( int v = 0; v < 3; v++ )
        {
            output.Pos = mul( input[v].Pos, g_mViewCM[f] );
            output.Pos = mul( output.Pos, mProj );
            output.Tex = input[v].Tex;
            CubeMapStream.Append( output );
        }
        CubeMapStream.RestartStrip();
    }
}
```



## <a name="minimum-shader-model"></a>Минимальная модель шейдера

Эта функция поддерживается в следующих моделях шейдеров.



| Модель шейдера                                              | Поддерживается |
|-----------------------------------------------------------|-----------|
| [Модель шейдера 4](dx-graphics-hlsl-sm4.md)                | yes       |
| [Модель шейдера 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | Нет        |
| [Модель шейдера 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | Нет        |
| [Модель шейдера 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | Нет        |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Потоковый выходной объект](dx-graphics-hlsl-so-type.md)
</dt> </dl>

 

 





