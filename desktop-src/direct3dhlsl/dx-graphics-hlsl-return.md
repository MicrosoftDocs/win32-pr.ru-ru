---
title: Оператор return
description: Оператор Return сообщает об окончании функции.
ms.assetid: e6c097af-ba0b-4abc-8099-69882ced1e18
keywords:
- Оператор Return HLSL
topic_type:
- apiref
api_name:
- return Statement
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 525abf6d815d2073ee39a6bc6a5a81120cf652ee
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104983757"
---
# <a name="return-statement"></a>Оператор return

Оператор Return сообщает об окончании функции.



|                   |
|-------------------|
| возвращаемое \[ значение \] ; |



 

Простейший оператор return возвращает управление из функции в вызывающую программу; Он не возвращает значения.


```
void main()
{
    return ;
}
```



Однако оператор return может возвращать одно или несколько значений. В этом примере возвращается литеральное значение:


```
float main( float input : COLOR0) : COLOR0
{
    return 0;
}
```



Этот пример возвращает скалярный результат выражения.


```
return  light.enabled = true ;
```



Этот пример возвращает вектор из четырех компонентов, созданный из локальной переменной и литерала.


```
return  float4(color.rgb, 1) ;
```



Этот пример возвращает вектор из четырех компонентов, созданный из результата, возвращаемого из встроенной функции, вместе с литеральными значениями.


```
float4 func(float2 a: POSITION): COLOR
{
    return float4(sin(length(a) * 100.0) * 0.5 + 0.5, sin(a.y * 50.0), 0, 1);
}
```



В этом примере возвращается структура, содержащая один или несколько элементов.


```
float4x4 WorldViewProj;

struct VS_OUTPUT
{
    float4 Pos  : POSITION;
};

VS_OUTPUT VertexShader_Tutorial_1(float4 inPos : POSITION )
{
    VS_OUTPUT out;
    out.Pos = mul(inPos, WorldViewProj );
    return out;
};
```



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции (DirectX HLSL)](dx-graphics-hlsl-functions.md)
</dt> </dl>

 

 




