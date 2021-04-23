---
description: Отправляется, когда Навигатор DVD анализирует пакет PCI.
ms.assetid: 25548c23-22f0-47cb-9062-273ad39d3007
title: EC_DVD_VOBU_Timestamp (Двдевкоде. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_VOBU_Timestamp
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 762a900a83154ce38ee00fcf4173ebc32b41cf30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675069"
---
# <a name="ec_dvd_vobu_timestamp"></a><span data-ttu-id="3d27c-103">\_Отметка \_ времени вобу DVD-диска EC \_</span><span class="sxs-lookup"><span data-stu-id="3d27c-103">EC\_DVD\_VOBU\_Timestamp</span></span>

<span data-ttu-id="3d27c-104">Отправляется, когда [Навигатор DVD](dvd-navigator-filter.md) АНАЛИЗИРУЕТ пакет PCI.</span><span class="sxs-lookup"><span data-stu-id="3d27c-104">Sent when the [DVD Navigator](dvd-navigator-filter.md) parses a PCI packet.</span></span>

<span data-ttu-id="3d27c-105">Данные события — это метка времени последней единицы видеообъекта (ВОБУ).</span><span class="sxs-lookup"><span data-stu-id="3d27c-105">The event data is the time stamp of the most recent video object unit (VOBU).</span></span>

## <a name="parameters"></a><span data-ttu-id="3d27c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3d27c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d27c-107"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="3d27c-107"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="3d27c-108">Содержит **параметр DWORD** нижнего порядка метки времени.</span><span class="sxs-lookup"><span data-stu-id="3d27c-108">Contains the low-order **DWORD** of the time stamp.</span></span>

</dd> <dt>

<span data-ttu-id="3d27c-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="3d27c-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="3d27c-110">Содержит **параметр DWORD** с высоким порядковым обозначением метки времени.</span><span class="sxs-lookup"><span data-stu-id="3d27c-110">Contains the high-order **DWORD** of the time stamp.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3d27c-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3d27c-111">Remarks</span></span>

<span data-ttu-id="3d27c-112">По умолчанию это событие отключено.</span><span class="sxs-lookup"><span data-stu-id="3d27c-112">This event is disabled by default.</span></span> <span data-ttu-id="3d27c-113">Чтобы включить это событие, вызовите [**IDvdControl2:: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) и установите для параметра **\_ енаблелоггинжевентс DVD** значение **true**.</span><span class="sxs-lookup"><span data-stu-id="3d27c-113">To enable this event, call [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) and set the **DVD\_EnableLoggingEvents** option to **TRUE**.</span></span>

<span data-ttu-id="3d27c-114">Воссоздайте отметку времени следующим образом:</span><span class="sxs-lookup"><span data-stu-id="3d27c-114">Reconstruct the time stamp as follows:</span></span>


```C++
LARGE_INTEGER li;
li.LowPart = DWORD( lParam1 );
li.HighPart = DWORD( lParam2 );
```



## <a name="requirements"></a><span data-ttu-id="3d27c-115">Требования</span><span class="sxs-lookup"><span data-stu-id="3d27c-115">Requirements</span></span>



| <span data-ttu-id="3d27c-116">Требование</span><span class="sxs-lookup"><span data-stu-id="3d27c-116">Requirement</span></span> | <span data-ttu-id="3d27c-117">Значение</span><span class="sxs-lookup"><span data-stu-id="3d27c-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d27c-118">Header</span><span class="sxs-lookup"><span data-stu-id="3d27c-118">Header</span></span><br/> | <dl> <span data-ttu-id="3d27c-119"><dt>Двдевкоде. h (включение DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3d27c-119"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d27c-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3d27c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d27c-121">DVD-приложения</span><span class="sxs-lookup"><span data-stu-id="3d27c-121">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="3d27c-122">Коды уведомлений о событиях DVD</span><span class="sxs-lookup"><span data-stu-id="3d27c-122">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="3d27c-123">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="3d27c-123">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




