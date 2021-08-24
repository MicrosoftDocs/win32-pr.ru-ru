---
description: Описывает буфер вершин.
ms.assetid: 0ae8f976-d0ca-4d55-b6db-5be85fa3c799
title: Структура D3DVERTEXBUFFER_DESC (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVERTEXBUFFER_DESC
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 1f1809bbf9352b022d2acfb15b119db47b0feab6302020cdaf5b24746945aa05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119750584"
---
# <a name="d3dvertexbuffer_desc-structure"></a>\_Структура D3DVERTEXBUFFER DESC

Описывает буфер вершин.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct D3DVERTEXBUFFER_DESC {
  D3DFORMAT       Format;
  D3DRESOURCETYPE Type;
  DWORD           Usage;
  D3DPOOL         Pool;
  UINT            Size;
  DWORD           FVF;
} D3DVERTEXBUFFER_DESC, *LPD3DVERTEXBUFFER_DESC;
```



## <a name="members"></a>Члены

<dl> <dt>

**Формат**
</dt> <dd>

Тип: **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Член перечисляемого типа [D3DFORMAT](d3dformat.md) , описывающий формат поверхности данных буфера вершин.

</dd> <dt>

**Тип**
</dt> <dd>

Тип: **[ **D3DRESOURCETYPE**](./d3dresourcetype.md)**

</dd> <dd>

Член перечисляемого типа [**D3DRESOURCETYPE**](./d3dresourcetype.md) , определяющий этот ресурс в качестве буфера вершин.

</dd> <dt>

**Использование**
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Сочетание одного или нескольких флагов [**D3DUSAGE**](d3dusage.md) .

</dd> <dt>

**Пул.**
</dt> <dd>

Тип: **[ **D3DPOOL**](./d3dpool.md)**

</dd> <dd>

Член перечисляемого типа [**D3DPOOL**](./d3dpool.md) , указывающий класс памяти, выделенной для этого буфера вершин.

</dd> <dt>

**Размер**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Размер буфера вершин в байтах.

</dd> <dt>

**фвф**
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Сочетание [D3DFVF](d3dfvf.md) , описывающее формат вершины вершин в этом буфере.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetDesc**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-getdesc)
</dt> <dt>

[Буферы вершин (Direct3D 9)](vertex-buffers.md)
</dt> </dl>

 

 
