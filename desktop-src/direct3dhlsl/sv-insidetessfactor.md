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
ms.openlocfilehash: 90d31aa6a11ce8e2bdd75ff1171705cc9b3de437
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826618"
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

 

 




