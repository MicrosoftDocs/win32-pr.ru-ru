---
description: Описывает том.
ms.assetid: c0224f4e-3d32-4bdd-b56c-4e8aa291bb27
title: Структура D3DVOLUME_DESC (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVOLUME_DESC
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: b736333cefcfc8a3307ff7a0cecd53cd96bc0af2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355190"
---
# <a name="d3dvolume_desc-structure"></a>\_Структура D3DVOLUME DESC

Описывает том.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct D3DVOLUME_DESC {
  D3DFORMAT       Format;
  D3DRESOURCETYPE Type;
  DWORD           Usage;
  D3DPOOL         Pool;
  UINT            Width;
  UINT            Height;
  UINT            Depth;
} D3DVOLUME_DESC, *LPD3DVOLUME_DESC;
```



## <a name="members"></a>Члены

<dl> <dt>

**Формат**
</dt> <dd>

Тип: **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Член перечисляемого типа [D3DFORMAT](d3dformat.md) , описывающий формат поверхности тома.

</dd> <dt>

**Тип**
</dt> <dd>

Тип: **[ **D3DRESOURCETYPE**](./d3dresourcetype.md)**

</dd> <dd>

Член перечисляемого типа [**D3DRESOURCETYPE**](./d3dresourcetype.md) , который определяет этот ресурс как том.

</dd> <dt>

**Использование**
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

В настоящее время не используется. Всегда возвращает значение 0.

</dd> <dt>

**Пул.**
</dt> <dd>

Тип: **[ **D3DPOOL**](./d3dpool.md)**

</dd> <dd>

Член перечисляемого типа [**D3DPOOL**](./d3dpool.md) , указывающий класс памяти, выделенной для этого тома.

</dd> <dt>

**Width**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Ширина тома (в пикселях).

</dd> <dt>

**Height**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Высота тома (в пикселях).

</dd> <dt>

**Depth**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Глубина тома в пикселях.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetDesc**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-getdesc)
</dt> <dt>

[**жетлевелдеск**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-getleveldesc)
</dt> </dl>

 

 
