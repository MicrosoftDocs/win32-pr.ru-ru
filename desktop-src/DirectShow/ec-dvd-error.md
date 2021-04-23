---
description: Сообщает о состоянии ошибки DVD.
ms.assetid: 2cd3e0c4-e2b7-4aa1-9f3c-9003eabfb08a
title: EC_DVD_ERROR (Двдевкоде. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_ERROR
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 3b338889836bf78a334784ea66c0e346e9f6b672
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675264"
---
# <a name="ec_dvd_error"></a><span data-ttu-id="d931e-103">\_Ошибка на DVD-диске EC \_</span><span class="sxs-lookup"><span data-stu-id="d931e-103">EC\_DVD\_ERROR</span></span>

<span data-ttu-id="d931e-104">Сообщает о состоянии ошибки DVD.</span><span class="sxs-lookup"><span data-stu-id="d931e-104">Signals a DVD error condition.</span></span>

## <a name="parameters"></a><span data-ttu-id="d931e-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="d931e-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d931e-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="d931e-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="d931e-107">Значение **типа DWORD** , указывающее на состояние ошибки.</span><span class="sxs-lookup"><span data-stu-id="d931e-107">**DWORD** value indicating the error condition.</span></span> <span data-ttu-id="d931e-108">Член перечисленного типа данных " [**\_ Ошибка DVD**](/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_error) ".</span><span class="sxs-lookup"><span data-stu-id="d931e-108">Member of the [**DVD\_ERROR**](/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_error) enumerated data type.</span></span>

</dd> <dt>

<span data-ttu-id="d931e-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="d931e-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="d931e-110">Значение зависит от значения *lParam1*.</span><span class="sxs-lookup"><span data-stu-id="d931e-110">Meaning depends on the value of *lParam1*.</span></span> <span data-ttu-id="d931e-111">Дополнительные сведения см. в разделе [**\_ об ошибках DVD**](/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_error) .</span><span class="sxs-lookup"><span data-stu-id="d931e-111">See [**DVD\_ERROR**](/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_error) for more information.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d931e-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d931e-112">Remarks</span></span>

<span data-ttu-id="d931e-113">Это событие возникает во всех доменах.</span><span class="sxs-lookup"><span data-stu-id="d931e-113">This event is raised in all domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="d931e-114">Требования</span><span class="sxs-lookup"><span data-stu-id="d931e-114">Requirements</span></span>



| <span data-ttu-id="d931e-115">Требование</span><span class="sxs-lookup"><span data-stu-id="d931e-115">Requirement</span></span> | <span data-ttu-id="d931e-116">Значение</span><span class="sxs-lookup"><span data-stu-id="d931e-116">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d931e-117">Header</span><span class="sxs-lookup"><span data-stu-id="d931e-117">Header</span></span><br/> | <dl> <span data-ttu-id="d931e-118"><dt>Двдевкоде. h (включение DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d931e-118"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d931e-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d931e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d931e-120">DVD-приложения</span><span class="sxs-lookup"><span data-stu-id="d931e-120">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="d931e-121">Коды уведомлений о событиях DVD</span><span class="sxs-lookup"><span data-stu-id="d931e-121">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="d931e-122">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="d931e-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




