---
description: Функция D3DXPlaneNormalize (D3dx9math. h) — нормализует коэффициенты плоскости таким образом, чтобы у плоскости была нормальная длина.
ms.assetid: 9c595986-e1f8-4153-ba23-1fa6e583a050
title: Функция D3DXPlaneNormalize (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneNormalize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d38ccbc3f688ed61779cf48a77e97dfb544c686e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094152"
---
# <a name="d3dxplanenormalize-function-d3dx9mathh"></a><span data-ttu-id="109a3-103">Функция D3DXPlaneNormalize (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="109a3-103">D3DXPlaneNormalize function (D3dx9math.h)</span></span>

<span data-ttu-id="109a3-104">Нормализует коэффициенты плоскости, чтобы у плоскости была нормальная длина единицы.</span><span class="sxs-lookup"><span data-stu-id="109a3-104">Normalizes the plane coefficients so that the plane normal has unit length.</span></span>

## <a name="syntax"></a><span data-ttu-id="109a3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="109a3-105">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneNormalize(
  _Inout_       D3DXPLANE *pOut,
  _In_    const D3DXPLANE *pP
);
```



## <a name="parameters"></a><span data-ttu-id="109a3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="109a3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="109a3-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="109a3-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="109a3-108">Тип: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="109a3-108">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="109a3-109">Указатель на структуру [**D3DXPLANE**](d3dxplane.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="109a3-109">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="109a3-110">*PP* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="109a3-110">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="109a3-111">Тип: **const [**D3DXPLANE**](d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="109a3-111">Type: **const [**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="109a3-112">Указатель на исходную структуру [**D3DXPLANE**](d3dxplane.md) .</span><span class="sxs-lookup"><span data-stu-id="109a3-112">Pointer to the source [**D3DXPLANE**](d3dxplane.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="109a3-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="109a3-113">Return value</span></span>

<span data-ttu-id="109a3-114">Тип: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="109a3-114">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="109a3-115">Указатель на структуру [**D3DXPLANE**](d3dxplane.md) , представляющую нормальную плоскость плоскости.</span><span class="sxs-lookup"><span data-stu-id="109a3-115">Pointer to a [**D3DXPLANE**](d3dxplane.md) structure that represents the normal of the plane.</span></span>

## <a name="remarks"></a><span data-ttu-id="109a3-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="109a3-116">Remarks</span></span>

<span data-ttu-id="109a3-117">Эта функция нормализует плоскость таким образом, чтобы \| a, b, c \| = = 1.</span><span class="sxs-lookup"><span data-stu-id="109a3-117">This function normalizes a plane so that \|a,b,c\| == 1.</span></span>

<span data-ttu-id="109a3-118">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="109a3-118">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="109a3-119">Таким образом, эта функция может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="109a3-119">In this way, this function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="109a3-120">Требования</span><span class="sxs-lookup"><span data-stu-id="109a3-120">Requirements</span></span>



| <span data-ttu-id="109a3-121">Требование</span><span class="sxs-lookup"><span data-stu-id="109a3-121">Requirement</span></span> | <span data-ttu-id="109a3-122">Значение</span><span class="sxs-lookup"><span data-stu-id="109a3-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="109a3-123">Header</span><span class="sxs-lookup"><span data-stu-id="109a3-123">Header</span></span><br/>  | <dl> <span data-ttu-id="109a3-124"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="109a3-124"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="109a3-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="109a3-125">Library</span></span><br/> | <dl> <span data-ttu-id="109a3-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="109a3-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="109a3-127">См. также</span><span class="sxs-lookup"><span data-stu-id="109a3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="109a3-128">Математические функции</span><span class="sxs-lookup"><span data-stu-id="109a3-128">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




