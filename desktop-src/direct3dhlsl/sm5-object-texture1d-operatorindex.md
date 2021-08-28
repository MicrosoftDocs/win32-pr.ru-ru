---
title: 'Функция Texture1D:: operator'
description: Возвращает переменную ресурса, доступную только для чтения, для Texture1D.
ms.assetid: df54097d-4d1b-496a-a17d-6e9a10cfb996
keywords:
- Оператор Function HLSL
topic_type:
- apiref
api_name:
- Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d2c11ef313531adb9b129ffb99103ea6c7778462eddf8c1c76f4b235c92951c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985914"
---
# <a name="texture1doperator--function"></a>Функция Texture1D:: operator

Возвращает переменную ресурса, доступную только для чтения, для [**Texture1D**](sm5-object-texture1d.md).

## <a name="syntax"></a>Синтаксис

``` syntax
R Operator[](
  in uint pos
);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*POS-терминал* \[ окне\]
</dt> <dd>

Тип: **uint**

Позиция индекса. Содержит координату x.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **R**

Переменная ресурса, доступная только для чтения.

## <a name="remarks"></a>Remarks

Этот метод всегда обращается к первому MIP уровню. Чтобы указать другие уровни MIP, используйте вместо него [**\[ \] \[ \] оператор MIP.**](sm5-object-texture1d-mipsoperatorindex.md)

Эта функция поддерживается для следующих типов шейдеров:



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Вычисления |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Texture1D](sm5-object-texture1d.md)
</dt> <dt>

[Модель шейдера 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




