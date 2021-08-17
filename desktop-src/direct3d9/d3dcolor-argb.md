---
description: Инициализирует цвет с заданными значениями альфа, красного, зеленого и синего.
ms.assetid: e862ba1b-fdcf-4058-8835-e58b4fc5e21a
title: Макрос D3DCOLOR_ARGB (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_ARGB
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 8b65ae82673e98d666754ae42348cb62b3c336a1e642a5f78607924dc58313dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118805434"
---
# <a name="d3dcolor_argb-macro"></a>D3DCOLOR \_ ARGB, макрос

Инициализирует цвет с заданными значениями альфа, красного, зеленого и синего.

## <a name="syntax"></a>Синтаксис


```C++
D3DCOLOR D3DCOLOR_ARGB(
   int a,
   int r,
   int g,
   int b
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*конкретного* 
</dt> <dd>

Альфа-компонент цвета. Это значение должно находиться в диапазоне от 0 до 255.

</dd> <dt>

*r* 
</dt> <dd>

Красный компонент цвета. Это значение должно находиться в диапазоне от 0 до 255.

</dd> <dt>

*g* 
</dt> <dd>

Зеленый компонент цвета. Это значение должно находиться в диапазоне от 0 до 255.

</dd> <dt>

*b* 
</dt> <dd>

Синий компонент цвета. Это значение должно находиться в диапазоне от 0 до 255.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение [D3DCOLOR](d3dcolor.md) , соответствующее указанным значениям ARGB.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Макросы](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[**D3DCOLOR \_ RGBA**](d3dcolor-rgba.md)
</dt> <dt>

[**D3DCOLOR \_ ксргб**](d3dcolor-xrgb.md)
</dt> </dl>

 

 




