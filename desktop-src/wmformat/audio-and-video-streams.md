---
title: Потоки аудио и видео
description: Потоки аудио и видео
ms.assetid: 809e5bb6-2bc4-4022-9117-a2be5418d7d1
keywords:
- Windows Media Format SDK, звуковые потоки
- Расширенный формат систем (ASF), звуковые потоки
- ASF (Расширенный системный формат), звуковые потоки
- Windows Media Format SDK, потоки видео
- Расширенный системный формат (ASF), видеопотоки
- ASF (Расширенный системный формат), видеопотоки
- Windows Media Format SDK, потоки
- Расширенный системный формат (ASF), потоки
- ASF (Расширенный системный формат), потоки
- звуковые потоки, сведения
- видеопотоки, сведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d72eb46a6fb19129da2b9a841eab1710da47013
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067905"
---
# <a name="audio-and-video-streams"></a><span data-ttu-id="6fa55-114">Потоки аудио и видео</span><span class="sxs-lookup"><span data-stu-id="6fa55-114">Audio and Video Streams</span></span>

<span data-ttu-id="6fa55-115">Наиболее распространенными типами потоков, используемых в файлах, созданных с помощью пакета SDK для Windows Media Format, являются потоки аудио и видео.</span><span class="sxs-lookup"><span data-stu-id="6fa55-115">The most common types of streams used in files created by using the Windows Media Format SDK are audio and video streams.</span></span> <span data-ttu-id="6fa55-116">Цифровые представления данных аудио и видео являются сложными и занимают большой объем памяти.</span><span class="sxs-lookup"><span data-stu-id="6fa55-116">Digital representations of audio and video data are complex and take up large amounts of memory.</span></span> <span data-ttu-id="6fa55-117">В большинстве случаев перед добавлением в файл ASF аудио и видео сжимаются.</span><span class="sxs-lookup"><span data-stu-id="6fa55-117">Under most circumstances, both audio and video are compressed before being added to an ASF file.</span></span> <span data-ttu-id="6fa55-118">Сжатие выполняется с помощью программы сжатия и распаковки (кодек).</span><span class="sxs-lookup"><span data-stu-id="6fa55-118">Compression is accomplished using a compressor/decompressor (codec).</span></span>

<span data-ttu-id="6fa55-119">В этот пакет SDK входит несколько кодеков Windows Media, которые обеспечивают качественное сжатие цифровых носителей.</span><span class="sxs-lookup"><span data-stu-id="6fa55-119">Several Windows Media codecs are included with this SDK, and they provide excellent quality compression for digital media.</span></span> <span data-ttu-id="6fa55-120">Дополнительные сведения о кодеках Windows Media см. в разделе [функции кодека](codec-features.md).</span><span class="sxs-lookup"><span data-stu-id="6fa55-120">For more information about the Windows Media codecs, see [Codec Features](codec-features.md).</span></span> <span data-ttu-id="6fa55-121">Многие другие кодеки доступны из различных источников.</span><span class="sxs-lookup"><span data-stu-id="6fa55-121">Many other codecs are available from various sources.</span></span> <span data-ttu-id="6fa55-122">При создании файлов ASF можно использовать любые кодеки, но объекты этого пакета SDK напрямую поддерживают только кодеки Windows Media.</span><span class="sxs-lookup"><span data-stu-id="6fa55-122">You can use whatever codecs you like when creating ASF files, but only the Windows Media codecs are directly supported by the objects of this SDK.</span></span> <span data-ttu-id="6fa55-123">Чтобы использовать другие кодеки, необходимо сжать образцы и передать их в объект модуля записи в качестве произвольных данных.</span><span class="sxs-lookup"><span data-stu-id="6fa55-123">To use other codecs, you must compress samples and pass them to the writer object as arbitrary data.</span></span>

<span data-ttu-id="6fa55-124">Самым важным различием между потоками аудио и видео и произвольными потоками является то, что потоки, содержащие аудио-или видеоданные Windows Media, проверяются объектами пакета SDK Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="6fa55-124">The most important distinction between audio or video streams and arbitrary streams is that streams containing Windows Media audio or video data are validated by the objects of the Windows Media Format SDK.</span></span> <span data-ttu-id="6fa55-125">Произвольные потоки данных не проверяются автоматически и должны проверяться на целостность приложения.</span><span class="sxs-lookup"><span data-stu-id="6fa55-125">Arbitrary data streams are not validated automatically, and should be checked for integrity by your application.</span></span>

<span data-ttu-id="6fa55-126">Свойства потока аудио или видео описаны в профиле, используемом для создания файла.</span><span class="sxs-lookup"><span data-stu-id="6fa55-126">The properties of an audio or video stream are described in the profile used to create the file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6fa55-127">См. также</span><span class="sxs-lookup"><span data-stu-id="6fa55-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6fa55-128">**Произвольные потоки**</span><span class="sxs-lookup"><span data-stu-id="6fa55-128">**Arbitrary Streams**</span></span>](arbitrary-streams.md)
</dt> <dt>

[<span data-ttu-id="6fa55-129">**Функции файлов ASF**</span><span class="sxs-lookup"><span data-stu-id="6fa55-129">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="6fa55-130">**Работа с профилями**</span><span class="sxs-lookup"><span data-stu-id="6fa55-130">**Working with Profiles**</span></span>](working-with-profiles.md)
</dt> </dl>

 

 




