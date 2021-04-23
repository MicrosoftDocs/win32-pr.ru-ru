---
description: Масштабирует сферический гармониовый вектор (SH); Иными словами, тоска \[ i \] = PA \[ \] \* , масштабирование.
ms.assetid: e7b08b55-e2e7-4f13-bbee-10b844d3ef91
title: Функция D3DXSHScale (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHScale
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1a8cc7c63880876f85969443502db3d5fb3278c5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157171"
---
# <a name="d3dxshscale-function-d3dx9mathh"></a><span data-ttu-id="1457e-103">Функция D3DXSHScale (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="1457e-103">D3DXSHScale function (D3dx9math.h)</span></span>

<span data-ttu-id="1457e-104">Масштабирует сферический гармониовый вектор (SH); Иными словами, тоска \[ i \] = PA \[ \] \* , масштабирование.</span><span class="sxs-lookup"><span data-stu-id="1457e-104">Scales a spherical harmonic (SH) vector; in other words, pOut\[i\] = pA\[i\]\*Scale.</span></span>

## <a name="syntax"></a><span data-ttu-id="1457e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1457e-105">Syntax</span></span>


```C++
FLOAT* D3DXSHScale(
  _Out_       FLOAT *pOut,
  _In_        UINT  Order,
  _In_  const FLOAT *pIn,
  _In_  const FLOAT *Scale
);
```



## <a name="parameters"></a><span data-ttu-id="1457e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1457e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1457e-107">*тоска* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="1457e-107">*pOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1457e-108">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="1457e-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1457e-109">Указатель на коэффициенты вывода в сферическую гармонию (SH).</span><span class="sxs-lookup"><span data-stu-id="1457e-109">Pointer to Spherical harmonic (SH) output coefficients.</span></span> <span data-ttu-id="1457e-110">При оценке создается коэффициент порядка ².</span><span class="sxs-lookup"><span data-stu-id="1457e-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="1457e-111">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="1457e-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="1457e-112">*Порядок следования* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1457e-112">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1457e-113">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1457e-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1457e-114">Порядок вычисления SH.</span><span class="sxs-lookup"><span data-stu-id="1457e-114">Order of the SH evaluation.</span></span> <span data-ttu-id="1457e-115">Должен находиться в диапазоне от [D3DXSH \_ МИНОРДЕР](other-d3dx-constants.md) до D3DXSH \_ максордер, включительно.</span><span class="sxs-lookup"><span data-stu-id="1457e-115">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="1457e-116">При оценке создается коэффициент порядка ².</span><span class="sxs-lookup"><span data-stu-id="1457e-116">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="1457e-117">Степень оценки — Order-1.</span><span class="sxs-lookup"><span data-stu-id="1457e-117">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="1457e-118">*закрепить* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1457e-118">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1457e-119">Тип: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="1457e-119">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1457e-120">Указатель на вектор SH для масштабирования.</span><span class="sxs-lookup"><span data-stu-id="1457e-120">Pointer to the SH vector to scale.</span></span>

</dd> <dt>

<span data-ttu-id="1457e-121">*Масштаб* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1457e-121">*Scale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1457e-122">Тип: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="1457e-122">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1457e-123">Указатель на значение шкалы.</span><span class="sxs-lookup"><span data-stu-id="1457e-123">Pointer to the scale value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1457e-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1457e-124">Return value</span></span>

<span data-ttu-id="1457e-125">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="1457e-125">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1457e-126">Указатель на коэффициенты вывода SH.</span><span class="sxs-lookup"><span data-stu-id="1457e-126">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="1457e-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1457e-127">Remarks</span></span>

<span data-ttu-id="1457e-128">Каждый коэффициент базисной функции илм хранится в памяти l ² + m + l, где:</span><span class="sxs-lookup"><span data-stu-id="1457e-128">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="1457e-129">l — это степень базовой функции.</span><span class="sxs-lookup"><span data-stu-id="1457e-129">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="1457e-130">m — это базовый индекс функции для заданного значения l и диапазон от-l до l включительно.</span><span class="sxs-lookup"><span data-stu-id="1457e-130">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="1457e-131">Требования</span><span class="sxs-lookup"><span data-stu-id="1457e-131">Requirements</span></span>



| <span data-ttu-id="1457e-132">Требование</span><span class="sxs-lookup"><span data-stu-id="1457e-132">Requirement</span></span> | <span data-ttu-id="1457e-133">Значение</span><span class="sxs-lookup"><span data-stu-id="1457e-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1457e-134">Header</span><span class="sxs-lookup"><span data-stu-id="1457e-134">Header</span></span><br/>  | <dl> <span data-ttu-id="1457e-135"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="1457e-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="1457e-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1457e-136">Library</span></span><br/> | <dl> <span data-ttu-id="1457e-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1457e-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1457e-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1457e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1457e-139">Математические функции</span><span class="sxs-lookup"><span data-stu-id="1457e-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="1457e-140">Предварительно вычисленный перенос Радианце (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="1457e-140">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
