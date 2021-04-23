---
description: Вычисляет натуральный логарифм.
ms.assetid: 576cf676-bb42-45ec-8e45-4612a7cdb167
title: Функция D3DXQuaternionLn (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 07b081e0e2063d18ab8f2bb010e2b436c38df097
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105674745"
---
# <a name="d3dxquaternionln-function-d3dx10mathh"></a><span data-ttu-id="b717e-103">Функция D3DXQuaternionLn (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="b717e-103">D3DXQuaternionLn function (D3DX10Math.h)</span></span>

<span data-ttu-id="b717e-104">Вычисляет натуральный логарифм.</span><span class="sxs-lookup"><span data-stu-id="b717e-104">Calculates the natural logarithm.</span></span>

## <a name="syntax"></a><span data-ttu-id="b717e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b717e-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionLn(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="b717e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b717e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b717e-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="b717e-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b717e-108">Тип: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="b717e-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="b717e-109">Указатель на [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) , который является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="b717e-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="b717e-110">*pQ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b717e-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b717e-111">Тип: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="b717e-111">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="b717e-112">Указатель на исходную структуру D3DXQUATERNION.</span><span class="sxs-lookup"><span data-stu-id="b717e-112">Pointer to the source D3DXQUATERNION structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b717e-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b717e-113">Return value</span></span>

<span data-ttu-id="b717e-114">Тип: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="b717e-114">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="b717e-115">Указатель на структуру D3DXQUATERNION, которая является естественным логарифмом.</span><span class="sxs-lookup"><span data-stu-id="b717e-115">Pointer to a D3DXQUATERNION structure that is the natural logarithm.</span></span>

## <a name="remarks"></a><span data-ttu-id="b717e-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b717e-116">Remarks</span></span>

<span data-ttu-id="b717e-117">Функция D3DXQuaternionLn работает только для единичных кватернионов.</span><span class="sxs-lookup"><span data-stu-id="b717e-117">The D3DXQuaternionLn function works only for unit quaternions.</span></span>


```
A unit quaternion, is defined by:
Q == (cos(theta), sin(theta) * v) where |v| = 1
The natural logarithm of Q is, ln(Q) = (0, theta * v)
```



<span data-ttu-id="b717e-118">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="b717e-118">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="b717e-119">Таким образом, функция D3DXQuaternionLn может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="b717e-119">In this way, the D3DXQuaternionLn function can be used as a parameter for another function.</span></span>

<span data-ttu-id="b717e-120">Используйте [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) для любых входных данных кватернион, которые еще не нормализованы.</span><span class="sxs-lookup"><span data-stu-id="b717e-120">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="b717e-121">Требования</span><span class="sxs-lookup"><span data-stu-id="b717e-121">Requirements</span></span>



| <span data-ttu-id="b717e-122">Требование</span><span class="sxs-lookup"><span data-stu-id="b717e-122">Requirement</span></span> | <span data-ttu-id="b717e-123">Значение</span><span class="sxs-lookup"><span data-stu-id="b717e-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b717e-124">Header</span><span class="sxs-lookup"><span data-stu-id="b717e-124">Header</span></span><br/>  | <dl> <span data-ttu-id="b717e-125"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="b717e-125"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="b717e-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b717e-126">Library</span></span><br/> | <dl> <span data-ttu-id="b717e-127"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b717e-127"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b717e-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b717e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b717e-129">Математические функции</span><span class="sxs-lookup"><span data-stu-id="b717e-129">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
