---
description: Задает прямоугольник, используемый для заключения глифов в монохромную поверхность.
ms.assetid: ce5d492f-38d1-4e7b-a9c2-68c791c84d0c
title: Структура D3DCOMPOSERECTDESC (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOMPOSERECTDESC
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: cf9ad5f1c075f4dc52d68b894b37c7d0f0a7b310
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424346"
---
# <a name="d3dcomposerectdesc-structure"></a>Структура D3DCOMPOSERECTDESC

Задает прямоугольник, используемый для заключения глифов в монохромную поверхность.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _D3DCOMPOSERECTDESC {
  USHORT X;
  USHORT Y;
  USHORT Width;
  USHORT Height;
} D3DCOMPOSERECTDESC;
```



## <a name="members"></a>Члены

<dl> <dt>

**X**
</dt> <dd>

Тип: **[ **UShort**](../winprog/windows-data-types.md)**

</dd> <dd>

Левая координата начинается копирование в.

</dd> <dt>

**да**
</dt> <dd>

Тип: **[ **UShort**](../winprog/windows-data-types.md)**

</dd> <dd>

Верхняя координата, с которой начинается копирование.

</dd> <dt>

**Width**
</dt> <dd>

Тип: **[ **UShort**](../winprog/windows-data-types.md)**

</dd> <dd>

Число пикселей текстуры от левой координаты.

</dd> <dt>

**Height**
</dt> <dd>

Тип: **[ **UShort**](../winprog/windows-data-types.md)**

</dd> <dd>

Число пикселей текстуры от верхней координаты.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Эта структура используется в вызовах [**компосеректс**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-composerects) для заключения глифов в исходную область. Буфер вершин (см. [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)), заполненный этими структурами, создается для хранения расположений глифов. Элементы USHORT используются для уменьшения объема памяти, насколько это возможно.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
