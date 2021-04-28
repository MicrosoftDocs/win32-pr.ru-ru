---
description: Функция D3DXPlaneFromPoints (D3dx9math. h) — конструирует плоскость из трех точек.
ms.assetid: 13d5ce6b-0046-441b-b826-f34f4fe16979
title: Функция D3DXPlaneFromPoints (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneFromPoints
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0d945dff9c124f4c66cea4f9d61c490c6eaf7a66
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094162"
---
# <a name="d3dxplanefrompoints-function-d3dx9mathh"></a><span data-ttu-id="c395e-103">Функция D3DXPlaneFromPoints (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="c395e-103">D3DXPlaneFromPoints function (D3dx9math.h)</span></span>

<span data-ttu-id="c395e-104">Конструирует плоскость из трех точек.</span><span class="sxs-lookup"><span data-stu-id="c395e-104">Constructs a plane from three points.</span></span>

## <a name="syntax"></a><span data-ttu-id="c395e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c395e-105">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneFromPoints(
  _Inout_       D3DXPLANE   *pOut,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2,
  _In_    const D3DXVECTOR3 *pV3
);
```



## <a name="parameters"></a><span data-ttu-id="c395e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c395e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c395e-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="c395e-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c395e-108">Тип: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="c395e-108">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="c395e-109">Указатель на структуру [**D3DXPLANE**](d3dxplane.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="c395e-109">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="c395e-110">*pV1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c395e-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c395e-111">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="c395e-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="c395e-112">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , определяющую одну из точек, используемых для создания плоскости.</span><span class="sxs-lookup"><span data-stu-id="c395e-112">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, defining one of the points used to construct the plane.</span></span>

</dd> <dt>

<span data-ttu-id="c395e-113">*pV2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c395e-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c395e-114">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="c395e-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="c395e-115">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , определяющую одну из точек, используемых для создания плоскости.</span><span class="sxs-lookup"><span data-stu-id="c395e-115">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, defining one of the points used to construct the plane.</span></span>

</dd> <dt>

<span data-ttu-id="c395e-116">*pV3* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c395e-116">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c395e-117">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="c395e-117">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="c395e-118">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , определяющую одну из точек, используемых для создания плоскости.</span><span class="sxs-lookup"><span data-stu-id="c395e-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, defining one of the points used to construct the plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c395e-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c395e-119">Return value</span></span>

<span data-ttu-id="c395e-120">Тип: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="c395e-120">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="c395e-121">Указатель на структуру [**D3DXPLANE**](d3dxplane.md) , созданную из заданных точек.</span><span class="sxs-lookup"><span data-stu-id="c395e-121">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure constructed from the given points.</span></span>

## <a name="remarks"></a><span data-ttu-id="c395e-122">Remarks</span><span class="sxs-lookup"><span data-stu-id="c395e-122">Remarks</span></span>

<span data-ttu-id="c395e-123">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="c395e-123">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="c395e-124">Таким образом, функция **D3DXPlaneFromPoints** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="c395e-124">In this way, the **D3DXPlaneFromPoints** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="c395e-125">Требования</span><span class="sxs-lookup"><span data-stu-id="c395e-125">Requirements</span></span>



| <span data-ttu-id="c395e-126">Требование</span><span class="sxs-lookup"><span data-stu-id="c395e-126">Requirement</span></span> | <span data-ttu-id="c395e-127">Значение</span><span class="sxs-lookup"><span data-stu-id="c395e-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c395e-128">Header</span><span class="sxs-lookup"><span data-stu-id="c395e-128">Header</span></span><br/>  | <dl> <span data-ttu-id="c395e-129"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="c395e-129"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="c395e-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c395e-130">Library</span></span><br/> | <dl> <span data-ttu-id="c395e-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c395e-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c395e-132">См. также</span><span class="sxs-lookup"><span data-stu-id="c395e-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c395e-133">Математические функции</span><span class="sxs-lookup"><span data-stu-id="c395e-133">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="c395e-134">**D3DXPlaneFromPointNormal**</span><span class="sxs-lookup"><span data-stu-id="c395e-134">**D3DXPlaneFromPointNormal**</span></span>](d3dxplanefrompointnormal.md)
</dt> </dl>

 

 




