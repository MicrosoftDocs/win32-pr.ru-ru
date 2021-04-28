---
description: Функция D3DXMatrixMultiplyTranspose (D3dx9math. h) — вычисляет транспроизведенное произведение двух матриц.
ms.assetid: 43927500-9413-41a4-a6ee-974d85dd1054
title: Функция D3DXMatrixMultiplyTranspose (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 87aaa45e7a7a16884d17ab340f0bf1efeccd93bb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107542"
---
# <a name="d3dxmatrixmultiplytranspose-function-d3dx9mathh"></a><span data-ttu-id="606da-103">Функция D3DXMatrixMultiplyTranspose (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="606da-103">D3DXMatrixMultiplyTranspose function (D3dx9math.h)</span></span>

<span data-ttu-id="606da-104">Вычисляет транспроизведенное произведение двух матриц.</span><span class="sxs-lookup"><span data-stu-id="606da-104">Calculates the transposed product of two matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="606da-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="606da-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixMultiplyTranspose(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXMATRIX *pM1,
  _In_    const D3DXMATRIX *pM2
);
```



## <a name="parameters"></a><span data-ttu-id="606da-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="606da-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="606da-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="606da-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="606da-108">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="606da-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="606da-109">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="606da-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="606da-110">*pM1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="606da-110">*pM1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="606da-111">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="606da-111">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="606da-112">Указатель на исходную структуру [**D3DXMATRIX**](d3dxmatrix.md) .</span><span class="sxs-lookup"><span data-stu-id="606da-112">Pointer to a source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="606da-113">*pM2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="606da-113">*pM2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="606da-114">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="606da-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="606da-115">Указатель на исходную структуру [**D3DXMATRIX**](d3dxmatrix.md) .</span><span class="sxs-lookup"><span data-stu-id="606da-115">Pointer to a source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="606da-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="606da-116">Return value</span></span>

<span data-ttu-id="606da-117">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="606da-117">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="606da-118">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , которая является произведением двух матриц.</span><span class="sxs-lookup"><span data-stu-id="606da-118">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is the product of two matrices.</span></span>

## <a name="remarks"></a><span data-ttu-id="606da-119">Remarks</span><span class="sxs-lookup"><span data-stu-id="606da-119">Remarks</span></span>

<span data-ttu-id="606da-120">Результатом является преобразование произведения двух матриц преобразования, out = T (M1 \* m2).</span><span class="sxs-lookup"><span data-stu-id="606da-120">The result is the transposed of the product of two transformation matrices, Out = T(M1\*M2).</span></span>

<span data-ttu-id="606da-121">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="606da-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="606da-122">Таким образом, функция **D3DXMatrixMultiplyTranspose** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="606da-122">In this way, the **D3DXMatrixMultiplyTranspose** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="606da-123">Эта функция полезна для установки матриц в качестве констант для шейдеров вершин и пикселей.</span><span class="sxs-lookup"><span data-stu-id="606da-123">This function is useful to set matrices as constants for vertex and pixel shaders.</span></span>

## <a name="requirements"></a><span data-ttu-id="606da-124">Требования</span><span class="sxs-lookup"><span data-stu-id="606da-124">Requirements</span></span>



| <span data-ttu-id="606da-125">Требование</span><span class="sxs-lookup"><span data-stu-id="606da-125">Requirement</span></span> | <span data-ttu-id="606da-126">Значение</span><span class="sxs-lookup"><span data-stu-id="606da-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="606da-127">Header</span><span class="sxs-lookup"><span data-stu-id="606da-127">Header</span></span><br/>  | <dl> <span data-ttu-id="606da-128"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="606da-128"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="606da-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="606da-129">Library</span></span><br/> | <dl> <span data-ttu-id="606da-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="606da-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="606da-131">См. также</span><span class="sxs-lookup"><span data-stu-id="606da-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="606da-132">Математические функции</span><span class="sxs-lookup"><span data-stu-id="606da-132">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="606da-133">**D3DXMatrixMultiply**</span><span class="sxs-lookup"><span data-stu-id="606da-133">**D3DXMatrixMultiply**</span></span>](d3dxmatrixmultiply.md)
</dt> <dt>

[<span data-ttu-id="606da-134">**D3DXQuaternionMultiply**</span><span class="sxs-lookup"><span data-stu-id="606da-134">**D3DXQuaternionMultiply**</span></span>](d3dxquaternionmultiply.md)
</dt> </dl>

 

 




