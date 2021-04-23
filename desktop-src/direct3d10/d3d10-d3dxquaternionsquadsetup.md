---
description: Настраивает контрольные точки для сферической куадрангле интерполяции.
ms.assetid: c66227bd-8cc1-4173-9dc2-5aab9d57301e
title: Функция D3DXQuaternionSquadSetup (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionSquadSetup
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4a0683bce3642b0300e68be348d8aed39b3c333d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703933"
---
# <a name="d3dxquaternionsquadsetup-function-d3dx10mathh"></a><span data-ttu-id="e8058-103">Функция D3DXQuaternionSquadSetup (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="e8058-103">D3DXQuaternionSquadSetup function (D3DX10Math.h)</span></span>

<span data-ttu-id="e8058-104">Настраивает контрольные точки для сферической куадрангле интерполяции.</span><span class="sxs-lookup"><span data-stu-id="e8058-104">Sets up control points for spherical quadrangle interpolation.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8058-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e8058-105">Syntax</span></span>


```C++
void D3DXQuaternionSquadSetup(
  _In_       D3DXQUATERNION *pAOut,
  _In_       D3DXQUATERNION *pBOut,
  _In_       D3DXQUATERNION *pCOut,
  _In_ const D3DXQUATERNION *pQ0,
  _In_ const D3DXQUATERNION *pQ1,
  _In_ const D3DXQUATERNION *pQ2,
  _In_ const D3DXQUATERNION *pQ3
);
```



## <a name="parameters"></a><span data-ttu-id="e8058-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e8058-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8058-107">*пааут* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e8058-107">*pAOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8058-108">Тип: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="e8058-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="e8058-109">Указатель на Ааут.</span><span class="sxs-lookup"><span data-stu-id="e8058-109">Pointer to AOut.</span></span>

</dd> <dt>

<span data-ttu-id="e8058-110">*пбаут* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e8058-110">*pBOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8058-111">Тип: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="e8058-111">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="e8058-112">Указатель на грамме.</span><span class="sxs-lookup"><span data-stu-id="e8058-112">Pointer to BOut.</span></span>

</dd> <dt>

<span data-ttu-id="e8058-113">*пкаут* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e8058-113">*pCOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8058-114">Тип: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="e8058-114">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="e8058-115">Указатель на COut.</span><span class="sxs-lookup"><span data-stu-id="e8058-115">Pointer to COut.</span></span>

</dd> <dt>

<span data-ttu-id="e8058-116">*pQ0* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e8058-116">*pQ0* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8058-117">Тип: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="e8058-117">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="e8058-118">Указатель на входную точку управления Q0.</span><span class="sxs-lookup"><span data-stu-id="e8058-118">Pointer to the input control point, Q0.</span></span>

</dd> <dt>

<span data-ttu-id="e8058-119">*pQ1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e8058-119">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8058-120">Тип: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="e8058-120">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="e8058-121">Указатель на точку управления ввода, Q1.</span><span class="sxs-lookup"><span data-stu-id="e8058-121">Pointer to the input control point, Q1.</span></span>

</dd> <dt>

<span data-ttu-id="e8058-122">*pQ2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e8058-122">*pQ2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8058-123">Тип: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="e8058-123">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="e8058-124">Указатель на точку управления ввода, Q2.</span><span class="sxs-lookup"><span data-stu-id="e8058-124">Pointer to the input control point, Q2.</span></span>

</dd> <dt>

<span data-ttu-id="e8058-125">*pQ3* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e8058-125">*pQ3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8058-126">Тип: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="e8058-126">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="e8058-127">Указатель на точку управления ввода, Q3.</span><span class="sxs-lookup"><span data-stu-id="e8058-127">Pointer to the input control point, Q3.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8058-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e8058-128">Return value</span></span>

<span data-ttu-id="e8058-129">Нет.</span><span class="sxs-lookup"><span data-stu-id="e8058-129">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8058-130">Remarks</span><span class="sxs-lookup"><span data-stu-id="e8058-130">Remarks</span></span>

<span data-ttu-id="e8058-131">Эта функция принимает четыре контрольные точки, которые предоставляются входным данным pQ0, pQ1, pQ2 и pQ3.</span><span class="sxs-lookup"><span data-stu-id="e8058-131">This function takes four control points, which are supplied to the inputs pQ0, pQ1, pQ2, and pQ3.</span></span> <span data-ttu-id="e8058-132">Затем функция изменяет эти значения, чтобы найти кривую, которая проходит вдоль кратчайшего пути.</span><span class="sxs-lookup"><span data-stu-id="e8058-132">The function then alters these values to find a curve that flows along the shortest path.</span></span> <span data-ttu-id="e8058-133">Значения Q0, Q2 и Q3 рассчитываются, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="e8058-133">The values of q0, q2, and q3 are calculated as shown below.</span></span>


```
q0 = |Q0 + Q1| < |Q0 - Q1| ? -Q0 : Q0
q2 = |Q1 + Q2| < |Q1 - Q2| ? -Q2 : Q2
q3 = |Q2 + Q3| < |Q2 - Q3| ? -Q3 : Q3
```



<span data-ttu-id="e8058-134">После вычисления новых значений Q значения для Ааут, грамме и COut рассчитываются следующим образом:</span><span class="sxs-lookup"><span data-stu-id="e8058-134">Having calculated the new Q values, the values for AOut, BOut, and COut are calculated as follows:</span></span>

<span data-ttu-id="e8058-135">Ааут = Q1 \* e<sup> \[ -0,25 \ \* (\ LN \[ exp (Q1) \* Q2 \] \ + \ LN \[ exp (Q1) \* Q0 \] \) \ \] </sup></span><span class="sxs-lookup"><span data-stu-id="e8058-135">AOut = q1 \* e<sup>\[-0.25\ \*(\ Ln\[Exp(q1)\*q2\]\ +\ Ln\[Exp(q1)\*q0\]\ )\ \]</sup></span></span>

<span data-ttu-id="e8058-136">Грамме = Q2 \* e<sup> \[ -0,25 \ \* (\ LN \[ exp (Q2) \* Q3 \] \ + \ LN \[ exp (Q2) \* Q1 \] \) \ \] </sup></span><span class="sxs-lookup"><span data-stu-id="e8058-136">BOut = q2 \* e<sup>\[-0.25\ \*(\ Ln\[Exp(q2)\*q3\]\ +\ Ln\[Exp(q2)\*q1\]\ )\ \]</sup></span></span>

<span data-ttu-id="e8058-137">COut = Q2</span><span class="sxs-lookup"><span data-stu-id="e8058-137">COut = q2</span></span>

> [!Note]  
> <span data-ttu-id="e8058-138">LN — это метод API [**D3DXQuaternionLn**](d3d10-d3dxquaternionln.md) , а exp — метод API [**D3DXQuaternionExp**](d3d10-d3dxquaternionexp.md).</span><span class="sxs-lookup"><span data-stu-id="e8058-138">Ln is the API method [**D3DXQuaternionLn**](d3d10-d3dxquaternionln.md) and Exp is the API method [**D3DXQuaternionExp**](d3d10-d3dxquaternionexp.md).</span></span>

 

<span data-ttu-id="e8058-139">Используйте [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) для любых входных данных кватернион, которые еще не нормализованы.</span><span class="sxs-lookup"><span data-stu-id="e8058-139">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

### <a name="examples"></a><span data-ttu-id="e8058-140">Примеры</span><span class="sxs-lookup"><span data-stu-id="e8058-140">Examples</span></span>

<span data-ttu-id="e8058-141">В следующем примере показано, как использовать набор ключей кватернион (q0, Q1, Q2, Q3) для расчета внутренних точек куадрангле (A, B, C).</span><span class="sxs-lookup"><span data-stu-id="e8058-141">The following example shows how to use a set of quaternion keys (Q0, Q1, Q2, Q3) to compute the inner quadrangle points (A, B, C).</span></span> <span data-ttu-id="e8058-142">Это гарантирует непрерывность касательных между смежными сегментами.</span><span class="sxs-lookup"><span data-stu-id="e8058-142">This ensures that the tangents are continuous across adjacent segments.</span></span>


```
      A     B
Q0    Q1    Q2    Q3
```



<span data-ttu-id="e8058-143">В следующем примере кода показано, как можно выполнить интерполяцию между Q1 и Q2.</span><span class="sxs-lookup"><span data-stu-id="e8058-143">The following code example demonstrates how you can interpolate between Q1 and Q2.</span></span>


```
// Rotation about the z-axis
D3DXQUATERNION Q0 = D3DXQUATERNION(0,  0, 0.707f, -.707f);
D3DXQUATERNION Q1 = D3DXQUATERNION(0,  0, 0.000f, 1.000f);
D3DXQUATERNION Q2 = D3DXQUATERNION(0,  0, 0.707f, 0.707f);
D3DXQUATERNION Q3 = D3DXQUATERNION(0,  0, 1.000f, 0.000f);
D3DXQUATERNION A, B, C, Qt;
FLOAT time = 0.5f;

D3DXQuaternionSquadSetup(&A, &B, &C, &Q0, &Q1, &Q2, &Q3);
D3DXQuaternionSquad(&Qt, &Q1, &A, &B, &C, time);
```



> [!Note]
>
> -   <span data-ttu-id="e8058-144">C — это +/-Q2 в зависимости от результата функции.</span><span class="sxs-lookup"><span data-stu-id="e8058-144">C is +/- Q2 depending on the result of the function.</span></span>
> -   <span data-ttu-id="e8058-145">Qt является результатом функции.</span><span class="sxs-lookup"><span data-stu-id="e8058-145">Qt is the result of the function.</span></span>
>
> <span data-ttu-id="e8058-146">Результатом является поворот на 45 градусов вокруг оси z для времени = 0,5.</span><span class="sxs-lookup"><span data-stu-id="e8058-146">The result is a rotation of 45 degrees around the z-axis for time = 0.5.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e8058-147">Требования</span><span class="sxs-lookup"><span data-stu-id="e8058-147">Requirements</span></span>



| <span data-ttu-id="e8058-148">Требование</span><span class="sxs-lookup"><span data-stu-id="e8058-148">Requirement</span></span> | <span data-ttu-id="e8058-149">Значение</span><span class="sxs-lookup"><span data-stu-id="e8058-149">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e8058-150">Header</span><span class="sxs-lookup"><span data-stu-id="e8058-150">Header</span></span><br/>  | <dl> <span data-ttu-id="e8058-151"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8058-151"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="e8058-152">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e8058-152">Library</span></span><br/> | <dl> <span data-ttu-id="e8058-153"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e8058-153"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e8058-154">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e8058-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8058-155">Математические функции</span><span class="sxs-lookup"><span data-stu-id="e8058-155">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
