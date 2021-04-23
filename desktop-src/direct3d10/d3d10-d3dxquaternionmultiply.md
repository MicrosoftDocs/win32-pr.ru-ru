---
description: Умножает два кватерниона.
ms.assetid: f549e383-9c39-47a9-84e4-82365bdf1155
title: Функция D3DXQuaternionMultiply (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionMultiply
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 74e10117bf27d922480418e5aa0b8ea60a13528c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105674753"
---
# <a name="d3dxquaternionmultiply-function-d3dx10mathh"></a><span data-ttu-id="2e2a9-103">Функция D3DXQuaternionMultiply (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="2e2a9-103">D3DXQuaternionMultiply function (D3DX10Math.h)</span></span>

<span data-ttu-id="2e2a9-104">Умножает два кватерниона.</span><span class="sxs-lookup"><span data-stu-id="2e2a9-104">Multiplies two quaternions.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e2a9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2e2a9-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionMultiply(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pQ2
);
```



## <a name="parameters"></a><span data-ttu-id="2e2a9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2e2a9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e2a9-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="2e2a9-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2e2a9-108">Тип: **[ **D3DXQUATERNION**](d3d10-d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="2e2a9-108">Type: **[**D3DXQUATERNION**](d3d10-d3dxquaternion.md)\***</span></span>

<span data-ttu-id="2e2a9-109">Указатель на [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) , который является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="2e2a9-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="2e2a9-110">*pQ1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2e2a9-110">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e2a9-111">Тип: **const [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="2e2a9-111">Type: **const [**D3DXQUATERNION**](d3d10-d3dxquaternion.md)\***</span></span>

<span data-ttu-id="2e2a9-112">Указатель на исходную структуру [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) .</span><span class="sxs-lookup"><span data-stu-id="2e2a9-112">Pointer to a source [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="2e2a9-113">*pQ2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2e2a9-113">*pQ2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e2a9-114">Тип: **const [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="2e2a9-114">Type: **const [**D3DXQUATERNION**](d3d10-d3dxquaternion.md)\***</span></span>

<span data-ttu-id="2e2a9-115">Указатель на исходную структуру [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) .</span><span class="sxs-lookup"><span data-stu-id="2e2a9-115">Pointer to a source [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e2a9-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2e2a9-116">Return value</span></span>

<span data-ttu-id="2e2a9-117">Тип: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="2e2a9-117">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="2e2a9-118">Указатель на структуру [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) , которая является произведением двух кватернионов.</span><span class="sxs-lookup"><span data-stu-id="2e2a9-118">Pointer to a [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) structure that is the product of two quaternions.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e2a9-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2e2a9-119">Remarks</span></span>

<span data-ttu-id="2e2a9-120">Результат представляет собой поворот Q1, за которым следует поворот Q2 (out = Q2 \* Q1).</span><span class="sxs-lookup"><span data-stu-id="2e2a9-120">The result represents the rotation Q1 followed by the rotation Q2 (Out = Q2 \* Q1).</span></span> <span data-ttu-id="2e2a9-121">Это делается так, что **D3DXQuaternionMultiply** поддерживает ту же семантику, что и [**D3DXMatrixMultiply**](d3d10-d3dxmatrixmultiply.md) , поскольку единичные кватерниона можно рассматривать как другой способ представления матриц вращения.</span><span class="sxs-lookup"><span data-stu-id="2e2a9-121">This is done so that **D3DXQuaternionMultiply** maintain the same semantics as [**D3DXMatrixMultiply**](d3d10-d3dxmatrixmultiply.md) because unit quaternions can be considered as another way to represent rotation matrices.</span></span>

<span data-ttu-id="2e2a9-122">Преобразования объединяются в одном и том же порядке для функций **D3DXQuaternionMultiply** и [**D3DXMatrixMultiply**](d3d10-d3dxmatrixmultiply.md) .</span><span class="sxs-lookup"><span data-stu-id="2e2a9-122">Transformations are concatenated in the same order for both the **D3DXQuaternionMultiply** and [**D3DXMatrixMultiply**](d3d10-d3dxmatrixmultiply.md) Functions.</span></span> <span data-ttu-id="2e2a9-123">Например, предположим, что mX и mY представляют те же вращения, что и ККС и Ки, и m, и q будут представлять одни и те же повороты.</span><span class="sxs-lookup"><span data-stu-id="2e2a9-123">For example, assuming mX and mY represent the same rotations as qX and qY, both m and q will represent the same rotations.</span></span>


```
D3DXMatrixMultiply(&m, &mX, &mY);
D3DXQuaternionMultiply(&q, &qX, &qY);
```



<span data-ttu-id="2e2a9-124">Умножение кватернионов не коммутативной.</span><span class="sxs-lookup"><span data-stu-id="2e2a9-124">The multiplication of quaternions is not commutative.</span></span>

<span data-ttu-id="2e2a9-125">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="2e2a9-125">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="2e2a9-126">Таким образом, функция **D3DXQuaternionMultiply** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="2e2a9-126">In this way, the **D3DXQuaternionMultiply** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="2e2a9-127">Используйте [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) для любых входных данных кватернион, которые еще не нормализованы.</span><span class="sxs-lookup"><span data-stu-id="2e2a9-127">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e2a9-128">Требования</span><span class="sxs-lookup"><span data-stu-id="2e2a9-128">Requirements</span></span>



| <span data-ttu-id="2e2a9-129">Требование</span><span class="sxs-lookup"><span data-stu-id="2e2a9-129">Requirement</span></span> | <span data-ttu-id="2e2a9-130">Значение</span><span class="sxs-lookup"><span data-stu-id="2e2a9-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e2a9-131">Header</span><span class="sxs-lookup"><span data-stu-id="2e2a9-131">Header</span></span><br/>  | <dl> <span data-ttu-id="2e2a9-132"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e2a9-132"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="2e2a9-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2e2a9-133">Library</span></span><br/> | <dl> <span data-ttu-id="2e2a9-134"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2e2a9-134"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2e2a9-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2e2a9-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e2a9-136">Математические функции</span><span class="sxs-lookup"><span data-stu-id="2e2a9-136">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
