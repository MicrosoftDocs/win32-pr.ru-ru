---
description: 'Вызывается источником мультимедиа для запроса нового скорости воспроизведения. Приложение должно вызывать Имфратеконтрол:: Сетрате с запрошенной частотой. Источник мультимедиа может вызвать это событие, если оно не может продолжать воспроизведение по текущей скорости.'
ms.assetid: 705e5a79-836b-417b-a7ed-c733572f6905
title: Событие Месаурцератечанжерекуестед (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9973a509541f3ec3d4f6a235b8f1277a20f7ed1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263640"
---
# <a name="mesourceratechangerequested-event"></a><span data-ttu-id="a7cf4-105">Событие Месаурцератечанжерекуестед</span><span class="sxs-lookup"><span data-stu-id="a7cf4-105">MESourceRateChangeRequested event</span></span>

<span data-ttu-id="a7cf4-106">Вызывается источником мультимедиа для запроса нового скорости воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="a7cf4-106">Raised by a media source to request a new playback rate.</span></span> <span data-ttu-id="a7cf4-107">Приложение должно вызывать [**имфратеконтрол:: сетрате**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) с запрошенной частотой.</span><span class="sxs-lookup"><span data-stu-id="a7cf4-107">The application should call [**IMFRateControl::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) with the requested rate.</span></span> <span data-ttu-id="a7cf4-108">Источник мультимедиа может вызвать это событие, если оно не может продолжать воспроизведение по текущей скорости.</span><span class="sxs-lookup"><span data-stu-id="a7cf4-108">A media source might raise this event if it cannot continue playback at the current rate.</span></span>

## <a name="event-values"></a><span data-ttu-id="a7cf4-109">Значения событий</span><span class="sxs-lookup"><span data-stu-id="a7cf4-109">Event values</span></span>

<span data-ttu-id="a7cf4-110">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="a7cf4-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="a7cf4-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="a7cf4-111">VARTYPE</span></span>           | <span data-ttu-id="a7cf4-112">Описание</span><span class="sxs-lookup"><span data-stu-id="a7cf4-112">Description</span></span>                                             |
|-------------------|---------------------------------------------------------|
| <span data-ttu-id="a7cf4-113">VT \_ R4</span><span class="sxs-lookup"><span data-stu-id="a7cf4-113">VT\_R4</span></span><br/> | <span data-ttu-id="a7cf4-114">Запрошенная Новая скорость воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="a7cf4-114">The requested new playback rate.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="a7cf4-115">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="a7cf4-115">Attributes</span></span>

<span data-ttu-id="a7cf4-116">Для этого события определены следующие атрибуты.</span><span class="sxs-lookup"><span data-stu-id="a7cf4-116">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="a7cf4-117">attribute</span><span class="sxs-lookup"><span data-stu-id="a7cf4-117">Attribute</span></span>                                                                    | <span data-ttu-id="a7cf4-118">Описание</span><span class="sxs-lookup"><span data-stu-id="a7cf4-118">Description</span></span>                                                                       |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="a7cf4-119">**\_событие MF \_ — \_ сужение**</span><span class="sxs-lookup"><span data-stu-id="a7cf4-119">**MF\_EVENT\_DO\_THINNING**</span></span>](mf-event-do-thinning-attribute.md)<br/> | <span data-ttu-id="a7cf4-120">Указывает, будет ли источник мультимедиа запрашивать тонкое.</span><span class="sxs-lookup"><span data-stu-id="a7cf4-120">Specifies whether the media source also requests thinning.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="a7cf4-121">Требования</span><span class="sxs-lookup"><span data-stu-id="a7cf4-121">Requirements</span></span>



| <span data-ttu-id="a7cf4-122">Требование</span><span class="sxs-lookup"><span data-stu-id="a7cf4-122">Requirement</span></span> | <span data-ttu-id="a7cf4-123">Значение</span><span class="sxs-lookup"><span data-stu-id="a7cf4-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7cf4-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a7cf4-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a7cf4-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a7cf4-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a7cf4-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a7cf4-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a7cf4-127">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a7cf4-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a7cf4-128">Header</span><span class="sxs-lookup"><span data-stu-id="a7cf4-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7cf4-129"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a7cf4-129"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7cf4-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a7cf4-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7cf4-131">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a7cf4-131">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




