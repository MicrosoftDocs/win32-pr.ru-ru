---
description: Настраивает контрольные точки для сферической куадрангле интерполяции.
ms.assetid: f800d457-8546-49a1-800e-e5c27af96710
title: Функция D3DXQuaternionSquadSetup (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 04bae9dafbb9df90fdcccee830a1eecb64c1430f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713616"
---
# <a name="d3dxquaternionsquadsetup-function-d3dx9mathh"></a><span data-ttu-id="d8f2f-103">Функция D3DXQuaternionSquadSetup (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="d8f2f-103">D3DXQuaternionSquadSetup function (D3dx9math.h)</span></span>

<span data-ttu-id="d8f2f-104">Настраивает контрольные точки для сферической куадрангле интерполяции.</span><span class="sxs-lookup"><span data-stu-id="d8f2f-104">Sets up control points for spherical quadrangle interpolation.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8f2f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d8f2f-105">Syntax</span></span>


```C++
void D3DXQuaternionSquadSetup(
  _Out_       D3DXQUATERNION *pAOut,
  _Out_       D3DXQUATERNION *pBOut,
  _Out_       D3DXQUATERNION *pCOut,
  _In_  const D3DXQUATERNION *pQ0,
  _In_  const D3DXQUATERNION *pQ1,
  _In_  const D3DXQUATERNION *pQ2,
  _In_  const D3DXQUATERNION *pQ3
);
```



## <a name="parameters"></a><span data-ttu-id="d8f2f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d8f2f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8f2f-107">*пааут* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d8f2f-107">*pAOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d8f2f-108">Тип: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="d8f2f-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="d8f2f-109">Указатель на Ааут.</span><span class="sxs-lookup"><span data-stu-id="d8f2f-109">Pointer to AOut.</span></span>

</dd> <dt>

<span data-ttu-id="d8f2f-110">*пбаут* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d8f2f-110">*pBOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d8f2f-111">Тип: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="d8f2f-111">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="d8f2f-112">Указатель на грамме.</span><span class="sxs-lookup"><span data-stu-id="d8f2f-112">Pointer to BOut.</span></span>

</dd> <dt>

<span data-ttu-id="d8f2f-113">*пкаут* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d8f2f-113">*pCOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d8f2f-114">Тип: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="d8f2f-114">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="d8f2f-115">Указатель на COut.</span><span class="sxs-lookup"><span data-stu-id="d8f2f-115">Pointer to COut.</span></span>

</dd> <dt>

<span data-ttu-id="d8f2f-116">*pQ0* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d8f2f-116">*pQ0* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8f2f-117">Тип: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="d8f2f-117">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="d8f2f-118">Указатель на входную точку управления Q0.</span><span class="sxs-lookup"><span data-stu-id="d8f2f-118">Pointer to the input control point, Q0.</span></span>

</dd> <dt>

<span data-ttu-id="d8f2f-119">*pQ1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d8f2f-119">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8f2f-120">Тип: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="d8f2f-120">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="d8f2f-121">Указатель на точку управления ввода, Q1.</span><span class="sxs-lookup"><span data-stu-id="d8f2f-121">Pointer to the input control point, Q1.</span></span>

</dd> <dt>

<span data-ttu-id="d8f2f-122">*pQ2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d8f2f-122">*pQ2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8f2f-123">Тип: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="d8f2f-123">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="d8f2f-124">Указатель на точку управления ввода, Q2.</span><span class="sxs-lookup"><span data-stu-id="d8f2f-124">Pointer to the input control point, Q2.</span></span>

</dd> <dt>

<span data-ttu-id="d8f2f-125">*pQ3* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d8f2f-125">*pQ3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8f2f-126">Тип: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="d8f2f-126">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="d8f2f-127">Указатель на точку управления ввода, Q3.</span><span class="sxs-lookup"><span data-stu-id="d8f2f-127">Pointer to the input control point, Q3.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8f2f-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d8f2f-128">Return value</span></span>

<span data-ttu-id="d8f2f-129">Нет.</span><span class="sxs-lookup"><span data-stu-id="d8f2f-129">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8f2f-130">Remarks</span><span class="sxs-lookup"><span data-stu-id="d8f2f-130">Remarks</span></span>

<span data-ttu-id="d8f2f-131">Эта функция принимает четыре контрольные точки, которые предоставляются входным данным pQ0, pQ1, pQ2 и pQ3.</span><span class="sxs-lookup"><span data-stu-id="d8f2f-131">This function takes four control points, which are supplied to the inputs pQ0, pQ1, pQ2, and pQ3.</span></span> <span data-ttu-id="d8f2f-132">Затем функция изменяет эти значения, чтобы найти кривую, которая проходит вдоль кратчайшего пути.</span><span class="sxs-lookup"><span data-stu-id="d8f2f-132">The function then alters these values to find a curve that flows along the shortest path.</span></span> <span data-ttu-id="d8f2f-133">Значения Q0, Q2 и Q3 рассчитываются, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="d8f2f-133">The values of q0, q2, and q3 are calculated as shown below.</span></span>


```
q0 = |Q0 + Q1| < |Q0 - Q1| ? -Q0 : Q0
q2 = |Q1 + Q2| < |Q1 - Q2| ? -Q2 : Q2
q3 = |Q2 + Q3| < |Q2 - Q3| ? -Q3 : Q3
```



<span data-ttu-id="d8f2f-134">После вычисления новых значений Q значения для Ааут, грамме и COut рассчитываются следующим образом:</span><span class="sxs-lookup"><span data-stu-id="d8f2f-134">Having calculated the new Q values, the values for AOut, BOut, and COut are calculated as follows:</span></span>

<span data-ttu-id="d8f2f-135">Ааут = Q1 \* e<sup> \[ -0,25 \ \* (\ LN \[ exp (Q1) \* Q2 \] \ + \ LN \[ exp (Q1) \* Q0 \] \) \ \] </sup></span><span class="sxs-lookup"><span data-stu-id="d8f2f-135">AOut = q1 \* e<sup>\[-0.25\ \*(\ Ln\[Exp(q1)\*q2\]\ +\ Ln\[Exp(q1)\*q0\]\ )\ \]</sup></span></span>

<span data-ttu-id="d8f2f-136">Грамме = Q2 \* e<sup> \[ -0,25 \ \* (\ LN \[ exp (Q2) \* Q3 \] \ + \ LN \[ exp (Q2) \* Q1 \] \) \ \] </sup></span><span class="sxs-lookup"><span data-stu-id="d8f2f-136">BOut = q2 \* e<sup>\[-0.25\ \*(\ Ln\[Exp(q2)\*q3\]\ +\ Ln\[Exp(q2)\*q1\]\ )\ \]</sup></span></span>

<span data-ttu-id="d8f2f-137">COut = Q2</span><span class="sxs-lookup"><span data-stu-id="d8f2f-137">COut = q2</span></span>

> [!Note]  
> <span data-ttu-id="d8f2f-138">LN — это метод API [**D3DXQuaternionLn**](d3dxquaternionln.md) , а exp — метод API [**D3DXQuaternionExp**](d3dxquaternionexp.md).</span><span class="sxs-lookup"><span data-stu-id="d8f2f-138">Ln is the API method [**D3DXQuaternionLn**](d3dxquaternionln.md) and Exp is the API method [**D3DXQuaternionExp**](d3dxquaternionexp.md).</span></span>

 

<span data-ttu-id="d8f2f-139">Используйте [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) для любых входных данных кватернион, которые еще не нормализованы.</span><span class="sxs-lookup"><span data-stu-id="d8f2f-139">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

### <a name="examples"></a><span data-ttu-id="d8f2f-140">Примеры</span><span class="sxs-lookup"><span data-stu-id="d8f2f-140">Examples</span></span>

<span data-ttu-id="d8f2f-141">В следующем примере показано, как использовать набор ключей кватернион (q0, Q1, Q2, Q3) для расчета внутренних точек куадрангле (A, B, C).</span><span class="sxs-lookup"><span data-stu-id="d8f2f-141">The following example shows how to use a set of quaternion keys (Q0, Q1, Q2, Q3) to compute the inner quadrangle points (A, B, C).</span></span> <span data-ttu-id="d8f2f-142">Это гарантирует непрерывность касательных между смежными сегментами.</span><span class="sxs-lookup"><span data-stu-id="d8f2f-142">This ensures that the tangents are continuous across adjacent segments.</span></span>


```
      A     B
Q0    Q1    Q2    Q3
```



<span data-ttu-id="d8f2f-143">В следующем примере кода показано, как можно выполнить интерполяцию между Q1 и Q2.</span><span class="sxs-lookup"><span data-stu-id="d8f2f-143">The following code example demonstrates how you can interpolate between Q1 and Q2.</span></span>


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
> -   <span data-ttu-id="d8f2f-144">C — это +/-Q2 в зависимости от результата функции.</span><span class="sxs-lookup"><span data-stu-id="d8f2f-144">C is +/- Q2 depending on the result of the function.</span></span>
> -   <span data-ttu-id="d8f2f-145">Qt является результатом функции.</span><span class="sxs-lookup"><span data-stu-id="d8f2f-145">Qt is the result of the function.</span></span>
>
> <span data-ttu-id="d8f2f-146">Результатом является поворот на 45 градусов вокруг оси z для времени = 0,5.</span><span class="sxs-lookup"><span data-stu-id="d8f2f-146">The result is a rotation of 45 degrees around the z-axis for time = 0.5.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d8f2f-147">Требования</span><span class="sxs-lookup"><span data-stu-id="d8f2f-147">Requirements</span></span>



| <span data-ttu-id="d8f2f-148">Требование</span><span class="sxs-lookup"><span data-stu-id="d8f2f-148">Requirement</span></span> | <span data-ttu-id="d8f2f-149">Значение</span><span class="sxs-lookup"><span data-stu-id="d8f2f-149">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d8f2f-150">Header</span><span class="sxs-lookup"><span data-stu-id="d8f2f-150">Header</span></span><br/>  | <dl> <span data-ttu-id="d8f2f-151"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8f2f-151"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="d8f2f-152">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d8f2f-152">Library</span></span><br/> | <dl> <span data-ttu-id="d8f2f-153"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d8f2f-153"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d8f2f-154">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d8f2f-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8f2f-155">Математические функции</span><span class="sxs-lookup"><span data-stu-id="d8f2f-155">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="d8f2f-156">**D3DXQuaternionSquad**</span><span class="sxs-lookup"><span data-stu-id="d8f2f-156">**D3DXQuaternionSquad**</span></span>](d3dxquaternionsquad.md)
</dt> </dl>

 

 




