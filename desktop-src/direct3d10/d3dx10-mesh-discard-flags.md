---
description: Указывает, какие части данных сетки следует отбросить от устройства. Используется с ID3DX10Mesh::D.
ms.assetid: 8b3c22ab-1337-4a66-ae32-17bd1b73f624
title: Перечисление D3DX10_MESH_DISCARD_FLAGS (D3DX10Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_MESH_DISCARD_FLAGS
api_type:
- HeaderDef
api_location:
- D3DX10Mesh.h
ms.openlocfilehash: d4b98550a2f3a896ed7b99f3e16f33a399a58035497e44420709ee8a0726901b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989474"
---
# <a name="d3dx10_mesh_discard_flags-enumeration"></a>\_ \_ \_ Перечисление флагов удаления сетки D3DX10

Указывает, какие части данных сетки следует отбросить от устройства. Используется с [**ID3DX10Mesh::D**](id3dx10mesh-discard.md).

## <a name="syntax"></a>Синтаксис


```C++
typedef enum D3DX10_MESH_DISCARD_FLAGS { 
  D3DX10_MESH_DISCARD_ATTRIBUTE_BUFFER  = 0x01,
  D3DX10_MESH_DISCARD_ATTRIBUTE_TABLE   = 0x02,
  D3DX10_MESH_DISCARD_POINTREPS         = 0x04,
  D3DX10_MESH_DISCARD_ADJACENCY         = 0x08,
  D3DX10_MESH_DISCARD_DEVICE_BUFFERS    = 0x10
} D3DX10_MESH_DISCARD_FLAGS, *LPD3DX10_MESH_DISCARD_FLAGS;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="D3DX10_MESH_DISCARD_ATTRIBUTE_BUFFER"></span><span id="d3dx10_mesh_discard_attribute_buffer"></span>**\_ \_ Буфер атрибута для отмены сетки \_ D3DX10 \_**
</dt> <dd>

Удаление буфера атрибута.

</dd> <dt>

<span id="D3DX10_MESH_DISCARD_ATTRIBUTE_TABLE"></span><span id="d3dx10_mesh_discard_attribute_table"></span>**\_ \_ Таблица атрибутов для отмены сетки \_ D3DX10 \_**
</dt> <dd>

Удаление таблицы атрибутов.

</dd> <dt>

<span id="D3DX10_MESH_DISCARD_POINTREPS"></span><span id="d3dx10_mesh_discard_pointreps"></span>**D3DX10 \_ сетчатой \_ отклонения \_ поинтрепс**
</dt> <dd>

Удалите буфер указателей.

</dd> <dt>

<span id="D3DX10_MESH_DISCARD_ADJACENCY"></span><span id="d3dx10_mesh_discard_adjacency"></span>**D3DX10 \_ , \_ Удаление \_ соседа из сети**
</dt> <dd>

Удалите буфер соседства.

</dd> <dt>

<span id="D3DX10_MESH_DISCARD_DEVICE_BUFFERS"></span><span id="d3dx10_mesh_discard_device_buffers"></span>**\_ \_ Буферы устройств для отклонения сетки \_ D3DX10 \_**
</dt> <dd>

Удаление буферов, зафиксированных на устройстве (с помощью [**ID3DX10Mesh:: коммиттодевице**](id3dx10mesh-committodevice.md)).

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|-----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3DX10Mesh. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Перечисления D3DX](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




