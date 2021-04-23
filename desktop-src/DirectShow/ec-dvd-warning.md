---
description: Сообщает о состоянии предупреждения DVD.
ms.assetid: d7221e8a-089f-4eaf-a193-548709c14336
title: EC_DVD_WARNING (Двдевкоде. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_WARNING
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 7f25d4565c2afeb4619f7832f6d5742e07dcca0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675067"
---
# <a name="ec_dvd_warning"></a><span data-ttu-id="c966e-103">\_предупреждение EC DVD \_</span><span class="sxs-lookup"><span data-stu-id="c966e-103">EC\_DVD\_WARNING</span></span>

<span data-ttu-id="c966e-104">Сообщает о состоянии предупреждения DVD.</span><span class="sxs-lookup"><span data-stu-id="c966e-104">Signals a DVD warning condition.</span></span>

## <a name="parameters"></a><span data-ttu-id="c966e-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="c966e-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c966e-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="c966e-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="c966e-107">Значение **типа DWORD** , указывающее на состояние предупреждения.</span><span class="sxs-lookup"><span data-stu-id="c966e-107">**DWORD** value indicating the warning condition.</span></span> <span data-ttu-id="c966e-108">Член типа данных [**\_ предупреждения о предупреждении DVD**](/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_warning) .</span><span class="sxs-lookup"><span data-stu-id="c966e-108">Member of the [**DVD\_WARNING**](/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_warning) enumerated data type.</span></span>

</dd> <dt>

<span data-ttu-id="c966e-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="c966e-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="c966e-110">Если *pParam1* соответствует DVD- \_ предупреждению \_ Open, Warning DVD \_ \_ Seek или DVD Warning \_ \_ Read, то *LParam2* содержит последний код ошибки, возвращенный из **GetLastError**.</span><span class="sxs-lookup"><span data-stu-id="c966e-110">If *pParam1* equals DVD\_WARNING\_Open, DVD\_WARNING\_Seek, or DVD\_WARNING\_Read, then *lParam2* contains the last error code returned from **GetLastError**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c966e-111">Требования</span><span class="sxs-lookup"><span data-stu-id="c966e-111">Requirements</span></span>



| <span data-ttu-id="c966e-112">Требование</span><span class="sxs-lookup"><span data-stu-id="c966e-112">Requirement</span></span> | <span data-ttu-id="c966e-113">Значение</span><span class="sxs-lookup"><span data-stu-id="c966e-113">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c966e-114">Header</span><span class="sxs-lookup"><span data-stu-id="c966e-114">Header</span></span><br/> | <dl> <span data-ttu-id="c966e-115"><dt>Двдевкоде. h (включение DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c966e-115"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c966e-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c966e-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c966e-117">DVD-приложения</span><span class="sxs-lookup"><span data-stu-id="c966e-117">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="c966e-118">Коды уведомлений о событиях DVD</span><span class="sxs-lookup"><span data-stu-id="c966e-118">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="c966e-119">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="c966e-119">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




