---
title: 'Функция Битеаддрессбуффер:: Load2 (UINT)'
description: 'Возвращает два значения. | Функция Битеаддрессбуффер:: Load2 (UINT)'
ms.assetid: 696ce310-4d65-4382-97ec-046160197c67
keywords:
- Функция Load2 HLSL
topic_type:
- apiref
api_name:
- Load2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fac3b1cd0fffca1a68089c3c21bfd5d6aea5f270493319b044a0bbe290d88a5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119845734"
---
# <a name="byteaddressbufferload2uint-function"></a>Функция Битеаддрессбуффер:: Load2 (UINT)

Возвращает два значения.

## <a name="syntax"></a>Синтаксис

``` syntax
uint2 Load2(
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

Тип: **uint2**

Два значения.

## <a name="remarks"></a>Remarks

Эта функция поддерживается для следующих типов шейдеров:



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Вычисления |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Методы Load2](byteaddressbuffer-load2.md)
</dt> <dt>

[Модель шейдера 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




