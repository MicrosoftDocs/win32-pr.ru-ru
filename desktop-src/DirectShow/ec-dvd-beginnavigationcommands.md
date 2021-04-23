---
description: Отправляется при запуске набора команд перехода DVD.
ms.assetid: 9cdcb211-a9e3-4a15-81bd-7ada2b9d823a
title: EC_DVD_BeginNavigationCommands (Двдевкоде. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_BeginNavigationCommands
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: cda904c4fcc0b1acdd16c8fc4596eef332140ec4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679670"
---
# <a name="ec_dvd_beginnavigationcommands"></a><span data-ttu-id="ea420-103">\_Бегиннавигатионкоммандс DVD-диск EC \_</span><span class="sxs-lookup"><span data-stu-id="ea420-103">EC\_DVD\_BeginNavigationCommands</span></span>

<span data-ttu-id="ea420-104">Отправляется при запуске набора команд перехода DVD.</span><span class="sxs-lookup"><span data-stu-id="ea420-104">Sent when a set of DVD navigation commands are starting.</span></span>

## <a name="parameters"></a><span data-ttu-id="ea420-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="ea420-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea420-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="ea420-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="ea420-107">Значение из перечисления [**DVD \_ навкмдтипе**](/windows/win32/api/strmif/ne-strmif-dvd_navcmdtype) .</span><span class="sxs-lookup"><span data-stu-id="ea420-107">A value from the [**DVD\_NavCmdType**](/windows/win32/api/strmif/ne-strmif-dvd_navcmdtype) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="ea420-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="ea420-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="ea420-109">Ноль.</span><span class="sxs-lookup"><span data-stu-id="ea420-109">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ea420-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ea420-110">Remarks</span></span>

<span data-ttu-id="ea420-111">По умолчанию это событие отключено.</span><span class="sxs-lookup"><span data-stu-id="ea420-111">This event is disabled by default.</span></span> <span data-ttu-id="ea420-112">Чтобы включить это событие, вызовите [**IDvdControl2:: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) и установите для параметра **\_ енаблелоггинжевентс DVD** значение **true**.</span><span class="sxs-lookup"><span data-stu-id="ea420-112">To enable this event, call [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) and set the **DVD\_EnableLoggingEvents** option to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea420-113">Требования</span><span class="sxs-lookup"><span data-stu-id="ea420-113">Requirements</span></span>



| <span data-ttu-id="ea420-114">Требование</span><span class="sxs-lookup"><span data-stu-id="ea420-114">Requirement</span></span> | <span data-ttu-id="ea420-115">Значение</span><span class="sxs-lookup"><span data-stu-id="ea420-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea420-116">Header</span><span class="sxs-lookup"><span data-stu-id="ea420-116">Header</span></span><br/> | <dl> <span data-ttu-id="ea420-117"><dt>Двдевкоде. h (включение DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ea420-117"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea420-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ea420-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea420-119">DVD-приложения</span><span class="sxs-lookup"><span data-stu-id="ea420-119">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="ea420-120">Коды уведомлений о событиях DVD</span><span class="sxs-lookup"><span data-stu-id="ea420-120">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="ea420-121">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="ea420-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




