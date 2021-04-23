---
description: Возвращает нормализованную версию трехмерного вектора.
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
ms.openlocfilehash: 413b807c53e0b46b115af2aa283e4902a45f5979
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103914783"
---
# <a name="d3dxvec3normalize-function-d3dx10mathh"></a><span data-ttu-id="c5ed9-103">Функция D3DXVec3Normalize (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="c5ed9-103">D3DXVec3Normalize function (D3DX10Math.h)</span></span>

<span data-ttu-id="c5ed9-104">Возвращает нормализованную версию трехмерного вектора.</span><span class="sxs-lookup"><span data-stu-id="c5ed9-104">Returns the normalized version of a 3D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5ed9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c5ed9-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Normalize(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="c5ed9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c5ed9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5ed9-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="c5ed9-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c5ed9-108">Тип: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="c5ed9-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="c5ed9-109">Указатель на [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , который является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="c5ed9-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="c5ed9-110">*ПС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c5ed9-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5ed9-111">Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="c5ed9-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="c5ed9-112">Указатель на исходную структуру D3DXVECTOR3.</span><span class="sxs-lookup"><span data-stu-id="c5ed9-112">Pointer to the source D3DXVECTOR3 structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5ed9-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c5ed9-113">Return value</span></span>

<span data-ttu-id="c5ed9-114">Тип: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="c5ed9-114">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="c5ed9-115">Указатель на структуру D3DXVECTOR3, которая является нормализованной версией указанного вектора.</span><span class="sxs-lookup"><span data-stu-id="c5ed9-115">Pointer to a D3DXVECTOR3 structure that is the normalized version of the specified vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5ed9-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c5ed9-116">Remarks</span></span>

<span data-ttu-id="c5ed9-117">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="c5ed9-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="c5ed9-118">Таким образом, функция D3DXVec3Normalize может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="c5ed9-118">In this way, the D3DXVec3Normalize function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5ed9-119">Требования</span><span class="sxs-lookup"><span data-stu-id="c5ed9-119">Requirements</span></span>



| <span data-ttu-id="c5ed9-120">Требование</span><span class="sxs-lookup"><span data-stu-id="c5ed9-120">Requirement</span></span> | <span data-ttu-id="c5ed9-121">Значение</span><span class="sxs-lookup"><span data-stu-id="c5ed9-121">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c5ed9-122">Header</span><span class="sxs-lookup"><span data-stu-id="c5ed9-122">Header</span></span><br/> | <dl> <span data-ttu-id="c5ed9-123"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5ed9-123"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5ed9-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c5ed9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5ed9-125">Математические функции</span><span class="sxs-lookup"><span data-stu-id="c5ed9-125">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
