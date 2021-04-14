---
description: Указывает, что текущий номер заголовка DVD изменяется.
ms.assetid: 9888f2ec-fc2d-4d6d-a03d-b381373337eb
title: EC_DVD_TITLE_CHANGE (Двдевкоде. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_TITLE_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 9539d29704797b1c7b001d426250762d2ed27b3e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651675"
---
# <a name="ec_dvd_title_change"></a><span data-ttu-id="81aec-103">\_изменение названия DVD-диска EC \_ \_</span><span class="sxs-lookup"><span data-stu-id="81aec-103">EC\_DVD\_TITLE\_CHANGE</span></span>

<span data-ttu-id="81aec-104">Указывает, что текущий номер заголовка DVD изменяется.</span><span class="sxs-lookup"><span data-stu-id="81aec-104">Indicates when the current DVD title number changes.</span></span>

## <a name="parameters"></a><span data-ttu-id="81aec-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="81aec-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81aec-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="81aec-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="81aec-107">Значение **типа DWORD** , указывающее новый номер заголовка.</span><span class="sxs-lookup"><span data-stu-id="81aec-107">**DWORD** value indicating the new title number.</span></span>

</dd> <dt>

<span data-ttu-id="81aec-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="81aec-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="81aec-109">Ноль.</span><span class="sxs-lookup"><span data-stu-id="81aec-109">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="81aec-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="81aec-110">Remarks</span></span>

<span data-ttu-id="81aec-111">Номера заголовков находятся в диапазоне от 1 до 99.</span><span class="sxs-lookup"><span data-stu-id="81aec-111">Title numbers range from 1 to 99.</span></span> <span data-ttu-id="81aec-112">Это число указывает на ТТН, то есть номер заголовка относительно целого диска, а не ВТС \_ ТТН, который является номером заголовка по отношению только к текущему ВТС.</span><span class="sxs-lookup"><span data-stu-id="81aec-112">This number indicates the TTN, which is the title number with respect to the whole disc, not the VTS\_TTN which is the title number with respect to just a current VTS.</span></span>

<span data-ttu-id="81aec-113">Это событие возникает в домене Title.</span><span class="sxs-lookup"><span data-stu-id="81aec-113">This event is raised in the title domain.</span></span>

## <a name="requirements"></a><span data-ttu-id="81aec-114">Требования</span><span class="sxs-lookup"><span data-stu-id="81aec-114">Requirements</span></span>



| <span data-ttu-id="81aec-115">Требование</span><span class="sxs-lookup"><span data-stu-id="81aec-115">Requirement</span></span> | <span data-ttu-id="81aec-116">Значение</span><span class="sxs-lookup"><span data-stu-id="81aec-116">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81aec-117">Header</span><span class="sxs-lookup"><span data-stu-id="81aec-117">Header</span></span><br/> | <dl> <span data-ttu-id="81aec-118"><dt>Двдевкоде. h (включение DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="81aec-118"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81aec-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="81aec-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81aec-120">DVD-приложения</span><span class="sxs-lookup"><span data-stu-id="81aec-120">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="81aec-121">Коды уведомлений о событиях DVD</span><span class="sxs-lookup"><span data-stu-id="81aec-121">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="81aec-122">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="81aec-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




