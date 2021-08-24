---
description: Задает типы режимов вывода для фильтрации.
ms.assetid: 4a03d0f0-dec5-4209-8c99-b58cc13064f5
title: Структура D3DDISPLAYMODEFILTER (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDISPLAYMODEFILTER
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: f59e2e095f7f0f1c6ee73fc940733e932efaef9af7ec05807ff1b38f35fe5189
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751064"
---
# <a name="d3ddisplaymodefilter-structure"></a>Структура D3DDISPLAYMODEFILTER

Задает типы режимов вывода для фильтрации.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct {
  UINT                Size;
  D3DFORMAT           Format;
  D3DSCANLINEORDERING ScanLineOrdering;
} D3DDISPLAYMODEFILTER;
```



## <a name="members"></a>Члены

<dl> <dt>

**Размер**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Размер этой структуры. Для этого параметра всегда должно быть задано значение sizeof (D3DDISPLAYMODEFILTER).

</dd> <dt>

**Формат**
</dt> <dd>

Тип: **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Формат режима экрана для фильтрации. См. [D3DFORMAT](d3dformat.md).

</dd> <dt>

**сканлинеордеринг**
</dt> <dd>

Тип: **[ **D3DSCANLINEORDERING**](./d3dscanlineordering.md)**

</dd> <dd>

Является ли порядок сканлине чередованием или прогрессивным. См. [**D3DSCANLINEORDERING**](./d3dscanlineordering.md).

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
