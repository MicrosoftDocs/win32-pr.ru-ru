---
title: countbits - функция
description: Подсчитывает количество битов (на компонент), заданных во входном целочисленном параметре.
ms.assetid: c4fafbc8-e21c-48cb-b433-8241a989ec85
keywords:
- Функция каунтбитс HLSL
topic_type:
- apiref
api_name:
- countbits
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5f3816152b91fd03348e64c7a36dd41e8b620bd5e5ef8f4463538c44ef974485
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118793972"
---
# <a name="countbits-function"></a>countbits - функция

Подсчитывает количество битов (на компонент), заданных во входном целочисленном параметре.

## <a name="syntax"></a>Синтаксис

``` syntax
uint countbits(
  in uint value
);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*значение* \[ окне\]
</dt> <dd>

Тип: **uint**

Входное значение.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **uint**

Число битов.

## <a name="remarks"></a>Remarks

Также доступны следующие перегруженные версии:

``` syntax
uint count_bits(uint value);
uint2 count_bits(uint2 value);
uint3 count_bits(uint3 value);
uint4 count_bits(uint4 value);
```

### <a name="minimum-shader-model"></a>Минимальная модель шейдера

Эта функция поддерживается в следующих моделях шейдеров.



| Модель шейдера                                                                | Поддерживается |
|-----------------------------------------------------------------------------|-----------|
| [Модели шейдера 5](d3d11-graphics-reference-sm5.md) и более поздних моделей шейдеров | Да       |



 

Эта функция поддерживается в следующих типах шейдеров:



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Службы вычислений |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Встроенные функции](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Модель шейдера 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




