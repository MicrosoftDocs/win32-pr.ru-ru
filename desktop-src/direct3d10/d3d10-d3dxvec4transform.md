---
description: Преобразует вектор 4D по заданной матрице.
ms.assetid: ccbf33bc-1f94-4cf8-b048-220d54516e00
title: Функция D3DXVec4Transform (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Transform
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 56fc6b3041d799cda3e98d459b2523d4b171df10
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103914712"
---
# <a name="d3dxvec4transform-function-d3dx10mathh"></a><span data-ttu-id="2ddad-103">Функция D3DXVec4Transform (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="2ddad-103">D3DXVec4Transform function (D3DX10Math.h)</span></span>

<span data-ttu-id="2ddad-104">Преобразует вектор 4D по заданной матрице.</span><span class="sxs-lookup"><span data-stu-id="2ddad-104">Transforms a 4D vector by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ddad-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2ddad-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Transform(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="2ddad-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2ddad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ddad-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="2ddad-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2ddad-108">Тип: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="2ddad-108">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="2ddad-109">Указатель на [**D3DXVECTOR4**](d3d10-d3dxvector4.md) , который является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="2ddad-109">Pointer to the [**D3DXVECTOR4**](d3d10-d3dxvector4.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="2ddad-110">*ПС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2ddad-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ddad-111">Тип: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="2ddad-111">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="2ddad-112">Указатель на исходную структуру D3DXVECTOR4.</span><span class="sxs-lookup"><span data-stu-id="2ddad-112">Pointer to the source D3DXVECTOR4 structure.</span></span>

</dd> <dt>

<span data-ttu-id="2ddad-113">*PM* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2ddad-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ddad-114">Тип: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="2ddad-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="2ddad-115">Указатель на исходную структуру [**D3DXMATRIX**](d3d10-d3dxmatrix.md) .</span><span class="sxs-lookup"><span data-stu-id="2ddad-115">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ddad-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2ddad-116">Return value</span></span>

<span data-ttu-id="2ddad-117">Тип: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="2ddad-117">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="2ddad-118">Указатель на структуру D3DXVECTOR4, которая является преобразованным вектором 4D.</span><span class="sxs-lookup"><span data-stu-id="2ddad-118">Pointer to a D3DXVECTOR4 structure that is the transformed 4D vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ddad-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2ddad-119">Remarks</span></span>

<span data-ttu-id="2ddad-120">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="2ddad-120">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="2ddad-121">Таким образом, функция D3DXVec4Transform может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="2ddad-121">In this way, the D3DXVec4Transform function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ddad-122">Требования</span><span class="sxs-lookup"><span data-stu-id="2ddad-122">Requirements</span></span>



| <span data-ttu-id="2ddad-123">Требование</span><span class="sxs-lookup"><span data-stu-id="2ddad-123">Requirement</span></span> | <span data-ttu-id="2ddad-124">Значение</span><span class="sxs-lookup"><span data-stu-id="2ddad-124">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2ddad-125">Header</span><span class="sxs-lookup"><span data-stu-id="2ddad-125">Header</span></span><br/> | <dl> <span data-ttu-id="2ddad-126"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ddad-126"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ddad-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2ddad-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ddad-128">Математические функции</span><span class="sxs-lookup"><span data-stu-id="2ddad-128">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
