---
description: Определяет, пересекается ли луч с этой сеткой.
ms.assetid: 74565d4a-94e6-4faa-bf70-9c1b35e5e5d8
title: Метод ID3DX10Mesh::Intersect (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.Intersect
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8ceed03ab21debf61371da9e53b5150d2dc83e4a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105647845"
---
# <a name="id3dx10meshintersect-method"></a><span data-ttu-id="aba6b-103">Метод ID3DX10Mesh:: Intersect</span><span class="sxs-lookup"><span data-stu-id="aba6b-103">ID3DX10Mesh::Intersect method</span></span>

<span data-ttu-id="aba6b-104">Определяет, пересекается ли луч с этой сеткой.</span><span class="sxs-lookup"><span data-stu-id="aba6b-104">Determines if a ray intersects with this mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="aba6b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="aba6b-105">Syntax</span></span>


```C++
HRESULT Intersect(
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



## <a name="parameters"></a><span data-ttu-id="aba6b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="aba6b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aba6b-107">*прайпос* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="aba6b-107">*pRayPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aba6b-108">Тип: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="aba6b-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="aba6b-109">Указатель на структуру [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , указывающий точку, с которой начинается луч.</span><span class="sxs-lookup"><span data-stu-id="aba6b-109">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, specifying the point where the ray begins.</span></span>

</dd> <dt>

<span data-ttu-id="aba6b-110">*прайдир* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="aba6b-110">*pRayDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aba6b-111">Тип: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="aba6b-111">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="aba6b-112">Указатель на структуру [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , в которой указывается направление луча.</span><span class="sxs-lookup"><span data-stu-id="aba6b-112">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, specifying the direction of the ray.</span></span>

</dd> <dt>

<span data-ttu-id="aba6b-113">*фиткаунт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="aba6b-113">*pHitCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aba6b-114">Тип: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="aba6b-114">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="aba6b-115">Количество раз, когда луч пересекается с сеткой.</span><span class="sxs-lookup"><span data-stu-id="aba6b-115">The number of times the ray intersected with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="aba6b-116">*пфацеиндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="aba6b-116">*pFaceIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aba6b-117">Тип: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="aba6b-117">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="aba6b-118">Указатель на значение индекса стороны, ближайшее к началу луча, если Фит имеет **значение true**.</span><span class="sxs-lookup"><span data-stu-id="aba6b-118">Pointer to an index value of the face closest to the ray origin, if pHit is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="aba6b-119">*PU* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="aba6b-119">*pU* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aba6b-120">Тип: **float \***</span><span class="sxs-lookup"><span data-stu-id="aba6b-120">Type: **float\***</span></span>

<span data-ttu-id="aba6b-121">Указатель на барицентрик координату нажатия, U.</span><span class="sxs-lookup"><span data-stu-id="aba6b-121">Pointer to a barycentric hit coordinate, U.</span></span>

</dd> <dt>

<span data-ttu-id="aba6b-122">*ПС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="aba6b-122">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aba6b-123">Тип: **float \***</span><span class="sxs-lookup"><span data-stu-id="aba6b-123">Type: **float\***</span></span>

<span data-ttu-id="aba6b-124">Указатель на барицентрик координату, V.</span><span class="sxs-lookup"><span data-stu-id="aba6b-124">Pointer to a barycentric hit coordinate, V.</span></span>

</dd> <dt>

<span data-ttu-id="aba6b-125">*пдист* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="aba6b-125">*pDist* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aba6b-126">Тип: **float \***</span><span class="sxs-lookup"><span data-stu-id="aba6b-126">Type: **float\***</span></span>

<span data-ttu-id="aba6b-127">Указатель на расстояние с параметром пересечения лучей.</span><span class="sxs-lookup"><span data-stu-id="aba6b-127">Pointer to a ray intersection parameter distance.</span></span>

</dd> <dt>

<span data-ttu-id="aba6b-128">*ппаллхитс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="aba6b-128">*ppAllHits* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aba6b-129">Тип: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="aba6b-129">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="aba6b-130">Указатель на [**интерфейс ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob), содержащий массив структур [**\_ \_ сведений о пересечении D3DX10**](d3dx10-intersect-info.md) .</span><span class="sxs-lookup"><span data-stu-id="aba6b-130">Pointer to an [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob), containing an array of [**D3DX10\_INTERSECT\_INFO**](d3dx10-intersect-info.md) structures.</span></span> <span data-ttu-id="aba6b-131">Это список всех попаданий, произошедших в тесте пересечения.</span><span class="sxs-lookup"><span data-stu-id="aba6b-131">This is a list of all the hits that occurred in the intersection test.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aba6b-132">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="aba6b-132">Return value</span></span>

<span data-ttu-id="aba6b-133">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="aba6b-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="aba6b-134">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="aba6b-134">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="aba6b-135">Комментарии</span><span class="sxs-lookup"><span data-stu-id="aba6b-135">Remarks</span></span>

<span data-ttu-id="aba6b-136">Этот API позволяет понять точки в и вокруг треугольника независимо от того, где фактически находится треугольник.</span><span class="sxs-lookup"><span data-stu-id="aba6b-136">This API provides a way to understand points in and around a triangle, independent of where the triangle is actually located.</span></span> <span data-ttu-id="aba6b-137">Эта функция возвращает результирующую точку, используя следующее уравнение: v1 + U (V2-v1) + V (v3-v1).</span><span class="sxs-lookup"><span data-stu-id="aba6b-137">This function returns the resulting point by using the following equation: V1 + U(V2 - V1) + V(V3 - V1).</span></span>

<span data-ttu-id="aba6b-138">Любая точка в плоскости V1V2V3 может быть представлена координатой барицентрик (U, V).</span><span class="sxs-lookup"><span data-stu-id="aba6b-138">Any point in the plane V1V2V3 can be represented by the barycentric coordinate (U,V).</span></span> <span data-ttu-id="aba6b-139">Параметр U управляет тем, сколько v2 имеет взвешенное значение в результате, а параметр V определяет, сколько будет иметь взвешенное значение v3 в результате.</span><span class="sxs-lookup"><span data-stu-id="aba6b-139">The parameter U controls how much V2 gets weighted into the result, and the parameter V controls how much V3 gets weighted into the result.</span></span> <span data-ttu-id="aba6b-140">Наконец, значение \[ 1 (U + V) \] определяет, сколько единиц измерения v1 будет взвешено по результату.</span><span class="sxs-lookup"><span data-stu-id="aba6b-140">Lastly, the value of \[1 - (U + V)\] controls how much V1 gets weighted into the result.</span></span>

<span data-ttu-id="aba6b-141">Координаты барицентрик — это форма общих координат.</span><span class="sxs-lookup"><span data-stu-id="aba6b-141">Barycentric coordinates are a form of general coordinates.</span></span> <span data-ttu-id="aba6b-142">В этом контексте использование координат барицентрик представляет собой изменение в системах координат.</span><span class="sxs-lookup"><span data-stu-id="aba6b-142">In this context, using barycentric coordinates represents a change in coordinate systems.</span></span> <span data-ttu-id="aba6b-143">Что содержит значение true для декартовых координат, имеет значение true для координат барицентрик.</span><span class="sxs-lookup"><span data-stu-id="aba6b-143">What holds true for Cartesian coordinates holds true for barycentric coordinates.</span></span>

<span data-ttu-id="aba6b-144">Координаты барицентрик определяют точку внутри треугольника с точки зрения вершин треугольника.</span><span class="sxs-lookup"><span data-stu-id="aba6b-144">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="aba6b-145">Более подробное описание координат барицентрик см. в разделе [Описание координат Барицентрик MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="aba6b-145">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="aba6b-146">Требования</span><span class="sxs-lookup"><span data-stu-id="aba6b-146">Requirements</span></span>



| <span data-ttu-id="aba6b-147">Требование</span><span class="sxs-lookup"><span data-stu-id="aba6b-147">Requirement</span></span> | <span data-ttu-id="aba6b-148">Значение</span><span class="sxs-lookup"><span data-stu-id="aba6b-148">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="aba6b-149">Header</span><span class="sxs-lookup"><span data-stu-id="aba6b-149">Header</span></span><br/>  | <dl> <span data-ttu-id="aba6b-150"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="aba6b-150"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="aba6b-151">Библиотека</span><span class="sxs-lookup"><span data-stu-id="aba6b-151">Library</span></span><br/> | <dl> <span data-ttu-id="aba6b-152"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aba6b-152"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aba6b-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="aba6b-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aba6b-154">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="aba6b-154">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="aba6b-155">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="aba6b-155">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
