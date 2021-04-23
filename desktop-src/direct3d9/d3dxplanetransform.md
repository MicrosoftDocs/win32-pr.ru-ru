---
description: Преобразует плоскость на матрицу. Входная матрица является инверсией фактического преобразования.
ms.assetid: 3581b397-cbd8-4aed-80dd-1841f331a367
title: Функция D3DXPlaneTransform (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneTransform
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fd82478d9fb1f08bb0320a8c84357efcdf20be26
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105674674"
---
# <a name="d3dxplanetransform-function-d3dx9mathh"></a><span data-ttu-id="68027-104">Функция D3DXPlaneTransform (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="68027-104">D3DXPlaneTransform function (D3dx9math.h)</span></span>

<span data-ttu-id="68027-105">Преобразует плоскость на матрицу.</span><span class="sxs-lookup"><span data-stu-id="68027-105">Transforms a plane by a matrix.</span></span> <span data-ttu-id="68027-106">Входная матрица является инверсией фактического преобразования.</span><span class="sxs-lookup"><span data-stu-id="68027-106">The input matrix is the inverse transpose of the actual transformation.</span></span>

## <a name="syntax"></a><span data-ttu-id="68027-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="68027-107">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneTransform(
  _Inout_       D3DXPLANE  *pOut,
  _In_    const D3DXPLANE  *pP,
  _In_    const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="68027-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="68027-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68027-109">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="68027-109">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="68027-110">Тип: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="68027-110">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="68027-111">Указатель на структуру [**D3DXPLANE**](d3dxplane.md) , содержащую полученную преобразованную плоскость.</span><span class="sxs-lookup"><span data-stu-id="68027-111">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure that contains the resulting transformed plane.</span></span> <span data-ttu-id="68027-112">Ознакомьтесь с примером ниже.</span><span class="sxs-lookup"><span data-stu-id="68027-112">See example.</span></span>

</dd> <dt>

<span data-ttu-id="68027-113">*PP* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="68027-113">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68027-114">Тип: **const [**D3DXPLANE**](d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="68027-114">Type: **const [**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="68027-115">Указатель на входную структуру [**D3DXPLANE**](d3dxplane.md) , которая содержит плоскость, которая будет преобразована.</span><span class="sxs-lookup"><span data-stu-id="68027-115">Pointer to the input [**D3DXPLANE**](d3dxplane.md) structure, which contains the plane that will be transformed.</span></span> <span data-ttu-id="68027-116">Вектор (a, b, c), описывающий плоскость, должен быть нормализован перед вызовом этой функции.</span><span class="sxs-lookup"><span data-stu-id="68027-116">The vector (a,b,c) that describes the plane must be normalized before this function is called.</span></span> <span data-ttu-id="68027-117">Ознакомьтесь с примером ниже.</span><span class="sxs-lookup"><span data-stu-id="68027-117">See example.</span></span>

</dd> <dt>

<span data-ttu-id="68027-118">*PM* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="68027-118">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68027-119">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="68027-119">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="68027-120">Указатель на исходную структуру [**D3DXMATRIX**](d3dxmatrix.md) , которая содержит значения преобразования.</span><span class="sxs-lookup"><span data-stu-id="68027-120">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure, which contains the transformation values.</span></span> <span data-ttu-id="68027-121">Эта матрица должна содержать обратную перестановку значений преобразования.</span><span class="sxs-lookup"><span data-stu-id="68027-121">This matrix must contain the inverse transpose of the transformation values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68027-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="68027-122">Return value</span></span>

<span data-ttu-id="68027-123">Тип: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="68027-123">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="68027-124">Указатель на структуру [**D3DXPLANE**](d3dxplane.md) , представляющую преобразованную плоскость.</span><span class="sxs-lookup"><span data-stu-id="68027-124">Pointer to a [**D3DXPLANE**](d3dxplane.md) structure, representing the transformed plane.</span></span> <span data-ttu-id="68027-125">Это то же значение, которое возвращается в параметре тоска, чтобы эту функцию можно было использовать в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="68027-125">This is the same value returned in the pOut parameter so that this function can be used as a parameter for another function.</span></span>

## <a name="remarks"></a><span data-ttu-id="68027-126">Remarks</span><span class="sxs-lookup"><span data-stu-id="68027-126">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="68027-127">Примеры</span><span class="sxs-lookup"><span data-stu-id="68027-127">Examples</span></span>

<span data-ttu-id="68027-128">Этот пример преобразует плоскость, применяя неоднородный масштаб.</span><span class="sxs-lookup"><span data-stu-id="68027-128">This example transforms a plane by applying a non-uniform scale.</span></span>


```
D3DXPLANE   planeNew;
D3DXPLANE   plane(0,1,1,0);
D3DXPlaneNormalize(&plane, &plane);

D3DXMATRIX  matrix;
D3DXMatrixScaling(&matrix, 1.0f,2.0f,3.0f); 
D3DXMatrixInverse(&matrix, NULL, &matrix);
D3DXMatrixTranspose(&matrix, &matrix);
D3DXPlaneTransform(&planeNew, &plane, &matrix);
```



<span data-ttu-id="68027-129">Плоскость описывается в AX + by + CZ + DW = 0.</span><span class="sxs-lookup"><span data-stu-id="68027-129">A plane is described by ax + by + cz + dw = 0.</span></span> <span data-ttu-id="68027-130">Первая плоскость создается с (a, b, c, d) = (0, 1, 1, 0), которая является плоскостью, описанной в разделе y + z = 0.</span><span class="sxs-lookup"><span data-stu-id="68027-130">The first plane is created with (a,b,c,d) = (0,1,1,0), which is a plane described by y + z = 0.</span></span> <span data-ttu-id="68027-131">После масштабирования новая плоскость содержит (a, b, c, d) = (0, 0.353 f, 0.235 f, 0), которая показывает новую плоскость, которая будет описываться 0.353 y + 0.235 z = 0.</span><span class="sxs-lookup"><span data-stu-id="68027-131">After scaling, the new plane contains (a,b,c,d) = (0, 0.353f, 0.235f, 0), which shows the new plane to be described by 0.353y + 0.235z = 0.</span></span>

<span data-ttu-id="68027-132">Параметр pM содержит обратную трансформацию матрицы преобразования.</span><span class="sxs-lookup"><span data-stu-id="68027-132">The parameter pM contains the inverse transpose of the transformation matrix.</span></span> <span data-ttu-id="68027-133">Обратная перестановка необходима этому методу, чтобы правильно преобразовать стандартный вектор преобразованной плоскости.</span><span class="sxs-lookup"><span data-stu-id="68027-133">The inverse transpose is required by this method so that the normal vector of the transformed plane can be correctly transformed as well.</span></span>

## <a name="requirements"></a><span data-ttu-id="68027-134">Требования</span><span class="sxs-lookup"><span data-stu-id="68027-134">Requirements</span></span>



| <span data-ttu-id="68027-135">Требование</span><span class="sxs-lookup"><span data-stu-id="68027-135">Requirement</span></span> | <span data-ttu-id="68027-136">Значение</span><span class="sxs-lookup"><span data-stu-id="68027-136">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="68027-137">Header</span><span class="sxs-lookup"><span data-stu-id="68027-137">Header</span></span><br/>  | <dl> <span data-ttu-id="68027-138"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="68027-138"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="68027-139">Библиотека</span><span class="sxs-lookup"><span data-stu-id="68027-139">Library</span></span><br/> | <dl> <span data-ttu-id="68027-140"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="68027-140"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="68027-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="68027-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68027-142">Математические функции</span><span class="sxs-lookup"><span data-stu-id="68027-142">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="68027-143">**D3DXPlaneNormalize**</span><span class="sxs-lookup"><span data-stu-id="68027-143">**D3DXPlaneNormalize**</span></span>](d3dxplanenormalize.md)
</dt> <dt>

[<span data-ttu-id="68027-144">**D3DXMatrixRotationX**</span><span class="sxs-lookup"><span data-stu-id="68027-144">**D3DXMatrixRotationX**</span></span>](d3dxmatrixrotationx.md)
</dt> <dt>

[<span data-ttu-id="68027-145">**D3DXMatrixRotationY**</span><span class="sxs-lookup"><span data-stu-id="68027-145">**D3DXMatrixRotationY**</span></span>](d3dxmatrixrotationy.md)
</dt> <dt>

[<span data-ttu-id="68027-146">**D3DXMatrixRotationZ**</span><span class="sxs-lookup"><span data-stu-id="68027-146">**D3DXMatrixRotationZ**</span></span>](d3dxmatrixrotationz.md)
</dt> <dt>

[<span data-ttu-id="68027-147">**D3DXMatrixInverse**</span><span class="sxs-lookup"><span data-stu-id="68027-147">**D3DXMatrixInverse**</span></span>](d3dxmatrixinverse.md)
</dt> <dt>

[<span data-ttu-id="68027-148">**D3DXMatrixTranspose**</span><span class="sxs-lookup"><span data-stu-id="68027-148">**D3DXMatrixTranspose**</span></span>](d3dxmatrixtranspose.md)
</dt> </dl>

 

 




