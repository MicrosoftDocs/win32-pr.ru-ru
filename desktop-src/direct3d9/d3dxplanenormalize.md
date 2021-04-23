---
description: Нормализует коэффициенты плоскости, чтобы у плоскости была нормальная длина единицы.
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
ms.openlocfilehash: 0f0c87028d3b37f785005725e7510f689cf56d61
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703639"
---
# <a name="d3dxplanenormalize-function-d3dx9mathh"></a><span data-ttu-id="33b50-103">Функция D3DXPlaneNormalize (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="33b50-103">D3DXPlaneNormalize function (D3dx9math.h)</span></span>

<span data-ttu-id="33b50-104">Нормализует коэффициенты плоскости, чтобы у плоскости была нормальная длина единицы.</span><span class="sxs-lookup"><span data-stu-id="33b50-104">Normalizes the plane coefficients so that the plane normal has unit length.</span></span>

## <a name="syntax"></a><span data-ttu-id="33b50-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="33b50-105">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneNormalize(
  _Inout_       D3DXPLANE *pOut,
  _In_    const D3DXPLANE *pP
);
```



## <a name="parameters"></a><span data-ttu-id="33b50-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="33b50-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33b50-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="33b50-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="33b50-108">Тип: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="33b50-108">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="33b50-109">Указатель на структуру [**D3DXPLANE**](d3dxplane.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="33b50-109">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="33b50-110">*PP* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="33b50-110">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33b50-111">Тип: **const [**D3DXPLANE**](d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="33b50-111">Type: **const [**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="33b50-112">Указатель на исходную структуру [**D3DXPLANE**](d3dxplane.md) .</span><span class="sxs-lookup"><span data-stu-id="33b50-112">Pointer to the source [**D3DXPLANE**](d3dxplane.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33b50-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="33b50-113">Return value</span></span>

<span data-ttu-id="33b50-114">Тип: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="33b50-114">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="33b50-115">Указатель на структуру [**D3DXPLANE**](d3dxplane.md) , представляющую нормальную плоскость плоскости.</span><span class="sxs-lookup"><span data-stu-id="33b50-115">Pointer to a [**D3DXPLANE**](d3dxplane.md) structure that represents the normal of the plane.</span></span>

## <a name="remarks"></a><span data-ttu-id="33b50-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="33b50-116">Remarks</span></span>

<span data-ttu-id="33b50-117">Эта функция нормализует плоскость таким образом, чтобы \| a, b, c \| = = 1.</span><span class="sxs-lookup"><span data-stu-id="33b50-117">This function normalizes a plane so that \|a,b,c\| == 1.</span></span>

<span data-ttu-id="33b50-118">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="33b50-118">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="33b50-119">Таким образом, эта функция может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="33b50-119">In this way, this function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="33b50-120">Требования</span><span class="sxs-lookup"><span data-stu-id="33b50-120">Requirements</span></span>



| <span data-ttu-id="33b50-121">Требование</span><span class="sxs-lookup"><span data-stu-id="33b50-121">Requirement</span></span> | <span data-ttu-id="33b50-122">Значение</span><span class="sxs-lookup"><span data-stu-id="33b50-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="33b50-123">Header</span><span class="sxs-lookup"><span data-stu-id="33b50-123">Header</span></span><br/>  | <dl> <span data-ttu-id="33b50-124"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="33b50-124"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="33b50-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="33b50-125">Library</span></span><br/> | <dl> <span data-ttu-id="33b50-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="33b50-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="33b50-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="33b50-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33b50-128">Математические функции</span><span class="sxs-lookup"><span data-stu-id="33b50-128">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




