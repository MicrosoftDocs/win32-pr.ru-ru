---
description: Выполняет интерполяцию Хермите сплайна, используя указанные трехмерные векторы.
ms.assetid: d2212299-0478-48a6-b303-60c212528058
title: Функция D3DXVec3Hermite (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Hermite
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: b2650bbaf33e5d768ed892bbde31493c8ec0d9d2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703805"
---
# <a name="d3dxvec3hermite-function-d3dx10mathh"></a><span data-ttu-id="a3b68-103">Функция D3DXVec3Hermite (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="a3b68-103">D3DXVec3Hermite function (D3DX10Math.h)</span></span>

<span data-ttu-id="a3b68-104">Выполняет интерполяцию Хермите сплайна, используя указанные трехмерные векторы.</span><span class="sxs-lookup"><span data-stu-id="a3b68-104">Performs a Hermite spline interpolation, using the specified 3D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3b68-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a3b68-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Hermite(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pT1,
  _In_    const D3DXVECTOR3 *pV2,
  _In_    const D3DXVECTOR3 *pT2,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a><span data-ttu-id="a3b68-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a3b68-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3b68-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="a3b68-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a3b68-108">Тип: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="a3b68-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="a3b68-109">Указатель на [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , который является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="a3b68-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="a3b68-110">*pV1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a3b68-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3b68-111">Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="a3b68-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="a3b68-112">Указатель на исходную структуру D3DXVECTOR3, вектор позиции.</span><span class="sxs-lookup"><span data-stu-id="a3b68-112">Pointer to a source D3DXVECTOR3 structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="a3b68-113">*pT1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a3b68-113">*pT1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3b68-114">Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="a3b68-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="a3b68-115">Указатель на исходную структуру D3DXVECTOR3 — вектор касательной.</span><span class="sxs-lookup"><span data-stu-id="a3b68-115">Pointer to a source D3DXVECTOR3 structure, a tangent vector.</span></span>

</dd> <dt>

<span data-ttu-id="a3b68-116">*pV2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a3b68-116">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3b68-117">Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="a3b68-117">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="a3b68-118">Указатель на исходную структуру D3DXVECTOR3, вектор позиции.</span><span class="sxs-lookup"><span data-stu-id="a3b68-118">Pointer to a source D3DXVECTOR3 structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="a3b68-119">*PT2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a3b68-119">*pT2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3b68-120">Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="a3b68-120">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="a3b68-121">Указатель на исходную структуру D3DXVECTOR3 — вектор касательной.</span><span class="sxs-lookup"><span data-stu-id="a3b68-121">Pointer to a source D3DXVECTOR3 structure, a tangent vector.</span></span>

</dd> <dt>

<span data-ttu-id="a3b68-122">*s* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="a3b68-122">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3b68-123">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a3b68-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a3b68-124">Весовой коэффициент.</span><span class="sxs-lookup"><span data-stu-id="a3b68-124">Weighting factor.</span></span> <span data-ttu-id="a3b68-125">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="a3b68-125">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3b68-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a3b68-126">Return value</span></span>

<span data-ttu-id="a3b68-127">Тип: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="a3b68-127">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="a3b68-128">Указатель на структуру D3DXVECTOR3, которая является результатом интерполяции Хермите сплайна.</span><span class="sxs-lookup"><span data-stu-id="a3b68-128">Pointer to a D3DXVECTOR3 structure that is the result of the Hermite spline interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3b68-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a3b68-129">Remarks</span></span>

<span data-ttu-id="a3b68-130">Функция **D3DXVec3Hermite** выполняет интерполяцию от (позиционирован, тангенс) к (Поситионб, танжентб) с помощью интерполяции хермите сплайна.</span><span class="sxs-lookup"><span data-stu-id="a3b68-130">The **D3DXVec3Hermite** function interpolates from (positionA, tangentA) to (positionB, tangentB) using Hermite spline interpolation.</span></span>

<span data-ttu-id="a3b68-131">Интерполяция сплайна — это обобщение простого и упрощенного сплайна.</span><span class="sxs-lookup"><span data-stu-id="a3b68-131">The spline interpolation is a generalization of the ease-in, ease-out spline.</span></span> <span data-ttu-id="a3b68-132">Пандус — это функция Q (s) со следующими свойствами.</span><span class="sxs-lookup"><span data-stu-id="a3b68-132">The ramp is a function of Q(s) with the following properties.</span></span>

<span data-ttu-id="a3b68-133">Q (s) = AS ³ + BS ² + CS + D (и, следовательно, Q "(s) = 3As ² + 2Bs + C)</span><span class="sxs-lookup"><span data-stu-id="a3b68-133">Q(s) = As³ + Bs² + Cs + D (and therefore, Q'(s) = 3As² + 2Bs + C)</span></span>

<span data-ttu-id="a3b68-134">a) Q (0) = v1, т. е. Q ' (0) = T1</span><span class="sxs-lookup"><span data-stu-id="a3b68-134">a) Q(0) = v1, so Q'(0) = t1</span></span>

<span data-ttu-id="a3b68-135">б) Q (1) = v2, so Q ' (1) = T2</span><span class="sxs-lookup"><span data-stu-id="a3b68-135">b) Q(1) = v2, so Q'(1) = t2</span></span>

<span data-ttu-id="a3b68-136">v1 — это содержимое pV1, v2 в содержимом pV2, T1 — это содержимое pT1, а T2 — содержимое pT2.</span><span class="sxs-lookup"><span data-stu-id="a3b68-136">v1 is the contents of pV1, v2 in the contents of pV2, t1 is the contents of pT1, and t2 is the contents of pT2.</span></span>

<span data-ttu-id="a3b68-137">Эти свойства используются для решения для A, B, C, D.</span><span class="sxs-lookup"><span data-stu-id="a3b68-137">These properties are used to solve for A, B, C, D.</span></span>


```
D = v1  (from a)
C = t1  (from a)
3A + 2B = t2 - t1 (substituting for C)
A + B = v2 - v1 - t1 (substituting for C and D)
```



<span data-ttu-id="a3b68-138">Подключайте решения для A, B, C и D, чтобы создать Q (ы).</span><span class="sxs-lookup"><span data-stu-id="a3b68-138">Plug in the solutions for A,B,C and D to generate Q(s).</span></span>


```
A = 2v1 - 2v2 + t2 + t1 
B = 3v2 - 3v1 - 2t1 - t2
C = t1 
D = v1
```



<span data-ttu-id="a3b68-139">Мы получаем такой результат:</span><span class="sxs-lookup"><span data-stu-id="a3b68-139">This yields:</span></span>

<span data-ttu-id="a3b68-140">Q (s) = (2V1-2v2 + T2 + T1) s ³ + (3V2-3v1-2T1-T2) s ² + t1s + v1</span><span class="sxs-lookup"><span data-stu-id="a3b68-140">Q(s) = (2v1 - 2v2 + t2 + t1)s³ + (3v2 - 3v1 - 2t1 - t2)s² + t1s + v1</span></span>

<span data-ttu-id="a3b68-141">Который можно изменить следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a3b68-141">Which can be rearranged as:</span></span>

<span data-ttu-id="a3b68-142">Q (s) = (2S ³-3S ² + 1) v1 + (-2S ³ + 3S ²) v2 + (s ³-2S ² + s) T1 + (s ³-s ²) T2</span><span class="sxs-lookup"><span data-stu-id="a3b68-142">Q(s) = (2s³ - 3s² + 1)v1 + (-2s³ + 3s²)v2 + (s³ - 2s² + s)t1 + (s³ - s²)t2</span></span>

<span data-ttu-id="a3b68-143">Хермитеные сплайны полезны для управления анимацией, так как кривая выполняется через все контрольные точки.</span><span class="sxs-lookup"><span data-stu-id="a3b68-143">Hermite splines are useful for controlling animation because the curve runs through all the control points.</span></span> <span data-ttu-id="a3b68-144">Кроме того, поскольку позиция и тангенс явно указываются на концах каждого сегмента, можно легко создать непрерывную кривую C2, пока вы убедитесь, что начальная позиция и тангенс соответствуют конечным значениям последнего сегмента.</span><span class="sxs-lookup"><span data-stu-id="a3b68-144">Also, because the position and tangent are explicitly specified at the ends of each segment, it is easy to create a C2 continuous curve as long as you make sure that your starting position and tangent match the ending values of the last segment.</span></span>

<span data-ttu-id="a3b68-145">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="a3b68-145">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="a3b68-146">Таким образом, функция **D3DXVec3Hermite** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="a3b68-146">In this way, the **D3DXVec3Hermite** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3b68-147">Требования</span><span class="sxs-lookup"><span data-stu-id="a3b68-147">Requirements</span></span>



| <span data-ttu-id="a3b68-148">Требование</span><span class="sxs-lookup"><span data-stu-id="a3b68-148">Requirement</span></span> | <span data-ttu-id="a3b68-149">Значение</span><span class="sxs-lookup"><span data-stu-id="a3b68-149">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a3b68-150">Header</span><span class="sxs-lookup"><span data-stu-id="a3b68-150">Header</span></span><br/> | <dl> <span data-ttu-id="a3b68-151"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3b68-151"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3b68-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a3b68-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3b68-153">Математические функции</span><span class="sxs-lookup"><span data-stu-id="a3b68-153">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
