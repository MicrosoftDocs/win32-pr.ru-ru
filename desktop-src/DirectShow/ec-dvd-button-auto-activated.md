---
description: Сигнализирует о том, что кнопка меню DVD была автоматически активирована для каждой инструкции на диске. Это происходит, когда время ожидания меню истекло, а на диске указана автоматическая активация кнопки.
ms.assetid: ecd79c2a-1717-473d-b111-2b1db2ca4cc1
title: EC_DVD_BUTTON_AUTO_ACTIVATED (Двдевкоде. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_BUTTON_AUTO_ACTIVATED
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 6a30ddcff32140165d5cb6cb648df84b3360a1b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679669"
---
# <a name="ec_dvd_button_auto_activated"></a><span data-ttu-id="6d5d2-103">\_ \_ \_ Автоматическая \_ Активация кнопки DVD в EC</span><span class="sxs-lookup"><span data-stu-id="6d5d2-103">EC\_DVD\_BUTTON\_AUTO\_ACTIVATED</span></span>

<span data-ttu-id="6d5d2-104">Сигнализирует о том, что кнопка меню DVD была автоматически активирована для каждой инструкции на диске. Это происходит, когда время ожидания меню истекло, а на диске указана автоматическая активация кнопки.</span><span class="sxs-lookup"><span data-stu-id="6d5d2-104">Signals that a DVD menu button has been automatically activated per instructions on the disc. This occurs when a menu times out and the disc has specified a button to be automatically activated.</span></span>

## <a name="parameters"></a><span data-ttu-id="6d5d2-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="6d5d2-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d5d2-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="6d5d2-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="6d5d2-107">Значение **типа DWORD** , указывающее на активированную кнопку.</span><span class="sxs-lookup"><span data-stu-id="6d5d2-107">**DWORD** value indicating the button that was activated.</span></span>

</dd> <dt>

<span data-ttu-id="6d5d2-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="6d5d2-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="6d5d2-109">Ноль.</span><span class="sxs-lookup"><span data-stu-id="6d5d2-109">Zero.</span></span>

</dd> </dl>

<span data-ttu-id="6d5d2-110">Это событие возникает во всех доменах.</span><span class="sxs-lookup"><span data-stu-id="6d5d2-110">This event is raised in all domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d5d2-111">Требования</span><span class="sxs-lookup"><span data-stu-id="6d5d2-111">Requirements</span></span>



| <span data-ttu-id="6d5d2-112">Требование</span><span class="sxs-lookup"><span data-stu-id="6d5d2-112">Requirement</span></span> | <span data-ttu-id="6d5d2-113">Значение</span><span class="sxs-lookup"><span data-stu-id="6d5d2-113">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d5d2-114">Header</span><span class="sxs-lookup"><span data-stu-id="6d5d2-114">Header</span></span><br/> | <dl> <span data-ttu-id="6d5d2-115"><dt>Двдевкоде. h (включение DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6d5d2-115"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d5d2-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6d5d2-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d5d2-117">DVD-приложения</span><span class="sxs-lookup"><span data-stu-id="6d5d2-117">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="6d5d2-118">Коды уведомлений о событиях DVD</span><span class="sxs-lookup"><span data-stu-id="6d5d2-118">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="6d5d2-119">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="6d5d2-119">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




