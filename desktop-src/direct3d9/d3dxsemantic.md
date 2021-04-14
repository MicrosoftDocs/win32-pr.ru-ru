---
description: Семантика сопоставляет параметр с регистрами вершин или шейдеров пикселей. Они также могут быть необязательными описательными строками, присоединенными к параметрам, не относящимся к регистру.
ms.assetid: 547a6ff3-be24-4299-9119-6719ad09b4ef
title: Структура D3DXSEMANTIC (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSEMANTIC
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 08a30ac4d669beb5b93f2823219cb167d9e8d67f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424373"
---
# <a name="d3dxsemantic-structure"></a>Структура D3DXSEMANTIC

Семантика сопоставляет параметр с регистрами вершин или шейдеров пикселей. Они также могут быть необязательными описательными строками, присоединенными к параметрам, не относящимся к регистру.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct D3DXSEMANTIC {
  UINT Usage;
  UINT UsageIndex;
} D3DXSEMANTIC, *LPD3DXSEMANTIC;
```



## <a name="members"></a>Члены

<dl> <dt>

**Использование**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Параметры, определяющие, как используются ресурсы. См. [**D3DDECLUSAGE**](./d3ddeclusage.md).

</dd> <dt>

**усажеиндекс**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Параметры, изменяющие способ интерпретации использования. Индекс использования и использования составляют объявление вершины. См. [Описание вершины (Direct3D 9)](vertex-declaration.md).

</dd> </dl>

## <a name="remarks"></a>Комментарии

Семантика необходима для построителя вершин и пиксельного шейдера, входных и выходных регистров.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9shader. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры эффектов](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
