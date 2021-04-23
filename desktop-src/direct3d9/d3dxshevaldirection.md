---
description: Вычисляет основные функции "сферический гармонией" (SH) на основе вектора направления ввода.
ms.assetid: f30ba32c-d6b0-4e4e-b5cd-839ed7821855
title: Функция D3DXSHEvalDirection (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHEvalDirection
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 005785667d25888550dea38c765a96ea56646d76
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104560244"
---
# <a name="d3dxshevaldirection-function-d3dx9mathh"></a><span data-ttu-id="5092b-103">Функция D3DXSHEvalDirection (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="5092b-103">D3DXSHEvalDirection function (D3dx9math.h)</span></span>

<span data-ttu-id="5092b-104">Вычисляет основные функции "сферический гармонией" (SH) на основе вектора направления ввода.</span><span class="sxs-lookup"><span data-stu-id="5092b-104">Evaluates the spherical harmonic (SH) basis functions from an input direction vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="5092b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5092b-105">Syntax</span></span>


```C++
FLOAT* D3DXSHEvalDirection(
  _Out_       FLOAT       *pOut,
  _In_        UINT        Order,
  _In_  const D3DXVECTOR3 *pDir
);
```



## <a name="parameters"></a><span data-ttu-id="5092b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5092b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5092b-107">*тоска* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="5092b-107">*pOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5092b-108">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="5092b-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="5092b-109">Указатель на коэффициенты вывода в сферическую гармонию (SH).</span><span class="sxs-lookup"><span data-stu-id="5092b-109">Pointer to Spherical harmonic (SH) output coefficients.</span></span> <span data-ttu-id="5092b-110">При оценке создается коэффициент порядка ².</span><span class="sxs-lookup"><span data-stu-id="5092b-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="5092b-111">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="5092b-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="5092b-112">*Порядок следования* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5092b-112">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5092b-113">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5092b-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5092b-114">Порядок вычисления SH.</span><span class="sxs-lookup"><span data-stu-id="5092b-114">Order of the SH evaluation.</span></span> <span data-ttu-id="5092b-115">Должен находиться в диапазоне от [D3DXSH \_ МИНОРДЕР](other-d3dx-constants.md) до D3DXSH \_ максордер, включительно.</span><span class="sxs-lookup"><span data-stu-id="5092b-115">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="5092b-116">При оценке создается коэффициент порядка ².</span><span class="sxs-lookup"><span data-stu-id="5092b-116">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="5092b-117">Степень оценки — Order-1.</span><span class="sxs-lookup"><span data-stu-id="5092b-117">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="5092b-118">*пдир* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5092b-118">*pDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5092b-119">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="5092b-119">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="5092b-120">вектор направления (x, y, z), в котором оцениваются функции-основания SH.</span><span class="sxs-lookup"><span data-stu-id="5092b-120">(x, y, z) direction vector in which to evaluate the SH basis functions.</span></span> <span data-ttu-id="5092b-121">Должен быть нормализован.</span><span class="sxs-lookup"><span data-stu-id="5092b-121">Must be normalized.</span></span> <span data-ttu-id="5092b-122">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="5092b-122">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5092b-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5092b-123">Return value</span></span>

<span data-ttu-id="5092b-124">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="5092b-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="5092b-125">Указатель на коэффициенты вывода SH.</span><span class="sxs-lookup"><span data-stu-id="5092b-125">Pointer to SH output coefficients.</span></span> <span data-ttu-id="5092b-126">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="5092b-126">See Remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="5092b-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5092b-127">Remarks</span></span>

<span data-ttu-id="5092b-128">Каждый коэффициент базисной функции илм хранится в памяти l ² + m + l, где:</span><span class="sxs-lookup"><span data-stu-id="5092b-128">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="5092b-129">l — это степень базовой функции.</span><span class="sxs-lookup"><span data-stu-id="5092b-129">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="5092b-130">m — это базовый индекс функции для заданного значения l и диапазон от-l до l включительно.</span><span class="sxs-lookup"><span data-stu-id="5092b-130">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

<span data-ttu-id="5092b-131">В сфере с радиусом единицы, как показано на следующем рисунке, направление может быть задано просто с помощью тета, угла относительно оси z в [правильном направлении](coordinate-systems.md), а значение фи — от z.</span><span class="sxs-lookup"><span data-stu-id="5092b-131">On the sphere with unit radius, as shown in the following illustration, direction can be specified simply with theta, the angle about the z-axis in the [right-handed direction](coordinate-systems.md), and phi, the angle from z.</span></span>

![Иллюстрация сферы с радиусом единицы](images/spherical-coordinates.png)

<span data-ttu-id="5092b-133">В следующих уравнениях показана связь между координатами декартовы (x, y, z) и сферами (тета, фи) в единичной сфере.</span><span class="sxs-lookup"><span data-stu-id="5092b-133">The following equations show the relationship between Cartesian (x, y, z) and spherical (theta, phi) coordinates on the unit sphere.</span></span> <span data-ttu-id="5092b-134">Угол тета зависит от диапазона от 0 до 2 Пи, а значение фи отличается от 0 до PI.</span><span class="sxs-lookup"><span data-stu-id="5092b-134">The angle theta varies over the range of 0 to 2 pi, while phi varies from 0 to pi.</span></span>

![формулы связи между декартовы и сферыми координатами](images/spherical-coordinates-equations.png)

## <a name="requirements"></a><span data-ttu-id="5092b-136">Требования</span><span class="sxs-lookup"><span data-stu-id="5092b-136">Requirements</span></span>



| <span data-ttu-id="5092b-137">Требование</span><span class="sxs-lookup"><span data-stu-id="5092b-137">Requirement</span></span> | <span data-ttu-id="5092b-138">Значение</span><span class="sxs-lookup"><span data-stu-id="5092b-138">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5092b-139">Header</span><span class="sxs-lookup"><span data-stu-id="5092b-139">Header</span></span><br/>  | <dl> <span data-ttu-id="5092b-140"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="5092b-140"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="5092b-141">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5092b-141">Library</span></span><br/> | <dl> <span data-ttu-id="5092b-142"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5092b-142"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5092b-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5092b-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5092b-144">Математические функции</span><span class="sxs-lookup"><span data-stu-id="5092b-144">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="5092b-145">Предварительно вычисленный перенос Радианце (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="5092b-145">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
