---
description: Функция D3DXSphereBoundProbe (D3DX10math. h). определяет, пересекает ли луч объем ограничивающего прямоугольника сферы.
ms.assetid: 5984a1a6-d36c-4a05-8c74-0ece7443356c
title: Функция D3DXSphereBoundProbe (D3DX10math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSphereBoundProbe
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: fb5a329e39631dff626ff1c7945ad4b05f9dcd58
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108472"
---
# <a name="d3dxsphereboundprobe-function-d3dx10mathh"></a><span data-ttu-id="31801-103">Функция D3DXSphereBoundProbe (D3DX10math. h)</span><span class="sxs-lookup"><span data-stu-id="31801-103">D3DXSphereBoundProbe function (D3DX10math.h)</span></span>

<span data-ttu-id="31801-104">Определяет, пересекает ли луч объем ограничивающего прямоугольника сферы.</span><span class="sxs-lookup"><span data-stu-id="31801-104">Determines if a ray intersects the volume of a sphere's bounding box.</span></span>

## <a name="syntax"></a><span data-ttu-id="31801-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="31801-105">Syntax</span></span>


```C++
BOOL D3DXSphereBoundProbe(
  _In_ const D3DXVECTOR3 *pCenter,
  _In_       FLOAT       Radius,
  _In_ const D3DXVECTOR3 *pRayPosition,
  _In_ const D3DXVECTOR3 *pRayDirection
);
```



## <a name="parameters"></a><span data-ttu-id="31801-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="31801-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31801-107">*пцентер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="31801-107">*pCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31801-108">Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="31801-108">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="31801-109">Указатель на структуру [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , задавая центральную координату сферы.</span><span class="sxs-lookup"><span data-stu-id="31801-109">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, specifying the center coordinate of the sphere.</span></span>

</dd> <dt>

<span data-ttu-id="31801-110">*Радиус* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="31801-110">*Radius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31801-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="31801-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="31801-112">Радиус сферы.</span><span class="sxs-lookup"><span data-stu-id="31801-112">Radius of the sphere.</span></span>

</dd> <dt>

<span data-ttu-id="31801-113">*прайпоситион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="31801-113">*pRayPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31801-114">Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="31801-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="31801-115">Указатель на структуру [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , задавая координату начала луча.</span><span class="sxs-lookup"><span data-stu-id="31801-115">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, specifying the origin coordinate of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="31801-116">*прайдиректион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="31801-116">*pRayDirection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31801-117">Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="31801-117">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="31801-118">Указатель на структуру [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , в которой указывается направление луча.</span><span class="sxs-lookup"><span data-stu-id="31801-118">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, specifying the direction of the ray.</span></span> <span data-ttu-id="31801-119">Этот вектор не должен быть (0, 0, 0), но не требует нормализации.</span><span class="sxs-lookup"><span data-stu-id="31801-119">This vector should not be (0,0,0) but does not need to be normalized.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31801-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="31801-120">Return value</span></span>

<span data-ttu-id="31801-121">Тип: **[ **bool** .](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="31801-121">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="31801-122">Возвращает **значение true** , если луч пересекает объем ограничивающего прямоугольника сферы.</span><span class="sxs-lookup"><span data-stu-id="31801-122">Returns **TRUE** if the ray intersects the volume of the sphere's bounding box.</span></span> <span data-ttu-id="31801-123">В противном случае возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="31801-123">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="31801-124">Remarks</span><span class="sxs-lookup"><span data-stu-id="31801-124">Remarks</span></span>

<span data-ttu-id="31801-125">**D3DXSphereBoundProbe** определяет, пересекает ли луч объем ограничивающего прямоугольника сферы, а не только поверхность сферы.</span><span class="sxs-lookup"><span data-stu-id="31801-125">**D3DXSphereBoundProbe** determines if the ray intersects the volume of the sphere's bounding box, not just the surface of the sphere.</span></span>

## <a name="requirements"></a><span data-ttu-id="31801-126">Требования</span><span class="sxs-lookup"><span data-stu-id="31801-126">Requirements</span></span>



| <span data-ttu-id="31801-127">Требование</span><span class="sxs-lookup"><span data-stu-id="31801-127">Requirement</span></span> | <span data-ttu-id="31801-128">Значение</span><span class="sxs-lookup"><span data-stu-id="31801-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="31801-129">Header</span><span class="sxs-lookup"><span data-stu-id="31801-129">Header</span></span><br/>  | <dl> <span data-ttu-id="31801-130"><dt>D3DX10math. h</dt></span><span class="sxs-lookup"><span data-stu-id="31801-130"><dt>D3DX10math.h</dt></span></span> </dl> |
| <span data-ttu-id="31801-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="31801-131">Library</span></span><br/> | <dl> <span data-ttu-id="31801-132"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="31801-132"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="31801-133">См. также</span><span class="sxs-lookup"><span data-stu-id="31801-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31801-134">Функции сетки</span><span class="sxs-lookup"><span data-stu-id="31801-134">Mesh Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
