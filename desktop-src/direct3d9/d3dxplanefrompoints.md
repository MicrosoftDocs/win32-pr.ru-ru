---
description: Конструирует плоскость из трех точек.
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
ms.openlocfilehash: c537915c56cdbbfb33228b0c5a5ea3f2acc2baff
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713458"
---
# <a name="d3dxplanefrompoints-function-d3dx9mathh"></a><span data-ttu-id="f4069-103">Функция D3DXPlaneFromPoints (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="f4069-103">D3DXPlaneFromPoints function (D3dx9math.h)</span></span>

<span data-ttu-id="f4069-104">Конструирует плоскость из трех точек.</span><span class="sxs-lookup"><span data-stu-id="f4069-104">Constructs a plane from three points.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4069-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f4069-105">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneFromPoints(
  _Inout_       D3DXPLANE   *pOut,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2,
  _In_    const D3DXVECTOR3 *pV3
);
```



## <a name="parameters"></a><span data-ttu-id="f4069-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f4069-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4069-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="f4069-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f4069-108">Тип: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="f4069-108">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="f4069-109">Указатель на структуру [**D3DXPLANE**](d3dxplane.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="f4069-109">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="f4069-110">*pV1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f4069-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4069-111">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="f4069-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="f4069-112">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , определяющую одну из точек, используемых для создания плоскости.</span><span class="sxs-lookup"><span data-stu-id="f4069-112">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, defining one of the points used to construct the plane.</span></span>

</dd> <dt>

<span data-ttu-id="f4069-113">*pV2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f4069-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4069-114">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="f4069-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="f4069-115">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , определяющую одну из точек, используемых для создания плоскости.</span><span class="sxs-lookup"><span data-stu-id="f4069-115">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, defining one of the points used to construct the plane.</span></span>

</dd> <dt>

<span data-ttu-id="f4069-116">*pV3* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f4069-116">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4069-117">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="f4069-117">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="f4069-118">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , определяющую одну из точек, используемых для создания плоскости.</span><span class="sxs-lookup"><span data-stu-id="f4069-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, defining one of the points used to construct the plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4069-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f4069-119">Return value</span></span>

<span data-ttu-id="f4069-120">Тип: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="f4069-120">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="f4069-121">Указатель на структуру [**D3DXPLANE**](d3dxplane.md) , созданную из заданных точек.</span><span class="sxs-lookup"><span data-stu-id="f4069-121">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure constructed from the given points.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4069-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f4069-122">Remarks</span></span>

<span data-ttu-id="f4069-123">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="f4069-123">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="f4069-124">Таким образом, функция **D3DXPlaneFromPoints** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="f4069-124">In this way, the **D3DXPlaneFromPoints** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4069-125">Требования</span><span class="sxs-lookup"><span data-stu-id="f4069-125">Requirements</span></span>



| <span data-ttu-id="f4069-126">Требование</span><span class="sxs-lookup"><span data-stu-id="f4069-126">Requirement</span></span> | <span data-ttu-id="f4069-127">Значение</span><span class="sxs-lookup"><span data-stu-id="f4069-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f4069-128">Header</span><span class="sxs-lookup"><span data-stu-id="f4069-128">Header</span></span><br/>  | <dl> <span data-ttu-id="f4069-129"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4069-129"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="f4069-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f4069-130">Library</span></span><br/> | <dl> <span data-ttu-id="f4069-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f4069-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f4069-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f4069-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4069-133">Математические функции</span><span class="sxs-lookup"><span data-stu-id="f4069-133">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="f4069-134">**D3DXPlaneFromPointNormal**</span><span class="sxs-lookup"><span data-stu-id="f4069-134">**D3DXPlaneFromPointNormal**</span></span>](d3dxplanefrompointnormal.md)
</dt> </dl>

 

 




