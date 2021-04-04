---
description: Вызывается приемником потока после вызова метода Имфстреамсинк::P Лацемаркер.
ms.assetid: 40f68352-86e5-4864-9ca0-f30998857fef
title: Событие Местреамсинкмаркер (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 071d6e5b25873739c176d1c808929c26e1e338bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811872"
---
# <a name="mestreamsinkmarker-event"></a><span data-ttu-id="35dcf-103">Событие Местреамсинкмаркер</span><span class="sxs-lookup"><span data-stu-id="35dcf-103">MEStreamSinkMarker event</span></span>

<span data-ttu-id="35dcf-104">Вызывается приемником потока после вызова метода [**имфстреамсинк::P лацемаркер**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) .</span><span class="sxs-lookup"><span data-stu-id="35dcf-104">Raised by a stream sink after the [**IMFStreamSink::PlaceMarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) method is called.</span></span>

## <a name="event-values"></a><span data-ttu-id="35dcf-105">Значения событий</span><span class="sxs-lookup"><span data-stu-id="35dcf-105">Event values</span></span>

<span data-ttu-id="35dcf-106">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="35dcf-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="35dcf-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="35dcf-107">VARTYPE</span></span>            | <span data-ttu-id="35dcf-108">Описание</span><span class="sxs-lookup"><span data-stu-id="35dcf-108">Description</span></span>                                                                                                                                                                                           |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35dcf-109">>любой</span><span class="sxs-lookup"><span data-stu-id="35dcf-109">>Any</span></span><br/> | <span data-ttu-id="35dcf-110">Значение события — это копия **пропвариант** , которую вызывающий объект указал в параметре *пварконтекствалуе* метода [**плацемаркер**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) .</span><span class="sxs-lookup"><span data-stu-id="35dcf-110">The event value is a copy of the **PROPVARIANT** that the caller specified in the *pvarContextValue* parameter of the [**PlaceMarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) method.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="35dcf-111">Требования</span><span class="sxs-lookup"><span data-stu-id="35dcf-111">Requirements</span></span>



| <span data-ttu-id="35dcf-112">Требование</span><span class="sxs-lookup"><span data-stu-id="35dcf-112">Requirement</span></span> | <span data-ttu-id="35dcf-113">Значение</span><span class="sxs-lookup"><span data-stu-id="35dcf-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35dcf-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="35dcf-114">Minimum supported client</span></span><br/> | <span data-ttu-id="35dcf-115">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="35dcf-115">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="35dcf-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="35dcf-116">Minimum supported server</span></span><br/> | <span data-ttu-id="35dcf-117">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="35dcf-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="35dcf-118">Header</span><span class="sxs-lookup"><span data-stu-id="35dcf-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="35dcf-119"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="35dcf-119"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35dcf-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="35dcf-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35dcf-121">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="35dcf-121">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="35dcf-122">Приемники носителей</span><span class="sxs-lookup"><span data-stu-id="35dcf-122">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 




