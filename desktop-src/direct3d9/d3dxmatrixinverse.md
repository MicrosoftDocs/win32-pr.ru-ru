---
description: Функция D3DXMatrixInverse (D3dx9math. h) — Вычисляет обратную матрицу.
ms.assetid: b8cad5c5-caa5-4426-b045-1770f8806b6b
title: Функция D3DXMatrixInverse (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixInverse
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0109481beaea282a785564c081e498fe4c7571b6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098152"
---
# <a name="d3dxmatrixinverse-function-d3dx9mathh"></a><span data-ttu-id="0547a-103">Функция D3DXMatrixInverse (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="0547a-103">D3DXMatrixInverse function (D3dx9math.h)</span></span>

<span data-ttu-id="0547a-104">Вычисляет обратную матрицу.</span><span class="sxs-lookup"><span data-stu-id="0547a-104">Calculates the inverse of a matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="0547a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0547a-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixInverse(
  _Inout_       D3DXMATRIX *pOut,
  _Inout_       FLOAT      *pDeterminant,
  _In_    const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="0547a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0547a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0547a-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="0547a-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0547a-108">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="0547a-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="0547a-109">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="0547a-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="0547a-110">*пдетерминант* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="0547a-110">*pDeterminant* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0547a-111">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="0547a-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0547a-112">Указатель на значение FLOAT, содержащее определитель матрицы.</span><span class="sxs-lookup"><span data-stu-id="0547a-112">Pointer to a FLOAT value containing the determinant of the matrix.</span></span> <span data-ttu-id="0547a-113">Если определитель не требуется, присвойте этому параметру **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="0547a-113">If the determinant is not needed, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="0547a-114">*PM* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0547a-114">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0547a-115">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="0547a-115">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="0547a-116">Указатель на исходную структуру [**D3DXMATRIX**](d3dxmatrix.md) .</span><span class="sxs-lookup"><span data-stu-id="0547a-116">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0547a-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0547a-117">Return value</span></span>

<span data-ttu-id="0547a-118">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="0547a-118">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="0547a-119">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , которая является инверсией матрицы.</span><span class="sxs-lookup"><span data-stu-id="0547a-119">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is the inverse of the matrix.</span></span> <span data-ttu-id="0547a-120">Если инверсия матрицы завершается ошибкой, возвращается **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="0547a-120">If matrix inversion fails, **NULL** is returned.</span></span>

<span data-ttu-id="0547a-121">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="0547a-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="0547a-122">Таким образом, функция **D3DXMatrixInverse** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="0547a-122">In this way, the **D3DXMatrixInverse** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="0547a-123">Требования</span><span class="sxs-lookup"><span data-stu-id="0547a-123">Requirements</span></span>



| <span data-ttu-id="0547a-124">Требование</span><span class="sxs-lookup"><span data-stu-id="0547a-124">Requirement</span></span> | <span data-ttu-id="0547a-125">Значение</span><span class="sxs-lookup"><span data-stu-id="0547a-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0547a-126">Header</span><span class="sxs-lookup"><span data-stu-id="0547a-126">Header</span></span><br/>  | <dl> <span data-ttu-id="0547a-127"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="0547a-127"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="0547a-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0547a-128">Library</span></span><br/> | <dl> <span data-ttu-id="0547a-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0547a-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0547a-130">См. также</span><span class="sxs-lookup"><span data-stu-id="0547a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0547a-131">Математические функции</span><span class="sxs-lookup"><span data-stu-id="0547a-131">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
