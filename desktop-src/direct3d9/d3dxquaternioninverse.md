---
description: Функция D3DXQuaternionInverse (D3dx9math. h) — сопряженная и ренормализация кватерниона.
ms.assetid: 25407a60-f7c0-4063-8d1d-2d6d03bdb217
title: Функция D3DXQuaternionInverse (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionInverse
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6ebb2520efa3c7c78d98fd8b90ec1ba9615e9927
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094072"
---
# <a name="d3dxquaternioninverse-function-d3dx9mathh"></a><span data-ttu-id="cac6c-103">Функция D3DXQuaternionInverse (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="cac6c-103">D3DXQuaternionInverse function (D3dx9math.h)</span></span>

<span data-ttu-id="cac6c-104">Сопряженный и ренормализованный кватернион.</span><span class="sxs-lookup"><span data-stu-id="cac6c-104">Conjugates and renormalizes a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="cac6c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cac6c-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionInverse(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="cac6c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cac6c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cac6c-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="cac6c-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="cac6c-108">Тип: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="cac6c-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="cac6c-109">Указатель на структуру [**D3DXQUATERNION**](d3dxquaternion.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="cac6c-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="cac6c-110">*pQ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cac6c-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cac6c-111">Тип: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="cac6c-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="cac6c-112">Указатель на исходную структуру [**D3DXQUATERNION**](d3dxquaternion.md) .</span><span class="sxs-lookup"><span data-stu-id="cac6c-112">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cac6c-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cac6c-113">Return value</span></span>

<span data-ttu-id="cac6c-114">Тип: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="cac6c-114">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="cac6c-115">Указатель на структуру [**D3DXQUATERNION**](d3dxquaternion.md) , которая является обратным кватернионом кватерниона.</span><span class="sxs-lookup"><span data-stu-id="cac6c-115">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the inverse quaternion of the quaternion.</span></span>

## <a name="remarks"></a><span data-ttu-id="cac6c-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="cac6c-116">Remarks</span></span>


```
A unit quaternion, is defined by:
Q == (cos(theta), sin(theta) * v) where |v| = 1
The natural logarithm of Q is, ln(Q) = (0, theta * v)
```



<span data-ttu-id="cac6c-117">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="cac6c-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="cac6c-118">Таким образом, функция **D3DXQuaternionInverse** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="cac6c-118">In this way, the **D3DXQuaternionInverse** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="cac6c-119">Используйте [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) для любых входных данных кватернион, которые еще не нормализованы.</span><span class="sxs-lookup"><span data-stu-id="cac6c-119">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="cac6c-120">Требования</span><span class="sxs-lookup"><span data-stu-id="cac6c-120">Requirements</span></span>



| <span data-ttu-id="cac6c-121">Требование</span><span class="sxs-lookup"><span data-stu-id="cac6c-121">Requirement</span></span> | <span data-ttu-id="cac6c-122">Значение</span><span class="sxs-lookup"><span data-stu-id="cac6c-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cac6c-123">Header</span><span class="sxs-lookup"><span data-stu-id="cac6c-123">Header</span></span><br/>  | <dl> <span data-ttu-id="cac6c-124"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="cac6c-124"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="cac6c-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cac6c-125">Library</span></span><br/> | <dl> <span data-ttu-id="cac6c-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cac6c-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="cac6c-127">См. также</span><span class="sxs-lookup"><span data-stu-id="cac6c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cac6c-128">Математические функции</span><span class="sxs-lookup"><span data-stu-id="cac6c-128">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="cac6c-129">**D3DXQuaternionConjugate**</span><span class="sxs-lookup"><span data-stu-id="cac6c-129">**D3DXQuaternionConjugate**</span></span>](d3dxquaternionconjugate.md)
</dt> <dt>

[<span data-ttu-id="cac6c-130">**D3DXQuaternionNormalize**</span><span class="sxs-lookup"><span data-stu-id="cac6c-130">**D3DXQuaternionNormalize**</span></span>](d3dxquaternionnormalize.md)
</dt> </dl>

 

 




