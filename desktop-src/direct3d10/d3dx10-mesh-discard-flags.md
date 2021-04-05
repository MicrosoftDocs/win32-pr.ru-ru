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
ms.openlocfilehash: 6640834cf81bfa5e4b6263d3b3cfbb1181bb16c9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000470"
---
# <a name="d3dx10_mesh_discard_flags-enumeration"></a><span data-ttu-id="30fe1-104">\_ \_ \_ Перечисление флагов удаления сетки D3DX10</span><span class="sxs-lookup"><span data-stu-id="30fe1-104">D3DX10\_MESH\_DISCARD\_FLAGS enumeration</span></span>

<span data-ttu-id="30fe1-105">Указывает, какие части данных сетки следует отбросить от устройства.</span><span class="sxs-lookup"><span data-stu-id="30fe1-105">Specifies which pieces of mesh data to discard from the device.</span></span> <span data-ttu-id="30fe1-106">Используется с [**ID3DX10Mesh::D**](id3dx10mesh-discard.md).</span><span class="sxs-lookup"><span data-stu-id="30fe1-106">Used with [**ID3DX10Mesh::Discard**](id3dx10mesh-discard.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="30fe1-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="30fe1-107">Syntax</span></span>


```C++
typedef enum D3DX10_MESH_DISCARD_FLAGS { 
  D3DX10_MESH_DISCARD_ATTRIBUTE_BUFFER  = 0x01,
  D3DX10_MESH_DISCARD_ATTRIBUTE_TABLE   = 0x02,
  D3DX10_MESH_DISCARD_POINTREPS         = 0x04,
  D3DX10_MESH_DISCARD_ADJACENCY         = 0x08,
  D3DX10_MESH_DISCARD_DEVICE_BUFFERS    = 0x10
} D3DX10_MESH_DISCARD_FLAGS, *LPD3DX10_MESH_DISCARD_FLAGS;
```



## <a name="constants"></a><span data-ttu-id="30fe1-108">Константы</span><span class="sxs-lookup"><span data-stu-id="30fe1-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="30fe1-109"><span id="D3DX10_MESH_DISCARD_ATTRIBUTE_BUFFER"></span><span id="d3dx10_mesh_discard_attribute_buffer"></span>**\_ \_ Буфер атрибута для отмены сетки \_ D3DX10 \_**</span><span class="sxs-lookup"><span data-stu-id="30fe1-109"><span id="D3DX10_MESH_DISCARD_ATTRIBUTE_BUFFER"></span><span id="d3dx10_mesh_discard_attribute_buffer"></span>**D3DX10\_MESH\_DISCARD\_ATTRIBUTE\_BUFFER**</span></span>
</dt> <dd>

<span data-ttu-id="30fe1-110">Удаление буфера атрибута.</span><span class="sxs-lookup"><span data-stu-id="30fe1-110">Discard the attribute buffer.</span></span>

</dd> <dt>

<span data-ttu-id="30fe1-111"><span id="D3DX10_MESH_DISCARD_ATTRIBUTE_TABLE"></span><span id="d3dx10_mesh_discard_attribute_table"></span>**\_ \_ Таблица атрибутов для отмены сетки \_ D3DX10 \_**</span><span class="sxs-lookup"><span data-stu-id="30fe1-111"><span id="D3DX10_MESH_DISCARD_ATTRIBUTE_TABLE"></span><span id="d3dx10_mesh_discard_attribute_table"></span>**D3DX10\_MESH\_DISCARD\_ATTRIBUTE\_TABLE**</span></span>
</dt> <dd>

<span data-ttu-id="30fe1-112">Удаление таблицы атрибутов.</span><span class="sxs-lookup"><span data-stu-id="30fe1-112">Discard the attribute table.</span></span>

</dd> <dt>

<span data-ttu-id="30fe1-113"><span id="D3DX10_MESH_DISCARD_POINTREPS"></span><span id="d3dx10_mesh_discard_pointreps"></span>**D3DX10 \_ сетчатой \_ отклонения \_ поинтрепс**</span><span class="sxs-lookup"><span data-stu-id="30fe1-113"><span id="D3DX10_MESH_DISCARD_POINTREPS"></span><span id="d3dx10_mesh_discard_pointreps"></span>**D3DX10\_MESH\_DISCARD\_POINTREPS**</span></span>
</dt> <dd>

<span data-ttu-id="30fe1-114">Удалите буфер указателей.</span><span class="sxs-lookup"><span data-stu-id="30fe1-114">Discard the pointer reps buffer.</span></span>

</dd> <dt>

<span data-ttu-id="30fe1-115"><span id="D3DX10_MESH_DISCARD_ADJACENCY"></span><span id="d3dx10_mesh_discard_adjacency"></span>**D3DX10 \_ , \_ Удаление \_ соседа из сети**</span><span class="sxs-lookup"><span data-stu-id="30fe1-115"><span id="D3DX10_MESH_DISCARD_ADJACENCY"></span><span id="d3dx10_mesh_discard_adjacency"></span>**D3DX10\_MESH\_DISCARD\_ADJACENCY**</span></span>
</dt> <dd>

<span data-ttu-id="30fe1-116">Удалите буфер соседства.</span><span class="sxs-lookup"><span data-stu-id="30fe1-116">Discard the adjacency buffer.</span></span>

</dd> <dt>

<span data-ttu-id="30fe1-117"><span id="D3DX10_MESH_DISCARD_DEVICE_BUFFERS"></span><span id="d3dx10_mesh_discard_device_buffers"></span>**\_ \_ Буферы устройств для отклонения сетки \_ D3DX10 \_**</span><span class="sxs-lookup"><span data-stu-id="30fe1-117"><span id="D3DX10_MESH_DISCARD_DEVICE_BUFFERS"></span><span id="d3dx10_mesh_discard_device_buffers"></span>**D3DX10\_MESH\_DISCARD\_DEVICE\_BUFFERS**</span></span>
</dt> <dd>

<span data-ttu-id="30fe1-118">Удаление буферов, зафиксированных на устройстве (с помощью [**ID3DX10Mesh:: коммиттодевице**](id3dx10mesh-committodevice.md)).</span><span class="sxs-lookup"><span data-stu-id="30fe1-118">Discard the buffers committed to the device (with [**ID3DX10Mesh::CommitToDevice**](id3dx10mesh-committodevice.md)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="30fe1-119">Требования</span><span class="sxs-lookup"><span data-stu-id="30fe1-119">Requirements</span></span>



| <span data-ttu-id="30fe1-120">Требование</span><span class="sxs-lookup"><span data-stu-id="30fe1-120">Requirement</span></span> | <span data-ttu-id="30fe1-121">Значение</span><span class="sxs-lookup"><span data-stu-id="30fe1-121">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="30fe1-122">Header</span><span class="sxs-lookup"><span data-stu-id="30fe1-122">Header</span></span><br/> | <dl> <span data-ttu-id="30fe1-123"><dt>D3DX10Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="30fe1-123"><dt>D3DX10Mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30fe1-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="30fe1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30fe1-125">Перечисления D3DX</span><span class="sxs-lookup"><span data-stu-id="30fe1-125">D3DX Enumerations</span></span>](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




