---
title: 'Функция Рвбитеаддрессбуффер:: Dimension'
description: 'Возвращает длину буфера. | Функция Рвбитеаддрессбуффер:: Dimension'
ms.assetid: 7d78aa0d-75b8-43d5-85d9-0a6fb04ae64f
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
ms.openlocfilehash: 2271f563251cfdb9c6f2a2174c91dc8c271c7354a2b10b9b2e7e55cb4af09d0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117725149"
---
# <a name="rwbyteaddressbuffergetdimensions-function"></a>Функция Рвбитеаддрессбуффер:: Dimension

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

Эта функция не возвращает значение.

## <a name="remarks"></a>Remarks

Эта функция поддерживается для следующих типов шейдеров:



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Службы вычислений |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[рвбитеаддрессбуффер](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[Модель шейдера 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




