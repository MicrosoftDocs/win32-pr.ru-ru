---
description: Просмотр скрытых субтитров
ms.assetid: 86c0c553-af35-4ad1-8918-63d9e4577c73
title: Просмотр скрытых субтитров
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82ff2d6d213259ccce6e9b02272d0c9db3ad7b71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104566664"
---
# <a name="viewing-closed-captions"></a><span data-ttu-id="7afad-103">Просмотр скрытых субтитров</span><span class="sxs-lookup"><span data-stu-id="7afad-103">Viewing Closed Captions</span></span>

<span data-ttu-id="7afad-104">Для поддержки субтитров в аналоговом телевизоре фильтр записи предоставляет ПИН-код, который доставляет либо ВБИ, либо закрытые данные субтитров.</span><span class="sxs-lookup"><span data-stu-id="7afad-104">To support closed captions in analog television, the capture filter exposes a pin that delivers either VBI or closed caption data.</span></span> <span data-ttu-id="7afad-105">ПИН-код будет иметь одну из следующих категорий ПИН-кода:</span><span class="sxs-lookup"><span data-stu-id="7afad-105">The pin will have one of the following pin categories:</span></span>

-   <span data-ttu-id="7afad-106">ВБИ (закрепить \_ категорию \_ ВБИ).</span><span class="sxs-lookup"><span data-stu-id="7afad-106">VBI pin (PIN\_CATEGORY\_VBI).</span></span> <span data-ttu-id="7afad-107">Доставляет поток примеров ВБИ волны.</span><span class="sxs-lookup"><span data-stu-id="7afad-107">Delivers a stream of VBI waveform samples.</span></span> <span data-ttu-id="7afad-108">Они передаются в фильтр декодера, который извлекает данные о закрытых субтитрах.</span><span class="sxs-lookup"><span data-stu-id="7afad-108">These are passed to a decoder filter that extracts the closed captioning data.</span></span>
-   <span data-ttu-id="7afad-109">ПИН-код копии (закрепить \_ категорию \_ CC).</span><span class="sxs-lookup"><span data-stu-id="7afad-109">CC pin (PIN\_CATEGORY\_CC).</span></span> <span data-ttu-id="7afad-110">Предоставляет пары байтов закрытых субтитров, извлеченные из данных строки 21.</span><span class="sxs-lookup"><span data-stu-id="7afad-110">Delivers closed-caption byte pairs, extracted from the line-21 data.</span></span>
-   <span data-ttu-id="7afad-111">Аппаратное копирование ПИН-кода для создания среза копии (ПИННАМЕ \_ видео \_ CC \_ ).</span><span class="sxs-lookup"><span data-stu-id="7afad-111">Hardware slicing CC pin (PINNAME\_VIDEO\_CC\_CAPTURE).</span></span>

<span data-ttu-id="7afad-112">Чтобы предварительно просмотреть скрытые субтитры, вызовите [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) с категорией ВБИ PIN. Если это не удается, вызовите его снова с помощью категории CC.</span><span class="sxs-lookup"><span data-stu-id="7afad-112">To preview closed captions, call [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) with the VBI pin category, and if that fails, call it again with the CC category.</span></span>


```C++
hr = pBuild->RenderStream(&PIN_CATEGORY_VBI, 0, pCap, 0, 0);
if (FAILED(hr))
{
    hr = pBuild->RenderStream(&PIN_CATEGORY_CC, 0, pCap, 0, 0);
}
```



<span data-ttu-id="7afad-113">На следующей диаграмме показан типичный граф фильтра для отображения закрытых субтитров.</span><span class="sxs-lookup"><span data-stu-id="7afad-113">The following diagram shows a typical filter graph for displaying closed captions.</span></span>

![Диаграмма предварительного просмотра скрытых субтитров](images/vidcap08.png)

<span data-ttu-id="7afad-115">Эта диаграмма использует следующие фильтры для отображения скрытых субтитров:</span><span class="sxs-lookup"><span data-stu-id="7afad-115">This graph uses the following filters for closed caption display:</span></span>

-   <span data-ttu-id="7afad-116">[Преобразователь tee/Sink-to-Sink](tee-sink-to-sink-converter.md).</span><span class="sxs-lookup"><span data-stu-id="7afad-116">[Tee/Sink-to-Sink Converter](tee-sink-to-sink-converter.md).</span></span> <span data-ttu-id="7afad-117">Принимает сведения ВБИ из фильтра записи и разделяет их на отдельные потоки для каждой из служб данных, имеющихся в сигнале.</span><span class="sxs-lookup"><span data-stu-id="7afad-117">Accepts the VBI information from the capture filter and splits it into separate streams for each of the data services present on the signal.</span></span> <span data-ttu-id="7afad-118">Корпорация Майкрософт предоставляет кодеки ВБИ для скрытых титров, НАБТС и стандартных телетекстов (WST).</span><span class="sxs-lookup"><span data-stu-id="7afad-118">Microsoft provides VBI codecs for Closed Caption, NABTS, and World Standard Teletext (WST).</span></span>
-   <span data-ttu-id="7afad-119">[Декодер CC](cc-decoder-filter.md).</span><span class="sxs-lookup"><span data-stu-id="7afad-119">[CC Decoder](cc-decoder-filter.md).</span></span> <span data-ttu-id="7afad-120">Декодирует данные CC из образцов аудио ВБИ, предоставленных фильтром записи.</span><span class="sxs-lookup"><span data-stu-id="7afad-120">Decodes CC data from the sampled VBI waveforms provided by the capture filter.</span></span>
-   <span data-ttu-id="7afad-121">[Декодер 21 Line](line-21-decoder-filter.md).</span><span class="sxs-lookup"><span data-stu-id="7afad-121">[Line 21 Decoder](line-21-decoder-filter.md).</span></span> <span data-ttu-id="7afad-122">Преобразует пары байтов копии и рисует текст заголовка на точечные рисунки.</span><span class="sxs-lookup"><span data-stu-id="7afad-122">Translates the CC byte pairs and draws the caption text onto bitmaps.</span></span> <span data-ttu-id="7afad-123">Нисходящий фильтр (в данном случае микшер наложения) накладывает на видео растровые изображения.</span><span class="sxs-lookup"><span data-stu-id="7afad-123">The downstream filter (in this case the Overlay Mixer) overlays the bitmaps onto the video.</span></span>

<span data-ttu-id="7afad-124">Метод [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) в построителе графов записи добавляет эти фильтры автоматически.</span><span class="sxs-lookup"><span data-stu-id="7afad-124">The Capture Graph Builder's [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method adds these filters automatically.</span></span> <span data-ttu-id="7afad-125">Если фильтр записи имеет ПИН-код CC, а не ВБИ ПИН-код, то ПИН-код CC подключается непосредственно к фильтру декодера Line 21.</span><span class="sxs-lookup"><span data-stu-id="7afad-125">If the capture filter has a CC pin instead of a VBI pin, the CC pin is connected directly to the Line 21 Decoder filter.</span></span>

> [!Note]  
> <span data-ttu-id="7afad-126">Если для подготовки к просмотру используется фильтр формирователя видео (VMR), используйте строку 21 декодер Filter 2.</span><span class="sxs-lookup"><span data-stu-id="7afad-126">If you are using the Video Mixing Renderer (VMR) filter for rendering, use the Line 21 Decoder Filter 2.</span></span> <span data-ttu-id="7afad-127">Этот фильтр имеет те же функциональные возможности, что и Line 21 декодер, но идентификатором CLSID является CLSID \_ Line21Decoder2.</span><span class="sxs-lookup"><span data-stu-id="7afad-127">This filter has the same functionality as the Line 21 Decoder, but the CLSID is CLSID\_Line21Decoder2.</span></span>

 

> [!Note]  
> <span data-ttu-id="7afad-128">Фильтр декодера CC был удален в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7afad-128">The CC Decoder filter was removed in Windows Vista.</span></span> <span data-ttu-id="7afad-129">Новые приложения должны использовать фильтр Вбикодек, который описан в документации по технологиям Microsoft TV.</span><span class="sxs-lookup"><span data-stu-id="7afad-129">New applications should use the VBICodec filter, which is documented in the Microsoft TV Technologies documentation.</span></span>

 

<span data-ttu-id="7afad-130">Если устройство записи использует порт видео, фильтр записи может иметь ПИН-код ВБИ ( \_ Категория \_ видеопорт \_ ВБИ).</span><span class="sxs-lookup"><span data-stu-id="7afad-130">If the capture device uses a video port, the capture filter might have a video port VBI pin (PIN\_CATEGORY\_VIDEOPORT\_VBI).</span></span> <span data-ttu-id="7afad-131">Этот ПИН-код должен быть подключен к фильтру [распределителя ВБИ Surface](vbi-surface-allocator.md) , который выделяет поверхности для хранения захваченных данных ВБИ.</span><span class="sxs-lookup"><span data-stu-id="7afad-131">This pin must be connected to the [VBI Surface Allocator](vbi-surface-allocator.md) filter, which allocates surfaces to hold the captured VBI data.</span></span> <span data-ttu-id="7afad-132">Метод [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) добавляет этот фильтр, если он необходим.</span><span class="sxs-lookup"><span data-stu-id="7afad-132">The [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method adds this filter if it is required.</span></span> <span data-ttu-id="7afad-133">На следующей схеме показан граф фильтра с распределительной поверхностью ВБИ.</span><span class="sxs-lookup"><span data-stu-id="7afad-133">The following diagram shows a filter graph with the VBI Surface Allocator.</span></span>

![Диаграмма предварительного просмотра субтитров с распределительной поверхностью ВБИ](images/vidcap09.png)

### <a name="enabling-and-disabling-the-captions"></a><span data-ttu-id="7afad-135">Включение и отключение заголовков</span><span class="sxs-lookup"><span data-stu-id="7afad-135">Enabling and Disabling the Captions</span></span>

<span data-ttu-id="7afad-136">Для управления отображением субтитров используйте интерфейс [**IAMLine21Decoder**](/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder) в фильтре Line 21.</span><span class="sxs-lookup"><span data-stu-id="7afad-136">To control the captioning display, use the [**IAMLine21Decoder**](/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder) interface on the Line 21 Decoder filter.</span></span> <span data-ttu-id="7afad-137">Например, можно отключить отображение субтитров с помощью метода [**IAMLine21Decoder:: SetServiceState**](/previous-versions/windows/desktop/api/il21dec/nf-il21dec-iamline21decoder-setservicestate) следующим образом:</span><span class="sxs-lookup"><span data-stu-id="7afad-137">For example, you can turn off the captioning display using the [**IAMLine21Decoder::SetServiceState**](/previous-versions/windows/desktop/api/il21dec/nf-il21dec-iamline21decoder-setservicestate) method, as follows:</span></span>


```C++
// Use the FindInterface method to find the interface.
IAMLine21Decoder *pLine21 = NULL;
hr = pBuild->FindInterface(
    &LOOK_DOWNSTREAM_ONLY, // Look downstream from pCap 
    NULL,                  // No particular media type
    pCap,                  // Pointer to the capture filter.
    IID_IAMLine21Decoder, (void**)&pLine21);
if (SUCCEEDED(hr))
{
    pLine21->SetServiceState(AM_L21_CCSTATE_Off);
    // (Use AM_L21_CCSTATE_On to enable.)
    pLine21->Release();
}
```



<span data-ttu-id="7afad-138">В этом примере используется метод [**ICaptureGraphBuilder2:: финдинтерфаце**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) для размещения интерфейса [**IAMLine21Decoder**](/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder) .</span><span class="sxs-lookup"><span data-stu-id="7afad-138">This example uses the [**ICaptureGraphBuilder2::FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) method to locate the [**IAMLine21Decoder**](/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder) interface.</span></span> <span data-ttu-id="7afad-139">Первый параметр для **финдинтерфаце** **&выглядеть \_ \_ только по нисходящей**, который указывает, что нужно искать дальше от фильтра записи (*ПКАП*).</span><span class="sxs-lookup"><span data-stu-id="7afad-139">The first parameter to **FindInterface** is **&LOOK\_DOWNSTREAM\_ONLY**, which specifies to search downstream from the capture filter (*pCap*).</span></span>

### <a name="capturing-closed-caption-bitmaps"></a><span data-ttu-id="7afad-140">Запись растровых изображений скрытых заголовков</span><span class="sxs-lookup"><span data-stu-id="7afad-140">Capturing Closed Caption Bitmaps</span></span>

<span data-ttu-id="7afad-141">Точечные рисунки заголовков можно записать в файл.</span><span class="sxs-lookup"><span data-stu-id="7afad-141">You can capture the caption bitmaps into a file.</span></span> <span data-ttu-id="7afad-142">Для этого добавьте раздел "запись файлов" графа фильтра, как описано в разделе [запись видео в файл](capturing-video-to-a-file.md).</span><span class="sxs-lookup"><span data-stu-id="7afad-142">To do so, add the file-writing section of the filter graph, as described in [Capturing Video to a File](capturing-video-to-a-file.md).</span></span> <span data-ttu-id="7afad-143">Затем отрисовываете ПИН-код CC или ВБИ в фильтре мультиплексора:</span><span class="sxs-lookup"><span data-stu-id="7afad-143">Then render the CC or VBI pin to the mux filter:</span></span>


```C++
hr = pBuild->RenderStream(&PIN_CATEGORY_VBI, 0, pCap, 0, pMux);
if (FAILED(hr))
{
    hr = pBuild->RenderStream(&PIN_CATEGORY_CC, 0, pCap, 0, pMux);
}
```



<span data-ttu-id="7afad-144">Если вы также записываете видео, будет создан файл с двумя отдельными видеопотоками.</span><span class="sxs-lookup"><span data-stu-id="7afad-144">If you are also capturing the video, this will create a file with two separate video streams.</span></span> <span data-ttu-id="7afad-145">Видео с субтитрами, наложенными поверх изображения, не записываются.</span><span class="sxs-lookup"><span data-stu-id="7afad-145">It will not capture video with captions overlaid on top of the picture.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7afad-146">См. также</span><span class="sxs-lookup"><span data-stu-id="7afad-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7afad-147">Субтитры и телетекст</span><span class="sxs-lookup"><span data-stu-id="7afad-147">Closed Captions and Teletext</span></span>](closed-captions-and-teletext.md)
</dt> </dl>

 

 



