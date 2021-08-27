---
title: 'Функция Texture2D:: operator'
description: 'Возвращает переменную ресурса, доступную только для чтения. | Функция Texture2D:: operator'
ms.assetid: 72ba3fc8-04c3-479a-b307-525020898bac
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
ms.openlocfilehash: 99323f1dcf212fc42c413a4be8231aa22acbd00cf3f40b408e3f9f5eca59f578
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095074"
---
# <a name="texture2doperator--function"></a>Функция Texture2D:: operator

Возвращает переменную ресурса, доступную только для чтения.

## <a name="syntax"></a>Синтаксис

``` syntax
R Operator[](
  in uint2 pos
);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*POS-терминал* \[ окне\]
</dt> <dd>

Тип: **uint2**

Позиция индекса. Содержит координаты (x, y).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **R**

Переменная ресурса, доступная только для чтения.

## <a name="remarks"></a>Remarks

Этот метод всегда обращается к первому MIP уровню. Чтобы указать другие уровни MIP, используйте вместо него метод [**MIP \[ \] \[ \] . operator**](sm5-object-texture2d-mipsoperatorindex.md) .

Примеры текстур можно использовать для интерполяции билинейной.

Эта функция поддерживается для следующих типов шейдеров:



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Службы вычислений |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Texture2D](sm5-object-texture2d.md)
</dt> <dt>

[Модель шейдера 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




