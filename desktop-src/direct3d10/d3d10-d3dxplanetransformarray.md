---
description: Функция D3DXPlaneTransformArray (D3DX10Math. h) — преобразует массив плоскостей по матрице. Векторы, описывающие каждую плоскость, должны быть нормализованы.
ms.assetid: 9529b06a-0575-4115-8d35-fc35a7bfb0bd
title: Функция D3DXPlaneTransformArray (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneTransformArray
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d8b02b64fd13e7466980340056fceccc1da784cf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103262"
---
# <a name="d3dxplanetransformarray-function-d3dx10mathh"></a><span data-ttu-id="77465-104">Функция D3DXPlaneTransformArray (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="77465-104">D3DXPlaneTransformArray function (D3DX10Math.h)</span></span>

<span data-ttu-id="77465-105">Преобразует массив плоскостей по матрице.</span><span class="sxs-lookup"><span data-stu-id="77465-105">Transforms an array of planes by a matrix.</span></span> <span data-ttu-id="77465-106">Векторы, описывающие каждую плоскость, должны быть нормализованы.</span><span class="sxs-lookup"><span data-stu-id="77465-106">The vectors that describe each plane must be normalized.</span></span>

## <a name="syntax"></a><span data-ttu-id="77465-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="77465-107">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneTransformArray(
  _Inout_       D3DXPLANE  *pOut,
  _In_          UINT       OutStride,
  _In_    const D3DXPLANE  *pP,
  _In_          UINT       PStride,
  _In_    const D3DXMATRIX *pM,
  _In_          UINT       n
);
```



## <a name="parameters"></a><span data-ttu-id="77465-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="77465-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77465-109">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="77465-109">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="77465-110">Тип: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="77465-110">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="77465-111">Указатель на структуру [**D3DXPLANE**](d3d10-d3dxplane.md) , содержащую полученную преобразованную плоскость.</span><span class="sxs-lookup"><span data-stu-id="77465-111">Pointer to the [**D3DXPLANE**](d3d10-d3dxplane.md) structure that contains the resulting transformed plane.</span></span> <span data-ttu-id="77465-112">См. пример.</span><span class="sxs-lookup"><span data-stu-id="77465-112">See Example.</span></span>

</dd> <dt>

<span data-ttu-id="77465-113">*Шаг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="77465-113">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77465-114">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="77465-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="77465-115">Шаг каждой преобразованной плоскости.</span><span class="sxs-lookup"><span data-stu-id="77465-115">The stride of each transformed plane.</span></span>

</dd> <dt>

<span data-ttu-id="77465-116">*PP* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="77465-116">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77465-117">Тип: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="77465-117">Type: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="77465-118">Указатель на входную структуру D3DXPLANE, содержащую массив плоскостей для преобразования.</span><span class="sxs-lookup"><span data-stu-id="77465-118">Pointer to the input D3DXPLANE structure, which contains the array of planes to transform.</span></span> <span data-ttu-id="77465-119">Вектор (a, b, c), описывающий плоскость, должен быть нормализован перед вызовом этой функции.</span><span class="sxs-lookup"><span data-stu-id="77465-119">The vector (a, b, c) that describes the plane must be normalized before this function is called.</span></span> <span data-ttu-id="77465-120">См. пример.</span><span class="sxs-lookup"><span data-stu-id="77465-120">See Example.</span></span>

</dd> <dt>

<span data-ttu-id="77465-121">*Пстриде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="77465-121">*PStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77465-122">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="77465-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="77465-123">Шаг для каждой непреобразованной плоскости.</span><span class="sxs-lookup"><span data-stu-id="77465-123">The stride of each non-transformed plane.</span></span>

</dd> <dt>

<span data-ttu-id="77465-124">*PM* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="77465-124">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77465-125">Тип: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="77465-125">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="77465-126">Указатель на исходную структуру [**D3DXMATRIX**](d3d10-d3dxmatrix.md) , которая содержит обратное преобразование значений преобразования.</span><span class="sxs-lookup"><span data-stu-id="77465-126">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure, which contains the inverse transpose of the transformation values.</span></span>

</dd> <dt>

<span data-ttu-id="77465-127">*n* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="77465-127">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77465-128">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="77465-128">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="77465-129">Число преобразуемых плоскостей.</span><span class="sxs-lookup"><span data-stu-id="77465-129">The number of planes to transform.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77465-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="77465-130">Return value</span></span>

<span data-ttu-id="77465-131">Тип: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="77465-131">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="77465-132">Указатель на структуру D3DXPLANE, представляющую преобразованную плоскость.</span><span class="sxs-lookup"><span data-stu-id="77465-132">Pointer to a D3DXPLANE structure, representing the transformed plane.</span></span> <span data-ttu-id="77465-133">Это то же значение, которое возвращается в параметре тоска, чтобы эту функцию можно было использовать в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="77465-133">This is the same value returned in the pOut parameter so that this function can be used as a parameter for another function.</span></span>

## <a name="remarks"></a><span data-ttu-id="77465-134">Remarks</span><span class="sxs-lookup"><span data-stu-id="77465-134">Remarks</span></span>

<span data-ttu-id="77465-135">Этот пример преобразует одну плоскость, применяя неоднородный масштаб.</span><span class="sxs-lookup"><span data-stu-id="77465-135">This example transforms one plane by applying a non-uniform scale.</span></span>


```
#define ARRAYSIZE 4
D3DXPLANE planeNew[ARRAYSIZE];
D3DXPLANE plane[ARRAYSIZE];

for(int i = 0; i < ARRAYSIZE; i++)
{
    plane = D3DXPLANE( 0.0f, 1.0f, 1.0f, 0.0f );
    D3DXPlaneNormalize( &plane[i], &plane[i] );
}

D3DXMATRIX  matrix;
D3DXMatrixScaling( &matrix, 1.0f, 2.0f, 3.0f ); 
D3DXMatrixInverse( &matrix, NULL, &matrix );
D3DXMatrixTranspose( &matrix, &matrix );
D3DXPlaneTransformArray( &planeNew, sizeof (D3DXPLANE), &plane, 
                         sizeof (D3DXPLANE), &matrix, ARRAYSIZE );
```



<span data-ttu-id="77465-136">Плоскость описывается в AX + by + CZ + DW = 0.</span><span class="sxs-lookup"><span data-stu-id="77465-136">A plane is described by ax + by + cz + dw = 0.</span></span> <span data-ttu-id="77465-137">Первая плоскость создается с (a, b, c, d) = (0, 1, 1, 0), которая является плоскостью, описанной в разделе y + z = 0.</span><span class="sxs-lookup"><span data-stu-id="77465-137">The first plane is created with (a,b,c,d) = (0,1,1,0), which is a plane described by y + z = 0.</span></span> <span data-ttu-id="77465-138">После масштабирования новая плоскость содержит (a, b, c, d) = (0, 0.353 f, 0.235 f, 0), которая показывает новую плоскость, которая будет описываться 0.353 y + 0.235 z = 0.</span><span class="sxs-lookup"><span data-stu-id="77465-138">After scaling, the new plane contains (a,b,c,d) = (0, 0.353f, 0.235f, 0), which shows the new plane to be described by 0.353y + 0.235z = 0.</span></span>

<span data-ttu-id="77465-139">Параметр pM содержит обратную перестановку матрицы преобразования.</span><span class="sxs-lookup"><span data-stu-id="77465-139">The parameter pM, contains the inverse transpose of the transformation matrix.</span></span> <span data-ttu-id="77465-140">Обратная перестановка необходима этому методу, чтобы правильно преобразовать стандартный вектор преобразованной плоскости.</span><span class="sxs-lookup"><span data-stu-id="77465-140">The inverse transpose is required by this method so that the normal vector of the transformed plane can be correctly transformed as well.</span></span>

## <a name="requirements"></a><span data-ttu-id="77465-141">Требования</span><span class="sxs-lookup"><span data-stu-id="77465-141">Requirements</span></span>



| <span data-ttu-id="77465-142">Требование</span><span class="sxs-lookup"><span data-stu-id="77465-142">Requirement</span></span> | <span data-ttu-id="77465-143">Значение</span><span class="sxs-lookup"><span data-stu-id="77465-143">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="77465-144">Header</span><span class="sxs-lookup"><span data-stu-id="77465-144">Header</span></span><br/>  | <dl> <span data-ttu-id="77465-145"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="77465-145"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="77465-146">Библиотека</span><span class="sxs-lookup"><span data-stu-id="77465-146">Library</span></span><br/> | <dl> <span data-ttu-id="77465-147"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="77465-147"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="77465-148">См. также</span><span class="sxs-lookup"><span data-stu-id="77465-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77465-149">Математические функции</span><span class="sxs-lookup"><span data-stu-id="77465-149">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
