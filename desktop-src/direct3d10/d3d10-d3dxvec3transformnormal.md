---
description: Преобразует трехмерный вектор в нормальный по заданной матрице.
ms.assetid: 8068b80f-6222-4f23-8b1c-2ff5592fa898
title: Функция D3DXVec3TransformNormal (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformNormal
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 602f366d3d7ccbcd37804226323d5584eed034f9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355300"
---
# <a name="d3dxvec3transformnormal-function-d3dx10mathh"></a><span data-ttu-id="bebbe-103">Функция D3DXVec3TransformNormal (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="bebbe-103">D3DXVec3TransformNormal function (D3DX10Math.h)</span></span>

<span data-ttu-id="bebbe-104">Преобразует трехмерный вектор в нормальный по заданной матрице.</span><span class="sxs-lookup"><span data-stu-id="bebbe-104">Transforms the 3D vector normal by the given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="bebbe-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bebbe-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3TransformNormal(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="bebbe-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bebbe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bebbe-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="bebbe-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bebbe-108">Тип: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="bebbe-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="bebbe-109">Указатель на [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , который является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="bebbe-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="bebbe-110">*ПС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bebbe-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bebbe-111">Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="bebbe-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="bebbe-112">Указатель на исходную структуру D3DXVECTOR3.</span><span class="sxs-lookup"><span data-stu-id="bebbe-112">Pointer to the source D3DXVECTOR3 structure.</span></span>

</dd> <dt>

<span data-ttu-id="bebbe-113">*PM* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bebbe-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bebbe-114">Тип: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="bebbe-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="bebbe-115">Указатель на исходную структуру [**D3DXMATRIX**](d3d10-d3dxmatrix.md) .</span><span class="sxs-lookup"><span data-stu-id="bebbe-115">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bebbe-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bebbe-116">Return value</span></span>

<span data-ttu-id="bebbe-117">Тип: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="bebbe-117">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="bebbe-118">Указатель на структуру D3DXVECTOR3, которая является преобразованным вектором.</span><span class="sxs-lookup"><span data-stu-id="bebbe-118">Pointer to a D3DXVECTOR3 structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="bebbe-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bebbe-119">Remarks</span></span>

<span data-ttu-id="bebbe-120">Эта функция преобразует вектор (ПС->x, pV->y, pV->z, 0) матрице, на которую указывает pM.</span><span class="sxs-lookup"><span data-stu-id="bebbe-120">This function transforms the vector (pV->x, pV->y, pV->z, 0) by the matrix pointed to by pM.</span></span>

<span data-ttu-id="bebbe-121">Если необходимо преобразовать обычное значение, то матрица, передаваемая в эту функцию, должна быть преобразована обратно в матрицу, которая будет использоваться для преобразования точки.</span><span class="sxs-lookup"><span data-stu-id="bebbe-121">If you want to transform a normal, the matrix you pass to this function should be the transpose of the inverse of the matrix you would use to transform a point.</span></span>

<span data-ttu-id="bebbe-122">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="bebbe-122">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="bebbe-123">Таким образом, функция **D3DXVec3TransformNormal** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="bebbe-123">In this way, the **D3DXVec3TransformNormal** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="bebbe-124">Требования</span><span class="sxs-lookup"><span data-stu-id="bebbe-124">Requirements</span></span>



| <span data-ttu-id="bebbe-125">Требование</span><span class="sxs-lookup"><span data-stu-id="bebbe-125">Requirement</span></span> | <span data-ttu-id="bebbe-126">Значение</span><span class="sxs-lookup"><span data-stu-id="bebbe-126">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bebbe-127">Header</span><span class="sxs-lookup"><span data-stu-id="bebbe-127">Header</span></span><br/> | <dl> <span data-ttu-id="bebbe-128"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="bebbe-128"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bebbe-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bebbe-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bebbe-130">Математические функции</span><span class="sxs-lookup"><span data-stu-id="bebbe-130">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
