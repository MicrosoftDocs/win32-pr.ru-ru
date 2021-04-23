---
description: Возвращает вектор 4D, который состоит из наименьших компонентов двух векторов 4D.
ms.assetid: ae3819a3-a5b6-47c2-b789-3e3f07db9f03
title: Функция D3DXVec4Minimize (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Minimize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9ccd4806bfa368fafa481500d3bd28e0ff55b7d2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703820"
---
# <a name="d3dxvec4minimize-function"></a><span data-ttu-id="8c6ec-103">Функция D3DXVec4Minimize</span><span class="sxs-lookup"><span data-stu-id="8c6ec-103">D3DXVec4Minimize function</span></span>

<span data-ttu-id="8c6ec-104">Возвращает вектор 4D, который состоит из наименьших компонентов двух векторов 4D.</span><span class="sxs-lookup"><span data-stu-id="8c6ec-104">Returns a 4D vector that is made up of the smallest components of two 4D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c6ec-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8c6ec-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Minimize(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV1,
  _In_    const D3DXVECTOR4 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="8c6ec-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8c6ec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c6ec-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="8c6ec-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8c6ec-108">Тип: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="8c6ec-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="8c6ec-109">Указатель на структуру [**D3DXVECTOR4**](d3dxvector4.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="8c6ec-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="8c6ec-110">*pV1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8c6ec-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c6ec-111">Тип: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="8c6ec-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="8c6ec-112">Указатель на исходную структуру [**D3DXVECTOR4**](d3dxvector4.md) .</span><span class="sxs-lookup"><span data-stu-id="8c6ec-112">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="8c6ec-113">*pV2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8c6ec-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c6ec-114">Тип: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="8c6ec-114">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="8c6ec-115">Указатель на исходную структуру [**D3DXVECTOR4**](d3dxvector4.md) .</span><span class="sxs-lookup"><span data-stu-id="8c6ec-115">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c6ec-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8c6ec-116">Return value</span></span>

<span data-ttu-id="8c6ec-117">Тип: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="8c6ec-117">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="8c6ec-118">Указатель на структуру [**D3DXVECTOR4**](d3dxvector4.md) , которая состоит из наименьших компонентов двух векторов.</span><span class="sxs-lookup"><span data-stu-id="8c6ec-118">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is made up of the smallest components of the two vectors.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c6ec-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8c6ec-119">Remarks</span></span>

<span data-ttu-id="8c6ec-120">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="8c6ec-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="8c6ec-121">Таким образом, функция **D3DXVec4Minimize** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="8c6ec-121">In this way, the **D3DXVec4Minimize** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c6ec-122">Требования</span><span class="sxs-lookup"><span data-stu-id="8c6ec-122">Requirements</span></span>



| <span data-ttu-id="8c6ec-123">Требование</span><span class="sxs-lookup"><span data-stu-id="8c6ec-123">Requirement</span></span> | <span data-ttu-id="8c6ec-124">Значение</span><span class="sxs-lookup"><span data-stu-id="8c6ec-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8c6ec-125">Header</span><span class="sxs-lookup"><span data-stu-id="8c6ec-125">Header</span></span><br/>  | <dl> <span data-ttu-id="8c6ec-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c6ec-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="8c6ec-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8c6ec-127">Library</span></span><br/> | <dl> <span data-ttu-id="8c6ec-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8c6ec-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8c6ec-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8c6ec-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c6ec-130">Математические функции</span><span class="sxs-lookup"><span data-stu-id="8c6ec-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="8c6ec-131">**D3DXVec4Maximize**</span><span class="sxs-lookup"><span data-stu-id="8c6ec-131">**D3DXVec4Maximize**</span></span>](d3dxvec4maximize.md)
</dt> </dl>

 

 




