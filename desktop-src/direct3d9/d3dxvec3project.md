---
description: Функция D3DXVec3Project (D3dx9math. h) — проецирует трехмерный вектор из объектного пространства в пространство экрана.
ms.assetid: b012771d-052f-4bf9-b39c-387d8a63fa59
title: Функция D3DXVec3Project (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Project
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a5a9abcb54c883d74bde831570b9df0b40fedfae
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115652"
---
# <a name="d3dxvec3project-function-d3dx9mathh"></a><span data-ttu-id="bcda8-103">Функция D3DXVec3Project (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="bcda8-103">D3DXVec3Project function (D3dx9math.h)</span></span>

<span data-ttu-id="bcda8-104">Проецирует трехмерный вектор из объектного пространства в пространство экрана.</span><span class="sxs-lookup"><span data-stu-id="bcda8-104">Projects a 3D vector from object space into screen space.</span></span>

## <a name="syntax"></a><span data-ttu-id="bcda8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bcda8-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Project(
  _Inout_       D3DXVECTOR3  *pOut,
  _In_    const D3DXVECTOR3  *pV,
  _In_    const D3DVIEWPORT9 *pViewport,
  _In_    const D3DXMATRIX   *pProjection,
  _In_    const D3DXMATRIX   *pView,
  _In_    const D3DXMATRIX   *pWorld
);
```



## <a name="parameters"></a><span data-ttu-id="bcda8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bcda8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bcda8-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="bcda8-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bcda8-108">Тип: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="bcda8-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="bcda8-109">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="bcda8-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="bcda8-110">*ПС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bcda8-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bcda8-111">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="bcda8-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="bcda8-112">Указатель на исходную структуру [**D3DXVECTOR3**](d3dxvector3.md) .</span><span class="sxs-lookup"><span data-stu-id="bcda8-112">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="bcda8-113">*пвиевпорт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bcda8-113">*pViewport* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bcda8-114">Тип: **const [**D3DVIEWPORT9**](d3dviewport9.md) \***</span><span class="sxs-lookup"><span data-stu-id="bcda8-114">Type: **const [**D3DVIEWPORT9**](d3dviewport9.md)\***</span></span>

<span data-ttu-id="bcda8-115">Указатель на структуру [**D3DVIEWPORT9**](d3dviewport9.md) , представляющую окно просмотра.</span><span class="sxs-lookup"><span data-stu-id="bcda8-115">Pointer to a [**D3DVIEWPORT9**](d3dviewport9.md) structure, representing the viewport.</span></span>

</dd> <dt>

<span data-ttu-id="bcda8-116">*ппрожектион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bcda8-116">*pProjection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bcda8-117">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="bcda8-117">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="bcda8-118">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , представляющую матрицу проекции.</span><span class="sxs-lookup"><span data-stu-id="bcda8-118">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the projection matrix.</span></span>

</dd> <dt>

<span data-ttu-id="bcda8-119">*pView* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bcda8-119">*pView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bcda8-120">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="bcda8-120">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="bcda8-121">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , представляющую матрицу представления.</span><span class="sxs-lookup"><span data-stu-id="bcda8-121">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the view matrix.</span></span>

</dd> <dt>

<span data-ttu-id="bcda8-122">*пворлд* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bcda8-122">*pWorld* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bcda8-123">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="bcda8-123">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="bcda8-124">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , представляющую матрицу мира.</span><span class="sxs-lookup"><span data-stu-id="bcda8-124">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the world matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bcda8-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bcda8-125">Return value</span></span>

<span data-ttu-id="bcda8-126">Тип: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="bcda8-126">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="bcda8-127">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , которая является вектором, проецируемым из пространства объекта в пространство экрана.</span><span class="sxs-lookup"><span data-stu-id="bcda8-127">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the vector projected from object space to screen space.</span></span>

## <a name="remarks"></a><span data-ttu-id="bcda8-128">Remarks</span><span class="sxs-lookup"><span data-stu-id="bcda8-128">Remarks</span></span>

<span data-ttu-id="bcda8-129">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="bcda8-129">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="bcda8-130">Таким образом, функция **D3DXVec3Project** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="bcda8-130">In this way, the **D3DXVec3Project** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="bcda8-131">Требования</span><span class="sxs-lookup"><span data-stu-id="bcda8-131">Requirements</span></span>



| <span data-ttu-id="bcda8-132">Требование</span><span class="sxs-lookup"><span data-stu-id="bcda8-132">Requirement</span></span> | <span data-ttu-id="bcda8-133">Значение</span><span class="sxs-lookup"><span data-stu-id="bcda8-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bcda8-134">Header</span><span class="sxs-lookup"><span data-stu-id="bcda8-134">Header</span></span><br/>  | <dl> <span data-ttu-id="bcda8-135"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="bcda8-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="bcda8-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="bcda8-136">Library</span></span><br/> | <dl> <span data-ttu-id="bcda8-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bcda8-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bcda8-138">См. также</span><span class="sxs-lookup"><span data-stu-id="bcda8-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcda8-139">Математические функции</span><span class="sxs-lookup"><span data-stu-id="bcda8-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="bcda8-140">**D3DXVec3Unproject**</span><span class="sxs-lookup"><span data-stu-id="bcda8-140">**D3DXVec3Unproject**</span></span>](d3dxvec3unproject.md)
</dt> </dl>

 

 




