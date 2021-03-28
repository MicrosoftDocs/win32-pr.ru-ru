---
title: 'Функция Texture2D:: Гасералфа (S, float, int2, int2, int2, int2)'
description: 'Возвращает альфа-компоненты четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации. | Функция Texture2D:: Гасералфа (S, float, int2, int2, int2, int2)'
ms.assetid: 925A5085-33CB-4DFC-B4E3-1ADA5892C13A
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
ms.openlocfilehash: 4dc2077c8c10d9a7caba1c9d7a3999ffd522b5ab
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998202"
---
# <a name="texture2dgatheralphasfloatint2int2int2int2-function"></a>Функция Texture2D:: Гасералфа (S, float, int2, int2, int2, int2)

Возвращает альфа-компоненты четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации.

## <a name="syntax"></a>Синтаксис


``` syntax
TemplateType GatherAlpha(
  in SamplerState S,
  in float        Location,
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

[Методы Гасералфа](texture2d-gatheralpha.md)
</dt> </dl>

 

 




