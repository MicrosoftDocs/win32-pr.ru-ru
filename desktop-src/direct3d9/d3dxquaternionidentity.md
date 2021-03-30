---
description: Возвращает идентификатор кватерниона.
ms.assetid: 8088897b-5755-4ea0-afef-bd49d1921f5c
title: Функция D3DXQuaternionIdentity (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionIdentity
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e2db9dd0638f5ba67b2dc2e8b8c248889225aaca
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354643"
---
# <a name="d3dxquaternionidentity-function"></a><span data-ttu-id="545fd-103">Функция D3DXQuaternionIdentity</span><span class="sxs-lookup"><span data-stu-id="545fd-103">D3DXQuaternionIdentity function</span></span>

<span data-ttu-id="545fd-104">Возвращает идентификатор кватерниона.</span><span class="sxs-lookup"><span data-stu-id="545fd-104">Returns the identity quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="545fd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="545fd-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionIdentity(
  _Inout_ D3DXQUATERNION *pOut
);
```



## <a name="parameters"></a><span data-ttu-id="545fd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="545fd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="545fd-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="545fd-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="545fd-108">Тип: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="545fd-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="545fd-109">Указатель на структуру [**D3DXQUATERNION**](d3dxquaternion.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="545fd-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="545fd-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="545fd-110">Return value</span></span>

<span data-ttu-id="545fd-111">Тип: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="545fd-111">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="545fd-112">Указатель на структуру [**D3DXQUATERNION**](d3dxquaternion.md) , которая является идентификатором кватерниона.</span><span class="sxs-lookup"><span data-stu-id="545fd-112">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the identity quaternion.</span></span>

## <a name="remarks"></a><span data-ttu-id="545fd-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="545fd-113">Remarks</span></span>

<span data-ttu-id="545fd-114">При наличии кватерниона (x, y, z, w) функция **D3DXQuaternionIdentity** возвратит кватернион (0, 0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="545fd-114">Given a quaternion (x, y, z, w), the **D3DXQuaternionIdentity** function will return the quaternion (0, 0, 0, 1).</span></span>

<span data-ttu-id="545fd-115">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="545fd-115">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="545fd-116">Таким образом, функция **D3DXQuaternionIdentity** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="545fd-116">In this way, the **D3DXQuaternionIdentity** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="545fd-117">Используйте [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) для любых входных данных кватернион, которые еще не нормализованы.</span><span class="sxs-lookup"><span data-stu-id="545fd-117">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="545fd-118">Требования</span><span class="sxs-lookup"><span data-stu-id="545fd-118">Requirements</span></span>



| <span data-ttu-id="545fd-119">Требование</span><span class="sxs-lookup"><span data-stu-id="545fd-119">Requirement</span></span> | <span data-ttu-id="545fd-120">Значение</span><span class="sxs-lookup"><span data-stu-id="545fd-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="545fd-121">Header</span><span class="sxs-lookup"><span data-stu-id="545fd-121">Header</span></span><br/>  | <dl> <span data-ttu-id="545fd-122"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="545fd-122"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="545fd-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="545fd-123">Library</span></span><br/> | <dl> <span data-ttu-id="545fd-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="545fd-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="545fd-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="545fd-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="545fd-126">Математические функции</span><span class="sxs-lookup"><span data-stu-id="545fd-126">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="545fd-127">**D3DXQuaternionIsIdentity**</span><span class="sxs-lookup"><span data-stu-id="545fd-127">**D3DXQuaternionIsIdentity**</span></span>](d3dxquaternionisidentity.md)
</dt> </dl>

 

 




