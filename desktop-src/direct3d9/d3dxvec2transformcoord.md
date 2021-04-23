---
description: Преобразует двумерный вектор по заданной матрице, проецирование результата обратно в w = 1.
ms.assetid: 0c0efdf8-77df-4f4a-86ce-89e11555f4dc
title: Функция D3DXVec2TransformCoord (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2TransformCoord
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7bc047075cd2f9f6aba6903f85ea6960e78e0ba1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105674717"
---
# <a name="d3dxvec2transformcoord-function-d3dx9mathh"></a><span data-ttu-id="8f9aa-103">Функция D3DXVec2TransformCoord (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="8f9aa-103">D3DXVec2TransformCoord function (D3dx9math.h)</span></span>

<span data-ttu-id="8f9aa-104">Преобразует двумерный вектор по заданной матрице, проецирование результата обратно в w = 1.</span><span class="sxs-lookup"><span data-stu-id="8f9aa-104">Transforms a 2D vector by a given matrix, projecting the result back into w = 1.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f9aa-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8f9aa-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2TransformCoord(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="8f9aa-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8f9aa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f9aa-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="8f9aa-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8f9aa-108">Тип: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="8f9aa-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="8f9aa-109">Указатель на структуру [**D3DXVECTOR2**](d3dxvector2.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="8f9aa-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="8f9aa-110">*ПС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8f9aa-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f9aa-111">Тип: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="8f9aa-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="8f9aa-112">Указатель на исходную структуру [**D3DXVECTOR2**](d3dxvector2.md) .</span><span class="sxs-lookup"><span data-stu-id="8f9aa-112">Pointer to the source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="8f9aa-113">*PM* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8f9aa-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f9aa-114">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="8f9aa-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="8f9aa-115">Указатель на исходную структуру [**D3DXMATRIX**](d3dxmatrix.md) .</span><span class="sxs-lookup"><span data-stu-id="8f9aa-115">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f9aa-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8f9aa-116">Return value</span></span>

<span data-ttu-id="8f9aa-117">Тип: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="8f9aa-117">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="8f9aa-118">Указатель на структуру [**D3DXVECTOR2**](d3dxvector2.md) , которая является преобразованным вектором.</span><span class="sxs-lookup"><span data-stu-id="8f9aa-118">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f9aa-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8f9aa-119">Remarks</span></span>

<span data-ttu-id="8f9aa-120">Эта функция преобразует вектор, *НЗ* (x, y, 0, 1), по матрице *, в* проекцию результата обратно в w = 1.</span><span class="sxs-lookup"><span data-stu-id="8f9aa-120">This function transforms the vector, *pV* (x, y, 0, 1), by the matrix, *pM*, projecting the result back into w=1.</span></span>

<span data-ttu-id="8f9aa-121">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="8f9aa-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="8f9aa-122">Таким образом, функция **D3DXVec2TransformCoord** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="8f9aa-122">In this way, the **D3DXVec2TransformCoord** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f9aa-123">Требования</span><span class="sxs-lookup"><span data-stu-id="8f9aa-123">Requirements</span></span>



| <span data-ttu-id="8f9aa-124">Требование</span><span class="sxs-lookup"><span data-stu-id="8f9aa-124">Requirement</span></span> | <span data-ttu-id="8f9aa-125">Значение</span><span class="sxs-lookup"><span data-stu-id="8f9aa-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8f9aa-126">Header</span><span class="sxs-lookup"><span data-stu-id="8f9aa-126">Header</span></span><br/>  | <dl> <span data-ttu-id="8f9aa-127"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f9aa-127"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="8f9aa-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8f9aa-128">Library</span></span><br/> | <dl> <span data-ttu-id="8f9aa-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8f9aa-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8f9aa-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8f9aa-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f9aa-131">Математические функции</span><span class="sxs-lookup"><span data-stu-id="8f9aa-131">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="8f9aa-132">**D3DXVec2Transform**</span><span class="sxs-lookup"><span data-stu-id="8f9aa-132">**D3DXVec2Transform**</span></span>](d3dxvec2transform.md)
</dt> <dt>

[<span data-ttu-id="8f9aa-133">**D3DXVec2TransformNormal**</span><span class="sxs-lookup"><span data-stu-id="8f9aa-133">**D3DXVec2TransformNormal**</span></span>](d3dxvec2transformnormal.md)
</dt> </dl>

 

 




