---
description: Определяет грани кубической карты.
ms.assetid: 6d18b410-6f22-4202-86ae-6b3ef85e6f69
title: Перечисление D3DCUBEMAP_FACES (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCUBEMAP_FACES
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: cd7222fcb561f23f742bfe689eb8323f2f5b70ed67d5c23c7dee4943e2642167
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989044"
---
# <a name="d3dcubemap_faces-enumeration"></a>\_Перечисление D3DCUBEMAP лиц

Определяет грани кубической карты.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum D3DCUBEMAP_FACES { 
  D3DCUBEMAP_FACE_POSITIVE_X   = 0,
  D3DCUBEMAP_FACE_NEGATIVE_X   = 1,
  D3DCUBEMAP_FACE_POSITIVE_Y   = 2,
  D3DCUBEMAP_FACE_NEGATIVE_Y   = 3,
  D3DCUBEMAP_FACE_POSITIVE_Z   = 4,
  D3DCUBEMAP_FACE_NEGATIVE_Z   = 5,
  D3DCUBEMAP_FACE_FORCE_DWORD  = 0xffffffff
} D3DCUBEMAP_FACES, *LPD3DCUBEMAP_FACES;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="D3DCUBEMAP_FACE_POSITIVE_X"></span><span id="d3dcubemap_face_positive_x"></span>**D3DCUBEMAP \_ лицо \_ плюс \_ X**
</dt> <dd>

Положительный x-face кубической карты.

</dd> <dt>

<span id="D3DCUBEMAP_FACE_NEGATIVE_X"></span><span id="d3dcubemap_face_negative_x"></span>**D3DCUBEMAP \_ лицевой стороны \_ минус \_ X**
</dt> <dd>

Отрицательное значение x-face кубической карты.

</dd> <dt>

<span id="D3DCUBEMAP_FACE_POSITIVE_Y"></span><span id="d3dcubemap_face_positive_y"></span>**D3DCUBEMAP \_ лицо \_ плюс \_ Y**
</dt> <dd>

Положительный y-лицо кубической карты.

</dd> <dt>

<span id="D3DCUBEMAP_FACE_NEGATIVE_Y"></span><span id="d3dcubemap_face_negative_y"></span>**D3DCUBEMAP \_ лицевой стороны, \_ отрицательный \_ Y**
</dt> <dd>

Отрицательный y-Face кубической карты.

</dd> <dt>

<span id="D3DCUBEMAP_FACE_POSITIVE_Z"></span><span id="d3dcubemap_face_positive_z"></span>**D3DCUBEMAP \_ лицо \_ плюс \_ Z**
</dt> <dd>

Положительное z-лицо кубической карты.

</dd> <dt>

<span id="D3DCUBEMAP_FACE_NEGATIVE_Z"></span><span id="d3dcubemap_face_negative_z"></span>**D3DCUBEMAP \_ лицевой стороны \_ минус \_ Z**
</dt> <dd>

Отрицательное z-лицо кубической карты.

</dd> <dt>

<span id="D3DCUBEMAP_FACE_FORCE_DWORD"></span><span id="d3dcubemap_face_force_dword"></span>**D3DCUBEMAP «Force», \_ \_ \_ параметр DWORD**
</dt> <dd>

Заставляет это перечисление компилироваться до 32 бит в размере. Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит. Это значение не используется.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Перечисления Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**IDirect3DCubeTexture9:: Адддиртирект**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-adddirtyrect)
</dt> <dt>

[**IDirect3DCubeTexture9:: Жеткубемапсурфаце**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface)
</dt> <dt>

[**IDirect3DCubeTexture9:: Локкрект**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[**IDirect3DCubeTexture9:: Унлоккрект**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-unlockrect)
</dt> </dl>

 

 
