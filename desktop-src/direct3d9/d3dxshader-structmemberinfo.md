---
description: Вспомогательная структура, содержащая сведения о структуре элементов.
ms.assetid: 2fbe5e97-047e-48bf-9413-dd297632288a
title: Структура D3DXSHADER_STRUCTMEMBERINFO (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHADER_STRUCTMEMBERINFO
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 6f41c3d1911a046165d929bee50ef4e0b5691cebee9d90007bc367636e343731
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118524217"
---
# <a name="d3dxshader_structmemberinfo-structure"></a>\_Структура СТРУКТМЕМБЕРИНФО D3DXSHADER

Вспомогательная структура, содержащая сведения о структуре элементов.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct D3DXSHADER_STRUCTMEMBERINFO {
  DWORD Name;
  DWORD TypeInfo;
} D3DXSHADER_STRUCTMEMBERINFO, *LPD3DXSHADER_STRUCTMEMBERINFO;
```



## <a name="members"></a>Члены

<dl> <dt>

**Имя**
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Смещение от начала этой структуры (в байтах) к строке, содержащей имя члена структуры.

</dd> <dt>

**TypeInfo**
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Смещение от начала этой структуры (в байтах) к строке, содержащей сведения о типе. См. [**D3DXSHADER \_ TYPEINFO**](d3dxshader-typeinfo.md).

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3dx9shader. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXSHADER \_ TYPEINFO**](d3dxshader-typeinfo.md)
</dt> </dl>

 

 
