---
description: Инициализирует цвет, используя значения (a, y, u, v).
ms.assetid: 47b65aab-511a-44c1-ab94-973bc2da7e04
title: Макрос D3DCOLOR_AYUV (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_AYUV
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 5e1900bf0d400971786eb37dd5138154913562982e1a1e3221c8002ac51fbf2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118300318"
---
# <a name="d3dcolor_ayuv-macro"></a>\_Макрос D3DCOLOR айув

Инициализирует цвет, используя значения (a, y, u, v).

## <a name="syntax"></a>Синтаксис


```C++
D3DCOLOR D3DCOLOR_AYUV(
   int a,
   int y,
   int u,
   int v
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*конкретного* 
</dt> <dd>

Альфа-компонент цвета. Это значение должно находиться в диапазоне от 0 до 255.

</dd> <dt>

*y* 
</dt> <dd>

Компонент освещенности цвета. Это значение должно находиться в диапазоне от 0 до 255.

</dd> <dt>

*u* 
</dt> <dd>

Синяя яркость цвета. Это значение должно находиться в диапазоне от 0 до 255.

</dd> <dt>

*3,3* 
</dt> <dd>

Красная яркость цвета. Это значение должно находиться в диапазоне от 0 до 255.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение [D3DCOLOR](d3dcolor.md) , соответствующее указанным значениям ARGB.

## <a name="remarks"></a>Remarks

Цвет RGB можно уменьшить до 16 бит на пиксель путем преобразования в цветовые различия и цвета в следующих уравнениях:


```C++
y (luminance) = 0.299*red + 0.587*green + 0.114*blue
u = blue - luminance
v = red - luminance 
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Макросы](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[**D3DCOLOR \_ ARGB**](d3dcolor-argb.md)
</dt> <dt>

[**D3DCOLOR \_ ксюв**](d3dcolor-xyuv.md)
</dt> </dl>

 

 




