---
description: Проецирует вектор из пространства экрана в объектное пространство.
ms.assetid: c96d732d-0594-42b4-bc54-458a313f153e
title: Функция D3DXVec3Unproject (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Unproject
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 21916392c689bcac794d44ec2c42c3e0b39abb0c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105674729"
---
# <a name="d3dxvec3unproject-function-d3dx10mathh"></a><span data-ttu-id="0be31-103">Функция D3DXVec3Unproject (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="0be31-103">D3DXVec3Unproject function (D3DX10Math.h)</span></span>

<span data-ttu-id="0be31-104">Проецирует вектор из пространства экрана в объектное пространство.</span><span class="sxs-lookup"><span data-stu-id="0be31-104">Projects a vector from screen space into object space.</span></span>

## <a name="syntax"></a><span data-ttu-id="0be31-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0be31-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Unproject(
  _Inout_       D3DXVECTOR3    *pOut,
  _In_    const D3DXVECTOR3    *pV,
  _In_    const D3D10_VIEWPORT *pViewport,
  _In_    const D3DXMATRIX     *pProjection,
  _In_    const D3DXMATRIX     *pView,
  _In_    const D3DXMATRIX     *pWorld
);
```



## <a name="parameters"></a><span data-ttu-id="0be31-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0be31-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0be31-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="0be31-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0be31-108">Тип: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="0be31-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="0be31-109">Указатель на [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , который является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="0be31-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="0be31-110">*ПС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0be31-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0be31-111">Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="0be31-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="0be31-112">Указатель на исходную структуру D3DXVECTOR3.</span><span class="sxs-lookup"><span data-stu-id="0be31-112">Pointer to the source D3DXVECTOR3 structure.</span></span>

</dd> <dt>

<span data-ttu-id="0be31-113">*пвиевпорт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0be31-113">*pViewport* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0be31-114">Тип: **const [**D3D10 \_ окно просмотра**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport) \***</span><span class="sxs-lookup"><span data-stu-id="0be31-114">Type: **const [**D3D10\_VIEWPORT**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport)\***</span></span>

<span data-ttu-id="0be31-115">Указатель на [**\_ окно просмотра D3D10**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport), представляющее окно просмотра.</span><span class="sxs-lookup"><span data-stu-id="0be31-115">Pointer to a [**D3D10\_VIEWPORT**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport), representing the viewport.</span></span>

</dd> <dt>

<span data-ttu-id="0be31-116">*ппрожектион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0be31-116">*pProjection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0be31-117">Тип: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="0be31-117">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="0be31-118">Указатель на структуру [**D3DXMATRIX**](d3d10-d3dxmatrix.md) , представляющую матрицу проекции.</span><span class="sxs-lookup"><span data-stu-id="0be31-118">Pointer to a [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure, representing the projection matrix.</span></span>

</dd> <dt>

<span data-ttu-id="0be31-119">*pView* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0be31-119">*pView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0be31-120">Тип: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="0be31-120">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="0be31-121">Указатель на структуру D3DXMATRIX, представляющую матрицу представления.</span><span class="sxs-lookup"><span data-stu-id="0be31-121">Pointer to a D3DXMATRIX structure, representing the view matrix.</span></span>

</dd> <dt>

<span data-ttu-id="0be31-122">*пворлд* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0be31-122">*pWorld* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0be31-123">Тип: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="0be31-123">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="0be31-124">Указатель на структуру D3DXMATRIX, представляющую матрицу мира.</span><span class="sxs-lookup"><span data-stu-id="0be31-124">Pointer to a D3DXMATRIX structure, representing the world matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0be31-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0be31-125">Return value</span></span>

<span data-ttu-id="0be31-126">Тип: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="0be31-126">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="0be31-127">Указатель на структуру D3DXVECTOR3, которая представляет собой вектор, проецируемый из пространства экрана в объектное пространство.</span><span class="sxs-lookup"><span data-stu-id="0be31-127">Pointer to a D3DXVECTOR3 structure that is the vector projected from screen space to object space.</span></span>

## <a name="remarks"></a><span data-ttu-id="0be31-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0be31-128">Remarks</span></span>

<span data-ttu-id="0be31-129">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="0be31-129">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="0be31-130">Таким образом, функция D3DXVec3Unproject может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="0be31-130">In this way, the D3DXVec3Unproject function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="0be31-131">Требования</span><span class="sxs-lookup"><span data-stu-id="0be31-131">Requirements</span></span>



| <span data-ttu-id="0be31-132">Требование</span><span class="sxs-lookup"><span data-stu-id="0be31-132">Requirement</span></span> | <span data-ttu-id="0be31-133">Значение</span><span class="sxs-lookup"><span data-stu-id="0be31-133">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0be31-134">Header</span><span class="sxs-lookup"><span data-stu-id="0be31-134">Header</span></span><br/> | <dl> <span data-ttu-id="0be31-135"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="0be31-135"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0be31-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0be31-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0be31-137">Математические функции</span><span class="sxs-lookup"><span data-stu-id="0be31-137">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
