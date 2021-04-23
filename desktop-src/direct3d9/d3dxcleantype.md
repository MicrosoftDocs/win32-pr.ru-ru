---
description: Определяет операции, выполняемые с вершинами при подготовке к очистке сетки.
ms.assetid: f222acaa-fa82-4591-b7c2-b520cb648ed5
title: Перечисление D3DXCLEANTYPE (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCLEANTYPE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: b38578d0f50521def552b8bd6608c2696b405d0f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273821"
---
# <a name="d3dxcleantype-enumeration"></a><span data-ttu-id="f9549-103">Перечисление D3DXCLEANTYPE</span><span class="sxs-lookup"><span data-stu-id="f9549-103">D3DXCLEANTYPE enumeration</span></span>

<span data-ttu-id="f9549-104">Определяет операции, выполняемые с вершинами при подготовке к очистке сетки.</span><span class="sxs-lookup"><span data-stu-id="f9549-104">Defines operations to perform on vertices in preparation for mesh cleaning.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9549-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f9549-105">Syntax</span></span>


```C++
typedef enum D3DXCLEANTYPE { 
  D3DXCLEAN_BACKFACING      = 1,
  D3DXCLEAN_BOWTIES         = 2,
  D3DXCLEAN_SKINNING        = D3DXCLEAN_BACKFACING,
  D3DXCLEAN_OPTIMIZATION    = D3DXCLEAN_BACKFACING,
  D3DXCLEAN_SIMPLIFICATION  = D3DXCLEAN_BACKFACING | D3DXCLEAN_BOWTIES
} D3DXCLEANTYPE, *LPD3DXCLEANTYPE;
```



## <a name="constants"></a><span data-ttu-id="f9549-106">Константы</span><span class="sxs-lookup"><span data-stu-id="f9549-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f9549-107"><span id="D3DXCLEAN_BACKFACING"></span><span id="d3dxclean_backfacing"></span>**D3DXCLEAN с \_ выходом**</span><span class="sxs-lookup"><span data-stu-id="f9549-107"><span id="D3DXCLEAN_BACKFACING"></span><span id="d3dxclean_backfacing"></span>**D3DXCLEAN\_BACKFACING**</span></span>
</dt> <dd>

<span data-ttu-id="f9549-108">Объедините треугольники, которые используют одни и те же индексы вершин, но имеют обычные нормали, указывающие в противоположных направлениях (треугольники с обратным переходом).</span><span class="sxs-lookup"><span data-stu-id="f9549-108">Merge triangles that share the same vertex indices but have face normals pointing in opposite directions (back-facing triangles).</span></span> <span data-ttu-id="f9549-109">Если треугольники не разбиваются путем добавления реплицируемой вершины, то данные о смежности между сетками из двух треугольников могут конфликтовать.</span><span class="sxs-lookup"><span data-stu-id="f9549-109">Unless the triangles are not split by adding a replicated vertex, mesh adjacency data from the two triangles may conflict.</span></span>

</dd> <dt>

<span data-ttu-id="f9549-110"><span id="D3DXCLEAN_BOWTIES"></span><span id="d3dxclean_bowties"></span>**D3DXCLEAN \_ бовтиес**</span><span class="sxs-lookup"><span data-stu-id="f9549-110"><span id="D3DXCLEAN_BOWTIES"></span><span id="d3dxclean_bowties"></span>**D3DXCLEAN\_BOWTIES**</span></span>
</dt> <dd>

<span data-ttu-id="f9549-111">Если вершина является вершине двух треугольников (bowtie), а операции сетки повлияют на один из вентиляторов, то разделите общую вершину на две новые вершины.</span><span class="sxs-lookup"><span data-stu-id="f9549-111">If a vertex is the apex of two triangle fans (a bowtie) and mesh operations will affect one of the fans, then split the shared vertex into two new vertices.</span></span> <span data-ttu-id="f9549-112">Бовтиес может вызвать проблемы для таких операций, как упрощение сетки, которое удаляет вершины, так как удаление одной вершины влияет на два отдельных набора треугольников.</span><span class="sxs-lookup"><span data-stu-id="f9549-112">Bowties can cause problems for operations such as mesh simplification that remove vertices, because removing one vertex affects two distinct sets of triangles.</span></span>

</dd> <dt>

<span data-ttu-id="f9549-113"><span id="D3DXCLEAN_SKINNING"></span><span id="d3dxclean_skinning"></span>**Выбор \_ обложки D3DXCLEAN**</span><span class="sxs-lookup"><span data-stu-id="f9549-113"><span id="D3DXCLEAN_SKINNING"></span><span id="d3dxclean_skinning"></span>**D3DXCLEAN\_SKINNING**</span></span>
</dt> <dd>

<span data-ttu-id="f9549-114">Используйте этот флаг, чтобы предотвратить бесконечные циклы во время операций настройки сетки.</span><span class="sxs-lookup"><span data-stu-id="f9549-114">Use this flag to prevent infinite loops during skinning setup mesh operations.</span></span>

</dd> <dt>

<span data-ttu-id="f9549-115"><span id="D3DXCLEAN_OPTIMIZATION"></span><span id="d3dxclean_optimization"></span>**\_Оптимизация D3DXCLEAN**</span><span class="sxs-lookup"><span data-stu-id="f9549-115"><span id="D3DXCLEAN_OPTIMIZATION"></span><span id="d3dxclean_optimization"></span>**D3DXCLEAN\_OPTIMIZATION**</span></span>
</dt> <dd>

<span data-ttu-id="f9549-116">Используйте этот флаг, чтобы предотвратить бесконечные циклы во время операций оптимизации сетки.</span><span class="sxs-lookup"><span data-stu-id="f9549-116">Use this flag to prevent infinite loops during mesh optimization operations.</span></span>

</dd> <dt>

<span data-ttu-id="f9549-117"><span id="D3DXCLEAN_SIMPLIFICATION"></span><span id="d3dxclean_simplification"></span>**\_Упрощение D3DXCLEAN**</span><span class="sxs-lookup"><span data-stu-id="f9549-117"><span id="D3DXCLEAN_SIMPLIFICATION"></span><span id="d3dxclean_simplification"></span>**D3DXCLEAN\_SIMPLIFICATION**</span></span>
</dt> <dd>

<span data-ttu-id="f9549-118">Используйте этот флаг, чтобы предотвратить бесконечные циклы во время операций упрощения сетки.</span><span class="sxs-lookup"><span data-stu-id="f9549-118">Use this flag to prevent infinite loops during mesh simplification operations.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f9549-119">Требования</span><span class="sxs-lookup"><span data-stu-id="f9549-119">Requirements</span></span>



| <span data-ttu-id="f9549-120">Требование</span><span class="sxs-lookup"><span data-stu-id="f9549-120">Requirement</span></span> | <span data-ttu-id="f9549-121">Значение</span><span class="sxs-lookup"><span data-stu-id="f9549-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f9549-122">Header</span><span class="sxs-lookup"><span data-stu-id="f9549-122">Header</span></span><br/> | <dl> <span data-ttu-id="f9549-123"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9549-123"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9549-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f9549-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9549-125">Перечисления D3DX</span><span class="sxs-lookup"><span data-stu-id="f9549-125">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




