---
description: Запись видео в файл Windows Media
ms.assetid: cc23bfce-34b9-4976-8602-e0602c7da2af
title: Запись видео в файл Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6442c1cf3751beac8d4eba751452d9573e9eede
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "104273260"
---
# <a name="capturing-video-to-a-windows-media-file"></a><span data-ttu-id="3a503-103">Запись видео в файл Windows Media</span><span class="sxs-lookup"><span data-stu-id="3a503-103">Capturing Video to a Windows Media File</span></span>

<span data-ttu-id="3a503-104">Чтобы записать видео и закодировать его в файл Windows Media Video (WMV), подключите ПИН-код записи к фильтру [модуля записи WM ASF](wm-asf-writer-filter.md) , как показано на следующей схеме.</span><span class="sxs-lookup"><span data-stu-id="3a503-104">To capture video and encode it to a Windows Media Video (WMV) file, connect the capture pin to the [WM ASF Writer](wm-asf-writer-filter.md) filter, as shown in the following diagram.</span></span>

![Диаграмма записи мультимедиа Windows](images/vidcap03.png)

<span data-ttu-id="3a503-106">Самый простой способ создать этот граф — задающего МЕДИАСУБТИПЕ \_ ASF в методе [**ICaptureGraphBuilder2:: сетаутпутфиленаме**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) :</span><span class="sxs-lookup"><span data-stu-id="3a503-106">The easiest way to build this graph is by specifing MEDIASUBTYPE\_Asf in the [**ICaptureGraphBuilder2::SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) method:</span></span>


```C++
IBaseFilter* pASFWriter = 0;
hr = pBuild->SetOutputFileName(
    &MEDIASUBTYPE_Asf,   // Create a Windows Media file.
    L"C:\\VidCap.wmv",   // File name.
    &pASFWriter,         // Receives a pointer to the filter.
    NULL);  // Receives an IFileSinkFilter interface pointer (optional).
```



<span data-ttu-id="3a503-107">Значение МЕДИАСУБТИПЕ \_ ASF сообщает построителю диаграмм о записи, что в качестве приемника файла используется фильтр модуля записи WM ASF.</span><span class="sxs-lookup"><span data-stu-id="3a503-107">The value MEDIASUBTYPE\_Asf tells the Capture Graph Builder to use the WM ASF Writer filter as the file sink.</span></span> <span data-ttu-id="3a503-108">Построитель диаграмм записи создает фильтр, добавляет его в граф и вызывает метод [**ифилесинкфилтер:: сетфиленаме**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) , чтобы задать имя выходного файла.</span><span class="sxs-lookup"><span data-stu-id="3a503-108">The Capture Graph Builder creates the filter, adds it to the graph, and calls [**IFileSinkFilter::SetFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) to set the name of the output file.</span></span> <span data-ttu-id="3a503-109">Он возвращает указатель на фильтр в качестве исходящего параметра (</span><span class="sxs-lookup"><span data-stu-id="3a503-109">It returns a pointer to the filter as an outgoing parameter (</span></span>


```
pASFWriter
```



<span data-ttu-id="3a503-110">в предыдущем примере).</span><span class="sxs-lookup"><span data-stu-id="3a503-110">in the previous example).</span></span>

<span data-ttu-id="3a503-111">Чтобы задать профиль Windows Media, используйте интерфейс [**иконфигасфвритер**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter) в модуле записи WM ASF.</span><span class="sxs-lookup"><span data-stu-id="3a503-111">Use the [**IConfigAsfWriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter) interface on the WM ASF Writer to set the Windows Media profile.</span></span> <span data-ttu-id="3a503-112">Это необходимо сделать перед подключением любых ПИН-кодов в модуле записи WM ASF.</span><span class="sxs-lookup"><span data-stu-id="3a503-112">You must do this before you connect any pins on the WM ASF Writer.</span></span>


```C++
IConfigAsfWriter *pConfig = 0;
hr = pASFWriter->QueryInterface(IID_IConfigAsfWriter, (void**)&pConfig);
if (SUCCEEDED(hr))
{
     // Configure the ASF Writer filter.
    pConfig->Release();
}
```



<span data-ttu-id="3a503-113">Дополнительные сведения о настройке профиля см. в разделе [Создание файлов ASF в DirectShow](creating-asf-files-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="3a503-113">For more information about setting the profile, see [Creating ASF Files in DirectShow](creating-asf-files-in-directshow.md).</span></span>

<span data-ttu-id="3a503-114">Вызовите [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) , чтобы подключить фильтр записи к модулю записи ASF:</span><span class="sxs-lookup"><span data-stu-id="3a503-114">Call [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) to connect the capture filter to the ASF Writer:</span></span>


```C++
hr = pBuild->RenderStream(
    &PIN_CATEGORY_CAPTURE,   // Capture pin.
    &MEDIATYPE_Video,        // Video. Use MEDIATYPE_Audio for audio.
    pCap,                    // Pointer to the capture filter. 
    0, 
    pASFWriter);             // Pointer to the sink filter (ASF Writer).
```



<span data-ttu-id="3a503-115">Каждый входной ПИН-код в фильтре модуля записи WM ASF соответствует потоку в профиле Windows Media.</span><span class="sxs-lookup"><span data-stu-id="3a503-115">Each input pin on the WM ASF Writer filter corresponds to a stream in the Windows Media profile.</span></span> <span data-ttu-id="3a503-116">Необходимо подключить каждый ПИН-код, чтобы содержимое файла совпадало с профилем.</span><span class="sxs-lookup"><span data-stu-id="3a503-116">You must connect every pin, so that the file content matches the profile.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3a503-117">См. также</span><span class="sxs-lookup"><span data-stu-id="3a503-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a503-118">Запись видео в файл</span><span class="sxs-lookup"><span data-stu-id="3a503-118">Capturing Video to a File</span></span>](capturing-video-to-a-file.md)
</dt> </dl>

 

 



