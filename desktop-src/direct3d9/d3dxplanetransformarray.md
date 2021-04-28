---
description: Функция D3DXPlaneTransformArray (D3dx9math. h) — преобразует массив плоскостей по матрице. Векторы, описывающие каждую плоскость, должны быть нормализованы.
ms.assetid: e82e830b-efbb-4bdc-b370-7bfa4326a669
title: Функция D3DXPlaneTransformArray (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bdbc845eda69d22f6e7097131f71b074a9b53985
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094132"
---
# <a name="d3dxplanetransformarray-function-d3dx9mathh"></a><span data-ttu-id="2479b-104">Функция D3DXPlaneTransformArray (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="2479b-104">D3DXPlaneTransformArray function (D3dx9math.h)</span></span>

<span data-ttu-id="2479b-105">Преобразует массив плоскостей по матрице.</span><span class="sxs-lookup"><span data-stu-id="2479b-105">Transforms an array of planes by a matrix.</span></span> <span data-ttu-id="2479b-106">Векторы, описывающие каждую плоскость, должны быть нормализованы.</span><span class="sxs-lookup"><span data-stu-id="2479b-106">The vectors that describe each plane must be normalized.</span></span>

## <a name="syntax"></a><span data-ttu-id="2479b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2479b-107">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneTransformArray(
  _Inout_       D3DXPLANE  *pOut,
  _Out_         UINT       OutStride,
  _In_    const D3DXPLANE  *pP,
  _In_          UINT       PStride,
  _In_    const D3DXMATRIX *pM,
  _In_          UINT       n
);
```



## <a name="parameters"></a><span data-ttu-id="2479b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="2479b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2479b-109">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="2479b-109">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2479b-110">Тип: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="2479b-110">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="2479b-111">Указатель на структуру [**D3DXPLANE**](d3dxplane.md) , содержащую полученную преобразованную плоскость.</span><span class="sxs-lookup"><span data-stu-id="2479b-111">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure that contains the resulting transformed plane.</span></span> <span data-ttu-id="2479b-112">См. пример.</span><span class="sxs-lookup"><span data-stu-id="2479b-112">See Example.</span></span>

</dd> <dt>

<span data-ttu-id="2479b-113">*Шаг* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2479b-113">*OutStride* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2479b-114">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2479b-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2479b-115">Шаг каждой преобразованной плоскости.</span><span class="sxs-lookup"><span data-stu-id="2479b-115">The stride of each transformed plane.</span></span>

</dd> <dt>

<span data-ttu-id="2479b-116">*PP* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2479b-116">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2479b-117">Тип: **const [**D3DXPLANE**](d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="2479b-117">Type: **const [**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="2479b-118">Указатель на входную структуру [**D3DXPLANE**](d3dxplane.md) , содержащую массив плоскостей для преобразования.</span><span class="sxs-lookup"><span data-stu-id="2479b-118">Pointer to the input [**D3DXPLANE**](d3dxplane.md) structure, which contains the array of planes to transform.</span></span> <span data-ttu-id="2479b-119">Вектор (a, b, c), описывающий плоскость, должен быть нормализован перед вызовом этой функции.</span><span class="sxs-lookup"><span data-stu-id="2479b-119">The vector (a,b,c) that describes the plane must be normalized before this function is called.</span></span> <span data-ttu-id="2479b-120">См. пример.</span><span class="sxs-lookup"><span data-stu-id="2479b-120">See Example.</span></span>

</dd> <dt>

<span data-ttu-id="2479b-121">*Пстриде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2479b-121">*PStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2479b-122">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2479b-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2479b-123">Шаг для каждой непреобразованной плоскости.</span><span class="sxs-lookup"><span data-stu-id="2479b-123">The stride of each non-transformed plane.</span></span>

</dd> <dt>

<span data-ttu-id="2479b-124">*PM* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2479b-124">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2479b-125">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="2479b-125">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="2479b-126">Указатель на исходную структуру [**D3DXMATRIX**](d3dxmatrix.md) , которая содержит обратное преобразование значений преобразования.</span><span class="sxs-lookup"><span data-stu-id="2479b-126">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure, which contains the inverse transpose of the transformation values.</span></span>

</dd> <dt>

<span data-ttu-id="2479b-127">*n* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="2479b-127">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2479b-128">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2479b-128">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2479b-129">Число преобразуемых плоскостей.</span><span class="sxs-lookup"><span data-stu-id="2479b-129">The number of planes to transform.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2479b-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2479b-130">Return value</span></span>

<span data-ttu-id="2479b-131">Тип: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="2479b-131">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="2479b-132">Указатель на структуру [**D3DXPLANE**](d3dxplane.md) , представляющую преобразованную плоскость.</span><span class="sxs-lookup"><span data-stu-id="2479b-132">Pointer to a [**D3DXPLANE**](d3dxplane.md) structure, representing the transformed plane.</span></span> <span data-ttu-id="2479b-133">Это то же значение, которое возвращается в параметре *тоска* , чтобы эту функцию можно было использовать в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="2479b-133">This is the same value returned in the *pOut* parameter so that this function can be used as a parameter for another function.</span></span>

## <a name="remarks"></a><span data-ttu-id="2479b-134">Remarks</span><span class="sxs-lookup"><span data-stu-id="2479b-134">Remarks</span></span>

<span data-ttu-id="2479b-135">Этот пример преобразует одну плоскость, применяя неоднородный масштаб.</span><span class="sxs-lookup"><span data-stu-id="2479b-135">This example transforms one plane by applying a non-uniform scale.</span></span>


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



<span data-ttu-id="2479b-136">Плоскость описывается в AX + by + CZ + DW = 0.</span><span class="sxs-lookup"><span data-stu-id="2479b-136">A plane is described by ax + by + cz + dw = 0.</span></span> <span data-ttu-id="2479b-137">Первая плоскость создается с (a, b, c, d) = (0, 1, 1, 0), которая является плоскостью, описанной в разделе y + z = 0.</span><span class="sxs-lookup"><span data-stu-id="2479b-137">The first plane is created with (a,b,c,d) = (0,1,1,0), which is a plane described by y + z = 0.</span></span> <span data-ttu-id="2479b-138">После масштабирования новая плоскость содержит (a, b, c, d) = (0, 0.353 f, 0.235 f, 0), которая показывает новую плоскость, которая будет описываться 0.353 y + 0.235 z = 0.</span><span class="sxs-lookup"><span data-stu-id="2479b-138">After scaling, the new plane contains (a,b,c,d) = (0, 0.353f, 0.235f, 0), which shows the new plane to be described by 0.353y + 0.235z = 0.</span></span>

<span data-ttu-id="2479b-139">Параметр *PM* содержит обратную трансформацию матрицы преобразования.</span><span class="sxs-lookup"><span data-stu-id="2479b-139">The parameter *pM* contains the inverse transpose of the transformation matrix.</span></span> <span data-ttu-id="2479b-140">Обратная перестановка необходима этому методу, чтобы правильно преобразовать стандартный вектор преобразованной плоскости.</span><span class="sxs-lookup"><span data-stu-id="2479b-140">The inverse transpose is required by this method so that the normal vector of the transformed plane can be correctly transformed as well.</span></span>

## <a name="requirements"></a><span data-ttu-id="2479b-141">Требования</span><span class="sxs-lookup"><span data-stu-id="2479b-141">Requirements</span></span>



| <span data-ttu-id="2479b-142">Требование</span><span class="sxs-lookup"><span data-stu-id="2479b-142">Requirement</span></span> | <span data-ttu-id="2479b-143">Значение</span><span class="sxs-lookup"><span data-stu-id="2479b-143">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2479b-144">Header</span><span class="sxs-lookup"><span data-stu-id="2479b-144">Header</span></span><br/>  | <dl> <span data-ttu-id="2479b-145"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="2479b-145"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="2479b-146">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2479b-146">Library</span></span><br/> | <dl> <span data-ttu-id="2479b-147"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2479b-147"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2479b-148">См. также</span><span class="sxs-lookup"><span data-stu-id="2479b-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2479b-149">Математические функции</span><span class="sxs-lookup"><span data-stu-id="2479b-149">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="2479b-150">**D3DXPlaneNormalize**</span><span class="sxs-lookup"><span data-stu-id="2479b-150">**D3DXPlaneNormalize**</span></span>](d3dxplanenormalize.md)
</dt> <dt>

[<span data-ttu-id="2479b-151">**D3DXMatrixRotationX**</span><span class="sxs-lookup"><span data-stu-id="2479b-151">**D3DXMatrixRotationX**</span></span>](d3dxmatrixrotationx.md)
</dt> <dt>

[<span data-ttu-id="2479b-152">**D3DXMatrixRotationY**</span><span class="sxs-lookup"><span data-stu-id="2479b-152">**D3DXMatrixRotationY**</span></span>](d3dxmatrixrotationy.md)
</dt> <dt>

[<span data-ttu-id="2479b-153">**D3DXMatrixRotationZ**</span><span class="sxs-lookup"><span data-stu-id="2479b-153">**D3DXMatrixRotationZ**</span></span>](d3dxmatrixrotationz.md)
</dt> <dt>

[<span data-ttu-id="2479b-154">**D3DXMatrixInverse**</span><span class="sxs-lookup"><span data-stu-id="2479b-154">**D3DXMatrixInverse**</span></span>](d3dxmatrixinverse.md)
</dt> <dt>

[<span data-ttu-id="2479b-155">**D3DXMatrixTranspose**</span><span class="sxs-lookup"><span data-stu-id="2479b-155">**D3DXMatrixTranspose**</span></span>](d3dxmatrixtranspose.md)
</dt> </dl>

 

 
