---
description: '\_Перечисление событий участника описывает события участников.'
ms.assetid: 678165f2-ad0b-415f-86bf-8c4e3bd8d793
title: Перечисление PARTICIPANT_EVENT (Ипмсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 225b1b9901efa5648dfaa326c53ed69cff2c4295
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685444"
---
# <a name="participant_event-enumeration"></a><span data-ttu-id="533f9-103">\_Перечисление событий участников</span><span class="sxs-lookup"><span data-stu-id="533f9-103">PARTICIPANT\_EVENT enumeration</span></span>

<span data-ttu-id="533f9-104">\[ Это перечисление недоступно для использования в Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="533f9-104">\[ This enumeration is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="533f9-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="533f9-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="533f9-106">Перечисление **\_ событий участника** описывает события участников.</span><span class="sxs-lookup"><span data-stu-id="533f9-106">The **PARTICIPANT\_EVENT** enum describes participant events.</span></span> <span data-ttu-id="533f9-107">Метод [**\_ события итпартиЦипантевент:: Get**](itparticipantevent-get-event.md) возвращает член этого перечисления для указания типа произошедшего события участника конференции.</span><span class="sxs-lookup"><span data-stu-id="533f9-107">The [**ITParticipantEvent::get\_Event**](itparticipantevent-get-event.md) method returns a member of this enum to indicate the type of conference participant event that occurred.</span></span> <span data-ttu-id="533f9-108">Это перечисление используется приложениями, которые обращаются к [ИПКОНФ MSP](ipconf-msp.md).</span><span class="sxs-lookup"><span data-stu-id="533f9-108">This enum is used by applications that access the [IPConf MSP](ipconf-msp.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="533f9-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="533f9-109">Syntax</span></span>


```C++
} PARTICIPANT_EVENT;
```



## <a name="constants"></a><span data-ttu-id="533f9-110">Константы</span><span class="sxs-lookup"><span data-stu-id="533f9-110">Constants</span></span>

<dl> <dt>

<span data-ttu-id="533f9-111"><span id="PE_NEW_PARTICIPANT"></span><span id="pe_new_participant"></span>**\_новый \_ участник PE**</span><span class="sxs-lookup"><span data-stu-id="533f9-111"><span id="PE_NEW_PARTICIPANT"></span><span id="pe_new_participant"></span>**PE\_NEW\_PARTICIPANT**</span></span>
</dt> <dd>

<span data-ttu-id="533f9-112">На конференцию был добавлен новый участник.</span><span class="sxs-lookup"><span data-stu-id="533f9-112">A new participant has been added to the conference.</span></span>

</dd> <dt>

<span data-ttu-id="533f9-113"><span id="PE_INFO_CHANGE"></span><span id="pe_info_change"></span>**\_изменение сведений \_ PE**</span><span class="sxs-lookup"><span data-stu-id="533f9-113"><span id="PE_INFO_CHANGE"></span><span id="pe_info_change"></span>**PE\_INFO\_CHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="533f9-114">Изменились сведения об участнике.</span><span class="sxs-lookup"><span data-stu-id="533f9-114">Information on a participant has changed.</span></span>

</dd> <dt>

<span data-ttu-id="533f9-115"><span id="PE_PARTICIPANT_LEAVE"></span><span id="pe_participant_leave"></span>**\_Выход участника \_ PE**</span><span class="sxs-lookup"><span data-stu-id="533f9-115"><span id="PE_PARTICIPANT_LEAVE"></span><span id="pe_participant_leave"></span>**PE\_PARTICIPANT\_LEAVE**</span></span>
</dt> <dd>

<span data-ttu-id="533f9-116">Участник покинул конференцию.</span><span class="sxs-lookup"><span data-stu-id="533f9-116">A participant has left the conference.</span></span>

</dd> <dt>

<span data-ttu-id="533f9-117"><span id="PE_NEW_SUBSTREAM"></span><span id="pe_new_substream"></span>**\_новый \_ ПОДпоток PE**</span><span class="sxs-lookup"><span data-stu-id="533f9-117"><span id="PE_NEW_SUBSTREAM"></span><span id="pe_new_substream"></span>**PE\_NEW\_SUBSTREAM**</span></span>
</dt> <dd>

<span data-ttu-id="533f9-118">К участнику добавлен новый подпоток.</span><span class="sxs-lookup"><span data-stu-id="533f9-118">A new substream has been added to the participant.</span></span>

</dd> <dt>

<span data-ttu-id="533f9-119"><span id="PE_SUBSTREAM_REMOVED"></span><span id="pe_substream_removed"></span>**\_ПОДПОТОК PE \_ удален**</span><span class="sxs-lookup"><span data-stu-id="533f9-119"><span id="PE_SUBSTREAM_REMOVED"></span><span id="pe_substream_removed"></span>**PE\_SUBSTREAM\_REMOVED**</span></span>
</dt> <dd>

<span data-ttu-id="533f9-120">Новый подпоток был удален из участника.</span><span class="sxs-lookup"><span data-stu-id="533f9-120">A new substream has been removed from the participant.</span></span>

</dd> <dt>

<span data-ttu-id="533f9-121"><span id="PE_SUBSTREAM_MAPPED"></span><span id="pe_substream_mapped"></span>**\_сопоставленный ПОДПОТОК PE \_**</span><span class="sxs-lookup"><span data-stu-id="533f9-121"><span id="PE_SUBSTREAM_MAPPED"></span><span id="pe_substream_mapped"></span>**PE\_SUBSTREAM\_MAPPED**</span></span>
</dt> <dd>

<span data-ttu-id="533f9-122">Участник сопоставлен с подпотоком.</span><span class="sxs-lookup"><span data-stu-id="533f9-122">A participant has been mapped to a substream.</span></span>

</dd> <dt>

<span data-ttu-id="533f9-123"><span id="PE_SUBSTREAM_UNMAPPED"></span><span id="pe_substream_unmapped"></span>**подпоток PE не \_ \_ сопоставлен**</span><span class="sxs-lookup"><span data-stu-id="533f9-123"><span id="PE_SUBSTREAM_UNMAPPED"></span><span id="pe_substream_unmapped"></span>**PE\_SUBSTREAM\_UNMAPPED**</span></span>
</dt> <dd>

<span data-ttu-id="533f9-124">Участник был отменен из подпотока.</span><span class="sxs-lookup"><span data-stu-id="533f9-124">A participant has been unmapped from a substream.</span></span>

</dd> <dt>

<span data-ttu-id="533f9-125"><span id="PE_PARTICIPANT_TIMEOUT"></span><span id="pe_participant_timeout"></span>**\_ \_ время ожидания участника PE**</span><span class="sxs-lookup"><span data-stu-id="533f9-125"><span id="PE_PARTICIPANT_TIMEOUT"></span><span id="pe_participant_timeout"></span>**PE\_PARTICIPANT\_TIMEOUT**</span></span>
</dt> <dd>

<span data-ttu-id="533f9-126">Участник был удален из конференции из-за истечения времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="533f9-126">A participant has been removed from the conference due to a timeout.</span></span>

</dd> <dt>

<span data-ttu-id="533f9-127"><span id="PE_PARTICIPANT_RECOVERED"></span><span id="pe_participant_recovered"></span>**\_участник PE \_ восстановлен**</span><span class="sxs-lookup"><span data-stu-id="533f9-127"><span id="PE_PARTICIPANT_RECOVERED"></span><span id="pe_participant_recovered"></span>**PE\_PARTICIPANT\_RECOVERED**</span></span>
</dt> <dd>

<span data-ttu-id="533f9-128">Удаленный участник снова становится видимым.</span><span class="sxs-lookup"><span data-stu-id="533f9-128">A removed participant is again visible.</span></span> <span data-ttu-id="533f9-129">Как правило, это участник, для которого истекло время ожидания, но теперь получаются сигналы.</span><span class="sxs-lookup"><span data-stu-id="533f9-129">Usually, this is a participant who timed out but signals are now being received.</span></span>

</dd> <dt>

<span data-ttu-id="533f9-130"><span id="PE_PARTICIPANT_ACTIVE"></span><span id="pe_participant_active"></span>**\_участник PE \_ активен**</span><span class="sxs-lookup"><span data-stu-id="533f9-130"><span id="PE_PARTICIPANT_ACTIVE"></span><span id="pe_participant_active"></span>**PE\_PARTICIPANT\_ACTIVE**</span></span>
</dt> <dd>

<span data-ttu-id="533f9-131">Участник стал активным на Конференции.</span><span class="sxs-lookup"><span data-stu-id="533f9-131">The participant has become active in the conference.</span></span>

</dd> <dt>

<span data-ttu-id="533f9-132"><span id="PE_PARTICIPANT_INACTIVE"></span><span id="pe_participant_inactive"></span>**\_участник PE \_ неактивен**</span><span class="sxs-lookup"><span data-stu-id="533f9-132"><span id="PE_PARTICIPANT_INACTIVE"></span><span id="pe_participant_inactive"></span>**PE\_PARTICIPANT\_INACTIVE**</span></span>
</dt> <dd>

<span data-ttu-id="533f9-133">Участник стал неактивным на Конференции.</span><span class="sxs-lookup"><span data-stu-id="533f9-133">The participant has become inactive in the conference.</span></span>

</dd> <dt>

<span data-ttu-id="533f9-134"><span id="PE_LOCAL_TALKING"></span><span id="pe_local_talking"></span>**\_локальный \_ разговор PE**</span><span class="sxs-lookup"><span data-stu-id="533f9-134"><span id="PE_LOCAL_TALKING"></span><span id="pe_local_talking"></span>**PE\_LOCAL\_TALKING**</span></span>
</dt> <dd>

<span data-ttu-id="533f9-135">Локальный участник начал говорить.</span><span class="sxs-lookup"><span data-stu-id="533f9-135">The local participant has started to talk.</span></span>

</dd> <dt>

<span data-ttu-id="533f9-136"><span id="PE_LOCAL_SILENT"></span><span id="pe_local_silent"></span>**\_Локальное \_ Автоматическое выполнение PE**</span><span class="sxs-lookup"><span data-stu-id="533f9-136"><span id="PE_LOCAL_SILENT"></span><span id="pe_local_silent"></span>**PE\_LOCAL\_SILENT**</span></span>
</dt> <dd>

<span data-ttu-id="533f9-137">Локальный участник стал незамеченным на Конференции.</span><span class="sxs-lookup"><span data-stu-id="533f9-137">The local participant has become silent in the conference.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="533f9-138">Требования</span><span class="sxs-lookup"><span data-stu-id="533f9-138">Requirements</span></span>



| <span data-ttu-id="533f9-139">Требование</span><span class="sxs-lookup"><span data-stu-id="533f9-139">Requirement</span></span> | <span data-ttu-id="533f9-140">Значение</span><span class="sxs-lookup"><span data-stu-id="533f9-140">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="533f9-141">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="533f9-141">TAPI version</span></span><br/> | <span data-ttu-id="533f9-142">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="533f9-142">Requires TAPI 3.0 or later</span></span><br/>                                              |
| <span data-ttu-id="533f9-143">Header</span><span class="sxs-lookup"><span data-stu-id="533f9-143">Header</span></span><br/>       | <dl> <span data-ttu-id="533f9-144"><dt>Ипмсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="533f9-144"><dt>Ipmsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="533f9-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="533f9-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="533f9-146">**Событие ИтпартиЦипантевент:: Get \_**</span><span class="sxs-lookup"><span data-stu-id="533f9-146">**ITParticipantEvent::get\_Event**</span></span>](itparticipantevent-get-event.md)
</dt> <dt>

[<span data-ttu-id="533f9-147">Ипконф MSP</span><span class="sxs-lookup"><span data-stu-id="533f9-147">IPConf MSP</span></span>](ipconf-msp.md)
</dt> <dt>

[<span data-ttu-id="533f9-148">Интерфейсы MSP Ипконф</span><span class="sxs-lookup"><span data-stu-id="533f9-148">IPConf MSP Interfaces</span></span>](ipconf-msp-interfaces.md)
</dt> </dl>

 

 




