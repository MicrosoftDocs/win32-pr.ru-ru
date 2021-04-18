---
description: Конструирует плоскость с точки и обычного.
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
ms.openlocfilehash: 8eeb8ea3a1725e0bf615be888d8e862c97730a2c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713457"
---
# <a name="d3dxplanefrompointnormal-function-d3dx9mathh"></a><span data-ttu-id="c376e-103">Функция D3DXPlaneFromPointNormal (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="c376e-103">D3DXPlaneFromPointNormal function (D3dx9math.h)</span></span>

<span data-ttu-id="c376e-104">Конструирует плоскость с точки и обычного.</span><span class="sxs-lookup"><span data-stu-id="c376e-104">Constructs a plane from a point and a normal.</span></span>

## <a name="syntax"></a><span data-ttu-id="c376e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c376e-105">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneFromPointNormal(
  _Inout_       D3DXPLANE   *pOut,
  _In_    const D3DXVECTOR3 *pPoint,
  _In_    const D3DXVECTOR3 *pNormal
);
```



## <a name="parameters"></a><span data-ttu-id="c376e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c376e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c376e-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="c376e-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c376e-108">Тип: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="c376e-108">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="c376e-109">Указатель на структуру [**D3DXPLANE**](d3dxplane.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="c376e-109">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="c376e-110">*ппоинт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c376e-110">*pPoint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c376e-111">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="c376e-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="c376e-112">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , определяющую точку, используемую для создания плоскости.</span><span class="sxs-lookup"><span data-stu-id="c376e-112">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, defining the point used to construct the plane.</span></span>

</dd> <dt>

<span data-ttu-id="c376e-113">*пнормал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c376e-113">*pNormal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c376e-114">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="c376e-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="c376e-115">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , определяющую нормальную, используемую для создания плоскости.</span><span class="sxs-lookup"><span data-stu-id="c376e-115">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, defining the normal used to construct the plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c376e-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c376e-116">Return value</span></span>

<span data-ttu-id="c376e-117">Тип: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="c376e-117">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="c376e-118">Указатель на структуру [**D3DXPLANE**](d3dxplane.md) , созданную из точки и обычного.</span><span class="sxs-lookup"><span data-stu-id="c376e-118">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure constructed from the point and the normal.</span></span>

## <a name="remarks"></a><span data-ttu-id="c376e-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c376e-119">Remarks</span></span>

<span data-ttu-id="c376e-120">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="c376e-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="c376e-121">Таким образом, функция **D3DXPlaneFromPointNormal** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="c376e-121">In this way, the **D3DXPlaneFromPointNormal** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="c376e-122">Требования</span><span class="sxs-lookup"><span data-stu-id="c376e-122">Requirements</span></span>



| <span data-ttu-id="c376e-123">Требование</span><span class="sxs-lookup"><span data-stu-id="c376e-123">Requirement</span></span> | <span data-ttu-id="c376e-124">Значение</span><span class="sxs-lookup"><span data-stu-id="c376e-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c376e-125">Header</span><span class="sxs-lookup"><span data-stu-id="c376e-125">Header</span></span><br/>  | <dl> <span data-ttu-id="c376e-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="c376e-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="c376e-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c376e-127">Library</span></span><br/> | <dl> <span data-ttu-id="c376e-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c376e-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c376e-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c376e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c376e-130">Математические функции</span><span class="sxs-lookup"><span data-stu-id="c376e-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="c376e-131">**D3DXPlaneFromPoints**</span><span class="sxs-lookup"><span data-stu-id="c376e-131">**D3DXPlaneFromPoints**</span></span>](d3dxplanefrompoints.md)
</dt> </dl>

 

 




