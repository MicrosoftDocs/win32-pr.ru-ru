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
ms.openlocfilehash: 398b5a6dba995a11dcf4ce8a78fecee9bb185ce98ec285453bdd52c1180a4eb3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067724"
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

## <a name="remarks"></a>Remarks

Эта функция поддерживается для следующих типов шейдеров:



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Вычисления |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>См. также

<dl> <dt>

[битеаддрессбуффер](sm5-object-byteaddressbuffer.md)
</dt> <dt>

[Модель шейдера 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




