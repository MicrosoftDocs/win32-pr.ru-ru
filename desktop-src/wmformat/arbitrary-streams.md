---
title: Произвольные потоки
description: Произвольные потоки
ms.assetid: 81fd3b07-7cf2-4013-97ed-9718142ca4c3
keywords:
- Windows Media Format SDK, произвольные потоки
- Расширенный системный формат (ASF), произвольные потоки
- ASF (Расширенный системный формат), произвольные потоки
- Windows Media Format SDK, потоки
- Расширенный системный формат (ASF), потоки
- ASF (Расширенный системный формат), потоки
- произвольные потоки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe28a3b30e0f711c69998b78c81fc1e745fe6360
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773406"
---
# <a name="arbitrary-streams"></a><span data-ttu-id="cc406-110">Произвольные потоки</span><span class="sxs-lookup"><span data-stu-id="cc406-110">Arbitrary Streams</span></span>

<span data-ttu-id="cc406-111">В дополнение к потокам аудио и видео и потокам изображений ASF-файл может размещать потоки, содержащие разнообразные данные.</span><span class="sxs-lookup"><span data-stu-id="cc406-111">In addition to audio and video streams and image streams, an ASF file can accommodate streams containing a variety of data.</span></span> <span data-ttu-id="cc406-112">Объекты пакета SDK Windows Media Format обеспечивают поддержку потоков сценариев, потоков передачи файлов, веб-потоков и произвольных потоков данных.</span><span class="sxs-lookup"><span data-stu-id="cc406-112">The objects of the Windows Media Format SDK provide support for script streams, file transfer streams, Web streams, and arbitrary data streams.</span></span> <span data-ttu-id="cc406-113">Все эти типы потоков являются произвольными, то есть проверка данных объектом Read не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cc406-113">All of these stream types are arbitrary, meaning that no data validation is performed by the reading object.</span></span> <span data-ttu-id="cc406-114">При включении в файлы потоков этих типов убедитесь, что приложение для чтения выполняет проверку или проверку данных, чтобы убедиться, что содержимое не повреждено или преднамеренно искажено вредоносной сторонней стороной.</span><span class="sxs-lookup"><span data-stu-id="cc406-114">When you include streams of these types in your files, be sure that the reading application performs validation or data checking to ensure that your content has not been corrupted or intentionally mangled by a malicious third party.</span></span>

<span data-ttu-id="cc406-115">Несмотря на то, что объекты этого пакета SDK не проверяют или не проверяют данные в произвольных потоках, изначально поддерживается несколько типов произвольных потоков.</span><span class="sxs-lookup"><span data-stu-id="cc406-115">Although the objects of this SDK do not verify or validate data in arbitrary streams, several types of arbitrary streams are natively supported.</span></span> <span data-ttu-id="cc406-116">В следующей таблице перечислены предопределенные произвольные типы потоков.</span><span class="sxs-lookup"><span data-stu-id="cc406-116">The following table lists the predefined arbitrary stream types.</span></span> <span data-ttu-id="cc406-117">Также поддерживаются потоки скриптов, но они рассматриваются отдельно в разделе [команды сценария](script-commands.md) .</span><span class="sxs-lookup"><span data-stu-id="cc406-117">Script streams are also supported, but are discussed separately in the [Script Commands](script-commands.md) section.</span></span> <span data-ttu-id="cc406-118">Дополнительные сведения о создании пользовательских типов см. в разделе [пользовательские произвольные потоки данных](custom-arbitrary-data-streams.md).</span><span class="sxs-lookup"><span data-stu-id="cc406-118">For more information about creating custom types, see [Custom Arbitrary Data Streams](custom-arbitrary-data-streams.md).</span></span>



| <span data-ttu-id="cc406-119">Произвольный тип</span><span class="sxs-lookup"><span data-stu-id="cc406-119">Arbitrary type</span></span>                   | <span data-ttu-id="cc406-120">Описание</span><span class="sxs-lookup"><span data-stu-id="cc406-120">Description</span></span>                                                       |
|----------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="cc406-121">Текстовые потоки</span><span class="sxs-lookup"><span data-stu-id="cc406-121">Text Streams</span></span>](text-streams.md) | <span data-ttu-id="cc406-122">Содержат текстовые строки.</span><span class="sxs-lookup"><span data-stu-id="cc406-122">Contain text strings.</span></span>                                             |
| [<span data-ttu-id="cc406-123">Файловые потоки</span><span class="sxs-lookup"><span data-stu-id="cc406-123">File Streams</span></span>](file-streams.md) | <span data-ttu-id="cc406-124">Содержит один или несколько файлов данных.</span><span class="sxs-lookup"><span data-stu-id="cc406-124">Contain one or more data files.</span></span>                                   |
| [<span data-ttu-id="cc406-125">Веб-потоки</span><span class="sxs-lookup"><span data-stu-id="cc406-125">Web Streams</span></span>](web-streams.md)   | <span data-ttu-id="cc406-126">Содержат файлы данных, эквивалентные кэшированной версии веб-страниц.</span><span class="sxs-lookup"><span data-stu-id="cc406-126">Contain data files equivalent to the cached version of Web pages.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="cc406-127">См. также</span><span class="sxs-lookup"><span data-stu-id="cc406-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc406-128">**Функции файлов ASF**</span><span class="sxs-lookup"><span data-stu-id="cc406-128">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="cc406-129">**Потоки аудио и видео**</span><span class="sxs-lookup"><span data-stu-id="cc406-129">**Audio and Video Streams**</span></span>](audio-and-video-streams.md)
</dt> <dt>

[<span data-ttu-id="cc406-130">**Настройка произвольных типов потоков**</span><span class="sxs-lookup"><span data-stu-id="cc406-130">**Configuring Arbitrary Stream Types**</span></span>](configuring-arbitrary-stream-types.md)
</dt> </dl>

 

 




