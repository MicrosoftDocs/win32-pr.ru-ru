---
description: Указывает, что воспроизведение DVD-диска было остановлено. Это событие отправляется, когда завершается заголовок или глава и Навигатор DVD не находит никаких других инструкций ветвления для последующего воспроизведения. Событие не отправляется, когда приложение останавливает воспроизведение.
ms.assetid: c8617307-d70e-48af-8e85-69105595aa10
title: EC_DVD_PLAYBACK_STOPPED (Двдевкоде. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_PLAYBACK_STOPPED
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 2304d83aea532b764777b683c57c3bdd4d5df79a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651767"
---
# <a name="ec_dvd_playback_stopped"></a><span data-ttu-id="034a8-105">\_Воспроизведение DVD-диска EC \_ \_ остановлено</span><span class="sxs-lookup"><span data-stu-id="034a8-105">EC\_DVD\_PLAYBACK\_STOPPED</span></span>

<span data-ttu-id="034a8-106">Указывает, что воспроизведение DVD-диска было остановлено.</span><span class="sxs-lookup"><span data-stu-id="034a8-106">Indicates that DVD playback has been stopped.</span></span> <span data-ttu-id="034a8-107">Это событие отправляется, когда завершается заголовок или глава и [Навигатор DVD](dvd-navigator-filter.md) не находит никаких других инструкций ветвления для последующего воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="034a8-107">This event is sent when a title or chapter completes and the [DVD Navigator](dvd-navigator-filter.md) does not find any other branching instruction for subsequent playback.</span></span> <span data-ttu-id="034a8-108">Событие не отправляется, когда приложение останавливает воспроизведение.</span><span class="sxs-lookup"><span data-stu-id="034a8-108">The event is not sent when the application stops playback.</span></span>

## <a name="parameters"></a><span data-ttu-id="034a8-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="034a8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="034a8-110"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="034a8-110"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="034a8-111">Член перечисления [**DVD \_ Pb \_**](/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_pb_stopped) , который указывает, почему воспроизведение остановлено.</span><span class="sxs-lookup"><span data-stu-id="034a8-111">A member of the [**DVD\_PB\_STOPPED**](/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_pb_stopped) enumeration, indicating why playback stopped.</span></span>

</dd> <dt>

<span data-ttu-id="034a8-112"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="034a8-112"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="034a8-113">Ноль.</span><span class="sxs-lookup"><span data-stu-id="034a8-113">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="034a8-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="034a8-114">Remarks</span></span>

<span data-ttu-id="034a8-115">Это событие возникает во всех доменах.</span><span class="sxs-lookup"><span data-stu-id="034a8-115">This event is raised in all domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="034a8-116">Требования</span><span class="sxs-lookup"><span data-stu-id="034a8-116">Requirements</span></span>



| <span data-ttu-id="034a8-117">Требование</span><span class="sxs-lookup"><span data-stu-id="034a8-117">Requirement</span></span> | <span data-ttu-id="034a8-118">Значение</span><span class="sxs-lookup"><span data-stu-id="034a8-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="034a8-119">Header</span><span class="sxs-lookup"><span data-stu-id="034a8-119">Header</span></span><br/> | <dl> <span data-ttu-id="034a8-120"><dt>Двдевкоде. h (включение DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="034a8-120"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="034a8-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="034a8-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="034a8-122">DVD-приложения</span><span class="sxs-lookup"><span data-stu-id="034a8-122">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="034a8-123">Коды уведомлений о событиях DVD</span><span class="sxs-lookup"><span data-stu-id="034a8-123">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="034a8-124">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="034a8-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




