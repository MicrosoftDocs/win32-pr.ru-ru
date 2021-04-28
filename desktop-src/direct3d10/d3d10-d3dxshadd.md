---
description: Функция D3DXSHAdd (D3DX10. h) — складывает два сферических гармонических (SH) вектора; Иными словами, тоска \[ i \] = PA \[ i \] + Pb \[ i \] .
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
ms.openlocfilehash: 8d39940fef4ad611ea530d95efea29c74266d22a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108662"
---
# <a name="d3dxshadd-function-d3dx10h"></a><span data-ttu-id="2a783-103">Функция D3DXSHAdd (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="2a783-103">D3DXSHAdd function (D3DX10.h)</span></span>

<span data-ttu-id="2a783-104">Добавляет два сферических гармонических (SH) вектора; Иными словами, тоска \[ i \] = PA \[ i \] + Pb \[ i \] .</span><span class="sxs-lookup"><span data-stu-id="2a783-104">Adds two spherical harmonic (SH) vectors; in other words, pOut\[i\] = pA\[i\] + pB\[i\].</span></span>

## <a name="syntax"></a><span data-ttu-id="2a783-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2a783-105">Syntax</span></span>


```C++
FLOAT* D3DXSHAdd(
  _In_       FLOAT *pOut,
  _In_       UINT  Order,
  _In_ const FLOAT *pA,
  _In_ const FLOAT *pB
);
```



## <a name="parameters"></a><span data-ttu-id="2a783-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2a783-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a783-107">*тоска* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2a783-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a783-108">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="2a783-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2a783-109">Указатель на коэффициенты вывода SH.</span><span class="sxs-lookup"><span data-stu-id="2a783-109">Pointer to SH output coefficients.</span></span> <span data-ttu-id="2a783-110">При оценке создается коэффициент порядка ².</span><span class="sxs-lookup"><span data-stu-id="2a783-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="2a783-111">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="2a783-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="2a783-112">*Порядок следования* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2a783-112">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a783-113">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2a783-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2a783-114">Порядок вычисления SH.</span><span class="sxs-lookup"><span data-stu-id="2a783-114">Order of the SH evaluation.</span></span> <span data-ttu-id="2a783-115">Должен находиться в диапазоне от D3DXSH \_ минордер до D3DXSH \_ максордер, включительно.</span><span class="sxs-lookup"><span data-stu-id="2a783-115">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="2a783-116">При оценке создается коэффициент порядка ².</span><span class="sxs-lookup"><span data-stu-id="2a783-116">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="2a783-117">Степень оценки — Order-1.</span><span class="sxs-lookup"><span data-stu-id="2a783-117">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="2a783-118">*PA* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2a783-118">*pA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a783-119">Тип: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="2a783-119">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2a783-120">Указатель на первый вектор SH.</span><span class="sxs-lookup"><span data-stu-id="2a783-120">Pointer to the first SH vector.</span></span>

</dd> <dt>

<span data-ttu-id="2a783-121">*Pb* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2a783-121">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a783-122">Тип: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="2a783-122">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2a783-123">Указатель на второй вектор SH.</span><span class="sxs-lookup"><span data-stu-id="2a783-123">Pointer to the second SH vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a783-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2a783-124">Return value</span></span>

<span data-ttu-id="2a783-125">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="2a783-125">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2a783-126">Указатель на коэффициенты вывода SH.</span><span class="sxs-lookup"><span data-stu-id="2a783-126">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a783-127">Remarks</span><span class="sxs-lookup"><span data-stu-id="2a783-127">Remarks</span></span>

<span data-ttu-id="2a783-128">Каждый коэффициент базисной функции илм хранится в памяти l ² + m + l, где:</span><span class="sxs-lookup"><span data-stu-id="2a783-128">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="2a783-129">l — это степень базовой функции.</span><span class="sxs-lookup"><span data-stu-id="2a783-129">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="2a783-130">m — это базовый индекс функции для заданного значения l и диапазон от-l до l включительно.</span><span class="sxs-lookup"><span data-stu-id="2a783-130">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a783-131">Требования</span><span class="sxs-lookup"><span data-stu-id="2a783-131">Requirements</span></span>



| <span data-ttu-id="2a783-132">Требование</span><span class="sxs-lookup"><span data-stu-id="2a783-132">Requirement</span></span> | <span data-ttu-id="2a783-133">Значение</span><span class="sxs-lookup"><span data-stu-id="2a783-133">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2a783-134">Header</span><span class="sxs-lookup"><span data-stu-id="2a783-134">Header</span></span><br/>  | <dl> <span data-ttu-id="2a783-135"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a783-135"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="2a783-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2a783-136">Library</span></span><br/> | <dl> <span data-ttu-id="2a783-137"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2a783-137"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a783-138">См. также</span><span class="sxs-lookup"><span data-stu-id="2a783-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a783-139">Математические функции</span><span class="sxs-lookup"><span data-stu-id="2a783-139">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
