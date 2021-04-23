---
description: Формирует матрицу трехмерного преобразования. Аргументы NULL обрабатываются как преобразования Identity.
ms.assetid: 54eac78f-57be-4a24-8dfb-0b519e97d6ca
title: Функция D3DXMatrixAffineTransformation (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 025485f0015e6f2d85851c8f0919f5462b2bdc3e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355440"
---
# <a name="d3dxmatrixaffinetransformation-function-d3dx9mathh"></a><span data-ttu-id="6adcc-104">Функция D3DXMatrixAffineTransformation (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="6adcc-104">D3DXMatrixAffineTransformation function (D3dx9math.h)</span></span>

<span data-ttu-id="6adcc-105">Формирует матрицу трехмерного преобразования.</span><span class="sxs-lookup"><span data-stu-id="6adcc-105">Builds a 3D affine transformation matrix.</span></span> <span data-ttu-id="6adcc-106">Аргументы **null** обрабатываются как преобразования Identity.</span><span class="sxs-lookup"><span data-stu-id="6adcc-106">**NULL** arguments are treated as identity transformations.</span></span>

## <a name="syntax"></a><span data-ttu-id="6adcc-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6adcc-107">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixAffineTransformation(
  _Inout_       D3DXMATRIX     *pOut,
  _In_          FLOAT          Scaling,
  _In_    const D3DXVECTOR3    *pRotationCenter,
  _In_    const D3DXQUATERNION *pRotation,
  _In_    const D3DXVECTOR3    *pTranslation
);
```



## <a name="parameters"></a><span data-ttu-id="6adcc-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6adcc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6adcc-109">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="6adcc-109">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6adcc-110">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="6adcc-110">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="6adcc-111">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="6adcc-111">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="6adcc-112">*Масштабирование* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6adcc-112">*Scaling* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6adcc-113">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6adcc-113">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6adcc-114">Коэффициент масштабирования.</span><span class="sxs-lookup"><span data-stu-id="6adcc-114">Scaling factor.</span></span>

</dd> <dt>

<span data-ttu-id="6adcc-115">*протатионцентер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6adcc-115">*pRotationCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6adcc-116">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="6adcc-116">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="6adcc-117">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) — точку, определяющую центр вращения.</span><span class="sxs-lookup"><span data-stu-id="6adcc-117">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, a point identifying the center of rotation.</span></span> <span data-ttu-id="6adcc-118">Если этот аргумент имеет **значение NULL**, то к формуле в разделе "Примечания" применяется матрица версии-<sub>кандидата</sub> Identity M.</span><span class="sxs-lookup"><span data-stu-id="6adcc-118">If this argument is **NULL**, an identity M<sub>rc</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="6adcc-119"> \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6adcc-119">*pRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6adcc-120">Тип: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="6adcc-120">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="6adcc-121">Указатель на структуру [**D3DXQUATERNION**](d3dxquaternion.md) , указывающую поворот.</span><span class="sxs-lookup"><span data-stu-id="6adcc-121">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that specifies the rotation.</span></span> <span data-ttu-id="6adcc-122">Если этот аргумент имеет **значение NULL**, к формуле в разделе "Примечания" применяется матрица с идентификатором M <sub>r</sub> .</span><span class="sxs-lookup"><span data-stu-id="6adcc-122">If this argument is **NULL**, an identity M<sub>r</sub> matrix is applied to the formula in Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="6adcc-123">*птранслатион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6adcc-123">*pTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6adcc-124">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="6adcc-124">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="6adcc-125">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , представляющую перевод.</span><span class="sxs-lookup"><span data-stu-id="6adcc-125">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure representing the translation.</span></span> <span data-ttu-id="6adcc-126">Если этот аргумент имеет **значение NULL**, к формуле в разделе "Примечания" применяется матрица-MT Identity.</span><span class="sxs-lookup"><span data-stu-id="6adcc-126">If this argument is **NULL**, an identity Mₜ matrix is applied to the formula in Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6adcc-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6adcc-127">Return value</span></span>

<span data-ttu-id="6adcc-128">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="6adcc-128">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="6adcc-129">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , которая является матрицей аффинного преобразования.</span><span class="sxs-lookup"><span data-stu-id="6adcc-129">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is an affine transformation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="6adcc-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6adcc-130">Remarks</span></span>

<span data-ttu-id="6adcc-131">Эта функция вычисляет матрицу аффинных преобразований с помощью следующей формулы, при этом сцепление матрицы вычисляется в порядке слева направо:</span><span class="sxs-lookup"><span data-stu-id="6adcc-131">This function calculates the affine transformation matrix with the following formula, with matrix concatenation evaluated in left-to-right order:</span></span>

<span data-ttu-id="6adcc-132">M<sub>out</sub> = MS \* (M<sub>RC</sub>) ⁻ ¹ \* m<sub>r</sub> \* m<sub>RC</sub> \* MT</span><span class="sxs-lookup"><span data-stu-id="6adcc-132">M<sub>out</sub> = Mₛ \* (M<sub>rc</sub>)⁻¹ \* M<sub>r</sub> \* M<sub>rc</sub> \* Mₜ</span></span>

<span data-ttu-id="6adcc-133">где:</span><span class="sxs-lookup"><span data-stu-id="6adcc-133">where:</span></span>

<span data-ttu-id="6adcc-134">M <sub>out</sub> = выходная матрица (*тоска*)</span><span class="sxs-lookup"><span data-stu-id="6adcc-134">M <sub>out</sub> = output matrix (*pOut*)</span></span>

<span data-ttu-id="6adcc-135">MS = матрица масштабирования (*масштабирование*)</span><span class="sxs-lookup"><span data-stu-id="6adcc-135">Mₛ = scaling matrix (*Scaling*)</span></span>

<span data-ttu-id="6adcc-136">M <sub>RC</sub> = центр матрицы вращения (*протатионцентер*)</span><span class="sxs-lookup"><span data-stu-id="6adcc-136">M <sub>rc</sub> = center of rotation matrix (*pRotationCenter*)</span></span>

<span data-ttu-id="6adcc-137">M <sub>r</sub> = матрица вращения *(* расведение)</span><span class="sxs-lookup"><span data-stu-id="6adcc-137">M <sub>r</sub> = rotation matrix (*pRotation*)</span></span>

<span data-ttu-id="6adcc-138">MT = матрица перевода (*птранслатион*)</span><span class="sxs-lookup"><span data-stu-id="6adcc-138">Mₜ = translation matrix (*pTranslation*)</span></span>

<span data-ttu-id="6adcc-139">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="6adcc-139">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="6adcc-140">Таким образом, функция **D3DXMatrixAffineTransformation** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="6adcc-140">In this way, the **D3DXMatrixAffineTransformation** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="6adcc-141">Для двумерных преобразований 2D используйте [**D3DXMatrixAffineTransformation2D**](d3dxmatrixaffinetransformation2d.md).</span><span class="sxs-lookup"><span data-stu-id="6adcc-141">For 2D affine transformations, use [**D3DXMatrixAffineTransformation2D**](d3dxmatrixaffinetransformation2d.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6adcc-142">Требования</span><span class="sxs-lookup"><span data-stu-id="6adcc-142">Requirements</span></span>



| <span data-ttu-id="6adcc-143">Требование</span><span class="sxs-lookup"><span data-stu-id="6adcc-143">Requirement</span></span> | <span data-ttu-id="6adcc-144">Значение</span><span class="sxs-lookup"><span data-stu-id="6adcc-144">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6adcc-145">Header</span><span class="sxs-lookup"><span data-stu-id="6adcc-145">Header</span></span><br/>  | <dl> <span data-ttu-id="6adcc-146"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="6adcc-146"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="6adcc-147">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6adcc-147">Library</span></span><br/> | <dl> <span data-ttu-id="6adcc-148"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6adcc-148"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6adcc-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6adcc-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6adcc-150">Математические функции</span><span class="sxs-lookup"><span data-stu-id="6adcc-150">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="6adcc-151">**D3DXMatrixTransformation**</span><span class="sxs-lookup"><span data-stu-id="6adcc-151">**D3DXMatrixTransformation**</span></span>](d3dxmatrixtransformation.md)
</dt> <dt>

[<span data-ttu-id="6adcc-152">Преобразования (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="6adcc-152">Transforms (Direct3D 9)</span></span>](transforms.md)
</dt> </dl>

 

 
