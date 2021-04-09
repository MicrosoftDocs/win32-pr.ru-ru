---
title: О пользовательских обработчиках файлов и потоков
description: О пользовательских обработчиках файлов и потоков
ms.assetid: 6a00c8db-3ac6-4826-a373-52b6b7d1652f
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
ms.openlocfilehash: 94e1872aa8a2f5c55df0db43860e318c792801e8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103889152"
---
# <a name="about-custom-file-and-stream-handlers"></a><span data-ttu-id="247de-111">О пользовательских обработчиках файлов и потоков</span><span class="sxs-lookup"><span data-stu-id="247de-111">About Custom File and Stream Handlers</span></span>

<span data-ttu-id="247de-112">Приложение может использовать пользовательский обработчик файлов для чтения из файла или записи в файл в нестандартном формате.</span><span class="sxs-lookup"><span data-stu-id="247de-112">Your application can use a custom file handler to read from a file or write to a file that is in a nonstandard format.</span></span> <span data-ttu-id="247de-113">Для этого приложение просто использует имя обработчика файлов при открытии файла или выделении файлового интерфейса.</span><span class="sxs-lookup"><span data-stu-id="247de-113">To do this, your application simply uses the name of your file handler when opening the file or allocating the file interface.</span></span> <span data-ttu-id="247de-114">Затем библиотека Авифиле использует функции из обработчика файлов, а не из другого обработчика файлов.</span><span class="sxs-lookup"><span data-stu-id="247de-114">The AVIFile library then uses the functions from your file handler instead of those from another file handler.</span></span> <span data-ttu-id="247de-115">Нестандартный формат отображается как стандартные данные AVI для приложения или для любого другого приложения, использующего пользовательский обработчик файлов.</span><span class="sxs-lookup"><span data-stu-id="247de-115">The nonstandard format appears as standard AVI data to your application or to any other application using your custom file handler.</span></span>

<span data-ttu-id="247de-116">Аналогичным образом приложение может использовать пользовательский обработчик потока для чтения потока, находящегося в нестандартном формате.</span><span class="sxs-lookup"><span data-stu-id="247de-116">Similarly, your application can use a custom stream handler to read a stream that is in a nonstandard format.</span></span> <span data-ttu-id="247de-117">Поток — это компонент AVI-файла, будь то звук, видео, MIDI, текст или пользовательские данные.</span><span class="sxs-lookup"><span data-stu-id="247de-117">A stream — whether it constitutes audio, video, MIDI, text, or custom data — is a component of an AVI file.</span></span> <span data-ttu-id="247de-118">Например, AVI-файл, содержащий последовательность видеороликов, на английском языке и на французском проходе, состоит из трех потоков.</span><span class="sxs-lookup"><span data-stu-id="247de-118">For example, an AVI file that contains a video sequence, an English soundtrack, and a French soundtrack consists of three streams.</span></span> <span data-ttu-id="247de-119">Приложение может указать потоки в файле AVI для обработки и направить каждый из этих потоков в обработчик, который может оптимизировать обработку соответствующего типа мультимедийных данных.</span><span class="sxs-lookup"><span data-stu-id="247de-119">Your application can specify the streams in an AVI file to process and direct each of those streams to a handler that can optimally process the appropriate type of multimedia data.</span></span>

> [!Note]  
> <span data-ttu-id="247de-120">Пользовательские обработчики потоков и файлов необходимо размещать в одной или нескольких библиотеках DLL, отделенных от основных файлов приложения.</span><span class="sxs-lookup"><span data-stu-id="247de-120">You must place custom stream and file handlers in one or more DLLs, separated from main application files.</span></span>

 

 

 




