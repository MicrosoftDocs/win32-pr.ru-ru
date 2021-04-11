---
description: Использует эффективную трассировку лучей в предварительно вычисленном моделировании радианце (PRT), чтобы определить, пересекаются ли луч с сеткой.
ms.assetid: e506aed3-bf14-4f29-845b-2091f5b00950
title: 'Метод ID3DXPRTEngine:: Клосестрайинтерсектс (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ClosestRayIntersects
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4fd802f636077c9ec2a9f0f1060ffd43493aabf1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273937"
---
# <a name="id3dxprtengineclosestrayintersects-method"></a><span data-ttu-id="25dfa-103">Метод ID3DXPRTEngine:: Клосестрайинтерсектс</span><span class="sxs-lookup"><span data-stu-id="25dfa-103">ID3DXPRTEngine::ClosestRayIntersects method</span></span>

<span data-ttu-id="25dfa-104">Использует эффективную трассировку лучей в предварительно вычисленном моделировании радианце (PRT), чтобы определить, пересекаются ли луч с сеткой.</span><span class="sxs-lookup"><span data-stu-id="25dfa-104">Uses efficient ray-tracing in precomputed radiance transfer (PRT) simulations to determine whether a ray intersects a mesh.</span></span> <span data-ttu-id="25dfa-105">Если пересечение обнаружено, метод возвращает индекс ближайшей грани сетки, которая достигнута лучом, и координатами барицентрик точки пересечения.</span><span class="sxs-lookup"><span data-stu-id="25dfa-105">If an intersection is found, the method returns the index of the closest mesh face hit by the ray and the barycentric coordinates of the intersection point.</span></span>

## <a name="syntax"></a><span data-ttu-id="25dfa-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="25dfa-106">Syntax</span></span>


```C++
BOOL ClosestRayIntersects(
  [in]  const D3DXVECTOR3 *pRayPos,
  [in]  const D3DXVECTOR3 *pRayDir,
  [in]        DWORD       *pFaceIndex,
  [out]       FLOAT       *pU,
  [out]       FLOAT       *pV,
  [out]       FLOAT       *pDist
);
```



## <a name="parameters"></a><span data-ttu-id="25dfa-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="25dfa-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25dfa-108">*прайпос* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="25dfa-108">*pRayPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25dfa-109">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="25dfa-109">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="25dfa-110">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , указывающий точку, с которой начинается луч.</span><span class="sxs-lookup"><span data-stu-id="25dfa-110">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the point where the ray begins.</span></span>

</dd> <dt>

<span data-ttu-id="25dfa-111">*прайдир* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="25dfa-111">*pRayDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25dfa-112">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="25dfa-112">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="25dfa-113">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , в которой указывается нормализованное направление луча.</span><span class="sxs-lookup"><span data-stu-id="25dfa-113">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the normalized direction of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="25dfa-114">*пфацеиндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="25dfa-114">*pFaceIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25dfa-115">Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="25dfa-115">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="25dfa-116">Указатель на индекс текущей грани сетки, который первым помещается на данный луч, на основе стека всех граней в сетке, расположенных перед текущей сеткой.</span><span class="sxs-lookup"><span data-stu-id="25dfa-116">Pointer to the index of the current mesh face that is first hit by the given ray, based upon stacking all blocker mesh faces in front of the current mesh.</span></span>

</dd> <dt>

<span data-ttu-id="25dfa-117">*PU* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="25dfa-117">*pU* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="25dfa-118">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="25dfa-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="25dfa-119">Указатель на барицентрик координату, U, для вершины 0 треугольника.</span><span class="sxs-lookup"><span data-stu-id="25dfa-119">Pointer to a barycentric hit coordinate, U, for vertex 0 of the triangle.</span></span>

</dd> <dt>

<span data-ttu-id="25dfa-120">*ПС* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="25dfa-120">*pV* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="25dfa-121">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="25dfa-121">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="25dfa-122">Указатель на барицентрик координату, V, для вершины 1 треугольника.</span><span class="sxs-lookup"><span data-stu-id="25dfa-122">Pointer to a barycentric hit coordinate, V, for vertex 1 of the triangle.</span></span>

</dd> <dt>

<span data-ttu-id="25dfa-123">*пдист* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="25dfa-123">*pDist* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="25dfa-124">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="25dfa-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="25dfa-125">Указатель на расстояние точки пересечения вдоль луча.</span><span class="sxs-lookup"><span data-stu-id="25dfa-125">Pointer to the distance of the intersection point along the ray.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25dfa-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="25dfa-126">Return value</span></span>

<span data-ttu-id="25dfa-127">Тип: **[ **bool** .](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="25dfa-127">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="25dfa-128">Возвращает **значение true** , если луч пересекает текущую сетку; в противном случае возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="25dfa-128">Returns **TRUE** if the ray intersects the current mesh; otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="25dfa-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="25dfa-129">Remarks</span></span>

<span data-ttu-id="25dfa-130">Используйте [**ID3DXPRTEngine:: сетминмаксинтерсектион**](id3dxprtengine--setminmaxintersection.md) , чтобы задать минимальное и максимальное расстояние пересечения с лучом.</span><span class="sxs-lookup"><span data-stu-id="25dfa-130">Use [**ID3DXPRTEngine::SetMinMaxIntersection**](id3dxprtengine--setminmaxintersection.md) to set minimum and maximum distances of intersection with the ray.</span></span>

<span data-ttu-id="25dfa-131">Координата барицентрик третьей вершины (вершина 2) треугольника — 1 (U + V).</span><span class="sxs-lookup"><span data-stu-id="25dfa-131">The barycentric coordinate of the third vertex (vertex 2) of the triangle is 1 - ( U + V ).</span></span>

<span data-ttu-id="25dfa-132">Этот метод выполняется медленнее, чем [**ID3DXPRTEngine:: шадоврайинтерсектс**](id3dxprtengine--shadowrayintersects.md).</span><span class="sxs-lookup"><span data-stu-id="25dfa-132">This method executes slower than [**ID3DXPRTEngine::ShadowRayIntersects**](id3dxprtengine--shadowrayintersects.md).</span></span> <span data-ttu-id="25dfa-133">Используйте **ID3DXPRTEngine:: шадоврайинтерсектс** , если расположение точки пересечения не требуется.</span><span class="sxs-lookup"><span data-stu-id="25dfa-133">Use **ID3DXPRTEngine::ShadowRayIntersects** if the location of the intersection point is not needed.</span></span>

<span data-ttu-id="25dfa-134">Координаты барицентрик определяют точку внутри треугольника с точки зрения вершин треугольника.</span><span class="sxs-lookup"><span data-stu-id="25dfa-134">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="25dfa-135">Более подробное описание координат барицентрик см. в разделе [Описание координат Барицентрик MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="25dfa-135">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="25dfa-136">Требования</span><span class="sxs-lookup"><span data-stu-id="25dfa-136">Requirements</span></span>



| <span data-ttu-id="25dfa-137">Требование</span><span class="sxs-lookup"><span data-stu-id="25dfa-137">Requirement</span></span> | <span data-ttu-id="25dfa-138">Значение</span><span class="sxs-lookup"><span data-stu-id="25dfa-138">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="25dfa-139">Header</span><span class="sxs-lookup"><span data-stu-id="25dfa-139">Header</span></span><br/>  | <dl> <span data-ttu-id="25dfa-140"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="25dfa-140"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="25dfa-141">Библиотека</span><span class="sxs-lookup"><span data-stu-id="25dfa-141">Library</span></span><br/> | <dl> <span data-ttu-id="25dfa-142"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="25dfa-142"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="25dfa-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="25dfa-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25dfa-144">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="25dfa-144">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="25dfa-145">**ID3DXPRTEngine:: Шадоврайинтерсектс**</span><span class="sxs-lookup"><span data-stu-id="25dfa-145">**ID3DXPRTEngine::ShadowRayIntersects**</span></span>](id3dxprtengine--shadowrayintersects.md)
</dt> <dt>

[<span data-ttu-id="25dfa-146">**ID3DXPRTEngine:: Сетминмаксинтерсектион**</span><span class="sxs-lookup"><span data-stu-id="25dfa-146">**ID3DXPRTEngine::SetMinMaxIntersection**</span></span>](id3dxprtengine--setminmaxintersection.md)
</dt> </dl>

 

 
