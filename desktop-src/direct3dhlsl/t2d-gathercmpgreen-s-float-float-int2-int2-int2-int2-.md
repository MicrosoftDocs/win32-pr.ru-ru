---
title: 'Функция Texture2D:: Гасеркмпгрин (S, float, float, int2, int2, int2, int2)'
description: 'Для четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации, функция возвращает сравнение зеленого компонента со значением сравнения. | Функция Texture2D:: Гасеркмпгрин (S, float, float, int2, int2, int2, int2)'
ms.assetid: AC19838B-BA51-408D-8299-DC5F4551628C
keywords:
- Функция Гасеркмпгрин HLSL
topic_type:
- apiref
api_name:
- GatherCmpGreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ffcb312bd450b7c468a1fc83d57ff91b102db8a1
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352742"
---
# <a name="texture2dgathercmpgreensfloatfloatint2int2int2int2-function"></a>Функция Texture2D:: Гасеркмпгрин (S, float, float, int2, int2, int2, int2)

Для четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации, функция возвращает сравнение зеленого компонента со значением сравнения.

## <a name="syntax"></a>Синтаксис


``` syntax
TemplateType GatherCmpGreen(
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

## <a name="remarks"></a>Примечания

Примеры текстур можно использовать для интерполяции билинейной.

Эта функция поддерживается для следующих типов шейдеров:



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Вычисления |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Методы Гасеркмпгрин](texture2d-gathercmpgreen.md)
</dt> </dl>

 

 




