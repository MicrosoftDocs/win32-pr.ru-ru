---
description: Функция D3DXIntersectTri (D3DX9Mesh. h) — вычисление пересечения луча и треугольника.
ms.assetid: f335a71d-7203-4ea1-a6bf-407b28c712e6
title: Функция D3DXIntersectTri (D3DX9Mesh. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 33d45beda51a7a2c80debafbab864c2accb33653
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098272"
---
# <a name="d3dxintersecttri-function-d3dx9meshh"></a><span data-ttu-id="05fea-103">Функция D3DXIntersectTri (D3DX9Mesh. h)</span><span class="sxs-lookup"><span data-stu-id="05fea-103">D3DXIntersectTri function (D3DX9Mesh.h)</span></span>

<span data-ttu-id="05fea-104">Вычисление пересечения луча и треугольника.</span><span class="sxs-lookup"><span data-stu-id="05fea-104">Computes the intersection of a ray and a triangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="05fea-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="05fea-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="05fea-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="05fea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05fea-107">*P0* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="05fea-107">*p0* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05fea-108">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="05fea-108">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="05fea-109">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , описывающий первую точку вершинного треугольника.</span><span class="sxs-lookup"><span data-stu-id="05fea-109">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, describing the first triangle vertex position.</span></span>

</dd> <dt>

<span data-ttu-id="05fea-110">*P1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="05fea-110">*p1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05fea-111">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="05fea-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="05fea-112">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , описывающий вторую точку вершинного треугольника.</span><span class="sxs-lookup"><span data-stu-id="05fea-112">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, describing the second triangle vertex position.</span></span>

</dd> <dt>

<span data-ttu-id="05fea-113">*P2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="05fea-113">*p2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05fea-114">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="05fea-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="05fea-115">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , описывающий третье расположение вершины треугольника.</span><span class="sxs-lookup"><span data-stu-id="05fea-115">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, describing the third triangle vertex position.</span></span>

</dd> <dt>

<span data-ttu-id="05fea-116">*прайпос* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="05fea-116">*pRayPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05fea-117">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="05fea-117">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="05fea-118">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , указывающий точку, с которой начинается луч.</span><span class="sxs-lookup"><span data-stu-id="05fea-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the point where the ray begins.</span></span>

</dd> <dt>

<span data-ttu-id="05fea-119">*прайдир* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="05fea-119">*pRayDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05fea-120">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="05fea-120">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="05fea-121">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , в которой указывается направление луча.</span><span class="sxs-lookup"><span data-stu-id="05fea-121">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the direction of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="05fea-122">*PU* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="05fea-122">*pU* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="05fea-123">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="05fea-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="05fea-124">Барицентрик координаты нажатия, U.</span><span class="sxs-lookup"><span data-stu-id="05fea-124">Barycentric hit coordinates, U.</span></span>

</dd> <dt>

<span data-ttu-id="05fea-125">*ПС* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="05fea-125">*pV* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="05fea-126">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="05fea-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="05fea-127">Барицентрик координаты точки останова, V.</span><span class="sxs-lookup"><span data-stu-id="05fea-127">Barycentric hit coordinates, V.</span></span>

</dd> <dt>

<span data-ttu-id="05fea-128">*пдист* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="05fea-128">*pDist* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="05fea-129">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="05fea-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="05fea-130">Расстояние для параметра пересечения лучей.</span><span class="sxs-lookup"><span data-stu-id="05fea-130">Ray-intersection parameter distance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05fea-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="05fea-131">Return value</span></span>

<span data-ttu-id="05fea-132">Тип: **[ **bool** .](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="05fea-132">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="05fea-133">Возвращает **значение true** , если луч пересекает область треугольника.</span><span class="sxs-lookup"><span data-stu-id="05fea-133">Returns **TRUE** if the ray intersects the area of the triangle.</span></span> <span data-ttu-id="05fea-134">В противном случае возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="05fea-134">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="05fea-135">Remarks</span><span class="sxs-lookup"><span data-stu-id="05fea-135">Remarks</span></span>

<span data-ttu-id="05fea-136">Функция [**D3DXIntersect**](d3dxintersect.md) предоставляет способ для понимания точек в треугольнике и вокруг него независимо от того, где фактически находится треугольник.</span><span class="sxs-lookup"><span data-stu-id="05fea-136">The [**D3DXIntersect**](d3dxintersect.md) function provides a way to understand points in and around a triangle, independent of where the triangle is actually located.</span></span> <span data-ttu-id="05fea-137">Эта функция возвращает результирующую точку, используя следующее уравнение: v1 + U (V2-v1) + V (v3-v1).</span><span class="sxs-lookup"><span data-stu-id="05fea-137">This function returns the resulting point by using the following equation: V1 + U(V2 - V1) + V(V3 - V1).</span></span>

<span data-ttu-id="05fea-138">Любая точка в плоскости V1V2V3 может быть представлена координатой барицентрик (U, V).</span><span class="sxs-lookup"><span data-stu-id="05fea-138">Any point in the plane V1V2V3 can be represented by the barycentric coordinate (U,V).</span></span> <span data-ttu-id="05fea-139">Параметр U управляет тем, сколько v2 имеет взвешенное значение в результате, а параметр V определяет, сколько будет иметь взвешенное значение v3 в результате.</span><span class="sxs-lookup"><span data-stu-id="05fea-139">The parameter U controls how much V2 gets weighted into the result, and the parameter V controls how much V3 gets weighted into the result.</span></span> <span data-ttu-id="05fea-140">Наконец, значение \[ 1 (U + V) \] определяет, сколько единиц измерения v1 будет взвешено по результату.</span><span class="sxs-lookup"><span data-stu-id="05fea-140">Lastly, the value of \[1 - (U + V)\] controls how much V1 gets weighted into the result.</span></span>

<span data-ttu-id="05fea-141">Координаты барицентрик — это форма общих координат.</span><span class="sxs-lookup"><span data-stu-id="05fea-141">Barycentric coordinates are a form of general coordinates.</span></span> <span data-ttu-id="05fea-142">В этом контексте использование координат барицентрик представляет собой изменение в системах координат.</span><span class="sxs-lookup"><span data-stu-id="05fea-142">In this context, using barycentric coordinates represents a change in coordinate systems.</span></span> <span data-ttu-id="05fea-143">Что содержит значение true для декартовых координат, имеет значение true для координат барицентрик.</span><span class="sxs-lookup"><span data-stu-id="05fea-143">What holds true for Cartesian coordinates holds true for barycentric coordinates.</span></span>

<span data-ttu-id="05fea-144">Координаты барицентрик определяют точку внутри треугольника с точки зрения вершин треугольника.</span><span class="sxs-lookup"><span data-stu-id="05fea-144">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="05fea-145">Более подробное описание координат барицентрик см. в разделе [Описание координат Барицентрик MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="05fea-145">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="05fea-146">Требования</span><span class="sxs-lookup"><span data-stu-id="05fea-146">Requirements</span></span>



| <span data-ttu-id="05fea-147">Требование</span><span class="sxs-lookup"><span data-stu-id="05fea-147">Requirement</span></span> | <span data-ttu-id="05fea-148">Значение</span><span class="sxs-lookup"><span data-stu-id="05fea-148">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="05fea-149">Header</span><span class="sxs-lookup"><span data-stu-id="05fea-149">Header</span></span><br/>  | <dl> <span data-ttu-id="05fea-150"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="05fea-150"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="05fea-151">Библиотека</span><span class="sxs-lookup"><span data-stu-id="05fea-151">Library</span></span><br/> | <dl> <span data-ttu-id="05fea-152"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="05fea-152"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="05fea-153">См. также</span><span class="sxs-lookup"><span data-stu-id="05fea-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05fea-154">Функции сетки</span><span class="sxs-lookup"><span data-stu-id="05fea-154">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
