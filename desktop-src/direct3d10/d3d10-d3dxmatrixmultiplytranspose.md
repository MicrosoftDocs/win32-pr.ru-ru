---
description: Вычисляет транспроизведенное произведение двух матриц.
ms.assetid: 3db4138c-407c-47b5-b8b9-04af8771e98e
title: Функция D3DXMatrixMultiplyTranspose (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixMultiplyTranspose
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 187912a4117ab502ea7b0b1b3fc1ea105ecbc3e7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105720969"
---
# <a name="d3dxmatrixmultiplytranspose-function-d3dx10mathh"></a><span data-ttu-id="d2bdc-103">Функция D3DXMatrixMultiplyTranspose (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="d2bdc-103">D3DXMatrixMultiplyTranspose function (D3DX10Math.h)</span></span>

<span data-ttu-id="d2bdc-104">Вычисляет транспроизведенное произведение двух матриц.</span><span class="sxs-lookup"><span data-stu-id="d2bdc-104">Calculates the transposed product of two matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2bdc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d2bdc-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixMultiplyTranspose(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXMATRIX *pM1,
  _In_    const D3DXMATRIX *pM2
);
```



## <a name="parameters"></a><span data-ttu-id="d2bdc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d2bdc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2bdc-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="d2bdc-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d2bdc-108">Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="d2bdc-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d2bdc-109">Указатель на структуру [**D3DXMATRIX**](d3d10-d3dxmatrix.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="d2bdc-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="d2bdc-110">*pM1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d2bdc-110">*pM1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2bdc-111">Тип: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="d2bdc-111">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d2bdc-112">Указатель на исходную структуру D3DXMATRIX (с левой стороны).</span><span class="sxs-lookup"><span data-stu-id="d2bdc-112">Pointer to a source D3DXMATRIX structure (left hand side).</span></span>

</dd> <dt>

<span data-ttu-id="d2bdc-113">*pM2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d2bdc-113">*pM2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2bdc-114">Тип: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="d2bdc-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d2bdc-115">Указатель на исходную структуру D3DXMATRIX (правую часть).</span><span class="sxs-lookup"><span data-stu-id="d2bdc-115">Pointer to a source D3DXMATRIX structure (right hand side).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2bdc-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d2bdc-116">Return value</span></span>

<span data-ttu-id="d2bdc-117">Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="d2bdc-117">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d2bdc-118">Указатель на структуру D3DXMATRIX, которая является произведением двух матриц.</span><span class="sxs-lookup"><span data-stu-id="d2bdc-118">Pointer to a D3DXMATRIX structure that is the product of two matrices.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2bdc-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d2bdc-119">Remarks</span></span>

<span data-ttu-id="d2bdc-120">Результатом является преобразование произведения двух матриц преобразования, out = T (M1 \* m2).</span><span class="sxs-lookup"><span data-stu-id="d2bdc-120">The result is the transposed of the product of two transformation matrices, Out = T(M1\*M2).</span></span>

<span data-ttu-id="d2bdc-121">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="d2bdc-121">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="d2bdc-122">Таким образом, функция D3DXMatrixMultiplyTranspose может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="d2bdc-122">In this way, the D3DXMatrixMultiplyTranspose function can be used as a parameter for another function.</span></span>

<span data-ttu-id="d2bdc-123">Эта функция полезна для установки матриц в качестве констант для шейдеров вершин и пикселей.</span><span class="sxs-lookup"><span data-stu-id="d2bdc-123">This function is useful to set matrices as constants for vertex and pixel shaders.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2bdc-124">Требования</span><span class="sxs-lookup"><span data-stu-id="d2bdc-124">Requirements</span></span>



| <span data-ttu-id="d2bdc-125">Требование</span><span class="sxs-lookup"><span data-stu-id="d2bdc-125">Requirement</span></span> | <span data-ttu-id="d2bdc-126">Значение</span><span class="sxs-lookup"><span data-stu-id="d2bdc-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d2bdc-127">Header</span><span class="sxs-lookup"><span data-stu-id="d2bdc-127">Header</span></span><br/>  | <dl> <span data-ttu-id="d2bdc-128"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2bdc-128"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="d2bdc-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d2bdc-129">Library</span></span><br/> | <dl> <span data-ttu-id="d2bdc-130"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d2bdc-130"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d2bdc-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d2bdc-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2bdc-132">Математические функции</span><span class="sxs-lookup"><span data-stu-id="d2bdc-132">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
