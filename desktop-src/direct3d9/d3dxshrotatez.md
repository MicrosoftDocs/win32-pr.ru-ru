---
description: Поворачивает сферический гармонической (SH) вектор на оси z на заданный угол.
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
ms.openlocfilehash: ac13cff212aaabdd8a9586b88e3152779bcfaf85
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424385"
---
# <a name="d3dxshrotatez-function-d3dx9mathh"></a><span data-ttu-id="f7b6d-103">Функция D3DXSHRotateZ (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="f7b6d-103">D3DXSHRotateZ function (D3dx9math.h)</span></span>

<span data-ttu-id="f7b6d-104">Поворачивает сферический гармонической (SH) вектор на оси z на заданный угол.</span><span class="sxs-lookup"><span data-stu-id="f7b6d-104">Rotates the spherical harmonic (SH) vector in the z-axis by the given angle.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7b6d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f7b6d-105">Syntax</span></span>


```C++
FLOAT* D3DXSHRotateZ(
  _Out_       FLOAT *pOut,
  _In_        UINT  Order,
  _In_        FLOAT Angle,
  _In_  const FLOAT *pIn
);
```



## <a name="parameters"></a><span data-ttu-id="f7b6d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f7b6d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7b6d-107">*тоска* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f7b6d-107">*pOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f7b6d-108">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="f7b6d-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f7b6d-109">Указатель на коэффициенты вывода в сферическую гармонию (SH).</span><span class="sxs-lookup"><span data-stu-id="f7b6d-109">Pointer to Spherical harmonic (SH) output coefficients.</span></span> <span data-ttu-id="f7b6d-110">При оценке создается коэффициент порядка ².</span><span class="sxs-lookup"><span data-stu-id="f7b6d-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="f7b6d-111">Этот указатель не должен иметь псевдоним с *ПИН-кодом*.</span><span class="sxs-lookup"><span data-stu-id="f7b6d-111">This pointer should not alias with *pIn*.</span></span> <span data-ttu-id="f7b6d-112">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="f7b6d-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="f7b6d-113">*Порядок следования* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f7b6d-113">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7b6d-114">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f7b6d-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f7b6d-115">Порядок вычисления SH.</span><span class="sxs-lookup"><span data-stu-id="f7b6d-115">Order of the SH evaluation.</span></span> <span data-ttu-id="f7b6d-116">Должен находиться в диапазоне от [D3DXSH \_ МИНОРДЕР](other-d3dx-constants.md) до D3DXSH \_ максордер, включительно.</span><span class="sxs-lookup"><span data-stu-id="f7b6d-116">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="f7b6d-117">При оценке создается коэффициент порядка ².</span><span class="sxs-lookup"><span data-stu-id="f7b6d-117">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="f7b6d-118">Степень оценки — Order-1.</span><span class="sxs-lookup"><span data-stu-id="f7b6d-118">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="f7b6d-119">*Угол* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f7b6d-119">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7b6d-120">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f7b6d-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f7b6d-121">Угол поворота в радианах.</span><span class="sxs-lookup"><span data-stu-id="f7b6d-121">Rotation angle in radians.</span></span> <span data-ttu-id="f7b6d-122">Поворот выполняется вокруг оси z.</span><span class="sxs-lookup"><span data-stu-id="f7b6d-122">The rotation is performed around the z-axis.</span></span>

</dd> <dt>

<span data-ttu-id="f7b6d-123">*закрепить* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f7b6d-123">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7b6d-124">Тип: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="f7b6d-124">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f7b6d-125">Указатель на повернутые коэффициенты SH.</span><span class="sxs-lookup"><span data-stu-id="f7b6d-125">Pointer to rotated SH coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7b6d-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f7b6d-126">Return value</span></span>

<span data-ttu-id="f7b6d-127">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="f7b6d-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f7b6d-128">Указатель на коэффициенты вывода SH.</span><span class="sxs-lookup"><span data-stu-id="f7b6d-128">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7b6d-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f7b6d-129">Remarks</span></span>

<span data-ttu-id="f7b6d-130">Каждый коэффициент базисной функции илм хранится в памяти l ² + m + l, где:</span><span class="sxs-lookup"><span data-stu-id="f7b6d-130">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="f7b6d-131">l — это степень базовой функции.</span><span class="sxs-lookup"><span data-stu-id="f7b6d-131">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="f7b6d-132">m — это базовый индекс функции для заданного значения l и диапазон от-l до l включительно.</span><span class="sxs-lookup"><span data-stu-id="f7b6d-132">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7b6d-133">Требования</span><span class="sxs-lookup"><span data-stu-id="f7b6d-133">Requirements</span></span>



| <span data-ttu-id="f7b6d-134">Требование</span><span class="sxs-lookup"><span data-stu-id="f7b6d-134">Requirement</span></span> | <span data-ttu-id="f7b6d-135">Значение</span><span class="sxs-lookup"><span data-stu-id="f7b6d-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f7b6d-136">Header</span><span class="sxs-lookup"><span data-stu-id="f7b6d-136">Header</span></span><br/>  | <dl> <span data-ttu-id="f7b6d-137"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7b6d-137"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="f7b6d-138">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f7b6d-138">Library</span></span><br/> | <dl> <span data-ttu-id="f7b6d-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f7b6d-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f7b6d-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f7b6d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7b6d-141">Математические функции</span><span class="sxs-lookup"><span data-stu-id="f7b6d-141">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="f7b6d-142">Предварительно вычисленный перенос Радианце (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="f7b6d-142">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
