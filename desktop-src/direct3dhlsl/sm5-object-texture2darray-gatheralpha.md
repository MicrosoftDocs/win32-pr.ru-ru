---
title: 'Функция Texture2DArray:: Гасералфа (S, float, int)'
description: 'Возвращает альфа-компоненты четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации. | Функция Texture2DArray:: Гасералфа (S, float, int)'
ms.assetid: d7270277-53c1-4034-bf66-9a95bc1b51e4
keywords:
- Функция Гасералфа HLSL
topic_type:
- apiref
api_name:
- GatherAlpha
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e79805ff931c6fe2da880c3ae090b72b87713b1c0547e6bafcf5986f07b810f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118224"
---
# <a name="texture2darraygatheralphasfloatint-function"></a>Функция Texture2DArray:: Гасералфа (S, float, int)

Возвращает альфа-компоненты четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации.

## <a name="syntax"></a>Синтаксис

``` syntax
TemplateType GatherAlpha(
  in sampler s,
  in float3 location,
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

Тип: **float3**

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

## <a name="remarks"></a>Remarks

Примеры текстур можно использовать для интерполяции билинейной.

Эта функция поддерживается для следующих типов шейдеров:



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Вычисления |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>См. также

<dl> <dt>

[Методы Гасералфа](texture2darray-gatheralpha.md)
</dt> <dt>

[Модель шейдера 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




