---
description: Вызывается модулем политики, когда начинается получение лицензии. Получение лицензии выполняется с помощью реализации интерфейса Имфконтентпротектионманажер в приложениях.
ms.assetid: c328743c-a69b-431e-8a05-0e140aad9b4d
title: Событие Мелиценсеаккуиситионстарт (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 914d2580c95cf40986a844a994c1e284c5ad9e22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683132"
---
# <a name="melicenseacquisitionstart-event"></a><span data-ttu-id="21ac8-104">Событие Мелиценсеаккуиситионстарт</span><span class="sxs-lookup"><span data-stu-id="21ac8-104">MELicenseAcquisitionStart event</span></span>

<span data-ttu-id="21ac8-105">Вызывается модулем политики, когда начинается получение лицензии.</span><span class="sxs-lookup"><span data-stu-id="21ac8-105">Raised by the policy engine when license acquisition is about to begin.</span></span> <span data-ttu-id="21ac8-106">Получение лицензии выполняется с помощью реализации интерфейса [**имфконтентпротектионманажер**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) в приложении.</span><span class="sxs-lookup"><span data-stu-id="21ac8-106">License acquisition is performed using the application's implementation of the [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) interface.</span></span>

## <a name="event-values"></a><span data-ttu-id="21ac8-107">Значения событий</span><span class="sxs-lookup"><span data-stu-id="21ac8-107">Event values</span></span>

<span data-ttu-id="21ac8-108">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="21ac8-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="21ac8-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="21ac8-109">VARTYPE</span></span>              | <span data-ttu-id="21ac8-110">Описание</span><span class="sxs-lookup"><span data-stu-id="21ac8-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="21ac8-111">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="21ac8-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="21ac8-112">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="21ac8-112">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="21ac8-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="21ac8-113">Remarks</span></span>

<span data-ttu-id="21ac8-114">По завершении приобретения лицензии обработчик политики вызывает событие [мелиценсеаккуиситионкомплетед](melicenseacquisitioncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="21ac8-114">When license acquisition is completed, the policy engine raises the [MELicenseAcquisitionCompleted](melicenseacquisitioncompleted.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="21ac8-115">Требования</span><span class="sxs-lookup"><span data-stu-id="21ac8-115">Requirements</span></span>



| <span data-ttu-id="21ac8-116">Требование</span><span class="sxs-lookup"><span data-stu-id="21ac8-116">Requirement</span></span> | <span data-ttu-id="21ac8-117">Значение</span><span class="sxs-lookup"><span data-stu-id="21ac8-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21ac8-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="21ac8-118">Minimum supported client</span></span><br/> | <span data-ttu-id="21ac8-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="21ac8-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="21ac8-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="21ac8-120">Minimum supported server</span></span><br/> | <span data-ttu-id="21ac8-121">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="21ac8-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="21ac8-122">Header</span><span class="sxs-lookup"><span data-stu-id="21ac8-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="21ac8-123"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="21ac8-123"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21ac8-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="21ac8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21ac8-125">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="21ac8-125">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




