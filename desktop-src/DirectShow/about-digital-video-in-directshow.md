---
description: О цифровом видео в DirectShow
ms.assetid: 0570bf7c-c38d-4ada-9593-27b9be117893
title: О цифровом видео в DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8f4ae0253754583bb89132289db87f0aad673d6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104559822"
---
# <a name="about-digital-video-in-directshow"></a><span data-ttu-id="0a4a3-103">О цифровом видео в DirectShow</span><span class="sxs-lookup"><span data-stu-id="0a4a3-103">About Digital Video in DirectShow</span></span>

<span data-ttu-id="0a4a3-104">Цифровое видео (DV) может быть записано с цифровой камеры, храниться в файле на компьютере пользователя или храниться на ленте с помощью записывающего видеомагнитофона (Втр).</span><span class="sxs-lookup"><span data-stu-id="0a4a3-104">Digital video (DV) can be captured from a DV camera, stored in a file on the user's computer, or stored on tape using a video tape recorder (VTR).</span></span> <span data-ttu-id="0a4a3-105">Таким образом, операции, которые приложение может выполнять в потоке DV, включают:</span><span class="sxs-lookup"><span data-stu-id="0a4a3-105">Thus, the operations that an application might perform on a DV stream include:</span></span>

-   <span data-ttu-id="0a4a3-106">Запись динамического видео с цифровой камеры.</span><span class="sxs-lookup"><span data-stu-id="0a4a3-106">Capture live video from a DV camera.</span></span>
-   <span data-ttu-id="0a4a3-107">Передача DV данных с ленты Втр на компьютер.</span><span class="sxs-lookup"><span data-stu-id="0a4a3-107">Transmit DV data from VTR tape to the computer.</span></span>
-   <span data-ttu-id="0a4a3-108">Передача DV данных с компьютера в Втр.</span><span class="sxs-lookup"><span data-stu-id="0a4a3-108">Transmit DV data from the computer to the VTR.</span></span>
-   <span data-ttu-id="0a4a3-109">Считывание DV-данных из файла.</span><span class="sxs-lookup"><span data-stu-id="0a4a3-109">Read DV data from a file.</span></span>
-   <span data-ttu-id="0a4a3-110">Запись DV-данных в файл.</span><span class="sxs-lookup"><span data-stu-id="0a4a3-110">Write DV data to a file.</span></span>
-   <span data-ttu-id="0a4a3-111">Отображение аудио и видео в DV-потоке.</span><span class="sxs-lookup"><span data-stu-id="0a4a3-111">Render the audio and video in a DV stream.</span></span>

<span data-ttu-id="0a4a3-112">DirectShow предоставляет следующие видеофильтры:</span><span class="sxs-lookup"><span data-stu-id="0a4a3-112">DirectShow provides the following DV filters:</span></span>

-   <span data-ttu-id="0a4a3-113">[Драйвер мсдв](msdv-driver.md).</span><span class="sxs-lookup"><span data-stu-id="0a4a3-113">[MSDV Driver](msdv-driver.md).</span></span> <span data-ttu-id="0a4a3-114">Драйвер МСДВ управляет DV-устройством, таким как видеокамера.</span><span class="sxs-lookup"><span data-stu-id="0a4a3-114">The MSDV driver controls a DV device, such as a camcorder.</span></span> <span data-ttu-id="0a4a3-115">Устройство может иметь подединицу камеры и подединицу Втр. МСДВ управляет обеими подразделениями.</span><span class="sxs-lookup"><span data-stu-id="0a4a3-115">The device may have a camera subunit and a VTR subunit; MSDV controls both subunits.</span></span> <span data-ttu-id="0a4a3-116">Драйвер МСДВ отображается как фильтр DirectShow для приложений.</span><span class="sxs-lookup"><span data-stu-id="0a4a3-116">The MSDV driver appears to applications as a DirectShow filter.</span></span>
-   <span data-ttu-id="0a4a3-117">Фильтр [разделителя DV](dv-splitter-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="0a4a3-117">[DV Splitter](dv-splitter-filter.md) filter.</span></span> <span data-ttu-id="0a4a3-118">Кадры DV содержат аудио и видео в одном кадре.</span><span class="sxs-lookup"><span data-stu-id="0a4a3-118">DV frames contain audio and video in the same frame.</span></span> <span data-ttu-id="0a4a3-119">Фильтр разделителя DV извлекает звуковые данные и выводит их в виде одного или двух звуковых потоков.</span><span class="sxs-lookup"><span data-stu-id="0a4a3-119">The DV Splitter filter extracts the audio data and outputs it as one or two audio streams.</span></span> <span data-ttu-id="0a4a3-120">Он выводит исходные данные в виде отдельного видеопотока DV.</span><span class="sxs-lookup"><span data-stu-id="0a4a3-120">It outputs the original data as a separate DV video stream.</span></span>
-   <span data-ttu-id="0a4a3-121">Фильтр [видеодекодера DV](dv-video-decoder-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="0a4a3-121">[DV Video Decoder](dv-video-decoder-filter.md) filter.</span></span> <span data-ttu-id="0a4a3-122">Декодирует видео в несжатом видео.</span><span class="sxs-lookup"><span data-stu-id="0a4a3-122">Decodes DV video into uncompressed video.</span></span>
-   <span data-ttu-id="0a4a3-123">Фильтр [Видеокодировщика DV](dv-video-encoder-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="0a4a3-123">[DV Video Encoder](dv-video-encoder-filter.md) filter.</span></span> <span data-ttu-id="0a4a3-124">Кодирует несжатое видео в видео в кодировке DV.</span><span class="sxs-lookup"><span data-stu-id="0a4a3-124">Encodes uncompressed video to DV-encoded video.</span></span>
-   <span data-ttu-id="0a4a3-125">[DV мультиплексор](dv-muxer-filter.md).</span><span class="sxs-lookup"><span data-stu-id="0a4a3-125">[DV Muxer](dv-muxer-filter.md).</span></span> <span data-ttu-id="0a4a3-126">Объединяет видеопоток DV с одним или двумя звуковыми потоками, чтобы создать одиночный DV-поток с чередованием.</span><span class="sxs-lookup"><span data-stu-id="0a4a3-126">Combines a DV video stream with one or two audio streams, to create a single interleaved DV stream.</span></span>

<span data-ttu-id="0a4a3-127">Видеодекодеры и видеоадаптеры DV работают вместе.</span><span class="sxs-lookup"><span data-stu-id="0a4a3-127">The DV Splitter and DV Video Decoder work together.</span></span> <span data-ttu-id="0a4a3-128">Разделитель принимает поток с чередованием и выводит отдельные потоки аудио и видео.</span><span class="sxs-lookup"><span data-stu-id="0a4a3-128">The splitter takes the interleaved stream and outputs separate audio and DV video streams.</span></span> <span data-ttu-id="0a4a3-129">Декодер преобразует DV Video в несжатое видео.</span><span class="sxs-lookup"><span data-stu-id="0a4a3-129">The decoder converts the DV video to uncompressed video.</span></span> <span data-ttu-id="0a4a3-130">Этот процесс показан на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="0a4a3-130">The following image illustrates this process.</span></span>

![цифровой видеоразделитель и декодер DV](images/dv-filters1.png)

<span data-ttu-id="0a4a3-132">Видеокодировщик DV и DV мультиплексор отменяют процесс: кодировщик преобразует несжатое видео в DV видео, а мультиплексор сочетает аудио и видеовидео для создания одного потока с чередованием, как показано на следующей схеме.</span><span class="sxs-lookup"><span data-stu-id="0a4a3-132">The DV Video Encoder and the DV Muxer reverse the process: The encoder converts uncompressed video to DV video, and the mux combines audio and DV video to create a single interleaved stream, as shown in the following diagram.</span></span>

![DV Encoder и DV мультиплексор](images/dv-filters2.png)

## <a name="related-topics"></a><span data-ttu-id="0a4a3-134">См. также</span><span class="sxs-lookup"><span data-stu-id="0a4a3-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a4a3-135">Цифровое видео в DirectShow</span><span class="sxs-lookup"><span data-stu-id="0a4a3-135">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 



