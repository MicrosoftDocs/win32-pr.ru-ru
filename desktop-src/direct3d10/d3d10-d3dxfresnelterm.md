---
description: Вычислите термин Френелю.
ms.assetid: eaa2e5ea-9b6f-4216-8b48-7be74501124d
title: Функция D3DXFresnelTerm (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFresnelTerm
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1e87649d340e7d90c4df02c641919fd906631268
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104548095"
---
# <a name="d3dxfresnelterm-function-d3dx10mathh"></a><span data-ttu-id="06d24-103">Функция D3DXFresnelTerm (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="06d24-103">D3DXFresnelTerm function (D3DX10Math.h)</span></span>

<span data-ttu-id="06d24-104">Вычислите термин Френелю.</span><span class="sxs-lookup"><span data-stu-id="06d24-104">Calculate the Fresnel term.</span></span>

## <a name="syntax"></a><span data-ttu-id="06d24-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="06d24-105">Syntax</span></span>


```C++
FLOAT D3DXFresnelTerm(
  _In_ FLOAT CosTheta,
  _In_ FLOAT RefractionIndex
);
```



## <a name="parameters"></a><span data-ttu-id="06d24-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="06d24-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06d24-107">*Коссета* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="06d24-107">*CosTheta* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06d24-108">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="06d24-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="06d24-109">Оно должно находиться в диапазоне от 0 до 1.</span><span class="sxs-lookup"><span data-stu-id="06d24-109">The value must be between 0 and 1.</span></span>

</dd> <dt>

<span data-ttu-id="06d24-110">*Рефрактиониндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="06d24-110">*RefractionIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06d24-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="06d24-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="06d24-112">Индекс передробки материала.</span><span class="sxs-lookup"><span data-stu-id="06d24-112">The refraction index of a material.</span></span> <span data-ttu-id="06d24-113">Значение должно быть больше 1.</span><span class="sxs-lookup"><span data-stu-id="06d24-113">The value must be greater than 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06d24-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="06d24-114">Return value</span></span>

<span data-ttu-id="06d24-115">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="06d24-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="06d24-116">Эта функция возвращает термин Френелю для неполярного источника.</span><span class="sxs-lookup"><span data-stu-id="06d24-116">This function returns the Fresnel term for unpolarized light.</span></span> <span data-ttu-id="06d24-117">Коссета — это косинус угла инцидента.</span><span class="sxs-lookup"><span data-stu-id="06d24-117">CosTheta is the cosine of the incident angle.</span></span>

## <a name="remarks"></a><span data-ttu-id="06d24-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="06d24-118">Remarks</span></span>

<span data-ttu-id="06d24-119">Чтобы найти термин Френелю (F), сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="06d24-119">To find the Fresnel term (F):</span></span>

<span data-ttu-id="06d24-120">Если значение равно «Angle», а «B» — угол дроби, то</span><span class="sxs-lookup"><span data-stu-id="06d24-120">If A is angle of incidence and B is the angle of refraction, then</span></span>


```
F = 0.5 * [tan2(A - B) / tan2(A + B) + sin2(A - B) / sin2(A + B)]
  = 0.5 * sin2(A - B) / sin2(A + B) * [cos2(A + B) / cos2(A - B) + 1]

Let r   = sina(A) / sin(B)      (the relative refractive index)
Let c   = cos(A)
Let g   = (r2 + c2 - 1)1/2
```



<span data-ttu-id="06d24-121">Затем, развернув с помощью тригонометрических удостоверений и упростите, вы получаете:</span><span class="sxs-lookup"><span data-stu-id="06d24-121">Then, expanding using the trig identities and simplifying, you get:</span></span>


```
F = 0.5 * (g + c)2 / (g - c)2 * ([c(g + c) - 1]2 / [c(g - c) + 1]2 + 1)
```



## <a name="requirements"></a><span data-ttu-id="06d24-122">Требования</span><span class="sxs-lookup"><span data-stu-id="06d24-122">Requirements</span></span>



| <span data-ttu-id="06d24-123">Требование</span><span class="sxs-lookup"><span data-stu-id="06d24-123">Requirement</span></span> | <span data-ttu-id="06d24-124">Значение</span><span class="sxs-lookup"><span data-stu-id="06d24-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="06d24-125">Header</span><span class="sxs-lookup"><span data-stu-id="06d24-125">Header</span></span><br/>  | <dl> <span data-ttu-id="06d24-126"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="06d24-126"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="06d24-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="06d24-127">Library</span></span><br/> | <dl> <span data-ttu-id="06d24-128"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="06d24-128"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="06d24-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="06d24-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06d24-130">Математические функции</span><span class="sxs-lookup"><span data-stu-id="06d24-130">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
