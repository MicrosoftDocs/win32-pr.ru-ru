---
description: Масштабирует вектор 4D.
ms.assetid: b185a9b9-f768-4b50-aa6c-667c71eac39a
title: Функция D3DXVec4Scale (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Scale
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a29ee7b8519c802deb0542b6b7ba3ea22692f36d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703819"
---
# <a name="d3dxvec4scale-function"></a><span data-ttu-id="2f2f8-103">Функция D3DXVec4Scale</span><span class="sxs-lookup"><span data-stu-id="2f2f8-103">D3DXVec4Scale function</span></span>

<span data-ttu-id="2f2f8-104">Масштабирует вектор 4D.</span><span class="sxs-lookup"><span data-stu-id="2f2f8-104">Scales a 4D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f2f8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2f2f8-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Scale(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a><span data-ttu-id="2f2f8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2f2f8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f2f8-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="2f2f8-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2f2f8-108">Тип: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="2f2f8-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="2f2f8-109">Указатель на структуру [**D3DXVECTOR4**](d3dxvector4.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="2f2f8-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="2f2f8-110">*ПС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2f2f8-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f2f8-111">Тип: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="2f2f8-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="2f2f8-112">Указатель на исходную структуру [**D3DXVECTOR4**](d3dxvector4.md) .</span><span class="sxs-lookup"><span data-stu-id="2f2f8-112">Pointer to the source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="2f2f8-113">*s* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="2f2f8-113">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f2f8-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2f2f8-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2f2f8-115">Значение масштабирования.</span><span class="sxs-lookup"><span data-stu-id="2f2f8-115">Scaling value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f2f8-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2f2f8-116">Return value</span></span>

<span data-ttu-id="2f2f8-117">Тип: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="2f2f8-117">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="2f2f8-118">Указатель на структуру [**D3DXVECTOR4**](d3dxvector4.md) , которая является масштабируемым вектором.</span><span class="sxs-lookup"><span data-stu-id="2f2f8-118">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the scaled vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f2f8-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2f2f8-119">Remarks</span></span>

<span data-ttu-id="2f2f8-120">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="2f2f8-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="2f2f8-121">Таким образом, функция **D3DXVec4Scale** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="2f2f8-121">In this way, the **D3DXVec4Scale** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f2f8-122">Требования</span><span class="sxs-lookup"><span data-stu-id="2f2f8-122">Requirements</span></span>



| <span data-ttu-id="2f2f8-123">Требование</span><span class="sxs-lookup"><span data-stu-id="2f2f8-123">Requirement</span></span> | <span data-ttu-id="2f2f8-124">Значение</span><span class="sxs-lookup"><span data-stu-id="2f2f8-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f2f8-125">Header</span><span class="sxs-lookup"><span data-stu-id="2f2f8-125">Header</span></span><br/>  | <dl> <span data-ttu-id="2f2f8-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f2f8-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="2f2f8-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2f2f8-127">Library</span></span><br/> | <dl> <span data-ttu-id="2f2f8-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2f2f8-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2f2f8-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2f2f8-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f2f8-130">Математические функции</span><span class="sxs-lookup"><span data-stu-id="2f2f8-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="2f2f8-131">**D3DXVec4Add**</span><span class="sxs-lookup"><span data-stu-id="2f2f8-131">**D3DXVec4Add**</span></span>](d3dxvec4add.md)
</dt> <dt>

[<span data-ttu-id="2f2f8-132">**D3DXVec4Subtract**</span><span class="sxs-lookup"><span data-stu-id="2f2f8-132">**D3DXVec4Subtract**</span></span>](d3dxvec4subtract.md)
</dt> </dl>

 

 
