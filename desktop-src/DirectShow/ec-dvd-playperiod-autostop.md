---
description: Указывает, что навигатор завершил воспроизведение сегмента, указанного в вызове IDvdControl2::P Лайпериодинтитлеаутостоп.
ms.assetid: 1716eabe-f106-436a-8a6a-ca43cee9341c
title: EC_DVD_PLAYPERIOD_AUTOSTOP (Двдевкоде. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_PLAYPERIOD_AUTOSTOP
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: c2081c8a5b7e5b6bd2165781af9552722ed9ddee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675254"
---
# <a name="ec_dvd_playperiod_autostop"></a><span data-ttu-id="87332-103">\_автозавершение плайпериод для диска EC DVD \_ \_</span><span class="sxs-lookup"><span data-stu-id="87332-103">EC\_DVD\_PLAYPERIOD\_AUTOSTOP</span></span>

<span data-ttu-id="87332-104">Указывает, что навигатор завершил воспроизведение сегмента, указанного в вызове [**IDvdControl2::P лайпериодинтитлеаутостоп**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playperiodintitleautostop).</span><span class="sxs-lookup"><span data-stu-id="87332-104">Indicates that the Navigator has finished playing the segment specified in a call to [**IDvdControl2::PlayPeriodInTitleAutoStop**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playperiodintitleautostop).</span></span>

## <a name="parameters"></a><span data-ttu-id="87332-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="87332-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87332-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="87332-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="87332-107">Ноль.</span><span class="sxs-lookup"><span data-stu-id="87332-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="87332-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="87332-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="87332-109">Ноль.</span><span class="sxs-lookup"><span data-stu-id="87332-109">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="87332-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="87332-110">Remarks</span></span>

<span data-ttu-id="87332-111">Это событие возникает в домене Title.</span><span class="sxs-lookup"><span data-stu-id="87332-111">This event is raised in the Title domain.</span></span>

<span data-ttu-id="87332-112">Это событие также отправляется, когда воспроизведение отменяется до того, как навигатор завершает воспроизведение указанного сегмента.</span><span class="sxs-lookup"><span data-stu-id="87332-112">This event is also sent when playback is canceled before the Navigator finishes playing the specified segment.</span></span>

## <a name="requirements"></a><span data-ttu-id="87332-113">Требования</span><span class="sxs-lookup"><span data-stu-id="87332-113">Requirements</span></span>



| <span data-ttu-id="87332-114">Требование</span><span class="sxs-lookup"><span data-stu-id="87332-114">Requirement</span></span> | <span data-ttu-id="87332-115">Значение</span><span class="sxs-lookup"><span data-stu-id="87332-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87332-116">Header</span><span class="sxs-lookup"><span data-stu-id="87332-116">Header</span></span><br/> | <dl> <span data-ttu-id="87332-117"><dt>Двдевкоде. h (включение DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="87332-117"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87332-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="87332-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87332-119">DVD-приложения</span><span class="sxs-lookup"><span data-stu-id="87332-119">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="87332-120">Коды уведомлений о событиях DVD</span><span class="sxs-lookup"><span data-stu-id="87332-120">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="87332-121">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="87332-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="87332-122">**IDvdControl2::P Лайпериодинтитлеаутостоп**</span><span class="sxs-lookup"><span data-stu-id="87332-122">**IDvdControl2::PlayPeriodInTitleAutoStop**</span></span>](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playperiodintitleautostop)
</dt> </dl>

 

 




