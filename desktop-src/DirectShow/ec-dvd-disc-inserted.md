---
description: Сигнализирует о вставке DVD-диска в дисковод.
ms.assetid: ce233c94-2eae-457c-919b-7c4d8334979a
title: EC_DVD_DISC_INSERTED (Двдевкоде. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_DISC_INSERTED
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: c98d32960e2ab6a21633899164b3ff84525f2aaf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675383"
---
# <a name="ec_dvd_disc_inserted"></a><span data-ttu-id="31968-103">\_вставлен DVD- \_ диск \_ EC</span><span class="sxs-lookup"><span data-stu-id="31968-103">EC\_DVD\_DISC\_INSERTED</span></span>

<span data-ttu-id="31968-104">Сигнализирует о вставке DVD-диска в дисковод.</span><span class="sxs-lookup"><span data-stu-id="31968-104">Signals that a DVD disc was inserted into the drive.</span></span>

## <a name="parameters"></a><span data-ttu-id="31968-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="31968-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31968-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="31968-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="31968-107">Ноль.</span><span class="sxs-lookup"><span data-stu-id="31968-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="31968-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="31968-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="31968-109">Ноль.</span><span class="sxs-lookup"><span data-stu-id="31968-109">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="31968-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="31968-110">Remarks</span></span>

<span data-ttu-id="31968-111">Воспроизведение начинается автоматически при вставке диска.</span><span class="sxs-lookup"><span data-stu-id="31968-111">Playback automatically begins when a disc is inserted.</span></span> <span data-ttu-id="31968-112">Приложению не нужно предпринимать никаких специальных действий в ответ на это событие.</span><span class="sxs-lookup"><span data-stu-id="31968-112">The application does not have to take any special action in response to this event.</span></span>

<span data-ttu-id="31968-113">Это событие возникает во всех доменах.</span><span class="sxs-lookup"><span data-stu-id="31968-113">This event is raised in all domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="31968-114">Требования</span><span class="sxs-lookup"><span data-stu-id="31968-114">Requirements</span></span>



| <span data-ttu-id="31968-115">Требование</span><span class="sxs-lookup"><span data-stu-id="31968-115">Requirement</span></span> | <span data-ttu-id="31968-116">Значение</span><span class="sxs-lookup"><span data-stu-id="31968-116">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31968-117">Header</span><span class="sxs-lookup"><span data-stu-id="31968-117">Header</span></span><br/> | <dl> <span data-ttu-id="31968-118"><dt>Двдевкоде. h (включение DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="31968-118"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31968-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="31968-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31968-120">DVD-приложения</span><span class="sxs-lookup"><span data-stu-id="31968-120">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="31968-121">Коды уведомлений о событиях DVD</span><span class="sxs-lookup"><span data-stu-id="31968-121">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="31968-122">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="31968-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




