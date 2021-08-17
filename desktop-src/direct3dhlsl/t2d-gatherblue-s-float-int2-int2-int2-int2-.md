---
title: 'Функция Texture2D:: Гасерблуе (S, float, int2, int2, int2, int2)'
description: 'Возвращает синие компоненты четырех шаг текселя значений, которые будут использоваться в операции линейной фильтрации. | Функция Texture2D:: Гасерблуе (S, float, int2, int2, int2, int2)'
ms.assetid: 0FFD3D82-E849-4C19-BEBC-85B9CCA40CA0
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
ms.openlocfilehash: d71f166a6e4ea205a8d2e41579e3907576314ce93aaf14cbc926b86e2cbe09e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118507760"
---
# <a name="gatherbluesfloatint2int2int2int2-function"></a>Функция Гасерблуе (S, float, int2, int2, int2, int2)

Возвращает синие компоненты четырех шаг текселя значений, которые будут использоваться в операции линейной фильтрации.

## <a name="syntax"></a>Синтаксис


``` syntax
TemplateType GatherBlue(
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

## <a name="remarks"></a>Remarks

Примеры текстур можно использовать для интерполяции билинейной.

Эта функция поддерживается для следующих типов шейдеров:



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Службы вычислений |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Методы Гасерблуе](texture2d-gatherblue.md)
</dt> </dl>

 

 




