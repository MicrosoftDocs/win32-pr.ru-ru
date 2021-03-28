---
title: 'Функция Битеаддрессбуффер:: Dimension'
description: 'Возвращает длину буфера. | Функция Битеаддрессбуффер:: Dimension'
ms.assetid: 32099118-8d8a-440e-96ba-2580d905f068
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
ms.openlocfilehash: 1cbb705789e444a6fa54aeb87190912996f65621
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998014"
---
# <a name="byteaddressbuffergetdimensions-function"></a>Функция Битеаддрессбуффер:: Dimension

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

## <a name="remarks"></a>Примечания

Эта функция поддерживается для следующих типов шейдеров:



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Вычисления |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[битеаддрессбуффер](sm5-object-byteaddressbuffer.md)
</dt> <dt>

[Модель шейдера 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




