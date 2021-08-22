---
description: Задает исходный глиф и расположение в монохромной поверхности, в которую копируются глифы.
ms.assetid: eda6fc82-6a06-4a59-a3ab-9f7e5c5bb5a1
title: Структура D3DCOMPOSERECTDESTINATION (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOMPOSERECTDESTINATION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: e6d859cb0bfd47c9be21f37feef287b38cdce4cc64360dd312b2b52bb825a23e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123314"
---
# <a name="d3dcomposerectdestination-structure"></a>Структура D3DCOMPOSERECTDESTINATION

Задает исходный глиф и расположение в монохромной поверхности, в которую копируются глифы.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _D3DCOMPOSERECTDESTINATION {
  USHORT SrcRectIndex;
  USHORT Reserved;
  USHORT X;
  USHORT Y;
} D3DCOMPOSERECTDESTINATION;
```



## <a name="members"></a>Члены

<dl> <dt>

**сркректиндекс**
</dt> <dd>

Тип: **[ **UShort**](../winprog/windows-data-types.md)**

</dd> <dd>

Определенный индексом глиф из буфера вершин, содержащего структуры [**D3DCOMPOSERECTDESC**](d3dcomposerectdesc.md) .

</dd> <dt>

**Reserved**
</dt> <dd>

Тип: **[ **UShort**](../winprog/windows-data-types.md)**

</dd> <dd>

Зарезервировано для целей выравнивания.

</dd> <dt>

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

</dd> </dl>

## <a name="remarks"></a>Remarks

Эта структура используется в вызовах [**компосеректс**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-composerects) , чтобы указать, куда должны копироваться глифы расположения и какой именно глиф следует копировать. Буфер вершин (см. [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)), заполненный этими структурами, создается для хранения расположений глифов. Элементы USHORT используются для уменьшения объема памяти, насколько это возможно.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
