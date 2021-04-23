---
title: Подготовка содержимого
description: Подготовка содержимого
ms.assetid: 9a3baa33-dac4-4742-8f80-33b05caada09
keywords:
- Пакет SDK для Windows Media Format, подготовка содержимого
- Расширенный системный формат (ASF), Отрисовка содержимого
- ASF (Расширенный системный формат), Отрисовка содержимого
- Расширенный системный формат (ASF), Отрисовка содержимого
- ASF (Расширенный системный формат), Отрисовка содержимого
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d6a171ce9b404c4cc16862ffd64b53ada5821b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103889084"
---
# <a name="rendering-content"></a><span data-ttu-id="5ed90-108">Подготовка содержимого</span><span class="sxs-lookup"><span data-stu-id="5ed90-108">Rendering Content</span></span>

<span data-ttu-id="5ed90-109">Пакет SDK для формата Windows Media не предоставляет никаких подпрограмм для отрисовки содержимого, доставляемого объектом Reader.</span><span class="sxs-lookup"><span data-stu-id="5ed90-109">The Windows Media Format SDK does not provide any routines for rendering content delivered by the reader object.</span></span> <span data-ttu-id="5ed90-110">При написании приложений для воспроизведения содержимого в файлах ASF необходимо реализовать собственные подпрограммы подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="5ed90-110">If you write applications to play back the content in ASF files, you must implement your own rendering routines.</span></span>

<span data-ttu-id="5ed90-111">Необходимо соблюдать осторожность при отрисовке содержимого, чтобы убедиться в том, что образцы подготавливаются к просмотру в порядке времени презентации, и что выборки из разных потоков синхронизируются при подготовке к просмотру.</span><span class="sxs-lookup"><span data-stu-id="5ed90-111">You must be careful when rendering content to ensure that samples are rendered in order of presentation time and that samples from different streams are synchronized when rendering.</span></span> <span data-ttu-id="5ed90-112">Метод, используемый для синхронизации потоков, будет зависеть от метода подготовки к просмотру, используемого для приложения.</span><span class="sxs-lookup"><span data-stu-id="5ed90-112">The method you employ to ensure stream synchronization will depend upon the rendering technique you use for your application.</span></span> <span data-ttu-id="5ed90-113">Как правило, при наличии потоков аудио и видео следует выполнить синхронизацию с аудио-потоком, так как несогласованность в звуковом потоке более заметна, чем несколько удаленных кадров в потоке видео.</span><span class="sxs-lookup"><span data-stu-id="5ed90-113">In general, if you have audio and video streams, you should synchronize to the audio stream, because inconsistency in the audio stream is more noticeable than a few dropped frames in a video stream.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5ed90-114">См. также</span><span class="sxs-lookup"><span data-stu-id="5ed90-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ed90-115">**Чтение файлов ASF**</span><span class="sxs-lookup"><span data-stu-id="5ed90-115">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> <dt>

[<span data-ttu-id="5ed90-116">**Получение примеров мультимедиа с помощью асинхронного модуля чтения**</span><span class="sxs-lookup"><span data-stu-id="5ed90-116">**To Retrieve Media Samples with the Asynchronous Reader**</span></span>](to-retrieve-media-samples-with-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="5ed90-117">**Получение примеров мультимедиа с помощью синхронного модуля чтения**</span><span class="sxs-lookup"><span data-stu-id="5ed90-117">**To Retrieve Media Samples with the Synchronous Reader**</span></span>](to-retrieve-media-samples-with-the-synchronous-reader.md)
</dt> </dl>

 

 




