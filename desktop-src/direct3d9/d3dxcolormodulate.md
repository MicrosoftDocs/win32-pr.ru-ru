---
description: Смешивает два цвета.
ms.assetid: deff70c7-2359-48b2-ab40-8c418acf5a07
title: Функция D3DXColorModulate (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorModulate
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cf9b202da786f6ec87ceca9816c2a4fc86776577
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273850"
---
# <a name="d3dxcolormodulate-function"></a><span data-ttu-id="b1966-103">Функция D3DXColorModulate</span><span class="sxs-lookup"><span data-stu-id="b1966-103">D3DXColorModulate function</span></span>

<span data-ttu-id="b1966-104">Смешивает два цвета.</span><span class="sxs-lookup"><span data-stu-id="b1966-104">Blends two colors.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1966-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b1966-105">Syntax</span></span>


```C++
D3DXCOLOR* D3DXColorModulate(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC1,
  _In_    const D3DXCOLOR *pC2
);
```



## <a name="parameters"></a><span data-ttu-id="b1966-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b1966-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1966-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="b1966-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b1966-108">Тип: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="b1966-108">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="b1966-109">Указатель на структуру [**D3DXCOLOR**](d3dxcolor.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="b1966-109">Pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="b1966-110">*pC1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b1966-110">*pC1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1966-111">Тип: **const [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="b1966-111">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="b1966-112">Указатель на исходную структуру [**D3DXCOLOR**](d3dxcolor.md) .</span><span class="sxs-lookup"><span data-stu-id="b1966-112">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="b1966-113">*pC2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b1966-113">*pC2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1966-114">Тип: **const [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="b1966-114">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="b1966-115">Указатель на исходную структуру [**D3DXCOLOR**](d3dxcolor.md) .</span><span class="sxs-lookup"><span data-stu-id="b1966-115">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1966-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b1966-116">Return value</span></span>

<span data-ttu-id="b1966-117">Тип: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="b1966-117">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="b1966-118">Эта функция возвращает указатель на структуру [**D3DXCOLOR**](d3dxcolor.md) , которая является результатом операции смешения.</span><span class="sxs-lookup"><span data-stu-id="b1966-118">This function returns a pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the blending operation.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1966-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b1966-119">Remarks</span></span>

<span data-ttu-id="b1966-120">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="b1966-120">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="b1966-121">Таким образом, функция **D3DXColorModulate** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="b1966-121">In this way, the **D3DXColorModulate** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="b1966-122">Эта функция объединяет два цвета, умножая соответствующие компоненты цвета, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="b1966-122">This function blends together two colors by multiplying matching color components, as shown in the following example.</span></span>


```
pOut->r = pC1->r * pC2->r;
```



## <a name="requirements"></a><span data-ttu-id="b1966-123">Требования</span><span class="sxs-lookup"><span data-stu-id="b1966-123">Requirements</span></span>



| <span data-ttu-id="b1966-124">Требование</span><span class="sxs-lookup"><span data-stu-id="b1966-124">Requirement</span></span> | <span data-ttu-id="b1966-125">Значение</span><span class="sxs-lookup"><span data-stu-id="b1966-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1966-126">Header</span><span class="sxs-lookup"><span data-stu-id="b1966-126">Header</span></span><br/>  | <dl> <span data-ttu-id="b1966-127"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1966-127"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="b1966-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b1966-128">Library</span></span><br/> | <dl> <span data-ttu-id="b1966-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b1966-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b1966-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b1966-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1966-131">Математические функции</span><span class="sxs-lookup"><span data-stu-id="b1966-131">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="b1966-132">**D3DXColorLerp**</span><span class="sxs-lookup"><span data-stu-id="b1966-132">**D3DXColorLerp**</span></span>](d3dxcolorlerp.md)
</dt> <dt>

[<span data-ttu-id="b1966-133">**D3DXColorNegative**</span><span class="sxs-lookup"><span data-stu-id="b1966-133">**D3DXColorNegative**</span></span>](d3dxcolornegative.md)
</dt> <dt>

[<span data-ttu-id="b1966-134">**D3DXColorScale**</span><span class="sxs-lookup"><span data-stu-id="b1966-134">**D3DXColorScale**</span></span>](d3dxcolorscale.md)
</dt> </dl>

 

 




