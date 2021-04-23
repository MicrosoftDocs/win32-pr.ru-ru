---
description: Формирует матрицу преобразования. Аргументы NULL обрабатываются как преобразования Identity.
ms.assetid: 39042fc6-f489-4e44-ad3f-858ca395575d
title: Функция D3DXMatrixTransformation (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f2174329e01e3e624ef27608ca56b33181b770db
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104081842"
---
# <a name="d3dxmatrixtransformation-function-d3dx9mathh"></a><span data-ttu-id="002f9-104">Функция D3DXMatrixTransformation (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="002f9-104">D3DXMatrixTransformation function (D3dx9math.h)</span></span>

<span data-ttu-id="002f9-105">Формирует матрицу преобразования.</span><span class="sxs-lookup"><span data-stu-id="002f9-105">Builds a transformation matrix.</span></span> <span data-ttu-id="002f9-106">Аргументы **null** обрабатываются как преобразования Identity.</span><span class="sxs-lookup"><span data-stu-id="002f9-106">**NULL** arguments are treated as identity transformations.</span></span>

## <a name="syntax"></a><span data-ttu-id="002f9-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="002f9-107">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="002f9-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="002f9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="002f9-109">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="002f9-109">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="002f9-110">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="002f9-110">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="002f9-111">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="002f9-111">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="002f9-112">*пскалингцентер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="002f9-112">*pScalingCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="002f9-113">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="002f9-113">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="002f9-114">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , определяющую центральную точку масштабирования.</span><span class="sxs-lookup"><span data-stu-id="002f9-114">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, identifying the scaling center point.</span></span> <span data-ttu-id="002f9-115">Если этот аргумент имеет **значение NULL**, к формуле в разделе "Примечания" применяется матрица Identity M <sub>SC</sub> .</span><span class="sxs-lookup"><span data-stu-id="002f9-115">If this argument is **NULL**, an identity M<sub>sc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="002f9-116">*пскалингротатион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="002f9-116">*pScalingRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="002f9-117">Тип: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="002f9-117">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="002f9-118">Указатель на структуру [**D3DXQUATERNION**](d3dxquaternion.md) , указывающую поворот масштабирования.</span><span class="sxs-lookup"><span data-stu-id="002f9-118">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that specifies the scaling rotation.</span></span> <span data-ttu-id="002f9-119">Если этот аргумент имеет **значение NULL**, то к формуле в разделе "Примечания" применяется матрица с идентификатором M <sub>SR</sub> .</span><span class="sxs-lookup"><span data-stu-id="002f9-119">If this argument is **NULL**, an identity M<sub>sr</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="002f9-120">*пскалинг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="002f9-120">*pScaling* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="002f9-121">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="002f9-121">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="002f9-122">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , вектор масштабирования.</span><span class="sxs-lookup"><span data-stu-id="002f9-122">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, the scaling vector.</span></span> <span data-ttu-id="002f9-123">Если этот аргумент имеет **значение NULL**, к формуле в примечаниях применяется удостоверение MS Matrix.</span><span class="sxs-lookup"><span data-stu-id="002f9-123">If this argument is **NULL**, an identity Mₛ matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="002f9-124">*протатионцентер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="002f9-124">*pRotationCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="002f9-125">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="002f9-125">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="002f9-126">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) — точку, определяющую центр вращения.</span><span class="sxs-lookup"><span data-stu-id="002f9-126">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, a point that identifies the center of rotation.</span></span> <span data-ttu-id="002f9-127">Если этот аргумент имеет **значение NULL**, то к формуле в разделе "Примечания" применяется матрица версии-<sub>кандидата</sub> Identity M.</span><span class="sxs-lookup"><span data-stu-id="002f9-127">If this argument is **NULL**, an identity M<sub>rc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="002f9-128"> \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="002f9-128">*pRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="002f9-129">Тип: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="002f9-129">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="002f9-130">Указатель на структуру [**D3DXQUATERNION**](d3dxquaternion.md) , указывающую поворот.</span><span class="sxs-lookup"><span data-stu-id="002f9-130">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that specifies the rotation.</span></span> <span data-ttu-id="002f9-131">Если этот аргумент имеет **значение NULL**, к формуле в разделе "Примечания" применяется матрица с идентификатором M <sub>r</sub> .</span><span class="sxs-lookup"><span data-stu-id="002f9-131">If this argument is **NULL**, an identity M<sub>r</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="002f9-132">*птранслатион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="002f9-132">*pTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="002f9-133">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="002f9-133">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="002f9-134">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , представляющую перевод.</span><span class="sxs-lookup"><span data-stu-id="002f9-134">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, representing the translation.</span></span> <span data-ttu-id="002f9-135">Если этот аргумент имеет **значение NULL**, к формуле в разделе "Примечания" применяется матрица-MT Identity.</span><span class="sxs-lookup"><span data-stu-id="002f9-135">If this argument is **NULL**, an identity Mₜ matrix is applied to the formula in Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="002f9-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="002f9-136">Return value</span></span>

<span data-ttu-id="002f9-137">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="002f9-137">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="002f9-138">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , которая является матрицей преобразования.</span><span class="sxs-lookup"><span data-stu-id="002f9-138">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is the transformation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="002f9-139">Комментарии</span><span class="sxs-lookup"><span data-stu-id="002f9-139">Remarks</span></span>

<span data-ttu-id="002f9-140">Эта функция вычисляет матрицу преобразования с помощью следующей формулы, при этом сцепление матрицы вычисляется в порядке слева направо:</span><span class="sxs-lookup"><span data-stu-id="002f9-140">This function calculates the transformation matrix with the following formula, with matrix concatenation evaluated in left-to-right order:</span></span>

<span data-ttu-id="002f9-141">M<sub>out</sub> = (m<sub>SC</sub>) ⁻ ¹ \* (m<sub>SR</sub>) ⁻ ¹ \* MS \* M<sub>SR</sub> \* M<sub>SC</sub> \* (m<sub>RC</sub>) ⁻ ¹ \* m<sub>r</sub> \* m<sub>RC</sub> \* MT</span><span class="sxs-lookup"><span data-stu-id="002f9-141">M<sub>out</sub> = (M<sub>sc</sub>)⁻¹ \* (M<sub>sr</sub>)⁻¹\* Mₛ \* M<sub>sr</sub> \* M<sub>sc</sub> \* (M<sub>rc</sub>)⁻¹\* M<sub>r</sub> \* M<sub>rc</sub> \* Mt</span></span>

<span data-ttu-id="002f9-142">где:</span><span class="sxs-lookup"><span data-stu-id="002f9-142">where:</span></span>

<span data-ttu-id="002f9-143">M <sub>out</sub> = выходная матрица (*тоска*)</span><span class="sxs-lookup"><span data-stu-id="002f9-143">M <sub>out</sub> = output matrix (*pOut*)</span></span>

<span data-ttu-id="002f9-144">M <sub>SC</sub> = матрица центра масштабирования (*пскалингцентер*)</span><span class="sxs-lookup"><span data-stu-id="002f9-144">M <sub>sc</sub> = scaling center matrix (*pScalingCenter*)</span></span>

<span data-ttu-id="002f9-145">M <sub>SR</sub> = матрица вращения масштабирования (*пскалингротатион*)</span><span class="sxs-lookup"><span data-stu-id="002f9-145">M <sub>sr</sub> = scaling rotation matrix (*pScalingRotation*)</span></span>

<span data-ttu-id="002f9-146">Матрица MS = масштабирования (*пскалинг*)</span><span class="sxs-lookup"><span data-stu-id="002f9-146">Mₛ = scaling matrix (*pScaling*)</span></span>

<span data-ttu-id="002f9-147">M <sub>RC</sub> = центр матрицы вращения (*протатионцентер*)</span><span class="sxs-lookup"><span data-stu-id="002f9-147">M <sub>rc</sub> = center of rotation matrix (*pRotationCenter*)</span></span>

<span data-ttu-id="002f9-148">M <sub>r</sub> = матрица вращения *(* расведение)</span><span class="sxs-lookup"><span data-stu-id="002f9-148">M <sub>r</sub> = rotation matrix (*pRotation*)</span></span>

<span data-ttu-id="002f9-149">MT = матрица перевода (*птранслатион*)</span><span class="sxs-lookup"><span data-stu-id="002f9-149">Mₜ = translation matrix (*pTranslation*)</span></span>

<span data-ttu-id="002f9-150">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="002f9-150">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="002f9-151">Таким образом, функция **D3DXMatrixTransformation** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="002f9-151">In this way, the **D3DXMatrixTransformation** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="002f9-152">Для двумерных преобразований используйте [**D3DXMatrixTransformation2D**](d3dxmatrixtransformation2d.md).</span><span class="sxs-lookup"><span data-stu-id="002f9-152">For 2D transformations, use [**D3DXMatrixTransformation2D**](d3dxmatrixtransformation2d.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="002f9-153">Требования</span><span class="sxs-lookup"><span data-stu-id="002f9-153">Requirements</span></span>



| <span data-ttu-id="002f9-154">Требование</span><span class="sxs-lookup"><span data-stu-id="002f9-154">Requirement</span></span> | <span data-ttu-id="002f9-155">Значение</span><span class="sxs-lookup"><span data-stu-id="002f9-155">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="002f9-156">Header</span><span class="sxs-lookup"><span data-stu-id="002f9-156">Header</span></span><br/>  | <dl> <span data-ttu-id="002f9-157"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="002f9-157"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="002f9-158">Библиотека</span><span class="sxs-lookup"><span data-stu-id="002f9-158">Library</span></span><br/> | <dl> <span data-ttu-id="002f9-159"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="002f9-159"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="002f9-160">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="002f9-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="002f9-161">Математические функции</span><span class="sxs-lookup"><span data-stu-id="002f9-161">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="002f9-162">**D3DXMatrixAffineTransformation**</span><span class="sxs-lookup"><span data-stu-id="002f9-162">**D3DXMatrixAffineTransformation**</span></span>](d3dxmatrixaffinetransformation.md)
</dt> <dt>

[<span data-ttu-id="002f9-163">Преобразования (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="002f9-163">Transforms (Direct3D 9)</span></span>](transforms.md)
</dt> </dl>

 

 




