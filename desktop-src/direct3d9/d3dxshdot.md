---
description: Функция D3DXSHDot (D3dx9math. h) — подсчитывает скалярное произведение двух сферических гармонических (SH) векторов.
ms.assetid: 71b7480d-ddac-4b02-bca7-d9318823d03e
title: Функция D3DXSHDot (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHDot
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 87f88c7c7b80871a68084607cb99621199dfcc0a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093932"
---
# <a name="d3dxshdot-function-d3dx9mathh"></a><span data-ttu-id="45342-103">Функция D3DXSHDot (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="45342-103">D3DXSHDot function (D3dx9math.h)</span></span>

<span data-ttu-id="45342-104">Рассчитывает скалярное произведение двух сферических гармонических (SH) векторов.</span><span class="sxs-lookup"><span data-stu-id="45342-104">Computes the dot product of two spherical harmonic (SH) vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="45342-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="45342-105">Syntax</span></span>


```C++
FLOAT D3DXSHDot(
  _In_       UINT  Order,
  _In_ const FLOAT *pA,
  _In_ const FLOAT *pB
);
```



## <a name="parameters"></a><span data-ttu-id="45342-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="45342-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45342-107">*Порядок следования* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="45342-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45342-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="45342-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="45342-109">Порядок вычисления сферического гармонического (SH).</span><span class="sxs-lookup"><span data-stu-id="45342-109">Order of the spherical harmonic (SH) evaluation.</span></span> <span data-ttu-id="45342-110">Должен находиться в диапазоне от [D3DXSH \_ МИНОРДЕР](other-d3dx-constants.md) до D3DXSH \_ максордер, включительно.</span><span class="sxs-lookup"><span data-stu-id="45342-110">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="45342-111">При оценке создается коэффициент порядка ².</span><span class="sxs-lookup"><span data-stu-id="45342-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="45342-112">Степень оценки — Order-1.</span><span class="sxs-lookup"><span data-stu-id="45342-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="45342-113">*PA* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="45342-113">*pA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45342-114">Тип: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="45342-114">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="45342-115">Указатель на первый вектор SH.</span><span class="sxs-lookup"><span data-stu-id="45342-115">Pointer to the first SH vector.</span></span>

</dd> <dt>

<span data-ttu-id="45342-116">*Pb* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="45342-116">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45342-117">Тип: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="45342-117">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="45342-118">Указатель на второй вектор SH.</span><span class="sxs-lookup"><span data-stu-id="45342-118">Pointer to the second SH vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45342-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="45342-119">Return value</span></span>

<span data-ttu-id="45342-120">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="45342-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="45342-121">Коэффициенты вывода SH.</span><span class="sxs-lookup"><span data-stu-id="45342-121">SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="45342-122">Remarks</span><span class="sxs-lookup"><span data-stu-id="45342-122">Remarks</span></span>

<span data-ttu-id="45342-123">Каждый коэффициент базисной функции илм хранится в памяти l ² + m + l, где:</span><span class="sxs-lookup"><span data-stu-id="45342-123">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="45342-124">l — это степень базовой функции.</span><span class="sxs-lookup"><span data-stu-id="45342-124">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="45342-125">m — это базовый индекс функции для заданного значения l и диапазон от-l до l включительно.</span><span class="sxs-lookup"><span data-stu-id="45342-125">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="45342-126">Требования</span><span class="sxs-lookup"><span data-stu-id="45342-126">Requirements</span></span>



| <span data-ttu-id="45342-127">Требование</span><span class="sxs-lookup"><span data-stu-id="45342-127">Requirement</span></span> | <span data-ttu-id="45342-128">Значение</span><span class="sxs-lookup"><span data-stu-id="45342-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="45342-129">Header</span><span class="sxs-lookup"><span data-stu-id="45342-129">Header</span></span><br/>  | <dl> <span data-ttu-id="45342-130"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="45342-130"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="45342-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="45342-131">Library</span></span><br/> | <dl> <span data-ttu-id="45342-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="45342-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="45342-133">См. также</span><span class="sxs-lookup"><span data-stu-id="45342-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45342-134">Математические функции</span><span class="sxs-lookup"><span data-stu-id="45342-134">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="45342-135">Предварительно вычисленный перенос Радианце (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="45342-135">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
