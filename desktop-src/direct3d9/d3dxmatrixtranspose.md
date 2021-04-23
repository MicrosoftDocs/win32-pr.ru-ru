---
description: Возвращает матрицу матрицы.
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
ms.openlocfilehash: 700fc023cd15227c2cf26cd5bdcab51dc0ae3297
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713473"
---
# <a name="d3dxmatrixtranspose-function-d3dx9mathh"></a><span data-ttu-id="8c19d-103">Функция D3DXMatrixTranspose (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="8c19d-103">D3DXMatrixTranspose function (D3dx9math.h)</span></span>

<span data-ttu-id="8c19d-104">Возвращает матрицу матрицы.</span><span class="sxs-lookup"><span data-stu-id="8c19d-104">Returns the matrix transpose of a matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c19d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8c19d-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixTranspose(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="8c19d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8c19d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c19d-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="8c19d-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8c19d-108">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="8c19d-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="8c19d-109">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="8c19d-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="8c19d-110">*PM* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8c19d-110">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c19d-111">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="8c19d-111">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="8c19d-112">Указатель на исходную структуру [**D3DXMATRIX**](d3dxmatrix.md) .</span><span class="sxs-lookup"><span data-stu-id="8c19d-112">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c19d-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8c19d-113">Return value</span></span>

<span data-ttu-id="8c19d-114">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="8c19d-114">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="8c19d-115">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , которая является матрицей матрицы.</span><span class="sxs-lookup"><span data-stu-id="8c19d-115">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the matrix transpose of the matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c19d-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8c19d-116">Remarks</span></span>

<span data-ttu-id="8c19d-117">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="8c19d-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="8c19d-118">Таким образом, функция **D3DXMatrixTranspose** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="8c19d-118">In this way, the **D3DXMatrixTranspose** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c19d-119">Требования</span><span class="sxs-lookup"><span data-stu-id="8c19d-119">Requirements</span></span>



| <span data-ttu-id="8c19d-120">Требование</span><span class="sxs-lookup"><span data-stu-id="8c19d-120">Requirement</span></span> | <span data-ttu-id="8c19d-121">Значение</span><span class="sxs-lookup"><span data-stu-id="8c19d-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8c19d-122">Header</span><span class="sxs-lookup"><span data-stu-id="8c19d-122">Header</span></span><br/>  | <dl> <span data-ttu-id="8c19d-123"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c19d-123"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="8c19d-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8c19d-124">Library</span></span><br/> | <dl> <span data-ttu-id="8c19d-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8c19d-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8c19d-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8c19d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c19d-127">Математические функции</span><span class="sxs-lookup"><span data-stu-id="8c19d-127">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




