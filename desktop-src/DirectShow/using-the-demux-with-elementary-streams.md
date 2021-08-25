---
description: использование демультиплексирование с простейшим Потоки
ms.assetid: dd98aada-8309-428e-9609-2542195bc6ec
title: использование демультиплексирование с простейшим Потоки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dec805b4c93432c6532edaefac50e9bd15ad8fac5a7d9672fd358c66e57363fd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119964674"
---
# <a name="using-the-demux-with-elementary-streams"></a>использование демультиплексирование с простейшим Потоки

Когда MPEG-2 демультиплексирование доставляет ПЕССИМИСТическую полезную нагрузку, он отправляет поток байтов ES в пакетах примеров носителей. Размер выборки по умолчанию — 8 КБ. Демультиплексирование запускает новый пример носителя на каждой PES-границе, но может разбивать одну PES-полезную нагрузку на несколько примеров. Например, если 20 000 полезные данные являются недопустимыми, она будет доставляться в двух примерах 8 КБ, за которыми следует один 4-килобайтный пример. Демультиплексирование не проверяет содержимое потока байтов. Для анализа заголовков последовательности и поиска изменений формата используется декодер.

Когда закрепление вывода фильтра демультиплексирование подключается к декодеру, он предлагает тип носителя, указанный при создании ПИН-кода. Так как демультиплексирование не проверяет поток байтов ES, он не проверяет тип носителя. Теоретически декодер MPEG-2 должен иметь возможность подключаться только к основным типам и подтипам, которые заполнены, чтобы указать тип данных. После этого декодер должен изучить заголовки последовательности, поступающие в образцы мультимедиа. Однако на практике многие декодеры не будут подключаться, если тип мультимедиа не включает полный блок формата.

Например, предположим, что PID 0x31 содержит видео о главном профиле MPEG-2. Как минимум, необходимо выполнить следующие действия.

Сначала создайте тип мультимедиа для видео MPEG-2. Выйти из блока Format сейчас:


```C++
AM_MEDIA_TYPE mt;
ZeroMemory(&mt, sizeof(AM_MEDIA_TYPE));
mt.majortype = MEDIATYPE_Video ;
mt.subtype = MEDIASUBTYPE_MPEG2_VIDEO;
// Possibly create a format block (not shown here).
```



Затем создайте закрепление вывода на демультиплексирование:


```C++
// Query the demux filter for IMpeg2Demultiplexer.
IMpeg2Demultiplexer *pDemux;
hr = pFilter->QueryInterface(IID_IMpeg2Demultiplexer, (void**)&pDemux);
if (SUCCEEDED(hr))
{
    // Create a new output pin.
    IPin *pPin0;
    hr = pDemux->CreateOutputPin(&mt, L"Video Pin", &pPin0);
    if (SUCCEEDED(hr))
    {
        ....
    }
}
```



Затем запросите новый ПИН-код для интерфейса **IMPEG2PIDMap** и вызовите **маппид**. Укажите номер PID 0x30 и \_ простейший \_ поток мультимедиа для PES полезных данных.


```C++
// Query the pin for IMPEG2PIDMap. This implicitly configures the
// demux to carry a transport stream. 
IMPEG2PIDMap *pPidMap;
hr = pPin0->QueryInterface(IID_IMPEG2PIDMap, (void**)&pPidMap);
if (SUCCEEDED(hr))
{
    // Assign PID 0x31 to pin 0. Set the type to "PES payload."
    ULONG Pid = 0x031;
    hr = pPidMap->MapPID(1, &Pid, MEDIA_ELEMENTARY_STREAM);
    pPidMap->Release();
}
```



Наконец, освободите все интерфейсы по завершении:


```C++
pPin0->Release();
pDemux->Release();
```



Ниже приведен более полный пример настройки типа мультимедиа, включая блок Format. В этом примере по-прежнему предполагается видео о основном профиле MPEG-2. Сведения будут зависеть от содержимого потока:


```C++
// Set up a byte array to hold the first sequence header. 
// This may or may not be required, depending on the decoder.
BYTE SeqHdr[] = { ... };  // Contains the sequence header (not shown).

AM_MEDIA_TYPE mt;
ZeroMemory(&mt, sizeof(AM_MEDIA_TYPE));
mt.majortype = MEDIATYPE_Video ;
mt.subtype = MEDIASUBTYPE_MPEG2_VIDEO;
mt.formattype = FORMAT_MPEG2Video;

// Allocate the format block, including space for the sequence header. 
mt.cbFormat = sizeof(MPEG2VIDEOINFO) + sizeof(SeqHdr);
mt.pbFormat = (BYTE*)CoTaskMemAlloc(mt.cbFormat);
if (mt.pbFormat == NULL)
{
    // Out of memory; return an error code.
}
ZeroMemory(mt.pbFormat, mt.cbFormat);

// Cast the buffer pointer to an MPEG2VIDEOINFO struct.
MPEG2VIDEOINFO *pMVIH = (MPEG2VIDEOINFO*)mt.pbFormat;

RECT rcSrc = {0, 480, 0, 720};        // Source rectangle.
pMVIH->hdr.rcSource = rcSrc;
pMVIH->hdr.dwBitRate = 4000000;       // Bit rate.
pMVIH->hdr.AvgTimePerFrame = 333667;  // 29.97 fps.
pMVIH->hdr.dwPictAspectRatioX = 4;    // 4:3 aspect ratio.
pMVIH->hdr.dwPictAspectRatioY = 3;

// BITMAPINFOHEADER information.
pMVIH->hdr.bmiHeader.biSize = 40;
pMVIH->hdr.bmiHeader.biWidth = 720;
pMVIH->hdr.bmiHeader.biHeight = 480;

pMVIH->dwLevel = AM_MPEG2Profile_Main;  // MPEG-2 profile. 
pMVIH->dwProfile = AM_MPEG2Level_Main;  // MPEG-2 level.

// Copy the sequence header into the format block.
pMVIH->cbSequenceHeader = sizeof(SeqHdr); // Size of sequence header.
memcpy(pMVIH->dwSequenceHeader, SeqHdr, sizeof(SeqHdr));
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование демультиплексора MPEG-2](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 



