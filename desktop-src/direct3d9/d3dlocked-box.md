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
ms.openlocfilehash: 41fc5b0fd81405f9f12f65fca4fae53239110bfa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273832"
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

## <a name="remarks"></a>Комментарии

Тома могут быть визуально обрабатываются в виде срезов 2D-поверхностей толщины x высота, разбитого на оси x высота x глубина. Дополнительные сведения см. в статье [ресурсы текстуры для томов (Direct3D 9)](volume-texture-resources.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**IDirect3DVolume9:: защищенное хранилище**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-lockbox)
</dt> <dt>

[**IDirect3DVolumeTexture9:: защищенное хранилище**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-lockbox)
</dt> </dl>

 

 
