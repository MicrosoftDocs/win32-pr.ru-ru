---
description: Определяет произведение двух матриц.
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
ms.openlocfilehash: ea578f54d3f690f01d9280e840cb9ee039d0cdf0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703643"
---
# <a name="d3dxmatrixmultiply-function-d3dx9mathh"></a><span data-ttu-id="d9352-103">Функция D3DXMatrixMultiply (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="d9352-103">D3DXMatrixMultiply function (D3dx9math.h)</span></span>

<span data-ttu-id="d9352-104">Определяет произведение двух матриц.</span><span class="sxs-lookup"><span data-stu-id="d9352-104">Determines the product of two matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9352-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d9352-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixMultiply(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXMATRIX *pM1,
  _In_    const D3DXMATRIX *pM2
);
```



## <a name="parameters"></a><span data-ttu-id="d9352-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d9352-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9352-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="d9352-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d9352-108">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="d9352-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d9352-109">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="d9352-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="d9352-110">*pM1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d9352-110">*pM1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9352-111">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="d9352-111">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d9352-112">Указатель на исходную структуру [**D3DXMATRIX**](d3dxmatrix.md) .</span><span class="sxs-lookup"><span data-stu-id="d9352-112">Pointer to a source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="d9352-113">*pM2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d9352-113">*pM2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9352-114">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="d9352-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d9352-115">Указатель на исходную структуру [**D3DXMATRIX**](d3dxmatrix.md) .</span><span class="sxs-lookup"><span data-stu-id="d9352-115">Pointer to a source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9352-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d9352-116">Return value</span></span>

<span data-ttu-id="d9352-117">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="d9352-117">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d9352-118">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , которая является произведением двух матриц.</span><span class="sxs-lookup"><span data-stu-id="d9352-118">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is the product of two matrices.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9352-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d9352-119">Remarks</span></span>

<span data-ttu-id="d9352-120">Результат представляет преобразование M1, за которым следует преобразование m2 (out = M1 \* m2).</span><span class="sxs-lookup"><span data-stu-id="d9352-120">The result represents the transformation M1 followed by the transformation M2 (Out = M1 \* M2).</span></span>

<span data-ttu-id="d9352-121">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="d9352-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="d9352-122">Таким образом, функция **D3DXMatrixMultiply** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="d9352-122">In this way, the **D3DXMatrixMultiply** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9352-123">Требования</span><span class="sxs-lookup"><span data-stu-id="d9352-123">Requirements</span></span>



| <span data-ttu-id="d9352-124">Требование</span><span class="sxs-lookup"><span data-stu-id="d9352-124">Requirement</span></span> | <span data-ttu-id="d9352-125">Значение</span><span class="sxs-lookup"><span data-stu-id="d9352-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d9352-126">Header</span><span class="sxs-lookup"><span data-stu-id="d9352-126">Header</span></span><br/>  | <dl> <span data-ttu-id="d9352-127"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9352-127"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="d9352-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d9352-128">Library</span></span><br/> | <dl> <span data-ttu-id="d9352-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d9352-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d9352-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d9352-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9352-131">Математические функции</span><span class="sxs-lookup"><span data-stu-id="d9352-131">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="d9352-132">**D3DXQuaternionMultiply**</span><span class="sxs-lookup"><span data-stu-id="d9352-132">**D3DXQuaternionMultiply**</span></span>](d3dxquaternionmultiply.md)
</dt> </dl>

 

 




