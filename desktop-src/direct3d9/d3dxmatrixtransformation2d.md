---
description: Формирует матрицу 2D-преобразования, представляющую преобразования в плоскости XY. Аргументы NULL обрабатываются как преобразования Identity.
ms.assetid: 671d3d67-b474-4fc1-9913-d21f05d66d9a
title: Функция D3DXMatrixTransformation2D (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixTransformation2D
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ead4d403917b5328776b33563bc477c28983d6ef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713659"
---
# <a name="d3dxmatrixtransformation2d-function-d3dx9mathh"></a><span data-ttu-id="776fd-104">Функция D3DXMatrixTransformation2D (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="776fd-104">D3DXMatrixTransformation2D function (D3dx9math.h)</span></span>

<span data-ttu-id="776fd-105">Формирует матрицу 2D-преобразования, представляющую преобразования в плоскости XY.</span><span class="sxs-lookup"><span data-stu-id="776fd-105">Builds a 2D transformation matrix that represents transformations in the xy plane.</span></span> <span data-ttu-id="776fd-106">Аргументы **null** обрабатываются как преобразования Identity.</span><span class="sxs-lookup"><span data-stu-id="776fd-106">**NULL** arguments are treated as identity transformations.</span></span>

## <a name="syntax"></a><span data-ttu-id="776fd-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="776fd-107">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixTransformation2D(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR2 *pScalingCenter,
  _In_          FLOAT       pScalingRotation,
  _In_    const D3DXVECTOR2 *pScaling,
  _In_    const D3DXVECTOR2 *pRotationCenter,
  _In_          FLOAT       Rotation,
  _In_    const D3DXVECTOR2 *pTranslation
);
```



## <a name="parameters"></a><span data-ttu-id="776fd-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="776fd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="776fd-109">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="776fd-109">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="776fd-110">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="776fd-110">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="776fd-111">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , содержащую результат преобразований.</span><span class="sxs-lookup"><span data-stu-id="776fd-111">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that contains the result of the transformations.</span></span>

</dd> <dt>

<span data-ttu-id="776fd-112">*пскалингцентер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="776fd-112">*pScalingCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="776fd-113">Тип: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="776fd-113">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="776fd-114">Указатель на структуру [**D3DXVECTOR2**](d3dxvector2.md) — точку, определяющую центр масштабирования.</span><span class="sxs-lookup"><span data-stu-id="776fd-114">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure, a point identifying the scaling center.</span></span> <span data-ttu-id="776fd-115">Если этот аргумент имеет **значение NULL**, к формуле в разделе "Примечания" применяется матрица Identity M <sub>SC</sub> .</span><span class="sxs-lookup"><span data-stu-id="776fd-115">If this argument is **NULL**, an identity M<sub>sc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="776fd-116">*пскалингротатион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="776fd-116">*pScalingRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="776fd-117">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="776fd-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="776fd-118">Коэффициент поворота масштабирования.</span><span class="sxs-lookup"><span data-stu-id="776fd-118">The scaling rotation factor.</span></span>

</dd> <dt>

<span data-ttu-id="776fd-119">*пскалинг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="776fd-119">*pScaling* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="776fd-120">Тип: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="776fd-120">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="776fd-121">Указатель на структуру [**D3DXVECTOR2**](d3dxvector2.md) — точку, определяющую масштаб.</span><span class="sxs-lookup"><span data-stu-id="776fd-121">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure, a point identifying the scale.</span></span> <span data-ttu-id="776fd-122">Если этот аргумент имеет **значение NULL**, к формуле в примечаниях применяется удостоверение MS Matrix.</span><span class="sxs-lookup"><span data-stu-id="776fd-122">If this argument is **NULL**, an identity Mₛ matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="776fd-123">*протатионцентер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="776fd-123">*pRotationCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="776fd-124">Тип: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="776fd-124">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="776fd-125">Указатель на структуру [**D3DXVECTOR2**](d3dxvector2.md) — точку, определяющую центр вращения.</span><span class="sxs-lookup"><span data-stu-id="776fd-125">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure, a point identifying the rotation center.</span></span> <span data-ttu-id="776fd-126">Если этот аргумент имеет **значение NULL**, то к формуле в разделе "Примечания" применяется матрица версии-<sub>кандидата</sub> Identity M.</span><span class="sxs-lookup"><span data-stu-id="776fd-126">If this argument is **NULL**, an identity M<sub>rc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="776fd-127">*Вращение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="776fd-127">*Rotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="776fd-128">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="776fd-128">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="776fd-129">Угол поворота в радианах.</span><span class="sxs-lookup"><span data-stu-id="776fd-129">The angle of rotation in radians.</span></span>

</dd> <dt>

<span data-ttu-id="776fd-130">*птранслатион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="776fd-130">*pTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="776fd-131">Тип: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="776fd-131">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="776fd-132">Указатель на структуру [**D3DXVECTOR2**](d3dxvector2.md) , идентифицирующую перевод.</span><span class="sxs-lookup"><span data-stu-id="776fd-132">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure, identifying the translation.</span></span> <span data-ttu-id="776fd-133">Если этот аргумент имеет **значение NULL**, к формуле в разделе "Примечания" применяется матрица-MT Identity.</span><span class="sxs-lookup"><span data-stu-id="776fd-133">If this argument is **NULL**, an identity Mₜ matrix is applied to the formula in Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="776fd-134">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="776fd-134">Return value</span></span>

<span data-ttu-id="776fd-135">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="776fd-135">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="776fd-136">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , содержащую матрицу преобразования.</span><span class="sxs-lookup"><span data-stu-id="776fd-136">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that contains the transformation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="776fd-137">Комментарии</span><span class="sxs-lookup"><span data-stu-id="776fd-137">Remarks</span></span>

<span data-ttu-id="776fd-138">Эта функция вычисляет матрицу преобразования с помощью следующей формулы, при этом сцепление матрицы вычисляется в порядке слева направо:</span><span class="sxs-lookup"><span data-stu-id="776fd-138">This function calculates the transformation matrix with the following formula, with matrix concatenation evaluated in left-to-right order:</span></span>

<span data-ttu-id="776fd-139">M<sub>out</sub> = (m<sub>SC</sub>) ⁻ ¹ \* (m<sub>SR</sub>) ⁻ ¹ \* MS \* M<sub>SR</sub> \* M<sub>SC</sub> \* (m<sub>RC</sub>) ⁻ ¹ \* m<sub>r</sub> \* m<sub>RC</sub> \* MT</span><span class="sxs-lookup"><span data-stu-id="776fd-139">M<sub>out</sub> = (M<sub>sc</sub>)⁻¹\* (M<sub>sr</sub>)⁻¹\* Mₛ \* M<sub>sr</sub> \* M<sub>sc</sub> \* (M<sub>rc</sub>)⁻¹\* M<sub>r</sub> \* M<sub>rc</sub> \* Mₜ</span></span>

<span data-ttu-id="776fd-140">где:</span><span class="sxs-lookup"><span data-stu-id="776fd-140">where:</span></span>

<span data-ttu-id="776fd-141">M <sub>out</sub> = выходная матрица (*тоска*)</span><span class="sxs-lookup"><span data-stu-id="776fd-141">M <sub>out</sub> = output matrix (*pOut*)</span></span>

<span data-ttu-id="776fd-142">M <sub>SC</sub> = матрица центра масштабирования (*пскалингцентер*)</span><span class="sxs-lookup"><span data-stu-id="776fd-142">M <sub>sc</sub> = scaling center matrix (*pScalingCenter*)</span></span>

<span data-ttu-id="776fd-143">M <sub>SR</sub> = матрица вращения масштабирования (*пскалингротатион*)</span><span class="sxs-lookup"><span data-stu-id="776fd-143">M <sub>sr</sub> = scaling rotation matrix (*pScalingRotation*)</span></span>

<span data-ttu-id="776fd-144">Матрица MS = масштабирования (*пскалинг*)</span><span class="sxs-lookup"><span data-stu-id="776fd-144">Mₛ = scaling matrix (*pScaling*)</span></span>

<span data-ttu-id="776fd-145">M <sub>RC</sub> = центр матрицы вращения (*протатионцентер*)</span><span class="sxs-lookup"><span data-stu-id="776fd-145">M <sub>rc</sub> = center of rotation matrix (*pRotationCenter*)</span></span>

<span data-ttu-id="776fd-146">M <sub>r</sub> = матрица вращения (*вращение*)</span><span class="sxs-lookup"><span data-stu-id="776fd-146">M <sub>r</sub> = rotation matrix (*Rotation*)</span></span>

<span data-ttu-id="776fd-147">MT = матрица перевода (*птранслатион*)</span><span class="sxs-lookup"><span data-stu-id="776fd-147">Mₜ = translation matrix (*pTranslation*)</span></span>

<span data-ttu-id="776fd-148">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="776fd-148">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="776fd-149">Таким образом, функция **D3DXMatrixTransformation2D** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="776fd-149">In this way, the **D3DXMatrixTransformation2D** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="776fd-150">Для трехмерных преобразований используйте [**D3DXMatrixTransformation**](d3dxmatrixtransformation.md).</span><span class="sxs-lookup"><span data-stu-id="776fd-150">For 3D transformations, use [**D3DXMatrixTransformation**](d3dxmatrixtransformation.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="776fd-151">Требования</span><span class="sxs-lookup"><span data-stu-id="776fd-151">Requirements</span></span>



| <span data-ttu-id="776fd-152">Требование</span><span class="sxs-lookup"><span data-stu-id="776fd-152">Requirement</span></span> | <span data-ttu-id="776fd-153">Значение</span><span class="sxs-lookup"><span data-stu-id="776fd-153">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="776fd-154">Header</span><span class="sxs-lookup"><span data-stu-id="776fd-154">Header</span></span><br/>  | <dl> <span data-ttu-id="776fd-155"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="776fd-155"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="776fd-156">Библиотека</span><span class="sxs-lookup"><span data-stu-id="776fd-156">Library</span></span><br/> | <dl> <span data-ttu-id="776fd-157"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="776fd-157"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="776fd-158">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="776fd-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="776fd-159">Математические функции</span><span class="sxs-lookup"><span data-stu-id="776fd-159">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="776fd-160">**D3DXMatrixAffineTransformation2D**</span><span class="sxs-lookup"><span data-stu-id="776fd-160">**D3DXMatrixAffineTransformation2D**</span></span>](d3dxmatrixaffinetransformation2d.md)
</dt> <dt>

[<span data-ttu-id="776fd-161">Преобразования (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="776fd-161">Transforms (Direct3D 9)</span></span>](transforms.md)
</dt> </dl>

 

 
