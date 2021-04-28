---
description: Функция D3DXSHRotateZ (D3DX10. h) — поворачивает сферическую гармонию (SH) на оси z на заданный угол.
ms.assetid: 7c4bec55-4a4c-4f7e-8849-1cac373a2340
title: Функция D3DXSHRotateZ (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHRotateZ
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 55e4663057bd25ac9768a5913963a5511b662f11
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108532"
---
# <a name="d3dxshrotatez-function-d3dx10h"></a><span data-ttu-id="6eb1d-103">Функция D3DXSHRotateZ (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="6eb1d-103">D3DXSHRotateZ function (D3DX10.h)</span></span>

<span data-ttu-id="6eb1d-104">Поворачивает сферический гармонической (SH) вектор на оси z на заданный угол.</span><span class="sxs-lookup"><span data-stu-id="6eb1d-104">Rotates the spherical harmonic (SH) vector in the z-axis by the given angle.</span></span>

## <a name="syntax"></a><span data-ttu-id="6eb1d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6eb1d-105">Syntax</span></span>


```C++
FLOAT* D3DXSHRotateZ(
  _In_       FLOAT *pOut,
  _In_       UINT  Order,
  _In_       FLOAT Angle,
  _In_ const FLOAT *pIn
);
```



## <a name="parameters"></a><span data-ttu-id="6eb1d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6eb1d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6eb1d-107">*тоска* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6eb1d-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6eb1d-108">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="6eb1d-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="6eb1d-109">Указатель на коэффициенты вывода в сферическую гармонию (SH).</span><span class="sxs-lookup"><span data-stu-id="6eb1d-109">Pointer to Spherical harmonic (SH) output coefficients.</span></span> <span data-ttu-id="6eb1d-110">При оценке создается коэффициент порядка ².</span><span class="sxs-lookup"><span data-stu-id="6eb1d-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="6eb1d-111">Этот указатель не должен иметь псевдоним с ПИН-кодом.</span><span class="sxs-lookup"><span data-stu-id="6eb1d-111">This pointer should not alias with pIn.</span></span> <span data-ttu-id="6eb1d-112">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="6eb1d-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="6eb1d-113">*Порядок следования* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6eb1d-113">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6eb1d-114">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6eb1d-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6eb1d-115">Порядок вычисления SH.</span><span class="sxs-lookup"><span data-stu-id="6eb1d-115">Order of the SH evaluation.</span></span> <span data-ttu-id="6eb1d-116">Должен находиться в диапазоне от D3DXSH \_ минордер до D3DXSH \_ максордер, включительно.</span><span class="sxs-lookup"><span data-stu-id="6eb1d-116">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="6eb1d-117">При оценке создается коэффициент порядка ².</span><span class="sxs-lookup"><span data-stu-id="6eb1d-117">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="6eb1d-118">Степень оценки — Order-1.</span><span class="sxs-lookup"><span data-stu-id="6eb1d-118">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="6eb1d-119">*Угол* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6eb1d-119">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6eb1d-120">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6eb1d-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6eb1d-121">Угол поворота в радианах.</span><span class="sxs-lookup"><span data-stu-id="6eb1d-121">Rotation angle in radians.</span></span> <span data-ttu-id="6eb1d-122">Поворот выполняется вокруг оси z.</span><span class="sxs-lookup"><span data-stu-id="6eb1d-122">The rotation is performed around the z-axis.</span></span>

</dd> <dt>

<span data-ttu-id="6eb1d-123">*закрепить* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6eb1d-123">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6eb1d-124">Тип: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="6eb1d-124">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="6eb1d-125">Указатель на повернутые коэффициенты SH.</span><span class="sxs-lookup"><span data-stu-id="6eb1d-125">Pointer to rotated SH coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6eb1d-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6eb1d-126">Return value</span></span>

<span data-ttu-id="6eb1d-127">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="6eb1d-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="6eb1d-128">Указатель на коэффициенты вывода SH.</span><span class="sxs-lookup"><span data-stu-id="6eb1d-128">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="6eb1d-129">Remarks</span><span class="sxs-lookup"><span data-stu-id="6eb1d-129">Remarks</span></span>

<span data-ttu-id="6eb1d-130">Каждый коэффициент базисной функции илм хранится в памяти l ² + m + l, где:</span><span class="sxs-lookup"><span data-stu-id="6eb1d-130">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="6eb1d-131">l — это степень базовой функции.</span><span class="sxs-lookup"><span data-stu-id="6eb1d-131">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="6eb1d-132">m — это базовый индекс функции для заданного значения l и диапазон от-l до l включительно.</span><span class="sxs-lookup"><span data-stu-id="6eb1d-132">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="6eb1d-133">Требования</span><span class="sxs-lookup"><span data-stu-id="6eb1d-133">Requirements</span></span>



| <span data-ttu-id="6eb1d-134">Требование</span><span class="sxs-lookup"><span data-stu-id="6eb1d-134">Requirement</span></span> | <span data-ttu-id="6eb1d-135">Значение</span><span class="sxs-lookup"><span data-stu-id="6eb1d-135">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6eb1d-136">Header</span><span class="sxs-lookup"><span data-stu-id="6eb1d-136">Header</span></span><br/>  | <dl> <span data-ttu-id="6eb1d-137"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="6eb1d-137"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="6eb1d-138">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6eb1d-138">Library</span></span><br/> | <dl> <span data-ttu-id="6eb1d-139"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6eb1d-139"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6eb1d-140">См. также</span><span class="sxs-lookup"><span data-stu-id="6eb1d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6eb1d-141">Математические функции</span><span class="sxs-lookup"><span data-stu-id="6eb1d-141">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
