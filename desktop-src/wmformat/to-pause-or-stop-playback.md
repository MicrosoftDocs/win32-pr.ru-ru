---
title: Приостановка и остановка воспроизведения
description: Приостановка и остановка воспроизведения
ms.assetid: 8e43ea80-36c7-4530-8ed3-dfdb64a3a2e3
keywords:
- Расширенный формат систем (ASF), приостановка воспроизведения
- ASF (Расширенный системный формат), приостановка воспроизведения
- Расширенный системный формат (ASF), асинхронный читатель
- ASF (Расширенный системный формат), асинхронный читатель
- Расширенный формат систем (ASF), остановка воспроизведения
- ASF (Расширенный системный формат), остановка воспроизведения
- Расширенный формат систем (ASF), воспроизведение приостанавливается или останавливается
- ASF (Расширенный системный формат), воспроизведение приостановлено или остановлено
- асинхронные модули чтения, приостановка воспроизведения
- асинхронные читатели, остановка воспроизведения
- асинхронный читатель, воспроизведение приостанавливается или останавливается
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 728ce4c58f9198f605764d0f19d0d5f55c7f6c6b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104532981"
---
# <a name="to-pause-or-stop-playback"></a><span data-ttu-id="e9bc3-114">Приостановка и остановка воспроизведения</span><span class="sxs-lookup"><span data-stu-id="e9bc3-114">To Pause or Stop Playback</span></span>

<span data-ttu-id="e9bc3-115">При вызове [**ивмреадер:: Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start) для начала воспроизведения файла асинхронный модуль чтения будет продолжать обработку в собственных отдельных потоках, пока не будет достигнут конец файла.</span><span class="sxs-lookup"><span data-stu-id="e9bc3-115">When you call [**IWMReader::Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start) to begin playing a file, the asynchronous reader will continue processing in its own separate threads until the end of the file is reached.</span></span> <span data-ttu-id="e9bc3-116">Вы можете приостановить или остановить доставку образцов с помощью методов [**ивмреадер::P Аусе**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-pause) или [**Ивмреадер:: Остановите**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-stop) соответственно.</span><span class="sxs-lookup"><span data-stu-id="e9bc3-116">You can pause or stop the delivery of samples using the [**IWMReader::Pause**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-pause) or [**IWMReader::Stop**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-stop) methods respectively.</span></span>

## <a name="pausing"></a><span data-ttu-id="e9bc3-117">Приостановка</span><span class="sxs-lookup"><span data-stu-id="e9bc3-117">Pausing</span></span>

<span data-ttu-id="e9bc3-118">При вызове **ивмреадер::P Аусе** для приостановки воспроизведения файла средство чтения отслеживает текущую позицией в файле.</span><span class="sxs-lookup"><span data-stu-id="e9bc3-118">When you call **IWMReader::Pause** to pause playback of a file, the reader keeps track of the current position in the file.</span></span> <span data-ttu-id="e9bc3-119">Чтобы возобновить воспроизведение после приостановки, вызовите метод [**ивмреадер:: Resume**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-resume).</span><span class="sxs-lookup"><span data-stu-id="e9bc3-119">To resume playing after pausing, call [**IWMReader::Resume**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-resume).</span></span> <span data-ttu-id="e9bc3-120">Воспроизведение продолжится с той точки, в которой оно приостанавливается.</span><span class="sxs-lookup"><span data-stu-id="e9bc3-120">Playback will resume from the point at which it paused.</span></span>

## <a name="stopping"></a><span data-ttu-id="e9bc3-121">Остановка</span><span class="sxs-lookup"><span data-stu-id="e9bc3-121">Stopping</span></span>

<span data-ttu-id="e9bc3-122">При вызове **ивмреадер::** halt для остановки воспроизведения файла средство чтения не отслеживает сведения о ходе воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="e9bc3-122">When you call **IWMReader::Stop** to halt playback of a file, the reader does not keep track of any information about the progress of playback.</span></span> <span data-ttu-id="e9bc3-123">Чтобы использовать команду **остановить** и позже вернуться к точке останова, необходимо сохранить время презентации последнего примера и использовать его в вызове **Ивмреадер:: Start**.</span><span class="sxs-lookup"><span data-stu-id="e9bc3-123">To use **Stop** and later return to the stopping point you must save the presentation time of the last sample delivered and use it in your call to **IWMReader::Start**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e9bc3-124">См. также</span><span class="sxs-lookup"><span data-stu-id="e9bc3-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9bc3-125">**Интерфейс Ивмреадер**</span><span class="sxs-lookup"><span data-stu-id="e9bc3-125">**IWMReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[<span data-ttu-id="e9bc3-126">**Чтение файлов с помощью асинхронного модуля чтения**</span><span class="sxs-lookup"><span data-stu-id="e9bc3-126">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> </dl>

 

 




