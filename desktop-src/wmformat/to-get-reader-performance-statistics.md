---
title: Получение статистики производительности читателя
description: Получение статистики производительности читателя
ms.assetid: 996abfe6-1444-48ab-8c34-ba923c4cd511
keywords:
- Расширенный формат систем (ASF), статистика производительности читателя
- ASF (Расширенный системный формат), статистика производительности читателя
- Расширенный системный формат (ASF), асинхронный читатель
- ASF (Расширенный системный формат), асинхронный читатель
- Расширенный системный формат (ASF), статистика производительности
- ASF (Расширенный системный формат), статистика производительности
- асинхронные модули чтения, статистика производительности
- производительность, статистика модуля чтения
- производительность, асинхронные читатели
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5484b211f2c2d1e9ad4cf9aac3773c7946757c2
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "103890236"
---
# <a name="to-get-reader-performance-statistics"></a><span data-ttu-id="63c4d-112">Получение статистики производительности читателя</span><span class="sxs-lookup"><span data-stu-id="63c4d-112">To Get Reader Performance Statistics</span></span>

<span data-ttu-id="63c4d-113">При локальном чтении файлов с помощью асинхронного модуля чтения нет необходимости проверять производительность операций чтения.</span><span class="sxs-lookup"><span data-stu-id="63c4d-113">When reading files locally with the asynchronous reader, it is not necessary to check the performance of reading operations.</span></span> <span data-ttu-id="63c4d-114">Если приложение считывает данные из источника потоковой передачи, то статистика производительности может быть очень важной.</span><span class="sxs-lookup"><span data-stu-id="63c4d-114">If your application is reading from a streaming source however, performance statistics can be very important.</span></span> <span data-ttu-id="63c4d-115">Приложение может реагировать на изменения в производительности воспроизведения, чтобы обеспечить лучшее взаимодействие с конечными пользователями.</span><span class="sxs-lookup"><span data-stu-id="63c4d-115">Your application can respond to changes in playback performance to ensure the best possible end-user experience.</span></span>

<span data-ttu-id="63c4d-116">Сведения о производительности, которые можно получить из средства чтения, включают в себя следующую статистику:</span><span class="sxs-lookup"><span data-stu-id="63c4d-116">The performance information you can retrieve from the reader includes the following statistics:</span></span>

-   <span data-ttu-id="63c4d-117">Текущая пропускная способность соединения.</span><span class="sxs-lookup"><span data-stu-id="63c4d-117">The current bandwidth of the connection.</span></span>
-   <span data-ttu-id="63c4d-118">Число пакетов, полученных с сервера.</span><span class="sxs-lookup"><span data-stu-id="63c4d-118">The number of packets received from the server.</span></span>
-   <span data-ttu-id="63c4d-119">Количество потерянных пакетов, которые были восстановлены.</span><span class="sxs-lookup"><span data-stu-id="63c4d-119">The number of lost packets that were recovered.</span></span>
-   <span data-ttu-id="63c4d-120">Количество потерянных пакетов, которые не были восстановлены.</span><span class="sxs-lookup"><span data-stu-id="63c4d-120">The number of lost packets that were not recovered.</span></span>
-   <span data-ttu-id="63c4d-121">Процент от общего числа полученных отправленных пакетов.</span><span class="sxs-lookup"><span data-stu-id="63c4d-121">The percentage of the total number of packets sent that have been received.</span></span>

<span data-ttu-id="63c4d-122">Чтобы получить статистику производительности читателя, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="63c4d-122">To get reader performance statistics, perform the following steps.</span></span>

1.  <span data-ttu-id="63c4d-123">Перед запуском воспроизведения Создайте структуру [**\_ \_ статистики модуля чтения WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_reader_statistics) .</span><span class="sxs-lookup"><span data-stu-id="63c4d-123">Before starting playback, create a [**WM\_READER\_STATISTICS**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_reader_statistics) structure.</span></span> <span data-ttu-id="63c4d-124">Необходимо задать для элемента **кбсизе** значение sizeof ( \_ Статистика модуля чтения WM \_ ).</span><span class="sxs-lookup"><span data-stu-id="63c4d-124">You must set the **cbSize** member to sizeof(WM\_READER\_STATISTICS).</span></span>
2.  <span data-ttu-id="63c4d-125">Получите указатель на интерфейс [**ивмреадерадванцед**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) объекта Reader, вызвав **Ивмреадер:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="63c4d-125">Obtain a pointer to the [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) interface of the reader object by calling **IWMReader::QueryInterface**.</span></span>
3.  <span data-ttu-id="63c4d-126">Во время воспроизведения Сделайте вызов [**ивмреадерадванцед:: Statistics**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics) часто для наблюдения за производительностью.</span><span class="sxs-lookup"><span data-stu-id="63c4d-126">During playback, make calls to [**IWMReaderAdvanced::GetStatistics**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics) frequently to monitor performance.</span></span> <span data-ttu-id="63c4d-127">Передайте **структуру \_ \_ статистики модуля чтения WM** с каждым вызовом и изучите соответствующие члены.</span><span class="sxs-lookup"><span data-stu-id="63c4d-127">Pass your **WM\_READER\_STATISTICS** structure with each call and examine the appropriate members.</span></span>

## <a name="related-topics"></a><span data-ttu-id="63c4d-128">См. также</span><span class="sxs-lookup"><span data-stu-id="63c4d-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63c4d-129">**Чтение файлов с помощью асинхронного модуля чтения**</span><span class="sxs-lookup"><span data-stu-id="63c4d-129">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> </dl>

 

 




