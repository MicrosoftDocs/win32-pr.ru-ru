---
title: Поиск по коду времени SMPTE с помощью асинхронного модуля чтения
description: Поиск по коду времени SMPTE с помощью асинхронного модуля чтения
ms.assetid: 5c618f04-3761-418c-b75a-70c7bf7fa5be
keywords:
- Расширенный системный формат (ASF), поиск по кодам времени SMPTE
- ASF (Расширенный системный формат), поиск по кодам времени SMPTE
- Расширенный системный формат (ASF), асинхронный читатель
- ASF (Расширенный системный формат), асинхронный читатель
- Расширенный формат систем (ASF), коды времени SMPTE
- ASF (Расширенный системный формат), коды времени SMPTE
- асинхронные средства чтения, поиск по кодам времени SMPTE
- асинхронные читатели, коды времени SMPTE
- Коды времени SMPTE, Поиск
- Коды времени SMPTE, асинхронные модули чтения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42bb90e899db9820ccbd14e42b9699a5f99c7434
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104412481"
---
# <a name="to-seek-by-smpte-time-code-using-the-asynchronous-reader"></a><span data-ttu-id="ac761-113">Поиск по коду времени SMPTE с помощью асинхронного модуля чтения</span><span class="sxs-lookup"><span data-stu-id="ac761-113">To Seek By SMPTE Time Code Using the Asynchronous Reader</span></span>

<span data-ttu-id="ac761-114">Объект Reader может перейти к точке в файле на основе кода времени SMPTE, связанного с потоком видео.</span><span class="sxs-lookup"><span data-stu-id="ac761-114">The reader object can seek to a point in a file based on the SMPTE time code associated with a video stream.</span></span> <span data-ttu-id="ac761-115">Данные кода времени инкапсулируются в структурах [**\_ \_ \_ данных расширения ВМТ**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data) Time, которые прикрепляются к образцам видео в виде модулей обработки данных.</span><span class="sxs-lookup"><span data-stu-id="ac761-115">Time code data is encapsulated in [**WMT\_TIMECODE\_EXTENSION\_DATA**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data) structures that are attached to video samples as data unit extensions.</span></span>

<span data-ttu-id="ac761-116">Коды времени SMPTE определяются диапазоном и кодом времени в пределах этого диапазона.</span><span class="sxs-lookup"><span data-stu-id="ac761-116">SMPTE time codes are defined by a range and a time code within that range.</span></span> <span data-ttu-id="ac761-117">Диапазон — это непрерывная последовательность кодов времени.</span><span class="sxs-lookup"><span data-stu-id="ac761-117">A range is a continuous series of time codes.</span></span> <span data-ttu-id="ac761-118">Каждый код времени определяется часами, минутами, секундами и кадрами.</span><span class="sxs-lookup"><span data-stu-id="ac761-118">Each time code is defined by hours, minutes, seconds, and frames.</span></span>

<span data-ttu-id="ac761-119">Чтобы найти данные в файле ASF, SMPTE код времени с помощью асинхронного модуля чтения, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ac761-119">To seek data in an ASF file by SMPTE time code using the asynchronous reader, perform the following steps.</span></span>

1.  <span data-ttu-id="ac761-120">Получите указатель на интерфейс [**IWMReaderAdvanced3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3) объекта Reader, вызвав **Ивмреадер:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="ac761-120">Obtain a pointer to the [**IWMReaderAdvanced3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3) interface of the reader object by calling **IWMReader::QueryInterface**.</span></span>
2.  <span data-ttu-id="ac761-121">Задайте код времени начала и длительность, вызвав [**IWMReaderAdvanced3:: стартатпоситион**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced3-startatposition).</span><span class="sxs-lookup"><span data-stu-id="ac761-121">Set the starting time code and duration by calling [**IWMReaderAdvanced3::StartAtPosition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced3-startatposition).</span></span> <span data-ttu-id="ac761-122">Необходимо указать номер потока видеопотока, индексируемого по коду времени.</span><span class="sxs-lookup"><span data-stu-id="ac761-122">You must specify the stream number of a video stream that is indexed by time code.</span></span> <span data-ttu-id="ac761-123">Модуль чтения синхронизирует остальные выходные данные с временем представления указанного кадра указанного потока и начинает доставку выходных данных.</span><span class="sxs-lookup"><span data-stu-id="ac761-123">The reader will synchronize the rest of the outputs to the presentation time of the specified frame of the specified stream and begin delivering output samples.</span></span>
3.  <span data-ttu-id="ac761-124">Обработайте примеры, как обычно в реализации метода **ивмреадеркаллбакк:: OnSample** .</span><span class="sxs-lookup"><span data-stu-id="ac761-124">Handle the samples as you normally would in your implementation of the **IWMReaderCallback::OnSample** method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ac761-125">См. также</span><span class="sxs-lookup"><span data-stu-id="ac761-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac761-126">**Чтение файлов с помощью асинхронного модуля чтения**</span><span class="sxs-lookup"><span data-stu-id="ac761-126">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="ac761-127">**Работа с индексами**</span><span class="sxs-lookup"><span data-stu-id="ac761-127">**Working with Indexes**</span></span>](working-with-indexes.md)
</dt> <dt>

[<span data-ttu-id="ac761-128">**Поддержка кода времени SMPTE**</span><span class="sxs-lookup"><span data-stu-id="ac761-128">**SMPTE Time Code Support**</span></span>](smpte-time-code-support.md)
</dt> </dl>

 

 




