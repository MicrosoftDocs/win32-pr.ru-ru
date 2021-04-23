---
description: '\_Константы линекаллоригин описывают происхождение вызова.'
ms.assetid: b830a40e-62d9-4a6c-b43f-8318f30a7cd4
title: Константы LINECALLORIGIN_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f00495d67dcff56ef7ee34cd85600a281e006ec3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675245"
---
# <a name="linecallorigin_-constants"></a><span data-ttu-id="2ce1d-103">\_Константы линекаллоригин</span><span class="sxs-lookup"><span data-stu-id="2ce1d-103">LINECALLORIGIN\_ Constants</span></span>

<span data-ttu-id="2ce1d-104">Константы **линекаллоригин \_** описывают происхождение вызова.</span><span class="sxs-lookup"><span data-stu-id="2ce1d-104">The **LINECALLORIGIN\_** constants describe the origin of a call.</span></span>

<dl> <dt>

<span data-ttu-id="2ce1d-105"><span id="LINECALLORIGIN_CONFERENCE"></span><span id="linecallorigin_conference"></span>**\_Конференция линекаллоригин**</span><span class="sxs-lookup"><span data-stu-id="2ce1d-105"><span id="LINECALLORIGIN_CONFERENCE"></span><span id="linecallorigin_conference"></span>**LINECALLORIGIN\_CONFERENCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2ce1d-106">Обработчик вызова предназначен для вызова конференции, т. е. это подключение приложения к мосту конференции в коммутаторе.</span><span class="sxs-lookup"><span data-stu-id="2ce1d-106">The call handle is for a conference call, that is, it is the application's connection to the conference bridge in the switch.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ce1d-107"><span id="LINECALLORIGIN_EXTERNAL"></span><span id="linecallorigin_external"></span>**ЛИНЕКАЛЛОРИГИН \_ внешний**</span><span class="sxs-lookup"><span data-stu-id="2ce1d-107"><span id="LINECALLORIGIN_EXTERNAL"></span><span id="linecallorigin_external"></span>**LINECALLORIGIN\_EXTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2ce1d-108">Вызов создан как входящий вызов на внешней строке.</span><span class="sxs-lookup"><span data-stu-id="2ce1d-108">The call originated as an incoming call on an external line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ce1d-109"><span id="LINECALLORIGIN_INBOUND"></span><span id="linecallorigin_inbound"></span>**ЛИНЕКАЛЛОРИГИН \_ входящий трафик**</span><span class="sxs-lookup"><span data-stu-id="2ce1d-109"><span id="LINECALLORIGIN_INBOUND"></span><span id="linecallorigin_inbound"></span>**LINECALLORIGIN\_INBOUND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2ce1d-110">Вызов создан как входящий вызов, но поставщик услуг не может определить, поступил ли он с другой станции на том же коммутаторе или на внешней строке.</span><span class="sxs-lookup"><span data-stu-id="2ce1d-110">The call originated as an incoming call, but the service provider is unable to determine whether it came from another station on the same switch or from an external line.</span></span> <span data-ttu-id="2ce1d-111">Поставщики услуг могут использовать эту константу только при согласовании TAPI версии 1,4 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="2ce1d-111">Service providers can use this constant only when TAPI version 1.4 or later has been negotiated.</span></span> <span data-ttu-id="2ce1d-112">В противном случае поставщик услуг может заменить ЛИНЕКАЛЛОРИГИН \_ .</span><span class="sxs-lookup"><span data-stu-id="2ce1d-112">Otherwise, the service provider can substitute LINECALLORIGIN\_UNAVAIL.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ce1d-113"><span id="LINECALLORIGIN_INTERNAL"></span><span id="linecallorigin_internal"></span>**\_Внутренняя линекаллоригин**</span><span class="sxs-lookup"><span data-stu-id="2ce1d-113"><span id="LINECALLORIGIN_INTERNAL"></span><span id="linecallorigin_internal"></span>**LINECALLORIGIN\_INTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2ce1d-114">Вызов создан как входящий вызов на станции, внутренней для той же среды коммутации.</span><span class="sxs-lookup"><span data-stu-id="2ce1d-114">The call originated as an incoming call at a station internal to the same switching environment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ce1d-115"><span id="LINECALLORIGIN_OUTBOUND"></span><span id="linecallorigin_outbound"></span>**ЛИНЕКАЛЛОРИГИН \_ исходящий трафик**</span><span class="sxs-lookup"><span data-stu-id="2ce1d-115"><span id="LINECALLORIGIN_OUTBOUND"></span><span id="linecallorigin_outbound"></span>**LINECALLORIGIN\_OUTBOUND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2ce1d-116">Вызов был получен от станции как исходящий вызов.</span><span class="sxs-lookup"><span data-stu-id="2ce1d-116">The call originated from this station as an outgoing call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ce1d-117"><span id="LINECALLORIGIN_UNAVAIL"></span><span id="linecallorigin_unavail"></span>**ЛИНЕКАЛЛОРИГИН \_ НЕсвободно**</span><span class="sxs-lookup"><span data-stu-id="2ce1d-117"><span id="LINECALLORIGIN_UNAVAIL"></span><span id="linecallorigin_unavail"></span>**LINECALLORIGIN\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2ce1d-118">Источник вызова недоступен и никогда не будет известен для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="2ce1d-118">The call origin is not available and will never become known for this call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ce1d-119"><span id="LINECALLORIGIN_UNKNOWN"></span><span id="linecallorigin_unknown"></span>**ЛИНЕКАЛЛОРИГИН \_ неизвестный**</span><span class="sxs-lookup"><span data-stu-id="2ce1d-119"><span id="LINECALLORIGIN_UNKNOWN"></span><span id="linecallorigin_unknown"></span>**LINECALLORIGIN\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2ce1d-120">Источник вызова сейчас неизвестен, но может быть известен позже.</span><span class="sxs-lookup"><span data-stu-id="2ce1d-120">The call origin is currently unknown but may become known later.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2ce1d-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2ce1d-121">Remarks</span></span>

<span data-ttu-id="2ce1d-122">Без расширяемости.</span><span class="sxs-lookup"><span data-stu-id="2ce1d-122">No extensibility.</span></span> <span data-ttu-id="2ce1d-123">Все 32 бит зарезервированы.</span><span class="sxs-lookup"><span data-stu-id="2ce1d-123">All 32 bits are reserved.</span></span>

<span data-ttu-id="2ce1d-124">Источник вызова хранится в элементе **dwOrigin** структуры [**линекаллинфо**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) вызова.</span><span class="sxs-lookup"><span data-stu-id="2ce1d-124">The origin of a call is stored in the **dwOrigin** member of the call's [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ce1d-125">Требования</span><span class="sxs-lookup"><span data-stu-id="2ce1d-125">Requirements</span></span>



| <span data-ttu-id="2ce1d-126">Требование</span><span class="sxs-lookup"><span data-stu-id="2ce1d-126">Requirement</span></span> | <span data-ttu-id="2ce1d-127">Значение</span><span class="sxs-lookup"><span data-stu-id="2ce1d-127">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="2ce1d-128">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="2ce1d-128">TAPI version</span></span><br/> | <span data-ttu-id="2ce1d-129">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="2ce1d-129">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="2ce1d-130">Header</span><span class="sxs-lookup"><span data-stu-id="2ce1d-130">Header</span></span><br/>       | <dl> <span data-ttu-id="2ce1d-131"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ce1d-131"><dt>Tapi.h</dt></span></span> </dl> |



 

 




