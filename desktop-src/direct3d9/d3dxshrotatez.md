---
description: Функция D3DXSHRotateZ (D3dx9math. h) — поворачивает сферическую гармонию (SH) на оси z на заданный угол.
ms.assetid: 1f471183-4c8e-4fa8-9a42-f6cc2bb1b0f2
title: Функция D3DXSHRotateZ (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ed7db57dc3acedd1e65edab7377b525940ea10e2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117852"
---
# <a name="d3dxshrotatez-function-d3dx9mathh"></a><span data-ttu-id="31029-103">Функция D3DXSHRotateZ (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="31029-103">D3DXSHRotateZ function (D3dx9math.h)</span></span>

<span data-ttu-id="31029-104">Поворачивает сферический гармонической (SH) вектор на оси z на заданный угол.</span><span class="sxs-lookup"><span data-stu-id="31029-104">Rotates the spherical harmonic (SH) vector in the z-axis by the given angle.</span></span>

## <a name="syntax"></a><span data-ttu-id="31029-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="31029-105">Syntax</span></span>


```C++
FLOAT* D3DXSHRotateZ(
  _Out_       FLOAT *pOut,
  _In_        UINT  Order,
  _In_        FLOAT Angle,
  _In_  const FLOAT *pIn
);
```



## <a name="parameters"></a><span data-ttu-id="31029-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="31029-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31029-107">*тоска* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="31029-107">*pOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="31029-108">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="31029-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="31029-109">Указатель на коэффициенты вывода в сферическую гармонию (SH).</span><span class="sxs-lookup"><span data-stu-id="31029-109">Pointer to Spherical harmonic (SH) output coefficients.</span></span> <span data-ttu-id="31029-110">При оценке создается коэффициент порядка ².</span><span class="sxs-lookup"><span data-stu-id="31029-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="31029-111">Этот указатель не должен иметь псевдоним с *ПИН-кодом*.</span><span class="sxs-lookup"><span data-stu-id="31029-111">This pointer should not alias with *pIn*.</span></span> <span data-ttu-id="31029-112">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="31029-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="31029-113">*Порядок следования* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="31029-113">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31029-114">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="31029-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="31029-115">Порядок вычисления SH.</span><span class="sxs-lookup"><span data-stu-id="31029-115">Order of the SH evaluation.</span></span> <span data-ttu-id="31029-116">Должен находиться в диапазоне от [D3DXSH \_ МИНОРДЕР](other-d3dx-constants.md) до D3DXSH \_ максордер, включительно.</span><span class="sxs-lookup"><span data-stu-id="31029-116">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="31029-117">При оценке создается коэффициент порядка ².</span><span class="sxs-lookup"><span data-stu-id="31029-117">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="31029-118">Степень оценки — Order-1.</span><span class="sxs-lookup"><span data-stu-id="31029-118">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="31029-119">*Угол* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="31029-119">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31029-120">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="31029-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="31029-121">Угол поворота в радианах.</span><span class="sxs-lookup"><span data-stu-id="31029-121">Rotation angle in radians.</span></span> <span data-ttu-id="31029-122">Поворот выполняется вокруг оси z.</span><span class="sxs-lookup"><span data-stu-id="31029-122">The rotation is performed around the z-axis.</span></span>

</dd> <dt>

<span data-ttu-id="31029-123">*закрепить* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="31029-123">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31029-124">Тип: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="31029-124">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="31029-125">Указатель на повернутые коэффициенты SH.</span><span class="sxs-lookup"><span data-stu-id="31029-125">Pointer to rotated SH coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31029-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="31029-126">Return value</span></span>

<span data-ttu-id="31029-127">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="31029-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="31029-128">Указатель на коэффициенты вывода SH.</span><span class="sxs-lookup"><span data-stu-id="31029-128">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="31029-129">Remarks</span><span class="sxs-lookup"><span data-stu-id="31029-129">Remarks</span></span>

<span data-ttu-id="31029-130">Каждый коэффициент базисной функции илм хранится в памяти l ² + m + l, где:</span><span class="sxs-lookup"><span data-stu-id="31029-130">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="31029-131">l — это степень базовой функции.</span><span class="sxs-lookup"><span data-stu-id="31029-131">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="31029-132">m — это базовый индекс функции для заданного значения l и диапазон от-l до l включительно.</span><span class="sxs-lookup"><span data-stu-id="31029-132">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="31029-133">Требования</span><span class="sxs-lookup"><span data-stu-id="31029-133">Requirements</span></span>



| <span data-ttu-id="31029-134">Требование</span><span class="sxs-lookup"><span data-stu-id="31029-134">Requirement</span></span> | <span data-ttu-id="31029-135">Значение</span><span class="sxs-lookup"><span data-stu-id="31029-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="31029-136">Header</span><span class="sxs-lookup"><span data-stu-id="31029-136">Header</span></span><br/>  | <dl> <span data-ttu-id="31029-137"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="31029-137"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="31029-138">Библиотека</span><span class="sxs-lookup"><span data-stu-id="31029-138">Library</span></span><br/> | <dl> <span data-ttu-id="31029-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="31029-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="31029-140">См. также</span><span class="sxs-lookup"><span data-stu-id="31029-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31029-141">Математические функции</span><span class="sxs-lookup"><span data-stu-id="31029-141">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="31029-142">Предварительно вычисленный перенос Радианце (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="31029-142">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
