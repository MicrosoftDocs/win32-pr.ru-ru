---
description: использование демультиплексирование с PSI Потоки
ms.assetid: 355e905e-ff21-4bde-a018-ed9631ef5ed5
title: использование демультиплексирование с PSI Потоки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3935e188b6e06d1037f08d4ca7bab98918f87d2c652b8506650a6cf3a280dc04
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633144"
---
# <a name="using-the-demux-with-psi-streams"></a>использование демультиплексирование с PSI Потоки

Чтобы получить сведения PSI из транспортного потока MPEG-2 с помощью фильтра демультиплексирование MPEG-2, создайте выходной ПИН-код на демультиплексирование со следующим типом носителя:

-   Основной тип: \_ разделы ксдатаформат типа \_ MPEG2 \_
-   Подтип: МЕДИАСУБТИПЕ \_ None
-   Тип формата: GUID \_ null

Затем вызовите метод [**IMPEG2PIDMap:: маппид**](/previous-versions/windows/desktop/api/Bdaiface/nf-bdaiface-impeg2pidmap-mappid) выходного контакта с нужным PID и флагом Media \_ MPEG2 \_ PSI.


```C++
// Query the demux filter for IMpeg2Demultiplexer.
IMpeg2Demultiplexer *pDemux = NULL;
hr = pFilter->QueryInterface(IID_IMpeg2Demultiplexer, (void**)&pDemux);
if (SUCCEEDED(hr))
{
    // Define the media type.
    AM_MEDIA_TYPE mt;
    ZeroMemory(&mt, sizeof(AM_MEDIA_TYPE));
    mt.majortype = KSDATAFORMAT_TYPE_MPEG2_SECTIONS;
    mt.subtype = MEDIASUBTYPE_None;

    // Create a new output pin.
    IPin *pPin;
    hr = pDemux->CreateOutputPin(&mt, L"PSI Pin", &pPin);
    if (SUCCEEDED(hr))
    {
        // Map the PID.
        IMPEG2PIDMap *pPidMap = NULL;
        hr = pPin->QueryInterface(IID_IMPEG2PIDMap, (void**)&pPidMap);
        if (SUCCEEDED(hr))
        {
            ULONG Pid[] = { 0x00 }; // Map any desired PIDs. 
            ULONG cPid = 1;
            hr = pPidMap->MapPID(cPid, Pid, MEDIA_MPEG2_PSI);
            pPidMap->Release();
        }
        pPin->Release();
    }
    pDemux->Release();
}
```



Каждый раздел PSI доставляется в один пример носителя. Чтобы получить номер PID, связанный с разделом таблицы, вызовите [**IMediaSample2::-Properties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) в примере носителя. Идентификатор процесса указывается в младших 13 битах флага **двтипеспеЦификфлагс** в структуре **\_ \_ свойств SAMPLE2** . Это полезно при сопоставлении нескольких PID PSI с одним и тем же выходным ПИН-кодом.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование демультиплексора MPEG-2](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 



