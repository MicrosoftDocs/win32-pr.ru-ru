---
title: 'Функция Texture2D:: Гасеркмпалфа (S, float, float, int2, int2, int2, int2)'
description: 'Для четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации, функция возвращает сравнение альфа-компонента со значением сравнения. | Функция Texture2D:: Гасеркмпалфа (S, float, float, int2, int2, int2, int2)'
ms.assetid: C8325626-F281-4D10-9299-0E5DA01BB1BD
keywords:
- Функция Гасеркмпалфа HLSL
topic_type:
- apiref
api_name:
- GatherCmpAlpha
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cbeb6a37abe3100a7709230769ab7c4afa5b246737c9a4d0c1c37337e9462eb2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117904547"
---
# <a name="texture2dgathercmpalphasfloatfloatint2int2int2int2-function"></a>Функция Texture2D:: Гасеркмпалфа (S, float, float, int2, int2, int2, int2)

Для четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации, функция возвращает сравнение альфа-компонента со значением сравнения.

## <a name="syntax"></a>Синтаксис


``` syntax
TemplateType GatherCmpAlpha(
  in SamplerState S,
  in float        Location,
  in float        CompareValue,
  in int2         Offset1,
  in int2         Offset2,
  in int2         Offset3,
  in int2         Offset4
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*S* \[ в\]
</dt> <dd>

Тип: **самплерстате**

Индекс выборки с отсчетом от нуля.

</dd> <dt>

*Расположение* \[ окне\]
</dt> <dd>

Тип: **float**

Образцы координат (u, v).

</dd> <dt>

*Компаревалуе* \[ окне\]
</dt> <dd>

Тип: **float**

Значение, сравниваемое по каждому значению выборки.

</dd> <dt>

*Offset1* \[ окне\]
</dt> <dd>

Тип: **int2**

Первый компонент смещения, применяемый к координатам текстуры перед выборкой.

</dd> <dt>

*Offset2* \[ окне\]
</dt> <dd>

Тип: **int2**

Второй компонент смещения, применяемый к координатам текстуры перед выборкой.

</dd> <dt>

*Offset3* \[ окне\]
</dt> <dd>

Тип: **int2**

Третий компонент смещения, применяемый к координатам текстуры перед выборкой.

</dd> <dt>

*Offset4* \[ окне\]
</dt> <dd>

Тип: **int2**

Четвертый компонент смещения, применяемый к координатам текстуры перед выборкой.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **TemplateType**

Значение из четырех компонентов, тип которого совпадает с типом шаблона.

## <a name="remarks"></a>Remarks

Примеры текстур можно использовать для интерполяции билинейной.

Эта функция поддерживается для следующих типов шейдеров:



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Службы вычислений |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Методы Гасеркмпалфа](texture2d-gathercmpalpha.md)
</dt> </dl>

 

 




