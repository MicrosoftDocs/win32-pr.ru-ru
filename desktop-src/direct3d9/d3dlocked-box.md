---
description: Описывает заблокированный прямоугольник (том).
ms.assetid: b371fb5e-2d65-453c-acd7-214de8aaa78a
title: Структура D3DLOCKED_BOX (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DLOCKED_BOX
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: deb83c71eb9fe9fa5c69667e6dc48187144fa5c18e1daf084e4a04c1fd213744
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119750994"
---
# <a name="d3dlocked_box-structure"></a>\_Структура Box D3DLOCKED

Описывает заблокированный прямоугольник (том).

## <a name="syntax"></a>Синтаксис


```C++
typedef struct D3DLOCKED_BOX {
  int  RowPitch;
  int  SlicePitch;
  void *pBits;
} D3DLOCKED_BOX, *LPD3DLOCKED_BOX;
```



## <a name="members"></a>Члены

<dl> <dt>

**ровпитч**
</dt> <dd>

Тип: **[ **int**](../winprog/windows-data-types.md)**

</dd> <dd>

Смещение в байтах от левого края одной строки к левому краю следующей строки.

</dd> <dt>

**слицепитч**
</dt> <dd>

Тип: **[ **int**](../winprog/windows-data-types.md)**

</dd> <dd>

Смещение в байтах от верхнего левого угла одного среза к левому верхнему краю следующего самого глубокого среза.

</dd> <dt>

**пбитс**
</dt> <dd>

Тип: **void \***

</dd> <dd>

Указатель на начало поля "том". Если в вызове защищенного хранилища была предоставлена [**D3DBOX**](d3dbox.md) , пбитс будет соответствующим образом смещен с начала тома.

</dd> </dl>

## <a name="remarks"></a>Remarks

Тома могут быть визуально обрабатываются в виде срезов 2D-поверхностей толщины x высота, разбитого на оси x высота x глубина. Дополнительные сведения см. в статье [ресурсы текстуры для томов (Direct3D 9)](volume-texture-resources.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Структуры Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**IDirect3DVolume9:: защищенное хранилище**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-lockbox)
</dt> <dt>

[**IDirect3DVolumeTexture9:: защищенное хранилище**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-lockbox)
</dt> </dl>

 

 
