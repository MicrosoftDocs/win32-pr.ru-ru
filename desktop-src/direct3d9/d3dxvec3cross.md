---
description: Определяет перекрестное произведение двух трехмерных векторов.
ms.assetid: c9623f35-c8fc-4fbe-87b6-0e5bb8ebd5e8
title: Функция D3DXVec3Cross (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Cross
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ba0d8a80690f43d5f8e9f6df55aa3b2e0db23dc2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703778"
---
# <a name="d3dxvec3cross-function"></a><span data-ttu-id="df20e-103">Функция D3DXVec3Cross</span><span class="sxs-lookup"><span data-stu-id="df20e-103">D3DXVec3Cross function</span></span>

<span data-ttu-id="df20e-104">Определяет перекрестное произведение двух трехмерных векторов.</span><span class="sxs-lookup"><span data-stu-id="df20e-104">Determines the cross-product of two 3D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="df20e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="df20e-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Cross(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="df20e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="df20e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df20e-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="df20e-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="df20e-108">Тип: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="df20e-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="df20e-109">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="df20e-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="df20e-110">*pV1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="df20e-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df20e-111">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="df20e-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="df20e-112">Указатель на исходную структуру [**D3DXVECTOR3**](d3dxvector3.md) .</span><span class="sxs-lookup"><span data-stu-id="df20e-112">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="df20e-113">*pV2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="df20e-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df20e-114">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="df20e-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="df20e-115">Указатель на исходную структуру [**D3DXVECTOR3**](d3dxvector3.md) .</span><span class="sxs-lookup"><span data-stu-id="df20e-115">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df20e-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="df20e-116">Return value</span></span>

<span data-ttu-id="df20e-117">Тип: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="df20e-117">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="df20e-118">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , которая является перекрестным произведением двух трехмерных векторов.</span><span class="sxs-lookup"><span data-stu-id="df20e-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the cross product of two 3D vectors.</span></span>

## <a name="remarks"></a><span data-ttu-id="df20e-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="df20e-119">Remarks</span></span>

<span data-ttu-id="df20e-120">Эта функция определяет кросс-Product с помощью следующего кода.</span><span class="sxs-lookup"><span data-stu-id="df20e-120">This function determines the cross-product with the following code.</span></span>


```
D3DXVECTOR3 v;
    
v.x = pV1->y * pV2->z - pV1->z * pV2->y;
v.y = pV1->z * pV2->x - pV1->x * pV2->z;
v.z = pV1->x * pV2->y - pV1->y * pV2->x;
    
*pOut = v;
```



<span data-ttu-id="df20e-121">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="df20e-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="df20e-122">Таким образом, функция **D3DXVec3Cross** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="df20e-122">In this way, the **D3DXVec3Cross** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="df20e-123">Требования</span><span class="sxs-lookup"><span data-stu-id="df20e-123">Requirements</span></span>



| <span data-ttu-id="df20e-124">Требование</span><span class="sxs-lookup"><span data-stu-id="df20e-124">Requirement</span></span> | <span data-ttu-id="df20e-125">Значение</span><span class="sxs-lookup"><span data-stu-id="df20e-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="df20e-126">Header</span><span class="sxs-lookup"><span data-stu-id="df20e-126">Header</span></span><br/>  | <dl> <span data-ttu-id="df20e-127"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="df20e-127"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="df20e-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="df20e-128">Library</span></span><br/> | <dl> <span data-ttu-id="df20e-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="df20e-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="df20e-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="df20e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df20e-131">Математические функции</span><span class="sxs-lookup"><span data-stu-id="df20e-131">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="df20e-132">**D3DXVec3Dot**</span><span class="sxs-lookup"><span data-stu-id="df20e-132">**D3DXVec3Dot**</span></span>](d3dxvec3dot.md)
</dt> </dl>

 

 




