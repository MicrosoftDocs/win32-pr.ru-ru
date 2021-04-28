---
description: Функция D3DXMatrixInverse (D3DX10Math. h) — Вычисляет обратную матрицу.
ms.assetid: 928a201b-814d-41cc-bfab-d2f8a12addeb
title: Функция D3DXMatrixInverse (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 6b42cf0ae3f9ee1154d385600b00a2dcb10c4fd9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113202"
---
# <a name="d3dxmatrixinverse-function-d3dx10mathh"></a><span data-ttu-id="20341-103">Функция D3DXMatrixInverse (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="20341-103">D3DXMatrixInverse function (D3DX10Math.h)</span></span>

<span data-ttu-id="20341-104">Вычисляет обратную матрицу.</span><span class="sxs-lookup"><span data-stu-id="20341-104">Calculates the inverse of a matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="20341-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="20341-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixInverse(
  _Inout_       D3DXMATRIX *pOut,
  _Inout_       FLOAT      *pDeterminant,
  _In_    const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="20341-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="20341-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20341-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="20341-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="20341-108">Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="20341-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="20341-109">Указатель на структуру [**D3DXMATRIX**](d3d10-d3dxmatrix.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="20341-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="20341-110">*пдетерминант* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="20341-110">*pDeterminant* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="20341-111">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="20341-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="20341-112">Указатель на значение FLOAT, содержащее определитель матрицы.</span><span class="sxs-lookup"><span data-stu-id="20341-112">Pointer to a FLOAT value containing the determinant of the matrix.</span></span> <span data-ttu-id="20341-113">Если определитель не требуется, присвойте этому параметру **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="20341-113">If the determinant is not needed, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="20341-114">*PM* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="20341-114">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20341-115">Тип: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="20341-115">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="20341-116">Указатель на исходную структуру D3DXMATRIX.</span><span class="sxs-lookup"><span data-stu-id="20341-116">Pointer to the source D3DXMATRIX structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20341-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="20341-117">Return value</span></span>

<span data-ttu-id="20341-118">Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="20341-118">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="20341-119">Указатель на структуру D3DXMATRIX, которая является инверсией матрицы.</span><span class="sxs-lookup"><span data-stu-id="20341-119">Pointer to a D3DXMATRIX structure that is the inverse of the matrix.</span></span> <span data-ttu-id="20341-120">Если инверсия матрицы завершается ошибкой, возвращается **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="20341-120">If matrix inversion fails, **NULL** is returned.</span></span>

<span data-ttu-id="20341-121">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="20341-121">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="20341-122">Таким образом, функция D3DXMatrixInverse может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="20341-122">In this way, the D3DXMatrixInverse function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="20341-123">Требования</span><span class="sxs-lookup"><span data-stu-id="20341-123">Requirements</span></span>



| <span data-ttu-id="20341-124">Требование</span><span class="sxs-lookup"><span data-stu-id="20341-124">Requirement</span></span> | <span data-ttu-id="20341-125">Значение</span><span class="sxs-lookup"><span data-stu-id="20341-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="20341-126">Header</span><span class="sxs-lookup"><span data-stu-id="20341-126">Header</span></span><br/>  | <dl> <span data-ttu-id="20341-127"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="20341-127"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="20341-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="20341-128">Library</span></span><br/> | <dl> <span data-ttu-id="20341-129"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="20341-129"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="20341-130">См. также</span><span class="sxs-lookup"><span data-stu-id="20341-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20341-131">Математические функции</span><span class="sxs-lookup"><span data-stu-id="20341-131">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
