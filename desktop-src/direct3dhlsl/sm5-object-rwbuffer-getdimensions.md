---
title: 'Функция Рвбуффер:: Dimension'
description: 'Возвращает длину буфера. | Функция Рвбуффер:: Dimension'
ms.assetid: 600147cb-9513-4b74-a873-1ed22b31cdf7
keywords:
- Функция Dimension HLSL
topic_type:
- apiref
api_name:
- GetDimensions
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 586f266fea0dbc035e8ff3a61e39cb18a7102d792ee05c44345a1b702cc1b574
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118244"
---
# <a name="rwbuffergetdimensions-function"></a>Функция Рвбуффер:: Dimension

Возвращает длину буфера.

## <a name="syntax"></a>Синтаксис

``` syntax
void GetDimensions(
  out uint dim
);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*затемнение* \[\]
</dt> <dd>

Тип: **uint**

Длина буфера в байтах.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Ничего

## <a name="remarks"></a>Remarks

Эта функция поддерживается для следующих типов шейдеров:



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Вычисления |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>См. также

<dl> <dt>

[рвбуффер](sm5-object-rwbuffer.md)
</dt> <dt>

[Модель шейдера 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




