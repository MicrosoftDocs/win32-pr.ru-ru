---
description: Функция D3DXQuaternionExp (D3DX10Math. h) — Вычисляет экспоненту.
ms.assetid: bd70c432-ac61-4c38-b10b-3b103e49ead8
title: Функция D3DXQuaternionExp (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 7c022b9df4302683a184b4fc8329561b22d341d5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103222"
---
# <a name="d3dxquaternionexp-function-d3dx10mathh"></a><span data-ttu-id="a62ec-103">Функция D3DXQuaternionExp (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="a62ec-103">D3DXQuaternionExp function (D3DX10Math.h)</span></span>

<span data-ttu-id="a62ec-104">Вычисляет экспоненту.</span><span class="sxs-lookup"><span data-stu-id="a62ec-104">Calculates the exponential.</span></span>

## <a name="syntax"></a><span data-ttu-id="a62ec-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a62ec-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionExp(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="a62ec-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a62ec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a62ec-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="a62ec-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a62ec-108">Тип: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="a62ec-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="a62ec-109">Указатель на [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) , который является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="a62ec-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="a62ec-110">*pQ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a62ec-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a62ec-111">Тип: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="a62ec-111">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="a62ec-112">Указатель на исходную структуру D3DXQUATERNION.</span><span class="sxs-lookup"><span data-stu-id="a62ec-112">Pointer to the source D3DXQUATERNION structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a62ec-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a62ec-113">Return value</span></span>

<span data-ttu-id="a62ec-114">Тип: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="a62ec-114">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="a62ec-115">Указатель на структуру D3DXQUATERNION, которая является экспонентой.</span><span class="sxs-lookup"><span data-stu-id="a62ec-115">Pointer to a D3DXQUATERNION structure that is the exponential.</span></span>

## <a name="remarks"></a><span data-ttu-id="a62ec-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="a62ec-116">Remarks</span></span>

<span data-ttu-id="a62ec-117">Этот метод преобразует чистый кватернион в единичный кватернион.</span><span class="sxs-lookup"><span data-stu-id="a62ec-117">This method converts a pure quaternion to a unit quaternion.</span></span> <span data-ttu-id="a62ec-118">D3DXQuaternionExp ждет чистого кватерниона, где w игнорируется при вычислении (w = = 0).</span><span class="sxs-lookup"><span data-stu-id="a62ec-118">D3DXQuaternionExp expects a pure quaternion, where w is ignored in the calculation (w == 0).</span></span>


```
Given a pure quaternion defined by:
q = (0, theta * v); 
    
This method calculates the exponential result.
exp(Q) = (cos(theta), sin(theta) * v)
```



<span data-ttu-id="a62ec-119">где v — это векторная часть кватерниона.</span><span class="sxs-lookup"><span data-stu-id="a62ec-119">where v is the vector portion of a quaternion.</span></span>

<span data-ttu-id="a62ec-120">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="a62ec-120">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="a62ec-121">Таким образом, функция D3DXQuaternionExp может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="a62ec-121">In this way, the D3DXQuaternionExp function can be used as a parameter for another function.</span></span>

<span data-ttu-id="a62ec-122">Метод [**D3DXQuaternionSquadSetup**](d3d10-d3dxquaternionsquadsetup.md) также можно использовать для настройки контрольных точек кватерниона.</span><span class="sxs-lookup"><span data-stu-id="a62ec-122">The [**D3DXQuaternionSquadSetup**](d3d10-d3dxquaternionsquadsetup.md) method can also be used to set up the control points of a quaternion.</span></span>

<span data-ttu-id="a62ec-123">Используйте [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) для любых входных данных кватернион, которые еще не нормализованы.</span><span class="sxs-lookup"><span data-stu-id="a62ec-123">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="a62ec-124">Требования</span><span class="sxs-lookup"><span data-stu-id="a62ec-124">Requirements</span></span>



| <span data-ttu-id="a62ec-125">Требование</span><span class="sxs-lookup"><span data-stu-id="a62ec-125">Requirement</span></span> | <span data-ttu-id="a62ec-126">Значение</span><span class="sxs-lookup"><span data-stu-id="a62ec-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a62ec-127">Header</span><span class="sxs-lookup"><span data-stu-id="a62ec-127">Header</span></span><br/>  | <dl> <span data-ttu-id="a62ec-128"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="a62ec-128"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="a62ec-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a62ec-129">Library</span></span><br/> | <dl> <span data-ttu-id="a62ec-130"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a62ec-130"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a62ec-131">См. также</span><span class="sxs-lookup"><span data-stu-id="a62ec-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a62ec-132">Математические функции</span><span class="sxs-lookup"><span data-stu-id="a62ec-132">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
