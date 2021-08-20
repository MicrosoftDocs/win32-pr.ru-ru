---
description: Медевицестреамкреатед — это расширенный тип события мультимедиа, созданный с помощью события мультимедиа Меункновн в MFT устройства.
ms.assetid: 8aaa6908-0f2e-4a73-9362-69f42b74f495
title: Событие Медевицестреамкреатед (мфтрансформ. h)
ms.topic: article
ms.date: 08/31/2018
ms.openlocfilehash: 99e13dae5db9d680909a435d5520f6b07d7d4b6c11782c340b72fcdd0eddc53a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117878071"
---
# <a name="medevicestreamcreated-event"></a>Событие Медевицестреамкреатед

Медевицестреамкреатед — это расширенный тип события мультимедиа, созданный с помощью события мультимедиа Меункновн в MFT устройства.

Этот расширенный тип события мультимедиа не имеет полезных данных.  Соответствующие значения HRESULT должны быть предоставлены с помощью метода [**имфмедиаевент:: with Status**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) .




## <a name="remarks"></a>Remarks

Это расширенное событие мультимедиа должно быть отправлено файлом MFT устройства как часть выбора типа носителя в потоке вывода ДМФТ.  Когда Сетаутпутстреамстате вызывается в интерфейсе Имфдевицетрансформ, ДМФТ отвечает за передачу изменений в требуемых состояниях входного потока с помощью события [метрансформинпутстреамстатечанжед](/windows-hardware/drivers/stream/metransforminputstreamstatechanged) мультимедиа. Когда изменение состояния входного потока было подтверждено конвейером с помощью вызова Сетинпутстреамстате из ДМФТ, ДМФТ отвечает за завершение своей внутренней настройки состояния и создание типа события **медевицестреамкреатед** Extended Media.

Если этот расширенный тип события мультимедиа не вызывается, Диспетчер преобразования устройств не будет доставлять входные кадры в ДМФТ.
Расширенный тип события мультимедиа также должен задаваться как атрибут Имфмедиаевент, идентификатор потока вывода с помощью атрибута **MF_EVENT_MFT_INPUT_STREAM_ID** .

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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10 \[ только классические приложения\]<br/>                                                           |
| Минимальная версия сервера<br/> | Windows Server 2016 \[ только классические приложения\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>мфтрансформ. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[События Media Foundation](media-foundation-events.md)
</dt> <dt>

[Потоковая прорисовка звука](streaming-audio-renderer.md)
</dt> </dl>

 

 
