---
title: 'Функция Рвбитеаддрессбуффер:: Load4 (UINT)'
description: 'Возвращает четыре значения. | Функция Рвбитеаддрессбуффер:: Load4 (UINT)'
ms.assetid: b46cd119-75be-4c2d-82f9-5dcabd7e4400
keywords:
- Функция Load4 HLSL
topic_type:
- apiref
api_name:
- Load4
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bb2bdc5adf3b3d95c68871a14c9382891a59ad52
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986723"
---
# <a name="rwbyteaddressbufferload4uint-function"></a>Функция Рвбитеаддрессбуффер:: Load4 (UINT)

Возвращает четыре значения.

## <a name="syntax"></a>Синтаксис

``` syntax
uint4 Load4(
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

Тип: **uint4**

Четыре значения.

## <a name="remarks"></a>Примечания

Эта функция поддерживается для следующих типов шейдеров:



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Вычисления |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Методы Load4](rwbyteaddressbuffer-load4.md)
</dt> <dt>

[Модель шейдера 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




