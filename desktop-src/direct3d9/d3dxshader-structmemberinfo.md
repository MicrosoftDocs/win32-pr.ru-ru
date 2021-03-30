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
ms.openlocfilehash: 01782331459956c0878b46861db0d4f11e19c7dc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354623"
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

**Name**
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
| Header<br/> | <dl> <dt>D3dx9shader. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXSHADER \_ TYPEINFO**](d3dxshader-typeinfo.md)
</dt> </dl>

 

 
