---
description: '\_Структура КОНСТАНТИНФО D3DXSHADER'
ms.assetid: 0c42cea7-559e-4475-b66a-e932a9cb42de
title: Структура D3DXSHADER_CONSTANTINFO (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHADER_CONSTANTINFO
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 34a9238ac7ab401a25874d65390ccfacb4dba68a9ccc4438500a1171e25e5e13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119122834"
---
# <a name="d3dxshader_constantinfo-structure"></a>\_Структура КОНСТАНТИНФО D3DXSHADER

## <a name="syntax"></a>Синтаксис


```C++
typedef struct D3DXSHADER_CONSTANTINFO {
  DWORD Name;
  WORD  RegisterSet;
  WORD  RegisterIndex;
  WORD  RegisterCount;
  WORD  Reserved;
  DWORD TypeInfo;
  DWORD DefaultValue;
} D3DXSHADER_CONSTANTINFO, *LPD3DXSHADER_CONSTANTINFO;
```



## <a name="members"></a>Члены

<dl> <dt>

**Имя**
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Смещение от начала этой структуры (в байтах) к строке, содержащей сведения о константе.

</dd> <dt>

**Register**
</dt> <dd>

Тип: **[ **слово**](../winprog/windows-data-types.md)**

</dd> <dd>

Набор регистров. См. раздел [**D3DXREGISTER \_ Set**](./d3dxregister-set.md).

</dd> <dt>

**регистериндекс**
</dt> <dd>

Тип: **[ **слово**](../winprog/windows-data-types.md)**

</dd> <dd>

Индекс регистра.

</dd> <dt>

**регистеркаунт**
</dt> <dd>

Тип: **[ **слово**](../winprog/windows-data-types.md)**

</dd> <dd>

Количество регистров.

</dd> <dt>

**Reserved**
</dt> <dd>

Тип: **[ **слово**](../winprog/windows-data-types.md)**

</dd> <dd>

Зарезервировано.

</dd> <dt>

**TypeInfo**
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Смещение от начала этой структуры (в байтах) к строке, содержащей сведения о [**D3DXSHADER \_ TYPEINFO**](d3dxshader-typeinfo.md) .

</dd> <dt>

**Максимально**
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Смещение от начала этой структуры (в байтах) к строке, содержащей значение по умолчанию.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3dx9shader. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
