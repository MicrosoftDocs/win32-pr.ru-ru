---
title: 'Функция Битеаддрессбуффер:: Load3 (UINT)'
description: 'Возвращает три значения. | Функция Битеаддрессбуффер:: Load3 (UINT)'
ms.assetid: 79afeb36-e0e7-44a2-b252-8e3577f4c1a5
keywords:
- Функция Load3 HLSL
topic_type:
- apiref
api_name:
- Load3
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bd36958eb2c16d45e6228c9919cb22bb772c8861131c26710fff032276bce6e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118510014"
---
# <a name="byteaddressbufferload3uint-function"></a>Функция Битеаддрессбуффер:: Load3 (UINT)

Возвращает три значения.

## <a name="syntax"></a>Синтаксис

``` syntax
uint3 Load3(
  in uint address
);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*адрес* \[ окне\]
</dt> <dd>

Тип: **uint**

Входной адрес в байтах, который должен быть кратным 4.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **uint3**

Три значения.

## <a name="remarks"></a>Remarks

Эта функция поддерживается для следующих типов шейдеров:



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Вычисления |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>См. также

<dl> <dt>

[Методы Load3](byteaddressbuffer-load3.md)
</dt> <dt>

[Модель шейдера 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




