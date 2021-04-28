---
description: Функция D3DXVec3BaryCentric (D3DX10Math. h) — возвращает точку в координатах Барицентрик, используя указанные трехмерные векторы.
ms.assetid: 572e151d-8044-480e-92b2-3f973d92d03e
title: Функция D3DXVec3BaryCentric (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3BaryCentric
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: e350bde6d1b898088ccb9b68d10a9a346935bfd5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108252"
---
# <a name="d3dxvec3barycentric-function-d3dx10mathh"></a><span data-ttu-id="1ba53-103">Функция D3DXVec3BaryCentric (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="1ba53-103">D3DXVec3BaryCentric function (D3DX10Math.h)</span></span>

<span data-ttu-id="1ba53-104">Возвращает точку в координатах Барицентрик с использованием указанных трехмерных векторов.</span><span class="sxs-lookup"><span data-stu-id="1ba53-104">Returns a point in Barycentric coordinates, using the specified 3D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ba53-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1ba53-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3BaryCentric(
  _In_       D3DXVECTOR3 *pOut,
  _In_ const D3DXVECTOR3 *pV1,
  _In_ const D3DXVECTOR3 *pV2,
  _In_ const D3DXVECTOR3 *pV3,
  _In_       FLOAT       f,
  _In_       FLOAT       g
);
```



## <a name="parameters"></a><span data-ttu-id="1ba53-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1ba53-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ba53-107">*тоска* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1ba53-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ba53-108">Тип: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="1ba53-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="1ba53-109">Указатель на [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , который является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="1ba53-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="1ba53-110">*pV1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1ba53-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ba53-111">Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="1ba53-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="1ba53-112">Указатель на исходную структуру D3DXVECTOR3.</span><span class="sxs-lookup"><span data-stu-id="1ba53-112">Pointer to a source D3DXVECTOR3 structure.</span></span>

</dd> <dt>

<span data-ttu-id="1ba53-113">*pV2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1ba53-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ba53-114">Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="1ba53-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="1ba53-115">Указатель на исходную структуру D3DXVECTOR3.</span><span class="sxs-lookup"><span data-stu-id="1ba53-115">Pointer to a source D3DXVECTOR3 structure.</span></span>

</dd> <dt>

<span data-ttu-id="1ba53-116">*pV3* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1ba53-116">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ba53-117">Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="1ba53-117">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="1ba53-118">Указатель на исходную структуру D3DXVECTOR3.</span><span class="sxs-lookup"><span data-stu-id="1ba53-118">Pointer to a source D3DXVECTOR3 structure.</span></span>

</dd> <dt>

<span data-ttu-id="1ba53-119">*f* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="1ba53-119">*f* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ba53-120">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1ba53-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1ba53-121">Весовой коэффициент.</span><span class="sxs-lookup"><span data-stu-id="1ba53-121">Weighting factor.</span></span> <span data-ttu-id="1ba53-122">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="1ba53-122">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="1ba53-123">*g* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="1ba53-123">*g* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ba53-124">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1ba53-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1ba53-125">Весовой коэффициент.</span><span class="sxs-lookup"><span data-stu-id="1ba53-125">Weighting factor.</span></span> <span data-ttu-id="1ba53-126">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="1ba53-126">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ba53-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1ba53-127">Return value</span></span>

<span data-ttu-id="1ba53-128">Тип: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="1ba53-128">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="1ba53-129">Указатель на структуру D3DXVECTOR3 в координатах Барицентрик.</span><span class="sxs-lookup"><span data-stu-id="1ba53-129">Pointer to a D3DXVECTOR3 structure in Barycentric coordinates.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ba53-130">Remarks</span><span class="sxs-lookup"><span data-stu-id="1ba53-130">Remarks</span></span>

<span data-ttu-id="1ba53-131">Функция D3DXVec3BaryCentric предоставляет способ для понимания точек в треугольнике и вокруг него независимо от того, где фактически находится треугольник.</span><span class="sxs-lookup"><span data-stu-id="1ba53-131">The D3DXVec3BaryCentric function provides a way to understand points in and around a triangle, independent of where the triangle is actually located.</span></span> <span data-ttu-id="1ba53-132">Эта функция возвращает результирующую точку, используя следующее уравнение: v1 + f (V2-v1) + g (v3-v1).</span><span class="sxs-lookup"><span data-stu-id="1ba53-132">This function returns the resulting point by using the following equation: V1 + f(V2-V1) + g(V3-V1).</span></span>

<span data-ttu-id="1ba53-133">Любая точка в плоскости V1V2V3 может быть представлена координатой Барицентрик (f, g). Параметр f управляет тем, сколько v2 имеет взвешенный результат, а параметр g определяет, сколько единиц измерения v3 будет взвешено по результату.</span><span class="sxs-lookup"><span data-stu-id="1ba53-133">Any point in the plane V1V2V3 can be represented by the Barycentric coordinate (f,g).The parameter f controls how much V2 gets weighted into the result and the parameter g controls how much V3 gets weighted into the result.</span></span> <span data-ttu-id="1ba53-134">Наконец, 1-f-g определяет, сколько единиц измерения v1 будет взвешено по результату.</span><span class="sxs-lookup"><span data-stu-id="1ba53-134">Lastly, 1-f-g controls how much V1 gets weighted into the result.</span></span>

<span data-ttu-id="1ba53-135">Обратите внимание на следующие связи.</span><span class="sxs-lookup"><span data-stu-id="1ba53-135">Note the following relations.</span></span>

-   <span data-ttu-id="1ba53-136">Если (f>= 0 &, & g>= 0 &, & 1-f-g>= 0), точка находится внутри треугольника V1V2V3.</span><span class="sxs-lookup"><span data-stu-id="1ba53-136">If (f>=0 &, & g>=0 &, & 1-f-g>=0), the point is inside the triangle V1V2V3.</span></span>
-   <span data-ttu-id="1ba53-137">Если (f = = 0 &, & g>= 0 &, & 1-f-g>= 0), точка находится в строке V1V3.</span><span class="sxs-lookup"><span data-stu-id="1ba53-137">If (f==0 &, & g>=0 &, & 1-f-g>=0), the point is on the line V1V3.</span></span>
-   <span data-ttu-id="1ba53-138">Если (f>= 0 &, & g = = 0 &, & 1-f-g>= 0), то точка находится в строке V1V2.</span><span class="sxs-lookup"><span data-stu-id="1ba53-138">If (f>=0 &, & g==0 &, & 1-f-g>=0), the point is on the line V1V2.</span></span>
-   <span data-ttu-id="1ba53-139">Если (f>= 0 &, & g>= 0 &, & 1-f-g = = 0), точка находится в строке V2V3.</span><span class="sxs-lookup"><span data-stu-id="1ba53-139">If (f>=0 &, & g>=0 &, & 1-f-g==0), the point is on the line V2V3.</span></span>

<span data-ttu-id="1ba53-140">Координаты барицентрик — это форма общих координат.</span><span class="sxs-lookup"><span data-stu-id="1ba53-140">Barycentric coordinates are a form of general coordinates.</span></span> <span data-ttu-id="1ba53-141">В этом контексте использование координат Барицентрик представляет собой изменение в системах координат.</span><span class="sxs-lookup"><span data-stu-id="1ba53-141">In this context, using Barycentric coordinates represents a change in coordinate systems.</span></span> <span data-ttu-id="1ba53-142">Что содержит значение true для декартовых координат, имеет значение true для координат Барицентрик.</span><span class="sxs-lookup"><span data-stu-id="1ba53-142">What holds true for Cartesian coordinates holds true for Barycentric coordinates.</span></span>

<span data-ttu-id="1ba53-143">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="1ba53-143">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="1ba53-144">Таким образом, функция D3DXVec3BaryCentric может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="1ba53-144">In this way, the D3DXVec3BaryCentric function can be used as a parameter for another function.</span></span>

<span data-ttu-id="1ba53-145">Координаты барицентрик определяют точку внутри треугольника с точки зрения вершин треугольника.</span><span class="sxs-lookup"><span data-stu-id="1ba53-145">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="1ba53-146">Более подробное описание координат барицентрик см. в разделе [Описание координат Барицентрик MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="1ba53-146">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="1ba53-147">Требования</span><span class="sxs-lookup"><span data-stu-id="1ba53-147">Requirements</span></span>



| <span data-ttu-id="1ba53-148">Требование</span><span class="sxs-lookup"><span data-stu-id="1ba53-148">Requirement</span></span> | <span data-ttu-id="1ba53-149">Значение</span><span class="sxs-lookup"><span data-stu-id="1ba53-149">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1ba53-150">Header</span><span class="sxs-lookup"><span data-stu-id="1ba53-150">Header</span></span><br/> | <dl> <span data-ttu-id="1ba53-151"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ba53-151"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ba53-152">См. также</span><span class="sxs-lookup"><span data-stu-id="1ba53-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ba53-153">Математические функции</span><span class="sxs-lookup"><span data-stu-id="1ba53-153">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
