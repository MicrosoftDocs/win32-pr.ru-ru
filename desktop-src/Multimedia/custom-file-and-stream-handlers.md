---
title: Пользовательские обработчики файлов и потоков
description: Пользовательские обработчики файлов и потоков
ms.assetid: c61e0118-d405-4c1e-9ae8-ed6a145a5d6b
keywords:
- Видео для Windows (VFW), пользовательские обработчики файлов
- Видео для Windows (VFW), пользовательские обработчики потока
- Видео для Windows (VFW), обработчики файлов
- Видео для Windows (VFW), обработчики потоков
- VFW (видео для Windows), пользовательские обработчики файлов
- VFW (видео для Windows), обработчики пользовательских потоков
- VFW (видео для Windows), обработчики файлов
- VFW (видео для Windows), обработчики потоков
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f991ac3197eb6d2f23fcd20d0d14e5f7c65e48de
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486869"
---
# <a name="custom-file-and-stream-handlers"></a><span data-ttu-id="cf967-111">Пользовательские обработчики файлов и потоков</span><span class="sxs-lookup"><span data-stu-id="cf967-111">Custom File and Stream Handlers</span></span>

<span data-ttu-id="cf967-112">Обработчики файлов и потоков — это драйверы, которые предоставляют последовательные интерфейсы для приложения, управляющего данными мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="cf967-112">File and stream handlers are drivers that provide consistent interfaces to an application that controls multimedia data.</span></span> <span data-ttu-id="cf967-113">Обработчики файлов и потоков, входящие в операционную систему, используют аудио-и звуковые данные, хранящиеся в файлах AVI и Audio-Video.</span><span class="sxs-lookup"><span data-stu-id="cf967-113">The file and stream handlers included in the operating system use video and waveform-audio data stored in audio-video interleaved (AVI) and waveform-audio files.</span></span>

<span data-ttu-id="cf967-114">Можно написать обработчики, позволяющие приложению записывать или получать доступ к данным мультимедиа из другого источника, например из файла, использующего собственный формат, AVI-файл, который был расширен и содержит дополнительные потоки данных, или обработчик, создающий собственные мультимедийные данные.</span><span class="sxs-lookup"><span data-stu-id="cf967-114">You can write handlers to allow your application to write or access multimedia data from another source, such as a file using a proprietary format, an AVI file that has been expanded to contain additional data streams, or a handler that generates its own multimedia data.</span></span> <span data-ttu-id="cf967-115">Если у вас есть пользовательский формат для данных AVI, которые вы хотите использовать с [функциями и макросами авифиле](avifile-functions-and-macros.md), необходимо написать пользовательский обработчик.</span><span class="sxs-lookup"><span data-stu-id="cf967-115">If you have a custom file format for AVI data that you would like to use with the [AVIFile Functions and Macros](avifile-functions-and-macros.md), you need to write a custom handler.</span></span>

-   [<span data-ttu-id="cf967-116">О пользовательских обработчиках файлов и потоков</span><span class="sxs-lookup"><span data-stu-id="cf967-116">About Custom File and Stream Handlers</span></span>](about-custom-file-and-stream-handlers.md)
-   [<span data-ttu-id="cf967-117">Использование пользовательских обработчиков файлов и потоков</span><span class="sxs-lookup"><span data-stu-id="cf967-117">Using Custom File and Stream Handlers</span></span>](using-custom-file-and-stream-handlers.md)
-   [<span data-ttu-id="cf967-118">Справочник по пользовательскому файлу и обработчику потока</span><span class="sxs-lookup"><span data-stu-id="cf967-118">Custom File and Stream Handler Reference</span></span>](custom-file-and-stream-handler-reference.md)

 

 




