---
description: Рассчитывает скалярное произведение двух сферических гармонических (SH) векторов.
ms.assetid: 30f0e858-4c31-4b25-9979-754d996a7d48
title: Функция D3DXSHDot (D3DX10. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 20f0896168dae0e2a779625c683777938c8e2df2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703906"
---
# <a name="d3dxshdot-function-d3dx10h"></a><span data-ttu-id="d99ea-103">Функция D3DXSHDot (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="d99ea-103">D3DXSHDot function (D3DX10.h)</span></span>

<span data-ttu-id="d99ea-104">Рассчитывает скалярное произведение двух сферических гармонических (SH) векторов.</span><span class="sxs-lookup"><span data-stu-id="d99ea-104">Computes the dot product of two spherical harmonic (SH) vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="d99ea-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d99ea-105">Syntax</span></span>


```C++
FLOAT D3DXSHDot(
  _In_       UINT  Order,
  _In_ const FLOAT *pA,
  _In_ const FLOAT *pB
);
```



## <a name="parameters"></a><span data-ttu-id="d99ea-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d99ea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d99ea-107">*Порядок следования* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d99ea-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d99ea-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d99ea-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d99ea-109">Порядок вычисления сферического гармонического (SH).</span><span class="sxs-lookup"><span data-stu-id="d99ea-109">Order of the spherical harmonic (SH) evaluation.</span></span> <span data-ttu-id="d99ea-110">Должен находиться в диапазоне от D3DXSH \_ минордер до D3DXSH \_ максордер, включительно.</span><span class="sxs-lookup"><span data-stu-id="d99ea-110">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="d99ea-111">При оценке создается коэффициент порядка ².</span><span class="sxs-lookup"><span data-stu-id="d99ea-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="d99ea-112">Степень оценки — Order-1.</span><span class="sxs-lookup"><span data-stu-id="d99ea-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="d99ea-113">*PA* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d99ea-113">*pA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d99ea-114">Тип: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="d99ea-114">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d99ea-115">Указатель на первый вектор SH.</span><span class="sxs-lookup"><span data-stu-id="d99ea-115">Pointer to the first SH vector.</span></span>

</dd> <dt>

<span data-ttu-id="d99ea-116">*Pb* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d99ea-116">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d99ea-117">Тип: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="d99ea-117">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d99ea-118">Указатель на второй вектор SH.</span><span class="sxs-lookup"><span data-stu-id="d99ea-118">Pointer to the second SH vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d99ea-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d99ea-119">Return value</span></span>

<span data-ttu-id="d99ea-120">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d99ea-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d99ea-121">Коэффициенты вывода SH.</span><span class="sxs-lookup"><span data-stu-id="d99ea-121">SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="d99ea-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d99ea-122">Remarks</span></span>

<span data-ttu-id="d99ea-123">Каждый коэффициент базисной функции илм хранится в памяти l ² + m + l, где:</span><span class="sxs-lookup"><span data-stu-id="d99ea-123">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="d99ea-124">l — это степень базовой функции.</span><span class="sxs-lookup"><span data-stu-id="d99ea-124">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="d99ea-125">m — это базовый индекс функции для заданного значения l и диапазон от-l до l включительно.</span><span class="sxs-lookup"><span data-stu-id="d99ea-125">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="d99ea-126">Требования</span><span class="sxs-lookup"><span data-stu-id="d99ea-126">Requirements</span></span>



| <span data-ttu-id="d99ea-127">Требование</span><span class="sxs-lookup"><span data-stu-id="d99ea-127">Requirement</span></span> | <span data-ttu-id="d99ea-128">Значение</span><span class="sxs-lookup"><span data-stu-id="d99ea-128">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d99ea-129">Header</span><span class="sxs-lookup"><span data-stu-id="d99ea-129">Header</span></span><br/>  | <dl> <span data-ttu-id="d99ea-130"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="d99ea-130"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="d99ea-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d99ea-131">Library</span></span><br/> | <dl> <span data-ttu-id="d99ea-132"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d99ea-132"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d99ea-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d99ea-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d99ea-134">Математические функции</span><span class="sxs-lookup"><span data-stu-id="d99ea-134">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
