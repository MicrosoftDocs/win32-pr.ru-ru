---
title: 'Функция Texture2DArray:: Гасеркмпблуе (S, float, float, int)'
description: 'Для четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации, функция возвращает сравнение их синего компонента со значением сравнения. | Функция Texture2DArray:: Гасеркмпблуе (S, float, float, int)'
ms.assetid: 5fa23e27-368a-4c55-b6d6-33506c932a43
keywords:
- Функция Гасеркмпблуе HLSL
topic_type:
- apiref
api_name:
- GatherCmpBlue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8b8783bf9c8fcb628d6d67a2e099877d67de7c84229d8f8f8e48769386b12e6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985897"
---
# <a name="texture2darraygathercmpbluesfloatfloatint-function"></a>Функция Texture2DArray:: Гасеркмпблуе (S, float, float, int)

Для четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации, функция возвращает сравнение их синего компонента со значением сравнения.

## <a name="syntax"></a>Синтаксис

``` syntax
float4 GatherCmpBlue(
  in SamplerComparisonState s,
  in float3 location,
  in float compare_value,
  in int2 offset
);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*s* \[ в\]
</dt> <dd>

Тип: **самплеркомпарисонстате**

Индекс выборки с отсчетом от нуля.

</dd> <dt>

*Расположение* \[ окне\]
</dt> <dd>

Тип: **float3**

Образцы координат (u, v).

</dd> <dt>

*сравнить \_ значение* \[ в\]
</dt> <dd>

Тип: **float**

Значение, сравниваемое по каждому значению выборки.

</dd> <dt>

*смещение* \[ окне\]
</dt> <dd>

Тип: **int2**

Смещение, применяемое к координате текстуры перед выборкой.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **float4**

Значение из четырех компонентов, каждый компонент которого является результатом сравнения каждого компонента.

## <a name="remarks"></a>Remarks

Примеры текстур можно использовать для интерполяции билинейной.

Эта функция поддерживается для следующих типов шейдеров:



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Вычисления |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Методы Гасеркмпблуе](texture2darray-gathercmpblue.md)
</dt> <dt>

[Модель шейдера 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




