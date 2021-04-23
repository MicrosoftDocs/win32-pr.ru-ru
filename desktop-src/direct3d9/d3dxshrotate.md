---
description: Поворачивает сферический гармониовый (SH) вектор на заданную матрицу.
ms.assetid: 9e319725-6cbb-441e-b996-ec2c6f66e5df
title: Функция D3DXSHRotate (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 606ef1909237fd9c0277c5d7112284f6b7018e0e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105647843"
---
# <a name="d3dxshrotate-function-d3dx9mathh"></a><span data-ttu-id="277df-103">Функция D3DXSHRotate (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="277df-103">D3DXSHRotate function (D3dx9math.h)</span></span>

<span data-ttu-id="277df-104">Поворачивает сферический гармониовый (SH) вектор на заданную матрицу.</span><span class="sxs-lookup"><span data-stu-id="277df-104">Rotates the spherical harmonic (SH) vector by the given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="277df-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="277df-105">Syntax</span></span>


```C++
FLOAT* D3DXSHRotate(
  _Out_       FLOAT      *pOut,
  _In_        UINT       Order,
  _In_  const D3DXMATRIX *pMatrix,
  _In_  const FLOAT      *pIn
);
```



## <a name="parameters"></a><span data-ttu-id="277df-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="277df-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="277df-107">*тоска* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="277df-107">*pOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="277df-108">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="277df-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="277df-109">Указатель на коэффициенты вывода в сферическую гармонию (SH).</span><span class="sxs-lookup"><span data-stu-id="277df-109">Pointer to Spherical harmonic (SH) output coefficients.</span></span> <span data-ttu-id="277df-110">При оценке создается коэффициент порядка ².</span><span class="sxs-lookup"><span data-stu-id="277df-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="277df-111">Этот указатель не должен иметь псевдоним с *ПИН-кодом*.</span><span class="sxs-lookup"><span data-stu-id="277df-111">This pointer should not alias with *pIn*.</span></span> <span data-ttu-id="277df-112">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="277df-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="277df-113">*Порядок следования* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="277df-113">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="277df-114">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="277df-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="277df-115">Порядок вычисления SH.</span><span class="sxs-lookup"><span data-stu-id="277df-115">Order of the SH evaluation.</span></span> <span data-ttu-id="277df-116">Должен находиться в диапазоне от [D3DXSH \_ МИНОРДЕР](other-d3dx-constants.md) до D3DXSH \_ максордер, включительно.</span><span class="sxs-lookup"><span data-stu-id="277df-116">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="277df-117">При оценке создается коэффициент порядка ².</span><span class="sxs-lookup"><span data-stu-id="277df-117">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="277df-118">Степень оценки — Order-1.</span><span class="sxs-lookup"><span data-stu-id="277df-118">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="277df-119">*пматрикс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="277df-119">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="277df-120">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="277df-120">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="277df-121">Указатель на матрицу вращения.</span><span class="sxs-lookup"><span data-stu-id="277df-121">Pointer to the rotation matrix.</span></span> <span data-ttu-id="277df-122">Подматрица вращения должна быть ортогональной с определителем единицы.</span><span class="sxs-lookup"><span data-stu-id="277df-122">The rotation sub-matrix must be orthogonal, with a unit determinant.</span></span>

</dd> <dt>

<span data-ttu-id="277df-123">*закрепить* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="277df-123">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="277df-124">Тип: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="277df-124">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="277df-125">Указатель на повернутые коэффициенты SH.</span><span class="sxs-lookup"><span data-stu-id="277df-125">Pointer to rotated SH coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="277df-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="277df-126">Return value</span></span>

<span data-ttu-id="277df-127">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="277df-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="277df-128">Указатель на коэффициенты вывода SH.</span><span class="sxs-lookup"><span data-stu-id="277df-128">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="277df-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="277df-129">Remarks</span></span>

<span data-ttu-id="277df-130">Каждый коэффициент базисной функции илм хранится в памяти l ² + m + l, где:</span><span class="sxs-lookup"><span data-stu-id="277df-130">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="277df-131">l — это степень базовой функции.</span><span class="sxs-lookup"><span data-stu-id="277df-131">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="277df-132">m — это базовый индекс функции для заданного значения l и диапазон от-l до l включительно.</span><span class="sxs-lookup"><span data-stu-id="277df-132">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="277df-133">Требования</span><span class="sxs-lookup"><span data-stu-id="277df-133">Requirements</span></span>



| <span data-ttu-id="277df-134">Требование</span><span class="sxs-lookup"><span data-stu-id="277df-134">Requirement</span></span> | <span data-ttu-id="277df-135">Значение</span><span class="sxs-lookup"><span data-stu-id="277df-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="277df-136">Header</span><span class="sxs-lookup"><span data-stu-id="277df-136">Header</span></span><br/>  | <dl> <span data-ttu-id="277df-137"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="277df-137"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="277df-138">Библиотека</span><span class="sxs-lookup"><span data-stu-id="277df-138">Library</span></span><br/> | <dl> <span data-ttu-id="277df-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="277df-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="277df-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="277df-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="277df-141">Математические функции</span><span class="sxs-lookup"><span data-stu-id="277df-141">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="277df-142">Предварительно вычисленный перенос Радианце (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="277df-142">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
