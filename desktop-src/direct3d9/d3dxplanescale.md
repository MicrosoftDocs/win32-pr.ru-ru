---
description: Масштабирование плоскости с помощью заданного коэффициента масштабирования.
ms.assetid: 3a0454ef-2821-472f-b7a4-5e49bb5f556e
title: Функция D3DXPlaneScale (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneScale
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 39bd80ceebaee915b8175f2adf13b3b200000fa6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105674675"
---
# <a name="d3dxplanescale-function"></a><span data-ttu-id="32337-103">Функция D3DXPlaneScale</span><span class="sxs-lookup"><span data-stu-id="32337-103">D3DXPlaneScale function</span></span>

<span data-ttu-id="32337-104">Масштабирование плоскости с помощью заданного коэффициента масштабирования.</span><span class="sxs-lookup"><span data-stu-id="32337-104">Scale the plane with the given scaling factor.</span></span>

## <a name="syntax"></a><span data-ttu-id="32337-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="32337-105">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneScale(
  _Inout_       D3DXPLANE *pOut,
  _In_    const D3DXPLANE *pP,
  _In_          FLOAT     s
);
```



## <a name="parameters"></a><span data-ttu-id="32337-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="32337-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32337-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="32337-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="32337-108">Тип: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="32337-108">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="32337-109">Указатель на структуру [**D3DXPLANE**](d3dxplane.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="32337-109">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="32337-110">*PP* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="32337-110">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32337-111">Тип: **const [**D3DXPLANE**](d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="32337-111">Type: **const [**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="32337-112">Указатель на исходную структуру [**D3DXPLANE**](d3dxplane.md) .</span><span class="sxs-lookup"><span data-stu-id="32337-112">Pointer to the source [**D3DXPLANE**](d3dxplane.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="32337-113">*s* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="32337-113">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32337-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="32337-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="32337-115">Коэффициент масштабирования.</span><span class="sxs-lookup"><span data-stu-id="32337-115">Scale factor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32337-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="32337-116">Return value</span></span>

<span data-ttu-id="32337-117">Тип: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="32337-117">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="32337-118">Указатель на структуру [**D3DXPLANE**](d3dxplane.md) , представляющую масштабированную плоскость.</span><span class="sxs-lookup"><span data-stu-id="32337-118">Pointer to a [**D3DXPLANE**](d3dxplane.md) structure that represents the scaled plane.</span></span>

## <a name="remarks"></a><span data-ttu-id="32337-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="32337-119">Remarks</span></span>

<span data-ttu-id="32337-120">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="32337-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="32337-121">Поэтому эту функцию можно использовать в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="32337-121">Therefore, this function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="32337-122">Требования</span><span class="sxs-lookup"><span data-stu-id="32337-122">Requirements</span></span>



| <span data-ttu-id="32337-123">Требование</span><span class="sxs-lookup"><span data-stu-id="32337-123">Requirement</span></span> | <span data-ttu-id="32337-124">Значение</span><span class="sxs-lookup"><span data-stu-id="32337-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="32337-125">Header</span><span class="sxs-lookup"><span data-stu-id="32337-125">Header</span></span><br/>  | <dl> <span data-ttu-id="32337-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="32337-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="32337-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="32337-127">Library</span></span><br/> | <dl> <span data-ttu-id="32337-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="32337-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="32337-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="32337-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32337-130">Математические функции</span><span class="sxs-lookup"><span data-stu-id="32337-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
