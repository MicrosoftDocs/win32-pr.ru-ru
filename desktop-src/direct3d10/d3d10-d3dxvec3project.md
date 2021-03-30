---
description: Проецирует трехмерный вектор из объектного пространства в пространство экрана.
ms.assetid: 6fc59788-c3f7-4f47-a345-9108105e820e
title: Функция D3DXVec3Project (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Project
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: c8d86949f754afb7639a0c28ff6d8b14c0e40ff0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354973"
---
# <a name="d3dxvec3project-function-d3dx10mathh"></a><span data-ttu-id="43499-103">Функция D3DXVec3Project (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="43499-103">D3DXVec3Project function (D3DX10Math.h)</span></span>

<span data-ttu-id="43499-104">Проецирует трехмерный вектор из объектного пространства в пространство экрана.</span><span class="sxs-lookup"><span data-stu-id="43499-104">Projects a 3D vector from object space into screen space.</span></span>

## <a name="syntax"></a><span data-ttu-id="43499-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="43499-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Project(
  _Inout_       D3DXVECTOR3    *pOut,
  _In_    const D3DXVECTOR3    *pV,
  _In_    const D3D10_VIEWPORT *pViewport,
  _In_    const D3DXMATRIX     *pProjection,
  _In_    const D3DXMATRIX     *pView,
  _In_    const D3DXMATRIX     *pWorld
);
```



## <a name="parameters"></a><span data-ttu-id="43499-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="43499-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43499-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="43499-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="43499-108">Тип: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="43499-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="43499-109">Указатель на [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , который является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="43499-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="43499-110">*ПС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="43499-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43499-111">Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="43499-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="43499-112">Указатель на исходную структуру D3DXVECTOR3.</span><span class="sxs-lookup"><span data-stu-id="43499-112">Pointer to the source D3DXVECTOR3 structure.</span></span>

</dd> <dt>

<span data-ttu-id="43499-113">*пвиевпорт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="43499-113">*pViewport* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43499-114">Тип: **const [**D3D10 \_ окно просмотра**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport) \***</span><span class="sxs-lookup"><span data-stu-id="43499-114">Type: **const [**D3D10\_VIEWPORT**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport)\***</span></span>

<span data-ttu-id="43499-115">Указатель на [**\_ окно просмотра D3D10**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport), представляющее окно просмотра.</span><span class="sxs-lookup"><span data-stu-id="43499-115">Pointer to a [**D3D10\_VIEWPORT**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport), representing the viewport.</span></span>

</dd> <dt>

<span data-ttu-id="43499-116">*ппрожектион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="43499-116">*pProjection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43499-117">Тип: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="43499-117">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="43499-118">Указатель на структуру [**D3DXMATRIX**](d3d10-d3dxmatrix.md) , представляющую матрицу проекции.</span><span class="sxs-lookup"><span data-stu-id="43499-118">Pointer to a [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure, representing the projection matrix.</span></span>

</dd> <dt>

<span data-ttu-id="43499-119">*pView* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="43499-119">*pView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43499-120">Тип: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="43499-120">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="43499-121">Указатель на структуру D3DXMATRIX, представляющую матрицу представления.</span><span class="sxs-lookup"><span data-stu-id="43499-121">Pointer to a D3DXMATRIX structure, representing the view matrix.</span></span>

</dd> <dt>

<span data-ttu-id="43499-122">*пворлд* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="43499-122">*pWorld* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43499-123">Тип: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="43499-123">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="43499-124">Указатель на структуру D3DXMATRIX, представляющую матрицу мира.</span><span class="sxs-lookup"><span data-stu-id="43499-124">Pointer to a D3DXMATRIX structure, representing the world matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43499-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="43499-125">Return value</span></span>

<span data-ttu-id="43499-126">Тип: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="43499-126">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="43499-127">Указатель на структуру D3DXVECTOR3, которая является вектором, проецируемым из пространства объекта в пространство экрана.</span><span class="sxs-lookup"><span data-stu-id="43499-127">Pointer to a D3DXVECTOR3 structure that is the vector projected from object space to screen space.</span></span>

## <a name="remarks"></a><span data-ttu-id="43499-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="43499-128">Remarks</span></span>

<span data-ttu-id="43499-129">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="43499-129">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="43499-130">Таким образом, функция D3DXVec3Project может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="43499-130">In this way, the D3DXVec3Project function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="43499-131">Требования</span><span class="sxs-lookup"><span data-stu-id="43499-131">Requirements</span></span>



| <span data-ttu-id="43499-132">Требование</span><span class="sxs-lookup"><span data-stu-id="43499-132">Requirement</span></span> | <span data-ttu-id="43499-133">Значение</span><span class="sxs-lookup"><span data-stu-id="43499-133">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="43499-134">Header</span><span class="sxs-lookup"><span data-stu-id="43499-134">Header</span></span><br/> | <dl> <span data-ttu-id="43499-135"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="43499-135"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43499-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="43499-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43499-137">Математические функции</span><span class="sxs-lookup"><span data-stu-id="43499-137">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
