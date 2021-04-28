---
description: Функция D3DXIntersectTri (D3DX10math. h) — вычисление пересечения луча и треугольника.
ms.assetid: 819f2543-8046-47c9-93b8-7d888264786f
title: Функция D3DXIntersectTri (D3DX10math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXIntersectTri
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c8bf502cca48701a7d71a083e515f9988cafe303
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113242"
---
# <a name="d3dxintersecttri-function-d3dx10mathh"></a><span data-ttu-id="d6912-103">Функция D3DXIntersectTri (D3DX10math. h)</span><span class="sxs-lookup"><span data-stu-id="d6912-103">D3DXIntersectTri function (D3DX10math.h)</span></span>

<span data-ttu-id="d6912-104">Вычисление пересечения луча и треугольника.</span><span class="sxs-lookup"><span data-stu-id="d6912-104">Computes the intersection of a ray and a triangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6912-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d6912-105">Syntax</span></span>


```C++
BOOL D3DXIntersectTri(
  _In_  const D3DXVECTOR3 *p0,
  _In_  const D3DXVECTOR3 *p1,
  _In_  const D3DXVECTOR3 *p2,
  _In_  const D3DXVECTOR3 *pRayPos,
  _In_  const D3DXVECTOR3 *pRayDir,
  _Out_       FLOAT       *pU,
  _Out_       FLOAT       *pV,
  _Out_       FLOAT       *pDist
);
```



## <a name="parameters"></a><span data-ttu-id="d6912-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d6912-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6912-107">*P0* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d6912-107">*p0* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6912-108">Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="d6912-108">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="d6912-109">Указатель на структуру [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , описывающий первую точку вершинного треугольника.</span><span class="sxs-lookup"><span data-stu-id="d6912-109">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, describing the first triangle vertex position.</span></span>

</dd> <dt>

<span data-ttu-id="d6912-110">*P1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d6912-110">*p1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6912-111">Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="d6912-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="d6912-112">Указатель на структуру [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , описывающий вторую точку вершинного треугольника.</span><span class="sxs-lookup"><span data-stu-id="d6912-112">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, describing the second triangle vertex position.</span></span>

</dd> <dt>

<span data-ttu-id="d6912-113">*P2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d6912-113">*p2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6912-114">Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="d6912-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="d6912-115">Указатель на структуру [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , описывающий третье расположение вершины треугольника.</span><span class="sxs-lookup"><span data-stu-id="d6912-115">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, describing the third triangle vertex position.</span></span>

</dd> <dt>

<span data-ttu-id="d6912-116">*прайпос* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d6912-116">*pRayPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6912-117">Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="d6912-117">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="d6912-118">Указатель на структуру [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , указывающий точку, с которой начинается луч.</span><span class="sxs-lookup"><span data-stu-id="d6912-118">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, specifying the point where the ray begins.</span></span>

</dd> <dt>

<span data-ttu-id="d6912-119">*прайдир* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d6912-119">*pRayDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6912-120">Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="d6912-120">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="d6912-121">Указатель на структуру [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , в которой указывается направление луча.</span><span class="sxs-lookup"><span data-stu-id="d6912-121">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, specifying the direction of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="d6912-122">*PU* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d6912-122">*pU* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d6912-123">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="d6912-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d6912-124">Барицентрик координаты нажатия, U.</span><span class="sxs-lookup"><span data-stu-id="d6912-124">Barycentric hit coordinates, U.</span></span>

</dd> <dt>

<span data-ttu-id="d6912-125">*ПС* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d6912-125">*pV* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d6912-126">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="d6912-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d6912-127">Барицентрик координаты точки останова, V.</span><span class="sxs-lookup"><span data-stu-id="d6912-127">Barycentric hit coordinates, V.</span></span>

</dd> <dt>

<span data-ttu-id="d6912-128">*пдист* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d6912-128">*pDist* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d6912-129">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="d6912-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d6912-130">Расстояние для параметра пересечения лучей.</span><span class="sxs-lookup"><span data-stu-id="d6912-130">Ray-intersection parameter distance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6912-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d6912-131">Return value</span></span>

<span data-ttu-id="d6912-132">Тип: **[ **bool** .](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d6912-132">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d6912-133">Возвращает **значение true** , если луч пересекает область треугольника.</span><span class="sxs-lookup"><span data-stu-id="d6912-133">Returns **TRUE** if the ray intersects the area of the triangle.</span></span> <span data-ttu-id="d6912-134">В противном случае возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="d6912-134">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6912-135">Remarks</span><span class="sxs-lookup"><span data-stu-id="d6912-135">Remarks</span></span>

<span data-ttu-id="d6912-136">Любая точка в плоскости V1V2V3 может быть представлена координатой барицентрик (U, V).</span><span class="sxs-lookup"><span data-stu-id="d6912-136">Any point in the plane V1V2V3 can be represented by the barycentric coordinate (U,V).</span></span> <span data-ttu-id="d6912-137">Параметр U управляет тем, сколько v2 имеет взвешенное значение в результате, а параметр V определяет, сколько будет иметь взвешенное значение v3 в результате.</span><span class="sxs-lookup"><span data-stu-id="d6912-137">The parameter U controls how much V2 gets weighted into the result, and the parameter V controls how much V3 gets weighted into the result.</span></span> <span data-ttu-id="d6912-138">Наконец, значение \[ 1 (U + V) \] определяет, сколько единиц измерения v1 будет взвешено по результату.</span><span class="sxs-lookup"><span data-stu-id="d6912-138">Lastly, the value of \[1 - (U + V)\] controls how much V1 gets weighted into the result.</span></span>

<span data-ttu-id="d6912-139">Координаты барицентрик — это форма общих координат.</span><span class="sxs-lookup"><span data-stu-id="d6912-139">Barycentric coordinates are a form of general coordinates.</span></span> <span data-ttu-id="d6912-140">В этом контексте использование координат барицентрик представляет собой изменение в системах координат.</span><span class="sxs-lookup"><span data-stu-id="d6912-140">In this context, using barycentric coordinates represents a change in coordinate systems.</span></span> <span data-ttu-id="d6912-141">Что содержит значение true для декартовых координат, имеет значение true для координат барицентрик.</span><span class="sxs-lookup"><span data-stu-id="d6912-141">What holds true for Cartesian coordinates holds true for barycentric coordinates.</span></span>

<span data-ttu-id="d6912-142">Координаты барицентрик определяют точку внутри треугольника с точки зрения вершин треугольника.</span><span class="sxs-lookup"><span data-stu-id="d6912-142">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="d6912-143">Более подробное описание координат барицентрик см. в разделе [Описание координат Барицентрик MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="d6912-143">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="d6912-144">Требования</span><span class="sxs-lookup"><span data-stu-id="d6912-144">Requirements</span></span>



| <span data-ttu-id="d6912-145">Требование</span><span class="sxs-lookup"><span data-stu-id="d6912-145">Requirement</span></span> | <span data-ttu-id="d6912-146">Значение</span><span class="sxs-lookup"><span data-stu-id="d6912-146">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d6912-147">Header</span><span class="sxs-lookup"><span data-stu-id="d6912-147">Header</span></span><br/>  | <dl> <span data-ttu-id="d6912-148"><dt>D3DX10math. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6912-148"><dt>D3DX10math.h</dt></span></span> </dl> |
| <span data-ttu-id="d6912-149">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d6912-149">Library</span></span><br/> | <dl> <span data-ttu-id="d6912-150"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d6912-150"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d6912-151">См. также</span><span class="sxs-lookup"><span data-stu-id="d6912-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6912-152">Функции сетки</span><span class="sxs-lookup"><span data-stu-id="d6912-152">Mesh Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
