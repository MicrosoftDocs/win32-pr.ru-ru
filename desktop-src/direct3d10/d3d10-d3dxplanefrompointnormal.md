---
description: Функция D3DXPlaneFromPointNormal (D3DX10Math. h) — конструирует плоскость с точки и обычного.
ms.assetid: 93c644d2-ab8c-47a1-9a3b-8b9c6a13178b
title: Функция D3DXPlaneFromPointNormal (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 519ce82a8d5a8c6adaf22b69047a8d365bd777ac
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108842"
---
# <a name="d3dxplanefrompointnormal-function-d3dx10mathh"></a><span data-ttu-id="34e88-103">Функция D3DXPlaneFromPointNormal (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="34e88-103">D3DXPlaneFromPointNormal function (D3DX10Math.h)</span></span>

<span data-ttu-id="34e88-104">Конструирует плоскость с точки и обычного.</span><span class="sxs-lookup"><span data-stu-id="34e88-104">Constructs a plane from a point and a normal.</span></span>

## <a name="syntax"></a><span data-ttu-id="34e88-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="34e88-105">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneFromPointNormal(
  _Inout_       D3DXPLANE   *pOut,
  _In_    const D3DXVECTOR3 *pPoint,
  _In_    const D3DXVECTOR3 *pNormal
);
```



## <a name="parameters"></a><span data-ttu-id="34e88-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="34e88-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34e88-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="34e88-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="34e88-108">Тип: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="34e88-108">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="34e88-109">Указатель на [**D3DXPLANE**](d3d10-d3dxplane.md) , который является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="34e88-109">Pointer to the [**D3DXPLANE**](d3d10-d3dxplane.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="34e88-110">*ппоинт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="34e88-110">*pPoint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34e88-111">Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="34e88-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="34e88-112">Указатель на [**D3DXVECTOR3**](d3d10-d3dxvector3.md), определяющий точку, используемую для создания плоскости.</span><span class="sxs-lookup"><span data-stu-id="34e88-112">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md), defining the point used to construct the plane.</span></span>

</dd> <dt>

<span data-ttu-id="34e88-113">*пнормал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="34e88-113">*pNormal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34e88-114">Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="34e88-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="34e88-115">Указатель на структуру D3DXVECTOR3, определяющую нормальную, используемую для создания плоскости.</span><span class="sxs-lookup"><span data-stu-id="34e88-115">Pointer to a D3DXVECTOR3 structure, defining the normal used to construct the plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34e88-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="34e88-116">Return value</span></span>

<span data-ttu-id="34e88-117">Тип: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="34e88-117">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="34e88-118">Указатель на структуру D3DXPLANE, созданную из точки и обычного.</span><span class="sxs-lookup"><span data-stu-id="34e88-118">Pointer to the D3DXPLANE structure constructed from the point and the normal.</span></span>

## <a name="remarks"></a><span data-ttu-id="34e88-119">Remarks</span><span class="sxs-lookup"><span data-stu-id="34e88-119">Remarks</span></span>

<span data-ttu-id="34e88-120">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="34e88-120">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="34e88-121">Таким образом, функция D3DXPlaneFromPointNormal может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="34e88-121">In this way, the D3DXPlaneFromPointNormal function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="34e88-122">Требования</span><span class="sxs-lookup"><span data-stu-id="34e88-122">Requirements</span></span>



| <span data-ttu-id="34e88-123">Требование</span><span class="sxs-lookup"><span data-stu-id="34e88-123">Requirement</span></span> | <span data-ttu-id="34e88-124">Значение</span><span class="sxs-lookup"><span data-stu-id="34e88-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="34e88-125">Header</span><span class="sxs-lookup"><span data-stu-id="34e88-125">Header</span></span><br/>  | <dl> <span data-ttu-id="34e88-126"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="34e88-126"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="34e88-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="34e88-127">Library</span></span><br/> | <dl> <span data-ttu-id="34e88-128"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="34e88-128"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="34e88-129">См. также</span><span class="sxs-lookup"><span data-stu-id="34e88-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34e88-130">Математические функции</span><span class="sxs-lookup"><span data-stu-id="34e88-130">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
