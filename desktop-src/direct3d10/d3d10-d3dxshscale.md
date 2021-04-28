---
description: Функция D3DXSHScale (D3DX10. h) — масштабирует сферический гармониовый вектор (SH); Иными словами, тоска \[ i \] = PA \[ \] \* , масштабирование.
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
ms.openlocfilehash: 0fab96575e5542eaaed725a88f9ba52c3289a4ad
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108502"
---
# <a name="d3dxshscale-function-d3dx10h"></a><span data-ttu-id="81517-103">Функция D3DXSHScale (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="81517-103">D3DXSHScale function (D3DX10.h)</span></span>

<span data-ttu-id="81517-104">Масштабирует сферический гармониовый вектор (SH); Иными словами, тоска \[ i \] = PA \[ \] \* , масштабирование.</span><span class="sxs-lookup"><span data-stu-id="81517-104">Scales a spherical harmonic (SH) vector; in other words, pOut\[i\] = pA\[i\]\*Scale.</span></span>

## <a name="syntax"></a><span data-ttu-id="81517-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="81517-105">Syntax</span></span>


```C++
FLOAT* D3DXSHScale(
  _In_       FLOAT *pOut,
  _In_       UINT  Order,
  _In_ const FLOAT *pIn,
  _In_ const FLOAT Scale
);
```



## <a name="parameters"></a><span data-ttu-id="81517-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="81517-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81517-107">*тоска* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="81517-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81517-108">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="81517-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="81517-109">Указатель на коэффициенты вывода в сферическую гармонию (SH).</span><span class="sxs-lookup"><span data-stu-id="81517-109">Pointer to Spherical harmonic (SH) output coefficients.</span></span> <span data-ttu-id="81517-110">При оценке создается коэффициент порядка ².</span><span class="sxs-lookup"><span data-stu-id="81517-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="81517-111">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="81517-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="81517-112">*Порядок следования* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="81517-112">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81517-113">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="81517-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="81517-114">Порядок вычисления SH.</span><span class="sxs-lookup"><span data-stu-id="81517-114">Order of the SH evaluation.</span></span> <span data-ttu-id="81517-115">Должен находиться в диапазоне от D3DXSH \_ минордер до D3DXSH \_ максордер, включительно.</span><span class="sxs-lookup"><span data-stu-id="81517-115">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="81517-116">При оценке создается коэффициент порядка ².</span><span class="sxs-lookup"><span data-stu-id="81517-116">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="81517-117">Степень оценки — Order-1.</span><span class="sxs-lookup"><span data-stu-id="81517-117">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="81517-118">*закрепить* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="81517-118">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81517-119">Тип: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="81517-119">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="81517-120">Указатель на вектор SH для масштабирования.</span><span class="sxs-lookup"><span data-stu-id="81517-120">Pointer to the SH vector to scale.</span></span>

</dd> <dt>

<span data-ttu-id="81517-121">*Масштаб* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="81517-121">*Scale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81517-122">Тип: **const [**float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="81517-122">Type: **const [**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="81517-123">Указатель на значение шкалы.</span><span class="sxs-lookup"><span data-stu-id="81517-123">Pointer to the scale value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81517-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="81517-124">Return value</span></span>

<span data-ttu-id="81517-125">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="81517-125">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="81517-126">Указатель на коэффициенты вывода SH.</span><span class="sxs-lookup"><span data-stu-id="81517-126">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="81517-127">Remarks</span><span class="sxs-lookup"><span data-stu-id="81517-127">Remarks</span></span>

<span data-ttu-id="81517-128">Каждый коэффициент базисной функции илм хранится в памяти l ² + m + l, где:</span><span class="sxs-lookup"><span data-stu-id="81517-128">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="81517-129">l — это степень базовой функции.</span><span class="sxs-lookup"><span data-stu-id="81517-129">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="81517-130">m — это базовый индекс функции для заданного значения l и диапазон от-l до l включительно.</span><span class="sxs-lookup"><span data-stu-id="81517-130">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="81517-131">Требования</span><span class="sxs-lookup"><span data-stu-id="81517-131">Requirements</span></span>



| <span data-ttu-id="81517-132">Требование</span><span class="sxs-lookup"><span data-stu-id="81517-132">Requirement</span></span> | <span data-ttu-id="81517-133">Значение</span><span class="sxs-lookup"><span data-stu-id="81517-133">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="81517-134">Header</span><span class="sxs-lookup"><span data-stu-id="81517-134">Header</span></span><br/>  | <dl> <span data-ttu-id="81517-135"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="81517-135"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="81517-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="81517-136">Library</span></span><br/> | <dl> <span data-ttu-id="81517-137"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="81517-137"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81517-138">См. также</span><span class="sxs-lookup"><span data-stu-id="81517-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81517-139">Математические функции</span><span class="sxs-lookup"><span data-stu-id="81517-139">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
