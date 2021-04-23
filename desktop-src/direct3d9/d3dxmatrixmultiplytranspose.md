---
description: Вычисляет транспроизведенное произведение двух матриц.
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
ms.openlocfilehash: b599453ae108a5a8bab8ee896858760c85799948
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703642"
---
# <a name="d3dxmatrixmultiplytranspose-function-d3dx9mathh"></a><span data-ttu-id="91509-103">Функция D3DXMatrixMultiplyTranspose (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="91509-103">D3DXMatrixMultiplyTranspose function (D3dx9math.h)</span></span>

<span data-ttu-id="91509-104">Вычисляет транспроизведенное произведение двух матриц.</span><span class="sxs-lookup"><span data-stu-id="91509-104">Calculates the transposed product of two matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="91509-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="91509-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixMultiplyTranspose(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXMATRIX *pM1,
  _In_    const D3DXMATRIX *pM2
);
```



## <a name="parameters"></a><span data-ttu-id="91509-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="91509-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91509-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="91509-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="91509-108">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="91509-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="91509-109">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="91509-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="91509-110">*pM1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="91509-110">*pM1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91509-111">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="91509-111">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="91509-112">Указатель на исходную структуру [**D3DXMATRIX**](d3dxmatrix.md) .</span><span class="sxs-lookup"><span data-stu-id="91509-112">Pointer to a source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="91509-113">*pM2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="91509-113">*pM2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91509-114">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="91509-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="91509-115">Указатель на исходную структуру [**D3DXMATRIX**](d3dxmatrix.md) .</span><span class="sxs-lookup"><span data-stu-id="91509-115">Pointer to a source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91509-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="91509-116">Return value</span></span>

<span data-ttu-id="91509-117">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="91509-117">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="91509-118">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , которая является произведением двух матриц.</span><span class="sxs-lookup"><span data-stu-id="91509-118">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is the product of two matrices.</span></span>

## <a name="remarks"></a><span data-ttu-id="91509-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="91509-119">Remarks</span></span>

<span data-ttu-id="91509-120">Результатом является преобразование произведения двух матриц преобразования, out = T (M1 \* m2).</span><span class="sxs-lookup"><span data-stu-id="91509-120">The result is the transposed of the product of two transformation matrices, Out = T(M1\*M2).</span></span>

<span data-ttu-id="91509-121">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="91509-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="91509-122">Таким образом, функция **D3DXMatrixMultiplyTranspose** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="91509-122">In this way, the **D3DXMatrixMultiplyTranspose** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="91509-123">Эта функция полезна для установки матриц в качестве констант для шейдеров вершин и пикселей.</span><span class="sxs-lookup"><span data-stu-id="91509-123">This function is useful to set matrices as constants for vertex and pixel shaders.</span></span>

## <a name="requirements"></a><span data-ttu-id="91509-124">Требования</span><span class="sxs-lookup"><span data-stu-id="91509-124">Requirements</span></span>



| <span data-ttu-id="91509-125">Требование</span><span class="sxs-lookup"><span data-stu-id="91509-125">Requirement</span></span> | <span data-ttu-id="91509-126">Значение</span><span class="sxs-lookup"><span data-stu-id="91509-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="91509-127">Header</span><span class="sxs-lookup"><span data-stu-id="91509-127">Header</span></span><br/>  | <dl> <span data-ttu-id="91509-128"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="91509-128"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="91509-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="91509-129">Library</span></span><br/> | <dl> <span data-ttu-id="91509-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="91509-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="91509-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="91509-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91509-132">Математические функции</span><span class="sxs-lookup"><span data-stu-id="91509-132">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="91509-133">**D3DXMatrixMultiply**</span><span class="sxs-lookup"><span data-stu-id="91509-133">**D3DXMatrixMultiply**</span></span>](d3dxmatrixmultiply.md)
</dt> <dt>

[<span data-ttu-id="91509-134">**D3DXQuaternionMultiply**</span><span class="sxs-lookup"><span data-stu-id="91509-134">**D3DXQuaternionMultiply**</span></span>](d3dxquaternionmultiply.md)
</dt> </dl>

 

 




