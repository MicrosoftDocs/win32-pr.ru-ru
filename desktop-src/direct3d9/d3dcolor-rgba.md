---
description: Инициализирует цвет с заданными значениями красного, зеленого, синего и альфа-канала.
ms.assetid: 87d322f1-4a26-42fd-a1c3-7be220cecf0f
title: Макрос D3DCOLOR_RGBA (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_RGBA
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: c5047f29a9afbe5bb18db213f90e559b5e11d273
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105647831"
---
# <a name="d3dcolor_rgba-macro"></a>\_Макрос D3DCOLOR RGBA

Инициализирует цвет с заданными значениями красного, зеленого, синего и альфа-канала.

## <a name="syntax"></a>Синтаксис


```C++
D3DCOLOR D3DCOLOR_RGBA(
   int r,
   int g,
   int b,
   int a
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

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

</dd> <dt>

*конкретного* 
</dt> <dd>

Альфа-компонент цвета. Это значение должно находиться в диапазоне от 0 до 255.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение [**D3DCOLOR**](d3dcolor.md) , соответствующее указанным значениям RGBA.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Макросы](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[**D3DCOLOR \_ ARGB**](d3dcolor-argb.md)
</dt> <dt>

[**D3DCOLOR \_ ксргб**](d3dcolor-xrgb.md)
</dt> </dl>

 

 




