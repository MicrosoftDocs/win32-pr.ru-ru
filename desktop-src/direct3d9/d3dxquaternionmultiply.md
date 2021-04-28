---
description: Функция D3DXQuaternionMultiply (D3dx9math. h) умножает два кватерниона.
ms.assetid: 11072fc9-dae8-4f63-b07d-b709eed381df
title: Функция D3DXQuaternionMultiply (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7250484e4943e8b077a63e35951c17a44eaf2de3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118042"
---
# <a name="d3dxquaternionmultiply-function-d3dx9mathh"></a><span data-ttu-id="8b809-103">Функция D3DXQuaternionMultiply (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="8b809-103">D3DXQuaternionMultiply function (D3dx9math.h)</span></span>

<span data-ttu-id="8b809-104">Умножает два кватерниона.</span><span class="sxs-lookup"><span data-stu-id="8b809-104">Multiplies two quaternions.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b809-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8b809-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionMultiply(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pQ2
);
```



## <a name="parameters"></a><span data-ttu-id="8b809-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8b809-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b809-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="8b809-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8b809-108">Тип: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="8b809-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="8b809-109">Указатель на структуру [**D3DXQUATERNION**](d3dxquaternion.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="8b809-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="8b809-110">*pQ1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8b809-110">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b809-111">Тип: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="8b809-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="8b809-112">Указатель на исходную структуру [**D3DXQUATERNION**](d3dxquaternion.md) .</span><span class="sxs-lookup"><span data-stu-id="8b809-112">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="8b809-113">*pQ2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8b809-113">*pQ2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b809-114">Тип: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="8b809-114">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="8b809-115">Указатель на исходную структуру [**D3DXQUATERNION**](d3dxquaternion.md) .</span><span class="sxs-lookup"><span data-stu-id="8b809-115">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b809-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8b809-116">Return value</span></span>

<span data-ttu-id="8b809-117">Тип: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="8b809-117">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="8b809-118">Указатель на структуру [**D3DXQUATERNION**](d3dxquaternion.md) , которая является произведением двух кватернионов.</span><span class="sxs-lookup"><span data-stu-id="8b809-118">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the product of two quaternions.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b809-119">Remarks</span><span class="sxs-lookup"><span data-stu-id="8b809-119">Remarks</span></span>

<span data-ttu-id="8b809-120">Результат представляет собой поворот Q1, за которым следует поворот Q2 (out = Q2 \* Q1).</span><span class="sxs-lookup"><span data-stu-id="8b809-120">The result represents the rotation Q1 followed by the rotation Q2 (Out = Q2 \* Q1).</span></span> <span data-ttu-id="8b809-121">Это делается так, что **D3DXQuaternionMultiply** поддерживает ту же семантику, что и [**D3DXMatrixMultiply**](d3dxmatrixmultiply.md) , поскольку единичные кватерниона можно рассматривать как другой способ представления матриц вращения.</span><span class="sxs-lookup"><span data-stu-id="8b809-121">This is done so that **D3DXQuaternionMultiply** maintain the same semantics as [**D3DXMatrixMultiply**](d3dxmatrixmultiply.md) because unit quaternions can be considered as another way to represent rotation matrices.</span></span>

<span data-ttu-id="8b809-122">Преобразования объединяются в одном и том же порядке для функций **D3DXQuaternionMultiply** и [**D3DXMatrixMultiply**](d3dxmatrixmultiply.md) .</span><span class="sxs-lookup"><span data-stu-id="8b809-122">Transformations are concatenated in the same order for both the **D3DXQuaternionMultiply** and [**D3DXMatrixMultiply**](d3dxmatrixmultiply.md) functions.</span></span> <span data-ttu-id="8b809-123">Например, предположим, что mX и mY представляют те же вращения, что и ККС и Ки, и m, и q будут представлять одни и те же повороты.</span><span class="sxs-lookup"><span data-stu-id="8b809-123">For example, assuming mX and mY represent the same rotations as qX and qY, both m and q will represent the same rotations.</span></span>


```
D3DXMatrixMultiply(&m, &mX, &mY);
D3DXQuaternionMultiply(&q, &qX, &qY);
```



<span data-ttu-id="8b809-124">Умножение кватернионов не коммутативной.</span><span class="sxs-lookup"><span data-stu-id="8b809-124">The multiplication of quaternions is not commutative.</span></span>

<span data-ttu-id="8b809-125">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="8b809-125">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="8b809-126">Таким образом, функция **D3DXQuaternionMultiply** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="8b809-126">In this way, the **D3DXQuaternionMultiply** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="8b809-127">Используйте [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) для любых входных данных кватернион, которые еще не нормализованы.</span><span class="sxs-lookup"><span data-stu-id="8b809-127">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b809-128">Требования</span><span class="sxs-lookup"><span data-stu-id="8b809-128">Requirements</span></span>



| <span data-ttu-id="8b809-129">Требование</span><span class="sxs-lookup"><span data-stu-id="8b809-129">Requirement</span></span> | <span data-ttu-id="8b809-130">Значение</span><span class="sxs-lookup"><span data-stu-id="8b809-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8b809-131">Header</span><span class="sxs-lookup"><span data-stu-id="8b809-131">Header</span></span><br/>  | <dl> <span data-ttu-id="8b809-132"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b809-132"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="8b809-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8b809-133">Library</span></span><br/> | <dl> <span data-ttu-id="8b809-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8b809-134"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8b809-135">См. также</span><span class="sxs-lookup"><span data-stu-id="8b809-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b809-136">Математические функции</span><span class="sxs-lookup"><span data-stu-id="8b809-136">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="8b809-137">**D3DXMatrixMultiply**</span><span class="sxs-lookup"><span data-stu-id="8b809-137">**D3DXMatrixMultiply**</span></span>](d3dxmatrixmultiply.md)
</dt> </dl>

 

 




