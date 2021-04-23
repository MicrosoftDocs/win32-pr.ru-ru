---
description: Определяет, пересекает ли луч том ограничивающего прямоугольника бокса.
ms.assetid: 45ff8540-ed5c-4f54-b3b7-3385087a6863
title: Функция D3DXBoxBoundProbe (D3DX9Mesh.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 707ab21a3babe7d9a93f776f438cbaab7137849b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157199"
---
# <a name="d3dxboxboundprobe-function"></a><span data-ttu-id="2f821-103">Функция D3DXBoxBoundProbe</span><span class="sxs-lookup"><span data-stu-id="2f821-103">D3DXBoxBoundProbe function</span></span>

<span data-ttu-id="2f821-104">Определяет, пересекает ли луч том ограничивающего прямоугольника бокса.</span><span class="sxs-lookup"><span data-stu-id="2f821-104">Determines whether a ray intersects the volume of a box's bounding box.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f821-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2f821-105">Syntax</span></span>


```C++
BOOL D3DXBoxBoundProbe(
  _In_ const D3DXVECTOR3 *pMin,
  _In_ const D3DXVECTOR3 *pMax,
  _In_ const D3DXVECTOR3 *pRayPosition,
  _In_ const D3DXVECTOR3 *pRayDirection
);
```



## <a name="parameters"></a><span data-ttu-id="2f821-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2f821-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f821-107">*ПМИН* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2f821-107">*pMin* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f821-108">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="2f821-108">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="2f821-109">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , описывающий левый нижний угол ограничивающего прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="2f821-109">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, describing the lower-left corner of the bounding box.</span></span> <span data-ttu-id="2f821-110">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="2f821-110">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="2f821-111">*ПМАКС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2f821-111">*pMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f821-112">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="2f821-112">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="2f821-113">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , описывающий правый верхний угол ограничивающего прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="2f821-113">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, describing the upper-right corner of the bounding box.</span></span> <span data-ttu-id="2f821-114">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="2f821-114">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="2f821-115">*прайпоситион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2f821-115">*pRayPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f821-116">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="2f821-116">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="2f821-117">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , задавая координату начала луча.</span><span class="sxs-lookup"><span data-stu-id="2f821-117">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the origin coordinate of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="2f821-118">*прайдиректион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2f821-118">*pRayDirection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f821-119">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="2f821-119">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="2f821-120">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , в которой указывается направление луча.</span><span class="sxs-lookup"><span data-stu-id="2f821-120">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the direction of the ray.</span></span> <span data-ttu-id="2f821-121">Этот вектор не должен быть (0, 0, 0), но не требует нормализации.</span><span class="sxs-lookup"><span data-stu-id="2f821-121">This vector should not be (0,0,0) but does not need to be normalized.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f821-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2f821-122">Return value</span></span>

<span data-ttu-id="2f821-123">Тип: **[ **bool** .](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2f821-123">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2f821-124">Возвращает **значение true** , если луч пересекает том ограничивающего прямоугольника бокса.</span><span class="sxs-lookup"><span data-stu-id="2f821-124">Returns **TRUE** if the ray intersects the volume of the box's bounding box.</span></span> <span data-ttu-id="2f821-125">В противном случае возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="2f821-125">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f821-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2f821-126">Remarks</span></span>

<span data-ttu-id="2f821-127">**D3DXboxBoundProbe** определяет, пересекает ли луч том ограничивающего прямоугольника бокса, а не только поверхность бокса.</span><span class="sxs-lookup"><span data-stu-id="2f821-127">**D3DXboxBoundProbe** determines if the ray intersects the volume of the box's bounding box, not just the surface of the box.</span></span>

<span data-ttu-id="2f821-128">Значения, передаваемые в **D3DXboxBoundProbe** , — это xMin, xMax, yMin, yMax, змин и змакс.</span><span class="sxs-lookup"><span data-stu-id="2f821-128">The values passed to **D3DXboxBoundProbe** are xmin, xmax, ymin, ymax, zmin, and zmax.</span></span> <span data-ttu-id="2f821-129">Таким же ниже определяются углы ограничивающего прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="2f821-129">Thus, the following defines the corners of the bounding box.</span></span>


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



<span data-ttu-id="2f821-130">Глубина ограничивающего прямоугольника в направлении по оси z равна змакс-змин, в направлении по оси y — ymax-ymin, а в направлении x — xmax-xmin.</span><span class="sxs-lookup"><span data-stu-id="2f821-130">The depth of the bounding box in the z direction is zmax - zmin, in the y direction is ymax - ymin, and in the x direction is xmax - xmin.</span></span> <span data-ttu-id="2f821-131">Например, при использовании следующих минимальных и максимальных векторов, min (-1,-1,-1) и Max (1, 1, 1) ограничивающий прямоугольник определяется следующим образом.</span><span class="sxs-lookup"><span data-stu-id="2f821-131">For example, with the following minimum and maximum vectors, min (-1, -1, -1) and max (1, 1, 1), the bounding box is defined in the following manner.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="2f821-132">Требования</span><span class="sxs-lookup"><span data-stu-id="2f821-132">Requirements</span></span>



| <span data-ttu-id="2f821-133">Требование</span><span class="sxs-lookup"><span data-stu-id="2f821-133">Requirement</span></span> | <span data-ttu-id="2f821-134">Значение</span><span class="sxs-lookup"><span data-stu-id="2f821-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f821-135">Header</span><span class="sxs-lookup"><span data-stu-id="2f821-135">Header</span></span><br/>  | <dl> <span data-ttu-id="2f821-136"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f821-136"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="2f821-137">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2f821-137">Library</span></span><br/> | <dl> <span data-ttu-id="2f821-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2f821-138"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2f821-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2f821-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f821-140">Функции сетки</span><span class="sxs-lookup"><span data-stu-id="2f821-140">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="2f821-141">**D3DXComputeBoundingBox**</span><span class="sxs-lookup"><span data-stu-id="2f821-141">**D3DXComputeBoundingBox**</span></span>](d3dxcomputeboundingbox.md)
</dt> </dl>

 

 
