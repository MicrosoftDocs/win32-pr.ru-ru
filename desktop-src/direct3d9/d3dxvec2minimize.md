---
description: Возвращает двумерный вектор, который состоит из наименьших компонентов двух двумерных векторов.
ms.assetid: 6944523e-33dd-456e-9cc2-17760d76c548
title: Функция D3DXVec2Minimize (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Minimize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1914ae9317d686e369f1cb2c7eb36ab54a29845f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703721"
---
# <a name="d3dxvec2minimize-function"></a><span data-ttu-id="9abb0-103">Функция D3DXVec2Minimize</span><span class="sxs-lookup"><span data-stu-id="9abb0-103">D3DXVec2Minimize function</span></span>

<span data-ttu-id="9abb0-104">Возвращает двумерный вектор, который состоит из наименьших компонентов двух двумерных векторов.</span><span class="sxs-lookup"><span data-stu-id="9abb0-104">Returns a 2D vector that is made up of the smallest components of two 2D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="9abb0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9abb0-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2Minimize(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV1,
  _In_    const D3DXVECTOR2 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="9abb0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9abb0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9abb0-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="9abb0-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9abb0-108">Тип: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="9abb0-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="9abb0-109">Указатель на структуру [**D3DXVECTOR2**](d3dxvector2.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="9abb0-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="9abb0-110">*pV1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9abb0-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9abb0-111">Тип: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="9abb0-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="9abb0-112">Указатель на исходную структуру [**D3DXVECTOR2**](d3dxvector2.md) .</span><span class="sxs-lookup"><span data-stu-id="9abb0-112">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="9abb0-113">*pV2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9abb0-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9abb0-114">Тип: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="9abb0-114">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="9abb0-115">Указатель на исходную структуру [**D3DXVECTOR2**](d3dxvector2.md) .</span><span class="sxs-lookup"><span data-stu-id="9abb0-115">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9abb0-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9abb0-116">Return value</span></span>

<span data-ttu-id="9abb0-117">Тип: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="9abb0-117">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="9abb0-118">Указатель на структуру [**D3DXVECTOR2**](d3dxvector2.md) , которая состоит из наименьших компонентов двух векторов.</span><span class="sxs-lookup"><span data-stu-id="9abb0-118">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that is made up of the smallest components of the two vectors.</span></span>

## <a name="remarks"></a><span data-ttu-id="9abb0-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9abb0-119">Remarks</span></span>

<span data-ttu-id="9abb0-120">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="9abb0-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="9abb0-121">Таким образом, функция **D3DXVec2Minimize** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="9abb0-121">In this way, the **D3DXVec2Minimize** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="9abb0-122">Требования</span><span class="sxs-lookup"><span data-stu-id="9abb0-122">Requirements</span></span>



| <span data-ttu-id="9abb0-123">Требование</span><span class="sxs-lookup"><span data-stu-id="9abb0-123">Requirement</span></span> | <span data-ttu-id="9abb0-124">Значение</span><span class="sxs-lookup"><span data-stu-id="9abb0-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9abb0-125">Header</span><span class="sxs-lookup"><span data-stu-id="9abb0-125">Header</span></span><br/>  | <dl> <span data-ttu-id="9abb0-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="9abb0-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="9abb0-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9abb0-127">Library</span></span><br/> | <dl> <span data-ttu-id="9abb0-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9abb0-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9abb0-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9abb0-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9abb0-130">Математические функции</span><span class="sxs-lookup"><span data-stu-id="9abb0-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="9abb0-131">**D3DXVec2Maximize**</span><span class="sxs-lookup"><span data-stu-id="9abb0-131">**D3DXVec2Maximize**</span></span>](d3dxvec2maximize.md)
</dt> </dl>

 

 




