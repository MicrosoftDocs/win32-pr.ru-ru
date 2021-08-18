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
ms.openlocfilehash: 7545c27ccd5f82b3fed1f36a1cc2b0f9d92a9d901f5614ba3b6bec4068cb8abb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117724974"
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

## <a name="remarks"></a>Remarks

Эта функция поддерживается для следующих типов шейдеров:



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Службы вычислений |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Методы Load4](rwbyteaddressbuffer-load4.md)
</dt> <dt>

[Модель шейдера 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




