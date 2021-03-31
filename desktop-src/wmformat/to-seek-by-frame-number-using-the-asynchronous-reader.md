---
title: Поиск по номеру кадра с помощью асинхронного модуля чтения
description: Поиск по номеру кадра с помощью асинхронного модуля чтения
ms.assetid: faab6344-3afc-47ff-9107-d2ce36c0a2b8
keywords:
- Расширенный формат систем (ASF), поиск по номерам кадров
- ASF (Расширенный системный формат), поиск по номерам кадров
- Расширенный системный формат (ASF), асинхронный читатель
- ASF (Расширенный системный формат), асинхронный читатель
- асинхронные читатели, поиск по номерам кадров
- видеопотокы, поиск по номерам кадров
- потоки видео, асинхронные читатели
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 169f5e1ac1e6034bc1db6f610e80af50dd3a0215
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104069551"
---
# <a name="to-seek-by-frame-number-using-the-asynchronous-reader"></a><span data-ttu-id="a9a89-110">Поиск по номеру кадра с помощью асинхронного модуля чтения</span><span class="sxs-lookup"><span data-stu-id="a9a89-110">To Seek By Frame Number Using the Asynchronous Reader</span></span>

<span data-ttu-id="a9a89-111">Объект асинхронного модуля чтения можно использовать для поиска номеров кадров видеопотоков в файле ASF.</span><span class="sxs-lookup"><span data-stu-id="a9a89-111">The asynchronous reader object can be used to seek to the frame numbers of video streams in an ASF file.</span></span> <span data-ttu-id="a9a89-112">Чтобы использовать поиск на основе кадров, файл, загруженный в модуль чтения, должен индексироваться по кадрам.</span><span class="sxs-lookup"><span data-stu-id="a9a89-112">To use frame-based seeking, the file loaded in the reader must be indexed by frame.</span></span> <span data-ttu-id="a9a89-113">Каждый отдельный поток видео может быть проиндексирован.</span><span class="sxs-lookup"><span data-stu-id="a9a89-113">Each individual video stream can be indexed.</span></span> <span data-ttu-id="a9a89-114">Чтобы определить, проиндексирован ли поток по кадру, можно проверить \_ атрибут g всзвмнумбероффрамес в заголовке файла, вызвав [**ивмхеадеринфо:: жетаттрибутебинаме**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname).</span><span class="sxs-lookup"><span data-stu-id="a9a89-114">To determine whether a stream has been indexed by frame, you can check the g\_wszWMNumberOfFrames attribute in the header of the file by calling [**IWMHeaderInfo::GetAttributeByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname).</span></span>

<span data-ttu-id="a9a89-115">Чтобы найти данные в файле ASF по номеру кадра с помощью асинхронного модуля чтения, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a9a89-115">To seek data in an ASF file by frame number using the asynchronous reader, perform the following steps.</span></span>

1.  <span data-ttu-id="a9a89-116">Получите указатель на интерфейс [**IWMReaderAdvanced3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3) объекта Reader, вызвав **Ивмреадер:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="a9a89-116">Obtain a pointer to the [**IWMReaderAdvanced3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3) interface of the reader object by calling **IWMReader::QueryInterface**.</span></span>
2.  <span data-ttu-id="a9a89-117">Задайте начальный номер кадра и длительность, вызвав [**IWMReaderAdvanced3:: стартатпоситион**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced3-startatposition).</span><span class="sxs-lookup"><span data-stu-id="a9a89-117">Set the starting frame number and duration by calling [**IWMReaderAdvanced3::StartAtPosition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced3-startatposition).</span></span> <span data-ttu-id="a9a89-118">Необходимо указать номер потока для видеопотока с индексированием кадров.</span><span class="sxs-lookup"><span data-stu-id="a9a89-118">You must specify the stream number of a frame-indexed video stream.</span></span> <span data-ttu-id="a9a89-119">Модуль чтения синхронизирует остальные выходные данные с временем представления указанного кадра указанного потока и начинает доставку выходных данных.</span><span class="sxs-lookup"><span data-stu-id="a9a89-119">The reader will synchronize the rest of the outputs to the presentation time of the specified frame of the specified stream and begin delivering output samples.</span></span>
3.  <span data-ttu-id="a9a89-120">Обработайте примеры, как обычно в реализации метода **ивмреадеркаллбакк:: OnSample** .</span><span class="sxs-lookup"><span data-stu-id="a9a89-120">Handle the samples as you normally would in your implementation of the **IWMReaderCallback::OnSample** method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a9a89-121">См. также</span><span class="sxs-lookup"><span data-stu-id="a9a89-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9a89-122">**Чтение файлов с помощью асинхронного модуля чтения**</span><span class="sxs-lookup"><span data-stu-id="a9a89-122">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="a9a89-123">**Считывание метаданных при воспроизведении**</span><span class="sxs-lookup"><span data-stu-id="a9a89-123">**Reading Metadata at Playback**</span></span>](reading-metadata-at-playback.md)
</dt> <dt>

[<span data-ttu-id="a9a89-124">**Работа с индексами**</span><span class="sxs-lookup"><span data-stu-id="a9a89-124">**Working with Indexes**</span></span>](working-with-indexes.md)
</dt> </dl>

 

 




