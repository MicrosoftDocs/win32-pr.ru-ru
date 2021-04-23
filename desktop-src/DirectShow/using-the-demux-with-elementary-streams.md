---
description: Использование демультиплексирование с простейшими потоками
ms.assetid: dd98aada-8309-428e-9609-2542195bc6ec
title: Использование демультиплексирование с простейшими потоками
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6b9004d6c99db96405797016b0d9854c96dae92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346395"
---
# <a name="using-the-demux-with-elementary-streams"></a><span data-ttu-id="3dd86-103">Использование демультиплексирование с простейшими потоками</span><span class="sxs-lookup"><span data-stu-id="3dd86-103">Using the Demux with Elementary Streams</span></span>

<span data-ttu-id="3dd86-104">Когда MPEG-2 демультиплексирование доставляет ПЕССИМИСТическую полезную нагрузку, он отправляет поток байтов ES в пакетах примеров носителей.</span><span class="sxs-lookup"><span data-stu-id="3dd86-104">When the MPEG-2 demux delivers PES payloads, it sends the ES byte stream in batches of media samples.</span></span> <span data-ttu-id="3dd86-105">Размер выборки по умолчанию — 8 КБ.</span><span class="sxs-lookup"><span data-stu-id="3dd86-105">The default sample size is 8K.</span></span> <span data-ttu-id="3dd86-106">Демультиплексирование запускает новый пример носителя на каждой PES-границе, но может разбивать одну PES-полезную нагрузку на несколько примеров.</span><span class="sxs-lookup"><span data-stu-id="3dd86-106">The demux starts a new media sample on each PES boundary, but may break a single PES payload into several samples.</span></span> <span data-ttu-id="3dd86-107">Например, если 20 000 полезные данные являются недопустимыми, она будет доставляться в двух примерах 8 КБ, за которыми следует один 4-килобайтный пример.</span><span class="sxs-lookup"><span data-stu-id="3dd86-107">For example, if a PES payload is 20K, it will be delivered in two 8K samples followed by one 4K sample.</span></span> <span data-ttu-id="3dd86-108">Демультиплексирование не проверяет содержимое потока байтов.</span><span class="sxs-lookup"><span data-stu-id="3dd86-108">The demux does not examine the contents of the byte stream.</span></span> <span data-ttu-id="3dd86-109">Для анализа заголовков последовательности и поиска изменений формата используется декодер.</span><span class="sxs-lookup"><span data-stu-id="3dd86-109">It is up to the decoder to parse the sequence headers and look for format changes.</span></span>

<span data-ttu-id="3dd86-110">Когда закрепление вывода фильтра демультиплексирование подключается к декодеру, он предлагает тип носителя, указанный при создании ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="3dd86-110">When the demux filter's output pin connects to the decoder, it offers the media type that was specified when the pin was created.</span></span> <span data-ttu-id="3dd86-111">Так как демультиплексирование не проверяет поток байтов ES, он не проверяет тип носителя.</span><span class="sxs-lookup"><span data-stu-id="3dd86-111">Because the demux does not examine the ES byte stream, it does not validate the media type.</span></span> <span data-ttu-id="3dd86-112">Теоретически декодер MPEG-2 должен иметь возможность подключаться только к основным типам и подтипам, которые заполнены, чтобы указать тип данных.</span><span class="sxs-lookup"><span data-stu-id="3dd86-112">In theory, an MPEG-2 decoder should be able to connect with just the major type and subtype filled in, to indicate the type of data.</span></span> <span data-ttu-id="3dd86-113">После этого декодер должен изучить заголовки последовательности, поступающие в образцы мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="3dd86-113">The decoder should then examine the sequence headers that arrive in the media samples.</span></span> <span data-ttu-id="3dd86-114">Однако на практике многие декодеры не будут подключаться, если тип мультимедиа не включает полный блок формата.</span><span class="sxs-lookup"><span data-stu-id="3dd86-114">However, in practice, many decoders will not connect unless the media type includes a complete format block.</span></span>

<span data-ttu-id="3dd86-115">Например, предположим, что PID 0x31 содержит видео о главном профиле MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="3dd86-115">For example, suppose that PID 0x31 contains MPEG-2 main profile video.</span></span> <span data-ttu-id="3dd86-116">Как минимум, необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="3dd86-116">At a minimum, you would need to do the following steps.</span></span>

<span data-ttu-id="3dd86-117">Сначала создайте тип мультимедиа для видео MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="3dd86-117">First, create a media type for MPEG-2 video.</span></span> <span data-ttu-id="3dd86-118">Выйти из блока Format сейчас:</span><span class="sxs-lookup"><span data-stu-id="3dd86-118">Leaving aside the format block for now:</span></span>


```C++
AM_MEDIA_TYPE mt;
ZeroMemory(&mt, sizeof(AM_MEDIA_TYPE));
mt.majortype = MEDIATYPE_Video ;
mt.subtype = MEDIASUBTYPE_MPEG2_VIDEO;
// Possibly create a format block (not shown here).
```



<span data-ttu-id="3dd86-119">Затем создайте закрепление вывода на демультиплексирование:</span><span class="sxs-lookup"><span data-stu-id="3dd86-119">Next, create an output pin on the demux:</span></span>


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



<span data-ttu-id="3dd86-120">Затем запросите новый ПИН-код для интерфейса **IMPEG2PIDMap** и вызовите **маппид**.</span><span class="sxs-lookup"><span data-stu-id="3dd86-120">Then, query the new pin for the **IMPEG2PIDMap** interface and call **MapPID**.</span></span> <span data-ttu-id="3dd86-121">Укажите номер PID 0x30 и \_ простейший \_ поток мультимедиа для PES полезных данных.</span><span class="sxs-lookup"><span data-stu-id="3dd86-121">Specify PID number 0x30, and MEDIA\_ELEMENTARY\_STREAM for PES payloads.</span></span>


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



<span data-ttu-id="3dd86-122">Наконец, освободите все интерфейсы по завершении:</span><span class="sxs-lookup"><span data-stu-id="3dd86-122">Finally, release all interfaces when you are done:</span></span>


```C++
pPin0->Release();
pDemux->Release();
```



<span data-ttu-id="3dd86-123">Ниже приведен более полный пример настройки типа мультимедиа, включая блок Format.</span><span class="sxs-lookup"><span data-stu-id="3dd86-123">Here is a more complete example of setting the media type, including the format block.</span></span> <span data-ttu-id="3dd86-124">В этом примере по-прежнему предполагается видео о основном профиле MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="3dd86-124">This example still assumes an MPEG-2 main profile video.</span></span> <span data-ttu-id="3dd86-125">Сведения будут зависеть от содержимого потока:</span><span class="sxs-lookup"><span data-stu-id="3dd86-125">The details will vary depending on stream contents:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="3dd86-126">См. также</span><span class="sxs-lookup"><span data-stu-id="3dd86-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3dd86-127">Использование демультиплексора MPEG-2</span><span class="sxs-lookup"><span data-stu-id="3dd86-127">Using the MPEG-2 Demultiplexer</span></span>](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 



