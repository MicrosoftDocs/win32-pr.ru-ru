---
title: Поиск по коду времени SMPTE с помощью синхронного модуля чтения
description: Поиск по коду времени SMPTE с помощью синхронного модуля чтения
ms.assetid: 1fd8885c-a694-43fd-b2a2-23eb0ae7ed72
keywords:
- Расширенный системный формат (ASF), поиск по кодам времени SMPTE
- ASF (Расширенный системный формат), поиск по кодам времени SMPTE
- Расширенный формат систем (ASF), синхронные средства чтения
- ASF (Расширенный системный формат), синхронные средства чтения
- Расширенный формат систем (ASF), коды времени SMPTE
- ASF (Расширенный системный формат), коды времени SMPTE
- синхронные читатели, поиск по кодам времени SMPTE
- синхронные читатели, коды времени SMPTE
- Коды времени SMPTE, Поиск
- Коды времени SMPTE, синхронные средства чтения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c843ba802272d02f1dfc885a3c65b3d124b7423
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104336399"
---
# <a name="to-seek-by-smpte-time-code-using-the-synchronous-reader"></a><span data-ttu-id="1c2a0-113">Поиск по коду времени SMPTE с помощью синхронного модуля чтения</span><span class="sxs-lookup"><span data-stu-id="1c2a0-113">To Seek By SMPTE Time Code Using the Synchronous Reader</span></span>

<span data-ttu-id="1c2a0-114">Синхронный объект Reader может выполнять поиск в точке файла на основе кода времени SMPTE, связанного с потоком видео.</span><span class="sxs-lookup"><span data-stu-id="1c2a0-114">The synchronous reader object can seek to a point in a file based on the SMPTE time code associated with a video stream.</span></span> <span data-ttu-id="1c2a0-115">Данные кода времени инкапсулируются в структурах [**\_ \_ \_ данных расширения ВМТ**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data) Time, которые прикрепляются к образцам видео в виде модулей обработки данных.</span><span class="sxs-lookup"><span data-stu-id="1c2a0-115">Time code data is encapsulated in [**WMT\_TIMECODE\_EXTENSION\_DATA**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data) structures that are attached to video samples as data unit extensions.</span></span>

<span data-ttu-id="1c2a0-116">Коды времени SMPTE определяются диапазоном и кодом времени в пределах этого диапазона.</span><span class="sxs-lookup"><span data-stu-id="1c2a0-116">SMPTE time codes are defined by a range and a time code within that range.</span></span> <span data-ttu-id="1c2a0-117">Диапазон — это непрерывная последовательность кодов времени.</span><span class="sxs-lookup"><span data-stu-id="1c2a0-117">A range is a continuous series of time codes.</span></span> <span data-ttu-id="1c2a0-118">Каждый код времени определяется часами, минутами, секундами и кадрами.</span><span class="sxs-lookup"><span data-stu-id="1c2a0-118">Each time code is defined by hours, minutes, seconds, and frames.</span></span>

<span data-ttu-id="1c2a0-119">Чтобы найти данные в файле ASF, SMPTE код времени с помощью синхронного модуля чтения, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="1c2a0-119">To seek data in an ASF file by SMPTE time code using the synchronous reader, perform the following steps.</span></span>

1.  <span data-ttu-id="1c2a0-120">Задайте начальный код времени и код времени окончания для образца доставки, вызвав [**ивмсинкреадер:: сетранжебифраме**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrangebyframe).</span><span class="sxs-lookup"><span data-stu-id="1c2a0-120">Set the starting time code and ending time code for sample delivery by calling [**IWMSyncReader::SetRangeByFrame**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrangebyframe).</span></span> <span data-ttu-id="1c2a0-121">Необходимо указать номер потока видеопотока, индексированного по коду времени.</span><span class="sxs-lookup"><span data-stu-id="1c2a0-121">You must specify the stream number of a video stream indexed by time code.</span></span> <span data-ttu-id="1c2a0-122">Синхронный модуль чтения синхронизирует остальные выходные данные с временем представления указанного кадра указанного потока.</span><span class="sxs-lookup"><span data-stu-id="1c2a0-122">The synchronous reader will synchronize the rest of the outputs to the presentation time of the specified frame of the specified stream.</span></span>
2.  <span data-ttu-id="1c2a0-123">Начало извлечения образцов с вызовами метода [**ивмсинкреадер:: жетнекстсампле**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample).</span><span class="sxs-lookup"><span data-stu-id="1c2a0-123">Begin retrieving samples with calls to [**IWMSyncReader::GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample).</span></span> <span data-ttu-id="1c2a0-124">Продолжайте работу, как обычно с синхронным модулем чтения.</span><span class="sxs-lookup"><span data-stu-id="1c2a0-124">Proceed as you normally would with the synchronous reader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1c2a0-125">См. также</span><span class="sxs-lookup"><span data-stu-id="1c2a0-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c2a0-126">**Чтение файлов с помощью синхронного модуля чтения**</span><span class="sxs-lookup"><span data-stu-id="1c2a0-126">**Reading Files with the Synchronous Reader**</span></span>](reading-files-with-the-synchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="1c2a0-127">**Поддержка кода времени SMPTE**</span><span class="sxs-lookup"><span data-stu-id="1c2a0-127">**SMPTE Time Code Support**</span></span>](smpte-time-code-support.md)
</dt> <dt>

[<span data-ttu-id="1c2a0-128">**Работа с индексами**</span><span class="sxs-lookup"><span data-stu-id="1c2a0-128">**Working with Indexes**</span></span>](working-with-indexes.md)
</dt> </dl>

 

 




