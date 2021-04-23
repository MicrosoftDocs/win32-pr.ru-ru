---
description: Медевицестреамкреатед — это расширенный тип события мультимедиа, созданный с помощью события мультимедиа Меункновн в MFT устройства.
ms.assetid: 8aaa6908-0f2e-4a73-9362-69f42b74f495
title: Событие Медевицестреамкреатед (мфтрансформ. h)
ms.topic: article
ms.date: 08/31/2018
ms.openlocfilehash: 632ebc305473cd596656a21f562be25d53c2bace
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263367"
---
# <a name="medevicestreamcreated-event"></a><span data-ttu-id="ad7d2-103">Событие Медевицестреамкреатед</span><span class="sxs-lookup"><span data-stu-id="ad7d2-103">MEDeviceStreamCreated event</span></span>

<span data-ttu-id="ad7d2-104">Медевицестреамкреатед — это расширенный тип события мультимедиа, созданный с помощью события мультимедиа Меункновн в MFT устройства.</span><span class="sxs-lookup"><span data-stu-id="ad7d2-104">MEDeviceStreamCreated is an extended media event type generated with an MEUnknown media event by the Device MFT.</span></span>

<span data-ttu-id="ad7d2-105">Этот расширенный тип события мультимедиа не имеет полезных данных.</span><span class="sxs-lookup"><span data-stu-id="ad7d2-105">This extended media event type has no payload.</span></span>  <span data-ttu-id="ad7d2-106">Соответствующие значения HRESULT должны быть предоставлены с помощью метода [**имфмедиаевент:: with Status**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) .</span><span class="sxs-lookup"><span data-stu-id="ad7d2-106">Appropriate HRESULT should be provided via the [**IMFMediaEvent::GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) method.</span></span>




## <a name="remarks"></a><span data-ttu-id="ad7d2-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ad7d2-107">Remarks</span></span>

<span data-ttu-id="ad7d2-108">Это расширенное событие мультимедиа должно быть отправлено файлом MFT устройства как часть выбора типа носителя в потоке вывода ДМФТ.</span><span class="sxs-lookup"><span data-stu-id="ad7d2-108">This extended media event must be sent by the Device MFT as a part of the media type selection on the output stream of the DMFT.</span></span>  <span data-ttu-id="ad7d2-109">Когда Сетаутпутстреамстате вызывается в интерфейсе Имфдевицетрансформ, ДМФТ отвечает за передачу изменений в требуемых состояниях входного потока с помощью события [метрансформинпутстреамстатечанжед](/windows-hardware/drivers/stream/metransforminputstreamstatechanged) мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="ad7d2-109">When the SetOutputStreamState is invoked on the IMFDeviceTransform interface, the DMFT is responsible for signaling the change in the required input stream states with the [METransformInputStreamStateChanged](/windows-hardware/drivers/stream/metransforminputstreamstatechanged) media event.</span></span> <span data-ttu-id="ad7d2-110">Когда изменение состояния входного потока было подтверждено конвейером с помощью вызова Сетинпутстреамстате из ДМФТ, ДМФТ отвечает за завершение своей внутренней настройки состояния и создание типа события **медевицестреамкреатед** Extended Media.</span><span class="sxs-lookup"><span data-stu-id="ad7d2-110">When the input stream state change has been acknowledged by the pipeline with the call into SetInputStreamState of the DMFT, the DMFT is responsible for completing its internal state configuration and raising the **MEDeviceStreamCreated** extended media event type.</span></span>

<span data-ttu-id="ad7d2-111">Если этот расширенный тип события мультимедиа не вызывается, Диспетчер преобразования устройств не будет доставлять входные кадры в ДМФТ.</span><span class="sxs-lookup"><span data-stu-id="ad7d2-111">If this extended media event type is not raised, the Device Transform Manager will not deliver any input frames to the DMFT.</span></span>
<span data-ttu-id="ad7d2-112">Расширенный тип события мультимедиа также должен задаваться как атрибут Имфмедиаевент, идентификатор потока вывода с помощью атрибута **MF_EVENT_MFT_INPUT_STREAM_ID** .</span><span class="sxs-lookup"><span data-stu-id="ad7d2-112">The extended media event type must also set as an attribute of the IMFMediaEvent, the output stream ID using the **MF_EVENT_MFT_INPUT_STREAM_ID** attribute.</span></span>

```cpp
IMFMediaEvent* pMediaEvent = nullptr;

hr = MFCreateMediaEvent (MEUnknown,
                         MEDeviceStreamCreated,
                         S_OK,
                         nullptr,
                         &pMediaEvent);
if (SUCCEEDED(hr))
{
    hr = pMediaEvent->SetUINT32(MF_EVENT_MFT_INPUT_STREAM_ID, GetOutputStreamId());
}

if (SUCCEEDED(hr))
{
    hr = m_pEventQueue->QueueEvent(pMediaEvent);
}

if (nullptr != pMediaEvent)
{
    pMediaEvent->Release();
    pMediaEvent = nullptr;
}

return hr;
```

## <a name="requirements"></a><span data-ttu-id="ad7d2-113">Требования</span><span class="sxs-lookup"><span data-stu-id="ad7d2-113">Requirements</span></span>



| <span data-ttu-id="ad7d2-114">Требование</span><span class="sxs-lookup"><span data-stu-id="ad7d2-114">Requirement</span></span> | <span data-ttu-id="ad7d2-115">Значение</span><span class="sxs-lookup"><span data-stu-id="ad7d2-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad7d2-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ad7d2-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ad7d2-117">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="ad7d2-117">Windows 10 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ad7d2-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ad7d2-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ad7d2-119">\[Только для настольных приложений Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="ad7d2-119">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ad7d2-120">Header</span><span class="sxs-lookup"><span data-stu-id="ad7d2-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad7d2-121"><dt>мфтрансформ. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad7d2-121"><dt>mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad7d2-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ad7d2-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad7d2-123">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ad7d2-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="ad7d2-124">Потоковая прорисовка звука</span><span class="sxs-lookup"><span data-stu-id="ad7d2-124">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 
