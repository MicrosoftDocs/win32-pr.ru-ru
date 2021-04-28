---
description: Функция D3DXQuaternionNormalize (D3dx9math. h) — выдает кватернион, равный единице измерения.
ms.assetid: 31f56c2b-96b0-4110-a5b9-ce09983779b6
title: Функция D3DXQuaternionNormalize (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a5d4a7938b96d3d8693fd2091fcbd4f664f465c5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094042"
---
# <a name="d3dxquaternionnormalize-function-d3dx9mathh"></a><span data-ttu-id="4ae88-103">Функция D3DXQuaternionNormalize (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="4ae88-103">D3DXQuaternionNormalize function (D3dx9math.h)</span></span>

<span data-ttu-id="4ae88-104">Выдает кватернион для единицы измерения длины.</span><span class="sxs-lookup"><span data-stu-id="4ae88-104">Computes a unit length quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ae88-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4ae88-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionNormalize(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="4ae88-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4ae88-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ae88-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="4ae88-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4ae88-108">Тип: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="4ae88-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="4ae88-109">Указатель на структуру [**D3DXQUATERNION**](d3dxquaternion.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="4ae88-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="4ae88-110">*pQ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4ae88-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ae88-111">Тип: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="4ae88-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="4ae88-112">Указатель на исходную структуру [**D3DXQUATERNION**](d3dxquaternion.md) .</span><span class="sxs-lookup"><span data-stu-id="4ae88-112">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ae88-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4ae88-113">Return value</span></span>

<span data-ttu-id="4ae88-114">Тип: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="4ae88-114">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="4ae88-115">Указатель на структуру [**D3DXQUATERNION**](d3dxquaternion.md) , которая является нормальным для кватерниона.</span><span class="sxs-lookup"><span data-stu-id="4ae88-115">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the normal of the quaternion.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ae88-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="4ae88-116">Remarks</span></span>

<span data-ttu-id="4ae88-117">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="4ae88-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="4ae88-118">Таким образом, функция **D3DXQuaternionNormalize** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="4ae88-118">In this way, the **D3DXQuaternionNormalize** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ae88-119">Требования</span><span class="sxs-lookup"><span data-stu-id="4ae88-119">Requirements</span></span>



| <span data-ttu-id="4ae88-120">Требование</span><span class="sxs-lookup"><span data-stu-id="4ae88-120">Requirement</span></span> | <span data-ttu-id="4ae88-121">Значение</span><span class="sxs-lookup"><span data-stu-id="4ae88-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4ae88-122">Header</span><span class="sxs-lookup"><span data-stu-id="4ae88-122">Header</span></span><br/>  | <dl> <span data-ttu-id="4ae88-123"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ae88-123"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="4ae88-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4ae88-124">Library</span></span><br/> | <dl> <span data-ttu-id="4ae88-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4ae88-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4ae88-126">См. также</span><span class="sxs-lookup"><span data-stu-id="4ae88-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ae88-127">Математические функции</span><span class="sxs-lookup"><span data-stu-id="4ae88-127">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="4ae88-128">**D3DXQuaternionInverse**</span><span class="sxs-lookup"><span data-stu-id="4ae88-128">**D3DXQuaternionInverse**</span></span>](d3dxquaternioninverse.md)
</dt> </dl>

 

 




