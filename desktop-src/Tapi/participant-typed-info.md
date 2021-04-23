---
description: 'Члены \_ перечисления типизированных сведений участника \_ определяют тип сведений о участнике, извлекаемых методом итпартиЦипант:: Get \_ партиЦипанттипединфо. Это перечисление используется приложениями, которые обращаются к Ипконф MSP.'
ms.assetid: ca933d8c-bfb4-4a92-b412-112e228ccca2
title: Перечисление PARTICIPANT_TYPED_INFO (Конфприв. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16ab94a487f0ea098ee9b92144874057dc463036
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675394"
---
# <a name="participant_typed_info-enumeration"></a><span data-ttu-id="aa47b-104">\_Перечисление типизированных \_ сведений участника</span><span class="sxs-lookup"><span data-stu-id="aa47b-104">PARTICIPANT\_TYPED\_INFO enumeration</span></span>

<span data-ttu-id="aa47b-105">\[**Участник \_ ТИПИЗИРОВАНная \_ информация** недоступна для использования в Windows Vista, windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="aa47b-105">\[**PARTICIPANT\_TYPED\_INFO** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="aa47b-106">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="aa47b-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="aa47b-107">Члены перечисления **\_ типизированных \_ сведений участника** определяют тип сведений о участнике, извлекаемых методом [**итпартиЦипант:: Get \_ партиЦипанттипединфо**](itparticipant-get-participanttypedinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="aa47b-107">The members of the **PARTICIPANT\_TYPED\_INFO** enum identify the type of participant information being retrieved by the [**ITParticipant::get\_ParticipantTypedInfo**](itparticipant-get-participanttypedinfo.md) method.</span></span> <span data-ttu-id="aa47b-108">Это перечисление используется приложениями, которые обращаются к [ИПКОНФ MSP](ipconf-msp.md).</span><span class="sxs-lookup"><span data-stu-id="aa47b-108">This enum is used by applications that access the [IPConf MSP](ipconf-msp.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="aa47b-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="aa47b-109">Syntax</span></span>


```C++
} PARTICIPANT_TYPED_INFO;
```



## <a name="constants"></a><span data-ttu-id="aa47b-110">Константы</span><span class="sxs-lookup"><span data-stu-id="aa47b-110">Constants</span></span>

<dl> <dt>

<span data-ttu-id="aa47b-111"><span id="PTI_CANONICALNAME"></span><span id="pti_canonicalname"></span>**Пти \_ каноникалнаме**</span><span class="sxs-lookup"><span data-stu-id="aa47b-111"><span id="PTI_CANONICALNAME"></span><span id="pti_canonicalname"></span>**PTI\_CANONICALNAME**</span></span>
</dt> <dd>

<span data-ttu-id="aa47b-112">Каноническое имя участника, например someone@example.com .</span><span class="sxs-lookup"><span data-stu-id="aa47b-112">Canonical name of participant, such as someone@example.com.</span></span>

</dd> <dt>

<span data-ttu-id="aa47b-113"><span id="PTI_NAME"></span><span id="pti_name"></span>**\_имя Пти**</span><span class="sxs-lookup"><span data-stu-id="aa47b-113"><span id="PTI_NAME"></span><span id="pti_name"></span>**PTI\_NAME**</span></span>
</dt> <dd>

<span data-ttu-id="aa47b-114">Отображаемое имя участника.</span><span class="sxs-lookup"><span data-stu-id="aa47b-114">Displayable name of participant.</span></span>

</dd> <dt>

<span data-ttu-id="aa47b-115"><span id="PTI_EMAILADDRESS"></span><span id="pti_emailaddress"></span>**Пти \_ EMAILADDRESS**</span><span class="sxs-lookup"><span data-stu-id="aa47b-115"><span id="PTI_EMAILADDRESS"></span><span id="pti_emailaddress"></span>**PTI\_EMAILADDRESS**</span></span>
</dt> <dd>

<span data-ttu-id="aa47b-116">Адрес электронной почты участника.</span><span class="sxs-lookup"><span data-stu-id="aa47b-116">Participant's email address.</span></span>

</dd> <dt>

<span data-ttu-id="aa47b-117"><span id="PTI_PHONENUMBER"></span><span id="pti_phonenumber"></span>**Пти \_ PHONENUMBER**</span><span class="sxs-lookup"><span data-stu-id="aa47b-117"><span id="PTI_PHONENUMBER"></span><span id="pti_phonenumber"></span>**PTI\_PHONENUMBER**</span></span>
</dt> <dd>

<span data-ttu-id="aa47b-118">Телефонный адрес участника.</span><span class="sxs-lookup"><span data-stu-id="aa47b-118">Participant's phone address.</span></span>

</dd> <dt>

<span data-ttu-id="aa47b-119"><span id="PTI_LOCATION"></span><span id="pti_location"></span>**\_Расположение Пти**</span><span class="sxs-lookup"><span data-stu-id="aa47b-119"><span id="PTI_LOCATION"></span><span id="pti_location"></span>**PTI\_LOCATION**</span></span>
</dt> <dd>

<span data-ttu-id="aa47b-120">Географический адрес участника.</span><span class="sxs-lookup"><span data-stu-id="aa47b-120">Participant's geographical address.</span></span>

</dd> <dt>

<span data-ttu-id="aa47b-121"><span id="PTI_TOOL"></span><span id="pti_tool"></span>**\_средство Пти**</span><span class="sxs-lookup"><span data-stu-id="aa47b-121"><span id="PTI_TOOL"></span><span id="pti_tool"></span>**PTI\_TOOL**</span></span>
</dt> <dd>

<span data-ttu-id="aa47b-122">Приложение участника.</span><span class="sxs-lookup"><span data-stu-id="aa47b-122">Participant's application.</span></span>

</dd> <dt>

<span data-ttu-id="aa47b-123"><span id="PTI_NOTES"></span><span id="pti_notes"></span>**\_заметки Пти**</span><span class="sxs-lookup"><span data-stu-id="aa47b-123"><span id="PTI_NOTES"></span><span id="pti_notes"></span>**PTI\_NOTES**</span></span>
</dt> <dd>

<span data-ttu-id="aa47b-124">Примечания, касающиеся участников.</span><span class="sxs-lookup"><span data-stu-id="aa47b-124">Notes concerning participant.</span></span>

</dd> <dt>

<span data-ttu-id="aa47b-125"><span id="PTI_PRIVATE"></span><span id="pti_private"></span>**Пти \_ закрытый**</span><span class="sxs-lookup"><span data-stu-id="aa47b-125"><span id="PTI_PRIVATE"></span><span id="pti_private"></span>**PTI\_PRIVATE**</span></span>
</dt> <dd>

<span data-ttu-id="aa47b-126">Определяет экспериментальное или зависящее от приложения расширение источника (СДЕС).</span><span class="sxs-lookup"><span data-stu-id="aa47b-126">Defines an experimental or application-specific Source Description (SDES) extension.</span></span> <span data-ttu-id="aa47b-127">Дополнительные сведения см. в RFC 1889.</span><span class="sxs-lookup"><span data-stu-id="aa47b-127">See RFC 1889 for details.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="aa47b-128">Требования</span><span class="sxs-lookup"><span data-stu-id="aa47b-128">Requirements</span></span>



| <span data-ttu-id="aa47b-129">Требование</span><span class="sxs-lookup"><span data-stu-id="aa47b-129">Requirement</span></span> | <span data-ttu-id="aa47b-130">Значение</span><span class="sxs-lookup"><span data-stu-id="aa47b-130">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="aa47b-131">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="aa47b-131">TAPI version</span></span><br/> | <span data-ttu-id="aa47b-132">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="aa47b-132">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="aa47b-133">Header</span><span class="sxs-lookup"><span data-stu-id="aa47b-133">Header</span></span><br/>       | <dl> <span data-ttu-id="aa47b-134"><dt>Конфприв. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa47b-134"><dt>Confpriv.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa47b-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="aa47b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa47b-136">**ИтпартиЦипант:: Get \_ партиЦипанттипединфо**</span><span class="sxs-lookup"><span data-stu-id="aa47b-136">**ITParticipant::get\_ParticipantTypedInfo**</span></span>](itparticipant-get-participanttypedinfo.md)
</dt> <dt>

[<span data-ttu-id="aa47b-137">Ипконф MSP</span><span class="sxs-lookup"><span data-stu-id="aa47b-137">IPConf MSP</span></span>](ipconf-msp.md)
</dt> <dt>

[<span data-ttu-id="aa47b-138">Интерфейсы MSP Ипконф</span><span class="sxs-lookup"><span data-stu-id="aa47b-138">IPConf MSP Interfaces</span></span>](ipconf-msp-interfaces.md)
</dt> </dl>

 

 




