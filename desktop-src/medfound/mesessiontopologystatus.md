---
description: Вызывается сеансом мультимедиа при изменении состояния топологии.
ms.assetid: b45fd598-ab1e-4b12-8d82-c88c96d1f770
title: Событие Месессионтопологистатус (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11948e27997037c1e875e192fd712a2f8a132b44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991488"
---
# <a name="mesessiontopologystatus-event"></a><span data-ttu-id="0da12-103">Событие Месессионтопологистатус</span><span class="sxs-lookup"><span data-stu-id="0da12-103">MESessionTopologyStatus event</span></span>

<span data-ttu-id="0da12-104">Вызывается сеансом мультимедиа при изменении состояния топологии.</span><span class="sxs-lookup"><span data-stu-id="0da12-104">Raised by the Media Session when the status of a topology changes.</span></span>

## <a name="event-values"></a><span data-ttu-id="0da12-105">Значения событий</span><span class="sxs-lookup"><span data-stu-id="0da12-105">Event values</span></span>

<span data-ttu-id="0da12-106">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="0da12-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="0da12-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="0da12-107">VARTYPE</span></span>                | <span data-ttu-id="0da12-108">Описание</span><span class="sxs-lookup"><span data-stu-id="0da12-108">Description</span></span>                                                                                         |
|------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0da12-109">VT \_ Unknown</span><span class="sxs-lookup"><span data-stu-id="0da12-109">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="0da12-110">Указатель на интерфейс [**имфтопологи**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) топологии.</span><span class="sxs-lookup"><span data-stu-id="0da12-110">Pointer to the [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) interface of the topology.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="0da12-111">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="0da12-111">Attributes</span></span>

<span data-ttu-id="0da12-112">Для этого события определены следующие атрибуты.</span><span class="sxs-lookup"><span data-stu-id="0da12-112">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="0da12-113">attribute</span><span class="sxs-lookup"><span data-stu-id="0da12-113">Attribute</span></span>                                                                            | <span data-ttu-id="0da12-114">Описание</span><span class="sxs-lookup"><span data-stu-id="0da12-114">Description</span></span>                                                      |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="0da12-115">**\_ \_ состояние ТОПОЛОГИИ событий \_ MF**</span><span class="sxs-lookup"><span data-stu-id="0da12-115">**MF\_EVENT\_TOPOLOGY\_STATUS**</span></span>](mf-event-topology-status-attribute.md)<br/> | <span data-ttu-id="0da12-116">Указывает новое состояние топологии.</span><span class="sxs-lookup"><span data-stu-id="0da12-116">Specifies the new status of the topology.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="0da12-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0da12-117">Remarks</span></span>

<span data-ttu-id="0da12-118">Пример кода, извлекающий указатель [**имфтопологи**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) из события, см. в разделе событие [месессионтопологисет](mesessiontopologyset.md) .</span><span class="sxs-lookup"><span data-stu-id="0da12-118">For a code example that retrieves the [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) pointer from the event, see [MESessionTopologySet](mesessiontopologyset.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="0da12-119">Требования</span><span class="sxs-lookup"><span data-stu-id="0da12-119">Requirements</span></span>



| <span data-ttu-id="0da12-120">Требование</span><span class="sxs-lookup"><span data-stu-id="0da12-120">Requirement</span></span> | <span data-ttu-id="0da12-121">Значение</span><span class="sxs-lookup"><span data-stu-id="0da12-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0da12-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0da12-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0da12-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0da12-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0da12-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0da12-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0da12-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0da12-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0da12-126">Header</span><span class="sxs-lookup"><span data-stu-id="0da12-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="0da12-127"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0da12-127"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0da12-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0da12-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0da12-129">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0da12-129">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




