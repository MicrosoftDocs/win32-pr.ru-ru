---
description: Строит матрицу 2D-преобразования в плоскости XY. Аргументы NULL обрабатываются как преобразования Identity.
ms.assetid: 335de919-ae4d-405d-b6bb-ca6bdc2d568a
title: Функция D3DXMatrixAffineTransformation2D (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a6edd0658eb80ec53d19b6c136a672cb78a2087b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703743"
---
# <a name="d3dxmatrixaffinetransformation2d-function-d3dx9mathh"></a><span data-ttu-id="1471f-104">Функция D3DXMatrixAffineTransformation2D (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="1471f-104">D3DXMatrixAffineTransformation2D function (D3dx9math.h)</span></span>

<span data-ttu-id="1471f-105">Строит матрицу 2D-преобразования в плоскости XY.</span><span class="sxs-lookup"><span data-stu-id="1471f-105">Builds a 2D affine transformation matrix in the xy plane.</span></span> <span data-ttu-id="1471f-106">Аргументы **null** обрабатываются как преобразования Identity.</span><span class="sxs-lookup"><span data-stu-id="1471f-106">**NULL** arguments are treated as identity transformations.</span></span>

## <a name="syntax"></a><span data-ttu-id="1471f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1471f-107">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixAffineTransformation2D(
  _Inout_       D3DXMATRIX  *pOut,
  _In_          FLOAT       Scaling,
  _In_    const D3DXVECTOR2 *pRotationCenter,
  _In_          FLOAT       Rotation,
  _In_    const D3DXVECTOR2 *pTranslation
);
```



## <a name="parameters"></a><span data-ttu-id="1471f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="1471f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1471f-109">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="1471f-109">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1471f-110">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="1471f-110">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1471f-111">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="1471f-111">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="1471f-112">*Масштабирование* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1471f-112">*Scaling* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1471f-113">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1471f-113">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1471f-114">Коэффициент масштабирования.</span><span class="sxs-lookup"><span data-stu-id="1471f-114">Scaling factor.</span></span>

</dd> <dt>

<span data-ttu-id="1471f-115">*протатионцентер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1471f-115">*pRotationCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1471f-116">Тип: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="1471f-116">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="1471f-117">Указатель на структуру [**D3DXVECTOR2**](d3dxvector2.md) — точку, определяющую центр вращения.</span><span class="sxs-lookup"><span data-stu-id="1471f-117">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure, a point identifying the center of rotation.</span></span> <span data-ttu-id="1471f-118">Если этот аргумент имеет **значение NULL**, то к формуле в разделе "Примечания" применяется матрица версии-<sub>кандидата</sub> Identity M.</span><span class="sxs-lookup"><span data-stu-id="1471f-118">If this argument is **NULL**, an identity M<sub>rc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="1471f-119">*Вращение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1471f-119">*Rotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1471f-120">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1471f-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1471f-121">Угол поворота.</span><span class="sxs-lookup"><span data-stu-id="1471f-121">The angle of rotation.</span></span>

</dd> <dt>

<span data-ttu-id="1471f-122">*птранслатион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1471f-122">*pTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1471f-123">Тип: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="1471f-123">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="1471f-124">Указатель на структуру [**D3DXVECTOR2**](d3dxvector2.md) , представляющую перевод.</span><span class="sxs-lookup"><span data-stu-id="1471f-124">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure, representing the translation.</span></span> <span data-ttu-id="1471f-125">Если этот аргумент имеет **значение NULL**, к формуле в разделе "Примечания" применяется матрица-MT Identity.</span><span class="sxs-lookup"><span data-stu-id="1471f-125">If this argument is **NULL**, an identity Mₜ matrix is applied to the formula in Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1471f-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1471f-126">Return value</span></span>

<span data-ttu-id="1471f-127">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="1471f-127">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1471f-128">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , которая является матрицей аффинного преобразования.</span><span class="sxs-lookup"><span data-stu-id="1471f-128">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is an affine transformation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="1471f-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1471f-129">Remarks</span></span>

<span data-ttu-id="1471f-130">Эта функция вычисляет матрицу аффинных преобразований с помощью следующей формулы, при этом сцепление матрицы вычисляется в порядке слева направо:</span><span class="sxs-lookup"><span data-stu-id="1471f-130">This function calculates the affine transformation matrix with the following formula, with matrix concatenation evaluated in left-to-right order:</span></span>

<span data-ttu-id="1471f-131">M<sub>out</sub> = MS \* (M<sub>RC</sub>) ⁻ ¹ \* m<sub>r</sub> \* m<sub>RC</sub> \* MT</span><span class="sxs-lookup"><span data-stu-id="1471f-131">M<sub>out</sub> = Mₛ \* (M<sub>rc</sub>)⁻¹ \* M<sub>r</sub> \* M<sub>rc</sub> \* Mₜ</span></span>

<span data-ttu-id="1471f-132">где:</span><span class="sxs-lookup"><span data-stu-id="1471f-132">where:</span></span>

<span data-ttu-id="1471f-133">M <sub>out</sub> = выходная матрица (*тоска*)</span><span class="sxs-lookup"><span data-stu-id="1471f-133">M <sub>out</sub> = output matrix (*pOut*)</span></span>

<span data-ttu-id="1471f-134">MS = матрица масштабирования (*масштабирование*)</span><span class="sxs-lookup"><span data-stu-id="1471f-134">Mₛ = scaling matrix (*Scaling*)</span></span>

<span data-ttu-id="1471f-135">M <sub>RC</sub> = центр матрицы вращения (*протатионцентер*)</span><span class="sxs-lookup"><span data-stu-id="1471f-135">M <sub>rc</sub> = center of rotation matrix (*pRotationCenter*)</span></span>

<span data-ttu-id="1471f-136">M <sub>r</sub> = матрица вращения (*вращение*)</span><span class="sxs-lookup"><span data-stu-id="1471f-136">M <sub>r</sub> = rotation matrix (*Rotation*)</span></span>

<span data-ttu-id="1471f-137">MT = матрица перевода (*птранслатион*)</span><span class="sxs-lookup"><span data-stu-id="1471f-137">Mₜ = translation matrix (*pTranslation*)</span></span>

<span data-ttu-id="1471f-138">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="1471f-138">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="1471f-139">Таким образом, функция **D3DXMatrixAffineTransformation2D** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="1471f-139">In this way, the **D3DXMatrixAffineTransformation2D** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="1471f-140">Для трехмерных преобразований используйте [**D3DXMatrixAffineTransformation**](d3dxmatrixaffinetransformation.md).</span><span class="sxs-lookup"><span data-stu-id="1471f-140">For 3D affine transformations, use [**D3DXMatrixAffineTransformation**](d3dxmatrixaffinetransformation.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1471f-141">Требования</span><span class="sxs-lookup"><span data-stu-id="1471f-141">Requirements</span></span>



| <span data-ttu-id="1471f-142">Требование</span><span class="sxs-lookup"><span data-stu-id="1471f-142">Requirement</span></span> | <span data-ttu-id="1471f-143">Значение</span><span class="sxs-lookup"><span data-stu-id="1471f-143">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1471f-144">Header</span><span class="sxs-lookup"><span data-stu-id="1471f-144">Header</span></span><br/>  | <dl> <span data-ttu-id="1471f-145"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="1471f-145"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="1471f-146">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1471f-146">Library</span></span><br/> | <dl> <span data-ttu-id="1471f-147"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1471f-147"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1471f-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1471f-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1471f-149">Математические функции</span><span class="sxs-lookup"><span data-stu-id="1471f-149">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="1471f-150">**D3DXMatrixTransformation2D**</span><span class="sxs-lookup"><span data-stu-id="1471f-150">**D3DXMatrixTransformation2D**</span></span>](d3dxmatrixtransformation2d.md)
</dt> <dt>

[<span data-ttu-id="1471f-151">Преобразования (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="1471f-151">Transforms (Direct3D 9)</span></span>](transforms.md)
</dt> </dl>

 

 
