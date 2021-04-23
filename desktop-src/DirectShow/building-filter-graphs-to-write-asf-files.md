---
description: Создание графов фильтра для записи файлов ASF
ms.assetid: c4885152-d7d2-4749-a79a-e0effd38837d
title: Создание графов фильтра для записи файлов ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0581672f9fd3e4bfa5e2c678c3bd3c0d3ea22fa0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495456"
---
# <a name="building-filter-graphs-to-write-asf-files"></a><span data-ttu-id="9845e-103">Создание графов фильтра для записи файлов ASF</span><span class="sxs-lookup"><span data-stu-id="9845e-103">Building Filter Graphs to Write ASF Files</span></span>

<span data-ttu-id="9845e-104">При создании содержимого на основе Windows Media в приложениях обычно используется один из следующих сценариев:</span><span class="sxs-lookup"><span data-stu-id="9845e-104">When creating Windows Media–based content, applications typically use one of the following scenarios:</span></span>

-   <span data-ttu-id="9845e-105">Преобразование или перекодирование содержимого из другого формата в формат Windows Media.</span><span class="sxs-lookup"><span data-stu-id="9845e-105">Converting or transcoding content from some other format into Windows Media Format.</span></span>
-   <span data-ttu-id="9845e-106">Вставка содержимого, не основанного на мультимедиа Windows (собственные форматы потока), в файлы ASF.</span><span class="sxs-lookup"><span data-stu-id="9845e-106">Inserting content that is not Windows Media-based (native stream formats) into ASF files.</span></span>
-   <span data-ttu-id="9845e-107">Запись динамических данных и их кодирование непосредственно в формате Windows Media.</span><span class="sxs-lookup"><span data-stu-id="9845e-107">Capturing live data and encoding it immediately into Windows Media Format.</span></span>

<span data-ttu-id="9845e-108">Перекодирование файлов ASF</span><span class="sxs-lookup"><span data-stu-id="9845e-108">Transcoding ASF Files</span></span>

<span data-ttu-id="9845e-109">Вы можете создать граф фильтра для перекодирования файлов с помощью [модуля записи WM ASF](wm-asf-writer-filter.md) различными способами.</span><span class="sxs-lookup"><span data-stu-id="9845e-109">You can build a file-transcoding filter graph using the [WM ASF Writer](wm-asf-writer-filter.md) in various ways.</span></span> <span data-ttu-id="9845e-110">Самый простой способ — добавить модуль записи WM ASF в граф фильтра, а затем использовать метод Играфбуилдер:: RenderFile для автоматической сборки графа.</span><span class="sxs-lookup"><span data-stu-id="9845e-110">The easiest way is to add the WM ASF Writer to the filter graph and then use the IGraphBuilder::RenderFile method to build the graph automatically.</span></span>

<span data-ttu-id="9845e-111">Другой способ — добавить каждый фильтр на диаграмму вручную и соединить эти контакты.</span><span class="sxs-lookup"><span data-stu-id="9845e-111">An alternative way is to add each filter manually to the graph and connect the pins.</span></span> <span data-ttu-id="9845e-112">После добавления модуля записи WM ASF настройте его с помощью методов Иконфигасфвритер, если профиль по умолчанию не подходит, и подключите входные ПИН-коды модуля записи WM ASF к соответствующим выходным контактам в вышестоящем фильтре.</span><span class="sxs-lookup"><span data-stu-id="9845e-112">After adding the WM ASF Writer, configure it by using the IConfigAsfWriter methods if the default profile is not suitable, and connect the WM ASF Writer input pins to the corresponding output pins on the upstream filters.</span></span>

<span data-ttu-id="9845e-113">На следующем рисунке показана типичная конфигурация графа фильтра модуля записи WM ASF.</span><span class="sxs-lookup"><span data-stu-id="9845e-113">The following illustration shows typical WM ASF Writer transcoding filter graph configurations.</span></span>

![граф фильтра перекодирования](images/asf-transcode.png)

<span data-ttu-id="9845e-115">Вставка собственных форматов потока в файлы ASF</span><span class="sxs-lookup"><span data-stu-id="9845e-115">Inserting Native Stream Formats Into ASF Files</span></span>

<span data-ttu-id="9845e-116">По умолчанию фильтр модуля записи WM ASF ждет несжатые аудио-и видеопотоки на входных ПИН-кодах и использует видеокодеки Windows Media Audio и Windows Media для сжатия потоков.</span><span class="sxs-lookup"><span data-stu-id="9845e-116">By default, the WM ASF Writer filter expects uncompressed audio and video streams on its input pins, and uses the Windows Media Audio and Windows Media Video codecs to compress the streams.</span></span> <span data-ttu-id="9845e-117">Однако контейнер файлов ASF можно использовать для любого типа данных.</span><span class="sxs-lookup"><span data-stu-id="9845e-117">However, the ASF file container can be used for any type of data.</span></span> <span data-ttu-id="9845e-118">Помещая цифровые мультимедийные данные в контейнер файлов ASF, можно добавлять функции, предоставляемые ASF, такие как метаданные и управление цифровыми правами (DRM), без необходимости перекодирования содержимого.</span><span class="sxs-lookup"><span data-stu-id="9845e-118">By placing digital media data into an ASF file container, you can add features provided by ASF, such as metadata and digital rights management (DRM), without having to transcode your content.</span></span>

<span data-ttu-id="9845e-119">Чтобы создать ASF-файл, содержащий содержимое, не основанное на Windows Media, приложение должно сжать поток в графе фильтра в потоке данных WM ASF и обойти механизм сжатия модуля записи WM ASF, вызвав [**IConfigAsfWriter2:: сетпарам**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter2-setparam) следующим образом:</span><span class="sxs-lookup"><span data-stu-id="9845e-119">To create an ASF file that contains content that is not Windows Media–based, the application must compress the stream in the filter graph upstream of the WM ASF Writer and bypass the WM ASF Writer's compression mechanism by calling [**IConfigAsfWriter2::SetParam**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter2-setparam) as follows:</span></span>


```C++
pConfigAsfWriter2->SetParam(AM_CONFIGASFWRITER_PARAM_DONTCOMPRESS,TRUE,0)
```



<span data-ttu-id="9845e-120">Затем настройте фильтр с нужным профилем.</span><span class="sxs-lookup"><span data-stu-id="9845e-120">Then configure the filter with the desired profile.</span></span> <span data-ttu-id="9845e-121">Очень важно, чтобы тип носителя входного потока точно совпадал с форматом в профиле.</span><span class="sxs-lookup"><span data-stu-id="9845e-121">It is essential that the media type of the input stream exactly matches the format in the profile.</span></span> <span data-ttu-id="9845e-122">В некоторых случаях может потребоваться проверить формат входного потока и создать настраиваемый профиль для его сопоставления.</span><span class="sxs-lookup"><span data-stu-id="9845e-122">In some cases, it may be necessary to examine the input stream's format, and create a custom profile to match it.</span></span>

<span data-ttu-id="9845e-123">При подключении модуля записи WM ASF к вышестоящему фильтру используйте метод Играфбуилдер:: Коннектдирект.</span><span class="sxs-lookup"><span data-stu-id="9845e-123">When you connect the WM ASF Writer to the upstream filter, use the IGraphBuilder::ConnectDirect method.</span></span> <span data-ttu-id="9845e-124">Не используйте методы Intelligent Connect, такие как Играфбуилдер:: Connect или Играфбуилдер:: RenderFile, для подключения фильтра, так как это приведет к отключению режима "обходного сжатия" фильтра.</span><span class="sxs-lookup"><span data-stu-id="9845e-124">Do not use any "intelligent connect" methods such as IGraphBuilder::Connect or IGraphBuilder::RenderFile to connect the filter because this will disable the filter's "bypass compression" mode.</span></span>

<span data-ttu-id="9845e-125">Запись непосредственно с устройства в ASF-файл</span><span class="sxs-lookup"><span data-stu-id="9845e-125">Capturing Directly from a Device to an ASF File</span></span>

<span data-ttu-id="9845e-126">При записи аудио или видео непосредственно в файл ASF граф фильтра будет выглядеть примерно так, как показано ниже, в зависимости от типа используемого устройства записи.</span><span class="sxs-lookup"><span data-stu-id="9845e-126">When capturing audio or video directly to an ASF file, the filter graph will look similar to the following, depending on the type of capture device being used.</span></span>

![граф захвата видео Windows Media](images/asf-webcam.png)

<span data-ttu-id="9845e-128">Дополнительные сведения о создании графов видеороликов и видеозаписей см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="9845e-128">For more information about creating video and audio capture graphs, see the following topics:</span></span>

-   [<span data-ttu-id="9845e-129">Запись звука</span><span class="sxs-lookup"><span data-stu-id="9845e-129">Audio Capture</span></span>](audio-capture.md)
-   [<span data-ttu-id="9845e-130">Видеозапись</span><span class="sxs-lookup"><span data-stu-id="9845e-130">Video Capture</span></span>](video-capture.md)

<span data-ttu-id="9845e-131">Модуль записи WM ASF не будет работать, пока не будут подключены все его ПИН-коды.</span><span class="sxs-lookup"><span data-stu-id="9845e-131">The WM ASF Writer will not run unless all of its pins are connected.</span></span> <span data-ttu-id="9845e-132">Если настроить модуль записи WM ASF с помощью системного профиля по умолчанию (не рекомендуется) или любого профиля с аудио-и видеопотоками, то он создаст входной ПИН-код для каждого потока, и каждый из этих контактов должен быть подключен.</span><span class="sxs-lookup"><span data-stu-id="9845e-132">If you configure the WM ASF Writer with the default system profile (not recommended), or any profile with audio and video streams, then it will create an input pin for each stream and each of those pins must be connected.</span></span> <span data-ttu-id="9845e-133">Если вы не собираетесь записывать звук, например, не забудьте настроить фильтр с помощью профиля только для видео, чтобы не создавался звуковой ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="9845e-133">If you do not intend to capture audio, for example, then be sure to configure the filter with a video-only profile so that no audio pin is created.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9845e-134">См. также</span><span class="sxs-lookup"><span data-stu-id="9845e-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9845e-135">Создание файлов ASF в DirectShow</span><span class="sxs-lookup"><span data-stu-id="9845e-135">Creating ASF Files in DirectShow</span></span>](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 



