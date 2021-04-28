---
description: Функция D3DXPlaneFromPointNormal (D3dx9math. h) — конструирует плоскость с точки и обычного.
ms.assetid: af396bbb-09b7-492f-a25f-9c950da7e605
title: Функция D3DXPlaneFromPointNormal (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneFromPointNormal
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e34765d150932d6a7b3b0293e603237ffb2b45ad
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098092"
---
# <a name="d3dxplanefrompointnormal-function-d3dx9mathh"></a><span data-ttu-id="07a80-103">Функция D3DXPlaneFromPointNormal (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="07a80-103">D3DXPlaneFromPointNormal function (D3dx9math.h)</span></span>

<span data-ttu-id="07a80-104">Конструирует плоскость с точки и обычного.</span><span class="sxs-lookup"><span data-stu-id="07a80-104">Constructs a plane from a point and a normal.</span></span>

## <a name="syntax"></a><span data-ttu-id="07a80-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="07a80-105">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneFromPointNormal(
  _Inout_       D3DXPLANE   *pOut,
  _In_    const D3DXVECTOR3 *pPoint,
  _In_    const D3DXVECTOR3 *pNormal
);
```



## <a name="parameters"></a><span data-ttu-id="07a80-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="07a80-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07a80-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="07a80-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="07a80-108">Тип: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="07a80-108">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="07a80-109">Указатель на структуру [**D3DXPLANE**](d3dxplane.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="07a80-109">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="07a80-110">*ппоинт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="07a80-110">*pPoint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07a80-111">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="07a80-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="07a80-112">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , определяющую точку, используемую для создания плоскости.</span><span class="sxs-lookup"><span data-stu-id="07a80-112">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, defining the point used to construct the plane.</span></span>

</dd> <dt>

<span data-ttu-id="07a80-113">*пнормал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="07a80-113">*pNormal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07a80-114">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="07a80-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="07a80-115">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , определяющую нормальную, используемую для создания плоскости.</span><span class="sxs-lookup"><span data-stu-id="07a80-115">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, defining the normal used to construct the plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07a80-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="07a80-116">Return value</span></span>

<span data-ttu-id="07a80-117">Тип: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="07a80-117">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="07a80-118">Указатель на структуру [**D3DXPLANE**](d3dxplane.md) , созданную из точки и обычного.</span><span class="sxs-lookup"><span data-stu-id="07a80-118">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure constructed from the point and the normal.</span></span>

## <a name="remarks"></a><span data-ttu-id="07a80-119">Remarks</span><span class="sxs-lookup"><span data-stu-id="07a80-119">Remarks</span></span>

<span data-ttu-id="07a80-120">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="07a80-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="07a80-121">Таким образом, функция **D3DXPlaneFromPointNormal** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="07a80-121">In this way, the **D3DXPlaneFromPointNormal** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="07a80-122">Требования</span><span class="sxs-lookup"><span data-stu-id="07a80-122">Requirements</span></span>



| <span data-ttu-id="07a80-123">Требование</span><span class="sxs-lookup"><span data-stu-id="07a80-123">Requirement</span></span> | <span data-ttu-id="07a80-124">Значение</span><span class="sxs-lookup"><span data-stu-id="07a80-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="07a80-125">Header</span><span class="sxs-lookup"><span data-stu-id="07a80-125">Header</span></span><br/>  | <dl> <span data-ttu-id="07a80-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="07a80-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="07a80-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="07a80-127">Library</span></span><br/> | <dl> <span data-ttu-id="07a80-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="07a80-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="07a80-129">См. также</span><span class="sxs-lookup"><span data-stu-id="07a80-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07a80-130">Математические функции</span><span class="sxs-lookup"><span data-stu-id="07a80-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="07a80-131">**D3DXPlaneFromPoints**</span><span class="sxs-lookup"><span data-stu-id="07a80-131">**D3DXPlaneFromPoints**</span></span>](d3dxplanefrompoints.md)
</dt> </dl>

 

 




