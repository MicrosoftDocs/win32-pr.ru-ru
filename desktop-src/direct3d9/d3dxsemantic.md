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
ms.openlocfilehash: 2534df72c246fdec361597a8e156f7f19b341ae35fcc04b3bdc6eb71c2903fef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119631024"
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

## <a name="remarks"></a>Remarks

Семантика необходима для построителя вершин и пиксельного шейдера, входных и выходных регистров.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3dx9shader. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры эффектов](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
