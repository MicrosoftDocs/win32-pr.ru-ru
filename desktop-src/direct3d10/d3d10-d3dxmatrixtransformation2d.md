---
description: Формирует матрицу 2D-преобразования, представляющую преобразования в плоскости XY. Аргументы NULL обрабатываются как преобразования Identity.
ms.assetid: 5b894c3b-a532-458a-bcbc-48fcd5c73c34
title: Функция D3DXMatrixTransformation2D (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: b41d8234dcd9dda1b3735c83460a20c7109e63d7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821388"
---
# <a name="d3dxmatrixtransformation2d-function-d3dx10mathh"></a><span data-ttu-id="b3fa8-104">Функция D3DXMatrixTransformation2D (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="b3fa8-104">D3DXMatrixTransformation2D function (D3DX10Math.h)</span></span>

<span data-ttu-id="b3fa8-105">Формирует матрицу 2D-преобразования, представляющую преобразования в плоскости XY.</span><span class="sxs-lookup"><span data-stu-id="b3fa8-105">Builds a 2D transformation matrix that represents transformations in the xy plane.</span></span> <span data-ttu-id="b3fa8-106">Аргументы **null** обрабатываются как преобразования Identity.</span><span class="sxs-lookup"><span data-stu-id="b3fa8-106">**NULL** arguments are treated as identity transformations.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3fa8-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b3fa8-107">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixTransformation2D(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR2 *pScalingCenter,
  _In_          FLOAT       ScalingRotation,
  _In_    const D3DXVECTOR2 *pScaling,
  _In_    const D3DXVECTOR2 *pRotationCenter,
  _In_          FLOAT       Rotation,
  _In_    const D3DXVECTOR2 *pTranslation
);
```



## <a name="parameters"></a><span data-ttu-id="b3fa8-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b3fa8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3fa8-109">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="b3fa8-109">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b3fa8-110">Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="b3fa8-110">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="b3fa8-111">Указатель на структуру [**D3DXMATRIX**](d3d10-d3dxmatrix.md) , содержащую результат преобразований.</span><span class="sxs-lookup"><span data-stu-id="b3fa8-111">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that contains the result of the transformations.</span></span>

</dd> <dt>

<span data-ttu-id="b3fa8-112">*пскалингцентер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b3fa8-112">*pScalingCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3fa8-113">Тип: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="b3fa8-113">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="b3fa8-114">Указатель на [**D3DXVECTOR2**](d3d10-d3dxvector2.md), указывающий центр масштабирования.</span><span class="sxs-lookup"><span data-stu-id="b3fa8-114">Pointer to a [**D3DXVECTOR2**](d3d10-d3dxvector2.md), a point identifying the scaling center.</span></span> <span data-ttu-id="b3fa8-115">Если этот аргумент имеет **значение NULL**, к формуле в разделе "Примечания" применяется матрица Identity M <sub>SC</sub> .</span><span class="sxs-lookup"><span data-stu-id="b3fa8-115">If this argument is **NULL**, an identity M<sub>sc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="b3fa8-116">*Скалингротатион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b3fa8-116">*ScalingRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3fa8-117">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b3fa8-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b3fa8-118">Указатель на коэффициент поворота масштабирования.</span><span class="sxs-lookup"><span data-stu-id="b3fa8-118">Pointer to the scaling rotation factor.</span></span>

</dd> <dt>

<span data-ttu-id="b3fa8-119">*пскалинг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b3fa8-119">*pScaling* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3fa8-120">Тип: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="b3fa8-120">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="b3fa8-121">Указатель на структуру D3DXVECTOR2 — точку, определяющую масштаб.</span><span class="sxs-lookup"><span data-stu-id="b3fa8-121">Pointer to a D3DXVECTOR2 structure, a point identifying the scale.</span></span> <span data-ttu-id="b3fa8-122">Если этот аргумент имеет **значение NULL**, к формуле в примечаниях применяется удостоверение MS Matrix.</span><span class="sxs-lookup"><span data-stu-id="b3fa8-122">If this argument is **NULL**, an identity Mₛ matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="b3fa8-123">*протатионцентер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b3fa8-123">*pRotationCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3fa8-124">Тип: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="b3fa8-124">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="b3fa8-125">Указатель на структуру D3DXVECTOR2 — точку, определяющую центр вращения.</span><span class="sxs-lookup"><span data-stu-id="b3fa8-125">Pointer to a D3DXVECTOR2 structure, a point identifying the rotation center.</span></span> <span data-ttu-id="b3fa8-126">Если этот аргумент имеет **значение NULL**, то к формуле в разделе "Примечания" применяется матрица версии-<sub>кандидата</sub> Identity M.</span><span class="sxs-lookup"><span data-stu-id="b3fa8-126">If this argument is **NULL**, an identity M<sub>rc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="b3fa8-127">*Вращение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b3fa8-127">*Rotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3fa8-128">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b3fa8-128">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b3fa8-129">Угол поворота в радианах.</span><span class="sxs-lookup"><span data-stu-id="b3fa8-129">The angle of rotation in radians.</span></span>

</dd> <dt>

<span data-ttu-id="b3fa8-130">*птранслатион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b3fa8-130">*pTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3fa8-131">Тип: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="b3fa8-131">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="b3fa8-132">Указатель на структуру D3DXVECTOR2, идентифицирующую перевод.</span><span class="sxs-lookup"><span data-stu-id="b3fa8-132">Pointer to a D3DXVECTOR2 structure, identifying the translation.</span></span> <span data-ttu-id="b3fa8-133">Если этот аргумент имеет **значение NULL**, к формуле в разделе "Примечания" применяется матрица-MT Identity.</span><span class="sxs-lookup"><span data-stu-id="b3fa8-133">If this argument is **NULL**, an identity Mₜ matrix is applied to the formula in Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3fa8-134">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b3fa8-134">Return value</span></span>

<span data-ttu-id="b3fa8-135">Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="b3fa8-135">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="b3fa8-136">Указатель на структуру D3DXMATRIX, содержащую матрицу преобразования.</span><span class="sxs-lookup"><span data-stu-id="b3fa8-136">Pointer to a D3DXMATRIX structure that contains the transformation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3fa8-137">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b3fa8-137">Remarks</span></span>

<span data-ttu-id="b3fa8-138">Эта функция вычисляет матрицу преобразования с помощью следующей формулы, при этом сцепление матрицы вычисляется в порядке слева направо:</span><span class="sxs-lookup"><span data-stu-id="b3fa8-138">This function calculates the transformation matrix with the following formula, with matrix concatenation evaluated in left-to-right order:</span></span>

<span data-ttu-id="b3fa8-139">M<sub>out</sub> = (m<sub>SC</sub>) ⁻ ¹ \* (m<sub>SR</sub>) ⁻ ¹ \* MS \* M<sub>SR</sub> \* M<sub>SC</sub> \* (m<sub>RC</sub>) ⁻ ¹ \* m<sub>r</sub> \* m<sub>RC</sub> \* MT</span><span class="sxs-lookup"><span data-stu-id="b3fa8-139">M<sub>out</sub> = (M<sub>sc</sub>)⁻¹\* (M<sub>sr</sub>)⁻¹\* Mₛ \* M<sub>sr</sub> \* M<sub>sc</sub> \* (M<sub>rc</sub>)⁻¹\* M<sub>r</sub> \* M<sub>rc</sub> \* Mₜ</span></span>

<span data-ttu-id="b3fa8-140">где:</span><span class="sxs-lookup"><span data-stu-id="b3fa8-140">where:</span></span>

<span data-ttu-id="b3fa8-141">M<sub>out</sub> = выходная матрица (Тоска)</span><span class="sxs-lookup"><span data-stu-id="b3fa8-141">M<sub>out</sub> = output matrix (pOut)</span></span>

<span data-ttu-id="b3fa8-142">M<sub>SC</sub> = матрица центра масштабирования (пскалингцентер)</span><span class="sxs-lookup"><span data-stu-id="b3fa8-142">M<sub>sc</sub> = scaling center matrix (pScalingCenter)</span></span>

<span data-ttu-id="b3fa8-143">M<sub>SR</sub> = матрица вращения масштабирования (пскалингротатион)</span><span class="sxs-lookup"><span data-stu-id="b3fa8-143">M<sub>sr</sub> = scaling rotation matrix (pScalingRotation)</span></span>

<span data-ttu-id="b3fa8-144">Матрица MS = масштабирования (Пскалинг)</span><span class="sxs-lookup"><span data-stu-id="b3fa8-144">Mₛ = scaling matrix (pScaling)</span></span>

<span data-ttu-id="b3fa8-145">M<sub>RC</sub> = центр матрицы вращения (протатионцентер)</span><span class="sxs-lookup"><span data-stu-id="b3fa8-145">M<sub>rc</sub> = center of rotation matrix (pRotationCenter)</span></span>

<span data-ttu-id="b3fa8-146">M<sub>r</sub> = матрица вращения (вращение)</span><span class="sxs-lookup"><span data-stu-id="b3fa8-146">M<sub>r</sub> = rotation matrix (Rotation)</span></span>

<span data-ttu-id="b3fa8-147">MT = матрица перевода (Птранслатион)</span><span class="sxs-lookup"><span data-stu-id="b3fa8-147">Mₜ = translation matrix (pTranslation)</span></span>

<span data-ttu-id="b3fa8-148">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="b3fa8-148">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="b3fa8-149">Таким образом, функция D3DXMatrixTransformation2D может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="b3fa8-149">In this way, the D3DXMatrixTransformation2D function can be used as a parameter for another function.</span></span>

<span data-ttu-id="b3fa8-150">Для трехмерных преобразований используйте [**D3DXMatrixTransformation**](d3d10-d3dxmatrixtransformation.md).</span><span class="sxs-lookup"><span data-stu-id="b3fa8-150">For 3D transformations, use [**D3DXMatrixTransformation**](d3d10-d3dxmatrixtransformation.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b3fa8-151">Требования</span><span class="sxs-lookup"><span data-stu-id="b3fa8-151">Requirements</span></span>



| <span data-ttu-id="b3fa8-152">Требование</span><span class="sxs-lookup"><span data-stu-id="b3fa8-152">Requirement</span></span> | <span data-ttu-id="b3fa8-153">Значение</span><span class="sxs-lookup"><span data-stu-id="b3fa8-153">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b3fa8-154">Header</span><span class="sxs-lookup"><span data-stu-id="b3fa8-154">Header</span></span><br/>  | <dl> <span data-ttu-id="b3fa8-155"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3fa8-155"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="b3fa8-156">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b3fa8-156">Library</span></span><br/> | <dl> <span data-ttu-id="b3fa8-157"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b3fa8-157"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b3fa8-158">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b3fa8-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3fa8-159">Математические функции</span><span class="sxs-lookup"><span data-stu-id="b3fa8-159">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
