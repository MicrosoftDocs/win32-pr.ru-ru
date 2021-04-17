---
description: Определяет, пересекается ли луч с сеткой.
ms.assetid: 325f5b40-80ba-4400-a143-bae41146ab07
title: Функция D3DXIntersect (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXIntersect
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: dc877fb1301e01b05184625ba2e92a2c680cfa9f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703785"
---
# <a name="d3dxintersect-function"></a><span data-ttu-id="056a4-103">Функция D3DXIntersect</span><span class="sxs-lookup"><span data-stu-id="056a4-103">D3DXIntersect function</span></span>

<span data-ttu-id="056a4-104">Определяет, пересекается ли луч с сеткой.</span><span class="sxs-lookup"><span data-stu-id="056a4-104">Determines if a ray intersects with a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="056a4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="056a4-105">Syntax</span></span>


```C++
HRESULT D3DXIntersect(
  _In_        LPD3DXBASEMESH pMesh,
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



## <a name="parameters"></a><span data-ttu-id="056a4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="056a4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="056a4-107">*пмеш* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="056a4-107">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="056a4-108">Тип: **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**</span><span class="sxs-lookup"><span data-stu-id="056a4-108">Type: **[**LPD3DXBASEMESH**](id3dxbasemesh.md)**</span></span>

<span data-ttu-id="056a4-109">Указатель на интерфейс [**ID3DXBaseMesh**](id3dxbasemesh.md) , представляющий проверяемую сеть.</span><span class="sxs-lookup"><span data-stu-id="056a4-109">Pointer to an [**ID3DXBaseMesh**](id3dxbasemesh.md) interface, representing the mesh to be tested.</span></span>

</dd> <dt>

<span data-ttu-id="056a4-110">*прайпос* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="056a4-110">*pRayPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="056a4-111">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="056a4-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="056a4-112">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , указывающий точку, с которой начинается луч.</span><span class="sxs-lookup"><span data-stu-id="056a4-112">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the point where the ray begins.</span></span>

</dd> <dt>

<span data-ttu-id="056a4-113">*прайдир* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="056a4-113">*pRayDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="056a4-114">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="056a4-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="056a4-115">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , в которой указывается направление луча.</span><span class="sxs-lookup"><span data-stu-id="056a4-115">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, specifying the direction of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="056a4-116">*Фит* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="056a4-116">*pHit* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="056a4-117">Тип: **[ **bool** .](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="056a4-117">Type: **[**BOOL**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="056a4-118">Указатель на логическое значение.</span><span class="sxs-lookup"><span data-stu-id="056a4-118">Pointer to a BOOL.</span></span> <span data-ttu-id="056a4-119">Если луч пересекает треугольную грань в сетке, это значение будет равно **true**.</span><span class="sxs-lookup"><span data-stu-id="056a4-119">If the ray intersects a triangular face on the mesh, this value will be set to **TRUE**.</span></span> <span data-ttu-id="056a4-120">В противном случае это значение равно **false**.</span><span class="sxs-lookup"><span data-stu-id="056a4-120">Otherwise, this value is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="056a4-121">*пфацеиндекс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="056a4-121">*pFaceIndex* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="056a4-122">Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="056a4-122">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="056a4-123">Указатель на значение индекса стороны, ближайшее к началу луча, если Фит имеет **значение true**.</span><span class="sxs-lookup"><span data-stu-id="056a4-123">Pointer to an index value of the face closest to the ray origin, if pHit is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="056a4-124">*PU* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="056a4-124">*pU* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="056a4-125">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="056a4-125">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="056a4-126">Указатель на барицентрик координату нажатия, U.</span><span class="sxs-lookup"><span data-stu-id="056a4-126">Pointer to a barycentric hit coordinate, U.</span></span>

</dd> <dt>

<span data-ttu-id="056a4-127">*ПС* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="056a4-127">*pV* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="056a4-128">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="056a4-128">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="056a4-129">Указатель на барицентрик координату, V.</span><span class="sxs-lookup"><span data-stu-id="056a4-129">Pointer to a barycentric hit coordinate, V.</span></span>

</dd> <dt>

<span data-ttu-id="056a4-130">*пдист* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="056a4-130">*pDist* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="056a4-131">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="056a4-131">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="056a4-132">Указатель на расстояние с параметром пересечения лучей.</span><span class="sxs-lookup"><span data-stu-id="056a4-132">Pointer to a ray intersection parameter distance.</span></span>

</dd> <dt>

<span data-ttu-id="056a4-133">*ппаллхитс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="056a4-133">*ppAllHits* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="056a4-134">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="056a4-134">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="056a4-135">Указатель на объект [**ID3DXBuffer**](id3dxbuffer.md) , содержащий массив структур [**D3DXINTERSECTINFO**](d3dxintersectinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="056a4-135">Pointer to an [**ID3DXBuffer**](id3dxbuffer.md) object, containing an array of [**D3DXINTERSECTINFO**](d3dxintersectinfo.md) structures.</span></span>

</dd> <dt>

<span data-ttu-id="056a4-136">*пкаунтофхитс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="056a4-136">*pCountOfHits* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="056a4-137">Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="056a4-137">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="056a4-138">Указатель на DWORD, содержащий количество записей в массиве Ппаллхитс.</span><span class="sxs-lookup"><span data-stu-id="056a4-138">Pointer to a DWORD that contains the number of entries in the ppAllHits array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="056a4-139">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="056a4-139">Return value</span></span>

<span data-ttu-id="056a4-140">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="056a4-140">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="056a4-141">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="056a4-141">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="056a4-142">Если функция завершается ошибкой, возвращаемое значение может быть следующим: E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="056a4-142">If the function fails, the return value can be: E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="056a4-143">Комментарии</span><span class="sxs-lookup"><span data-stu-id="056a4-143">Remarks</span></span>

<span data-ttu-id="056a4-144">Функция **D3DXIntersect** предоставляет способ для понимания точек в треугольнике и вокруг него независимо от того, где фактически находится треугольник.</span><span class="sxs-lookup"><span data-stu-id="056a4-144">The **D3DXIntersect** function provides a way to understand points in and around a triangle, independent of where the triangle is actually located.</span></span> <span data-ttu-id="056a4-145">Эта функция возвращает результирующую точку, используя следующее уравнение: v1 + U (V2-v1) + V (v3-v1).</span><span class="sxs-lookup"><span data-stu-id="056a4-145">This function returns the resulting point by using the following equation: V1 + U(V2 - V1) + V(V3 - V1).</span></span>

<span data-ttu-id="056a4-146">Любая точка в плоскости V1V2V3 может быть представлена координатой барицентрик (U, V).</span><span class="sxs-lookup"><span data-stu-id="056a4-146">Any point in the plane V1V2V3 can be represented by the barycentric coordinate (U,V).</span></span> <span data-ttu-id="056a4-147">Параметр U управляет тем, сколько v2 имеет взвешенное значение в результате, а параметр V определяет, сколько будет иметь взвешенное значение v3 в результате.</span><span class="sxs-lookup"><span data-stu-id="056a4-147">The parameter U controls how much V2 gets weighted into the result, and the parameter V controls how much V3 gets weighted into the result.</span></span> <span data-ttu-id="056a4-148">Наконец, значение \[ 1 (U + V) \] определяет, сколько единиц измерения v1 будет взвешено по результату.</span><span class="sxs-lookup"><span data-stu-id="056a4-148">Lastly, the value of \[1 - (U + V)\] controls how much V1 gets weighted into the result.</span></span>

<span data-ttu-id="056a4-149">Координаты барицентрик — это форма общих координат.</span><span class="sxs-lookup"><span data-stu-id="056a4-149">Barycentric coordinates are a form of general coordinates.</span></span> <span data-ttu-id="056a4-150">В этом контексте использование координат барицентрик представляет собой изменение в системах координат.</span><span class="sxs-lookup"><span data-stu-id="056a4-150">In this context, using barycentric coordinates represents a change in coordinate systems.</span></span> <span data-ttu-id="056a4-151">Что содержит значение true для декартовых координат, имеет значение true для координат барицентрик.</span><span class="sxs-lookup"><span data-stu-id="056a4-151">What holds true for Cartesian coordinates holds true for barycentric coordinates.</span></span>

<span data-ttu-id="056a4-152">Координаты барицентрик определяют точку внутри треугольника с точки зрения вершин треугольника.</span><span class="sxs-lookup"><span data-stu-id="056a4-152">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="056a4-153">Более подробное описание координат барицентрик см. в разделе [Описание координат Барицентрик MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="056a4-153">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="056a4-154">Требования</span><span class="sxs-lookup"><span data-stu-id="056a4-154">Requirements</span></span>



| <span data-ttu-id="056a4-155">Требование</span><span class="sxs-lookup"><span data-stu-id="056a4-155">Requirement</span></span> | <span data-ttu-id="056a4-156">Значение</span><span class="sxs-lookup"><span data-stu-id="056a4-156">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="056a4-157">Header</span><span class="sxs-lookup"><span data-stu-id="056a4-157">Header</span></span><br/>  | <dl> <span data-ttu-id="056a4-158"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="056a4-158"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="056a4-159">Библиотека</span><span class="sxs-lookup"><span data-stu-id="056a4-159">Library</span></span><br/> | <dl> <span data-ttu-id="056a4-160"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="056a4-160"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="056a4-161">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="056a4-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="056a4-162">Функции сетки</span><span class="sxs-lookup"><span data-stu-id="056a4-162">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
