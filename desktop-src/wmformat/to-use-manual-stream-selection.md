---
title: Использование ручного выбора потока
description: Использование ручного выбора потока
ms.assetid: 49ec283f-670a-4a0e-9477-c60a80919a1e
keywords:
- Расширенный системный формат (ASF), выбор потока вручную
- ASF (Расширенный системный формат), выбор потока вручную
- Расширенный системный формат (ASF), асинхронный читатель
- ASF (Расширенный системный формат), асинхронный читатель
- Расширенный системный формат (ASF), выбор потока
- ASF (Расширенный системный формат), выбор потока
- Расширенный формат систем (ASF), взаимное исключение
- ASF (Расширенный системный формат), взаимное исключение
- асинхронные модули чтения, выбор потока вручную
- асинхронные читатели, выбор потоков
- потоки, выбор вручную
- взаимное исключение, выбор потока вручную
- потоки, асинхронные модули чтения
- взаимное исключение, асинхронные модули чтения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a87c493bc8f41bc2a03ba15832ed402939adbeff
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "105691460"
---
# <a name="to-use-manual-stream-selection"></a><span data-ttu-id="39061-117">Использование ручного выбора потока</span><span class="sxs-lookup"><span data-stu-id="39061-117">To Use Manual Stream Selection</span></span>

<span data-ttu-id="39061-118">При доставке несжатых образцов с помощью объекта Reader их можно доставлять только по номеру выхода.</span><span class="sxs-lookup"><span data-stu-id="39061-118">When delivering uncompressed samples with the reader object, you can deliver them only by output number.</span></span> <span data-ttu-id="39061-119">В случае взаимоисключающих потоков это означает, что вы можете получать образцы только из одного потока в взаимном исключении за раз.</span><span class="sxs-lookup"><span data-stu-id="39061-119">In the case of mutually exclusive streams, this means that you can receive samples only from one stream in the mutual exclusion at a time.</span></span> <span data-ttu-id="39061-120">Процесс выбора взаимоисключающего потока для доставки называется выбором потока.</span><span class="sxs-lookup"><span data-stu-id="39061-120">The process of choosing which mutually exclusive stream to deliver is called stream selection.</span></span>

<span data-ttu-id="39061-121">Для взаимного исключения с использованием битовой скорости модуль чтения автоматически выбирает поток в зависимости от условий на размещающем компьютере при воспроизведении.</span><span class="sxs-lookup"><span data-stu-id="39061-121">For bit-rate mutual exclusion, the reader makes stream selections automatically based on the conditions on the host machine at playback.</span></span> <span data-ttu-id="39061-122">Для других типов взаимного исключения модуль чтения будет доставлять образцы из потока по умолчанию, если только вы не вручную выбрали другой поток.</span><span class="sxs-lookup"><span data-stu-id="39061-122">For other types of mutual exclusion, the reader will deliver samples from the default stream unless you manually select a different stream yourself.</span></span> <span data-ttu-id="39061-123">Также могут быть экземпляры, когда требуется выбрать поток вручную с помощью взаимного исключения с побитовой скоростью.</span><span class="sxs-lookup"><span data-stu-id="39061-123">There may also be instances when you want to select a stream manually from a bit-rate mutual exclusion.</span></span>

<span data-ttu-id="39061-124">Ручной выбор потока может быть включен или выключен для всего файла.</span><span class="sxs-lookup"><span data-stu-id="39061-124">Manual stream selection is either on or off for the entire file.</span></span> <span data-ttu-id="39061-125">Если файл содержит взаимное исключение с битовой скоростью и другой тип взаимного исключения, необходимо вручную выбрать потоковую скорость на основе потока.</span><span class="sxs-lookup"><span data-stu-id="39061-125">If a file contains bit-rate mutual exclusion and some other mutual exclusion type, you must select the bit rate based streams manually.</span></span>

<span data-ttu-id="39061-126">Чтобы выбрать взаимоисключающий поток вручную, необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="39061-126">To select a mutually exclusive stream manually, you must perform the following steps.</span></span>

1.  <span data-ttu-id="39061-127">Получите указатель на интерфейс [**ивмреадерадванцед**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) объекта Reader, вызвав **Ивмреадер:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="39061-127">Retrieve a pointer to the [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) interface of the reader object by calling **IWMReader::QueryInterface**.</span></span>
2.  <span data-ttu-id="39061-128">Включить выбор потока вручную путем вызова [**ивмреадерадванцед:: сетмануалстреамселектион**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setmanualstreamselection).</span><span class="sxs-lookup"><span data-stu-id="39061-128">Enable manual stream selection by calling [**IWMReaderAdvanced::SetManualStreamSelection**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setmanualstreamselection).</span></span>
3.  <span data-ttu-id="39061-129">Чтобы определить, выбран ли определенный поток, вызовите метод [**ивмреадерадванцед:: жетстреамселектед**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstreamselected).</span><span class="sxs-lookup"><span data-stu-id="39061-129">To find out if a particular stream is selected, call [**IWMReaderAdvanced::GetStreamSelected**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstreamselected).</span></span> <span data-ttu-id="39061-130">Необходимо передать указатель на переменную типа перечисления [**\_ \_ выбора потока ВМТ**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_stream_selection) .</span><span class="sxs-lookup"><span data-stu-id="39061-130">You must pass a pointer to a variable of the [**WMT\_STREAM\_SELECTION**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_stream_selection) enumeration type.</span></span> <span data-ttu-id="39061-131">При возвращении вызова значение в переменной будет описывать текущий тип выбора потока.</span><span class="sxs-lookup"><span data-stu-id="39061-131">When the call returns, the value in the variable will describe the current selection type of the stream.</span></span>
4.  <span data-ttu-id="39061-132">Чтобы выбрать поток, вызовите метод [**ивмреадерадванцед:: сетстреамсселектед**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setstreamsselected).</span><span class="sxs-lookup"><span data-stu-id="39061-132">To select a stream, call [**IWMReaderAdvanced::SetStreamsSelected**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setstreamsselected).</span></span> <span data-ttu-id="39061-133">Этот метод позволяет указать несколько потоков одновременно для синхронизации переключения потоков.</span><span class="sxs-lookup"><span data-stu-id="39061-133">This method enables you to specify multiple streams at the same time for synchronized stream switching.</span></span>

## <a name="related-topics"></a><span data-ttu-id="39061-134">См. также</span><span class="sxs-lookup"><span data-stu-id="39061-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39061-135">**Чтение файлов с помощью асинхронного модуля чтения**</span><span class="sxs-lookup"><span data-stu-id="39061-135">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> </dl>

 

 




