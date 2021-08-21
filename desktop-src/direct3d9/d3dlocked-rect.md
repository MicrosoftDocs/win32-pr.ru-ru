---
description: Описывает Заблокированную прямоугольную область.
ms.assetid: ee5d2ea6-bf98-4b09-bc67-b808ffcb23c6
title: Структура D3DLOCKED_RECT (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DLOCKED_RECT
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: b419483329e5461de5bc98b3a37b556e37138a055932b1d6c80d3a19b13ae516
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988904"
---
# <a name="d3dlocked_rect-structure"></a>\_Структура Rect D3DLOCKED

Описывает Заблокированную прямоугольную область.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct D3DLOCKED_RECT {
  INT  Pitch;
  void *pBits;
} D3DLOCKED_RECT, *LPD3DLOCKED_RECT;
```



## <a name="members"></a>Члены

<dl> <dt>

**Высота тона**
</dt> <dd>

Тип: **[ **int**](../winprog/windows-data-types.md)**

</dd> <dd>

Число байтов в одной строке поверхности.

</dd> <dt>

**пбитс**
</dt> <dd>

Тип: **void \***

</dd> <dd>

Указатель на заблокированные биты. Если для вызова [**локкрект**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-lockrect) был предоставлен [**Rect**](/previous-versions//dd162897(v=vs.85)) , пбитс будет соответствующим образом смещен с начала поверхности.

</dd> </dl>

## <a name="remarks"></a>Remarks

Высота форматов Дкстн отличается от того, что было возвращено в DirectX 7. Теперь он ссылается на число байтов в строке блоков. Например, если ширина 16, то у вас будет шаг 4 блока (4 \* 8 для DXT1, 4 \* 16 для DXT2-5).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**IDirect3DCubeTexture9:: Локкрект**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[**IDirect3DSurface9:: Локкрект**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-lockrect)
</dt> <dt>

[**IDirect3DTexture9:: Локкрект**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-lockrect)
</dt> </dl>

 

 
