---
description: Пересекает указанный луч с заданным подмножеством сетки. Это обеспечивает аналогичную функциональность для D3DXIntersect.
ms.assetid: 4a757b9e-18eb-424e-9f3e-cdf917c23787
title: Функция D3DXIntersectSubset (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXIntersectSubset
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 621f45d7c2a6d8ff162f539ef62153d3ae70f6e9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273773"
---
# <a name="d3dxintersectsubset-function"></a><span data-ttu-id="07283-104">Функция D3DXIntersectSubset</span><span class="sxs-lookup"><span data-stu-id="07283-104">D3DXIntersectSubset function</span></span>

<span data-ttu-id="07283-105">Пересекает указанный луч с заданным подмножеством сетки.</span><span class="sxs-lookup"><span data-stu-id="07283-105">Intersects the specified ray with the given mesh subset.</span></span> <span data-ttu-id="07283-106">Это обеспечивает аналогичную функциональность для [**D3DXIntersect**](d3dxintersect.md).</span><span class="sxs-lookup"><span data-stu-id="07283-106">This provides similar functionality to [**D3DXIntersect**](d3dxintersect.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="07283-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="07283-107">Syntax</span></span>


```C++
HRESULT D3DXIntersectSubset(
  _In_        LPD3DXBASEMESH pMesh,
  _In_        DWORD          AttribId,
  _In_  const D3DXVECTOR3    *pRayPos,
  _In_  const D3DXVECTOR3    *pRayDir,
  _Out_       BOOL           *pHit,
  _Out_       DWORD          *pFaceIndex,
  _Out_       FLOAT          *pU,
  _Out_       FLOAT          *pV,
  _Out_       FLOAT          *pDist,
  _Out_       LPD3DXBUFFER   *ppAllHits,
  _Out_       DWORD          *pCountOfHits
);
```



## <a name="parameters"></a><span data-ttu-id="07283-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="07283-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07283-109">*пмеш* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="07283-109">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07283-110">Тип: **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**</span><span class="sxs-lookup"><span data-stu-id="07283-110">Type: **[**LPD3DXBASEMESH**](id3dxbasemesh.md)**</span></span>

<span data-ttu-id="07283-111">Указатель на интерфейс [**ID3DXBaseMesh**](id3dxbasemesh.md) , представляющий проверяемую сеть.</span><span class="sxs-lookup"><span data-stu-id="07283-111">Pointer to an [**ID3DXBaseMesh**](id3dxbasemesh.md) interface, representing the mesh to be tested.</span></span> <span data-ttu-id="07283-112">Сетка должна быть отсортирована по атрибуту.</span><span class="sxs-lookup"><span data-stu-id="07283-112">The mesh must be attribute sorted.</span></span>

</dd> <dt>

<span data-ttu-id="07283-113">*Аттрибид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="07283-113">*AttribId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07283-114">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="07283-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="07283-115">Идентификатор атрибута подмножества, которое необходимо пересекать с.</span><span class="sxs-lookup"><span data-stu-id="07283-115">Attribute identifier of the subset to intersect with.</span></span>

</dd> <dt>

<span data-ttu-id="07283-116">*прайпос* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="07283-116">*pRayPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07283-117">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="07283-117">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="07283-118">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , указывающий точку, с которой начинается луч.</span><span class="sxs-lookup"><span data-stu-id="07283-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the point where the ray begins.</span></span>

</dd> <dt>

<span data-ttu-id="07283-119">*прайдир* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="07283-119">*pRayDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07283-120">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="07283-120">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="07283-121">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , в которой указывается направление луча.</span><span class="sxs-lookup"><span data-stu-id="07283-121">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the direction of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="07283-122">*Фит* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="07283-122">*pHit* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="07283-123">Тип: **[ **bool** .](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="07283-123">Type: **[**BOOL**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="07283-124">Указатель на логическое значение.</span><span class="sxs-lookup"><span data-stu-id="07283-124">Pointer to a BOOL.</span></span> <span data-ttu-id="07283-125">Если луч пересекает треугольную грань в сетке, это значение будет равно **true**.</span><span class="sxs-lookup"><span data-stu-id="07283-125">If the ray intersects a triangular face on the mesh, this value will be set to **TRUE**.</span></span> <span data-ttu-id="07283-126">В противном случае это значение равно **false**.</span><span class="sxs-lookup"><span data-stu-id="07283-126">Otherwise, this value is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="07283-127">*пфацеиндекс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="07283-127">*pFaceIndex* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="07283-128">Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="07283-128">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="07283-129">Указатель на значение индекса стороны, ближайшее к началу луча, если Фит имеет **значение true**.</span><span class="sxs-lookup"><span data-stu-id="07283-129">Pointer to an index value of the face closest to the ray origin, if pHit is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="07283-130">*PU* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="07283-130">*pU* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="07283-131">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="07283-131">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="07283-132">Указатель на барицентрик координату нажатия, U.</span><span class="sxs-lookup"><span data-stu-id="07283-132">Pointer to a barycentric hit coordinate, U.</span></span>

</dd> <dt>

<span data-ttu-id="07283-133">*ПС* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="07283-133">*pV* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="07283-134">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="07283-134">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="07283-135">Указатель на барицентрик координату, V.</span><span class="sxs-lookup"><span data-stu-id="07283-135">Pointer to a barycentric hit coordinate, V.</span></span>

</dd> <dt>

<span data-ttu-id="07283-136">*пдист* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="07283-136">*pDist* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="07283-137">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="07283-137">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="07283-138">Указатель на расстояние с параметром пересечения лучей.</span><span class="sxs-lookup"><span data-stu-id="07283-138">Pointer to a ray intersection parameter distance.</span></span>

</dd> <dt>

<span data-ttu-id="07283-139">*ппаллхитс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="07283-139">*ppAllHits* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="07283-140">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="07283-140">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="07283-141">Массив структур [**D3DXINTERSECTINFO**](d3dxintersectinfo.md) , представляющий все попадания, а не только ближайшие.</span><span class="sxs-lookup"><span data-stu-id="07283-141">Array of [**D3DXINTERSECTINFO**](d3dxintersectinfo.md) structures, representing all hits, not just closest hits.</span></span>

</dd> <dt>

<span data-ttu-id="07283-142">*пкаунтофхитс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="07283-142">*pCountOfHits* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="07283-143">Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="07283-143">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="07283-144">Число элементов в массиве, возвращаемых из Ппаллхитс.</span><span class="sxs-lookup"><span data-stu-id="07283-144">Number of elements in the array returned from ppAllHits.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07283-145">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="07283-145">Return value</span></span>

<span data-ttu-id="07283-146">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="07283-146">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="07283-147">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="07283-147">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="07283-148">Если функция завершается ошибкой, возвращаемое значение может иметь следующее значение: E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="07283-148">If the function fails, the return value can be the following value: E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="07283-149">Комментарии</span><span class="sxs-lookup"><span data-stu-id="07283-149">Remarks</span></span>

<span data-ttu-id="07283-150">Функция **D3DXIntersectSubset** предоставляет способ для понимания точек в треугольнике и вокруг него независимо от того, где фактически находится треугольник.</span><span class="sxs-lookup"><span data-stu-id="07283-150">The **D3DXIntersectSubset** function provides a way to understand points in and around a triangle, independent of where the triangle is actually located.</span></span> <span data-ttu-id="07283-151">Эта функция возвращает результирующую точку, используя следующее уравнение: v1 + U (V2-v1) + V (v3-v1).</span><span class="sxs-lookup"><span data-stu-id="07283-151">This function returns the resulting point by using the following equation: V1 + U(V2 - V1) + V(V3 - V1).</span></span>

<span data-ttu-id="07283-152">Любая точка в плоскости V1V2V3 может быть представлена координатой барицентрик (U, V).</span><span class="sxs-lookup"><span data-stu-id="07283-152">Any point in the plane V1V2V3 can be represented by the barycentric coordinate (U,V).</span></span> <span data-ttu-id="07283-153">Параметр U управляет тем, сколько v2 имеет взвешенный результат, а параметр V определяет, сколько будет иметь взвешенное значение v3 в результате.</span><span class="sxs-lookup"><span data-stu-id="07283-153">The parameter U controls how much V2 gets weighted into the result and the parameter V controls how much V3 gets weighted into the result.</span></span> <span data-ttu-id="07283-154">Наконец, значение \[ 1 (U + V) \] определяет, сколько единиц измерения v1 будет взвешено по результату.</span><span class="sxs-lookup"><span data-stu-id="07283-154">Lastly, the value of \[1 - (U + V)\] controls how much V1 gets weighted into the result.</span></span>

<span data-ttu-id="07283-155">Координаты барицентрик — это форма общих координат.</span><span class="sxs-lookup"><span data-stu-id="07283-155">Barycentric coordinates are a form of general coordinates.</span></span> <span data-ttu-id="07283-156">В этом контексте использование координат барицентрик представляет собой изменение в системах координат.</span><span class="sxs-lookup"><span data-stu-id="07283-156">In this context, using barycentric coordinates represents a change in coordinate systems.</span></span> <span data-ttu-id="07283-157">Что содержит значение true для декартовых координат, имеет значение true для координат барицентрик.</span><span class="sxs-lookup"><span data-stu-id="07283-157">What holds true for Cartesian coordinates holds true for barycentric coordinates.</span></span>

<span data-ttu-id="07283-158">Координаты барицентрик определяют точку внутри треугольника с точки зрения вершин треугольника.</span><span class="sxs-lookup"><span data-stu-id="07283-158">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="07283-159">Более подробное описание координат барицентрик см. в разделе [Описание координат Барицентрик MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="07283-159">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="07283-160">Требования</span><span class="sxs-lookup"><span data-stu-id="07283-160">Requirements</span></span>



| <span data-ttu-id="07283-161">Требование</span><span class="sxs-lookup"><span data-stu-id="07283-161">Requirement</span></span> | <span data-ttu-id="07283-162">Значение</span><span class="sxs-lookup"><span data-stu-id="07283-162">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="07283-163">Header</span><span class="sxs-lookup"><span data-stu-id="07283-163">Header</span></span><br/>  | <dl> <span data-ttu-id="07283-164"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="07283-164"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="07283-165">Библиотека</span><span class="sxs-lookup"><span data-stu-id="07283-165">Library</span></span><br/> | <dl> <span data-ttu-id="07283-166"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="07283-166"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="07283-167">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="07283-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07283-168">Функции сетки</span><span class="sxs-lookup"><span data-stu-id="07283-168">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
