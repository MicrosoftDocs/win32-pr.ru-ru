---
title: SV_InsideTessFactor
description: Определяет объем тесселяции в области исправления.
ms.assetid: f0762aca-d84d-44c0-a163-9737ef92c1e5
keywords:
- SV_InsideTessFactor HLSL
topic_type:
- apiref
api_name:
- SV_InsideTessFactor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 043d1a43186623e81cb529d2906d4475291547d326bf2d75758c8ee696a812b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118285510"
---
# <a name="sv_insidetessfactor"></a>ОКП \_ инсидетессфактор

Определяет объем тесселяции в области исправления.

## <a name="type"></a>Тип



|  Тип          | Топология ввода               |
|------------|----------------|
| float \[ 2\] | четыре исправления     |
| FLOAT      | три исправления      |
| unused     | исолине        |



 

Факторы тесселяции должны быть объявлены как массив. они не могут быть упакованы в один вектор.

## <a name="remarks"></a>Remarks

Это значение должно быть определено во время функции Constant исправления шейдера поверхности.

Обязательное выходное значение для шейдера поверхности при использовании исправлений с четырьмя или тремя обновлениями. Это значение является обязательным входом для шейдера домена, чтобы оборудование соответствовало сигнатурам через тесселяцию.

Эта функция поддерживается в следующих типах шейдеров:



| Вершина | Поверхности | Домен | Geometry | Пиксель | Вычисления |
|--------|------|--------|----------|-------|---------|
|        | x    | x      |          |       |         |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Семантика](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[Модель шейдера 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




