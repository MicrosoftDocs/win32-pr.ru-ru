---
title: 'Функция Texture2D:: собрать (S, float, int)'
description: 'Возвращает четыре значения шаг текселя, которые будут использоваться в операции линейной фильтрации. | Функция Texture2D:: собрать (S, float, int)'
ms.assetid: 5d196c1c-8cc9-4add-9d33-654294314ee2
keywords:
- Собрать функцию HLSL
topic_type:
- apiref
api_name:
- Gather
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4d0a58be0580572441f91a3b3f637601d70cd9c8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "103820701"
---
# <a name="texture2dgathersfloatint-function"></a>Функция Texture2D:: собрать (S, float, int)

Возвращает четыре значения шаг текселя, которые будут использоваться в операции линейной фильтрации.

## <a name="syntax"></a>Синтаксис

``` syntax
TemplateType Gather(
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

Смещение, применяемое к координатам текстуры перед выборкой.

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

[Собрать методы](texture2d-gather.md)
</dt> <dt>

[Модель шейдера 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




