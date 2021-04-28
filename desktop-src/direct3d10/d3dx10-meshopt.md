---
description: Перечисление D3DX10_MESHOPT — указывает тип выполняемой оптимизации сетки.
ms.assetid: 20d1da8c-8c3d-4045-9a37-d534a8682716
title: Перечисление D3DX10_MESHOPT (D3DX10Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_MESHOPT
api_type:
- HeaderDef
api_location:
- D3DX10Mesh.h
ms.openlocfilehash: 7b3085cf9970f2c1f6fe3748cc4db8f4fb2b2a78
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105452"
---
# <a name="d3dx10_meshopt-enumeration"></a><span data-ttu-id="45cc2-103">\_Перечисление МЕШОПТ D3DX10</span><span class="sxs-lookup"><span data-stu-id="45cc2-103">D3DX10\_MESHOPT enumeration</span></span>

<span data-ttu-id="45cc2-104">Указывает тип оптимизации сетки для выполнения.</span><span class="sxs-lookup"><span data-stu-id="45cc2-104">Specifies the type of mesh optimization to be performed.</span></span>

## <a name="syntax"></a><span data-ttu-id="45cc2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="45cc2-105">Syntax</span></span>


```C++
typedef enum D3DX10_MESHOPT { 
  D3DX10_MESHOPT_COMPACT             = 0x01000000,
  D3DX10_MESHOPT_ATTR_SORT           = 0x02000000,
  D3DX10_MESHOPT_VERTEX_CACHE        = 0x04000000,
  D3DX10_MESHOPT_STRIP_REORDER       = 0x08000000,
  D3DX10_MESHOPT_IGNORE_VERTS        = 0x10000000,
  D3DX10_MESHOPT_DO_NOT_SPLIT        = 0x20000000,
  D3DX10_MESHOPT_DEVICE_INDEPENDENT  = 0x00400000
} D3DX10_MESHOPT, *LPD3DX10_MESHOPT;
```



## <a name="constants"></a><span data-ttu-id="45cc2-106">Константы</span><span class="sxs-lookup"><span data-stu-id="45cc2-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="45cc2-107"><span id="D3DX10_MESHOPT_COMPACT"></span><span id="d3dx10_meshopt_compact"></span>**D3DX10 \_ мешопт \_ Compact**</span><span class="sxs-lookup"><span data-stu-id="45cc2-107"><span id="D3DX10_MESHOPT_COMPACT"></span><span id="d3dx10_meshopt_compact"></span>**D3DX10\_MESHOPT\_COMPACT**</span></span>
</dt> <dd>

<span data-ttu-id="45cc2-108">Переупорядочивает лица, чтобы удалить неиспользуемые вершины и грани.</span><span class="sxs-lookup"><span data-stu-id="45cc2-108">Reorders faces to remove unused vertices and faces.</span></span>

</dd> <dt>

<span data-ttu-id="45cc2-109"><span id="D3DX10_MESHOPT_ATTR_SORT"></span><span id="d3dx10_meshopt_attr_sort"></span>**D3DX10 \_ мешопт \_ attr \_ Sort**</span><span class="sxs-lookup"><span data-stu-id="45cc2-109"><span id="D3DX10_MESHOPT_ATTR_SORT"></span><span id="d3dx10_meshopt_attr_sort"></span>**D3DX10\_MESHOPT\_ATTR\_SORT**</span></span>
</dt> <dd>

<span data-ttu-id="45cc2-110">Переупорядочивает лиц, чтобы оптимизировать для уменьшения количества изменений состояния набора атрибутов и повышения производительности Дравсубсет.</span><span class="sxs-lookup"><span data-stu-id="45cc2-110">Reorders faces to optimize for fewer attribute bundle state changes and enhanced DrawSubset performance.</span></span>

</dd> <dt>

<span data-ttu-id="45cc2-111"><span id="D3DX10_MESHOPT_VERTEX_CACHE"></span><span id="d3dx10_meshopt_vertex_cache"></span>**\_ \_ Кэш вершин D3DX10 \_ мешопт**</span><span class="sxs-lookup"><span data-stu-id="45cc2-111"><span id="D3DX10_MESHOPT_VERTEX_CACHE"></span><span id="d3dx10_meshopt_vertex_cache"></span>**D3DX10\_MESHOPT\_VERTEX\_CACHE**</span></span>
</dt> <dd>

<span data-ttu-id="45cc2-112">Переупорядочивает лиц, чтобы увеличить количество попаданий в кэш вершин.</span><span class="sxs-lookup"><span data-stu-id="45cc2-112">Reorders faces to increase the cache hit rate of vertex caches.</span></span>

</dd> <dt>

<span data-ttu-id="45cc2-113"><span id="D3DX10_MESHOPT_STRIP_REORDER"></span><span id="d3dx10_meshopt_strip_reorder"></span>**\_ \_ Переупорядочение чередующихся мешопт D3DX10 \_**</span><span class="sxs-lookup"><span data-stu-id="45cc2-113"><span id="D3DX10_MESHOPT_STRIP_REORDER"></span><span id="d3dx10_meshopt_strip_reorder"></span>**D3DX10\_MESHOPT\_STRIP\_REORDER**</span></span>
</dt> <dd>

<span data-ttu-id="45cc2-114">Переупорядочивает лиц, чтобы максимально увеличить длину смежных треугольников.</span><span class="sxs-lookup"><span data-stu-id="45cc2-114">Reorders faces to maximize length of adjacent triangles.</span></span>

</dd> <dt>

<span data-ttu-id="45cc2-115"><span id="D3DX10_MESHOPT_IGNORE_VERTS"></span><span id="d3dx10_meshopt_ignore_verts"></span>**D3DX10 \_ мешопт \_ игнорировать \_ вертикальные**</span><span class="sxs-lookup"><span data-stu-id="45cc2-115"><span id="D3DX10_MESHOPT_IGNORE_VERTS"></span><span id="d3dx10_meshopt_ignore_verts"></span>**D3DX10\_MESHOPT\_IGNORE\_VERTS**</span></span>
</dt> <dd>

<span data-ttu-id="45cc2-116">Оптимизируйте только грани; не Оптимизируйте вершины.</span><span class="sxs-lookup"><span data-stu-id="45cc2-116">Optimize the faces only; do not optimize the vertices.</span></span>

</dd> <dt>

<span data-ttu-id="45cc2-117"><span id="D3DX10_MESHOPT_DO_NOT_SPLIT"></span><span id="d3dx10_meshopt_do_not_split"></span>**D3DX10 \_ мешопт \_ \_ не \_ разбиваются**</span><span class="sxs-lookup"><span data-stu-id="45cc2-117"><span id="D3DX10_MESHOPT_DO_NOT_SPLIT"></span><span id="d3dx10_meshopt_do_not_split"></span>**D3DX10\_MESHOPT\_DO\_NOT\_SPLIT**</span></span>
</dt> <dd>

<span data-ttu-id="45cc2-118">При сортировке атрибутов не разделите вершины, которые являются общими между группами атрибутов.</span><span class="sxs-lookup"><span data-stu-id="45cc2-118">While attribute sorting, do not split vertices that are shared between attribute groups.</span></span>

</dd> <dt>

<span data-ttu-id="45cc2-119"><span id="D3DX10_MESHOPT_DEVICE_INDEPENDENT"></span><span id="d3dx10_meshopt_device_independent"></span>**\_ \_ Независимое устройство D3DX10 мешопт \_**</span><span class="sxs-lookup"><span data-stu-id="45cc2-119"><span id="D3DX10_MESHOPT_DEVICE_INDEPENDENT"></span><span id="d3dx10_meshopt_device_independent"></span>**D3DX10\_MESHOPT\_DEVICE\_INDEPENDENT**</span></span>
</dt> <dd>

<span data-ttu-id="45cc2-120">Влияет на размер кэша вершин.</span><span class="sxs-lookup"><span data-stu-id="45cc2-120">Affects the vertex cache size.</span></span> <span data-ttu-id="45cc2-121">С помощью этого флага задается размер кэша вершин по умолчанию, который хорошо работает на устаревшем оборудовании.</span><span class="sxs-lookup"><span data-stu-id="45cc2-121">Using this flag specifies a default vertex cache size that works well on legacy hardware.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="45cc2-122">Remarks</span><span class="sxs-lookup"><span data-stu-id="45cc2-122">Remarks</span></span>

<span data-ttu-id="45cc2-123">\_Флаги оптимизации D3DXMESHOPT стрипреордер и D3DXMESHOPT \_ вертекскаче являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="45cc2-123">The D3DXMESHOPT\_STRIPREORDER and D3DXMESHOPT\_VERTEXCACHE optimization flags are mutually exclusive.</span></span>

<span data-ttu-id="45cc2-124">Флаг D3DXMESHOPT \_ шаревб был удален из этого перечисления.</span><span class="sxs-lookup"><span data-stu-id="45cc2-124">The D3DXMESHOPT\_SHAREVB flag has been removed from this enumeration.</span></span> <span data-ttu-id="45cc2-125">\_ \_ Вместо этого используйте общую папку VB D3DXMESH в D3DXMESH.</span><span class="sxs-lookup"><span data-stu-id="45cc2-125">Use D3DXMESH\_VB\_SHARE instead, in D3DXMESH.</span></span>

## <a name="requirements"></a><span data-ttu-id="45cc2-126">Требования</span><span class="sxs-lookup"><span data-stu-id="45cc2-126">Requirements</span></span>



| <span data-ttu-id="45cc2-127">Требование</span><span class="sxs-lookup"><span data-stu-id="45cc2-127">Requirement</span></span> | <span data-ttu-id="45cc2-128">Значение</span><span class="sxs-lookup"><span data-stu-id="45cc2-128">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="45cc2-129">Header</span><span class="sxs-lookup"><span data-stu-id="45cc2-129">Header</span></span><br/> | <dl> <span data-ttu-id="45cc2-130"><dt>D3DX10Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="45cc2-130"><dt>D3DX10Mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45cc2-131">См. также</span><span class="sxs-lookup"><span data-stu-id="45cc2-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45cc2-132">Перечисления D3DX</span><span class="sxs-lookup"><span data-stu-id="45cc2-132">D3DX Enumerations</span></span>](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




