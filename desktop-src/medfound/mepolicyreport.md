---
description: Вызывается доверенным выходом для отправки сведений о состоянии применения политики вывода.
ms.assetid: 4906f6c3-1570-421f-aef1-914bd338bb1f
title: Событие Меполицирепорт (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a0053fb551a69b820beeb4237211cb9af446f97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673503"
---
# <a name="mepolicyreport-event"></a><span data-ttu-id="42539-103">Событие Меполицирепорт</span><span class="sxs-lookup"><span data-stu-id="42539-103">MEPolicyReport event</span></span>

<span data-ttu-id="42539-104">Вызывается доверенным выходом для отправки сведений о состоянии применения политики вывода.</span><span class="sxs-lookup"><span data-stu-id="42539-104">Raised by a trusted output to send status information about the enforcement of the output policy.</span></span>

## <a name="event-values"></a><span data-ttu-id="42539-105">Значения событий</span><span class="sxs-lookup"><span data-stu-id="42539-105">Event values</span></span>

<span data-ttu-id="42539-106">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="42539-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="42539-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="42539-107">VARTYPE</span></span>              | <span data-ttu-id="42539-108">Описание</span><span class="sxs-lookup"><span data-stu-id="42539-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="42539-109">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="42539-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="42539-110">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="42539-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="42539-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="42539-111">Remarks</span></span>

<span data-ttu-id="42539-112">Атрибуты и коды состояния для этого события зависят от конкретной системы защиты содержимого, которую обеспечивает доверенный выход.</span><span class="sxs-lookup"><span data-stu-id="42539-112">Attributes and status codes for this event depend on the specific content protection system enforced by the trusted output.</span></span>

## <a name="requirements"></a><span data-ttu-id="42539-113">Требования</span><span class="sxs-lookup"><span data-stu-id="42539-113">Requirements</span></span>



| <span data-ttu-id="42539-114">Требование</span><span class="sxs-lookup"><span data-stu-id="42539-114">Requirement</span></span> | <span data-ttu-id="42539-115">Значение</span><span class="sxs-lookup"><span data-stu-id="42539-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42539-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="42539-116">Minimum supported client</span></span><br/> | <span data-ttu-id="42539-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="42539-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="42539-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="42539-118">Minimum supported server</span></span><br/> | <span data-ttu-id="42539-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="42539-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="42539-120">Header</span><span class="sxs-lookup"><span data-stu-id="42539-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="42539-121"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="42539-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42539-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="42539-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42539-123">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="42539-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




