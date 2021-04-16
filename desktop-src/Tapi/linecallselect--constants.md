---
description: '\_Константы побитового флага линекаллселект описывают, какие вызовы должны быть выбраны.'
ms.assetid: f19a41bc-403a-4d4b-ab85-240a73514ebb
title: Константы LINECALLSELECT_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8330b4c4e4e14ac399595d10d4a208a3c67f5b2a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679904"
---
# <a name="linecallselect_-constants"></a><span data-ttu-id="481b3-103">\_Константы линекаллселект</span><span class="sxs-lookup"><span data-stu-id="481b3-103">LINECALLSELECT\_ Constants</span></span>

<span data-ttu-id="481b3-104">Константы побитового флага **линекаллселект \_** описывают, какие вызовы должны быть выбраны.</span><span class="sxs-lookup"><span data-stu-id="481b3-104">The **LINECALLSELECT\_** bit-flag constants describe which calls are to be selected.</span></span>

<dl> <dt>

<span data-ttu-id="481b3-105"><span id="LINECALLSELECT_ADDRESS"></span><span id="linecallselect_address"></span>**ЛИНЕКАЛЛСЕЛЕКТ \_ адрес**</span><span class="sxs-lookup"><span data-stu-id="481b3-105"><span id="LINECALLSELECT_ADDRESS"></span><span id="linecallselect_address"></span>**LINECALLSELECT\_ADDRESS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="481b3-106">Выбирает вызов по указанному адресу.</span><span class="sxs-lookup"><span data-stu-id="481b3-106">Selects call on the specified address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="481b3-107"><span id="LINECALLSELECT_CALL"></span><span id="linecallselect_call"></span>**\_вызов линекаллселект**</span><span class="sxs-lookup"><span data-stu-id="481b3-107"><span id="LINECALLSELECT_CALL"></span><span id="linecallselect_call"></span>**LINECALLSELECT\_CALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="481b3-108">Выбирает связанные вызовы для указанного вызова.</span><span class="sxs-lookup"><span data-stu-id="481b3-108">Selects related calls to the specified call.</span></span> <span data-ttu-id="481b3-109">Например, участники конференц-связи.</span><span class="sxs-lookup"><span data-stu-id="481b3-109">For example, the parties in a conference call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="481b3-110"><span id="LINECALLSELECT_CALLID"></span><span id="linecallselect_callid"></span>**ЛИНЕКАЛЛСЕЛЕКТ \_ каллид**</span><span class="sxs-lookup"><span data-stu-id="481b3-110"><span id="LINECALLSELECT_CALLID"></span><span id="linecallselect_callid"></span>**LINECALLSELECT\_CALLID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="481b3-111">Выбирает связанные вызовы к указанному идентификатору вызова.</span><span class="sxs-lookup"><span data-stu-id="481b3-111">Selects related calls to the specified call identifier.</span></span> <span data-ttu-id="481b3-112">Этот флаг предоставляется только приложениям, которые согласовывают версию TAPI 3,0 или более позднюю.</span><span class="sxs-lookup"><span data-stu-id="481b3-112">This flag is exposed only to applications that negotiate a TAPI version of 3.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="481b3-113"><span id="LINECALLSELECT_DEVICEID"></span><span id="linecallselect_deviceid"></span>**DEVICEID для ЛИНЕКАЛЛСЕЛЕКТ \_**</span><span class="sxs-lookup"><span data-stu-id="481b3-113"><span id="LINECALLSELECT_DEVICEID"></span><span id="linecallselect_deviceid"></span>**LINECALLSELECT\_DEVICEID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="481b3-114">Выбирает вызовы по указанному идентификатору устройства.</span><span class="sxs-lookup"><span data-stu-id="481b3-114">Selects calls on the specified device identifier.</span></span> <span data-ttu-id="481b3-115">Этот флаг предоставляется только приложениям, которые согласовывают версию TAPI 2,1 или более позднюю.</span><span class="sxs-lookup"><span data-stu-id="481b3-115">This flag is exposed only to applications that negotiate a TAPI version of 2.1 or higher.</span></span> <span data-ttu-id="481b3-116">В приложениях следует использовать \_ константу строки линекаллселект, а не ее.</span><span class="sxs-lookup"><span data-stu-id="481b3-116">Applications should consider using the LINECALLSELECT\_LINE constant instead of this one.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="481b3-117"><span id="LINECALLSELECT_LINE"></span><span id="linecallselect_line"></span>**ЛИНЕКАЛЛСЕЛЕКТ \_ строка**</span><span class="sxs-lookup"><span data-stu-id="481b3-117"><span id="LINECALLSELECT_LINE"></span><span id="linecallselect_line"></span>**LINECALLSELECT\_LINE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="481b3-118">Выбирает вызовы на указанном устройстве линии.</span><span class="sxs-lookup"><span data-stu-id="481b3-118">Selects calls on the specified line device.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="481b3-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="481b3-119">Remarks</span></span>

<span data-ttu-id="481b3-120">Без расширяемости.</span><span class="sxs-lookup"><span data-stu-id="481b3-120">No extensibility.</span></span> <span data-ttu-id="481b3-121">Все 32 бит зарезервированы.</span><span class="sxs-lookup"><span data-stu-id="481b3-121">All 32 bits are reserved.</span></span>

<span data-ttu-id="481b3-122">Эта константа используется в [**линежетневкаллс**](/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls) и для указания выбора (области) запрашиваемых вызовов.</span><span class="sxs-lookup"><span data-stu-id="481b3-122">This constant is used in [**lineGetNewCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls) and to specify a selection (scope) of the calls that are requested.</span></span>

## <a name="requirements"></a><span data-ttu-id="481b3-123">Требования</span><span class="sxs-lookup"><span data-stu-id="481b3-123">Requirements</span></span>



| <span data-ttu-id="481b3-124">Требование</span><span class="sxs-lookup"><span data-stu-id="481b3-124">Requirement</span></span> | <span data-ttu-id="481b3-125">Значение</span><span class="sxs-lookup"><span data-stu-id="481b3-125">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="481b3-126">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="481b3-126">TAPI version</span></span><br/> | <span data-ttu-id="481b3-127">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="481b3-127">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="481b3-128">Header</span><span class="sxs-lookup"><span data-stu-id="481b3-128">Header</span></span><br/>       | <dl> <span data-ttu-id="481b3-129"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="481b3-129"><dt>Tapi.h</dt></span></span> </dl> |



 

 




