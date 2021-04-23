---
description: Вычисляет экспоненту.
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
ms.openlocfilehash: d00292cc073679e3e90c2470630ba1851d0d3cd8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821253"
---
# <a name="d3dxquaternionexp-function-d3dx10mathh"></a><span data-ttu-id="0c41c-103">Функция D3DXQuaternionExp (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="0c41c-103">D3DXQuaternionExp function (D3DX10Math.h)</span></span>

<span data-ttu-id="0c41c-104">Вычисляет экспоненту.</span><span class="sxs-lookup"><span data-stu-id="0c41c-104">Calculates the exponential.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c41c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0c41c-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionExp(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="0c41c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0c41c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c41c-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="0c41c-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0c41c-108">Тип: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="0c41c-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="0c41c-109">Указатель на [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) , который является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="0c41c-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="0c41c-110">*pQ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0c41c-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c41c-111">Тип: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="0c41c-111">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="0c41c-112">Указатель на исходную структуру D3DXQUATERNION.</span><span class="sxs-lookup"><span data-stu-id="0c41c-112">Pointer to the source D3DXQUATERNION structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c41c-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0c41c-113">Return value</span></span>

<span data-ttu-id="0c41c-114">Тип: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="0c41c-114">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="0c41c-115">Указатель на структуру D3DXQUATERNION, которая является экспонентой.</span><span class="sxs-lookup"><span data-stu-id="0c41c-115">Pointer to a D3DXQUATERNION structure that is the exponential.</span></span>

## <a name="remarks"></a><span data-ttu-id="0c41c-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0c41c-116">Remarks</span></span>

<span data-ttu-id="0c41c-117">Этот метод преобразует чистый кватернион в единичный кватернион.</span><span class="sxs-lookup"><span data-stu-id="0c41c-117">This method converts a pure quaternion to a unit quaternion.</span></span> <span data-ttu-id="0c41c-118">D3DXQuaternionExp ждет чистого кватерниона, где w игнорируется при вычислении (w = = 0).</span><span class="sxs-lookup"><span data-stu-id="0c41c-118">D3DXQuaternionExp expects a pure quaternion, where w is ignored in the calculation (w == 0).</span></span>


```
Given a pure quaternion defined by:
q = (0, theta * v); 
    
This method calculates the exponential result.
exp(Q) = (cos(theta), sin(theta) * v)
```



<span data-ttu-id="0c41c-119">где v — это векторная часть кватерниона.</span><span class="sxs-lookup"><span data-stu-id="0c41c-119">where v is the vector portion of a quaternion.</span></span>

<span data-ttu-id="0c41c-120">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="0c41c-120">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="0c41c-121">Таким образом, функция D3DXQuaternionExp может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="0c41c-121">In this way, the D3DXQuaternionExp function can be used as a parameter for another function.</span></span>

<span data-ttu-id="0c41c-122">Метод [**D3DXQuaternionSquadSetup**](d3d10-d3dxquaternionsquadsetup.md) также можно использовать для настройки контрольных точек кватерниона.</span><span class="sxs-lookup"><span data-stu-id="0c41c-122">The [**D3DXQuaternionSquadSetup**](d3d10-d3dxquaternionsquadsetup.md) method can also be used to set up the control points of a quaternion.</span></span>

<span data-ttu-id="0c41c-123">Используйте [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) для любых входных данных кватернион, которые еще не нормализованы.</span><span class="sxs-lookup"><span data-stu-id="0c41c-123">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c41c-124">Требования</span><span class="sxs-lookup"><span data-stu-id="0c41c-124">Requirements</span></span>



| <span data-ttu-id="0c41c-125">Требование</span><span class="sxs-lookup"><span data-stu-id="0c41c-125">Requirement</span></span> | <span data-ttu-id="0c41c-126">Значение</span><span class="sxs-lookup"><span data-stu-id="0c41c-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0c41c-127">Header</span><span class="sxs-lookup"><span data-stu-id="0c41c-127">Header</span></span><br/>  | <dl> <span data-ttu-id="0c41c-128"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c41c-128"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="0c41c-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0c41c-129">Library</span></span><br/> | <dl> <span data-ttu-id="0c41c-130"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0c41c-130"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0c41c-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0c41c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c41c-132">Математические функции</span><span class="sxs-lookup"><span data-stu-id="0c41c-132">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
