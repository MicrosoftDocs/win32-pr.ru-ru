---
title: Директива pragma DEF
description: Директива pragma, которая вручную выделяет регистр шейдера с плавающей запятой.
ms.assetid: 45db94c4-f6f6-4c88-9bf2-4eaa9abf7844
keywords:
- Директива pragma DEF HLSL
topic_type:
- apiref
api_name:
- def pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2a921e17f8ddee4aaabfe50e75f42ce44812863d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104996823"
---
# <a name="def-pragma-directive"></a><span data-ttu-id="fae17-104">Директива pragma DEF</span><span class="sxs-lookup"><span data-stu-id="fae17-104">def pragma Directive</span></span>

<span data-ttu-id="fae17-105">Директива pragma, которая вручную выделяет регистр шейдера с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="fae17-105">Pragma directive that manually allocates a floating-point shader register.</span></span>



| <span data-ttu-id="fae17-106">\#pragma DEF ( *Целевая*, *Регистрация*, *val1*, *val2*,*val3*, *val4* )</span><span class="sxs-lookup"><span data-stu-id="fae17-106">\#pragma def( *target*, *register*, *val1*, *val2*,*val3*, *val4* )</span></span> |
|---------------------------------------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="fae17-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="fae17-107">Parameters</span></span>



| <span data-ttu-id="fae17-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="fae17-108">Item</span></span>                                                                        | <span data-ttu-id="fae17-109">Описание</span><span class="sxs-lookup"><span data-stu-id="fae17-109">Description</span></span>                                                                 |
|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="fae17-110"><span id="target"></span><span id="TARGET"></span>*мишень*</span><span class="sxs-lookup"><span data-stu-id="fae17-110"><span id="target"></span><span id="TARGET"></span>*target*</span></span><br/>       | <span data-ttu-id="fae17-111">Целевой объект, содержащий регистр для выделения.</span><span class="sxs-lookup"><span data-stu-id="fae17-111">Target that contains the register to allocate.</span></span> <br/>                  |
| <span data-ttu-id="fae17-112"><span id="register"></span><span id="REGISTER"></span>*зарегистрировать*</span><span class="sxs-lookup"><span data-stu-id="fae17-112"><span id="register"></span><span id="REGISTER"></span>*register*</span></span><br/> | <span data-ttu-id="fae17-113">Регистр шейдера с плавающей точкой для выделения.</span><span class="sxs-lookup"><span data-stu-id="fae17-113">Floating-point shader register to allocate.</span></span> <br/>                     |
| <span data-ttu-id="fae17-114"><span id="val0"></span><span id="VAL0"></span>*val0*</span><span class="sxs-lookup"><span data-stu-id="fae17-114"><span id="val0"></span><span id="VAL0"></span>*val0*</span></span><br/>             | <span data-ttu-id="fae17-115">Первый байт значения, которое необходимо выделить указанному регистру.</span><span class="sxs-lookup"><span data-stu-id="fae17-115">First byte of the value to allocate to the specified register.</span></span> <br/>  |
| <span data-ttu-id="fae17-116"><span id="val1"></span><span id="VAL1"></span>*val1*</span><span class="sxs-lookup"><span data-stu-id="fae17-116"><span id="val1"></span><span id="VAL1"></span>*val1*</span></span><br/>             | <span data-ttu-id="fae17-117">Второй байт значения, которое необходимо выделить указанному регистру.</span><span class="sxs-lookup"><span data-stu-id="fae17-117">Second byte of the value to allocate to the specified register.</span></span> <br/> |
| <span data-ttu-id="fae17-118"><span id="val2"></span><span id="VAL2"></span>*val2*</span><span class="sxs-lookup"><span data-stu-id="fae17-118"><span id="val2"></span><span id="VAL2"></span>*val2*</span></span><br/>             | <span data-ttu-id="fae17-119">Третий байт значения, которое необходимо выделить указанному регистру.</span><span class="sxs-lookup"><span data-stu-id="fae17-119">Third byte of the value to allocate to the specified register.</span></span> <br/>  |
| <span data-ttu-id="fae17-120"><span id="val3"></span><span id="VAL3"></span>*val3*</span><span class="sxs-lookup"><span data-stu-id="fae17-120"><span id="val3"></span><span id="VAL3"></span>*val3*</span></span><br/>             | <span data-ttu-id="fae17-121">Четвертый байт значения, которое необходимо выделить указанному регистру.</span><span class="sxs-lookup"><span data-stu-id="fae17-121">Fourth byte of the value to allocate to the specified register.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="fae17-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="fae17-122">Remarks</span></span>

<span data-ttu-id="fae17-123">Директива pragma DEF позволяет разработчику предварительно заполнить регистр шейдера с плавающей точкой с указанным значением.</span><span class="sxs-lookup"><span data-stu-id="fae17-123">The def pragma allows a developer to prefill a floating-point shader register with the specified value.</span></span> <span data-ttu-id="fae17-124">Эта директива pragma используется редко.</span><span class="sxs-lookup"><span data-stu-id="fae17-124">This pragma is infrequently used.</span></span>

## <a name="see-also"></a><span data-ttu-id="fae17-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fae17-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fae17-126">Директивы препроцессора (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fae17-126">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[<span data-ttu-id="fae17-127">\#Директива pragma (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fae17-127">\#pragma Directive (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-pre-pragma.md)
</dt> </dl>

 

 





