---
description: Инициализирует цвет с помощью значений (y, u, v).
ms.assetid: e3091eaf-8639-428c-8dd8-6feeb7d7776e
title: Макрос D3DCOLOR_XYUV (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_XYUV
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 12d539e44528c5e54a54209763e4cbe262cd16f7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103914704"
---
# <a name="d3dcolor_xyuv-macro"></a>\_Макрос D3DCOLOR ксюв

Инициализирует цвет с помощью значений (y, u, v).

## <a name="syntax"></a>Синтаксис


```C++
D3DCOLOR D3DCOLOR_XYUV(
   int y,
   int u,
   int v
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

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

Возвращает значение [**D3DCOLOR**](d3dcolor.md) , соответствующее указанным значениям (y, u, v).

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

[**D3DCOLOR \_ айув**](d3dcolor-ayuv.md)
</dt> </dl>

 

 




