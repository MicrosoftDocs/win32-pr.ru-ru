---
description: Сигнализирует, что проигрыватель DVD запустил воспроизведение новой программы в \_ домене заголовка DVD-домена \_ .
ms.assetid: c0745615-d527-4d93-9118-30419c6c811e
title: EC_DVD_CHAPTER_START (Двдевкоде. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_CHAPTER_START
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 87a4408f1631d8a23cf42e790688856d6c246393
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651653"
---
# <a name="ec_dvd_chapter_start"></a><span data-ttu-id="f5545-103">\_начало главы с DVD-дисками EC \_ \_</span><span class="sxs-lookup"><span data-stu-id="f5545-103">EC\_DVD\_CHAPTER\_START</span></span>

<span data-ttu-id="f5545-104">Сигнализирует, что проигрыватель DVD запустил воспроизведение новой программы в \_ домене заголовка DVD-домена \_ .</span><span class="sxs-lookup"><span data-stu-id="f5545-104">Signals that the DVD player started playback of a new program in the DVD\_DOMAIN\_Title domain.</span></span>

## <a name="parameters"></a><span data-ttu-id="f5545-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="f5545-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5545-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="f5545-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="f5545-107">Значение **типа DWORD** , указывающее новый номер главы (Program).</span><span class="sxs-lookup"><span data-stu-id="f5545-107">**DWORD** value indicating the new chapter (program) number.</span></span>

</dd> <dt>

<span data-ttu-id="f5545-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="f5545-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="f5545-109">Ноль.</span><span class="sxs-lookup"><span data-stu-id="f5545-109">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f5545-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f5545-110">Remarks</span></span>

<span data-ttu-id="f5545-111">Это событие сигнализирует только простым линейным роликам.</span><span class="sxs-lookup"><span data-stu-id="f5545-111">Only simple linear movies signal this event.</span></span>

<span data-ttu-id="f5545-112">Это событие возникает в домене Title.</span><span class="sxs-lookup"><span data-stu-id="f5545-112">This event is raised in the title domain.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5545-113">Требования</span><span class="sxs-lookup"><span data-stu-id="f5545-113">Requirements</span></span>



| <span data-ttu-id="f5545-114">Требование</span><span class="sxs-lookup"><span data-stu-id="f5545-114">Requirement</span></span> | <span data-ttu-id="f5545-115">Значение</span><span class="sxs-lookup"><span data-stu-id="f5545-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5545-116">Header</span><span class="sxs-lookup"><span data-stu-id="f5545-116">Header</span></span><br/> | <dl> <span data-ttu-id="f5545-117"><dt>Двдевкоде. h (включение DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f5545-117"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5545-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f5545-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5545-119">DVD-приложения</span><span class="sxs-lookup"><span data-stu-id="f5545-119">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="f5545-120">Коды уведомлений о событиях DVD</span><span class="sxs-lookup"><span data-stu-id="f5545-120">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="f5545-121">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="f5545-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="f5545-122">**\_Перечисление доменов DVD**</span><span class="sxs-lookup"><span data-stu-id="f5545-122">**DVD\_DOMAIN Enumeration**</span></span>](/windows/win32/api/strmif/ne-strmif-dvd_domain)
</dt> </dl>

 

 




