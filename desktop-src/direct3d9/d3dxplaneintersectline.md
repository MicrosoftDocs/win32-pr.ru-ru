---
description: Находит пересечение между плоскостью и линией.
ms.assetid: 2723cd3e-fdc3-4aab-a089-0089e5b14e3e
title: Функция D3DXPlaneIntersectLine (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneIntersectLine
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b4a91a4592d039510e11147ffb680c880c43ccec
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273697"
---
# <a name="d3dxplaneintersectline-function-d3dx9mathh"></a><span data-ttu-id="2872c-103">Функция D3DXPlaneIntersectLine (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="2872c-103">D3DXPlaneIntersectLine function (D3dx9math.h)</span></span>

<span data-ttu-id="2872c-104">Находит пересечение между плоскостью и линией.</span><span class="sxs-lookup"><span data-stu-id="2872c-104">Finds the intersection between a plane and a line.</span></span>

## <a name="syntax"></a><span data-ttu-id="2872c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2872c-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXPlaneIntersectLine(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXPLANE   *pP,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="2872c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2872c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2872c-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="2872c-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2872c-108">Тип: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="2872c-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="2872c-109">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , определяющую пересечение между указанной плоскостью и линией.</span><span class="sxs-lookup"><span data-stu-id="2872c-109">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, identifying the intersection between the specified plane and line.</span></span>

</dd> <dt>

<span data-ttu-id="2872c-110">*PP* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2872c-110">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2872c-111">Тип: **const [**D3DXPLANE**](d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="2872c-111">Type: **const [**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="2872c-112">Указатель на исходную структуру [**D3DXPLANE**](d3dxplane.md) .</span><span class="sxs-lookup"><span data-stu-id="2872c-112">Pointer to the source [**D3DXPLANE**](d3dxplane.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="2872c-113">*pV1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2872c-113">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2872c-114">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="2872c-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="2872c-115">Указатель на исходную структуру [**D3DXVECTOR3**](d3dxvector3.md) , определяющую начальную точку строки.</span><span class="sxs-lookup"><span data-stu-id="2872c-115">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure, defining a line starting point.</span></span>

</dd> <dt>

<span data-ttu-id="2872c-116">*pV2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2872c-116">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2872c-117">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="2872c-117">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="2872c-118">Указатель на исходную структуру [**D3DXVECTOR3**](d3dxvector3.md) , определяющую конечную точку строки.</span><span class="sxs-lookup"><span data-stu-id="2872c-118">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure, defining a line ending point.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2872c-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2872c-119">Return value</span></span>

<span data-ttu-id="2872c-120">Тип: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="2872c-120">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="2872c-121">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , которая является пересечением между указанной плоскостью и линией.</span><span class="sxs-lookup"><span data-stu-id="2872c-121">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the intersection between the specified plane and line.</span></span>

## <a name="remarks"></a><span data-ttu-id="2872c-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2872c-122">Remarks</span></span>

<span data-ttu-id="2872c-123">Если линия параллельна плоскости, возвращается **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="2872c-123">If the line is parallel to the plane, **NULL** is returned.</span></span>

<span data-ttu-id="2872c-124">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="2872c-124">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="2872c-125">Таким образом, функция **D3DXPlaneIntersectLine** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="2872c-125">In this way, the **D3DXPlaneIntersectLine** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="2872c-126">Требования</span><span class="sxs-lookup"><span data-stu-id="2872c-126">Requirements</span></span>



| <span data-ttu-id="2872c-127">Требование</span><span class="sxs-lookup"><span data-stu-id="2872c-127">Requirement</span></span> | <span data-ttu-id="2872c-128">Значение</span><span class="sxs-lookup"><span data-stu-id="2872c-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2872c-129">Header</span><span class="sxs-lookup"><span data-stu-id="2872c-129">Header</span></span><br/>  | <dl> <span data-ttu-id="2872c-130"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="2872c-130"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="2872c-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2872c-131">Library</span></span><br/> | <dl> <span data-ttu-id="2872c-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2872c-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2872c-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2872c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2872c-134">Математические функции</span><span class="sxs-lookup"><span data-stu-id="2872c-134">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




