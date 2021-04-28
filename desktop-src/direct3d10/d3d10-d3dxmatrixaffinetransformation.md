---
description: Функция D3DXMatrixAffineTransformation (D3DX10Math. h) — строит матрицу трехмерного преобразования. Аргументы NULL обрабатываются как преобразования Identity.
ms.assetid: 36044272-a8ce-47db-8f52-30dc680f8174
title: Функция D3DXMatrixAffineTransformation (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixAffineTransformation
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 01c6b3c3ffe2de9b7c7003b78f1b07a0f35cc3a1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113182"
---
# <a name="d3dxmatrixaffinetransformation-function-d3dx10mathh"></a><span data-ttu-id="f5e01-104">Функция D3DXMatrixAffineTransformation (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="f5e01-104">D3DXMatrixAffineTransformation function (D3DX10Math.h)</span></span>

<span data-ttu-id="f5e01-105">Формирует матрицу трехмерного преобразования.</span><span class="sxs-lookup"><span data-stu-id="f5e01-105">Builds a 3D affine transformation matrix.</span></span> <span data-ttu-id="f5e01-106">Аргументы **null** обрабатываются как преобразования Identity.</span><span class="sxs-lookup"><span data-stu-id="f5e01-106">**NULL** arguments are treated as identity transformations.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5e01-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f5e01-107">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixAffineTransformation(
  _In_       D3DXMATRIX     *pOut,
  _In_       FLOAT          Scaling,
  _In_ const D3DXVECTOR3    *pRotationCenter,
  _In_ const D3DXQUATERNION *pRotation,
  _In_ const D3DXVECTOR3    *pTranslation
);
```



## <a name="parameters"></a><span data-ttu-id="f5e01-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f5e01-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5e01-109">*тоска* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f5e01-109">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5e01-110">Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="f5e01-110">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f5e01-111">Указатель на [**D3DXMATRIX**](d3d10-d3dxmatrix.md) , который является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="f5e01-111">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="f5e01-112">*Масштабирование* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f5e01-112">*Scaling* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5e01-113">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f5e01-113">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f5e01-114">Коэффициент масштабирования.</span><span class="sxs-lookup"><span data-stu-id="f5e01-114">Scaling factor.</span></span>

</dd> <dt>

<span data-ttu-id="f5e01-115">*протатионцентер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f5e01-115">*pRotationCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5e01-116">Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="f5e01-116">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="f5e01-117">Указатель на [**D3DXVECTOR3**](d3d10-d3dxvector3.md), указывающий центр вращения.</span><span class="sxs-lookup"><span data-stu-id="f5e01-117">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md), a point identifying the center of rotation.</span></span> <span data-ttu-id="f5e01-118">Если этот аргумент имеет **значение NULL**, то к формуле в разделе "Примечания" применяется матрица версии-<sub>кандидата</sub> Identity M.</span><span class="sxs-lookup"><span data-stu-id="f5e01-118">If this argument is **NULL**, an identity M<sub>rc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="f5e01-119"> \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f5e01-119">*pRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5e01-120">Тип: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="f5e01-120">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="f5e01-121">Указатель на [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) , указывающий поворот.</span><span class="sxs-lookup"><span data-stu-id="f5e01-121">Pointer to a [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that specifies the rotation.</span></span> <span data-ttu-id="f5e01-122">Если этот аргумент имеет **значение NULL**, к формуле в разделе "Примечания" применяется матрица с идентификатором M <sub>r</sub> .</span><span class="sxs-lookup"><span data-stu-id="f5e01-122">If this argument is **NULL**, an identity M<sub>r</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="f5e01-123">*птранслатион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f5e01-123">*pTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5e01-124">Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="f5e01-124">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="f5e01-125">Указатель на структуру D3DXVECTOR3, представляющую перевод.</span><span class="sxs-lookup"><span data-stu-id="f5e01-125">Pointer to a D3DXVECTOR3 structure representing the translation.</span></span> <span data-ttu-id="f5e01-126">Если этот аргумент имеет **значение NULL**, к формуле в разделе "Примечания" применяется матрица-MT Identity.</span><span class="sxs-lookup"><span data-stu-id="f5e01-126">If this argument is **NULL**, an identity Mₜ matrix is applied to the formula in Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5e01-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f5e01-127">Return value</span></span>

<span data-ttu-id="f5e01-128">Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="f5e01-128">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f5e01-129">Указатель на структуру D3DXMATRIX, которая является матрицей аффинного преобразования.</span><span class="sxs-lookup"><span data-stu-id="f5e01-129">Pointer to a D3DXMATRIX structure that is an affine transformation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5e01-130">Remarks</span><span class="sxs-lookup"><span data-stu-id="f5e01-130">Remarks</span></span>

<span data-ttu-id="f5e01-131">Эта функция вычисляет матрицу аффинных преобразований с помощью следующей формулы, при этом сцепление матрицы вычисляется в порядке слева направо:</span><span class="sxs-lookup"><span data-stu-id="f5e01-131">This function calculates the affine transformation matrix with the following formula, with matrix concatenation evaluated in left-to-right order:</span></span>

<span data-ttu-id="f5e01-132">M<sub>out</sub> = MS \* (M<sub>RC</sub>)-1 \* M<sub>r</sub> \* m<sub>RC</sub> \* MT</span><span class="sxs-lookup"><span data-stu-id="f5e01-132">M<sub>out</sub> = Mₛ \* (M<sub>rc</sub>)-1 \* M<sub>r</sub> \* M<sub>rc</sub> \* Mₜ</span></span>

<span data-ttu-id="f5e01-133">где:</span><span class="sxs-lookup"><span data-stu-id="f5e01-133">where:</span></span>

<span data-ttu-id="f5e01-134">M<sub>out</sub> = выходная матрица (Тоска)</span><span class="sxs-lookup"><span data-stu-id="f5e01-134">M<sub>out</sub> = output matrix (pOut)</span></span>

<span data-ttu-id="f5e01-135">MS = матрица масштабирования (масштабирование)</span><span class="sxs-lookup"><span data-stu-id="f5e01-135">Mₛ = scaling matrix (Scaling)</span></span>

<span data-ttu-id="f5e01-136">M<sub>RC</sub> = центр матрицы вращения (протатионцентер)</span><span class="sxs-lookup"><span data-stu-id="f5e01-136">M<sub>rc</sub> = center of rotation matrix (pRotationCenter)</span></span>

<span data-ttu-id="f5e01-137">M<sub>r</sub> = матрица вращения (расведение)</span><span class="sxs-lookup"><span data-stu-id="f5e01-137">M<sub>r</sub> = rotation matrix (pRotation)</span></span>

<span data-ttu-id="f5e01-138">MT = матрица перевода (Птранслатион)</span><span class="sxs-lookup"><span data-stu-id="f5e01-138">Mₜ = translation matrix (pTranslation)</span></span>

<span data-ttu-id="f5e01-139">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="f5e01-139">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="f5e01-140">Таким образом, функция D3DXMatrixAffineTransformation может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="f5e01-140">In this way, the D3DXMatrixAffineTransformation function can be used as a parameter for another function.</span></span>

<span data-ttu-id="f5e01-141">Для двумерных преобразований 2D используйте D3DXMatrixAffineTransformation2D.</span><span class="sxs-lookup"><span data-stu-id="f5e01-141">For 2D affine transformations, use D3DXMatrixAffineTransformation2D.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5e01-142">Требования</span><span class="sxs-lookup"><span data-stu-id="f5e01-142">Requirements</span></span>



| <span data-ttu-id="f5e01-143">Требование</span><span class="sxs-lookup"><span data-stu-id="f5e01-143">Requirement</span></span> | <span data-ttu-id="f5e01-144">Значение</span><span class="sxs-lookup"><span data-stu-id="f5e01-144">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f5e01-145">Header</span><span class="sxs-lookup"><span data-stu-id="f5e01-145">Header</span></span><br/>  | <dl> <span data-ttu-id="f5e01-146"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5e01-146"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="f5e01-147">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f5e01-147">Library</span></span><br/> | <dl> <span data-ttu-id="f5e01-148"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f5e01-148"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f5e01-149">См. также</span><span class="sxs-lookup"><span data-stu-id="f5e01-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5e01-150">Математические функции</span><span class="sxs-lookup"><span data-stu-id="f5e01-150">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
