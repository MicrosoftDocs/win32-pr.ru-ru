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
# <a name="d3dxmesh-enumeration"></a><span data-ttu-id="e5076-103">Перечисление D3DXMESH</span><span class="sxs-lookup"><span data-stu-id="e5076-103">D3DXMESH enumeration</span></span>

<span data-ttu-id="e5076-104">Флаги, используемые для указания параметров создания сетки.</span><span class="sxs-lookup"><span data-stu-id="e5076-104">Flags used to specify creation options for a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5076-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e5076-105">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="e5076-106">Константы</span><span class="sxs-lookup"><span data-stu-id="e5076-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="e5076-107"><span id="D3DXMESH_32BIT"></span><span id="d3dxmesh_32bit"></span>**D3DXMESH- \_ 32-разрядный**</span><span class="sxs-lookup"><span data-stu-id="e5076-107"><span id="D3DXMESH_32BIT"></span><span id="d3dxmesh_32bit"></span>**D3DXMESH\_32BIT**</span></span>
</dt> <dd>

<span data-ttu-id="e5076-108">Сетка имеет 32-разрядные индексы вместо 16-разрядных индексов.</span><span class="sxs-lookup"><span data-stu-id="e5076-108">The mesh has 32-bit indices instead of 16-bit indices.</span></span> <span data-ttu-id="e5076-109">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="e5076-109">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="e5076-110"><span id="D3DXMESH_DONOTCLIP"></span><span id="d3dxmesh_donotclip"></span>**D3DXMESH \_ донотклип**</span><span class="sxs-lookup"><span data-stu-id="e5076-110"><span id="D3DXMESH_DONOTCLIP"></span><span id="d3dxmesh_donotclip"></span>**D3DXMESH\_DONOTCLIP**</span></span>
</dt> <dd>

<span data-ttu-id="e5076-111">Используйте флаг [**D3DUSAGE \_ донотклип**](d3dusage.md) Usage для буферов вершин и индексов.</span><span class="sxs-lookup"><span data-stu-id="e5076-111">Use the [**D3DUSAGE\_DONOTCLIP**](d3dusage.md) usage flag for vertex and index buffers.</span></span>

</dd> <dt>

<span data-ttu-id="e5076-112"><span id="D3DXMESH_POINTS"></span><span id="d3dxmesh_points"></span>**\_Точки D3DXMESH**</span><span class="sxs-lookup"><span data-stu-id="e5076-112"><span id="D3DXMESH_POINTS"></span><span id="d3dxmesh_points"></span>**D3DXMESH\_POINTS**</span></span>
</dt> <dd>

<span data-ttu-id="e5076-113">Используйте флаг [**использования \_ точек D3DUSAGE**](d3dusage.md) для буферов вершин и индексов.</span><span class="sxs-lookup"><span data-stu-id="e5076-113">Use the [**D3DUSAGE\_POINTS**](d3dusage.md) usage flag for vertex and index buffers.</span></span>

</dd> <dt>

<span data-ttu-id="e5076-114"><span id="D3DXMESH_RTPATCHES"></span><span id="d3dxmesh_rtpatches"></span>**D3DXMESH \_ ртпатчес**</span><span class="sxs-lookup"><span data-stu-id="e5076-114"><span id="D3DXMESH_RTPATCHES"></span><span id="d3dxmesh_rtpatches"></span>**D3DXMESH\_RTPATCHES**</span></span>
</dt> <dd>

<span data-ttu-id="e5076-115">Используйте флаг [**D3DUSAGE \_ ртпатчес**](d3dusage.md) Usage для буферов вершин и индексов.</span><span class="sxs-lookup"><span data-stu-id="e5076-115">Use the [**D3DUSAGE\_RTPATCHES**](d3dusage.md) usage flag for vertex and index buffers.</span></span>

</dd> <dt>

<span data-ttu-id="e5076-116"><span id="D3DXMESH_NPATCHES"></span><span id="d3dxmesh_npatches"></span>**D3DXMESH \_ нпатчес**</span><span class="sxs-lookup"><span data-stu-id="e5076-116"><span id="D3DXMESH_NPATCHES"></span><span id="d3dxmesh_npatches"></span>**D3DXMESH\_NPATCHES**</span></span>
</dt> <dd>

<span data-ttu-id="e5076-117">Указание этого флага приводит к созданию вершины и буфера индекса сетки с флагом [**D3DUSAGE \_ нпатчес**](d3dusage.md) .</span><span class="sxs-lookup"><span data-stu-id="e5076-117">Specifying this flag causes the vertex and index buffer of the mesh to be created with [**D3DUSAGE\_NPATCHES**](d3dusage.md) flag.</span></span> <span data-ttu-id="e5076-118">Это необходимо, если объект сетки должен быть визуализирован с помощью N-patch с помощью Direct3D.</span><span class="sxs-lookup"><span data-stu-id="e5076-118">This is required if the mesh object is to be rendered using N-patch enhancement using Direct3D.</span></span>

</dd> <dt>

<span data-ttu-id="e5076-119"><span id="D3DXMESH_VB_SYSTEMMEM"></span><span id="d3dxmesh_vb_systemmem"></span>**D3DXMESH \_ VB \_ системмем**</span><span class="sxs-lookup"><span data-stu-id="e5076-119"><span id="D3DXMESH_VB_SYSTEMMEM"></span><span id="d3dxmesh_vb_systemmem"></span>**D3DXMESH\_VB\_SYSTEMMEM**</span></span>
</dt> <dd>

<span data-ttu-id="e5076-120">Используйте флаг [**D3DPOOL \_ системмем**](./d3dpool.md) Usage для буферов вершин.</span><span class="sxs-lookup"><span data-stu-id="e5076-120">Use the [**D3DPOOL\_SYSTEMMEM**](./d3dpool.md) usage flag for vertex buffers.</span></span>

</dd> <dt>

<span data-ttu-id="e5076-121"><span id="D3DXMESH_VB_MANAGED"></span><span id="d3dxmesh_vb_managed"></span>**\_ \_ Управляемый VB D3DXMESH**</span><span class="sxs-lookup"><span data-stu-id="e5076-121"><span id="D3DXMESH_VB_MANAGED"></span><span id="d3dxmesh_vb_managed"></span>**D3DXMESH\_VB\_MANAGED**</span></span>
</dt> <dd>

<span data-ttu-id="e5076-122">Используйте [**\_ управляемый**](./d3dpool.md) флаг использования D3DPOOL для буферов вершин.</span><span class="sxs-lookup"><span data-stu-id="e5076-122">Use the [**D3DPOOL\_MANAGED**](./d3dpool.md) usage flag for vertex buffers.</span></span>

</dd> <dt>

<span data-ttu-id="e5076-123"><span id="D3DXMESH_VB_WRITEONLY"></span><span id="d3dxmesh_vb_writeonly"></span>**D3DXMESH \_ VB \_ WRITEONLY**</span><span class="sxs-lookup"><span data-stu-id="e5076-123"><span id="D3DXMESH_VB_WRITEONLY"></span><span id="d3dxmesh_vb_writeonly"></span>**D3DXMESH\_VB\_WRITEONLY**</span></span>
</dt> <dd>

<span data-ttu-id="e5076-124">Используйте флаг использования [**D3DUSAGE \_ WRITEONLY**](d3dusage.md) для буферов вершин.</span><span class="sxs-lookup"><span data-stu-id="e5076-124">Use the [**D3DUSAGE\_WRITEONLY**](d3dusage.md) usage flag for vertex buffers.</span></span>

</dd> <dt>

<span data-ttu-id="e5076-125"><span id="D3DXMESH_VB_DYNAMIC"></span><span id="d3dxmesh_vb_dynamic"></span>**D3DXMESH \_ VB \_ dynamic**</span><span class="sxs-lookup"><span data-stu-id="e5076-125"><span id="D3DXMESH_VB_DYNAMIC"></span><span id="d3dxmesh_vb_dynamic"></span>**D3DXMESH\_VB\_DYNAMIC**</span></span>
</dt> <dd>

<span data-ttu-id="e5076-126">Используйте флаг [**\_ динамического использования D3DUSAGE**](d3dusage.md) для буферов вершин.</span><span class="sxs-lookup"><span data-stu-id="e5076-126">Use the [**D3DUSAGE\_DYNAMIC**](d3dusage.md) usage flag for vertex buffers.</span></span>

</dd> <dt>

<span data-ttu-id="e5076-127"><span id="D3DXMESH_VB_SOFTWAREPROCESSING"></span><span id="d3dxmesh_vb_softwareprocessing"></span>**D3DXMESH \_ VB \_ софтварепроцессинг**</span><span class="sxs-lookup"><span data-stu-id="e5076-127"><span id="D3DXMESH_VB_SOFTWAREPROCESSING"></span><span id="d3dxmesh_vb_softwareprocessing"></span>**D3DXMESH\_VB\_SOFTWAREPROCESSING**</span></span>
</dt> <dd>

<span data-ttu-id="e5076-128">Используйте флаг [**D3DUSAGE \_ софтварепроцессинг**](d3dusage.md) Usage для буферов вершин.</span><span class="sxs-lookup"><span data-stu-id="e5076-128">Use the [**D3DUSAGE\_SOFTWAREPROCESSING**](d3dusage.md) usage flag for vertex buffers.</span></span>

</dd> <dt>

<span data-ttu-id="e5076-129"><span id="D3DXMESH_IB_SYSTEMMEM"></span><span id="d3dxmesh_ib_systemmem"></span>**D3DXMESH \_ \_ системмем**</span><span class="sxs-lookup"><span data-stu-id="e5076-129"><span id="D3DXMESH_IB_SYSTEMMEM"></span><span id="d3dxmesh_ib_systemmem"></span>**D3DXMESH\_IB\_SYSTEMMEM**</span></span>
</dt> <dd>

<span data-ttu-id="e5076-130">Используйте флаг [**D3DPOOL \_ системмем**](./d3dpool.md) Usage для буферных индексов.</span><span class="sxs-lookup"><span data-stu-id="e5076-130">Use the [**D3DPOOL\_SYSTEMMEM**](./d3dpool.md) usage flag for index buffers.</span></span>

</dd> <dt>

<span data-ttu-id="e5076-131"><span id="D3DXMESH_IB_MANAGED"></span><span id="d3dxmesh_ib_managed"></span>**\_ \_ УПРАВЛЯЕМый D3DXMESH**</span><span class="sxs-lookup"><span data-stu-id="e5076-131"><span id="D3DXMESH_IB_MANAGED"></span><span id="d3dxmesh_ib_managed"></span>**D3DXMESH\_IB\_MANAGED**</span></span>
</dt> <dd>

<span data-ttu-id="e5076-132">Используйте [**\_ управляемый**](./d3dpool.md) флаг использования D3DPOOL для буферных индексов.</span><span class="sxs-lookup"><span data-stu-id="e5076-132">Use the [**D3DPOOL\_MANAGED**](./d3dpool.md) usage flag for index buffers.</span></span>

</dd> <dt>

<span data-ttu-id="e5076-133"><span id="D3DXMESH_IB_WRITEONLY"></span><span id="d3dxmesh_ib_writeonly"></span>**D3DXMESHа ( \_ \_ WRITEONLY)**</span><span class="sxs-lookup"><span data-stu-id="e5076-133"><span id="D3DXMESH_IB_WRITEONLY"></span><span id="d3dxmesh_ib_writeonly"></span>**D3DXMESH\_IB\_WRITEONLY**</span></span>
</dt> <dd>

<span data-ttu-id="e5076-134">Используйте флаг использования [**D3DUSAGE \_ WRITEONLY**](d3dusage.md) для буферных индексов.</span><span class="sxs-lookup"><span data-stu-id="e5076-134">Use the [**D3DUSAGE\_WRITEONLY**](d3dusage.md) usage flag for index buffers.</span></span>

</dd> <dt>

<span data-ttu-id="e5076-135"><span id="D3DXMESH_IB_DYNAMIC"></span><span id="d3dxmesh_ib_dynamic"></span>**\_Динамический D3DXMESH \_**</span><span class="sxs-lookup"><span data-stu-id="e5076-135"><span id="D3DXMESH_IB_DYNAMIC"></span><span id="d3dxmesh_ib_dynamic"></span>**D3DXMESH\_IB\_DYNAMIC**</span></span>
</dt> <dd>

<span data-ttu-id="e5076-136">Используйте флаг [**\_ динамического использования D3DUSAGE**](d3dusage.md) для буферных индексов.</span><span class="sxs-lookup"><span data-stu-id="e5076-136">Use the [**D3DUSAGE\_DYNAMIC**](d3dusage.md) usage flag for index buffers.</span></span>

</dd> <dt>

<span data-ttu-id="e5076-137"><span id="D3DXMESH_IB_SOFTWAREPROCESSING"></span><span id="d3dxmesh_ib_softwareprocessing"></span>**D3DXMESH \_ \_ софтварепроцессинг**</span><span class="sxs-lookup"><span data-stu-id="e5076-137"><span id="D3DXMESH_IB_SOFTWAREPROCESSING"></span><span id="d3dxmesh_ib_softwareprocessing"></span>**D3DXMESH\_IB\_SOFTWAREPROCESSING**</span></span>
</dt> <dd>

<span data-ttu-id="e5076-138">Используйте флаг [**D3DUSAGE \_ софтварепроцессинг**](d3dusage.md) Usage для буферных индексов.</span><span class="sxs-lookup"><span data-stu-id="e5076-138">Use the [**D3DUSAGE\_SOFTWAREPROCESSING**](d3dusage.md) usage flag for index buffers.</span></span>

</dd> <dt>

<span data-ttu-id="e5076-139"><span id="D3DXMESH_VB_SHARE"></span><span id="d3dxmesh_vb_share"></span>**\_ \_ Общая папка VB D3DXMESH**</span><span class="sxs-lookup"><span data-stu-id="e5076-139"><span id="D3DXMESH_VB_SHARE"></span><span id="d3dxmesh_vb_share"></span>**D3DXMESH\_VB\_SHARE**</span></span>
</dt> <dd>

<span data-ttu-id="e5076-140">Заставляет клонированные сетки совместно использовать буферы вершин.</span><span class="sxs-lookup"><span data-stu-id="e5076-140">Forces the cloned meshes to share vertex buffers.</span></span>

</dd> <dt>

<span data-ttu-id="e5076-141"><span id="D3DXMESH_USEHWONLY"></span><span id="d3dxmesh_usehwonly"></span>**D3DXMESH \_ усехвонли**</span><span class="sxs-lookup"><span data-stu-id="e5076-141"><span id="D3DXMESH_USEHWONLY"></span><span id="d3dxmesh_usehwonly"></span>**D3DXMESH\_USEHWONLY**</span></span>
</dt> <dd>

<span data-ttu-id="e5076-142">Использовать только аппаратную обработку.</span><span class="sxs-lookup"><span data-stu-id="e5076-142">Use hardware processing only.</span></span> <span data-ttu-id="e5076-143">Для устройств в смешанном режиме этот флаг приведет к тому, что система будет использовать оборудование (если поддерживается в оборудовании) или будет по умолчанию обрабатывать программное обеспечение.</span><span class="sxs-lookup"><span data-stu-id="e5076-143">For mixed-mode device, this flag will cause the system to use hardware (if supported in hardware) or will default to software processing.</span></span>

</dd> <dt>

<span data-ttu-id="e5076-144"><span id="D3DXMESH_SYSTEMMEM"></span><span id="d3dxmesh_systemmem"></span>**D3DXMESH \_ системмем**</span><span class="sxs-lookup"><span data-stu-id="e5076-144"><span id="D3DXMESH_SYSTEMMEM"></span><span id="d3dxmesh_systemmem"></span>**D3DXMESH\_SYSTEMMEM**</span></span>
</dt> <dd>

<span data-ttu-id="e5076-145">Эквивалентно указанию D3DXMESH \_ VB \_ СИСТЕММЕМ и D3DXMESH \_ \_ системмем.</span><span class="sxs-lookup"><span data-stu-id="e5076-145">Equivalent to specifying both D3DXMESH\_VB\_SYSTEMMEM and D3DXMESH\_IB\_SYSTEMMEM.</span></span>

</dd> <dt>

<span data-ttu-id="e5076-146"><span id="D3DXMESH_MANAGED"></span><span id="d3dxmesh_managed"></span>**\_Управляемый D3DXMESH**</span><span class="sxs-lookup"><span data-stu-id="e5076-146"><span id="D3DXMESH_MANAGED"></span><span id="d3dxmesh_managed"></span>**D3DXMESH\_MANAGED**</span></span>
</dt> <dd>

<span data-ttu-id="e5076-147">Эквивалентно указанию \_ \_ управляемого и D3DXMESHного \_ управления D3DXMESH VB \_ .</span><span class="sxs-lookup"><span data-stu-id="e5076-147">Equivalent to specifying both D3DXMESH\_VB\_MANAGED and D3DXMESH\_IB\_MANAGED.</span></span>

</dd> <dt>

<span data-ttu-id="e5076-148"><span id="D3DXMESH_WRITEONLY"></span><span id="d3dxmesh_writeonly"></span>**D3DXMESH \_ WRITEONLY**</span><span class="sxs-lookup"><span data-stu-id="e5076-148"><span id="D3DXMESH_WRITEONLY"></span><span id="d3dxmesh_writeonly"></span>**D3DXMESH\_WRITEONLY**</span></span>
</dt> <dd>

<span data-ttu-id="e5076-149">Эквивалентно указанию D3DXMESH \_ VB \_ WRITEONLY и D3DXMESH с помощью \_ \_ WRITEONLY.</span><span class="sxs-lookup"><span data-stu-id="e5076-149">Equivalent to specifying both D3DXMESH\_VB\_WRITEONLY and D3DXMESH\_IB\_WRITEONLY.</span></span>

</dd> <dt>

<span data-ttu-id="e5076-150"><span id="D3DXMESH_DYNAMIC"></span><span id="d3dxmesh_dynamic"></span>**D3DXMESH \_ dynamic**</span><span class="sxs-lookup"><span data-stu-id="e5076-150"><span id="D3DXMESH_DYNAMIC"></span><span id="d3dxmesh_dynamic"></span>**D3DXMESH\_DYNAMIC**</span></span>
</dt> <dd>

<span data-ttu-id="e5076-151">Эквивалентно указанию D3DXMESH \_ VB \_ dynamic и D3DXMESH \_ , \_ dynamic.</span><span class="sxs-lookup"><span data-stu-id="e5076-151">Equivalent to specifying both D3DXMESH\_VB\_DYNAMIC and D3DXMESH\_IB\_DYNAMIC.</span></span>

</dd> <dt>

<span data-ttu-id="e5076-152"><span id="D3DXMESH_SOFTWAREPROCESSING"></span><span id="d3dxmesh_softwareprocessing"></span>**D3DXMESH \_ софтварепроцессинг**</span><span class="sxs-lookup"><span data-stu-id="e5076-152"><span id="D3DXMESH_SOFTWAREPROCESSING"></span><span id="d3dxmesh_softwareprocessing"></span>**D3DXMESH\_SOFTWAREPROCESSING**</span></span>
</dt> <dd>

<span data-ttu-id="e5076-153">Эквивалентно указанию D3DXMESH \_ VB \_ СОФТВАРЕПРОЦЕССИНГ и D3DXMESH \_ \_ софтварепроцессинг.</span><span class="sxs-lookup"><span data-stu-id="e5076-153">Equivalent to specifying both D3DXMESH\_VB\_SOFTWAREPROCESSING and D3DXMESH\_IB\_SOFTWAREPROCESSING.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e5076-154">Remarks</span><span class="sxs-lookup"><span data-stu-id="e5076-154">Remarks</span></span>

<span data-ttu-id="e5076-155">32-разрядная сеть (D3DXMESH \_ 32) теоретически может поддерживать (2 ^ 32)-1 лица и вершины.</span><span class="sxs-lookup"><span data-stu-id="e5076-155">A 32-bit mesh (D3DXMESH\_32BIT) can theoretically support (2^32)-1 faces and vertices.</span></span> <span data-ttu-id="e5076-156">Однако выделение памяти для сетки, которая велика в 32-разрядной операционной системе, не является практичной.</span><span class="sxs-lookup"><span data-stu-id="e5076-156">However, allocating memory for a mesh that large on a 32-bit operating system is not practical.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5076-157">Требования</span><span class="sxs-lookup"><span data-stu-id="e5076-157">Requirements</span></span>



| <span data-ttu-id="e5076-158">Требование</span><span class="sxs-lookup"><span data-stu-id="e5076-158">Requirement</span></span> | <span data-ttu-id="e5076-159">Значение</span><span class="sxs-lookup"><span data-stu-id="e5076-159">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e5076-160">Header</span><span class="sxs-lookup"><span data-stu-id="e5076-160">Header</span></span><br/> | <dl> <span data-ttu-id="e5076-161"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5076-161"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5076-162">См. также</span><span class="sxs-lookup"><span data-stu-id="e5076-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5076-163">Перечисления D3DX</span><span class="sxs-lookup"><span data-stu-id="e5076-163">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 
