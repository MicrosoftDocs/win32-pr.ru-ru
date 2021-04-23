---
description: Преобразует радианы в градусы.
ms.assetid: 1b19af39-ca23-4364-9121-f532d7fed099
title: D3DXToDegree (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXToDegree
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: ad77ea661f4d67318566079aa7c1072fe0f86c91
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105684998"
---
# <a name="d3dxtodegree"></a><span data-ttu-id="21078-103">D3DXToDegree</span><span class="sxs-lookup"><span data-stu-id="21078-103">D3DXToDegree</span></span>

<span data-ttu-id="21078-104">Преобразует радианы в градусы.</span><span class="sxs-lookup"><span data-stu-id="21078-104">Converts radians into degrees.</span></span>

``` syntax
#define D3DXToDegree(radian) ((radian) * (180.0f / D3DX_PI))
```

## <a name="parameters"></a><span data-ttu-id="21078-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="21078-105">Parameters</span></span>



| <span data-ttu-id="21078-106">Параметр</span><span class="sxs-lookup"><span data-stu-id="21078-106">Parameter</span></span>                                                           | <span data-ttu-id="21078-107">Описание</span><span class="sxs-lookup"><span data-stu-id="21078-107">Description</span></span>                                              |
|---------------------------------------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="21078-108"><span id="radian"></span><span id="RADIAN"></span>диапазоне</span><span class="sxs-lookup"><span data-stu-id="21078-108"><span id="radian"></span><span id="RADIAN"></span>radian</span></span><br/> | <span data-ttu-id="21078-109">Значение в радианах для преобразования в градусы.</span><span class="sxs-lookup"><span data-stu-id="21078-109">The value, in radians, to convert to degrees.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="21078-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="21078-110">Return Value</span></span>

<span data-ttu-id="21078-111">Макрос возвращает значение радианы в градусах.</span><span class="sxs-lookup"><span data-stu-id="21078-111">The macro returns the radian value in degrees.</span></span>

## <a name="requirements"></a><span data-ttu-id="21078-112">Требования</span><span class="sxs-lookup"><span data-stu-id="21078-112">Requirements</span></span>



| <span data-ttu-id="21078-113">Требование</span><span class="sxs-lookup"><span data-stu-id="21078-113">Requirement</span></span> | <span data-ttu-id="21078-114">Значение</span><span class="sxs-lookup"><span data-stu-id="21078-114">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="21078-115">Header</span><span class="sxs-lookup"><span data-stu-id="21078-115">Header</span></span><br/> | <dl> <span data-ttu-id="21078-116"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="21078-116"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21078-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="21078-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21078-118">Макросы</span><span class="sxs-lookup"><span data-stu-id="21078-118">Macros</span></span>](dx9-graphics-reference-d3dx-macros.md)
</dt> <dt>

[<span data-ttu-id="21078-119">**D3DXToRadian**</span><span class="sxs-lookup"><span data-stu-id="21078-119">**D3DXToRadian**</span></span>](d3dxtoradian.md)
</dt> <dt>

[<span data-ttu-id="21078-120">D3DX \_ Pi</span><span class="sxs-lookup"><span data-stu-id="21078-120">D3DX\_PI</span></span>](other-d3dx-constants.md)
</dt> </dl>

 

 




