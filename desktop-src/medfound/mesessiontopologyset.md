---
description: 'Вызывается после асинхронного завершения метода Имфмедиасессион:: Сеттопологи. Сеанс мультимедиа создает это событие после того, как оно разрешает топологию в полную топологию и помещает топологию для воспроизведения в очередь.'
ms.assetid: 22a298b7-d32b-44ed-b0a1-4e0398ecfe04
title: Событие Месессионтопологисет (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 338668b0ec9b4dd81140edfb55a823a5a595459b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991487"
---
# <a name="mesessiontopologyset-event"></a><span data-ttu-id="2897d-104">Событие Месессионтопологисет</span><span class="sxs-lookup"><span data-stu-id="2897d-104">MESessionTopologySet event</span></span>

<span data-ttu-id="2897d-105">Вызывается после асинхронного завершения метода [**имфмедиасессион:: сеттопологи**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) .</span><span class="sxs-lookup"><span data-stu-id="2897d-105">Raised after the [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) method completes asynchronously.</span></span> <span data-ttu-id="2897d-106">Сеанс мультимедиа создает это событие после того, как оно разрешает топологию в полную топологию и помещает топологию для воспроизведения в очередь.</span><span class="sxs-lookup"><span data-stu-id="2897d-106">The Media Session raises this event after it resolves the topology into a full topology and queues the topology for playback.</span></span>

## <a name="event-values"></a><span data-ttu-id="2897d-107">Значения событий</span><span class="sxs-lookup"><span data-stu-id="2897d-107">Event values</span></span>

<span data-ttu-id="2897d-108">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="2897d-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="2897d-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="2897d-109">VARTYPE</span></span>                | <span data-ttu-id="2897d-110">Описание</span><span class="sxs-lookup"><span data-stu-id="2897d-110">Description</span></span>                                                                                              |
|------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2897d-111">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="2897d-111">VT\_EMPTY</span></span><br/>   | <span data-ttu-id="2897d-112">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="2897d-112">No event data.</span></span><br/> <br/>                                                                    |
| <span data-ttu-id="2897d-113">VT \_ Unknown</span><span class="sxs-lookup"><span data-stu-id="2897d-113">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="2897d-114">Указатель на интерфейс [**имфтопологи**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) полной топологии.</span><span class="sxs-lookup"><span data-stu-id="2897d-114">Pointer to the [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) interface of the full topology.</span></span><br/> <br/> |



## <a name="examples"></a><span data-ttu-id="2897d-115">Примеры</span><span class="sxs-lookup"><span data-stu-id="2897d-115">Examples</span></span>

<span data-ttu-id="2897d-116">В следующем примере извлекается указатель [**имфтопологи**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) из события месессионтопологисет.</span><span class="sxs-lookup"><span data-stu-id="2897d-116">The following example retrieves the [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) pointer from an MESessionTopologySet event.</span></span>


```
HRESULT GetTopologyFromEvent(IMFMediaEvent *pEvent, IMFTopology **ppTopology)
{
    HRESULT hr = S_OK;
    PROPVARIANT var;

    PropVariantInit(&var);
    hr = pEvent->GetValue(&var);
    if (SUCCEEDED(hr))
    {
        if (var.vt != VT_UNKNOWN)
        {
            hr = E_UNEXPECTED;
        }
    }
    if (SUCCEEDED(hr))
    {
        hr = var.punkVal->QueryInterface(__uuidof(IMFTopology), (void**)ppTopology);
    }
    PropVariantClear(&var);
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="2897d-117">Требования</span><span class="sxs-lookup"><span data-stu-id="2897d-117">Requirements</span></span>



| <span data-ttu-id="2897d-118">Требование</span><span class="sxs-lookup"><span data-stu-id="2897d-118">Requirement</span></span> | <span data-ttu-id="2897d-119">Значение</span><span class="sxs-lookup"><span data-stu-id="2897d-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2897d-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2897d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2897d-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2897d-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2897d-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2897d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2897d-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2897d-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2897d-124">Header</span><span class="sxs-lookup"><span data-stu-id="2897d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2897d-125"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2897d-125"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2897d-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2897d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2897d-127">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2897d-127">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




