---
title: 'Функция Texture2D:: Гасеркмпред (S, float, float, int2, int2, int2, int2)'
description: 'Для четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации, функция возвращает сравнение их красного компонента со значением сравнения. | Функция Texture2D:: Гасеркмпред (S, float, float, int2, int2, int2, int2)'
ms.assetid: B20A766E-0B4F-4FBA-A691-70ACE7BECF33
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
ms.openlocfilehash: 1f5314fb143d8607a66402ca2b27fdf4902ffb08646d55b6fed0702c0979c8b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118507611"
---
# <a name="texture2dgathercmpredsfloatfloatint2int2int2int2-function"></a>Функция Texture2D:: Гасеркмпред (S, float, float, int2, int2, int2, int2)

Для четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации, функция возвращает сравнение их красного компонента со значением сравнения.

## <a name="syntax"></a>Синтаксис


``` syntax
TemplateType GatherCmpRed(
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



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Вычисления |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>См. также

<dl> <dt>

[Методы Гасеркмпред](texture2d-gathercmpred.md)
</dt> </dl>

 

 




