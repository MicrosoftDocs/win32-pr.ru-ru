---
title: Потоки изображений
description: Потоки изображений
ms.assetid: 17a945aa-463a-4aac-82cc-68b49c720c0a
keywords:
- Windows Media Format SDK, потоки изображений
- Расширенный системный формат (ASF), потоки изображений
- ASF (Расширенный системный формат), потоки изображений
- Windows Media Format SDK, потоки
- Расширенный системный формат (ASF), потоки
- ASF (Расширенный системный формат), потоки
- потоки изображений, о
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 280d029715a3c722d05ee335a3a88ae4632cabbb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331608"
---
# <a name="image-streams"></a><span data-ttu-id="55bbd-110">Потоки изображений</span><span class="sxs-lookup"><span data-stu-id="55bbd-110">Image Streams</span></span>

<span data-ttu-id="55bbd-111">Поток изображений — это специальный тип потока, который содержит изображения, назначенные времени представления.</span><span class="sxs-lookup"><span data-stu-id="55bbd-111">An image stream is a special type of stream that contains still images assigned to presentation times.</span></span> <span data-ttu-id="55bbd-112">Приложение может отображать изображения в потоке изображений по желанию, но Типичная реализация — отображение каждого изображения до тех пор, пока не будет доставлено следующее изображение, например слайд-шоу.</span><span class="sxs-lookup"><span data-stu-id="55bbd-112">An application can display the pictures in an image stream as desired, but the typical implementation is to display each picture until the next picture is delivered, like a slide show.</span></span> <span data-ttu-id="55bbd-113">Как правило, поток изображений кодируется в файл с аудио-потоком для создания простого представления изображений, синхронизированных с музыкой или речью.</span><span class="sxs-lookup"><span data-stu-id="55bbd-113">Usually, an image stream is encoded in a file with an audio stream to produce a simple presentation of images synchronized with music or speech.</span></span>

<span data-ttu-id="55bbd-114">Потоки изображений подобны видеопотокам в том, что они создаются из несжатых образцов, сжатых как часть процесса записи файлов, но они также подобны произвольным потокам, так как необходимо назначить для содержимого скорость потока и окно буфера, не полагаясь на свойства, назначенные кодеком.</span><span class="sxs-lookup"><span data-stu-id="55bbd-114">Image streams are like video streams in that they are created from uncompressed samples that are compressed as part of the file writing process, but they are also like arbitrary streams because you must assign a bit rate and buffer window appropriate to the content without relying on codec-assigned properties.</span></span>

## <a name="related-topics"></a><span data-ttu-id="55bbd-115">См. также</span><span class="sxs-lookup"><span data-stu-id="55bbd-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55bbd-116">**Произвольные потоки**</span><span class="sxs-lookup"><span data-stu-id="55bbd-116">**Arbitrary Streams**</span></span>](arbitrary-streams.md)
</dt> <dt>

[<span data-ttu-id="55bbd-117">**Функции файлов ASF**</span><span class="sxs-lookup"><span data-stu-id="55bbd-117">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="55bbd-118">**Потоки аудио и видео**</span><span class="sxs-lookup"><span data-stu-id="55bbd-118">**Audio and Video Streams**</span></span>](audio-and-video-streams.md)
</dt> <dt>

[<span data-ttu-id="55bbd-119">**Запись потоков изображений**</span><span class="sxs-lookup"><span data-stu-id="55bbd-119">**Writing Image Streams**</span></span>](writing-image-streams.md)
</dt> </dl>

 

 




