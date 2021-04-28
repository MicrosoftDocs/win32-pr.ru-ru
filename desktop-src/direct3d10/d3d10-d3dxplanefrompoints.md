---
description: Функция D3DXPlaneFromPoints (D3DX10Math. h) — конструирует плоскость из трех точек.
ms.assetid: 0e77af1b-cedf-482c-8398-10becb398a2c
title: Функция D3DXPlaneFromPoints (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a3af01df7d1ce66029994226d040544b733a75df
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103322"
---
# <a name="d3dxplanefrompoints-function-d3dx10mathh"></a><span data-ttu-id="cbcf4-103">Функция D3DXPlaneFromPoints (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="cbcf4-103">D3DXPlaneFromPoints function (D3DX10Math.h)</span></span>

<span data-ttu-id="cbcf4-104">Конструирует плоскость из трех точек.</span><span class="sxs-lookup"><span data-stu-id="cbcf4-104">Constructs a plane from three points.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbcf4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cbcf4-105">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneFromPoints(
  _Inout_       D3DXPLANE   *pOut,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2,
  _In_    const D3DXVECTOR3 *pV3
);
```



## <a name="parameters"></a><span data-ttu-id="cbcf4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cbcf4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cbcf4-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="cbcf4-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="cbcf4-108">Тип: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="cbcf4-108">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="cbcf4-109">Указатель на [**D3DXPLANE**](d3d10-d3dxplane.md) , который является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="cbcf4-109">Pointer to the [**D3DXPLANE**](d3d10-d3dxplane.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="cbcf4-110">*pV1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cbcf4-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbcf4-111">Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="cbcf4-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="cbcf4-112">Указатель на [**D3DXVECTOR3**](d3d10-d3dxvector3.md), определяющий одну из точек, используемых для создания плоскости.</span><span class="sxs-lookup"><span data-stu-id="cbcf4-112">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md), defining one of the points used to construct the plane.</span></span>

</dd> <dt>

<span data-ttu-id="cbcf4-113">*pV2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cbcf4-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbcf4-114">Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="cbcf4-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="cbcf4-115">Указатель на структуру D3DXVECTOR3, определяющую одну из точек, используемых для создания плоскости.</span><span class="sxs-lookup"><span data-stu-id="cbcf4-115">Pointer to a D3DXVECTOR3 structure, defining one of the points used to construct the plane.</span></span>

</dd> <dt>

<span data-ttu-id="cbcf4-116">*pV3* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cbcf4-116">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbcf4-117">Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="cbcf4-117">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="cbcf4-118">Указатель на структуру D3DXVECTOR3, определяющую одну из точек, используемых для создания плоскости.</span><span class="sxs-lookup"><span data-stu-id="cbcf4-118">Pointer to a D3DXVECTOR3 structure, defining one of the points used to construct the plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cbcf4-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cbcf4-119">Return value</span></span>

<span data-ttu-id="cbcf4-120">Тип: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="cbcf4-120">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="cbcf4-121">Указатель на структуру D3DXPLANE, созданную из заданных точек.</span><span class="sxs-lookup"><span data-stu-id="cbcf4-121">Pointer to the D3DXPLANE structure constructed from the given points.</span></span>

## <a name="remarks"></a><span data-ttu-id="cbcf4-122">Remarks</span><span class="sxs-lookup"><span data-stu-id="cbcf4-122">Remarks</span></span>

<span data-ttu-id="cbcf4-123">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="cbcf4-123">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="cbcf4-124">Таким образом, функция D3DXPlaneFromPoints может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="cbcf4-124">In this way, the D3DXPlaneFromPoints function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="cbcf4-125">Требования</span><span class="sxs-lookup"><span data-stu-id="cbcf4-125">Requirements</span></span>



| <span data-ttu-id="cbcf4-126">Требование</span><span class="sxs-lookup"><span data-stu-id="cbcf4-126">Requirement</span></span> | <span data-ttu-id="cbcf4-127">Значение</span><span class="sxs-lookup"><span data-stu-id="cbcf4-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cbcf4-128">Header</span><span class="sxs-lookup"><span data-stu-id="cbcf4-128">Header</span></span><br/>  | <dl> <span data-ttu-id="cbcf4-129"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="cbcf4-129"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="cbcf4-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cbcf4-130">Library</span></span><br/> | <dl> <span data-ttu-id="cbcf4-131"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cbcf4-131"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="cbcf4-132">См. также</span><span class="sxs-lookup"><span data-stu-id="cbcf4-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbcf4-133">Математические функции</span><span class="sxs-lookup"><span data-stu-id="cbcf4-133">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
