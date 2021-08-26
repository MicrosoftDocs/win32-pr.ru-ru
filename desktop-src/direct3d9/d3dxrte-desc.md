---
description: Описывает экранный целевой объект отрисовки, используемый экземпляром ID3DXRenderToEnvMap.
ms.assetid: 805df4da-e882-4d54-bf2c-49cfcbc59ac6
title: Структура D3DXRTE_DESC (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXRTE_DESC
api_type:
- HeaderDef
api_location:
- d3dx9core.h
ms.openlocfilehash: 91efe4dff2b392310ed2fd6bdc30db12c883c5d08e6b2cf110c2cb29d73c54ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120027284"
---
# <a name="d3dxrte_desc-structure"></a>\_Структура D3DXRTE DESC

Описывает экранный целевой объект отрисовки, используемый экземпляром [**ID3DXRenderToEnvMap**](id3dxrendertoenvmap.md).

## <a name="syntax"></a>Синтаксис


```C++
typedef struct D3DXRTE_DESC {
  UINT      Size;
  UINT      MipLevels;
  D3DFORMAT Format;
  BOOL      DepthStencil;
  D3DFORMAT DepthStencilFormat;
} D3DXRTE_DESC, *LPD3DXRTE_DESC;
```



## <a name="members"></a>Члены

<dl> <dt>

**Размер**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Ширина и высота в пикселях.

</dd> <dt>

**миплевелс**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Максимальный уровень детализации (Лод).

</dd> <dt>

**Формат**
</dt> <dd>

Тип: **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Формат цветового буфера.

</dd> <dt>

**депсстенЦил**
</dt> <dd>

Тип: **[ **bool** .](../winprog/windows-data-types.md)**

</dd> <dd>

Указывает, требуется ли z-буфер.

</dd> <dt>

**депсстенЦилформат**
</dt> <dd>

Тип: **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Формат буфера глубины.

</dd> </dl>

## <a name="remarks"></a>Remarks

Этот метод используется для возврата параметров создания, используемых при создании объекта [**ID3DXRenderToEnvMap**](id3dxrendertoenvmap.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3dx9core. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
