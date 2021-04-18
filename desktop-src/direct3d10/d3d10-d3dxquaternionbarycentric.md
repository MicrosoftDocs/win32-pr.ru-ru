---
description: Возвращает кватернион в координатах барицентрик.
ms.assetid: 0a8d8d5a-f486-4457-86e9-27e76eaf1bc4
title: Функция D3DXQuaternionBaryCentric (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: f7cdfcf5b8e7052fcbea72f12123a0ea44422853
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105674747"
---
# <a name="d3dxquaternionbarycentric-function-d3dx10mathh"></a><span data-ttu-id="a630c-103">Функция D3DXQuaternionBaryCentric (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="a630c-103">D3DXQuaternionBaryCentric function (D3DX10Math.h)</span></span>

<span data-ttu-id="a630c-104">Возвращает кватернион в координатах барицентрик.</span><span class="sxs-lookup"><span data-stu-id="a630c-104">Returns a quaternion in barycentric coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="a630c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a630c-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="a630c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a630c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a630c-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="a630c-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a630c-108">Тип: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="a630c-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="a630c-109">Указатель на [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) , который является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="a630c-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="a630c-110">*pQ1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a630c-110">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a630c-111">Тип: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="a630c-111">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="a630c-112">Указатель на исходную структуру D3DXQUATERNION.</span><span class="sxs-lookup"><span data-stu-id="a630c-112">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="a630c-113">*pQ2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a630c-113">*pQ2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a630c-114">Тип: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="a630c-114">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="a630c-115">Указатель на исходную структуру D3DXQUATERNION.</span><span class="sxs-lookup"><span data-stu-id="a630c-115">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="a630c-116">*pQ3* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a630c-116">*pQ3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a630c-117">Тип: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="a630c-117">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="a630c-118">Указатель на исходную структуру D3DXQUATERNION.</span><span class="sxs-lookup"><span data-stu-id="a630c-118">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="a630c-119">*f* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="a630c-119">*f* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a630c-120">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a630c-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a630c-121">Весовой коэффициент.</span><span class="sxs-lookup"><span data-stu-id="a630c-121">Weighting factor.</span></span> <span data-ttu-id="a630c-122">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="a630c-122">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="a630c-123">*g* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="a630c-123">*g* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a630c-124">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a630c-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a630c-125">Весовой коэффициент.</span><span class="sxs-lookup"><span data-stu-id="a630c-125">Weighting factor.</span></span> <span data-ttu-id="a630c-126">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="a630c-126">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a630c-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a630c-127">Return value</span></span>

<span data-ttu-id="a630c-128">Тип: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="a630c-128">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="a630c-129">Указатель на структуру D3DXQUATERNION в координатах Барицентрик.</span><span class="sxs-lookup"><span data-stu-id="a630c-129">Pointer to a D3DXQUATERNION structure in Barycentric coordinates.</span></span>

## <a name="remarks"></a><span data-ttu-id="a630c-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a630c-130">Remarks</span></span>

<span data-ttu-id="a630c-131">Чтобы вычислить координаты барицентрик, функция D3DXQuaternionBaryCentric реализует следующую последовательность сферческих операций интерполяции.</span><span class="sxs-lookup"><span data-stu-id="a630c-131">To compute the barycentric coordinates, the D3DXQuaternionBaryCentric function implements the following series of spherical linear interpolation operations:</span></span>


```
Slerp(Slerp(Q1, Q2, f+g), Slerp(Q1, Q3, f+g), g/(f+g))
```



<span data-ttu-id="a630c-132">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="a630c-132">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="a630c-133">Таким образом, функция D3DXQuaternionBaryCentric может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="a630c-133">In this way, the D3DXQuaternionBaryCentric function can be used as a parameter for another function.</span></span>

<span data-ttu-id="a630c-134">Используйте [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) для любых входных данных кватернион, которые еще не нормализованы.</span><span class="sxs-lookup"><span data-stu-id="a630c-134">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

<span data-ttu-id="a630c-135">Координаты барицентрик определяют точку внутри треугольника с точки зрения вершин треугольника.</span><span class="sxs-lookup"><span data-stu-id="a630c-135">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="a630c-136">Более подробное описание координат барицентрик см. в разделе [Описание координат Барицентрик MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="a630c-136">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="a630c-137">Требования</span><span class="sxs-lookup"><span data-stu-id="a630c-137">Requirements</span></span>



| <span data-ttu-id="a630c-138">Требование</span><span class="sxs-lookup"><span data-stu-id="a630c-138">Requirement</span></span> | <span data-ttu-id="a630c-139">Значение</span><span class="sxs-lookup"><span data-stu-id="a630c-139">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a630c-140">Header</span><span class="sxs-lookup"><span data-stu-id="a630c-140">Header</span></span><br/>  | <dl> <span data-ttu-id="a630c-141"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="a630c-141"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="a630c-142">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a630c-142">Library</span></span><br/> | <dl> <span data-ttu-id="a630c-143"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a630c-143"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a630c-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a630c-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a630c-145">Математические функции</span><span class="sxs-lookup"><span data-stu-id="a630c-145">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
