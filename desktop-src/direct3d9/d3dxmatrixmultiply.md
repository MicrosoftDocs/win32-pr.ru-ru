---
description: Функция D3DXMatrixMultiply (D3dx9math. h) — Определяет произведение двух матриц.
ms.assetid: 160c801a-6589-4a0d-8e90-7e7a99fbd5f7
title: Функция D3DXMatrixMultiply (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixMultiply
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3d183fc3c79797bab886d3a40211448ccf57d552
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107552"
---
# <a name="d3dxmatrixmultiply-function-d3dx9mathh"></a><span data-ttu-id="4f649-103">Функция D3DXMatrixMultiply (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="4f649-103">D3DXMatrixMultiply function (D3dx9math.h)</span></span>

<span data-ttu-id="4f649-104">Определяет произведение двух матриц.</span><span class="sxs-lookup"><span data-stu-id="4f649-104">Determines the product of two matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f649-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4f649-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixMultiply(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXMATRIX *pM1,
  _In_    const D3DXMATRIX *pM2
);
```



## <a name="parameters"></a><span data-ttu-id="4f649-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4f649-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f649-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="4f649-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4f649-108">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="4f649-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="4f649-109">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="4f649-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="4f649-110">*pM1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4f649-110">*pM1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f649-111">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="4f649-111">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="4f649-112">Указатель на исходную структуру [**D3DXMATRIX**](d3dxmatrix.md) .</span><span class="sxs-lookup"><span data-stu-id="4f649-112">Pointer to a source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="4f649-113">*pM2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4f649-113">*pM2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f649-114">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="4f649-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="4f649-115">Указатель на исходную структуру [**D3DXMATRIX**](d3dxmatrix.md) .</span><span class="sxs-lookup"><span data-stu-id="4f649-115">Pointer to a source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f649-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4f649-116">Return value</span></span>

<span data-ttu-id="4f649-117">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="4f649-117">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="4f649-118">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , которая является произведением двух матриц.</span><span class="sxs-lookup"><span data-stu-id="4f649-118">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is the product of two matrices.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f649-119">Remarks</span><span class="sxs-lookup"><span data-stu-id="4f649-119">Remarks</span></span>

<span data-ttu-id="4f649-120">Результат представляет преобразование M1, за которым следует преобразование m2 (out = M1 \* m2).</span><span class="sxs-lookup"><span data-stu-id="4f649-120">The result represents the transformation M1 followed by the transformation M2 (Out = M1 \* M2).</span></span>

<span data-ttu-id="4f649-121">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="4f649-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="4f649-122">Таким образом, функция **D3DXMatrixMultiply** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="4f649-122">In this way, the **D3DXMatrixMultiply** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f649-123">Требования</span><span class="sxs-lookup"><span data-stu-id="4f649-123">Requirements</span></span>



| <span data-ttu-id="4f649-124">Требование</span><span class="sxs-lookup"><span data-stu-id="4f649-124">Requirement</span></span> | <span data-ttu-id="4f649-125">Значение</span><span class="sxs-lookup"><span data-stu-id="4f649-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f649-126">Header</span><span class="sxs-lookup"><span data-stu-id="4f649-126">Header</span></span><br/>  | <dl> <span data-ttu-id="4f649-127"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f649-127"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="4f649-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4f649-128">Library</span></span><br/> | <dl> <span data-ttu-id="4f649-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4f649-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4f649-130">См. также</span><span class="sxs-lookup"><span data-stu-id="4f649-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f649-131">Математические функции</span><span class="sxs-lookup"><span data-stu-id="4f649-131">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="4f649-132">**D3DXQuaternionMultiply**</span><span class="sxs-lookup"><span data-stu-id="4f649-132">**D3DXQuaternionMultiply**</span></span>](d3dxquaternionmultiply.md)
</dt> </dl>

 

 




