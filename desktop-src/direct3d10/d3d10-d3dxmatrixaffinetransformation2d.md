---
description: Строит матрицу двумерных преобразований в плоскости x-y. Аргументы NULL обрабатываются как преобразования Identity.
ms.assetid: f46a307c-4566-42c8-8def-fb189116144e
title: Функция D3DXMatrixAffineTransformation2D (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixAffineTransformation2D
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 223ef5d2d9a68c993553d52f5d4cf63e8b95dd3b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694276"
---
# <a name="d3dxmatrixaffinetransformation2d-function-d3dx10mathh"></a><span data-ttu-id="9b6be-104">Функция D3DXMatrixAffineTransformation2D (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="9b6be-104">D3DXMatrixAffineTransformation2D function (D3DX10Math.h)</span></span>

<span data-ttu-id="9b6be-105">Строит матрицу двумерных преобразований в плоскости x-y.</span><span class="sxs-lookup"><span data-stu-id="9b6be-105">Builds a 2D affine transformation matrix in the x-y plane.</span></span> <span data-ttu-id="9b6be-106">Аргументы **null** обрабатываются как преобразования Identity.</span><span class="sxs-lookup"><span data-stu-id="9b6be-106">**NULL** arguments are treated as identity transformations.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b6be-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9b6be-107">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixAffineTransformation2D(
  _In_       D3DXMATRIX  *pOut,
  _In_       FLOAT       Scaling,
  _In_ const D3DXVECTOR2 *pRotationCenter,
  _In_       FLOAT       Rotation,
  _In_ const D3DXVECTOR2 *pTranslation
);
```



## <a name="parameters"></a><span data-ttu-id="9b6be-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9b6be-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b6be-109">*тоска* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9b6be-109">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b6be-110">Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="9b6be-110">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="9b6be-111">Указатель на [**D3DXMATRIX**](d3d10-d3dxmatrix.md) , который является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="9b6be-111">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="9b6be-112">*Масштабирование* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9b6be-112">*Scaling* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b6be-113">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9b6be-113">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9b6be-114">Коэффициент масштабирования.</span><span class="sxs-lookup"><span data-stu-id="9b6be-114">Scaling factor.</span></span>

</dd> <dt>

<span data-ttu-id="9b6be-115">*протатионцентер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9b6be-115">*pRotationCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b6be-116">Тип: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="9b6be-116">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="9b6be-117">Указатель на [**D3DXVECTOR2**](d3d10-d3dxvector2.md), указывающий центр вращения.</span><span class="sxs-lookup"><span data-stu-id="9b6be-117">Pointer to a [**D3DXVECTOR2**](d3d10-d3dxvector2.md), a point identifying the center of rotation.</span></span> <span data-ttu-id="9b6be-118">Если этот аргумент имеет **значение NULL**, то к формуле в разделе "Примечания" применяется матрица версии-<sub>кандидата</sub> Identity M.</span><span class="sxs-lookup"><span data-stu-id="9b6be-118">If this argument is **NULL**, an identity M<sub>rc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="9b6be-119">*Вращение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9b6be-119">*Rotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b6be-120">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9b6be-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9b6be-121">Угол поворота.</span><span class="sxs-lookup"><span data-stu-id="9b6be-121">The angle of rotation.</span></span>

</dd> <dt>

<span data-ttu-id="9b6be-122">*птранслатион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9b6be-122">*pTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b6be-123">Тип: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="9b6be-123">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="9b6be-124">Указатель на [**D3DXVECTOR2**](d3d10-d3dxvector2.md), представляющий перевод.</span><span class="sxs-lookup"><span data-stu-id="9b6be-124">Pointer to a [**D3DXVECTOR2**](d3d10-d3dxvector2.md), representing the translation.</span></span> <span data-ttu-id="9b6be-125">Если этот аргумент имеет **значение NULL**, к формуле в разделе "Примечания" применяется матрица-MT Identity.</span><span class="sxs-lookup"><span data-stu-id="9b6be-125">If this argument is **NULL**, an identity Mₜ matrix is applied to the formula in Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b6be-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9b6be-126">Return value</span></span>

<span data-ttu-id="9b6be-127">Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="9b6be-127">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="9b6be-128">Указатель на структуру D3DXMATRIX, которая является матрицей аффинного преобразования.</span><span class="sxs-lookup"><span data-stu-id="9b6be-128">Pointer to a D3DXMATRIX structure that is an affine transformation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b6be-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9b6be-129">Remarks</span></span>

<span data-ttu-id="9b6be-130">Эта функция вычисляет матрицу аффинных преобразований с помощью следующей формулы, при этом сцепление матрицы вычисляется в порядке слева направо:</span><span class="sxs-lookup"><span data-stu-id="9b6be-130">This function calculates the affine transformation matrix with the following formula, with matrix concatenation evaluated in left-to-right order:</span></span>

<span data-ttu-id="9b6be-131">M<sub>out</sub> = MS \* (M<sub>RC</sub>)-1 \* M<sub>r</sub> \* m<sub>RC</sub> \* MT</span><span class="sxs-lookup"><span data-stu-id="9b6be-131">M<sub>out</sub> = Mₛ \* (M<sub>rc</sub>)-1 \* M<sub>r</sub> \* M<sub>rc</sub> \* Mₜ</span></span>

<span data-ttu-id="9b6be-132">где:</span><span class="sxs-lookup"><span data-stu-id="9b6be-132">where:</span></span>

<span data-ttu-id="9b6be-133">M<sub>out</sub> = выходная матрица (Тоска)</span><span class="sxs-lookup"><span data-stu-id="9b6be-133">M<sub>out</sub> = output matrix (pOut)</span></span>

<span data-ttu-id="9b6be-134">MS = матрица масштабирования (масштабирование)</span><span class="sxs-lookup"><span data-stu-id="9b6be-134">Mₛ = scaling matrix (Scaling)</span></span>

<span data-ttu-id="9b6be-135">M<sub>RC</sub> = центр матрицы вращения (протатионцентер)</span><span class="sxs-lookup"><span data-stu-id="9b6be-135">M<sub>rc</sub> = center of rotation matrix (pRotationCenter)</span></span>

<span data-ttu-id="9b6be-136">M<sub>r</sub> = матрица вращения (вращение)</span><span class="sxs-lookup"><span data-stu-id="9b6be-136">M<sub>r</sub> = rotation matrix (Rotation)</span></span>

<span data-ttu-id="9b6be-137">MT = матрица перевода (Птранслатион)</span><span class="sxs-lookup"><span data-stu-id="9b6be-137">Mₜ = translation matrix (pTranslation)</span></span>

<span data-ttu-id="9b6be-138">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="9b6be-138">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="9b6be-139">Таким образом, функция D3DXMatrixAffineTransformation2D может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="9b6be-139">In this way, the D3DXMatrixAffineTransformation2D function can be used as a parameter for another function.</span></span>

<span data-ttu-id="9b6be-140">Для трехмерных преобразований используйте D3DXMatrixAffineTransformation.</span><span class="sxs-lookup"><span data-stu-id="9b6be-140">For 3D affine transformations, use D3DXMatrixAffineTransformation.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b6be-141">Требования</span><span class="sxs-lookup"><span data-stu-id="9b6be-141">Requirements</span></span>



| <span data-ttu-id="9b6be-142">Требование</span><span class="sxs-lookup"><span data-stu-id="9b6be-142">Requirement</span></span> | <span data-ttu-id="9b6be-143">Значение</span><span class="sxs-lookup"><span data-stu-id="9b6be-143">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9b6be-144">Header</span><span class="sxs-lookup"><span data-stu-id="9b6be-144">Header</span></span><br/>  | <dl> <span data-ttu-id="9b6be-145"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b6be-145"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="9b6be-146">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9b6be-146">Library</span></span><br/> | <dl> <span data-ttu-id="9b6be-147"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9b6be-147"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9b6be-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9b6be-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b6be-149">Математические функции</span><span class="sxs-lookup"><span data-stu-id="9b6be-149">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
