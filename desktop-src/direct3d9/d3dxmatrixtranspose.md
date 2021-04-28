---
description: Функция D3DXMatrixTranspose (D3dx9math. h) — Возвращает матрицу матрицы.
ms.assetid: 0ba9682f-3dd6-48b2-82b1-6e34e8ce5452
title: Функция D3DXMatrixTranspose (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixTranspose
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9cb050061b10de963258bcd7527d3c86260d5abc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098112"
---
# <a name="d3dxmatrixtranspose-function-d3dx9mathh"></a><span data-ttu-id="0042a-103">Функция D3DXMatrixTranspose (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="0042a-103">D3DXMatrixTranspose function (D3dx9math.h)</span></span>

<span data-ttu-id="0042a-104">Возвращает матрицу матрицы.</span><span class="sxs-lookup"><span data-stu-id="0042a-104">Returns the matrix transpose of a matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="0042a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0042a-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixTranspose(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="0042a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0042a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0042a-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="0042a-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0042a-108">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="0042a-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="0042a-109">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="0042a-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="0042a-110">*PM* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0042a-110">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0042a-111">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="0042a-111">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="0042a-112">Указатель на исходную структуру [**D3DXMATRIX**](d3dxmatrix.md) .</span><span class="sxs-lookup"><span data-stu-id="0042a-112">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0042a-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0042a-113">Return value</span></span>

<span data-ttu-id="0042a-114">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="0042a-114">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="0042a-115">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , которая является матрицей матрицы.</span><span class="sxs-lookup"><span data-stu-id="0042a-115">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the matrix transpose of the matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="0042a-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="0042a-116">Remarks</span></span>

<span data-ttu-id="0042a-117">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="0042a-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="0042a-118">Таким образом, функция **D3DXMatrixTranspose** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="0042a-118">In this way, the **D3DXMatrixTranspose** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="0042a-119">Требования</span><span class="sxs-lookup"><span data-stu-id="0042a-119">Requirements</span></span>



| <span data-ttu-id="0042a-120">Требование</span><span class="sxs-lookup"><span data-stu-id="0042a-120">Requirement</span></span> | <span data-ttu-id="0042a-121">Значение</span><span class="sxs-lookup"><span data-stu-id="0042a-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0042a-122">Header</span><span class="sxs-lookup"><span data-stu-id="0042a-122">Header</span></span><br/>  | <dl> <span data-ttu-id="0042a-123"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="0042a-123"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="0042a-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0042a-124">Library</span></span><br/> | <dl> <span data-ttu-id="0042a-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0042a-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0042a-126">См. также</span><span class="sxs-lookup"><span data-stu-id="0042a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0042a-127">Математические функции</span><span class="sxs-lookup"><span data-stu-id="0042a-127">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




