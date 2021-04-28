---
description: Функция D3DXVec4Normalize (D3dx9math. h) — Возвращает нормализованную версию вектора 4D.
ms.assetid: e12d5dc7-b26f-41dd-b89d-1df9ba23077a
title: Функция D3DXVec4Normalize (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Normalize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 78984c393d7caf259b4c310a31e01ed8fcbd4d47
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097662"
---
# <a name="d3dxvec4normalize-function-d3dx9mathh"></a><span data-ttu-id="f8888-103">Функция D3DXVec4Normalize (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="f8888-103">D3DXVec4Normalize function (D3dx9math.h)</span></span>

<span data-ttu-id="f8888-104">Возвращает нормализованную версию вектора 4D.</span><span class="sxs-lookup"><span data-stu-id="f8888-104">Returns the normalized version of a 4D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8888-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f8888-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Normalize(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="f8888-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f8888-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8888-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="f8888-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f8888-108">Тип: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="f8888-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="f8888-109">Указатель на структуру [**D3DXVECTOR4**](d3dxvector4.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="f8888-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="f8888-110">*ПС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f8888-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8888-111">Тип: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="f8888-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="f8888-112">Указатель на исходную структуру [**D3DXVECTOR4**](d3dxvector4.md) .</span><span class="sxs-lookup"><span data-stu-id="f8888-112">Pointer to the source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8888-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f8888-113">Return value</span></span>

<span data-ttu-id="f8888-114">Тип: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="f8888-114">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="f8888-115">Указатель на структуру [**D3DXVECTOR4**](d3dxvector4.md) , которая является нормализованной версией вектора.</span><span class="sxs-lookup"><span data-stu-id="f8888-115">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is the normalized version of the vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8888-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="f8888-116">Remarks</span></span>

<span data-ttu-id="f8888-117">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="f8888-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="f8888-118">Таким образом, функция **D3DXVec4Normalize** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="f8888-118">In this way, the **D3DXVec4Normalize** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8888-119">Требования</span><span class="sxs-lookup"><span data-stu-id="f8888-119">Requirements</span></span>



| <span data-ttu-id="f8888-120">Требование</span><span class="sxs-lookup"><span data-stu-id="f8888-120">Requirement</span></span> | <span data-ttu-id="f8888-121">Значение</span><span class="sxs-lookup"><span data-stu-id="f8888-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f8888-122">Header</span><span class="sxs-lookup"><span data-stu-id="f8888-122">Header</span></span><br/>  | <dl> <span data-ttu-id="f8888-123"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8888-123"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="f8888-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f8888-124">Library</span></span><br/> | <dl> <span data-ttu-id="f8888-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f8888-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f8888-126">См. также</span><span class="sxs-lookup"><span data-stu-id="f8888-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8888-127">Математические функции</span><span class="sxs-lookup"><span data-stu-id="f8888-127">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




