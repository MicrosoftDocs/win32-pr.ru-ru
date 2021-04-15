---
description: Тип настраиваемого события.
ms.assetid: a54a446c-0e96-467b-90f6-0f64a7c1727d
title: Событие Микстендедтипе (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d5551110fc3637a40834a7bf9251826f151ec62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683133"
---
# <a name="meextendedtype-event"></a><span data-ttu-id="2d944-103">Событие Микстендедтипе</span><span class="sxs-lookup"><span data-stu-id="2d944-103">MEExtendedType event</span></span>

<span data-ttu-id="2d944-104">Тип настраиваемого события.</span><span class="sxs-lookup"><span data-stu-id="2d944-104">Custom event type.</span></span> <span data-ttu-id="2d944-105">Этот тип события можно использовать для определения пользовательских событий для компонента.</span><span class="sxs-lookup"><span data-stu-id="2d944-105">You can use this event type to define custom events for your component.</span></span> <span data-ttu-id="2d944-106">Для обнаружения события используйте тип расширенного события.</span><span class="sxs-lookup"><span data-stu-id="2d944-106">Use the extended event type to identify the event.</span></span> <span data-ttu-id="2d944-107">Тип расширенного события — это значение GUID, связанное с событием.</span><span class="sxs-lookup"><span data-stu-id="2d944-107">The extended event type is a GUID value associated with the event.</span></span> <span data-ttu-id="2d944-108">Дополнительные сведения см. в разделе [**имфмедиаевент:: жетекстендедтипе**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getextendedtype).</span><span class="sxs-lookup"><span data-stu-id="2d944-108">For more information, see [**IMFMediaEvent::GetExtendedType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getextendedtype).</span></span>

## <a name="event-values"></a><span data-ttu-id="2d944-109">Значения событий</span><span class="sxs-lookup"><span data-stu-id="2d944-109">Event values</span></span>

<span data-ttu-id="2d944-110">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="2d944-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="2d944-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="2d944-111">VARTYPE</span></span>              | <span data-ttu-id="2d944-112">Описание</span><span class="sxs-lookup"><span data-stu-id="2d944-112">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="2d944-113">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="2d944-113">VT\_EMPTY</span></span><br/> | <span data-ttu-id="2d944-114">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="2d944-114">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="2d944-115">Требования</span><span class="sxs-lookup"><span data-stu-id="2d944-115">Requirements</span></span>



| <span data-ttu-id="2d944-116">Требование</span><span class="sxs-lookup"><span data-stu-id="2d944-116">Requirement</span></span> | <span data-ttu-id="2d944-117">Значение</span><span class="sxs-lookup"><span data-stu-id="2d944-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d944-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2d944-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2d944-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2d944-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2d944-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2d944-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2d944-121">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2d944-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2d944-122">Header</span><span class="sxs-lookup"><span data-stu-id="2d944-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d944-123"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2d944-123"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d944-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2d944-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d944-125">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2d944-125">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




