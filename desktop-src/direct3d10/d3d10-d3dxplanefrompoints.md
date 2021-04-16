---
description: Конструирует плоскость из трех точек.
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
ms.openlocfilehash: eed4426492f05b2bfe3c762915edb8fdc21dc789
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105720953"
---
# <a name="d3dxplanefrompoints-function-d3dx10mathh"></a><span data-ttu-id="b8164-103">Функция D3DXPlaneFromPoints (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="b8164-103">D3DXPlaneFromPoints function (D3DX10Math.h)</span></span>

<span data-ttu-id="b8164-104">Конструирует плоскость из трех точек.</span><span class="sxs-lookup"><span data-stu-id="b8164-104">Constructs a plane from three points.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8164-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b8164-105">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneFromPoints(
  _Inout_       D3DXPLANE   *pOut,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2,
  _In_    const D3DXVECTOR3 *pV3
);
```



## <a name="parameters"></a><span data-ttu-id="b8164-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b8164-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8164-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="b8164-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b8164-108">Тип: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="b8164-108">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="b8164-109">Указатель на [**D3DXPLANE**](d3d10-d3dxplane.md) , который является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="b8164-109">Pointer to the [**D3DXPLANE**](d3d10-d3dxplane.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="b8164-110">*pV1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b8164-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8164-111">Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="b8164-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="b8164-112">Указатель на [**D3DXVECTOR3**](d3d10-d3dxvector3.md), определяющий одну из точек, используемых для создания плоскости.</span><span class="sxs-lookup"><span data-stu-id="b8164-112">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md), defining one of the points used to construct the plane.</span></span>

</dd> <dt>

<span data-ttu-id="b8164-113">*pV2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b8164-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8164-114">Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="b8164-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="b8164-115">Указатель на структуру D3DXVECTOR3, определяющую одну из точек, используемых для создания плоскости.</span><span class="sxs-lookup"><span data-stu-id="b8164-115">Pointer to a D3DXVECTOR3 structure, defining one of the points used to construct the plane.</span></span>

</dd> <dt>

<span data-ttu-id="b8164-116">*pV3* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b8164-116">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8164-117">Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="b8164-117">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="b8164-118">Указатель на структуру D3DXVECTOR3, определяющую одну из точек, используемых для создания плоскости.</span><span class="sxs-lookup"><span data-stu-id="b8164-118">Pointer to a D3DXVECTOR3 structure, defining one of the points used to construct the plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8164-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b8164-119">Return value</span></span>

<span data-ttu-id="b8164-120">Тип: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="b8164-120">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="b8164-121">Указатель на структуру D3DXPLANE, созданную из заданных точек.</span><span class="sxs-lookup"><span data-stu-id="b8164-121">Pointer to the D3DXPLANE structure constructed from the given points.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8164-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b8164-122">Remarks</span></span>

<span data-ttu-id="b8164-123">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="b8164-123">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="b8164-124">Таким образом, функция D3DXPlaneFromPoints может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="b8164-124">In this way, the D3DXPlaneFromPoints function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8164-125">Требования</span><span class="sxs-lookup"><span data-stu-id="b8164-125">Requirements</span></span>



| <span data-ttu-id="b8164-126">Требование</span><span class="sxs-lookup"><span data-stu-id="b8164-126">Requirement</span></span> | <span data-ttu-id="b8164-127">Значение</span><span class="sxs-lookup"><span data-stu-id="b8164-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b8164-128">Header</span><span class="sxs-lookup"><span data-stu-id="b8164-128">Header</span></span><br/>  | <dl> <span data-ttu-id="b8164-129"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8164-129"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="b8164-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b8164-130">Library</span></span><br/> | <dl> <span data-ttu-id="b8164-131"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b8164-131"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b8164-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b8164-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8164-133">Математические функции</span><span class="sxs-lookup"><span data-stu-id="b8164-133">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
