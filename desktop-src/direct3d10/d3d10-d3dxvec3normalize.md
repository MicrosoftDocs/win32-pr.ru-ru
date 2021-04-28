---
description: Функция D3DXVec3Normalize (D3DX10Math. h) — Возвращает нормализованную версию трехмерного вектора.
ms.assetid: 420321a2-0c3b-419c-9620-acf184e7b4f0
title: Функция D3DXVec3Normalize (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Normalize
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 3f1317b1b8887b9ff306fcaed2cb6da2d077010f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108182"
---
# <a name="d3dxvec3normalize-function-d3dx10mathh"></a><span data-ttu-id="6d217-103">Функция D3DXVec3Normalize (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="6d217-103">D3DXVec3Normalize function (D3DX10Math.h)</span></span>

<span data-ttu-id="6d217-104">Возвращает нормализованную версию трехмерного вектора.</span><span class="sxs-lookup"><span data-stu-id="6d217-104">Returns the normalized version of a 3D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d217-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6d217-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Normalize(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="6d217-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6d217-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d217-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="6d217-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6d217-108">Тип: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="6d217-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="6d217-109">Указатель на [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , который является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="6d217-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="6d217-110">*ПС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6d217-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d217-111">Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="6d217-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="6d217-112">Указатель на исходную структуру D3DXVECTOR3.</span><span class="sxs-lookup"><span data-stu-id="6d217-112">Pointer to the source D3DXVECTOR3 structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d217-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6d217-113">Return value</span></span>

<span data-ttu-id="6d217-114">Тип: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="6d217-114">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="6d217-115">Указатель на структуру D3DXVECTOR3, которая является нормализованной версией указанного вектора.</span><span class="sxs-lookup"><span data-stu-id="6d217-115">Pointer to a D3DXVECTOR3 structure that is the normalized version of the specified vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d217-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="6d217-116">Remarks</span></span>

<span data-ttu-id="6d217-117">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="6d217-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="6d217-118">Таким образом, функция D3DXVec3Normalize может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="6d217-118">In this way, the D3DXVec3Normalize function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d217-119">Требования</span><span class="sxs-lookup"><span data-stu-id="6d217-119">Requirements</span></span>



| <span data-ttu-id="6d217-120">Требование</span><span class="sxs-lookup"><span data-stu-id="6d217-120">Requirement</span></span> | <span data-ttu-id="6d217-121">Значение</span><span class="sxs-lookup"><span data-stu-id="6d217-121">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6d217-122">Header</span><span class="sxs-lookup"><span data-stu-id="6d217-122">Header</span></span><br/> | <dl> <span data-ttu-id="6d217-123"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d217-123"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d217-124">См. также</span><span class="sxs-lookup"><span data-stu-id="6d217-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d217-125">Математические функции</span><span class="sxs-lookup"><span data-stu-id="6d217-125">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
