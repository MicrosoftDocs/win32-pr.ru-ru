---
description: Вычисляет экспоненту.
ms.assetid: 648aeaf1-ead3-4b21-819f-cd2a70881a13
title: Функция D3DXQuaternionExp (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionExp
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b9cb5765e01c4fbbc6ab3785363425262ee491ef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703734"
---
# <a name="d3dxquaternionexp-function-d3dx9mathh"></a><span data-ttu-id="3bd7e-103">Функция D3DXQuaternionExp (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="3bd7e-103">D3DXQuaternionExp function (D3dx9math.h)</span></span>

<span data-ttu-id="3bd7e-104">Вычисляет экспоненту.</span><span class="sxs-lookup"><span data-stu-id="3bd7e-104">Calculates the exponential.</span></span>

## <a name="syntax"></a><span data-ttu-id="3bd7e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3bd7e-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionExp(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="3bd7e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3bd7e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3bd7e-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="3bd7e-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3bd7e-108">Тип: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="3bd7e-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="3bd7e-109">Указатель на структуру [**D3DXQUATERNION**](d3dxquaternion.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="3bd7e-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="3bd7e-110">*pQ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3bd7e-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3bd7e-111">Тип: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="3bd7e-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="3bd7e-112">Указатель на исходную структуру [**D3DXQUATERNION**](d3dxquaternion.md) .</span><span class="sxs-lookup"><span data-stu-id="3bd7e-112">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3bd7e-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3bd7e-113">Return value</span></span>

<span data-ttu-id="3bd7e-114">Тип: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="3bd7e-114">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="3bd7e-115">Указатель на структуру [**D3DXQUATERNION**](d3dxquaternion.md) , которая является экспонентой.</span><span class="sxs-lookup"><span data-stu-id="3bd7e-115">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the exponential.</span></span>

## <a name="remarks"></a><span data-ttu-id="3bd7e-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3bd7e-116">Remarks</span></span>

<span data-ttu-id="3bd7e-117">Этот метод преобразует чистый кватернион в единичный кватернион.</span><span class="sxs-lookup"><span data-stu-id="3bd7e-117">This method converts a pure quaternion to a unit quaternion.</span></span> <span data-ttu-id="3bd7e-118">**D3DXQuaternionExp** ждет чистого кватерниона, где w игнорируется при вычислении (w = = 0).</span><span class="sxs-lookup"><span data-stu-id="3bd7e-118">**D3DXQuaternionExp** expects a pure quaternion, where w is ignored in the calculation (w == 0).</span></span>


```
Given a pure quaternion defined by:
q = (0, theta * v); 
    
This method calculates the exponential result.
exp(Q) = (cos(theta), sin(theta) * v)
```



<span data-ttu-id="3bd7e-119">где v — это векторная часть кватерниона.</span><span class="sxs-lookup"><span data-stu-id="3bd7e-119">where v is the vector portion of a quaternion.</span></span>

<span data-ttu-id="3bd7e-120">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="3bd7e-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="3bd7e-121">Таким образом, функция **D3DXQuaternionExp** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="3bd7e-121">In this way, the **D3DXQuaternionExp** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="3bd7e-122">Метод [**D3DXQuaternionSquadSetup**](d3dxquaternionsquadsetup.md) также можно использовать для настройки контрольных точек кватерниона.</span><span class="sxs-lookup"><span data-stu-id="3bd7e-122">The [**D3DXQuaternionSquadSetup**](d3dxquaternionsquadsetup.md) method can also be used to set up the control points of a quaternion.</span></span>

<span data-ttu-id="3bd7e-123">Используйте [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) для любых входных данных кватернион, которые еще не нормализованы.</span><span class="sxs-lookup"><span data-stu-id="3bd7e-123">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="3bd7e-124">Требования</span><span class="sxs-lookup"><span data-stu-id="3bd7e-124">Requirements</span></span>



| <span data-ttu-id="3bd7e-125">Требование</span><span class="sxs-lookup"><span data-stu-id="3bd7e-125">Requirement</span></span> | <span data-ttu-id="3bd7e-126">Значение</span><span class="sxs-lookup"><span data-stu-id="3bd7e-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3bd7e-127">Header</span><span class="sxs-lookup"><span data-stu-id="3bd7e-127">Header</span></span><br/>  | <dl> <span data-ttu-id="3bd7e-128"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="3bd7e-128"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="3bd7e-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3bd7e-129">Library</span></span><br/> | <dl> <span data-ttu-id="3bd7e-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3bd7e-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3bd7e-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3bd7e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bd7e-132">Математические функции</span><span class="sxs-lookup"><span data-stu-id="3bd7e-132">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="3bd7e-133">**D3DXQuaternionLn**</span><span class="sxs-lookup"><span data-stu-id="3bd7e-133">**D3DXQuaternionLn**</span></span>](d3dxquaternionln.md)
</dt> <dt>

[<span data-ttu-id="3bd7e-134">**D3DXQuaternionSquad**</span><span class="sxs-lookup"><span data-stu-id="3bd7e-134">**D3DXQuaternionSquad**</span></span>](d3dxquaternionsquad.md)
</dt> </dl>

 

 




