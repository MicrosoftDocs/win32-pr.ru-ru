---
title: 'Функция Texture2DArray:: Гасеркмпред (S, float, float, int)'
description: 'Для четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации, функция возвращает сравнение их красного компонента со значением сравнения. | Функция Texture2DArray:: Гасеркмпред (S, float, float, int)'
ms.assetid: aa7fadf8-fe96-406a-9c93-9ae0c59ef087
keywords:
- Функция Гасеркмпред HLSL
topic_type:
- apiref
api_name:
- GatherCmpRed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: aea723bbcdc2822adb8084cbdb5feff155165158d3abaf872a96259a77accdcc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117724615"
---
# <a name="texture2darraygathercmpredsfloatfloatint-function"></a>Функция Texture2DArray:: Гасеркмпред (S, float, float, int)

Для четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации, функция возвращает сравнение их красного компонента со значением сравнения.

## <a name="syntax"></a>Синтаксис

``` syntax
float4 GatherCmpRed(
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



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Службы вычислений |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Методы Гасеркмпред](texture2darray-gathercmpred.md)
</dt> <dt>

[Модель шейдера 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




