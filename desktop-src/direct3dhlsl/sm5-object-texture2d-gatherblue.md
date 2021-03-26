---
title: 'Функция Texture2D:: Гасерблуе (S, float, int)'
description: 'Возвращает синие компоненты четырех шаг текселя значений, которые будут использоваться в операции линейной фильтрации. | Функция Texture2D:: Гасерблуе (S, float, int)'
ms.assetid: 6d753ef2-2818-4990-81df-52dda044d21d
keywords:
- Функция Гасерблуе HLSL
topic_type:
- apiref
api_name:
- GatherBlue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 54885ccd8f31fdf55270b6c9ac2dbafa1805d866
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986417"
---
# <a name="texture2dgatherbluesfloatint-function"></a>Функция Texture2D:: Гасерблуе (S, float, int)

Возвращает синие компоненты четырех шаг текселя значений, которые будут использоваться в операции линейной фильтрации.

## <a name="syntax"></a>Синтаксис

``` syntax
TemplateType GatherBlue(
  in sampler s,
  in float2 location,
  in int2 offset
);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*s* \[ в\]
</dt> <dd>

Тип: **образец**

Индекс выборки с отсчетом от нуля.

</dd> <dt>

*Расположение* \[ окне\]
</dt> <dd>

Тип: **float2**

Образцы координат (u, v).

</dd> <dt>

*смещение* \[ окне\]
</dt> <dd>

Тип: **int2**

Смещение, применяемое к координате текстуры перед выборкой.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **TemplateType**

Значение из четырех компонентов, тип которого совпадает с типом шаблона.

## <a name="remarks"></a>Примечания

Примеры текстур можно использовать для интерполяции билинейной.

Эта функция поддерживается для следующих типов шейдеров:



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Вычисления |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Методы Гасерблуе](texture2d-gatherblue.md)
</dt> <dt>

[Модель шейдера 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




