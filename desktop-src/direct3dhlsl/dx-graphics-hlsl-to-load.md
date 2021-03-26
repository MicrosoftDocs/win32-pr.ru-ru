---
title: Load (объект текстуры DirectX HLSL)
description: Считывает данные шаг текселя без какой бы то ни было фильтрации или выборки.
ms.assetid: a2fbda88-29c7-4d28-bd3e-df1d9aa36ee8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 08d3964788a238492ff7d5189544603b35808465
ms.sourcegitcommit: 4c00910ed754d7d0a68c9a833751d714c06e3b39
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "104139198"
---
# <a name="load-directx-hlsl-texture-object"></a>Load (объект текстуры DirectX HLSL)

Считывает данные шаг текселя без какой бы то ни было фильтрации или выборки.



<table>
<tbody>
<tr class="odd">
<td>Объект Ret. Load (<dl> Расположение Типекс,<br />
[Типекс SampleIndex,]<br />
[смещение Типекс]<br />
</dl>);</td>
</tr>
</tbody>
</table>

Типекс указывает, что существует четыре возможных типа: **int**, **int2**,, **корпус** или **INT4**.

 

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Объектами*
</dt> <dd>

Тип [объекта текстуры](dx-graphics-hlsl-to-type.md) (за исключением Текстурекубе или текстурекубеаррай).

</dd> <dt>

<span id="Location"></span><span id="location"></span><span id="LOCATION"></span>*Места*
</dt> <dd>

\[в \] координатах текстуры последний компонент указывает уровень mipmap. Этот метод использует систему координат на основе 0, а не систему 0,0-1,0 UV. Тип аргумента зависит от типа объекта текстуры.



| Тип объекта                                  | Тип параметра |
|----------------------------------------------|----------------|
| Буфер                                       | INT            |
| Texture1D, Texture2DMS                       | int2           |
| Texture1DArray, 2D-текстура, Texture2DMSArray | int3           |
| Texture2DArray, Texture3D                    | int4           |



 

Например, чтобы получить доступ к двухмерной текстуре, укажите UV-координаты для первых двух компонентов и уровень mipmap для третьего компонента.

> [!Note]  
> Если одно или несколько координат в *расположении* превышают размеры mipmap в единицах измерения u, v или w, то **Load** возвращает ноль во всех компонентах. Direct3D гарантирует возврат нуля для любого ресурса, доступ к которому осуществляется вне границ.

 

</dd> <dt>

<span id="SampleIndex"></span><span id="sampleindex"></span><span id="SAMPLEINDEX"></span>*SampleIndex*
</dt> <dd>

\[в \] необязательном индексе выборки.



| Тип текстуры                                                                                                   | Тип параметра |
|----------------------------------------------------------------------------------------------------------------|----------------|
| Texture1D, Texture1DArray, Texture2D, Texture2DArray, Texture3D, Texture2DArray, Текстурекубе, Текстурекубеаррай | не поддерживается  |
| Texture2DMS, Texture2DMSArray ¹                                                                                 | INT            |



 

> [!Note]  
> *SampleIndex* доступен только для многопримерных текстур.

 

</dd> <dt>

<span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span>*Собой*
</dt> <dd>

\[в \] необязательном смещении, применяемом к координатам текстуры перед выборкой. Тип смещения зависит от типа объекта «текстура» и должен быть статическим.



| Тип текстуры                                             | Тип параметра |
|----------------------------------------------------------|----------------|
| Texture1D, Texture1DArray                                | INT            |
| Texture2D, Texture2DArray, Texture2DMS, Texture2DMSArray | int2           |
| Texture3D, Texture2DArray                                | int3           |



 

> [!Note]  
> Если используется *смещение* с несколькими образцами текстур, необходимо также указать *SampleIndex*.

 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемый тип соответствует типу в объявлении *объекта* . Например, Объект Texture2D, объявленный как "Texture2d <uint4> митекстуре;", имеет возвращаемое значение типа **uint4**.

## <a name="minimum-shader-model"></a>Минимальная модель шейдера

Эта функция поддерживается в следующих моделях шейдеров.



| VS \_ 4 \_ 0 | VS \_ 4 \_ 1 ¹ | PS \_ 4 \_ 0 | PS \_ 4 \_ 1 ¹ | GS \_ 4 \_ 0 | GS \_ 4 \_ 1 ¹ |
|----------|-----------|----------|-----------|----------|-----------|
| x        | x         | x        | x         | x        | x         |



 

-   Модель шейдеров 4,1 доступна в Direct3D 10,1 или более поздней версии.

## <a name="example"></a>Например, .

Этот частичный пример кода относится к файлу Paint. FX в [образце адванцедпартиклес](https://msdn.microsoft.com/library/Ee416394(v=VS.85).aspx).


```
// Object Declarations
Buffer<float4> g_ParticleBuffer;

// Shader body calling the intrinsic function
float4 PSPaint(PSQuadIn input) : SV_Target
{       
    ... 
    for( int i=g_ParticleStart; i<g_NumParticles; i+=g_ParticleStep )
    {
        ... 
        // load the particle
        float4 particlePos = g_ParticleBuffer.Load( i*4 );
        float4 particleColor = g_ParticleBuffer.Load( (i*4) + 2 );
        ...     
    }
    ...
}   
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Текстура-объект](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 




