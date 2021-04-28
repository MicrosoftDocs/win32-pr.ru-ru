---
description: Перечисление D3DXMESHOPT — указывает тип выполняемой оптимизации сетки.
ms.assetid: 32ef227a-b299-47c4-96b8-c0ea7bf549e1
title: Перечисление D3DXMESHOPT (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _D3DXMESHOPT
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: db7c2a2411d1c846c7369fc1d925a8e5569df3b1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114352"
---
# <a name="d3dxmeshopt-enumeration"></a><span data-ttu-id="e7351-103">Перечисление D3DXMESHOPT</span><span class="sxs-lookup"><span data-stu-id="e7351-103">D3DXMESHOPT enumeration</span></span>

<span data-ttu-id="e7351-104">Указывает тип оптимизации сетки для выполнения.</span><span class="sxs-lookup"><span data-stu-id="e7351-104">Specifies the type of mesh optimization to be performed.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7351-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e7351-105">Syntax</span></span>


```C++
enum _D3DXMESHOPT {
  D3DXMESHOPT_COMPACT            = 0x01000000, 
  D3DXMESHOPT_ATTRSORT           = 0x02000000, 
  D3DXMESHOPT_VERTEXCACHE        = 0x04000000, 
  D3DXMESHOPT_STRIPREORDER       = 0x08000000, 
  D3DXMESHOPT_IGNOREVERTS        = 0x10000000, 
  D3DXMESHOPT_DONOTSPLIT         = 0x20000000, 
  D3DXMESHOPT_DEVICEINDEPENDENT  = 0x40000000 

};
```



## <a name="constants"></a><span data-ttu-id="e7351-106">Константы</span><span class="sxs-lookup"><span data-stu-id="e7351-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="e7351-107"><span id="D3DXMESHOPT_COMPACT"></span><span id="d3dxmeshopt_compact"></span>**D3DXMESHOPT \_ Compact**</span><span class="sxs-lookup"><span data-stu-id="e7351-107"><span id="D3DXMESHOPT_COMPACT"></span><span id="d3dxmeshopt_compact"></span>**D3DXMESHOPT\_COMPACT**</span></span>
</dt> <dd>

<span data-ttu-id="e7351-108">Переупорядочивает лица, чтобы удалить неиспользуемые вершины и грани.</span><span class="sxs-lookup"><span data-stu-id="e7351-108">Reorders faces to remove unused vertices and faces.</span></span>

</dd> <dt>

<span data-ttu-id="e7351-109"><span id="D3DXMESHOPT_ATTRSORT"></span><span id="d3dxmeshopt_attrsort"></span>**D3DXMESHOPT \_ аттрсорт**</span><span class="sxs-lookup"><span data-stu-id="e7351-109"><span id="D3DXMESHOPT_ATTRSORT"></span><span id="d3dxmeshopt_attrsort"></span>**D3DXMESHOPT\_ATTRSORT**</span></span>
</dt> <dd>

<span data-ttu-id="e7351-110">Переупорядочивает лиц, чтобы оптимизировать для уменьшения количества изменений состояния набора атрибутов и повышения производительности [**ID3DXBaseMesh::D равсубсет**](id3dxbasemesh--drawsubset.md) .</span><span class="sxs-lookup"><span data-stu-id="e7351-110">Reorders faces to optimize for fewer attribute bundle state changes and enhanced [**ID3DXBaseMesh::DrawSubset**](id3dxbasemesh--drawsubset.md) performance.</span></span>

</dd> <dt>

<span data-ttu-id="e7351-111"><span id="D3DXMESHOPT_VERTEXCACHE"></span><span id="d3dxmeshopt_vertexcache"></span>**D3DXMESHOPT \_ вертекскаче**</span><span class="sxs-lookup"><span data-stu-id="e7351-111"><span id="D3DXMESHOPT_VERTEXCACHE"></span><span id="d3dxmeshopt_vertexcache"></span>**D3DXMESHOPT\_VERTEXCACHE**</span></span>
</dt> <dd>

<span data-ttu-id="e7351-112">Переупорядочивает лиц, чтобы увеличить количество попаданий в кэш вершин.</span><span class="sxs-lookup"><span data-stu-id="e7351-112">Reorders faces to increase the cache hit rate of vertex caches.</span></span>

</dd> <dt>

<span data-ttu-id="e7351-113"><span id="D3DXMESHOPT_STRIPREORDER"></span><span id="d3dxmeshopt_stripreorder"></span>**D3DXMESHOPT \_ стрипреордер**</span><span class="sxs-lookup"><span data-stu-id="e7351-113"><span id="D3DXMESHOPT_STRIPREORDER"></span><span id="d3dxmeshopt_stripreorder"></span>**D3DXMESHOPT\_STRIPREORDER**</span></span>
</dt> <dd>

<span data-ttu-id="e7351-114">Переупорядочивает лиц, чтобы максимально увеличить длину смежных треугольников.</span><span class="sxs-lookup"><span data-stu-id="e7351-114">Reorders faces to maximize length of adjacent triangles.</span></span>

</dd> <dt>

<span data-ttu-id="e7351-115"><span id="D3DXMESHOPT_IGNOREVERTS"></span><span id="d3dxmeshopt_ignoreverts"></span>**D3DXMESHOPT \_ игноревертс**</span><span class="sxs-lookup"><span data-stu-id="e7351-115"><span id="D3DXMESHOPT_IGNOREVERTS"></span><span id="d3dxmeshopt_ignoreverts"></span>**D3DXMESHOPT\_IGNOREVERTS**</span></span>
</dt> <dd>

<span data-ttu-id="e7351-116">Оптимизируйте только грани; не Оптимизируйте вершины.</span><span class="sxs-lookup"><span data-stu-id="e7351-116">Optimize the faces only; do not optimize the vertices.</span></span>

</dd> <dt>

<span data-ttu-id="e7351-117"><span id="D3DXMESHOPT_DONOTSPLIT"></span><span id="d3dxmeshopt_donotsplit"></span>**D3DXMESHOPT \_ донотсплит**</span><span class="sxs-lookup"><span data-stu-id="e7351-117"><span id="D3DXMESHOPT_DONOTSPLIT"></span><span id="d3dxmeshopt_donotsplit"></span>**D3DXMESHOPT\_DONOTSPLIT**</span></span>
</dt> <dd>

<span data-ttu-id="e7351-118">При сортировке атрибутов не разделите вершины, которые являются общими между группами атрибутов.</span><span class="sxs-lookup"><span data-stu-id="e7351-118">While attribute sorting, do not split vertices that are shared between attribute groups.</span></span>

</dd> <dt>

<span data-ttu-id="e7351-119"><span id="D3DXMESHOPT_DEVICEINDEPENDENT"></span><span id="d3dxmeshopt_deviceindependent"></span>**D3DXMESHOPT \_ девицеиндепендент**</span><span class="sxs-lookup"><span data-stu-id="e7351-119"><span id="D3DXMESHOPT_DEVICEINDEPENDENT"></span><span id="d3dxmeshopt_deviceindependent"></span>**D3DXMESHOPT\_DEVICEINDEPENDENT**</span></span>
</dt> <dd>

<span data-ttu-id="e7351-120">Влияет на размер кэша вершин.</span><span class="sxs-lookup"><span data-stu-id="e7351-120">Affects the vertex cache size.</span></span> <span data-ttu-id="e7351-121">С помощью этого флага задается размер кэша вершин по умолчанию, который хорошо работает на устаревшем оборудовании.</span><span class="sxs-lookup"><span data-stu-id="e7351-121">Using this flag specifies a default vertex cache size that works well on legacy hardware.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e7351-122">Remarks</span><span class="sxs-lookup"><span data-stu-id="e7351-122">Remarks</span></span>

<span data-ttu-id="e7351-123">\_Флаги оптимизации D3DXMESHOPT стрипреордер и D3DXMESHOPT \_ вертекскаче являются взаимоисключающими.</span><span class="sxs-lookup"><span data-stu-id="e7351-123">The D3DXMESHOPT\_STRIPREORDER and D3DXMESHOPT\_VERTEXCACHE optimization flags are mutually exclusive.</span></span>

<span data-ttu-id="e7351-124">Флаг D3DXMESHOPT \_ шаревб был удален из этого перечисления.</span><span class="sxs-lookup"><span data-stu-id="e7351-124">The D3DXMESHOPT\_SHAREVB flag has been removed from this enumeration.</span></span> <span data-ttu-id="e7351-125">\_ \_ Вместо этого используйте общую папку VB D3DXMESH в [**D3DXMESH**](./d3dxmesh.md).</span><span class="sxs-lookup"><span data-stu-id="e7351-125">Use D3DXMESH\_VB\_SHARE instead, in [**D3DXMESH**](./d3dxmesh.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e7351-126">Требования</span><span class="sxs-lookup"><span data-stu-id="e7351-126">Requirements</span></span>



| <span data-ttu-id="e7351-127">Требование</span><span class="sxs-lookup"><span data-stu-id="e7351-127">Requirement</span></span> | <span data-ttu-id="e7351-128">Значение</span><span class="sxs-lookup"><span data-stu-id="e7351-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e7351-129">Header</span><span class="sxs-lookup"><span data-stu-id="e7351-129">Header</span></span><br/> | <dl> <span data-ttu-id="e7351-130"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7351-130"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7351-131">См. также</span><span class="sxs-lookup"><span data-stu-id="e7351-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7351-132">Перечисления D3DX</span><span class="sxs-lookup"><span data-stu-id="e7351-132">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 
