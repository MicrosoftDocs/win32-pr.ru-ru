---
description: Задает свойства материала.
ms.assetid: 943e6f6d-8091-462f-8c44-e0c27686934a
title: Структура D3DMATERIAL9 (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DMATERIAL9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 640fd4ce0110f47aa20a04d0df595b0ae8bf5052c229825dd93e1066150c6306
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118527584"
---
# <a name="d3dmaterial9-structure"></a>Структура D3DMATERIAL9

Задает свойства материала.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct D3DMATERIAL9 {
  D3DCOLORVALUE Diffuse;
  D3DCOLORVALUE Ambient;
  D3DCOLORVALUE Specular;
  D3DCOLORVALUE Emissive;
  float         Power;
} D3DMATERIAL9, *LPD3DMATERIAL9;
```



## <a name="members"></a>Члены

<dl> <dt>

**Диффузное**
</dt> <dd>

Тип: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

Значение, указывающее рассеянный цвет материала. См. [**D3DCOLORVALUE**](d3dcolorvalue.md).

</dd> <dt>

**Окружающее**
</dt> <dd>

Тип: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

Значение, указывающее внешний цвет материала. См. [**D3DCOLORVALUE**](d3dcolorvalue.md).

</dd> <dt>

**Отражающее**
</dt> <dd>

Тип: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

Значение, указывающее отражающий цвет материала. См. [**D3DCOLORVALUE**](d3dcolorvalue.md).

</dd> <dt>

**Эмиссионное**
</dt> <dd>

Тип: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

Значение, указывающее цвет эмиссионный материала. См. [**D3DCOLORVALUE**](d3dcolorvalue.md).

</dd> <dt>

**Power**
</dt> <dd>

Тип: **float**

</dd> <dd>

Значение с плавающей запятой, определяющее четкость отраженных светов. Чем выше значение, тем четче выделение.

</dd> </dl>

## <a name="remarks"></a>Remarks

Чтобы отключить отраженные блики, присвойте параметру D3DRS \_ Спекуларенабле **значение false**, используя [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md). Это самый быстрый вариант, так как отраженные блики не будут вычисляться.

Дополнительные сведения об использовании механизма освещения для вычисления отраженного освещения см. в разделе [Зеркальное освещение (Direct3D 9)](specular-lighting.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**IDirect3DDevice9:: о.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getmaterial)
</dt> <dt>

[**IDirect3DDevice9:: Сетматериал**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial)
</dt> </dl>

 

 
