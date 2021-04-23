---
description: Возвращает точку в координатах Барицентрик с использованием указанных двумерных векторов.
ms.assetid: afbffe6d-d786-4d65-b737-ae201613d1ac
title: Функция D3DXVec2BaryCentric (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2BaryCentric
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8feb2f999ccc3628419c986ec0263d0e7e167d67
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157167"
---
# <a name="d3dxvec2barycentric-function-d3dx9mathh"></a><span data-ttu-id="5a9cb-103">Функция D3DXVec2BaryCentric (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="5a9cb-103">D3DXVec2BaryCentric function (D3dx9math.h)</span></span>

<span data-ttu-id="5a9cb-104">Возвращает точку в координатах Барицентрик с использованием указанных двумерных векторов.</span><span class="sxs-lookup"><span data-stu-id="5a9cb-104">Returns a point in Barycentric coordinates, using the specified 2D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a9cb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5a9cb-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2BaryCentric(
  _Out_       D3DXVECTOR2 *pOut,
  _In_  const D3DXVECTOR2 *pV1,
  _In_  const D3DXVECTOR2 *pV2,
  _In_  const D3DXVECTOR2 *pV3,
  _In_        FLOAT       f,
  _In_        FLOAT       g
);
```



## <a name="parameters"></a><span data-ttu-id="5a9cb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5a9cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a9cb-107">*тоска* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="5a9cb-107">*pOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5a9cb-108">Тип: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="5a9cb-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="5a9cb-109">Указатель на структуру [**D3DXVECTOR2**](d3dxvector2.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="5a9cb-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="5a9cb-110">*pV1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5a9cb-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a9cb-111">Тип: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="5a9cb-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="5a9cb-112">Указатель на исходную структуру [**D3DXVECTOR2**](d3dxvector2.md) .</span><span class="sxs-lookup"><span data-stu-id="5a9cb-112">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="5a9cb-113">*pV2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5a9cb-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a9cb-114">Тип: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="5a9cb-114">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="5a9cb-115">Указатель на исходную структуру [**D3DXVECTOR2**](d3dxvector2.md) .</span><span class="sxs-lookup"><span data-stu-id="5a9cb-115">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="5a9cb-116">*pV3* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5a9cb-116">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a9cb-117">Тип: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="5a9cb-117">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="5a9cb-118">Указатель на исходную структуру [**D3DXVECTOR2**](d3dxvector2.md) .</span><span class="sxs-lookup"><span data-stu-id="5a9cb-118">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="5a9cb-119">*f* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="5a9cb-119">*f* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a9cb-120">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5a9cb-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5a9cb-121">Весовой коэффициент.</span><span class="sxs-lookup"><span data-stu-id="5a9cb-121">Weighting factor.</span></span> <span data-ttu-id="5a9cb-122">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="5a9cb-122">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="5a9cb-123">*g* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="5a9cb-123">*g* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a9cb-124">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5a9cb-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5a9cb-125">Весовой коэффициент.</span><span class="sxs-lookup"><span data-stu-id="5a9cb-125">Weighting factor.</span></span> <span data-ttu-id="5a9cb-126">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="5a9cb-126">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a9cb-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5a9cb-127">Return value</span></span>

<span data-ttu-id="5a9cb-128">Тип: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="5a9cb-128">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="5a9cb-129">Указатель на структуру [**D3DXVECTOR2**](d3dxvector2.md) в координатах барицентрик.</span><span class="sxs-lookup"><span data-stu-id="5a9cb-129">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure in Barycentric coordinates.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a9cb-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5a9cb-130">Remarks</span></span>

<span data-ttu-id="5a9cb-131">Функция **D3DXVec2BaryCentric** предоставляет способ для понимания точек в треугольнике и вокруг него независимо от того, где фактически находится треугольник.</span><span class="sxs-lookup"><span data-stu-id="5a9cb-131">The **D3DXVec2BaryCentric** function provides a way to understand points in and around a triangle, independent of where the triangle is actually located.</span></span> <span data-ttu-id="5a9cb-132">Эта функция возвращает результирующую точку, используя следующее уравнение: v1 + f (V2-v1) + g (v3-v1).</span><span class="sxs-lookup"><span data-stu-id="5a9cb-132">This function returns the resulting point by using the following equation: V1 + f(V2-V1) + g(V3-V1).</span></span>

<span data-ttu-id="5a9cb-133">Любая точка в плоскости V1V2V3 может быть представлена координатой Барицентрик (f, g). Параметр *f* управляет тем, сколько v2 имеет взвешенный результат, а параметр *g* определяет, сколько будет иметь взвешенное значение v3 в результате.</span><span class="sxs-lookup"><span data-stu-id="5a9cb-133">Any point in the plane V1V2V3 can be represented by the Barycentric coordinate (f,g).The parameter *f* controls how much V2 gets weighted into the result, and the parameter *g* controls how much V3 gets weighted into the result.</span></span> <span data-ttu-id="5a9cb-134">Наконец, 1-f-g определяет, сколько единиц измерения v1 будет взвешено по результату.</span><span class="sxs-lookup"><span data-stu-id="5a9cb-134">Lastly, 1-f-g controls how much V1 gets weighted into the result.</span></span>

<span data-ttu-id="5a9cb-135">Обратите внимание на следующие связи.</span><span class="sxs-lookup"><span data-stu-id="5a9cb-135">Note the following relations.</span></span>

-   <span data-ttu-id="5a9cb-136">Если (f>= 0 &, & g>= 0 &, & 1-f-g>= 0), точка находится внутри треугольника V1V2V3.</span><span class="sxs-lookup"><span data-stu-id="5a9cb-136">If (f>=0 &, & g>=0 &, & 1-f-g>=0), the point is inside the triangle V1V2V3.</span></span>
-   <span data-ttu-id="5a9cb-137">Если (f = = 0 &, & g>= 0 &, & 1-f-g>= 0), точка находится в строке V1V3.</span><span class="sxs-lookup"><span data-stu-id="5a9cb-137">If (f==0 &, & g>=0 &, & 1-f-g>=0), the point is on the line V1V3.</span></span>
-   <span data-ttu-id="5a9cb-138">Если (f>= 0 &, & g = = 0 &, & 1-f-g>= 0), то точка находится в строке V1V2.</span><span class="sxs-lookup"><span data-stu-id="5a9cb-138">If (f>=0 &, & g==0 &, & 1-f-g>=0), the point is on the line V1V2.</span></span>
-   <span data-ttu-id="5a9cb-139">Если (f>= 0 &, & g>= 0 &, & 1-f-g = = 0), точка находится в строке V2V3.</span><span class="sxs-lookup"><span data-stu-id="5a9cb-139">If (f>=0 &, & g>=0 &, & 1-f-g==0), the point is on the line V2V3.</span></span>

<span data-ttu-id="5a9cb-140">Координаты барицентрик — это форма общих координат.</span><span class="sxs-lookup"><span data-stu-id="5a9cb-140">Barycentric coordinates are a form of general coordinates.</span></span> <span data-ttu-id="5a9cb-141">В этом контексте использование координат Барицентрик представляет собой изменение в системах координат.</span><span class="sxs-lookup"><span data-stu-id="5a9cb-141">In this context, using Barycentric coordinates represents a change in coordinate systems.</span></span> <span data-ttu-id="5a9cb-142">Что содержит значение true для декартовых координат, имеет значение true для координат Барицентрик.</span><span class="sxs-lookup"><span data-stu-id="5a9cb-142">What holds true for Cartesian coordinates holds true for Barycentric coordinates.</span></span>

<span data-ttu-id="5a9cb-143">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="5a9cb-143">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="5a9cb-144">Таким образом, функция **D3DXVec2BaryCentric** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="5a9cb-144">In this way, the **D3DXVec2BaryCentric** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="5a9cb-145">Координаты барицентрик определяют точку внутри треугольника с точки зрения вершин треугольника.</span><span class="sxs-lookup"><span data-stu-id="5a9cb-145">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="5a9cb-146">Более подробное описание координат барицентрик см. в разделе [Описание координат Барицентрик MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="5a9cb-146">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span> <span data-ttu-id="5a9cb-147">(Этот ресурс может быть недоступен в некоторых языках и странах.)</span><span class="sxs-lookup"><span data-stu-id="5a9cb-147">(This resource may not be available in some languages and countries.)</span></span>

## <a name="requirements"></a><span data-ttu-id="5a9cb-148">Требования</span><span class="sxs-lookup"><span data-stu-id="5a9cb-148">Requirements</span></span>



| <span data-ttu-id="5a9cb-149">Требование</span><span class="sxs-lookup"><span data-stu-id="5a9cb-149">Requirement</span></span> | <span data-ttu-id="5a9cb-150">Значение</span><span class="sxs-lookup"><span data-stu-id="5a9cb-150">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5a9cb-151">Header</span><span class="sxs-lookup"><span data-stu-id="5a9cb-151">Header</span></span><br/>  | <dl> <span data-ttu-id="5a9cb-152"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a9cb-152"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="5a9cb-153">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5a9cb-153">Library</span></span><br/> | <dl> <span data-ttu-id="5a9cb-154"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5a9cb-154"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5a9cb-155">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5a9cb-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a9cb-156">Математические функции</span><span class="sxs-lookup"><span data-stu-id="5a9cb-156">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
