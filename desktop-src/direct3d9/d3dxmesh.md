---
description: D3DXMESH enumeration — флаги, используемые для указания параметров создания сетки.
ms.assetid: c94e19ab-8024-4a28-9d1a-6d57707c3a52
title: Перечисление D3DXMESH (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMESH
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: a312c2618960691184182039afe38acc8947eb6a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098102"
---
# <a name="d3dxmesh-enumeration"></a>Перечисление D3DXMESH

Флаги, используемые для указания параметров создания сетки.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum D3DXMESH { 
  D3DXMESH_32BIT                  = 0x001,
  D3DXMESH_DONOTCLIP              = 0x002,
  D3DXMESH_POINTS                 = 0x004,
  D3DXMESH_RTPATCHES              = 0x008,
  D3DXMESH_NPATCHES               = 0x4000,
  D3DXMESH_VB_SYSTEMMEM           = 0x010,
  D3DXMESH_VB_MANAGED             = 0x020,
  D3DXMESH_VB_WRITEONLY           = 0x040,
  D3DXMESH_VB_DYNAMIC             = 0x080,
  D3DXMESH_VB_SOFTWAREPROCESSING  = 0x8000,
  D3DXMESH_IB_SYSTEMMEM           = 0x100,
  D3DXMESH_IB_MANAGED             = 0x200,
  D3DXMESH_IB_WRITEONLY           = 0x400,
  D3DXMESH_IB_DYNAMIC             = 0x800,
  D3DXMESH_IB_SOFTWAREPROCESSING  = 0x10000,
  D3DXMESH_VB_SHARE               = 0x1000,
  D3DXMESH_USEHWONLY              = 0x2000,
  D3DXMESH_SYSTEMMEM              = 0x110,
  D3DXMESH_MANAGED                = 0x220,
  D3DXMESH_WRITEONLY              = 0x440,
  D3DXMESH_DYNAMIC                = 0x880,
  D3DXMESH_SOFTWAREPROCESSING     = 0x18000
} D3DXMESH, *LPD3DXMESH;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="D3DXMESH_32BIT"></span><span id="d3dxmesh_32bit"></span>**D3DXMESH- \_ 32-разрядный**
</dt> <dd>

Сетка имеет 32-разрядные индексы вместо 16-разрядных индексов. См. заметки.

</dd> <dt>

<span id="D3DXMESH_DONOTCLIP"></span><span id="d3dxmesh_donotclip"></span>**D3DXMESH \_ донотклип**
</dt> <dd>

Используйте флаг [**D3DUSAGE \_ донотклип**](d3dusage.md) Usage для буферов вершин и индексов.

</dd> <dt>

<span id="D3DXMESH_POINTS"></span><span id="d3dxmesh_points"></span>**\_Точки D3DXMESH**
</dt> <dd>

Используйте флаг [**использования \_ точек D3DUSAGE**](d3dusage.md) для буферов вершин и индексов.

</dd> <dt>

<span id="D3DXMESH_RTPATCHES"></span><span id="d3dxmesh_rtpatches"></span>**D3DXMESH \_ ртпатчес**
</dt> <dd>

Используйте флаг [**D3DUSAGE \_ ртпатчес**](d3dusage.md) Usage для буферов вершин и индексов.

</dd> <dt>

<span id="D3DXMESH_NPATCHES"></span><span id="d3dxmesh_npatches"></span>**D3DXMESH \_ нпатчес**
</dt> <dd>

Указание этого флага приводит к созданию вершины и буфера индекса сетки с флагом [**D3DUSAGE \_ нпатчес**](d3dusage.md) . Это необходимо, если объект сетки должен быть визуализирован с помощью N-patch с помощью Direct3D.

</dd> <dt>

<span id="D3DXMESH_VB_SYSTEMMEM"></span><span id="d3dxmesh_vb_systemmem"></span>**D3DXMESH \_ VB \_ системмем**
</dt> <dd>

Используйте флаг [**D3DPOOL \_ системмем**](./d3dpool.md) Usage для буферов вершин.

</dd> <dt>

<span id="D3DXMESH_VB_MANAGED"></span><span id="d3dxmesh_vb_managed"></span>**\_ \_ Управляемый VB D3DXMESH**
</dt> <dd>

Используйте [**\_ управляемый**](./d3dpool.md) флаг использования D3DPOOL для буферов вершин.

</dd> <dt>

<span id="D3DXMESH_VB_WRITEONLY"></span><span id="d3dxmesh_vb_writeonly"></span>**D3DXMESH \_ VB \_ WRITEONLY**
</dt> <dd>

Используйте флаг использования [**D3DUSAGE \_ WRITEONLY**](d3dusage.md) для буферов вершин.

</dd> <dt>

<span id="D3DXMESH_VB_DYNAMIC"></span><span id="d3dxmesh_vb_dynamic"></span>**D3DXMESH \_ VB \_ dynamic**
</dt> <dd>

Используйте флаг [**\_ динамического использования D3DUSAGE**](d3dusage.md) для буферов вершин.

</dd> <dt>

<span id="D3DXMESH_VB_SOFTWAREPROCESSING"></span><span id="d3dxmesh_vb_softwareprocessing"></span>**D3DXMESH \_ VB \_ софтварепроцессинг**
</dt> <dd>

Используйте флаг [**D3DUSAGE \_ софтварепроцессинг**](d3dusage.md) Usage для буферов вершин.

</dd> <dt>

<span id="D3DXMESH_IB_SYSTEMMEM"></span><span id="d3dxmesh_ib_systemmem"></span>**D3DXMESH \_ \_ системмем**
</dt> <dd>

Используйте флаг [**D3DPOOL \_ системмем**](./d3dpool.md) Usage для буферных индексов.

</dd> <dt>

<span id="D3DXMESH_IB_MANAGED"></span><span id="d3dxmesh_ib_managed"></span>**\_ \_ УПРАВЛЯЕМый D3DXMESH**
</dt> <dd>

Используйте [**\_ управляемый**](./d3dpool.md) флаг использования D3DPOOL для буферных индексов.

</dd> <dt>

<span id="D3DXMESH_IB_WRITEONLY"></span><span id="d3dxmesh_ib_writeonly"></span>**D3DXMESHа ( \_ \_ WRITEONLY)**
</dt> <dd>

Используйте флаг использования [**D3DUSAGE \_ WRITEONLY**](d3dusage.md) для буферных индексов.

</dd> <dt>

<span id="D3DXMESH_IB_DYNAMIC"></span><span id="d3dxmesh_ib_dynamic"></span>**\_Динамический D3DXMESH \_**
</dt> <dd>

Используйте флаг [**\_ динамического использования D3DUSAGE**](d3dusage.md) для буферных индексов.

</dd> <dt>

<span id="D3DXMESH_IB_SOFTWAREPROCESSING"></span><span id="d3dxmesh_ib_softwareprocessing"></span>**D3DXMESH \_ \_ софтварепроцессинг**
</dt> <dd>

Используйте флаг [**D3DUSAGE \_ софтварепроцессинг**](d3dusage.md) Usage для буферных индексов.

</dd> <dt>

<span id="D3DXMESH_VB_SHARE"></span><span id="d3dxmesh_vb_share"></span>**\_ \_ Общая папка VB D3DXMESH**
</dt> <dd>

Заставляет клонированные сетки совместно использовать буферы вершин.

</dd> <dt>

<span id="D3DXMESH_USEHWONLY"></span><span id="d3dxmesh_usehwonly"></span>**D3DXMESH \_ усехвонли**
</dt> <dd>

Использовать только аппаратную обработку. Для устройств в смешанном режиме этот флаг приведет к тому, что система будет использовать оборудование (если поддерживается в оборудовании) или будет по умолчанию обрабатывать программное обеспечение.

</dd> <dt>

<span id="D3DXMESH_SYSTEMMEM"></span><span id="d3dxmesh_systemmem"></span>**D3DXMESH \_ системмем**
</dt> <dd>

Эквивалентно указанию D3DXMESH \_ VB \_ СИСТЕММЕМ и D3DXMESH \_ \_ системмем.

</dd> <dt>

<span id="D3DXMESH_MANAGED"></span><span id="d3dxmesh_managed"></span>**\_Управляемый D3DXMESH**
</dt> <dd>

Эквивалентно указанию \_ \_ управляемого и D3DXMESHного \_ управления D3DXMESH VB \_ .

</dd> <dt>

<span id="D3DXMESH_WRITEONLY"></span><span id="d3dxmesh_writeonly"></span>**D3DXMESH \_ WRITEONLY**
</dt> <dd>

Эквивалентно указанию D3DXMESH \_ VB \_ WRITEONLY и D3DXMESH с помощью \_ \_ WRITEONLY.

</dd> <dt>

<span id="D3DXMESH_DYNAMIC"></span><span id="d3dxmesh_dynamic"></span>**D3DXMESH \_ dynamic**
</dt> <dd>

Эквивалентно указанию D3DXMESH \_ VB \_ dynamic и D3DXMESH \_ , \_ dynamic.

</dd> <dt>

<span id="D3DXMESH_SOFTWAREPROCESSING"></span><span id="d3dxmesh_softwareprocessing"></span>**D3DXMESH \_ софтварепроцессинг**
</dt> <dd>

Эквивалентно указанию D3DXMESH \_ VB \_ СОФТВАРЕПРОЦЕССИНГ и D3DXMESH \_ \_ софтварепроцессинг.

</dd> </dl>

## <a name="remarks"></a>Remarks

32-разрядная сеть (D3DXMESH \_ 32) теоретически может поддерживать (2 ^ 32)-1 лица и вершины. Однако выделение памяти для сетки, которая велика в 32-разрядной операционной системе, не является практичной.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Перечисления D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 
