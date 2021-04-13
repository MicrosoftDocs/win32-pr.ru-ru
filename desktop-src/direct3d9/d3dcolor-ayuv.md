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
ms.openlocfilehash: 62a34e94fbdc6c47ed034a46bdae6e9b32a7c95d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105647832"
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

## <a name="remarks"></a>Комментарии

Цвет RGB можно уменьшить до 16 бит на пиксель путем преобразования в цветовые различия и цвета в следующих уравнениях:


```C++
y (luminance) = 0.299*red + 0.587*green + 0.114*blue
u = blue - luminance
v = red - luminance 
```



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

[**D3DCOLOR \_ ксюв**](d3dcolor-xyuv.md)
</dt> </dl>

 

 




