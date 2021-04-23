---
description: Использует линейную интерполяцию для создания значения цвета.
ms.assetid: bf7bf2f4-5fb5-44d3-a7e5-7998640d7d49
title: Функция D3DXColorLerp (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorLerp
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3521ee9e76aecd486093f903d336c08553e0e4ef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103914744"
---
# <a name="d3dxcolorlerp-function"></a><span data-ttu-id="85dba-103">Функция D3DXColorLerp</span><span class="sxs-lookup"><span data-stu-id="85dba-103">D3DXColorLerp function</span></span>

<span data-ttu-id="85dba-104">Использует линейную интерполяцию для создания значения цвета.</span><span class="sxs-lookup"><span data-stu-id="85dba-104">Uses linear interpolation to create a color value.</span></span>

## <a name="syntax"></a><span data-ttu-id="85dba-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="85dba-105">Syntax</span></span>


```C++
D3DXCOLOR* D3DXColorLerp(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC1,
  _In_    const D3DXCOLOR *pC2,
  _In_          FLOAT     s
);
```



## <a name="parameters"></a><span data-ttu-id="85dba-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="85dba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85dba-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="85dba-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="85dba-108">Тип: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="85dba-108">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="85dba-109">Указатель на структуру [**D3DXCOLOR**](d3dxcolor.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="85dba-109">Pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="85dba-110">*pC1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="85dba-110">*pC1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85dba-111">Тип: **const [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="85dba-111">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="85dba-112">Указатель на исходную структуру [**D3DXCOLOR**](d3dxcolor.md) .</span><span class="sxs-lookup"><span data-stu-id="85dba-112">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="85dba-113">*pC2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="85dba-113">*pC2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85dba-114">Тип: **const [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="85dba-114">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="85dba-115">Указатель на исходную структуру [**D3DXCOLOR**](d3dxcolor.md) .</span><span class="sxs-lookup"><span data-stu-id="85dba-115">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="85dba-116">*s* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="85dba-116">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85dba-117">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="85dba-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="85dba-118">Параметр, который линейно выполняет интерполяцию между цветами, pC1 и pC2, рассматривая их как векторы 4D.</span><span class="sxs-lookup"><span data-stu-id="85dba-118">Parameter that linearly interpolates between the colors, pC1 and pC2, treating them both as 4D vectors.</span></span> <span data-ttu-id="85dba-119">Ограничения на значение s отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="85dba-119">There are no limits on the value of s.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85dba-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="85dba-120">Return value</span></span>

<span data-ttu-id="85dba-121">Тип: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="85dba-121">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="85dba-122">Эта функция возвращает указатель на структуру [**D3DXCOLOR**](d3dxcolor.md) , которая является результатом линейной интерполяции.</span><span class="sxs-lookup"><span data-stu-id="85dba-122">This function returns a pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the linear interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="85dba-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="85dba-123">Remarks</span></span>

<span data-ttu-id="85dba-124">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="85dba-124">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="85dba-125">Таким образом, функция **D3DXColorLerp** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="85dba-125">In this way, the **D3DXColorLerp** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="85dba-126">Эта функция выполняет интерполяцию красного, зеленого, синего и альфа-компонентов структуры [**D3DXCOLOR**](d3dxcolor.md) между двумя цветами, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="85dba-126">This function interpolates the red, green, blue, and alpha components of a [**D3DXCOLOR**](d3dxcolor.md) structure between two colors, as shown in the following example.</span></span>


```
   
pOut->r = pC1->r + s * (pC2->r - pC1->r);
```



<span data-ttu-id="85dba-127">Если линейная интерполяция между цветами A и B и s равна 0, то результирующим цветом будет. Если параметр s имеет значение 1, то полученный цвет будет иметь цвет B.</span><span class="sxs-lookup"><span data-stu-id="85dba-127">If you are linearly interpolating between the colors A and B, and s is 0, the resulting color is A. If s is 1, the resulting color is color B.</span></span>

## <a name="requirements"></a><span data-ttu-id="85dba-128">Требования</span><span class="sxs-lookup"><span data-stu-id="85dba-128">Requirements</span></span>



| <span data-ttu-id="85dba-129">Требование</span><span class="sxs-lookup"><span data-stu-id="85dba-129">Requirement</span></span> | <span data-ttu-id="85dba-130">Значение</span><span class="sxs-lookup"><span data-stu-id="85dba-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="85dba-131">Header</span><span class="sxs-lookup"><span data-stu-id="85dba-131">Header</span></span><br/>  | <dl> <span data-ttu-id="85dba-132"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="85dba-132"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="85dba-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="85dba-133">Library</span></span><br/> | <dl> <span data-ttu-id="85dba-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="85dba-134"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="85dba-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="85dba-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85dba-136">Математические функции</span><span class="sxs-lookup"><span data-stu-id="85dba-136">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="85dba-137">**D3DXColorModulate**</span><span class="sxs-lookup"><span data-stu-id="85dba-137">**D3DXColorModulate**</span></span>](d3dxcolormodulate.md)
</dt> <dt>

[<span data-ttu-id="85dba-138">**D3DXColorNegative**</span><span class="sxs-lookup"><span data-stu-id="85dba-138">**D3DXColorNegative**</span></span>](d3dxcolornegative.md)
</dt> <dt>

[<span data-ttu-id="85dba-139">**D3DXColorScale**</span><span class="sxs-lookup"><span data-stu-id="85dba-139">**D3DXColorScale**</span></span>](d3dxcolorscale.md)
</dt> </dl>

 

 
