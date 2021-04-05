---
description: Выдает кватернион для единицы измерения длины.
ms.assetid: 6735a632-64d7-4bc1-b63e-d0cd27f5a29b
title: Функция D3DXQuaternionNormalize (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionNormalize
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e121ef4892c65a0f04acaa89d44d4a5a9090740e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273888"
---
# <a name="d3dxquaternionnormalize-function-d3dx10mathh"></a><span data-ttu-id="dafc1-103">Функция D3DXQuaternionNormalize (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="dafc1-103">D3DXQuaternionNormalize function (D3DX10Math.h)</span></span>

<span data-ttu-id="dafc1-104">Выдает кватернион для единицы измерения длины.</span><span class="sxs-lookup"><span data-stu-id="dafc1-104">Computes a unit length quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="dafc1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dafc1-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionNormalize(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="dafc1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="dafc1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dafc1-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="dafc1-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="dafc1-108">Тип: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="dafc1-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="dafc1-109">Указатель на [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) , который является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="dafc1-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="dafc1-110">*pQ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dafc1-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dafc1-111">Тип: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="dafc1-111">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="dafc1-112">Указатель на исходную структуру D3DXQUATERNION.</span><span class="sxs-lookup"><span data-stu-id="dafc1-112">Pointer to the source D3DXQUATERNION structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dafc1-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dafc1-113">Return value</span></span>

<span data-ttu-id="dafc1-114">Тип: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="dafc1-114">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="dafc1-115">Указатель на структуру D3DXQUATERNION, которая является нормальным для кватерниона.</span><span class="sxs-lookup"><span data-stu-id="dafc1-115">Pointer to a D3DXQUATERNION structure that is the normal of the quaternion.</span></span>

## <a name="remarks"></a><span data-ttu-id="dafc1-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dafc1-116">Remarks</span></span>

<span data-ttu-id="dafc1-117">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="dafc1-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="dafc1-118">Таким образом, функция D3DXQuaternionNormalize может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="dafc1-118">In this way, the D3DXQuaternionNormalize function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="dafc1-119">Требования</span><span class="sxs-lookup"><span data-stu-id="dafc1-119">Requirements</span></span>



| <span data-ttu-id="dafc1-120">Требование</span><span class="sxs-lookup"><span data-stu-id="dafc1-120">Requirement</span></span> | <span data-ttu-id="dafc1-121">Значение</span><span class="sxs-lookup"><span data-stu-id="dafc1-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dafc1-122">Header</span><span class="sxs-lookup"><span data-stu-id="dafc1-122">Header</span></span><br/>  | <dl> <span data-ttu-id="dafc1-123"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="dafc1-123"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="dafc1-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="dafc1-124">Library</span></span><br/> | <dl> <span data-ttu-id="dafc1-125"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dafc1-125"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="dafc1-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dafc1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dafc1-127">Математические функции</span><span class="sxs-lookup"><span data-stu-id="dafc1-127">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
