---
title: Функция ddx_fine
description: Выполняет частичное производные от высокой точности относительно координаты x пространства экрана. | Функция ddx_fine
ms.assetid: 41062d6f-2b7f-4594-a6de-da37ded5d444
keywords:
- Функция ddx_fine HLSL
topic_type:
- apiref
api_name:
- ddx_fine
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c1a579ba5899cf4d3ac3f25ef5a40337f6291977
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986756"
---
# <a name="ddx_fine-function"></a>\_функция DDX прекрасно

Выполняет частичное производные от высокой точности относительно координаты x пространства экрана.

## <a name="syntax"></a>Синтаксис

``` syntax
float ddx_fine(
  in float value
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
float2 ddx_fine(float2 value);
float3 ddx_fine(float3 value);
float4 ddx_fine(float4 value);
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

 

 




