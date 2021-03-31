---
description: Возвращает сопряженный кватернион.
ms.assetid: f690fdd8-7805-4fc1-9064-4f249d5f7c4f
title: Функция D3DXQuaternionConjugate (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionConjugate
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bbf288724dbdede9d98ec4ee21afd1bb57dd7a49
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273864"
---
# <a name="d3dxquaternionconjugate-function"></a><span data-ttu-id="2f39c-103">Функция D3DXQuaternionConjugate</span><span class="sxs-lookup"><span data-stu-id="2f39c-103">D3DXQuaternionConjugate function</span></span>

<span data-ttu-id="2f39c-104">Возвращает сопряженный кватернион.</span><span class="sxs-lookup"><span data-stu-id="2f39c-104">Returns the conjugate of a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f39c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2f39c-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionConjugate(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="2f39c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2f39c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f39c-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="2f39c-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2f39c-108">Тип: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="2f39c-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="2f39c-109">Указатель на структуру [**D3DXQUATERNION**](d3dxquaternion.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="2f39c-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="2f39c-110">*pQ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2f39c-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f39c-111">Тип: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="2f39c-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="2f39c-112">Указатель на исходную структуру [**D3DXQUATERNION**](d3dxquaternion.md) .</span><span class="sxs-lookup"><span data-stu-id="2f39c-112">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f39c-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2f39c-113">Return value</span></span>

<span data-ttu-id="2f39c-114">Тип: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="2f39c-114">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="2f39c-115">Указатель на структуру [**D3DXQUATERNION**](d3dxquaternion.md) , которая является сопряженной для кватерниона.</span><span class="sxs-lookup"><span data-stu-id="2f39c-115">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the conjugate of the quaternion.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f39c-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2f39c-116">Remarks</span></span>

<span data-ttu-id="2f39c-117">При наличии кватерниона (x, y, z, w) функция **D3DXQuaternionConjugate** вернет кватернион (-x,-y,-z, w).</span><span class="sxs-lookup"><span data-stu-id="2f39c-117">Given a quaternion (x, y, z, w), the **D3DXQuaternionConjugate** function will return the quaternion (-x, -y, -z, w).</span></span>

<span data-ttu-id="2f39c-118">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="2f39c-118">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="2f39c-119">Таким образом, функция **D3DXQuaternionConjugate** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="2f39c-119">In this way, the **D3DXQuaternionConjugate** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="2f39c-120">Используйте [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) для любых входных данных кватернион, которые еще не нормализованы.</span><span class="sxs-lookup"><span data-stu-id="2f39c-120">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f39c-121">Требования</span><span class="sxs-lookup"><span data-stu-id="2f39c-121">Requirements</span></span>



| <span data-ttu-id="2f39c-122">Требование</span><span class="sxs-lookup"><span data-stu-id="2f39c-122">Requirement</span></span> | <span data-ttu-id="2f39c-123">Значение</span><span class="sxs-lookup"><span data-stu-id="2f39c-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f39c-124">Header</span><span class="sxs-lookup"><span data-stu-id="2f39c-124">Header</span></span><br/>  | <dl> <span data-ttu-id="2f39c-125"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f39c-125"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="2f39c-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2f39c-126">Library</span></span><br/> | <dl> <span data-ttu-id="2f39c-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2f39c-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2f39c-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2f39c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f39c-129">Математические функции</span><span class="sxs-lookup"><span data-stu-id="2f39c-129">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="2f39c-130">**D3DXQuaternionInverse**</span><span class="sxs-lookup"><span data-stu-id="2f39c-130">**D3DXQuaternionInverse**</span></span>](d3dxquaternioninverse.md)
</dt> </dl>

 

 




