---
description: Поворачивает сферический гармонической (SH) вектор на оси z на заданный угол.
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
ms.openlocfilehash: 0348dd8dfed9b100f64c53427ca2b77dd48ccded
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000438"
---
# <a name="d3dxshrotatez-function-d3dx10h"></a><span data-ttu-id="12d9a-103">Функция D3DXSHRotateZ (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="12d9a-103">D3DXSHRotateZ function (D3DX10.h)</span></span>

<span data-ttu-id="12d9a-104">Поворачивает сферический гармонической (SH) вектор на оси z на заданный угол.</span><span class="sxs-lookup"><span data-stu-id="12d9a-104">Rotates the spherical harmonic (SH) vector in the z-axis by the given angle.</span></span>

## <a name="syntax"></a><span data-ttu-id="12d9a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="12d9a-105">Syntax</span></span>


```C++
FLOAT* D3DXSHRotateZ(
  _In_       FLOAT *pOut,
  _In_       UINT  Order,
  _In_       FLOAT Angle,
  _In_ const FLOAT *pIn
);
```



## <a name="parameters"></a><span data-ttu-id="12d9a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="12d9a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12d9a-107">*тоска* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="12d9a-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12d9a-108">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="12d9a-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="12d9a-109">Указатель на коэффициенты вывода в сферическую гармонию (SH).</span><span class="sxs-lookup"><span data-stu-id="12d9a-109">Pointer to Spherical harmonic (SH) output coefficients.</span></span> <span data-ttu-id="12d9a-110">При оценке создается коэффициент порядка ².</span><span class="sxs-lookup"><span data-stu-id="12d9a-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="12d9a-111">Этот указатель не должен иметь псевдоним с ПИН-кодом.</span><span class="sxs-lookup"><span data-stu-id="12d9a-111">This pointer should not alias with pIn.</span></span> <span data-ttu-id="12d9a-112">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="12d9a-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="12d9a-113">*Порядок следования* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="12d9a-113">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12d9a-114">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="12d9a-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="12d9a-115">Порядок вычисления SH.</span><span class="sxs-lookup"><span data-stu-id="12d9a-115">Order of the SH evaluation.</span></span> <span data-ttu-id="12d9a-116">Должен находиться в диапазоне от D3DXSH \_ минордер до D3DXSH \_ максордер, включительно.</span><span class="sxs-lookup"><span data-stu-id="12d9a-116">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="12d9a-117">При оценке создается коэффициент порядка ².</span><span class="sxs-lookup"><span data-stu-id="12d9a-117">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="12d9a-118">Степень оценки — Order-1.</span><span class="sxs-lookup"><span data-stu-id="12d9a-118">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="12d9a-119">*Угол* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="12d9a-119">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12d9a-120">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="12d9a-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="12d9a-121">Угол поворота в радианах.</span><span class="sxs-lookup"><span data-stu-id="12d9a-121">Rotation angle in radians.</span></span> <span data-ttu-id="12d9a-122">Поворот выполняется вокруг оси z.</span><span class="sxs-lookup"><span data-stu-id="12d9a-122">The rotation is performed around the z-axis.</span></span>

</dd> <dt>

<span data-ttu-id="12d9a-123">*закрепить* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="12d9a-123">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12d9a-124">Тип: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="12d9a-124">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="12d9a-125">Указатель на повернутые коэффициенты SH.</span><span class="sxs-lookup"><span data-stu-id="12d9a-125">Pointer to rotated SH coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12d9a-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="12d9a-126">Return value</span></span>

<span data-ttu-id="12d9a-127">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="12d9a-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="12d9a-128">Указатель на коэффициенты вывода SH.</span><span class="sxs-lookup"><span data-stu-id="12d9a-128">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="12d9a-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="12d9a-129">Remarks</span></span>

<span data-ttu-id="12d9a-130">Каждый коэффициент базисной функции илм хранится в памяти l ² + m + l, где:</span><span class="sxs-lookup"><span data-stu-id="12d9a-130">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="12d9a-131">l — это степень базовой функции.</span><span class="sxs-lookup"><span data-stu-id="12d9a-131">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="12d9a-132">m — это базовый индекс функции для заданного значения l и диапазон от-l до l включительно.</span><span class="sxs-lookup"><span data-stu-id="12d9a-132">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="12d9a-133">Требования</span><span class="sxs-lookup"><span data-stu-id="12d9a-133">Requirements</span></span>



| <span data-ttu-id="12d9a-134">Требование</span><span class="sxs-lookup"><span data-stu-id="12d9a-134">Requirement</span></span> | <span data-ttu-id="12d9a-135">Значение</span><span class="sxs-lookup"><span data-stu-id="12d9a-135">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="12d9a-136">Header</span><span class="sxs-lookup"><span data-stu-id="12d9a-136">Header</span></span><br/>  | <dl> <span data-ttu-id="12d9a-137"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="12d9a-137"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="12d9a-138">Библиотека</span><span class="sxs-lookup"><span data-stu-id="12d9a-138">Library</span></span><br/> | <dl> <span data-ttu-id="12d9a-139"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="12d9a-139"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12d9a-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="12d9a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12d9a-141">Математические функции</span><span class="sxs-lookup"><span data-stu-id="12d9a-141">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
