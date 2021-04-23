---
description: Отправляется при изменении текущего набора заголовков видео (ВТС).
ms.assetid: 7b8849c8-c71e-44d6-b33a-8e80247bdb22
title: EC_DVD_TITLE_SET_CHANGE (Двдевкоде. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_TITLE_SET_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: c5685cfb909a7fa24c39dff969076269845a663e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675248"
---
# <a name="ec_dvd_title_set_change"></a><span data-ttu-id="08046-103">\_ \_ изменение набора заголовков DVD EC \_ \_</span><span class="sxs-lookup"><span data-stu-id="08046-103">EC\_DVD\_TITLE\_SET\_CHANGE</span></span>

<span data-ttu-id="08046-104">Отправляется при изменении текущего набора заголовков видео (ВТС).</span><span class="sxs-lookup"><span data-stu-id="08046-104">Sent when current Video Title Set (VTS) changes.</span></span>

## <a name="parameters"></a><span data-ttu-id="08046-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="08046-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08046-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="08046-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="08046-107">Номер нового набора заголовков видео (ВТСН).</span><span class="sxs-lookup"><span data-stu-id="08046-107">The new Video Title Set Number (VTSN).</span></span>

</dd> <dt>

<span data-ttu-id="08046-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="08046-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="08046-109">Ноль.</span><span class="sxs-lookup"><span data-stu-id="08046-109">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="08046-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="08046-110">Remarks</span></span>

<span data-ttu-id="08046-111">По умолчанию это событие отключено.</span><span class="sxs-lookup"><span data-stu-id="08046-111">This event is disabled by default.</span></span> <span data-ttu-id="08046-112">Чтобы включить это событие, вызовите [**IDvdControl2:: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) и установите для параметра **\_ нотифипоситиончанже DVD** значение **true**.</span><span class="sxs-lookup"><span data-stu-id="08046-112">To enable this event, call [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) and set the **DVD\_NotifyPositionChange** option to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="08046-113">Требования</span><span class="sxs-lookup"><span data-stu-id="08046-113">Requirements</span></span>



| <span data-ttu-id="08046-114">Требование</span><span class="sxs-lookup"><span data-stu-id="08046-114">Requirement</span></span> | <span data-ttu-id="08046-115">Значение</span><span class="sxs-lookup"><span data-stu-id="08046-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08046-116">Header</span><span class="sxs-lookup"><span data-stu-id="08046-116">Header</span></span><br/> | <dl> <span data-ttu-id="08046-117"><dt>Двдевкоде. h (включение DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="08046-117"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08046-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="08046-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08046-119">DVD-приложения</span><span class="sxs-lookup"><span data-stu-id="08046-119">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="08046-120">Коды уведомлений о событиях DVD</span><span class="sxs-lookup"><span data-stu-id="08046-120">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="08046-121">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="08046-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




