---
description: Преобразует двумерный вектор, нормализованный заданной матрицей.
ms.assetid: fc238bb1-155f-4018-9c92-16352726920d
title: Функция D3DXVec2TransformNormal (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2TransformNormal
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c4043a8f5a57f14be3e8506dc257690ef581835d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000378"
---
# <a name="d3dxvec2transformnormal-function-d3dx10mathh"></a><span data-ttu-id="275b2-103">Функция D3DXVec2TransformNormal (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="275b2-103">D3DXVec2TransformNormal function (D3DX10Math.h)</span></span>

<span data-ttu-id="275b2-104">Преобразует двумерный вектор, нормализованный заданной матрицей.</span><span class="sxs-lookup"><span data-stu-id="275b2-104">Transforms the 2D vector normal by the given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="275b2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="275b2-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2TransformNormal(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="275b2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="275b2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="275b2-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="275b2-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="275b2-108">Тип: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="275b2-108">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="275b2-109">Указатель на [**D3DXVECTOR2**](d3d10-d3dxvector2.md) , который является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="275b2-109">Pointer to the [**D3DXVECTOR2**](d3d10-d3dxvector2.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="275b2-110">*ПС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="275b2-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="275b2-111">Тип: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="275b2-111">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="275b2-112">Указатель на исходную структуру D3DXVECTOR2.</span><span class="sxs-lookup"><span data-stu-id="275b2-112">Pointer to the source D3DXVECTOR2 structure.</span></span>

</dd> <dt>

<span data-ttu-id="275b2-113">*PM* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="275b2-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="275b2-114">Тип: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="275b2-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="275b2-115">Указатель на исходную структуру [**D3DXMATRIX**](d3d10-d3dxmatrix.md) .</span><span class="sxs-lookup"><span data-stu-id="275b2-115">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="275b2-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="275b2-116">Return value</span></span>

<span data-ttu-id="275b2-117">Тип: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="275b2-117">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="275b2-118">Указатель на структуру D3DXVECTOR2, которая является преобразованным вектором.</span><span class="sxs-lookup"><span data-stu-id="275b2-118">Pointer to a D3DXVECTOR2 structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="275b2-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="275b2-119">Remarks</span></span>

<span data-ttu-id="275b2-120">Эта функция преобразует вектор (pV->x, pV->y, 0, 0) на матрицу, на которую указывает pM.</span><span class="sxs-lookup"><span data-stu-id="275b2-120">This function transforms the vector (pV->x, pV->y, 0, 0) by the matrix pointed to by pM.</span></span>

<span data-ttu-id="275b2-121">Если необходимо преобразовать обычное значение, то матрица, передаваемая в эту функцию, должна быть преобразована обратно в матрицу, которая будет использоваться для преобразования точки.</span><span class="sxs-lookup"><span data-stu-id="275b2-121">If you want to transform a normal, the matrix you pass to this function should be the transpose of the inverse of the matrix you would use to transform a point.</span></span>

<span data-ttu-id="275b2-122">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="275b2-122">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="275b2-123">Таким образом, функция **D3DXVec2TransformNormal** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="275b2-123">In this way, the **D3DXVec2TransformNormal** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="275b2-124">Требования</span><span class="sxs-lookup"><span data-stu-id="275b2-124">Requirements</span></span>



| <span data-ttu-id="275b2-125">Требование</span><span class="sxs-lookup"><span data-stu-id="275b2-125">Requirement</span></span> | <span data-ttu-id="275b2-126">Значение</span><span class="sxs-lookup"><span data-stu-id="275b2-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="275b2-127">Header</span><span class="sxs-lookup"><span data-stu-id="275b2-127">Header</span></span><br/>  | <dl> <span data-ttu-id="275b2-128"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="275b2-128"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="275b2-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="275b2-129">Library</span></span><br/> | <dl> <span data-ttu-id="275b2-130"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="275b2-130"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="275b2-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="275b2-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="275b2-132">Математические функции</span><span class="sxs-lookup"><span data-stu-id="275b2-132">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
