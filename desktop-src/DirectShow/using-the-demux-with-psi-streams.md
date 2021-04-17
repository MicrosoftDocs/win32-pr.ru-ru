---
description: Использование демультиплексирование с потоками PSI
ms.assetid: 355e905e-ff21-4bde-a018-ed9631ef5ed5
title: Использование демультиплексирование с потоками PSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 659e4a12bfef25f24a5e6cac38d191f86ab80b4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663763"
---
# <a name="using-the-demux-with-psi-streams"></a>Использование демультиплексирование с потоками PSI

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

## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование демультиплексора MPEG-2](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 



