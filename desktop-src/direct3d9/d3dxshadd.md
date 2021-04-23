---
description: Добавляет два сферических гармонических (SH) вектора; Иными словами, тоска \[ i \] = PA \[ i \] + Pb \[ i \] .
ms.assetid: 12775c90-ed9d-4931-a449-2571816dd079
title: Функция D3DXSHAdd (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6b8f65a14cf745e8b378728d4fa6e0a234284d2d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105720887"
---
# <a name="d3dxshadd-function-d3dx9mathh"></a><span data-ttu-id="e86c2-103">Функция D3DXSHAdd (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="e86c2-103">D3DXSHAdd function (D3dx9math.h)</span></span>

<span data-ttu-id="e86c2-104">Добавляет два сферических гармонических (SH) вектора; Иными словами, тоска \[ i \] = PA \[ i \] + Pb \[ i \] .</span><span class="sxs-lookup"><span data-stu-id="e86c2-104">Adds two spherical harmonic (SH) vectors; in other words, pOut\[i\] = pA\[i\] + pB\[i\].</span></span>

## <a name="syntax"></a><span data-ttu-id="e86c2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e86c2-105">Syntax</span></span>


```C++
FLOAT* D3DXSHAdd(
  _Out_       FLOAT *pOut,
  _In_        UINT  Order,
  _In_  const FLOAT *pA,
  _In_  const FLOAT *pB
);
```



## <a name="parameters"></a><span data-ttu-id="e86c2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e86c2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e86c2-107">*тоска* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e86c2-107">*pOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e86c2-108">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="e86c2-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e86c2-109">Указатель на коэффициенты вывода SH.</span><span class="sxs-lookup"><span data-stu-id="e86c2-109">Pointer to SH output coefficients.</span></span> <span data-ttu-id="e86c2-110">При оценке создается коэффициент порядка ².</span><span class="sxs-lookup"><span data-stu-id="e86c2-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="e86c2-111">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="e86c2-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="e86c2-112">*Порядок следования* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e86c2-112">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e86c2-113">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e86c2-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e86c2-114">Порядок вычисления SH.</span><span class="sxs-lookup"><span data-stu-id="e86c2-114">Order of the SH evaluation.</span></span> <span data-ttu-id="e86c2-115">Должен находиться в диапазоне от [D3DXSH \_ МИНОРДЕР](other-d3dx-constants.md) до D3DXSH \_ максордер, включительно.</span><span class="sxs-lookup"><span data-stu-id="e86c2-115">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="e86c2-116">При оценке создается коэффициент порядка ².</span><span class="sxs-lookup"><span data-stu-id="e86c2-116">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="e86c2-117">Степень оценки — Order-1.</span><span class="sxs-lookup"><span data-stu-id="e86c2-117">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="e86c2-118">*PA* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e86c2-118">*pA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e86c2-119">Тип: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="e86c2-119">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e86c2-120">Указатель на первый вектор SH.</span><span class="sxs-lookup"><span data-stu-id="e86c2-120">Pointer to the first SH vector.</span></span>

</dd> <dt>

<span data-ttu-id="e86c2-121">*Pb* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e86c2-121">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e86c2-122">Тип: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="e86c2-122">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e86c2-123">Указатель на второй вектор SH.</span><span class="sxs-lookup"><span data-stu-id="e86c2-123">Pointer to the second SH vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e86c2-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e86c2-124">Return value</span></span>

<span data-ttu-id="e86c2-125">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="e86c2-125">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e86c2-126">Указатель на коэффициенты вывода SH.</span><span class="sxs-lookup"><span data-stu-id="e86c2-126">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="e86c2-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e86c2-127">Remarks</span></span>

<span data-ttu-id="e86c2-128">Каждый коэффициент базисной функции илм хранится в памяти l ² + m + l, где:</span><span class="sxs-lookup"><span data-stu-id="e86c2-128">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="e86c2-129">l — это степень базовой функции.</span><span class="sxs-lookup"><span data-stu-id="e86c2-129">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="e86c2-130">m — это базовый индекс функции для заданного значения l и диапазон от-l до l включительно.</span><span class="sxs-lookup"><span data-stu-id="e86c2-130">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="e86c2-131">Требования</span><span class="sxs-lookup"><span data-stu-id="e86c2-131">Requirements</span></span>



| <span data-ttu-id="e86c2-132">Требование</span><span class="sxs-lookup"><span data-stu-id="e86c2-132">Requirement</span></span> | <span data-ttu-id="e86c2-133">Значение</span><span class="sxs-lookup"><span data-stu-id="e86c2-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e86c2-134">Header</span><span class="sxs-lookup"><span data-stu-id="e86c2-134">Header</span></span><br/>  | <dl> <span data-ttu-id="e86c2-135"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="e86c2-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="e86c2-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e86c2-136">Library</span></span><br/> | <dl> <span data-ttu-id="e86c2-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e86c2-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e86c2-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e86c2-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e86c2-139">Математические функции</span><span class="sxs-lookup"><span data-stu-id="e86c2-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="e86c2-140">Предварительно вычисленный перенос Радианце (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="e86c2-140">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
