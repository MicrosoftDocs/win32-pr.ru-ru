---
title: 'Функция RWTexture3D:: operator'
description: Возвращает переменную ресурса RWTexture3D.
ms.assetid: 0b4ea895-ac34-49e5-80e6-74229c33bfe9
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
ms.openlocfilehash: 8db7073ef20976ecb6c39839d5639a1f0fcfe1fad765c2cf9b0ecdf086622b9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118509140"
---
# <a name="rwtexture3doperator--function"></a>Функция RWTexture3D:: operator

Возвращает переменную ресурса [**RWTexture3D**](sm5-object-rwtexture3d.md).

## <a name="syntax"></a>Синтаксис

``` syntax
R Operator[](
  in uint3 pos
);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*POS-терминал* \[ окне\]
</dt> <dd>

Тип: **uint3**

Позиция индекса. Содержит координаты (x, y, z).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **R**

Переменная ресурса.

## <a name="remarks"></a>Remarks

Эта функция поддерживается для следующих типов шейдеров:



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Службы вычислений |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[RWTexture3D](sm5-object-rwtexture3d.md)
</dt> <dt>

[Модель шейдера 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




