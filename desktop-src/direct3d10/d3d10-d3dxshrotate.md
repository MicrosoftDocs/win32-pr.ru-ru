---
description: Функция D3DXSHRotate (D3DX10. h) — поворачивает сферическую гармонию (SH) на заданную матрицу.
ms.assetid: 22ed379a-ce08-46df-9cc1-8d5fde87c179
title: Функция D3DXSHRotate (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHRotate
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 2f2af3fe59c57ba32bc03bb59233bec72722bbb5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108542"
---
# <a name="d3dxshrotate-function-d3dx10h"></a><span data-ttu-id="4cc16-103">Функция D3DXSHRotate (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="4cc16-103">D3DXSHRotate function (D3DX10.h)</span></span>

<span data-ttu-id="4cc16-104">Поворачивает сферический гармониовый (SH) вектор на заданную матрицу.</span><span class="sxs-lookup"><span data-stu-id="4cc16-104">Rotates the spherical harmonic (SH) vector by the given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cc16-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4cc16-105">Syntax</span></span>


```C++
FLOAT* D3DXSHRotate(
  _In_       FLOAT      *pOut,
  _In_       UINT       Order,
  _In_ const D3DXMATRIX *pMatrix,
  _In_ const FLOAT      *pIn
);
```



## <a name="parameters"></a><span data-ttu-id="4cc16-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4cc16-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cc16-107">*тоска* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4cc16-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cc16-108">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="4cc16-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="4cc16-109">Указатель на коэффициенты вывода в сферическую гармонию (SH).</span><span class="sxs-lookup"><span data-stu-id="4cc16-109">Pointer to Spherical harmonic (SH) output coefficients.</span></span> <span data-ttu-id="4cc16-110">При оценке создается коэффициент порядка ².</span><span class="sxs-lookup"><span data-stu-id="4cc16-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="4cc16-111">Этот указатель не должен иметь псевдоним с ПИН-кодом.</span><span class="sxs-lookup"><span data-stu-id="4cc16-111">This pointer should not alias with pIn.</span></span> <span data-ttu-id="4cc16-112">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="4cc16-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="4cc16-113">*Порядок следования* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4cc16-113">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cc16-114">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4cc16-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4cc16-115">Порядок вычисления SH.</span><span class="sxs-lookup"><span data-stu-id="4cc16-115">Order of the SH evaluation.</span></span> <span data-ttu-id="4cc16-116">Должен находиться в диапазоне от D3DXSH \_ минордер до D3DXSH \_ максордер, включительно.</span><span class="sxs-lookup"><span data-stu-id="4cc16-116">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="4cc16-117">При оценке создается коэффициент порядка ².</span><span class="sxs-lookup"><span data-stu-id="4cc16-117">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="4cc16-118">Степень оценки — Order-1.</span><span class="sxs-lookup"><span data-stu-id="4cc16-118">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="4cc16-119">*пматрикс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4cc16-119">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cc16-120">Тип: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="4cc16-120">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="4cc16-121">Указатель на матрицу вращения.</span><span class="sxs-lookup"><span data-stu-id="4cc16-121">Pointer to the rotation matrix.</span></span> <span data-ttu-id="4cc16-122">Подматрица вращения должна быть ортогональной с определителем единицы.</span><span class="sxs-lookup"><span data-stu-id="4cc16-122">The rotation sub-matrix must be orthogonal, with a unit determinant.</span></span>

</dd> <dt>

<span data-ttu-id="4cc16-123">*закрепить* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4cc16-123">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cc16-124">Тип: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="4cc16-124">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="4cc16-125">Указатель на повернутые коэффициенты SH.</span><span class="sxs-lookup"><span data-stu-id="4cc16-125">Pointer to rotated SH coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cc16-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4cc16-126">Return value</span></span>

<span data-ttu-id="4cc16-127">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="4cc16-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="4cc16-128">Указатель на коэффициенты вывода SH.</span><span class="sxs-lookup"><span data-stu-id="4cc16-128">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="4cc16-129">Remarks</span><span class="sxs-lookup"><span data-stu-id="4cc16-129">Remarks</span></span>

<span data-ttu-id="4cc16-130">Каждый коэффициент базисной функции илм хранится в памяти l ² + m + l, где:</span><span class="sxs-lookup"><span data-stu-id="4cc16-130">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="4cc16-131">l — это степень базовой функции.</span><span class="sxs-lookup"><span data-stu-id="4cc16-131">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="4cc16-132">m — это базовый индекс функции для заданного значения l и диапазон от-l до l включительно.</span><span class="sxs-lookup"><span data-stu-id="4cc16-132">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="4cc16-133">Требования</span><span class="sxs-lookup"><span data-stu-id="4cc16-133">Requirements</span></span>



| <span data-ttu-id="4cc16-134">Требование</span><span class="sxs-lookup"><span data-stu-id="4cc16-134">Requirement</span></span> | <span data-ttu-id="4cc16-135">Значение</span><span class="sxs-lookup"><span data-stu-id="4cc16-135">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4cc16-136">Header</span><span class="sxs-lookup"><span data-stu-id="4cc16-136">Header</span></span><br/>  | <dl> <span data-ttu-id="4cc16-137"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="4cc16-137"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="4cc16-138">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4cc16-138">Library</span></span><br/> | <dl> <span data-ttu-id="4cc16-139"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4cc16-139"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4cc16-140">См. также</span><span class="sxs-lookup"><span data-stu-id="4cc16-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cc16-141">Математические функции</span><span class="sxs-lookup"><span data-stu-id="4cc16-141">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
