---
description: Добавляет два сферических гармонических (SH) вектора; Иными словами, тоска \[ i \] = PA \[ i \] + Pb \[ i \] .
ms.assetid: dbfea12b-c110-42a7-84b6-0dff3d958032
title: Функция D3DXSHAdd (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHAdd
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1750b473764daf030160adc42d258a1f911f5f16
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273915"
---
# <a name="d3dxshadd-function-d3dx10h"></a><span data-ttu-id="e6e13-103">Функция D3DXSHAdd (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="e6e13-103">D3DXSHAdd function (D3DX10.h)</span></span>

<span data-ttu-id="e6e13-104">Добавляет два сферических гармонических (SH) вектора; Иными словами, тоска \[ i \] = PA \[ i \] + Pb \[ i \] .</span><span class="sxs-lookup"><span data-stu-id="e6e13-104">Adds two spherical harmonic (SH) vectors; in other words, pOut\[i\] = pA\[i\] + pB\[i\].</span></span>

## <a name="syntax"></a><span data-ttu-id="e6e13-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e6e13-105">Syntax</span></span>


```C++
FLOAT* D3DXSHAdd(
  _In_       FLOAT *pOut,
  _In_       UINT  Order,
  _In_ const FLOAT *pA,
  _In_ const FLOAT *pB
);
```



## <a name="parameters"></a><span data-ttu-id="e6e13-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e6e13-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6e13-107">*тоска* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e6e13-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6e13-108">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="e6e13-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e6e13-109">Указатель на коэффициенты вывода SH.</span><span class="sxs-lookup"><span data-stu-id="e6e13-109">Pointer to SH output coefficients.</span></span> <span data-ttu-id="e6e13-110">При оценке создается коэффициент порядка ².</span><span class="sxs-lookup"><span data-stu-id="e6e13-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="e6e13-111">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="e6e13-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="e6e13-112">*Порядок следования* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e6e13-112">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6e13-113">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e6e13-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e6e13-114">Порядок вычисления SH.</span><span class="sxs-lookup"><span data-stu-id="e6e13-114">Order of the SH evaluation.</span></span> <span data-ttu-id="e6e13-115">Должен находиться в диапазоне от D3DXSH \_ минордер до D3DXSH \_ максордер, включительно.</span><span class="sxs-lookup"><span data-stu-id="e6e13-115">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="e6e13-116">При оценке создается коэффициент порядка ².</span><span class="sxs-lookup"><span data-stu-id="e6e13-116">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="e6e13-117">Степень оценки — Order-1.</span><span class="sxs-lookup"><span data-stu-id="e6e13-117">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="e6e13-118">*PA* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e6e13-118">*pA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6e13-119">Тип: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="e6e13-119">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e6e13-120">Указатель на первый вектор SH.</span><span class="sxs-lookup"><span data-stu-id="e6e13-120">Pointer to the first SH vector.</span></span>

</dd> <dt>

<span data-ttu-id="e6e13-121">*Pb* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e6e13-121">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6e13-122">Тип: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="e6e13-122">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e6e13-123">Указатель на второй вектор SH.</span><span class="sxs-lookup"><span data-stu-id="e6e13-123">Pointer to the second SH vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6e13-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e6e13-124">Return value</span></span>

<span data-ttu-id="e6e13-125">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="e6e13-125">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e6e13-126">Указатель на коэффициенты вывода SH.</span><span class="sxs-lookup"><span data-stu-id="e6e13-126">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6e13-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e6e13-127">Remarks</span></span>

<span data-ttu-id="e6e13-128">Каждый коэффициент базисной функции илм хранится в памяти l ² + m + l, где:</span><span class="sxs-lookup"><span data-stu-id="e6e13-128">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="e6e13-129">l — это степень базовой функции.</span><span class="sxs-lookup"><span data-stu-id="e6e13-129">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="e6e13-130">m — это базовый индекс функции для заданного значения l и диапазон от-l до l включительно.</span><span class="sxs-lookup"><span data-stu-id="e6e13-130">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6e13-131">Требования</span><span class="sxs-lookup"><span data-stu-id="e6e13-131">Requirements</span></span>



| <span data-ttu-id="e6e13-132">Требование</span><span class="sxs-lookup"><span data-stu-id="e6e13-132">Requirement</span></span> | <span data-ttu-id="e6e13-133">Значение</span><span class="sxs-lookup"><span data-stu-id="e6e13-133">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e6e13-134">Header</span><span class="sxs-lookup"><span data-stu-id="e6e13-134">Header</span></span><br/>  | <dl> <span data-ttu-id="e6e13-135"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6e13-135"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="e6e13-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e6e13-136">Library</span></span><br/> | <dl> <span data-ttu-id="e6e13-137"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e6e13-137"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6e13-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e6e13-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6e13-139">Математические функции</span><span class="sxs-lookup"><span data-stu-id="e6e13-139">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
