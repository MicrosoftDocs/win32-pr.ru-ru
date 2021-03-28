---
title: 'Функция Битеаддрессбуффер:: Load (int)'
description: 'Возвращает одно значение. | Функция Битеаддрессбуффер:: Load (int)'
ms.assetid: a63f4099-2c3b-4d37-9135-b8c63df30824
keywords:
- Загрузить функцию HLSL
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e0de7d1a8ef8a7fe3173016fe07a433a930c3d59
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998059"
---
# <a name="byteaddressbufferloadint-function"></a>Функция Битеаддрессбуффер:: Load (int)

Возвращает одно значение.

## <a name="syntax"></a>Синтаксис

``` syntax
uint Load(
  in int address
);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*адрес* \[ окне\]
</dt> <dd>

Тип: **int**

Входной адрес в байтах, который должен быть кратным 4.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **uint**

Одно значение.

## <a name="remarks"></a>Примечания

Эта функция поддерживается для следующих типов шейдеров:



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Вычисления |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Методы Load](byteaddressbuffer-load.md)
</dt> <dt>

[Модель шейдера 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




