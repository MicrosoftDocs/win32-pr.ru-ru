---
description: Сопряженный и ренормализованный кватернион.
ms.assetid: 8e1bba91-8895-43a2-805b-1368050f8e82
title: Функция D3DXQuaternionInverse (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d58231c076dd44f77c7082a755d92ae997515ffb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105674746"
---
# <a name="d3dxquaternioninverse-function-d3dx10mathh"></a><span data-ttu-id="9d250-103">Функция D3DXQuaternionInverse (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="9d250-103">D3DXQuaternionInverse function (D3DX10Math.h)</span></span>

<span data-ttu-id="9d250-104">Сопряженный и ренормализованный кватернион.</span><span class="sxs-lookup"><span data-stu-id="9d250-104">Conjugates and renormalizes a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d250-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9d250-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionInverse(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="9d250-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9d250-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d250-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="9d250-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9d250-108">Тип: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="9d250-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="9d250-109">Указатель на [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) , который является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="9d250-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="9d250-110">*pQ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9d250-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d250-111">Тип: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="9d250-111">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="9d250-112">Указатель на исходную структуру D3DXQUATERNION.</span><span class="sxs-lookup"><span data-stu-id="9d250-112">Pointer to the source D3DXQUATERNION structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d250-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9d250-113">Return value</span></span>

<span data-ttu-id="9d250-114">Тип: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="9d250-114">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="9d250-115">Указатель на структуру D3DXQUATERNION, которая является обратным кватернионом кватерниона.</span><span class="sxs-lookup"><span data-stu-id="9d250-115">Pointer to a D3DXQUATERNION structure that is the inverse quaternion of the quaternion.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d250-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9d250-116">Remarks</span></span>


```
A unit quaternion, is defined by:
Q == (cos(theta), sin(theta) * v) where |v| = 1
The natural logarithm of Q is, ln(Q) = (0, theta * v)
```



<span data-ttu-id="9d250-117">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="9d250-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="9d250-118">Таким образом, функция D3DXQuaternionInverse может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="9d250-118">In this way, the D3DXQuaternionInverse function can be used as a parameter for another function.</span></span>

<span data-ttu-id="9d250-119">Используйте [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) для любых входных данных кватернион, которые еще не нормализованы.</span><span class="sxs-lookup"><span data-stu-id="9d250-119">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d250-120">Требования</span><span class="sxs-lookup"><span data-stu-id="9d250-120">Requirements</span></span>



| <span data-ttu-id="9d250-121">Требование</span><span class="sxs-lookup"><span data-stu-id="9d250-121">Requirement</span></span> | <span data-ttu-id="9d250-122">Значение</span><span class="sxs-lookup"><span data-stu-id="9d250-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9d250-123">Header</span><span class="sxs-lookup"><span data-stu-id="9d250-123">Header</span></span><br/>  | <dl> <span data-ttu-id="9d250-124"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d250-124"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="9d250-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9d250-125">Library</span></span><br/> | <dl> <span data-ttu-id="9d250-126"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9d250-126"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9d250-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9d250-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d250-128">Математические функции</span><span class="sxs-lookup"><span data-stu-id="9d250-128">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
