---
description: Вычисляет натуральный логарифм.
ms.assetid: 73ca7d13-1e20-48fc-b0ed-0d3127d094a7
title: Функция D3DXQuaternionLn (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionLn
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b51fcc77da29216acd2bfc1c011a063014da5d69
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104548047"
---
# <a name="d3dxquaternionln-function-d3dx9mathh"></a><span data-ttu-id="39038-103">Функция D3DXQuaternionLn (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="39038-103">D3DXQuaternionLn function (D3dx9math.h)</span></span>

<span data-ttu-id="39038-104">Вычисляет натуральный логарифм.</span><span class="sxs-lookup"><span data-stu-id="39038-104">Calculates the natural logarithm.</span></span>

## <a name="syntax"></a><span data-ttu-id="39038-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="39038-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionLn(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="39038-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="39038-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39038-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="39038-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="39038-108">Тип: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="39038-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="39038-109">Указатель на структуру [**D3DXQUATERNION**](d3dxquaternion.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="39038-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="39038-110">*pQ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="39038-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39038-111">Тип: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="39038-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="39038-112">Указатель на исходную структуру [**D3DXQUATERNION**](d3dxquaternion.md) .</span><span class="sxs-lookup"><span data-stu-id="39038-112">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39038-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="39038-113">Return value</span></span>

<span data-ttu-id="39038-114">Тип: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="39038-114">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="39038-115">Указатель на структуру [**D3DXQUATERNION**](d3dxquaternion.md) , которая является естественным логарифмом.</span><span class="sxs-lookup"><span data-stu-id="39038-115">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the natural logarithm.</span></span>

## <a name="remarks"></a><span data-ttu-id="39038-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="39038-116">Remarks</span></span>

<span data-ttu-id="39038-117">Функция **D3DXQuaternionLn** работает только для единичных кватернионов.</span><span class="sxs-lookup"><span data-stu-id="39038-117">The **D3DXQuaternionLn** function works only for unit quaternions.</span></span>


```
A unit quaternion, is defined by:
Q == (cos(theta), sin(theta) * v) where |v| = 1
The natural logarithm of Q is, ln(Q) = (0, theta * v)
```



<span data-ttu-id="39038-118">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="39038-118">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="39038-119">Таким образом, функция **D3DXQuaternionLn** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="39038-119">In this way, the **D3DXQuaternionLn** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="39038-120">Используйте [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) для любых входных данных кватернион, которые еще не нормализованы.</span><span class="sxs-lookup"><span data-stu-id="39038-120">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="39038-121">Требования</span><span class="sxs-lookup"><span data-stu-id="39038-121">Requirements</span></span>



| <span data-ttu-id="39038-122">Требование</span><span class="sxs-lookup"><span data-stu-id="39038-122">Requirement</span></span> | <span data-ttu-id="39038-123">Значение</span><span class="sxs-lookup"><span data-stu-id="39038-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="39038-124">Header</span><span class="sxs-lookup"><span data-stu-id="39038-124">Header</span></span><br/>  | <dl> <span data-ttu-id="39038-125"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="39038-125"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="39038-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="39038-126">Library</span></span><br/> | <dl> <span data-ttu-id="39038-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="39038-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="39038-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="39038-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39038-129">Математические функции</span><span class="sxs-lookup"><span data-stu-id="39038-129">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="39038-130">**D3DXQuaternionExp**</span><span class="sxs-lookup"><span data-stu-id="39038-130">**D3DXQuaternionExp**</span></span>](d3dxquaternionexp.md)
</dt> <dt>

[<span data-ttu-id="39038-131">**D3DXQuaternionSquad**</span><span class="sxs-lookup"><span data-stu-id="39038-131">**D3DXQuaternionSquad**</span></span>](d3dxquaternionsquad.md)
</dt> </dl>

 

 




