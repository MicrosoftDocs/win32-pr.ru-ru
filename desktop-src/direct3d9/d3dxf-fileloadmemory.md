---
description: Определяет данные памяти.
ms.assetid: 0ec0597f-d83a-4c1e-b993-30f0bbd64e6b
title: Структура D3DXF_FILELOADMEMORY (D3dx9xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXF_FILELOADMEMORY
api_type:
- HeaderDef
api_location:
- d3dx9xof.h
ms.openlocfilehash: a7ad988d9906101db57af6f8f5042766c3e32ccc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000364"
---
# <a name="d3dxf_fileloadmemory-structure"></a>\_Структура ФИЛЕЛОАДМЕМОРИ D3DXF

Определяет данные памяти.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct D3DXF_FILELOADMEMORY {
  LPCVOID lpMemory;
  SIZE_T  dSize;
} D3DXF_FILELOADMEMORY, *LPD3DXF_FILELOADMEMORY;
```



## <a name="members"></a>Члены

<dl> <dt>

**лпмемори**
</dt> <dd>

Тип: **[ **лпквоид**](../winprog/windows-data-types.md)**

</dd> <dd>

Указатель на блок памяти для загрузки.

</dd> <dt>

**дсизе**
</dt> <dd>

Type: **[ **size \_ T**](../winprog/windows-data-types.md)**

</dd> <dd>

Размер блока памяти, который должен быть загружен, в байтах.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Эта структура определяет данные, загружаемые из памяти, когда приложение использует метод [**креатинумобжект**](id3dxfile--createenumobject.md) и ЗАДАЕТ \_ флаг D3DXF филелоад \_ фроммемори.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9xof. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры файлов D3DX X](dx9-graphics-reference-d3dx-x-file-structures.md)
</dt> </dl>

 

 
