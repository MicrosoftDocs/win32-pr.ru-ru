---
description: Масштабирует сферический гармониовый вектор (SH); Иными словами, тоска \[ i \] = PA \[ \] \* , масштабирование.
ms.assetid: e323d238-f635-4780-982d-8798ba178f31
title: Функция D3DXSHScale (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHScale
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 7aa7ee66b29c7d9816708a8625bb568426a62b57
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694262"
---
# <a name="d3dxshscale-function-d3dx10h"></a><span data-ttu-id="ac88c-103">Функция D3DXSHScale (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="ac88c-103">D3DXSHScale function (D3DX10.h)</span></span>

<span data-ttu-id="ac88c-104">Масштабирует сферический гармониовый вектор (SH); Иными словами, тоска \[ i \] = PA \[ \] \* , масштабирование.</span><span class="sxs-lookup"><span data-stu-id="ac88c-104">Scales a spherical harmonic (SH) vector; in other words, pOut\[i\] = pA\[i\]\*Scale.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac88c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ac88c-105">Syntax</span></span>


```C++
FLOAT* D3DXSHScale(
  _In_       FLOAT *pOut,
  _In_       UINT  Order,
  _In_ const FLOAT *pIn,
  _In_ const FLOAT Scale
);
```



## <a name="parameters"></a><span data-ttu-id="ac88c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ac88c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac88c-107">*тоска* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ac88c-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac88c-108">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="ac88c-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ac88c-109">Указатель на коэффициенты вывода в сферическую гармонию (SH).</span><span class="sxs-lookup"><span data-stu-id="ac88c-109">Pointer to Spherical harmonic (SH) output coefficients.</span></span> <span data-ttu-id="ac88c-110">При оценке создается коэффициент порядка ².</span><span class="sxs-lookup"><span data-stu-id="ac88c-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="ac88c-111">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="ac88c-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="ac88c-112">*Порядок следования* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ac88c-112">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac88c-113">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ac88c-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ac88c-114">Порядок вычисления SH.</span><span class="sxs-lookup"><span data-stu-id="ac88c-114">Order of the SH evaluation.</span></span> <span data-ttu-id="ac88c-115">Должен находиться в диапазоне от D3DXSH \_ минордер до D3DXSH \_ максордер, включительно.</span><span class="sxs-lookup"><span data-stu-id="ac88c-115">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="ac88c-116">При оценке создается коэффициент порядка ².</span><span class="sxs-lookup"><span data-stu-id="ac88c-116">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="ac88c-117">Степень оценки — Order-1.</span><span class="sxs-lookup"><span data-stu-id="ac88c-117">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="ac88c-118">*закрепить* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ac88c-118">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac88c-119">Тип: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="ac88c-119">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ac88c-120">Указатель на вектор SH для масштабирования.</span><span class="sxs-lookup"><span data-stu-id="ac88c-120">Pointer to the SH vector to scale.</span></span>

</dd> <dt>

<span data-ttu-id="ac88c-121">*Масштаб* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ac88c-121">*Scale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac88c-122">Тип: **const [**float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ac88c-122">Type: **const [**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ac88c-123">Указатель на значение шкалы.</span><span class="sxs-lookup"><span data-stu-id="ac88c-123">Pointer to the scale value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac88c-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ac88c-124">Return value</span></span>

<span data-ttu-id="ac88c-125">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="ac88c-125">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ac88c-126">Указатель на коэффициенты вывода SH.</span><span class="sxs-lookup"><span data-stu-id="ac88c-126">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac88c-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ac88c-127">Remarks</span></span>

<span data-ttu-id="ac88c-128">Каждый коэффициент базисной функции илм хранится в памяти l ² + m + l, где:</span><span class="sxs-lookup"><span data-stu-id="ac88c-128">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="ac88c-129">l — это степень базовой функции.</span><span class="sxs-lookup"><span data-stu-id="ac88c-129">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="ac88c-130">m — это базовый индекс функции для заданного значения l и диапазон от-l до l включительно.</span><span class="sxs-lookup"><span data-stu-id="ac88c-130">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac88c-131">Требования</span><span class="sxs-lookup"><span data-stu-id="ac88c-131">Requirements</span></span>



| <span data-ttu-id="ac88c-132">Требование</span><span class="sxs-lookup"><span data-stu-id="ac88c-132">Requirement</span></span> | <span data-ttu-id="ac88c-133">Значение</span><span class="sxs-lookup"><span data-stu-id="ac88c-133">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ac88c-134">Header</span><span class="sxs-lookup"><span data-stu-id="ac88c-134">Header</span></span><br/>  | <dl> <span data-ttu-id="ac88c-135"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac88c-135"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="ac88c-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ac88c-136">Library</span></span><br/> | <dl> <span data-ttu-id="ac88c-137"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ac88c-137"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac88c-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ac88c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac88c-139">Математические функции</span><span class="sxs-lookup"><span data-stu-id="ac88c-139">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
