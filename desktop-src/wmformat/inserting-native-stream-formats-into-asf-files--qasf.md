---
title: Вставка собственных форматов потока в файлы ASF (КАСФ)
description: Вставка собственных форматов потока в файлы ASF (КАСФ)
ms.assetid: ec7a69f3-0d4c-43dd-8d4b-fe066329a98f
keywords:
- Windows Media Format SDK, собственные форматы потока (КАСФ)
- Windows Media Format SDK, Вставка собственных форматов потоков в файлы ASF (КАСФ)
- Пакет SDK для Windows Media Format, DirectShow
- Расширенный системный формат (ASF), Вставка собственных форматов потока (КАСФ)
- ASF (Расширенный системный формат), Вставка собственных форматов потока (КАСФ)
- Расширенный системный формат (ASF), собственные форматы потока (КАСФ)
- ASF (Расширенный системный формат), форматы машинного потока (КАСФ)
- Расширенный системный формат (ASF), DirectShow
- ASF (Расширенный системный формат), DirectShow
- DirectShow, собственные форматы потока (КАСФ)
- DirectShow, Вставка собственных форматов потоков в файлы ASF (КАСФ)
- Windows Media Format SDK, КАСФ
- Расширенный системный формат (ASF), КАСФ
- ASF (Расширенный системный формат), КАСФ
- DirectShow, КАСФ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af4736c450b3620a05fe01dcc1808adc297ebbd1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888928"
---
# <a name="inserting-native-stream-formats-into-asf-files-qasf"></a><span data-ttu-id="7c1a9-118">Вставка собственных форматов потока в файлы ASF (КАСФ)</span><span class="sxs-lookup"><span data-stu-id="7c1a9-118">Inserting Native Stream Formats Into ASF Files (QASF)</span></span>

<span data-ttu-id="7c1a9-119">По умолчанию [средство записи WM ASF](wm-asf-writer-filter.md) ждет несжатые аудио-и видеопотоки на входных ПИН-кодах и использует пакет SDK Windows Media Format для доступа к кодекам Windows Media Audio и Windows Media Video, которые сжимают потоки.</span><span class="sxs-lookup"><span data-stu-id="7c1a9-119">By default, the [WM ASF Writer](wm-asf-writer-filter.md) expects uncompressed audio and video streams on its input pins, and uses the Windows Media Format SDK to access the Windows Media Audio and Windows Media Video codecs, which compress the streams.</span></span> <span data-ttu-id="7c1a9-120">Но контейнер файлов ASF можно использовать для любого типа данных.</span><span class="sxs-lookup"><span data-stu-id="7c1a9-120">But the ASF file container can be used for any type of data.</span></span> <span data-ttu-id="7c1a9-121">Помещая цифровые мультимедийные данные в контейнер файлов ASF, можно добавлять функции, предоставляемые ASF, такие как метаданные и управление цифровыми правами (DRM), без необходимости перекодирования содержимого.</span><span class="sxs-lookup"><span data-stu-id="7c1a9-121">By placing digital media data into an ASF file container, you can add features provided by ASF, such as metadata and digital rights management (DRM), without having to transcode your content.</span></span>

<span data-ttu-id="7c1a9-122">Чтобы создать ASF-файл, содержащий содержимое, не основанное на Windows Media, приложение должно сжать поток в графе фильтра в потоке данных WM ASF и обойти механизм сжатия модуля записи WM ASF, вызвав [**IConfigAsfWriter2:: сетпарам**](iconfigasfwriter2-setparam.md) следующим образом:</span><span class="sxs-lookup"><span data-stu-id="7c1a9-122">To create an ASF file that contains content that is not Windows Media–based, the application must compress the stream in the filter graph upstream of the WM ASF Writer and bypass the WM ASF Writer's compression mechanism by calling [**IConfigAsfWriter2::SetParam**](iconfigasfwriter2-setparam.md) as follows:</span></span>


```C++
pConfigAsfWriter2->SetParam(AM_CONFIGASFWRITER_PARAM_DONTCOMPRESS,TRUE,0)

```



<span data-ttu-id="7c1a9-123">Затем настройте фильтр с нужным профилем.</span><span class="sxs-lookup"><span data-stu-id="7c1a9-123">Then configure the filter with the desired profile.</span></span> <span data-ttu-id="7c1a9-124">Очень важно, чтобы тип носителя входного потока точно совпадал с форматом в профиле.</span><span class="sxs-lookup"><span data-stu-id="7c1a9-124">It is essential that the media type of the input stream exactly matches the format in the profile.</span></span> <span data-ttu-id="7c1a9-125">В некоторых случаях может потребоваться проверить формат входного потока и создать настраиваемый профиль для его сопоставления.</span><span class="sxs-lookup"><span data-stu-id="7c1a9-125">In some cases, it may be necessary to examine the input stream's format, and create a custom profile to match it.</span></span> <span data-ttu-id="7c1a9-126">Дополнительные сведения см. [в разделе Создание файлов ASF с помощью сторонних кодеков](to-create-asf-files-using-third-party-codecs.md).</span><span class="sxs-lookup"><span data-stu-id="7c1a9-126">For more information, see [To Create ASF Files Using Third-Party Codecs](to-create-asf-files-using-third-party-codecs.md).</span></span>

<span data-ttu-id="7c1a9-127">При подключении модуля записи WM ASF к вышестоящему фильтру используйте метод **играфбуилдер:: коннектдирект** .</span><span class="sxs-lookup"><span data-stu-id="7c1a9-127">When you connect the WM ASF Writer to the upstream filter, use the **IGraphBuilder::ConnectDirect** method.</span></span> <span data-ttu-id="7c1a9-128">Не используйте методы Intelligent Connect, такие как **играфбуилдер:: Connect** или **Играфбуилдер:: renderFile** , для подключения фильтра, так как это приведет к отключению режима "обходного сжатия" фильтра.</span><span class="sxs-lookup"><span data-stu-id="7c1a9-128">Do not use any "intelligent connect" methods such as **IGraphBuilder::Connect** or **IGraphBuilder::RenderFile** to connect the filter because this will disable the filter's "bypass compression" mode.</span></span>

 

 




