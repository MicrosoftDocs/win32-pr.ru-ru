---
description: Определяет, является ли кватернион единичным кватернион.
ms.assetid: 1cd39e1b-9b68-434d-b7b0-3ec6cddb8757
title: Функция D3DXQuaternionIsIdentity (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionIsIdentity
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b2b02bdddb4b7a2d31a685f576434e34952c0a22
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703927"
---
# <a name="d3dxquaternionisidentity-function"></a><span data-ttu-id="0e37d-103">Функция D3DXQuaternionIsIdentity</span><span class="sxs-lookup"><span data-stu-id="0e37d-103">D3DXQuaternionIsIdentity function</span></span>

<span data-ttu-id="0e37d-104">Определяет, является ли кватернион единичным кватернион.</span><span class="sxs-lookup"><span data-stu-id="0e37d-104">Determines if a quaternion is an identity quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e37d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0e37d-105">Syntax</span></span>


```C++
BOOL D3DXQuaternionIsIdentity(
  _In_ const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="0e37d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0e37d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e37d-107">*pQ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0e37d-107">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e37d-108">Тип: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="0e37d-108">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="0e37d-109">Указатель на структуру [**D3DXQUATERNION**](d3dxquaternion.md) , которая будет протестирована для идентификации.</span><span class="sxs-lookup"><span data-stu-id="0e37d-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that will be tested for identity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e37d-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0e37d-110">Return value</span></span>

<span data-ttu-id="0e37d-111">Тип: **[ **bool** .](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0e37d-111">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0e37d-112">Если кватернион является единичным кватернион, эта функция возвращает **значение true**.</span><span class="sxs-lookup"><span data-stu-id="0e37d-112">If the quaternion is an identity quaternion, this function returns **TRUE**.</span></span> <span data-ttu-id="0e37d-113">В противном случае эта функция возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="0e37d-113">Otherwise, this function returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e37d-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0e37d-114">Remarks</span></span>

<span data-ttu-id="0e37d-115">Используйте [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) для любых входных данных кватернион, которые еще не нормализованы.</span><span class="sxs-lookup"><span data-stu-id="0e37d-115">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e37d-116">Требования</span><span class="sxs-lookup"><span data-stu-id="0e37d-116">Requirements</span></span>



| <span data-ttu-id="0e37d-117">Требование</span><span class="sxs-lookup"><span data-stu-id="0e37d-117">Requirement</span></span> | <span data-ttu-id="0e37d-118">Значение</span><span class="sxs-lookup"><span data-stu-id="0e37d-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0e37d-119">Header</span><span class="sxs-lookup"><span data-stu-id="0e37d-119">Header</span></span><br/>  | <dl> <span data-ttu-id="0e37d-120"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e37d-120"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="0e37d-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0e37d-121">Library</span></span><br/> | <dl> <span data-ttu-id="0e37d-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0e37d-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0e37d-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0e37d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e37d-124">Математические функции</span><span class="sxs-lookup"><span data-stu-id="0e37d-124">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="0e37d-125">**D3DXQuaternionIdentity**</span><span class="sxs-lookup"><span data-stu-id="0e37d-125">**D3DXQuaternionIdentity**</span></span>](d3dxquaternionidentity.md)
</dt> </dl>

 

 
