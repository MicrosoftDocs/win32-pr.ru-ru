---
description: Проецирует вектор из пространства экрана в объектное пространство.
ms.assetid: 9fd69cae-1d9c-4fae-9e15-8eb9950b4850
title: Функция D3DXVec3Unproject (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Unproject
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2bab9af4a2c88a3e3b3b7f342b6c7c9cc89ceb66
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355623"
---
# <a name="d3dxvec3unproject-function-d3dx9mathh"></a><span data-ttu-id="fd619-103">Функция D3DXVec3Unproject (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="fd619-103">D3DXVec3Unproject function (D3dx9math.h)</span></span>

<span data-ttu-id="fd619-104">Проецирует вектор из пространства экрана в объектное пространство.</span><span class="sxs-lookup"><span data-stu-id="fd619-104">Projects a vector from screen space into object space.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd619-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fd619-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Unproject(
  _Inout_       D3DXVECTOR3  *pOut,
  _In_    const D3DXVECTOR3  *pV,
  _In_    const D3DVIEWPORT9 *pViewport,
  _In_    const D3DXMATRIX   *pProjection,
  _In_    const D3DXMATRIX   *pView,
  _In_    const D3DXMATRIX   *pWorld
);
```



## <a name="parameters"></a><span data-ttu-id="fd619-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fd619-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd619-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="fd619-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fd619-108">Тип: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="fd619-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="fd619-109">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="fd619-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="fd619-110">*ПС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fd619-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd619-111">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="fd619-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="fd619-112">Указатель на исходную структуру [**D3DXVECTOR3**](d3dxvector3.md) .</span><span class="sxs-lookup"><span data-stu-id="fd619-112">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="fd619-113">*пвиевпорт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fd619-113">*pViewport* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd619-114">Тип: **const [**D3DVIEWPORT9**](d3dviewport9.md) \***</span><span class="sxs-lookup"><span data-stu-id="fd619-114">Type: **const [**D3DVIEWPORT9**](d3dviewport9.md)\***</span></span>

<span data-ttu-id="fd619-115">Указатель на структуру [**D3DVIEWPORT9**](d3dviewport9.md) , представляющую окно просмотра.</span><span class="sxs-lookup"><span data-stu-id="fd619-115">Pointer to a [**D3DVIEWPORT9**](d3dviewport9.md) structure, representing the viewport.</span></span>

</dd> <dt>

<span data-ttu-id="fd619-116">*ппрожектион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fd619-116">*pProjection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd619-117">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="fd619-117">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="fd619-118">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , представляющую матрицу проекции.</span><span class="sxs-lookup"><span data-stu-id="fd619-118">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the projection matrix.</span></span>

</dd> <dt>

<span data-ttu-id="fd619-119">*pView* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fd619-119">*pView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd619-120">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="fd619-120">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="fd619-121">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , представляющую матрицу представления.</span><span class="sxs-lookup"><span data-stu-id="fd619-121">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the view matrix.</span></span>

</dd> <dt>

<span data-ttu-id="fd619-122">*пворлд* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fd619-122">*pWorld* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd619-123">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="fd619-123">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="fd619-124">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , представляющую матрицу мира.</span><span class="sxs-lookup"><span data-stu-id="fd619-124">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the world matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd619-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fd619-125">Return value</span></span>

<span data-ttu-id="fd619-126">Тип: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="fd619-126">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="fd619-127">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , которая представляет собой вектор, проецируемый из пространства экрана в объектное пространство.</span><span class="sxs-lookup"><span data-stu-id="fd619-127">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the vector projected from screen space to object space.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd619-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fd619-128">Remarks</span></span>

<span data-ttu-id="fd619-129">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="fd619-129">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="fd619-130">Таким образом, функция **D3DXVec3Unproject** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="fd619-130">In this way, the **D3DXVec3Unproject** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd619-131">Требования</span><span class="sxs-lookup"><span data-stu-id="fd619-131">Requirements</span></span>



| <span data-ttu-id="fd619-132">Требование</span><span class="sxs-lookup"><span data-stu-id="fd619-132">Requirement</span></span> | <span data-ttu-id="fd619-133">Значение</span><span class="sxs-lookup"><span data-stu-id="fd619-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd619-134">Header</span><span class="sxs-lookup"><span data-stu-id="fd619-134">Header</span></span><br/>  | <dl> <span data-ttu-id="fd619-135"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd619-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="fd619-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="fd619-136">Library</span></span><br/> | <dl> <span data-ttu-id="fd619-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fd619-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fd619-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fd619-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd619-139">Математические функции</span><span class="sxs-lookup"><span data-stu-id="fd619-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="fd619-140">**D3DXVec3Project**</span><span class="sxs-lookup"><span data-stu-id="fd619-140">**D3DXVec3Project**</span></span>](d3dxvec3project.md)
</dt> </dl>

 

 




