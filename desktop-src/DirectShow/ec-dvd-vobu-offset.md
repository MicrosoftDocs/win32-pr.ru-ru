---
description: EC_DVD_VOBU_Offset — отправляется, когда Навигатор DVD выполняет синтаксический анализ пакета PCI.
ms.assetid: e2e65007-7c34-4be4-86b9-9491061891e5
title: EC_DVD_VOBU_Offset (Двдевкоде. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_VOBU_Offset
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 9223f2d5bb25d7b950dba8fb19c152cf3184af93
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119772"
---
# <a name="ec_dvd_vobu_offset"></a><span data-ttu-id="86fc6-103">\_Смещение вобу DVD-диска EC \_ \_</span><span class="sxs-lookup"><span data-stu-id="86fc6-103">EC\_DVD\_VOBU\_Offset</span></span>

<span data-ttu-id="86fc6-104">Отправляется, когда [Навигатор DVD](dvd-navigator-filter.md) АНАЛИЗИРУЕТ пакет PCI.</span><span class="sxs-lookup"><span data-stu-id="86fc6-104">Sent when the [DVD Navigator](dvd-navigator-filter.md) parses a PCI packet.</span></span>

## <a name="parameters"></a><span data-ttu-id="86fc6-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="86fc6-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86fc6-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="86fc6-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="86fc6-107">Смещение блока последней единицы видео объекта (ВОБУ).</span><span class="sxs-lookup"><span data-stu-id="86fc6-107">The block offset of the most recent video object unit (VOBU).</span></span>

</dd> <dt>

<span data-ttu-id="86fc6-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="86fc6-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="86fc6-109">Номер текущего набора заголовков видео (ВТСН).</span><span class="sxs-lookup"><span data-stu-id="86fc6-109">The current video title set number (VTSN).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="86fc6-110">Remarks</span><span class="sxs-lookup"><span data-stu-id="86fc6-110">Remarks</span></span>

<span data-ttu-id="86fc6-111">По умолчанию это событие отключено.</span><span class="sxs-lookup"><span data-stu-id="86fc6-111">This event is disabled by default.</span></span> <span data-ttu-id="86fc6-112">Чтобы включить это событие, вызовите [**IDvdControl2:: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) и установите для параметра **\_ енаблелоггинжевентс DVD** значение **true**.</span><span class="sxs-lookup"><span data-stu-id="86fc6-112">To enable this event, call [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) and set the **DVD\_EnableLoggingEvents** option to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="86fc6-113">Требования</span><span class="sxs-lookup"><span data-stu-id="86fc6-113">Requirements</span></span>



| <span data-ttu-id="86fc6-114">Требование</span><span class="sxs-lookup"><span data-stu-id="86fc6-114">Requirement</span></span> | <span data-ttu-id="86fc6-115">Значение</span><span class="sxs-lookup"><span data-stu-id="86fc6-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86fc6-116">Header</span><span class="sxs-lookup"><span data-stu-id="86fc6-116">Header</span></span><br/> | <dl> <span data-ttu-id="86fc6-117"><dt>Двдевкоде. h (включение DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="86fc6-117"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86fc6-118">См. также</span><span class="sxs-lookup"><span data-stu-id="86fc6-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86fc6-119">DVD-приложения</span><span class="sxs-lookup"><span data-stu-id="86fc6-119">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="86fc6-120">Коды уведомлений о событиях DVD</span><span class="sxs-lookup"><span data-stu-id="86fc6-120">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="86fc6-121">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="86fc6-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




