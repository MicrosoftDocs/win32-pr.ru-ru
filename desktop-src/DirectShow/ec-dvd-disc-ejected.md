---
description: Сигнализирует, что диск DVD был извлечен.
ms.assetid: 031156c2-f0f0-4a9e-b792-4d656ec49aef
title: EC_DVD_DISC_EJECTED (Двдевкоде. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_DISC_EJECTED
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: ab6c1333245b589d4f13bafcba89eada3ef98ab0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651855"
---
# <a name="ec_dvd_disc_ejected"></a><span data-ttu-id="7f793-103">\_DVD- \_ диск EC \_ извлечен</span><span class="sxs-lookup"><span data-stu-id="7f793-103">EC\_DVD\_DISC\_EJECTED</span></span>

<span data-ttu-id="7f793-104">Сигнализирует, что диск DVD был извлечен.</span><span class="sxs-lookup"><span data-stu-id="7f793-104">Signals that a DVD disc was ejected.</span></span>

## <a name="parameters"></a><span data-ttu-id="7f793-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="7f793-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f793-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="7f793-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="7f793-107">Ноль.</span><span class="sxs-lookup"><span data-stu-id="7f793-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="7f793-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="7f793-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="7f793-109">Ноль.</span><span class="sxs-lookup"><span data-stu-id="7f793-109">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7f793-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7f793-110">Remarks</span></span>

<span data-ttu-id="7f793-111">Воспроизведение автоматически останавливается при извлечении диска.</span><span class="sxs-lookup"><span data-stu-id="7f793-111">Playback automatically stops when a disc is ejected.</span></span> <span data-ttu-id="7f793-112">Приложению не нужно предпринимать никаких специальных действий в ответ на это событие.</span><span class="sxs-lookup"><span data-stu-id="7f793-112">The application does not have to take any special action in response to this event.</span></span>

<span data-ttu-id="7f793-113">Это событие возникает во всех доменах.</span><span class="sxs-lookup"><span data-stu-id="7f793-113">This event is raised in all domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f793-114">Требования</span><span class="sxs-lookup"><span data-stu-id="7f793-114">Requirements</span></span>



| <span data-ttu-id="7f793-115">Требование</span><span class="sxs-lookup"><span data-stu-id="7f793-115">Requirement</span></span> | <span data-ttu-id="7f793-116">Значение</span><span class="sxs-lookup"><span data-stu-id="7f793-116">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f793-117">Header</span><span class="sxs-lookup"><span data-stu-id="7f793-117">Header</span></span><br/> | <dl> <span data-ttu-id="7f793-118"><dt>Двдевкоде. h (включение DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7f793-118"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f793-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7f793-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f793-120">DVD-приложения</span><span class="sxs-lookup"><span data-stu-id="7f793-120">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="7f793-121">Коды уведомлений о событиях DVD</span><span class="sxs-lookup"><span data-stu-id="7f793-121">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="7f793-122">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="7f793-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




