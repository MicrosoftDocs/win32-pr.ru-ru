---
description: Функция D3DXPlaneNormalize (D3DX10Math. h) — нормализует коэффициенты плоскости таким образом, чтобы у плоскости была нормальная длина.
ms.assetid: 52ae36a7-e37b-457a-9832-e62900a85bde
title: Функция D3DXPlaneNormalize (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8b3499297a008b0d8f5dc705080bbd1d5bbe3af4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103312"
---
# <a name="d3dxplanenormalize-function-d3dx10mathh"></a><span data-ttu-id="327b7-103">Функция D3DXPlaneNormalize (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="327b7-103">D3DXPlaneNormalize function (D3DX10Math.h)</span></span>

<span data-ttu-id="327b7-104">Нормализует коэффициенты плоскости, чтобы у плоскости была нормальная длина единицы.</span><span class="sxs-lookup"><span data-stu-id="327b7-104">Normalizes the plane coefficients so that the plane normal has unit length.</span></span>

## <a name="syntax"></a><span data-ttu-id="327b7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="327b7-105">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneNormalize(
  _Inout_       D3DXPLANE *pOut,
  _In_    const D3DXPLANE *pP
);
```



## <a name="parameters"></a><span data-ttu-id="327b7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="327b7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="327b7-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="327b7-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="327b7-108">Тип: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="327b7-108">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="327b7-109">Указатель на [**D3DXPLANE**](d3d10-d3dxplane.md) , который является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="327b7-109">Pointer to the [**D3DXPLANE**](d3d10-d3dxplane.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="327b7-110">*PP* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="327b7-110">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="327b7-111">Тип: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="327b7-111">Type: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="327b7-112">Указатель на исходную структуру D3DXPLANE.</span><span class="sxs-lookup"><span data-stu-id="327b7-112">Pointer to the source D3DXPLANE structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="327b7-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="327b7-113">Return value</span></span>

<span data-ttu-id="327b7-114">Тип: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="327b7-114">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="327b7-115">Указатель на структуру D3DXPLANE, представляющую нормальную плоскость плоскости.</span><span class="sxs-lookup"><span data-stu-id="327b7-115">Pointer to a D3DXPLANE structure that represents the normal of the plane.</span></span>

## <a name="remarks"></a><span data-ttu-id="327b7-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="327b7-116">Remarks</span></span>

<span data-ttu-id="327b7-117">Эта функция нормализует плоскость таким образом, чтобы \| a, b, c \| = = 1.</span><span class="sxs-lookup"><span data-stu-id="327b7-117">This function normalizes a plane so that \|a,b,c\| == 1.</span></span>

<span data-ttu-id="327b7-118">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="327b7-118">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="327b7-119">Таким образом, эта функция может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="327b7-119">In this way, this function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="327b7-120">Требования</span><span class="sxs-lookup"><span data-stu-id="327b7-120">Requirements</span></span>



| <span data-ttu-id="327b7-121">Требование</span><span class="sxs-lookup"><span data-stu-id="327b7-121">Requirement</span></span> | <span data-ttu-id="327b7-122">Значение</span><span class="sxs-lookup"><span data-stu-id="327b7-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="327b7-123">Header</span><span class="sxs-lookup"><span data-stu-id="327b7-123">Header</span></span><br/>  | <dl> <span data-ttu-id="327b7-124"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="327b7-124"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="327b7-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="327b7-125">Library</span></span><br/> | <dl> <span data-ttu-id="327b7-126"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="327b7-126"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="327b7-127">См. также</span><span class="sxs-lookup"><span data-stu-id="327b7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="327b7-128">Математические функции</span><span class="sxs-lookup"><span data-stu-id="327b7-128">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
