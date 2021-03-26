---
title: firstbithigh - функция
description: Возвращает расположение первого набора битов, начиная с самого высокого бита и заканчивая его обработкой вниз, на каждый компонент.
ms.assetid: 0fa89a9e-1706-44f7-8dd3-c37af5c11ddc
keywords:
- Функция фирстбисигх HLSL
topic_type:
- apiref
api_name:
- firstbithigh
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4da4956aa3a12d064566a3767423f42039b01355
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413148"
---
# <a name="firstbithigh-function"></a>firstbithigh - функция

Возвращает расположение первого набора битов, начиная с самого высокого бита и заканчивая его обработкой вниз, на каждый компонент.

## <a name="syntax"></a>Синтаксис

``` syntax
int firstbithigh(
  in int value
);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*значение* \[ окне\]
</dt> <dd>

Тип: **[ **int**](/windows/desktop/WinProg/windows-data-types)**

Входное значение.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **int**](/windows/desktop/WinProg/windows-data-types)**

Расположение первого набора бит.

## <a name="remarks"></a>Примечания

Для целого числа со знаком Первый значащий бит равен нулю для отрицательного числа.

Также доступны следующие перегруженные версии:

``` syntax
int2 firstbithigh(int2 value);
int3 firstbithigh(int3 value);
int4 firstbithigh(int4 value);
uint firstbithigh(uint value);
uint2 firstbithigh(uint2 value);
uint3 firstbithigh(uint3 value);
uint4 firstbithigh(uint4 value);
```

### <a name="minimum-shader-model"></a>Минимальная модель шейдера

Эта функция поддерживается в следующих моделях шейдеров.



| Модель шейдера                                                                | Поддерживается |
|-----------------------------------------------------------------------------|-----------|
| [Модели шейдера 5](d3d11-graphics-reference-sm5.md) и более поздних моделей шейдеров | да       |



 

Эта функция поддерживается в следующих типах шейдеров:



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Вычисления |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Встроенные функции](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Модель шейдера 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 