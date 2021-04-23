---
description: Функция D3DXBoxBoundProbe (D3DX10math. h) определяет, пересекает ли луч том ограничивающего прямоугольника бокса.
ms.assetid: d3cdcf89-461b-44b0-b5d0-ca2e3869a5ad
title: Функция D3DXBoxBoundProbe (D3DX10math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXBoxBoundProbe
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e1a8d1a7b879814cff43e31b060cc2af53167818
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187817"
---
# <a name="d3dxboxboundprobe-function-d3dx10mathh"></a><span data-ttu-id="2dae8-103">Функция D3DXBoxBoundProbe (D3DX10math. h)</span><span class="sxs-lookup"><span data-stu-id="2dae8-103">D3DXBoxBoundProbe function (D3DX10math.h)</span></span>

<span data-ttu-id="2dae8-104">Определяет, пересекает ли луч том ограничивающего прямоугольника бокса.</span><span class="sxs-lookup"><span data-stu-id="2dae8-104">Determines whether a ray intersects the volume of a box's bounding box.</span></span>

## <a name="syntax"></a><span data-ttu-id="2dae8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2dae8-105">Syntax</span></span>


```C++
BOOL D3DXBoxBoundProbe(
  _In_ const D3DXVECTOR3 *pMin,
  _In_ const D3DXVECTOR3 *pMax,
  _In_ const D3DXVECTOR3 *pRayPosition,
  _In_ const D3DXVECTOR3 *pRayDirection
);
```



## <a name="parameters"></a><span data-ttu-id="2dae8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2dae8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2dae8-107">*ПМИН* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2dae8-107">*pMin* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2dae8-108">Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="2dae8-108">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="2dae8-109">Указатель на [**D3DXVECTOR3**](d3d10-d3dxvector3.md), описывающий левый нижний угол ограничивающего прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="2dae8-109">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md), describing the lower-left corner of the bounding box.</span></span> <span data-ttu-id="2dae8-110">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="2dae8-110">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="2dae8-111">*ПМАКС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2dae8-111">*pMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2dae8-112">Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="2dae8-112">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="2dae8-113">Указатель на структуру [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , описывающий правый верхний угол ограничивающего прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="2dae8-113">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, describing the upper-right corner of the bounding box.</span></span> <span data-ttu-id="2dae8-114">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="2dae8-114">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="2dae8-115">*прайпоситион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2dae8-115">*pRayPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2dae8-116">Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="2dae8-116">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="2dae8-117">Указатель на структуру D3DXVECTOR3, задавая координату начала луча.</span><span class="sxs-lookup"><span data-stu-id="2dae8-117">Pointer to a D3DXVECTOR3 structure, specifying the origin coordinate of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="2dae8-118">*прайдиректион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2dae8-118">*pRayDirection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2dae8-119">Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="2dae8-119">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="2dae8-120">Указатель на структуру D3DXVECTOR3, в которой указывается направление луча.</span><span class="sxs-lookup"><span data-stu-id="2dae8-120">Pointer to a D3DXVECTOR3 structure, specifying the direction of the ray.</span></span> <span data-ttu-id="2dae8-121">Этот вектор не должен быть (0, 0, 0), но не требует нормализации.</span><span class="sxs-lookup"><span data-stu-id="2dae8-121">This vector should not be (0,0,0) but does not need to be normalized.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2dae8-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2dae8-122">Return value</span></span>

<span data-ttu-id="2dae8-123">Тип: **[ **bool** .](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2dae8-123">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2dae8-124">Возвращает **значение true** , если луч пересекает том ограничивающего прямоугольника бокса.</span><span class="sxs-lookup"><span data-stu-id="2dae8-124">Returns **TRUE** if the ray intersects the volume of the box's bounding box.</span></span> <span data-ttu-id="2dae8-125">В противном случае возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="2dae8-125">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="2dae8-126">Remarks</span><span class="sxs-lookup"><span data-stu-id="2dae8-126">Remarks</span></span>

<span data-ttu-id="2dae8-127">**D3DXBoxBoundProbe** определяет, пересекает ли луч том ограничивающего прямоугольника бокса, а не только поверхность бокса.</span><span class="sxs-lookup"><span data-stu-id="2dae8-127">**D3DXBoxBoundProbe** determines if the ray intersects the volume of the box's bounding box, not just the surface of the box.</span></span>

<span data-ttu-id="2dae8-128">Значения, передаваемые в **D3DXBoxBoundProbe** , — это xMin, xMax, yMin, yMax, змин и змакс.</span><span class="sxs-lookup"><span data-stu-id="2dae8-128">The values passed to **D3DXBoxBoundProbe** are xmin, xmax, ymin, ymax, zmin, and zmax.</span></span> <span data-ttu-id="2dae8-129">Таким же ниже определяются углы ограничивающего прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="2dae8-129">Thus, the following defines the corners of the bounding box.</span></span>


```
xmax, ymax, zmax
xmax, ymax, zmin
xmax, ymin, zmax
xmax, ymin, zmin
xmin, ymax, zmax
xmin, ymax, zmin
xmin, ymin, zmax
xmin, ymin, zmin
```



<span data-ttu-id="2dae8-130">Глубина ограничивающего прямоугольника в направлении по оси z равна змакс-змин, в направлении по оси y — ymax-ymin, а в направлении x — xmax-xmin.</span><span class="sxs-lookup"><span data-stu-id="2dae8-130">The depth of the bounding box in the z direction is zmax - zmin, in the y direction is ymax - ymin, and in the x direction is xmax - xmin.</span></span> <span data-ttu-id="2dae8-131">Например, при использовании следующих минимальных и максимальных векторов, min (-1,-1,-1) и Max (1, 1, 1) ограничивающий прямоугольник определяется следующим образом.</span><span class="sxs-lookup"><span data-stu-id="2dae8-131">For example, with the following minimum and maximum vectors, min (-1, -1, -1) and max (1, 1, 1), the bounding box is defined in the following manner.</span></span>


```
 1,  1,  1
 1,  1, -1
 1, -1,  1
 1, -1, -1
-1,  1,  1
-1,  1, -1
-1, -1,  1
-1, -1, -l
```



## <a name="requirements"></a><span data-ttu-id="2dae8-132">Требования</span><span class="sxs-lookup"><span data-stu-id="2dae8-132">Requirements</span></span>



| <span data-ttu-id="2dae8-133">Требование</span><span class="sxs-lookup"><span data-stu-id="2dae8-133">Requirement</span></span> | <span data-ttu-id="2dae8-134">Значение</span><span class="sxs-lookup"><span data-stu-id="2dae8-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2dae8-135">Заголовок</span><span class="sxs-lookup"><span data-stu-id="2dae8-135">Header</span></span>  | <span data-ttu-id="2dae8-136">D3DX10math. h</span><span class="sxs-lookup"><span data-stu-id="2dae8-136">D3DX10math.h</span></span> |
| <span data-ttu-id="2dae8-137">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2dae8-137">Library</span></span> | <span data-ttu-id="2dae8-138">D3DX10. lib</span><span class="sxs-lookup"><span data-stu-id="2dae8-138">D3DX10.lib</span></span>  |



## <a name="see-also"></a><span data-ttu-id="2dae8-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2dae8-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2dae8-140">Функции сетки</span><span class="sxs-lookup"><span data-stu-id="2dae8-140">Mesh Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
