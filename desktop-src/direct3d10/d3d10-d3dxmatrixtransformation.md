---
description: Функция D3DXMatrixTransformation (D3DX10Math. h) — создает матрицу преобразования. Аргументы NULL обрабатываются как преобразования Identity.
ms.assetid: 99c75ce9-3683-4753-b635-760eb8aaf46e
title: Функция D3DXMatrixTransformation (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixTransformation
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 10ed63b292dd69acb58d8567e6336b5aab4f7997
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108902"
---
# <a name="d3dxmatrixtransformation-function-d3dx10mathh"></a><span data-ttu-id="1cef0-104">Функция D3DXMatrixTransformation (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="1cef0-104">D3DXMatrixTransformation function (D3DX10Math.h)</span></span>

<span data-ttu-id="1cef0-105">Формирует матрицу преобразования.</span><span class="sxs-lookup"><span data-stu-id="1cef0-105">Builds a transformation matrix.</span></span> <span data-ttu-id="1cef0-106">Аргументы **null** обрабатываются как преобразования Identity.</span><span class="sxs-lookup"><span data-stu-id="1cef0-106">**NULL** arguments are treated as identity transformations.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cef0-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1cef0-107">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixTransformation(
  _Inout_       D3DXMATRIX     *pOut,
  _In_    const D3DXVECTOR3    *pScalingCenter,
  _In_    const D3DXQUATERNION *pScalingRotation,
  _In_    const D3DXVECTOR3    *pScaling,
  _In_    const D3DXVECTOR3    *pRotationCenter,
  _In_    const D3DXQUATERNION *pRotation,
  _In_    const D3DXVECTOR3    *pTranslation
);
```



## <a name="parameters"></a><span data-ttu-id="1cef0-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="1cef0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cef0-109">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="1cef0-109">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1cef0-110">Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="1cef0-110">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1cef0-111">Указатель на структуру [**D3DXMATRIX**](d3d10-d3dxmatrix.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="1cef0-111">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="1cef0-112">*пскалингцентер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1cef0-112">*pScalingCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cef0-113">Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="1cef0-113">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="1cef0-114">Указатель на [**D3DXVECTOR3**](d3d10-d3dxvector3.md), определяющий центральную точку масштабирования.</span><span class="sxs-lookup"><span data-stu-id="1cef0-114">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md), identifying the scaling center point.</span></span> <span data-ttu-id="1cef0-115">Если этот аргумент имеет **значение NULL**, к формуле в разделе "Примечания" применяется матрица Identity M <sub>SC</sub> .</span><span class="sxs-lookup"><span data-stu-id="1cef0-115">If this argument is **NULL**, an identity M<sub>sc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="1cef0-116">*пскалингротатион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1cef0-116">*pScalingRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cef0-117">Тип: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="1cef0-117">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="1cef0-118">Указатель на [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) , указывающий поворот масштабирования.</span><span class="sxs-lookup"><span data-stu-id="1cef0-118">Pointer to a [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that specifies the scaling rotation.</span></span> <span data-ttu-id="1cef0-119">Если этот аргумент имеет **значение NULL**, то к формуле в разделе "Примечания" применяется матрица с идентификатором M <sub>SR</sub> .</span><span class="sxs-lookup"><span data-stu-id="1cef0-119">If this argument is **NULL**, an identity M<sub>sr</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="1cef0-120">*пскалинг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1cef0-120">*pScaling* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cef0-121">Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="1cef0-121">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="1cef0-122">Указатель на структуру D3DXVECTOR3, вектор масштабирования.</span><span class="sxs-lookup"><span data-stu-id="1cef0-122">Pointer to a D3DXVECTOR3 structure, the scaling vector.</span></span> <span data-ttu-id="1cef0-123">Если этот аргумент имеет **значение NULL**, к формуле в примечаниях применяется удостоверение MS Matrix.</span><span class="sxs-lookup"><span data-stu-id="1cef0-123">If this argument is **NULL**, an identity Mₛ matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="1cef0-124">*протатионцентер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1cef0-124">*pRotationCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cef0-125">Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="1cef0-125">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="1cef0-126">Указатель на структуру D3DXVECTOR3 — точку, определяющую центр вращения.</span><span class="sxs-lookup"><span data-stu-id="1cef0-126">Pointer to a D3DXVECTOR3 structure, a point that identifies the center of rotation.</span></span> <span data-ttu-id="1cef0-127">Если этот аргумент имеет **значение NULL**, то к формуле в разделе "Примечания" применяется матрица версии-<sub>кандидата</sub> Identity M.</span><span class="sxs-lookup"><span data-stu-id="1cef0-127">If this argument is **NULL**, an identity M<sub>rc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="1cef0-128"> \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1cef0-128">*pRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cef0-129">Тип: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="1cef0-129">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="1cef0-130">Указатель на структуру D3DXQUATERNION, указывающую поворот.</span><span class="sxs-lookup"><span data-stu-id="1cef0-130">Pointer to a D3DXQUATERNION structure that specifies the rotation.</span></span> <span data-ttu-id="1cef0-131">Если этот аргумент имеет **значение NULL**, к формуле в разделе "Примечания" применяется матрица с идентификатором M <sub>r</sub> .</span><span class="sxs-lookup"><span data-stu-id="1cef0-131">If this argument is **NULL**, an identity M<sub>r</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="1cef0-132">*птранслатион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1cef0-132">*pTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cef0-133">Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="1cef0-133">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="1cef0-134">Указатель на структуру D3DXVECTOR3, представляющую перевод.</span><span class="sxs-lookup"><span data-stu-id="1cef0-134">Pointer to a D3DXVECTOR3 structure, representing the translation.</span></span> <span data-ttu-id="1cef0-135">Если этот аргумент имеет **значение NULL**, к формуле в разделе "Примечания" применяется матрица-MT Identity.</span><span class="sxs-lookup"><span data-stu-id="1cef0-135">If this argument is **NULL**, an identity Mₜ matrix is applied to the formula in Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1cef0-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1cef0-136">Return value</span></span>

<span data-ttu-id="1cef0-137">Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="1cef0-137">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1cef0-138">Указатель на структуру D3DXMATRIX, которая является матрицей преобразования.</span><span class="sxs-lookup"><span data-stu-id="1cef0-138">Pointer to a D3DXMATRIX structure that is the transformation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="1cef0-139">Remarks</span><span class="sxs-lookup"><span data-stu-id="1cef0-139">Remarks</span></span>

<span data-ttu-id="1cef0-140">Эта функция вычисляет матрицу преобразования с помощью следующей формулы, при этом сцепление матрицы вычисляется в порядке слева направо:</span><span class="sxs-lookup"><span data-stu-id="1cef0-140">This function calculates the transformation matrix with the following formula, with matrix concatenation evaluated in left-to-right order:</span></span>

<span data-ttu-id="1cef0-141">M<sub>out</sub> = (m<sub>SC</sub>) ⁻ ¹ \* (m<sub>SR</sub>) ⁻ ¹ \* MS \* M<sub>SR</sub> \* M<sub>SC</sub> \* (m<sub>RC</sub>) ⁻ ¹ \* m<sub>r</sub> \* m<sub>RC</sub> \* MT</span><span class="sxs-lookup"><span data-stu-id="1cef0-141">M<sub>out</sub> = (M<sub>sc</sub>)⁻¹ \* (M<sub>sr</sub>)⁻¹\* Mₛ \* M<sub>sr</sub> \* M<sub>sc</sub> \* (M<sub>rc</sub>)⁻¹\* M<sub>r</sub> \* M<sub>rc</sub> \* Mt</span></span>

<span data-ttu-id="1cef0-142">где:</span><span class="sxs-lookup"><span data-stu-id="1cef0-142">where:</span></span>

<span data-ttu-id="1cef0-143">M<sub>out</sub> = выходная матрица (Тоска)</span><span class="sxs-lookup"><span data-stu-id="1cef0-143">M<sub>out</sub> = output matrix (pOut)</span></span>

<span data-ttu-id="1cef0-144">M<sub>SC</sub> = матрица центра масштабирования (пскалингцентер)</span><span class="sxs-lookup"><span data-stu-id="1cef0-144">M<sub>sc</sub> = scaling center matrix (pScalingCenter)</span></span>

<span data-ttu-id="1cef0-145">M<sub>SR</sub> = матрица вращения масштабирования (пскалингротатион)</span><span class="sxs-lookup"><span data-stu-id="1cef0-145">M<sub>sr</sub> = scaling rotation matrix (pScalingRotation)</span></span>

<span data-ttu-id="1cef0-146">Матрица MS = масштабирования (Пскалинг)</span><span class="sxs-lookup"><span data-stu-id="1cef0-146">Mₛ = scaling matrix (pScaling)</span></span>

<span data-ttu-id="1cef0-147">M<sub>RC</sub> = центр матрицы вращения (протатионцентер)</span><span class="sxs-lookup"><span data-stu-id="1cef0-147">M<sub>rc</sub> = center of rotation matrix (pRotationCenter)</span></span>

<span data-ttu-id="1cef0-148">M<sub>r</sub> = матрица вращения (расведение)</span><span class="sxs-lookup"><span data-stu-id="1cef0-148">M<sub>r</sub> = rotation matrix (pRotation)</span></span>

<span data-ttu-id="1cef0-149">MT = матрица перевода (Птранслатион)</span><span class="sxs-lookup"><span data-stu-id="1cef0-149">Mₜ = translation matrix (pTranslation)</span></span>

<span data-ttu-id="1cef0-150">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="1cef0-150">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="1cef0-151">Таким образом, функция D3DXMatrixTransformation может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="1cef0-151">In this way, the D3DXMatrixTransformation function can be used as a parameter for another function.</span></span>

<span data-ttu-id="1cef0-152">Для двумерных преобразований используйте [**D3DXMatrixTransformation2D**](d3d10-d3dxmatrixtransformation2d.md).</span><span class="sxs-lookup"><span data-stu-id="1cef0-152">For 2D transformations, use [**D3DXMatrixTransformation2D**](d3d10-d3dxmatrixtransformation2d.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1cef0-153">Требования</span><span class="sxs-lookup"><span data-stu-id="1cef0-153">Requirements</span></span>



| <span data-ttu-id="1cef0-154">Требование</span><span class="sxs-lookup"><span data-stu-id="1cef0-154">Requirement</span></span> | <span data-ttu-id="1cef0-155">Значение</span><span class="sxs-lookup"><span data-stu-id="1cef0-155">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1cef0-156">Header</span><span class="sxs-lookup"><span data-stu-id="1cef0-156">Header</span></span><br/>  | <dl> <span data-ttu-id="1cef0-157"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="1cef0-157"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="1cef0-158">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1cef0-158">Library</span></span><br/> | <dl> <span data-ttu-id="1cef0-159"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1cef0-159"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1cef0-160">См. также</span><span class="sxs-lookup"><span data-stu-id="1cef0-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cef0-161">Математические функции</span><span class="sxs-lookup"><span data-stu-id="1cef0-161">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
