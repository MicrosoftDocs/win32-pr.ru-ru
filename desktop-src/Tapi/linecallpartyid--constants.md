---
description: '\_Константы побитового флага линекаллпартид описывают характер доступной информации о сторонах, вовлеченных в вызов.'
ms.assetid: e2a89f25-15f0-4f3c-9ac8-1e6b72c0d8db
title: Константы LINECALLPARTYID_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5dd8cca75fe6e91b97fac63dca6c0fdda554394
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689388"
---
# <a name="linecallpartyid_-constants"></a><span data-ttu-id="e8d72-103">\_Константы линекаллпартид</span><span class="sxs-lookup"><span data-stu-id="e8d72-103">LINECALLPARTYID\_ Constants</span></span>

<span data-ttu-id="e8d72-104">Константы побитового флага **линекаллпартид \_** описывают характер доступной информации о сторонах, вовлеченных в вызов.</span><span class="sxs-lookup"><span data-stu-id="e8d72-104">The **LINECALLPARTYID\_** bit-flag constants describe the nature of the information available about the parties involved in a call.</span></span>

<dl> <dt>

<span data-ttu-id="e8d72-105"><span id="LINECALLPARTYID_ADDRESS"></span><span id="linecallpartyid_address"></span>**ЛИНЕКАЛЛПАРТИД \_ адрес**</span><span class="sxs-lookup"><span data-stu-id="e8d72-105"><span id="LINECALLPARTYID_ADDRESS"></span><span id="linecallpartyid_address"></span>**LINECALLPARTYID\_ADDRESS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e8d72-106">Сведения об идентификаторе субъекта состоят из адреса субъекта в каноническом формате адреса или в формате коммутируемого адреса.</span><span class="sxs-lookup"><span data-stu-id="e8d72-106">Party identifier information consists of the party's address in either canonical address format or dialable address format.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8d72-107"><span id="LINECALLPARTYID_BLOCKED"></span><span id="linecallpartyid_blocked"></span>**ЛИНЕКАЛЛПАРТИД \_ заблокирована**</span><span class="sxs-lookup"><span data-stu-id="e8d72-107"><span id="LINECALLPARTYID_BLOCKED"></span><span id="linecallpartyid_blocked"></span>**LINECALLPARTYID\_BLOCKED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e8d72-108">Сведения об идентификаторе субъекта недоступны, так как они заблокированы удаленной стороной.</span><span class="sxs-lookup"><span data-stu-id="e8d72-108">Party identifier information is not available because it has been blocked by the remote party.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8d72-109"><span id="LINECALLPARTYID_NAME"></span><span id="linecallpartyid_name"></span>**\_имя линекаллпартид**</span><span class="sxs-lookup"><span data-stu-id="e8d72-109"><span id="LINECALLPARTYID_NAME"></span><span id="linecallpartyid_name"></span>**LINECALLPARTYID\_NAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e8d72-110">Сведения об идентификаторе субъекта состоят из имени стороны (например, из каталога, который хранится внутри коммутатора).</span><span class="sxs-lookup"><span data-stu-id="e8d72-110">Party identifier information consists of the party's name (as, for example, from a directory kept inside the switch).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8d72-111"><span id="LINECALLPARTYID_OUTOFAREA"></span><span id="linecallpartyid_outofarea"></span>**ЛИНЕКАЛЛПАРТИД \_ аутофареа**</span><span class="sxs-lookup"><span data-stu-id="e8d72-111"><span id="LINECALLPARTYID_OUTOFAREA"></span><span id="linecallpartyid_outofarea"></span>**LINECALLPARTYID\_OUTOFAREA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e8d72-112">Сведения об ИДЕНТИФИКАТОРе вызывающего объекта недоступны, так как они не распространяются по сети.</span><span class="sxs-lookup"><span data-stu-id="e8d72-112">Caller ID information for the call is not available because it is not propagated all the way by the network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8d72-113"><span id="LINECALLPARTYID_PARTIAL"></span><span id="linecallpartyid_partial"></span>**ЛИНЕКАЛЛПАРТИД \_ частичный**</span><span class="sxs-lookup"><span data-stu-id="e8d72-113"><span id="LINECALLPARTYID_PARTIAL"></span><span id="linecallpartyid_partial"></span>**LINECALLPARTYID\_PARTIAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e8d72-114">Сведения об идентификаторе субъекта допустимы, но ограничены только частичными сведениями.</span><span class="sxs-lookup"><span data-stu-id="e8d72-114">Party identifier information is valid but it is limited to partial information only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8d72-115"><span id="LINECALLPARTYID_UNAVAIL"></span><span id="linecallpartyid_unavail"></span>**ЛИНЕКАЛЛПАРТИД \_ НЕсвободно**</span><span class="sxs-lookup"><span data-stu-id="e8d72-115"><span id="LINECALLPARTYID_UNAVAIL"></span><span id="linecallpartyid_unavail"></span>**LINECALLPARTYID\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e8d72-116">Сведения об идентификаторе субъекта недоступны и станут недоступны позже.</span><span class="sxs-lookup"><span data-stu-id="e8d72-116">Party identifier information is not available and will not become available later.</span></span> <span data-ttu-id="e8d72-117">Сведения могут быть недоступны по неопределенным причинам.</span><span class="sxs-lookup"><span data-stu-id="e8d72-117">Information may be unavailable for unspecified reasons.</span></span> <span data-ttu-id="e8d72-118">Например, информация не была доставлена сетью, она была пропущена поставщиком услуг и т. д.</span><span class="sxs-lookup"><span data-stu-id="e8d72-118">For example, the information was not delivered by the network, it was ignored by the service provider, and so forth.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8d72-119"><span id="LINECALLPARTYID_UNKNOWN"></span><span id="linecallpartyid_unknown"></span>**ЛИНЕКАЛЛПАРТИД \_ неизвестный**</span><span class="sxs-lookup"><span data-stu-id="e8d72-119"><span id="LINECALLPARTYID_UNKNOWN"></span><span id="linecallpartyid_unknown"></span>**LINECALLPARTYID\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e8d72-120">Сведения об идентификаторе субъекта в настоящее время неизвестны, но могут быть известны позже.</span><span class="sxs-lookup"><span data-stu-id="e8d72-120">Party identifier information is currently unknown but may become known later.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e8d72-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e8d72-121">Remarks</span></span>

<span data-ttu-id="e8d72-122">Без расширяемости.</span><span class="sxs-lookup"><span data-stu-id="e8d72-122">No extensibility.</span></span> <span data-ttu-id="e8d72-123">Все 32 бит зарезервированы.</span><span class="sxs-lookup"><span data-stu-id="e8d72-123">All 32 bits are reserved.</span></span>

<span data-ttu-id="e8d72-124">Для каждой из возможных сторон, участвующих в вызове, константы **линекаллпартид \_** описывают форматирование сведений об идентификаторе субъекта.</span><span class="sxs-lookup"><span data-stu-id="e8d72-124">For each of the possible parties involved in a call, the **LINECALLPARTYID\_** constants describe how the party identifier information is formatted.</span></span> <span data-ttu-id="e8d72-125">Эта информация предоставляется в структуре данных [**линекаллинфо**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) .</span><span class="sxs-lookup"><span data-stu-id="e8d72-125">This information is supplied in the [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) data structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8d72-126">Требования</span><span class="sxs-lookup"><span data-stu-id="e8d72-126">Requirements</span></span>



| <span data-ttu-id="e8d72-127">Требование</span><span class="sxs-lookup"><span data-stu-id="e8d72-127">Requirement</span></span> | <span data-ttu-id="e8d72-128">Значение</span><span class="sxs-lookup"><span data-stu-id="e8d72-128">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="e8d72-129">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="e8d72-129">TAPI version</span></span><br/> | <span data-ttu-id="e8d72-130">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="e8d72-130">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="e8d72-131">Header</span><span class="sxs-lookup"><span data-stu-id="e8d72-131">Header</span></span><br/>       | <dl> <span data-ttu-id="e8d72-132"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8d72-132"><dt>Tapi.h</dt></span></span> </dl> |



 

 




