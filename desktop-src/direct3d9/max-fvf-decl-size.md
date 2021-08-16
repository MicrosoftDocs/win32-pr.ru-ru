---
description: Эта константа является максимальным числом деклараторов вершин для сетки.
ms.assetid: 234e99a2-1907-4065-b03b-fb9e8d6812ab
title: Перечисление MAX_FVF_DECL_SIZE (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MAX_FVF_DECL_SIZE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 52ac939cc77bbd87dbecffc07253f0fadc5cbbdaa48e07f938f163c453c21e14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118798800"
---
# <a name="max_fvf_decl_size-enumeration"></a>\_Перечисление Max фвф \_ DECL \_ size

Эта константа является максимальным числом деклараторов вершин для сетки.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum  { 
  MAX_FVF_DECL_SIZE  = MAXD3DDECLLENGTH + 1
} MAX_FVF_DECL_SIZE;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="MAX_FVF_DECL_SIZE"></span><span id="max_fvf_decl_size"></span>**МАКСИМАЛЬНЫЙ \_ \_ Размер DECL \_ фвф**
</dt> <dd>

Максимальное число элементов в объявлении вершины. Дополнительный (+ 1) — для [**D3DDECL \_ End**](d3ddecl-end.md).

</dd> </dl>

## <a name="remarks"></a>Remarks

MAXD3DDECLLENGTH определяется как максимум 64 (см. d3d9types. h). Это не включает элемент вершины маркера End.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Перечисления D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[**ID3DXBaseMesh**](id3dxbasemesh.md)
</dt> <dt>

[**Объявление о выходе**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexdeclaration9-getdeclaration)
</dt> <dt>

[**D3DXDeclaratorFromFVF**](d3dxdeclaratorfromfvf.md)
</dt> <dt>

[**ID3DXSkinInfo**](id3dxskininfo.md)
</dt> </dl>

 

 
