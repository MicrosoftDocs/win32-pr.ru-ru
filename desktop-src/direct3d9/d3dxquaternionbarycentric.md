---
description: Возвращает кватернион в координатах барицентрик.
ms.assetid: 8fcd2e16-1bf1-4e18-afc9-17c92f2bbac5
title: Функция D3DXQuaternionBaryCentric (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionBaryCentric
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 002d235ab9957784c19b5e5a699dd87dfed74d4b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703736"
---
# <a name="d3dxquaternionbarycentric-function-d3dx9mathh"></a><span data-ttu-id="e5400-103">Функция D3DXQuaternionBaryCentric (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="e5400-103">D3DXQuaternionBaryCentric function (D3dx9math.h)</span></span>

<span data-ttu-id="e5400-104">Возвращает кватернион в координатах барицентрик.</span><span class="sxs-lookup"><span data-stu-id="e5400-104">Returns a quaternion in barycentric coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5400-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e5400-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionBaryCentric(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pQ2,
  _In_    const D3DXQUATERNION *pQ3,
  _In_          FLOAT          f,
  _In_          FLOAT          g
);
```



## <a name="parameters"></a><span data-ttu-id="e5400-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e5400-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5400-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="e5400-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e5400-108">Тип: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="e5400-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="e5400-109">Указатель на структуру [**D3DXQUATERNION**](d3dxquaternion.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="e5400-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="e5400-110">*pQ1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e5400-110">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5400-111">Тип: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="e5400-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="e5400-112">Указатель на исходную структуру [**D3DXQUATERNION**](d3dxquaternion.md) .</span><span class="sxs-lookup"><span data-stu-id="e5400-112">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="e5400-113">*pQ2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e5400-113">*pQ2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5400-114">Тип: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="e5400-114">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="e5400-115">Указатель на исходную структуру [**D3DXQUATERNION**](d3dxquaternion.md) .</span><span class="sxs-lookup"><span data-stu-id="e5400-115">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="e5400-116">*pQ3* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e5400-116">*pQ3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5400-117">Тип: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="e5400-117">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="e5400-118">Указатель на исходную структуру [**D3DXQUATERNION**](d3dxquaternion.md) .</span><span class="sxs-lookup"><span data-stu-id="e5400-118">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="e5400-119">*f* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="e5400-119">*f* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5400-120">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e5400-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e5400-121">Весовой коэффициент.</span><span class="sxs-lookup"><span data-stu-id="e5400-121">Weighting factor.</span></span> <span data-ttu-id="e5400-122">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="e5400-122">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="e5400-123">*g* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="e5400-123">*g* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5400-124">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e5400-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e5400-125">Весовой коэффициент.</span><span class="sxs-lookup"><span data-stu-id="e5400-125">Weighting factor.</span></span> <span data-ttu-id="e5400-126">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="e5400-126">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5400-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e5400-127">Return value</span></span>

<span data-ttu-id="e5400-128">Тип: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="e5400-128">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="e5400-129">Указатель на структуру [**D3DXQUATERNION**](d3dxquaternion.md) в координатах барицентрик.</span><span class="sxs-lookup"><span data-stu-id="e5400-129">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure in Barycentric coordinates.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5400-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e5400-130">Remarks</span></span>

<span data-ttu-id="e5400-131">Чтобы вычислить координаты барицентрик, функция **D3DXQuaternionBaryCentric** реализует следующую последовательность сферческих операций интерполяции.</span><span class="sxs-lookup"><span data-stu-id="e5400-131">To compute the barycentric coordinates, the **D3DXQuaternionBaryCentric** function implements the following series of spherical linear interpolation operations:</span></span>


```
Slerp(Slerp(Q1, Q2, f+g), Slerp(Q1, Q3, f+g), g/(f+g))
```



<span data-ttu-id="e5400-132">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="e5400-132">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="e5400-133">Таким образом, функция **D3DXQuaternionBaryCentric** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="e5400-133">In this way, the **D3DXQuaternionBaryCentric** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="e5400-134">Используйте [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) для любых входных данных кватернион, которые еще не нормализованы.</span><span class="sxs-lookup"><span data-stu-id="e5400-134">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

<span data-ttu-id="e5400-135">Координаты барицентрик определяют точку внутри треугольника с точки зрения вершин треугольника.</span><span class="sxs-lookup"><span data-stu-id="e5400-135">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="e5400-136">Более подробное описание координат барицентрик см. в разделе [Описание координат Барицентрик MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="e5400-136">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="e5400-137">Требования</span><span class="sxs-lookup"><span data-stu-id="e5400-137">Requirements</span></span>



| <span data-ttu-id="e5400-138">Требование</span><span class="sxs-lookup"><span data-stu-id="e5400-138">Requirement</span></span> | <span data-ttu-id="e5400-139">Значение</span><span class="sxs-lookup"><span data-stu-id="e5400-139">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e5400-140">Header</span><span class="sxs-lookup"><span data-stu-id="e5400-140">Header</span></span><br/>  | <dl> <span data-ttu-id="e5400-141"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5400-141"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="e5400-142">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e5400-142">Library</span></span><br/> | <dl> <span data-ttu-id="e5400-143"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e5400-143"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e5400-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e5400-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5400-145">Математические функции</span><span class="sxs-lookup"><span data-stu-id="e5400-145">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
