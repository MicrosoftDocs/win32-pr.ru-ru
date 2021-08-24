---
description: Инициализирует цвет с заданными значениями красного, зеленого, синего и альфа-точечных чисел.
ms.assetid: 61825e33-4150-47cd-97f2-2144434a45e2
title: Макрос D3DCOLOR_COLORVALUE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_COLORVALUE
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: f4ee10003e0f4fdeae937d8ac786b4d389a91ec0326c2d6288d10af2a63e2286
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751234"
---
# <a name="d3dcolor_colorvalue-macro"></a>\_Макрос D3DCOLOR колорвалуе

Инициализирует цвет с заданными значениями красного, зеленого, синего и альфа-точечных чисел.

## <a name="syntax"></a>Синтаксис


```C++
D3DCOLOR D3DCOLOR_COLORVALUE(
   float r,
   float g,
   float b,
   float a
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*r* 
</dt> <dd>

Красный компонент цвета. Это значение должно быть значением с плавающей запятой в диапазоне от 0,0 до 1,0.

</dd> <dt>

*g* 
</dt> <dd>

Зеленый компонент цвета. Это значение должно быть значением с плавающей запятой в диапазоне от 0,0 до 1,0.

</dd> <dt>

*b* 
</dt> <dd>

Синий компонент цвета. Это значение должно быть значением с плавающей запятой в диапазоне от 0,0 до 1,0.

</dd> <dt>

*конкретного* 
</dt> <dd>

Альфа-компонент цвета. Это значение должно быть значением с плавающей запятой в диапазоне от 0,0 до 1,0.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение [**D3DCOLOR**](d3dcolor.md) , соответствующее указанным значениям RGBA.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Макросы](dx9-graphics-reference-d3d-macros.md)
</dt> </dl>

 

 




