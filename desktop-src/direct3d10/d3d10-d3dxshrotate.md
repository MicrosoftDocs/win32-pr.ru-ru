---
description: Поворачивает сферический гармониовый (SH) вектор на заданную матрицу.
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
ms.openlocfilehash: 1cdff4a74cb92943db2bd6dc9f207dbac2208afa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694263"
---
# <a name="d3dxshrotate-function-d3dx10h"></a><span data-ttu-id="187fa-103">Функция D3DXSHRotate (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="187fa-103">D3DXSHRotate function (D3DX10.h)</span></span>

<span data-ttu-id="187fa-104">Поворачивает сферический гармониовый (SH) вектор на заданную матрицу.</span><span class="sxs-lookup"><span data-stu-id="187fa-104">Rotates the spherical harmonic (SH) vector by the given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="187fa-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="187fa-105">Syntax</span></span>


```C++
FLOAT* D3DXSHRotate(
  _In_       FLOAT      *pOut,
  _In_       UINT       Order,
  _In_ const D3DXMATRIX *pMatrix,
  _In_ const FLOAT      *pIn
);
```



## <a name="parameters"></a><span data-ttu-id="187fa-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="187fa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="187fa-107">*тоска* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="187fa-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="187fa-108">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="187fa-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="187fa-109">Указатель на коэффициенты вывода в сферическую гармонию (SH).</span><span class="sxs-lookup"><span data-stu-id="187fa-109">Pointer to Spherical harmonic (SH) output coefficients.</span></span> <span data-ttu-id="187fa-110">При оценке создается коэффициент порядка ².</span><span class="sxs-lookup"><span data-stu-id="187fa-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="187fa-111">Этот указатель не должен иметь псевдоним с ПИН-кодом.</span><span class="sxs-lookup"><span data-stu-id="187fa-111">This pointer should not alias with pIn.</span></span> <span data-ttu-id="187fa-112">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="187fa-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="187fa-113">*Порядок следования* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="187fa-113">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="187fa-114">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="187fa-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="187fa-115">Порядок вычисления SH.</span><span class="sxs-lookup"><span data-stu-id="187fa-115">Order of the SH evaluation.</span></span> <span data-ttu-id="187fa-116">Должен находиться в диапазоне от D3DXSH \_ минордер до D3DXSH \_ максордер, включительно.</span><span class="sxs-lookup"><span data-stu-id="187fa-116">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="187fa-117">При оценке создается коэффициент порядка ².</span><span class="sxs-lookup"><span data-stu-id="187fa-117">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="187fa-118">Степень оценки — Order-1.</span><span class="sxs-lookup"><span data-stu-id="187fa-118">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="187fa-119">*пматрикс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="187fa-119">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="187fa-120">Тип: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="187fa-120">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="187fa-121">Указатель на матрицу вращения.</span><span class="sxs-lookup"><span data-stu-id="187fa-121">Pointer to the rotation matrix.</span></span> <span data-ttu-id="187fa-122">Подматрица вращения должна быть ортогональной с определителем единицы.</span><span class="sxs-lookup"><span data-stu-id="187fa-122">The rotation sub-matrix must be orthogonal, with a unit determinant.</span></span>

</dd> <dt>

<span data-ttu-id="187fa-123">*закрепить* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="187fa-123">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="187fa-124">Тип: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="187fa-124">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="187fa-125">Указатель на повернутые коэффициенты SH.</span><span class="sxs-lookup"><span data-stu-id="187fa-125">Pointer to rotated SH coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="187fa-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="187fa-126">Return value</span></span>

<span data-ttu-id="187fa-127">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="187fa-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="187fa-128">Указатель на коэффициенты вывода SH.</span><span class="sxs-lookup"><span data-stu-id="187fa-128">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="187fa-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="187fa-129">Remarks</span></span>

<span data-ttu-id="187fa-130">Каждый коэффициент базисной функции илм хранится в памяти l ² + m + l, где:</span><span class="sxs-lookup"><span data-stu-id="187fa-130">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="187fa-131">l — это степень базовой функции.</span><span class="sxs-lookup"><span data-stu-id="187fa-131">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="187fa-132">m — это базовый индекс функции для заданного значения l и диапазон от-l до l включительно.</span><span class="sxs-lookup"><span data-stu-id="187fa-132">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="187fa-133">Требования</span><span class="sxs-lookup"><span data-stu-id="187fa-133">Requirements</span></span>



| <span data-ttu-id="187fa-134">Требование</span><span class="sxs-lookup"><span data-stu-id="187fa-134">Requirement</span></span> | <span data-ttu-id="187fa-135">Значение</span><span class="sxs-lookup"><span data-stu-id="187fa-135">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="187fa-136">Header</span><span class="sxs-lookup"><span data-stu-id="187fa-136">Header</span></span><br/>  | <dl> <span data-ttu-id="187fa-137"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="187fa-137"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="187fa-138">Библиотека</span><span class="sxs-lookup"><span data-stu-id="187fa-138">Library</span></span><br/> | <dl> <span data-ttu-id="187fa-139"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="187fa-139"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="187fa-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="187fa-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="187fa-141">Математические функции</span><span class="sxs-lookup"><span data-stu-id="187fa-141">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
