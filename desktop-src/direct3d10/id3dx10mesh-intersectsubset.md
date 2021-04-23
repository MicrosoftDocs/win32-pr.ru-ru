---
description: Определяет, пересекается ли луч с подмножеством этой сетки.
ms.assetid: 31f90141-60be-4c7f-8d6a-a1a97ff26d9d
title: Метод ID3DX10Mesh::IntersectSubset (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.IntersectSubset
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a08d4db92dc75f40d0073367dda9a9ea26863418
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273877"
---
# <a name="id3dx10meshintersectsubset-method"></a><span data-ttu-id="04507-103">Метод ID3DX10Mesh:: Интерсектсубсет</span><span class="sxs-lookup"><span data-stu-id="04507-103">ID3DX10Mesh::IntersectSubset method</span></span>

<span data-ttu-id="04507-104">Определяет, пересекается ли луч с подмножеством этой сетки.</span><span class="sxs-lookup"><span data-stu-id="04507-104">Determines if a ray intersects with a subset of this mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="04507-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="04507-105">Syntax</span></span>


```C++
HRESULT IntersectSubset(
  [in]  UINT        AttribId,
  [in]  D3DXVECTOR3 *pRayPos,
  [in]  D3DXVECTOR3 *pRayDir,
  [in]  UINT        *pHitCount,
  [in]  UINT        *pFaceIndex,
  [in]  float       *pU,
  [in]  float       *pV,
  [in]  float       *pDist,
  [out] ID3D10Blob  **ppAllHits
);
```



## <a name="parameters"></a><span data-ttu-id="04507-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="04507-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04507-107">*Аттрибид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="04507-107">*AttribId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04507-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="04507-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="04507-109">Идентификатор атрибута, определяющий подмножество сетки.</span><span class="sxs-lookup"><span data-stu-id="04507-109">Attribute ID identifying the subset of the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="04507-110">*прайпос* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="04507-110">*pRayPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04507-111">Тип: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="04507-111">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="04507-112">Указатель на структуру [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , указывающий точку, с которой начинается луч.</span><span class="sxs-lookup"><span data-stu-id="04507-112">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, specifying the point where the ray begins.</span></span>

</dd> <dt>

<span data-ttu-id="04507-113">*прайдир* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="04507-113">*pRayDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04507-114">Тип: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="04507-114">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="04507-115">Указатель на структуру [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , в которой указывается направление луча.</span><span class="sxs-lookup"><span data-stu-id="04507-115">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, specifying the direction of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="04507-116">*фиткаунт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="04507-116">*pHitCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04507-117">Тип: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="04507-117">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="04507-118">Количество раз, когда луч пересекается с сеткой.</span><span class="sxs-lookup"><span data-stu-id="04507-118">The number of times the ray intersected with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="04507-119">*пфацеиндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="04507-119">*pFaceIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04507-120">Тип: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="04507-120">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="04507-121">Указатель на значение индекса стороны, ближайшее к началу луча, если Фит имеет **значение true**.</span><span class="sxs-lookup"><span data-stu-id="04507-121">Pointer to an index value of the face closest to the ray origin, if pHit is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="04507-122">*PU* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="04507-122">*pU* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04507-123">Тип: **float \***</span><span class="sxs-lookup"><span data-stu-id="04507-123">Type: **float\***</span></span>

<span data-ttu-id="04507-124">Указатель на барицентрик координату нажатия, U.</span><span class="sxs-lookup"><span data-stu-id="04507-124">Pointer to a barycentric hit coordinate, U.</span></span>

</dd> <dt>

<span data-ttu-id="04507-125">*ПС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="04507-125">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04507-126">Тип: **float \***</span><span class="sxs-lookup"><span data-stu-id="04507-126">Type: **float\***</span></span>

<span data-ttu-id="04507-127">Указатель на барицентрик координату, V.</span><span class="sxs-lookup"><span data-stu-id="04507-127">Pointer to a barycentric hit coordinate, V.</span></span>

</dd> <dt>

<span data-ttu-id="04507-128">*пдист* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="04507-128">*pDist* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04507-129">Тип: **float \***</span><span class="sxs-lookup"><span data-stu-id="04507-129">Type: **float\***</span></span>

<span data-ttu-id="04507-130">Указатель на расстояние с параметром пересечения лучей.</span><span class="sxs-lookup"><span data-stu-id="04507-130">Pointer to a ray intersection parameter distance.</span></span>

</dd> <dt>

<span data-ttu-id="04507-131">*ппаллхитс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="04507-131">*ppAllHits* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="04507-132">Тип: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="04507-132">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="04507-133">Указатель на [**интерфейс ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob), содержащий массив структур [**\_ \_ сведений о пересечении D3DX10**](d3dx10-intersect-info.md) .</span><span class="sxs-lookup"><span data-stu-id="04507-133">Pointer to an [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob), containing an array of [**D3DX10\_INTERSECT\_INFO**](d3dx10-intersect-info.md) structures.</span></span> <span data-ttu-id="04507-134">Это список всех попаданий, произошедших в тесте пересечения.</span><span class="sxs-lookup"><span data-stu-id="04507-134">This is a list of all the hits that occurred in the intersection test.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04507-135">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="04507-135">Return value</span></span>

<span data-ttu-id="04507-136">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="04507-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="04507-137">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="04507-137">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="04507-138">Комментарии</span><span class="sxs-lookup"><span data-stu-id="04507-138">Remarks</span></span>

<span data-ttu-id="04507-139">Этот API позволяет понять точки в и вокруг треугольника независимо от того, где фактически находится треугольник.</span><span class="sxs-lookup"><span data-stu-id="04507-139">This API provides a way to understand points in and around a triangle, independent of where the triangle is actually located.</span></span> <span data-ttu-id="04507-140">Эта функция возвращает результирующую точку, используя следующее уравнение: v1 + U (V2-v1) + V (v3-v1).</span><span class="sxs-lookup"><span data-stu-id="04507-140">This function returns the resulting point by using the following equation: V1 + U(V2 - V1) + V(V3 - V1).</span></span>

<span data-ttu-id="04507-141">Любая точка в плоскости V1V2V3 может быть представлена координатой барицентрик (U, V).</span><span class="sxs-lookup"><span data-stu-id="04507-141">Any point in the plane V1V2V3 can be represented by the barycentric coordinate (U,V).</span></span> <span data-ttu-id="04507-142">Параметр U управляет тем, сколько v2 имеет взвешенное значение в результате, а параметр V определяет, сколько будет иметь взвешенное значение v3 в результате.</span><span class="sxs-lookup"><span data-stu-id="04507-142">The parameter U controls how much V2 gets weighted into the result, and the parameter V controls how much V3 gets weighted into the result.</span></span> <span data-ttu-id="04507-143">Наконец, значение \[ 1 (U + V) \] определяет, сколько единиц измерения v1 будет взвешено по результату.</span><span class="sxs-lookup"><span data-stu-id="04507-143">Lastly, the value of \[1 - (U + V)\] controls how much V1 gets weighted into the result.</span></span>

<span data-ttu-id="04507-144">Координаты барицентрик — это форма общих координат.</span><span class="sxs-lookup"><span data-stu-id="04507-144">Barycentric coordinates are a form of general coordinates.</span></span> <span data-ttu-id="04507-145">В этом контексте использование координат барицентрик представляет собой изменение в системах координат.</span><span class="sxs-lookup"><span data-stu-id="04507-145">In this context, using barycentric coordinates represents a change in coordinate systems.</span></span> <span data-ttu-id="04507-146">Что содержит значение true для декартовых координат, имеет значение true для координат барицентрик.</span><span class="sxs-lookup"><span data-stu-id="04507-146">What holds true for Cartesian coordinates holds true for barycentric coordinates.</span></span>

<span data-ttu-id="04507-147">Координаты барицентрик определяют точку внутри треугольника с точки зрения вершин треугольника.</span><span class="sxs-lookup"><span data-stu-id="04507-147">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="04507-148">Более подробное описание координат барицентрик см. в разделе [Описание координат Барицентрик MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="04507-148">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="04507-149">Требования</span><span class="sxs-lookup"><span data-stu-id="04507-149">Requirements</span></span>



| <span data-ttu-id="04507-150">Требование</span><span class="sxs-lookup"><span data-stu-id="04507-150">Requirement</span></span> | <span data-ttu-id="04507-151">Значение</span><span class="sxs-lookup"><span data-stu-id="04507-151">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="04507-152">Header</span><span class="sxs-lookup"><span data-stu-id="04507-152">Header</span></span><br/>  | <dl> <span data-ttu-id="04507-153"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="04507-153"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="04507-154">Библиотека</span><span class="sxs-lookup"><span data-stu-id="04507-154">Library</span></span><br/> | <dl> <span data-ttu-id="04507-155"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="04507-155"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04507-156">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="04507-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04507-157">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="04507-157">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="04507-158">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="04507-158">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
