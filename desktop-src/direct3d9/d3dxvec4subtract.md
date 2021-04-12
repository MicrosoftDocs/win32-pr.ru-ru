---
description: Вычитает два вектора 4D.
ms.assetid: 3bc55b38-818e-40eb-859e-495ee28fc4ae
title: Функция D3DXVec4Subtract (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Subtract
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1110930d8e37cf04f7de5129c2a72db4ecc4ac8d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104356133"
---
# <a name="d3dxvec4subtract-function"></a><span data-ttu-id="f15bf-103">Функция D3DXVec4Subtract</span><span class="sxs-lookup"><span data-stu-id="f15bf-103">D3DXVec4Subtract function</span></span>

<span data-ttu-id="f15bf-104">Вычитает два вектора 4D.</span><span class="sxs-lookup"><span data-stu-id="f15bf-104">Subtracts two 4D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="f15bf-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f15bf-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Subtract(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV1,
  _In_    const D3DXVECTOR4 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="f15bf-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f15bf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f15bf-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="f15bf-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f15bf-108">Тип: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="f15bf-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="f15bf-109">Указатель на структуру [**D3DXVECTOR4**](d3dxvector4.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="f15bf-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="f15bf-110">*pV1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f15bf-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f15bf-111">Тип: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="f15bf-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="f15bf-112">Указатель на исходную структуру [**D3DXVECTOR4**](d3dxvector4.md) .</span><span class="sxs-lookup"><span data-stu-id="f15bf-112">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="f15bf-113">*pV2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f15bf-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f15bf-114">Тип: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="f15bf-114">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="f15bf-115">Указатель на исходную структуру [**D3DXVECTOR4**](d3dxvector4.md) .</span><span class="sxs-lookup"><span data-stu-id="f15bf-115">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f15bf-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f15bf-116">Return value</span></span>

<span data-ttu-id="f15bf-117">Тип: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="f15bf-117">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="f15bf-118">Указатель на структуру [**D3DXVECTOR4**](d3dxvector4.md) , которая является разностью двух векторов.</span><span class="sxs-lookup"><span data-stu-id="f15bf-118">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is the difference of two vectors.</span></span>

## <a name="remarks"></a><span data-ttu-id="f15bf-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f15bf-119">Remarks</span></span>

<span data-ttu-id="f15bf-120">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="f15bf-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="f15bf-121">Таким образом, функция **D3DXVec4Subtract** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="f15bf-121">In this way, the **D3DXVec4Subtract** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="f15bf-122">Требования</span><span class="sxs-lookup"><span data-stu-id="f15bf-122">Requirements</span></span>



| <span data-ttu-id="f15bf-123">Требование</span><span class="sxs-lookup"><span data-stu-id="f15bf-123">Requirement</span></span> | <span data-ttu-id="f15bf-124">Значение</span><span class="sxs-lookup"><span data-stu-id="f15bf-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f15bf-125">Header</span><span class="sxs-lookup"><span data-stu-id="f15bf-125">Header</span></span><br/>  | <dl> <span data-ttu-id="f15bf-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="f15bf-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="f15bf-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f15bf-127">Library</span></span><br/> | <dl> <span data-ttu-id="f15bf-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f15bf-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f15bf-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f15bf-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f15bf-130">Математические функции</span><span class="sxs-lookup"><span data-stu-id="f15bf-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="f15bf-131">**D3DXVec3Add**</span><span class="sxs-lookup"><span data-stu-id="f15bf-131">**D3DXVec3Add**</span></span>](d3dxvec3add.md)
</dt> <dt>

[<span data-ttu-id="f15bf-132">**D3DXVec3Scale**</span><span class="sxs-lookup"><span data-stu-id="f15bf-132">**D3DXVec3Scale**</span></span>](d3dxvec3scale.md)
</dt> </dl>

 

 




