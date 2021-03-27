---
title: Функция ddy_coarse
description: Выполняет частичное производные от низкой точности относительно координаты y экранного пространства.
ms.assetid: f6103cd3-f7ee-41c2-b3cf-9e72ca84b25e
keywords:
- Функция ddy_coarse HLSL
topic_type:
- apiref
api_name:
- ddy_coarse
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b6fef330e919a31e39306742bb03280454d47626
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104069134"
---
# <a name="ddy_coarse-function"></a>ДДИ \_ грубая функция

Выполняет частичное производные от низкой точности относительно координаты y экранного пространства.

## <a name="syntax"></a>Синтаксис

``` syntax
float ddy_coarse(
  in float value
);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*значение* \[ окне\]
</dt> <dd>

Тип: **float**

Входное значение.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **float**

Частичная точность, производная от *value*.

## <a name="remarks"></a>Примечания

Также доступны следующие перегруженные версии:

``` syntax
float2 ddy_coarse(float2 value);
float3 ddy_coarse(float3 value);
float4 ddy_coarse(float4 value);
```

### <a name="minimum-shader-model"></a>Минимальная модель шейдера

Эта функция поддерживается в следующих моделях шейдеров.



| Модель шейдера                                                                | Поддерживается |
|-----------------------------------------------------------------------------|-----------|
| [Модели шейдера 5](d3d11-graphics-reference-sm5.md) и более поздних моделей шейдеров | да       |



 

Эта функция поддерживается в следующих типах шейдеров:



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Вычисления |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     |         |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Встроенные функции](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Модель шейдера 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




