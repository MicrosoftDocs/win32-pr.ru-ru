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
ms.openlocfilehash: 3d5bb780a5999d8931335da1e9f49ad8af88dc12
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103820964"
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
| Header<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Макросы](dx9-graphics-reference-d3d-macros.md)
</dt> </dl>

 

 




