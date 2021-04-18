---
description: Преобразует градусы в радианы.
ms.assetid: 450806bd-db2f-47be-ae80-c261088b1bb8
title: D3DXToRadian (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXToRadian
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: e06184a0d3c654a2c0e82431ff25a339f5682837
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713634"
---
# <a name="d3dxtoradian"></a><span data-ttu-id="3ddfd-103">D3DXToRadian</span><span class="sxs-lookup"><span data-stu-id="3ddfd-103">D3DXToRadian</span></span>

<span data-ttu-id="3ddfd-104">Преобразует градусы в радианы.</span><span class="sxs-lookup"><span data-stu-id="3ddfd-104">Converts degrees into radians.</span></span>

``` syntax
#define D3DXToRadian(degree) ((degree) * (D3DX_PI / 180.0f))
```

## <a name="parameters"></a><span data-ttu-id="3ddfd-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="3ddfd-105">Parameters</span></span>



| <span data-ttu-id="3ddfd-106">Параметр</span><span class="sxs-lookup"><span data-stu-id="3ddfd-106">Parameter</span></span>                                                           | <span data-ttu-id="3ddfd-107">Описание</span><span class="sxs-lookup"><span data-stu-id="3ddfd-107">Description</span></span>                                              |
|---------------------------------------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="3ddfd-108"><span id="degree"></span><span id="DEGREE"></span>иной</span><span class="sxs-lookup"><span data-stu-id="3ddfd-108"><span id="degree"></span><span id="DEGREE"></span>degree</span></span><br/> | <span data-ttu-id="3ddfd-109">Значение (в градусах) для преобразования в радианы.</span><span class="sxs-lookup"><span data-stu-id="3ddfd-109">The value, in degrees, to convert to radians.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="3ddfd-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3ddfd-110">Return Value</span></span>

<span data-ttu-id="3ddfd-111">Макрос возвращает значение градуса в радианах.</span><span class="sxs-lookup"><span data-stu-id="3ddfd-111">The macro returns the degree value in radians.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ddfd-112">Требования</span><span class="sxs-lookup"><span data-stu-id="3ddfd-112">Requirements</span></span>



| <span data-ttu-id="3ddfd-113">Требование</span><span class="sxs-lookup"><span data-stu-id="3ddfd-113">Requirement</span></span> | <span data-ttu-id="3ddfd-114">Значение</span><span class="sxs-lookup"><span data-stu-id="3ddfd-114">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3ddfd-115">Header</span><span class="sxs-lookup"><span data-stu-id="3ddfd-115">Header</span></span><br/> | <dl> <span data-ttu-id="3ddfd-116"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ddfd-116"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ddfd-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3ddfd-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ddfd-118">Макросы</span><span class="sxs-lookup"><span data-stu-id="3ddfd-118">Macros</span></span>](dx9-graphics-reference-d3dx-macros.md)
</dt> <dt>

[<span data-ttu-id="3ddfd-119">**D3DXToDegree**</span><span class="sxs-lookup"><span data-stu-id="3ddfd-119">**D3DXToDegree**</span></span>](d3dxtodegree.md)
</dt> <dt>

[<span data-ttu-id="3ddfd-120">D3DX \_ Pi</span><span class="sxs-lookup"><span data-stu-id="3ddfd-120">D3DX\_PI</span></span>](other-d3dx-constants.md)
</dt> </dl>

 

 




