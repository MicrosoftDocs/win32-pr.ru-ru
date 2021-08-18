---
title: Функция асуинт
description: Повторно интерпретирует битовый шаблон 64-разрядного значения как два целых числа без знака (32).
ms.assetid: 29671661-4fec-46e5-9b6f-56fba8e1d756
keywords:
- Функция асуинт HLSL
topic_type:
- apiref
api_name:
- asuint
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 02f0df4d31ca978b8b58b50cd0c91710056aa9ac0f3cac1ae370a4edba6a9edf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119626594"
---
# <a name="asuint-function"></a>Функция асуинт

Повторно интерпретирует битовый шаблон 64-разрядного значения как два целых числа без знака (32).

## <a name="syntax"></a>Синтаксис

``` syntax
void asuint(
  in  double value,
  out uint lowbits,
  out uint highbits
);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*значение* \[ окне\]
</dt> <dd>

Тип: **Double**

Входное значение.

</dd> <dt>

*ловбитс* \[ заполняет\]
</dt> <dd>

Тип: **uint**

Младший 32-разрядный шаблон *значения*.

</dd> <dt>

*хигхбитс* \[ заполняет\]
</dt> <dd>

Тип: **uint**

Старший 32-разрядный шаблон *значения*.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

## <a name="remarks"></a>Remarks

Эта функция является альтернативной версией встроенной функции [**асуинт**](dx-graphics-hlsl-asuint.md) , которая была доступна в более ранних моделях шейдеров и была представлена для шейдера Model 5. Исходная функция (распознанная в компиляторе HLSL по другой сигнатуре) остается доступной для модели шейдера 5.

### <a name="minimum-shader-model"></a>Минимальная модель шейдера

Эта функция поддерживается в следующих моделях шейдеров.



| Модель шейдера                                                                | Поддерживается |
|-----------------------------------------------------------------------------|-----------|
| [Модели шейдера 5](d3d11-graphics-reference-sm5.md) и более поздних моделей шейдеров | Да       |



 

Эта функция поддерживается в следующих типах шейдеров:



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Вычисления |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Встроенные функции](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[**асуинт (DirectX HLSL)**](dx-graphics-hlsl-asuint.md)
</dt> <dt>

[Модель шейдера 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




