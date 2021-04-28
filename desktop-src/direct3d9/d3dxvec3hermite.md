---
description: Функция D3DXVec3Hermite (D3dx9math. h) — выполняет интерполяцию Хермите сплайна, используя указанные трехмерные векторы.
ms.assetid: d45b1179-0e11-4f58-8d50-432236cb88ca
title: Функция D3DXVec3Hermite (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Hermite
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fd45851108d3700446a2b7f27aa00a4cc61ca39b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097872"
---
# <a name="d3dxvec3hermite-function-d3dx9mathh"></a><span data-ttu-id="7a736-103">Функция D3DXVec3Hermite (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="7a736-103">D3DXVec3Hermite function (D3dx9math.h)</span></span>

<span data-ttu-id="7a736-104">Выполняет интерполяцию Хермите сплайна, используя указанные трехмерные векторы.</span><span class="sxs-lookup"><span data-stu-id="7a736-104">Performs a Hermite spline interpolation, using the specified 3D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a736-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7a736-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="7a736-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7a736-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a736-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="7a736-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7a736-108">Тип: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="7a736-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="7a736-109">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="7a736-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="7a736-110">*pV1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7a736-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a736-111">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="7a736-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="7a736-112">Указатель на исходную структуру [**D3DXVECTOR3**](d3dxvector3.md) , вектор позиции.</span><span class="sxs-lookup"><span data-stu-id="7a736-112">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="7a736-113">*pT1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7a736-113">*pT1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a736-114">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="7a736-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="7a736-115">Указатель на исходную структуру [**D3DXVECTOR3**](d3dxvector3.md) — вектор касательной.</span><span class="sxs-lookup"><span data-stu-id="7a736-115">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure, a tangent vector.</span></span>

</dd> <dt>

<span data-ttu-id="7a736-116">*pV2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7a736-116">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a736-117">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="7a736-117">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="7a736-118">Указатель на исходную структуру [**D3DXVECTOR3**](d3dxvector3.md) , вектор позиции.</span><span class="sxs-lookup"><span data-stu-id="7a736-118">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="7a736-119">*PT2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7a736-119">*pT2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a736-120">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="7a736-120">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="7a736-121">Указатель на исходную структуру [**D3DXVECTOR3**](d3dxvector3.md) — вектор касательной.</span><span class="sxs-lookup"><span data-stu-id="7a736-121">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure, a tangent vector.</span></span>

</dd> <dt>

<span data-ttu-id="7a736-122">*s* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="7a736-122">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a736-123">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7a736-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7a736-124">Весовой коэффициент.</span><span class="sxs-lookup"><span data-stu-id="7a736-124">Weighting factor.</span></span> <span data-ttu-id="7a736-125">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="7a736-125">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a736-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7a736-126">Return value</span></span>

<span data-ttu-id="7a736-127">Тип: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="7a736-127">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="7a736-128">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , которая является результатом интерполяции хермите сплайна.</span><span class="sxs-lookup"><span data-stu-id="7a736-128">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the Hermite spline interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a736-129">Remarks</span><span class="sxs-lookup"><span data-stu-id="7a736-129">Remarks</span></span>

<span data-ttu-id="7a736-130">Функция **D3DXVec3Hermite** выполняет интерполяцию от (позиционирован, тангенс) к (Поситионб, танжентб) с помощью интерполяции хермите сплайна.</span><span class="sxs-lookup"><span data-stu-id="7a736-130">The **D3DXVec3Hermite** function interpolates from (positionA, tangentA) to (positionB, tangentB) using Hermite spline interpolation.</span></span>

<span data-ttu-id="7a736-131">Интерполяция сплайна — это обобщение простого и упрощенного сплайна.</span><span class="sxs-lookup"><span data-stu-id="7a736-131">The spline interpolation is a generalization of the ease-in, ease-out spline.</span></span> <span data-ttu-id="7a736-132">Пандус — это функция Q (s) со следующими свойствами.</span><span class="sxs-lookup"><span data-stu-id="7a736-132">The ramp is a function of Q(s) with the following properties.</span></span>

<span data-ttu-id="7a736-133">Q (s) = AS ³ + BS ² + CS + D (и, следовательно, Q "(s) = 3As ² + 2Bs + C)</span><span class="sxs-lookup"><span data-stu-id="7a736-133">Q(s) = As³ + Bs² + Cs + D (and therefore, Q'(s) = 3As² + 2Bs + C)</span></span>

<span data-ttu-id="7a736-134">a) Q (0) = v1, т. е. Q ' (0) = T1</span><span class="sxs-lookup"><span data-stu-id="7a736-134">a) Q(0) = v1, so Q'(0) = t1</span></span>

<span data-ttu-id="7a736-135">б) Q (1) = v2, so Q ' (1) = T2</span><span class="sxs-lookup"><span data-stu-id="7a736-135">b) Q(1) = v2, so Q'(1) = t2</span></span>

<span data-ttu-id="7a736-136">v1 — это содержимое pV1, v2 в содержимом pV2, T1 — это содержимое pT1, а T2 — содержимое pT2.</span><span class="sxs-lookup"><span data-stu-id="7a736-136">v1 is the contents of pV1, v2 in the contents of pV2, t1 is the contents of pT1, and t2 is the contents of pT2.</span></span>

<span data-ttu-id="7a736-137">Эти свойства используются для решения для A, B, C, D.</span><span class="sxs-lookup"><span data-stu-id="7a736-137">These properties are used to solve for A, B, C, D.</span></span>

``` syntax
D = v1  (from a)
C = t1  (from a)
3A + 2B = t2 - t1 (substituting for C)
A + B = v2 - v1 - t1 (substituting for C and D)
```

<span data-ttu-id="7a736-138">Подключайте решения для A, B, C и D, чтобы создать Q (ы).</span><span class="sxs-lookup"><span data-stu-id="7a736-138">Plug in the solutions for A,B,C and D to generate Q(s).</span></span>

``` syntax
A = 2v1 - 2v2 + t2 + t1 
B = 3v2 - 3v1 - 2t1 - t2
C = t1 
D = v1
```

<span data-ttu-id="7a736-139">Мы получаем такой результат:</span><span class="sxs-lookup"><span data-stu-id="7a736-139">This yields:</span></span>

<span data-ttu-id="7a736-140">Q (s) = (2V1-2v2 + T2 + T1) s ³ + (3V2-3v1-2T1-T2) s ² + t1s + v1</span><span class="sxs-lookup"><span data-stu-id="7a736-140">Q(s) = (2v1 - 2v2 + t2 + t1)s³ + (3v2 - 3v1 - 2t1 - t2)s² + t1s + v1</span></span>

<span data-ttu-id="7a736-141">Который можно изменить следующим образом:</span><span class="sxs-lookup"><span data-stu-id="7a736-141">Which can be rearranged as:</span></span>

<span data-ttu-id="7a736-142">Q (s) = (2S ³-3S ² + 1) v1 + (-2S ³ + 3S ²) v2 + (s ³-2S ² + s) T1 + (s ³-s ²) T2</span><span class="sxs-lookup"><span data-stu-id="7a736-142">Q(s) = (2s³ - 3s² + 1)v1 + (-2s³ + 3s²)v2 + (s³ - 2s² + s)t1 + (s³ - s²)t2</span></span>

<span data-ttu-id="7a736-143">Хермитеные сплайны полезны для управления анимацией, так как кривая выполняется через все контрольные точки.</span><span class="sxs-lookup"><span data-stu-id="7a736-143">Hermite splines are useful for controlling animation because the curve runs through all the control points.</span></span> <span data-ttu-id="7a736-144">Кроме того, поскольку позиция и тангенс явно указываются на концах каждого сегмента, можно легко создать непрерывную кривую C2, пока вы убедитесь, что начальная позиция и тангенс соответствуют конечным значениям последнего сегмента.</span><span class="sxs-lookup"><span data-stu-id="7a736-144">Also, because the position and tangent are explicitly specified at the ends of each segment, it is easy to create a C2 continuous curve as long as you make sure that your starting position and tangent match the ending values of the last segment.</span></span>

<span data-ttu-id="7a736-145">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="7a736-145">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="7a736-146">Таким образом, функция **D3DXVec3Hermite** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="7a736-146">In this way, the **D3DXVec3Hermite** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a736-147">Требования</span><span class="sxs-lookup"><span data-stu-id="7a736-147">Requirements</span></span>



| <span data-ttu-id="7a736-148">Требование</span><span class="sxs-lookup"><span data-stu-id="7a736-148">Requirement</span></span> | <span data-ttu-id="7a736-149">Значение</span><span class="sxs-lookup"><span data-stu-id="7a736-149">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7a736-150">Header</span><span class="sxs-lookup"><span data-stu-id="7a736-150">Header</span></span><br/>  | <dl> <span data-ttu-id="7a736-151"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a736-151"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="7a736-152">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7a736-152">Library</span></span><br/> | <dl> <span data-ttu-id="7a736-153"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7a736-153"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7a736-154">См. также</span><span class="sxs-lookup"><span data-stu-id="7a736-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a736-155">Математические функции</span><span class="sxs-lookup"><span data-stu-id="7a736-155">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
