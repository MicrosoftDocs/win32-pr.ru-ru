---
description: Функция D3DXVec4Transform (D3dx9math. h) — преобразует вектор 4D по заданной матрице.
ms.assetid: de93f138-7cf8-43cc-8255-c053c799aea8
title: Функция D3DXVec4Transform (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Transform
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2e5a9fdd92a2d978c746543fbbbeec6503d07404
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115512"
---
# <a name="d3dxvec4transform-function-d3dx9mathh"></a><span data-ttu-id="ddec3-103">Функция D3DXVec4Transform (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="ddec3-103">D3DXVec4Transform function (D3dx9math.h)</span></span>

<span data-ttu-id="ddec3-104">Преобразует вектор 4D по заданной матрице.</span><span class="sxs-lookup"><span data-stu-id="ddec3-104">Transforms a 4D vector by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="ddec3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ddec3-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Transform(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="ddec3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ddec3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ddec3-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="ddec3-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ddec3-108">Тип: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="ddec3-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="ddec3-109">Указатель на структуру [**D3DXVECTOR4**](d3dxvector4.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="ddec3-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="ddec3-110">*ПС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ddec3-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ddec3-111">Тип: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="ddec3-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="ddec3-112">Указатель на исходную структуру [**D3DXVECTOR4**](d3dxvector4.md) .</span><span class="sxs-lookup"><span data-stu-id="ddec3-112">Pointer to the source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="ddec3-113">*PM* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ddec3-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ddec3-114">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="ddec3-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="ddec3-115">Указатель на исходную структуру [**D3DXMATRIX**](d3dxmatrix.md) .</span><span class="sxs-lookup"><span data-stu-id="ddec3-115">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ddec3-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ddec3-116">Return value</span></span>

<span data-ttu-id="ddec3-117">Тип: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="ddec3-117">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="ddec3-118">Указатель на структуру [**D3DXVECTOR4**](d3dxvector4.md) , которая является преобразованным вектором 4d.</span><span class="sxs-lookup"><span data-stu-id="ddec3-118">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is the transformed 4D vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="ddec3-119">Remarks</span><span class="sxs-lookup"><span data-stu-id="ddec3-119">Remarks</span></span>

<span data-ttu-id="ddec3-120">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="ddec3-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="ddec3-121">Таким образом, функция **D3DXVec4Transform** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="ddec3-121">In this way, the **D3DXVec4Transform** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="ddec3-122">Требования</span><span class="sxs-lookup"><span data-stu-id="ddec3-122">Requirements</span></span>



| <span data-ttu-id="ddec3-123">Требование</span><span class="sxs-lookup"><span data-stu-id="ddec3-123">Requirement</span></span> | <span data-ttu-id="ddec3-124">Значение</span><span class="sxs-lookup"><span data-stu-id="ddec3-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ddec3-125">Header</span><span class="sxs-lookup"><span data-stu-id="ddec3-125">Header</span></span><br/>  | <dl> <span data-ttu-id="ddec3-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="ddec3-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="ddec3-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ddec3-127">Library</span></span><br/> | <dl> <span data-ttu-id="ddec3-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ddec3-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ddec3-129">См. также</span><span class="sxs-lookup"><span data-stu-id="ddec3-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddec3-130">Математические функции</span><span class="sxs-lookup"><span data-stu-id="ddec3-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




