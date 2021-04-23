---
description: Вызывается модулем политики при завершении индивидуализации. Дополнительные сведения см. в разделе Меиндивидуализатионстарт Event.
ms.assetid: 44a4956f-19ba-410d-b96c-e7774cbe2d7e
title: Событие Меиндивидуализатионкомплетед (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7143274d12a9ad113f714062ff8f88c1fb8277cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701901"
---
# <a name="meindividualizationcompleted-event"></a><span data-ttu-id="5fa1e-104">Событие Меиндивидуализатионкомплетед</span><span class="sxs-lookup"><span data-stu-id="5fa1e-104">MEIndividualizationCompleted event</span></span>

<span data-ttu-id="5fa1e-105">Вызывается модулем политики при завершении индивидуализации.</span><span class="sxs-lookup"><span data-stu-id="5fa1e-105">Raised by the policy engine when individualization is complete.</span></span> <span data-ttu-id="5fa1e-106">Дополнительные сведения см. в разделе [меиндивидуализатионстарт](meindividualizationstart.md) Event.</span><span class="sxs-lookup"><span data-stu-id="5fa1e-106">For more information, see [MEIndividualizationStart](meindividualizationstart.md) event.</span></span>

## <a name="event-values"></a><span data-ttu-id="5fa1e-107">Значения событий</span><span class="sxs-lookup"><span data-stu-id="5fa1e-107">Event values</span></span>

<span data-ttu-id="5fa1e-108">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="5fa1e-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="5fa1e-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="5fa1e-109">VARTYPE</span></span>              | <span data-ttu-id="5fa1e-110">Описание</span><span class="sxs-lookup"><span data-stu-id="5fa1e-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="5fa1e-111">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="5fa1e-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="5fa1e-112">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="5fa1e-112">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="5fa1e-113">Требования</span><span class="sxs-lookup"><span data-stu-id="5fa1e-113">Requirements</span></span>



| <span data-ttu-id="5fa1e-114">Требование</span><span class="sxs-lookup"><span data-stu-id="5fa1e-114">Requirement</span></span> | <span data-ttu-id="5fa1e-115">Значение</span><span class="sxs-lookup"><span data-stu-id="5fa1e-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fa1e-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5fa1e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5fa1e-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5fa1e-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5fa1e-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5fa1e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5fa1e-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5fa1e-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5fa1e-120">Header</span><span class="sxs-lookup"><span data-stu-id="5fa1e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="5fa1e-121"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5fa1e-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5fa1e-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5fa1e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fa1e-123">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5fa1e-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




