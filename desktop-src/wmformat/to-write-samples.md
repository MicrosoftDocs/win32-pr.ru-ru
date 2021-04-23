---
title: Написание образцов
description: Написание образцов
ms.assetid: 9ce10a77-9e80-45e0-a7e7-2ffdf8b57773
keywords:
- Расширенный системный формат (ASF), написание примеров
- ASF (Расширенный системный формат), написание образцов
- Расширенный формат систем (ASF), передача образцов в модуль записи
- ASF (Расширенный системный формат), передача образцов в модуль записи
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 738014b3c42441e878105d12a8ebf23ce4b266f7
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104412503"
---
# <a name="to-write-samples"></a><span data-ttu-id="49430-107">Написание образцов</span><span class="sxs-lookup"><span data-stu-id="49430-107">To Write Samples</span></span>

<span data-ttu-id="49430-108">Определив и настроив входные данные для файла, который вы пишете, можно начать передавать примеры в модуль записи.</span><span class="sxs-lookup"><span data-stu-id="49430-108">When you have identified and configured the inputs for the file you are writing, you can begin passing samples to the writer.</span></span> <span data-ttu-id="49430-109">При возможности необходимо передавать образцы в порядке, если это возможно, чтобы сделать процесс записи более эффективным.</span><span class="sxs-lookup"><span data-stu-id="49430-109">You should pass samples in presentation-time order, if possible, to make the writing process more efficient.</span></span>

<span data-ttu-id="49430-110">Перед передачей всех выборок необходимо настроить для модуля записи возможность их принятия путем вызова [**ивмвритер:: бегинвритинг**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).</span><span class="sxs-lookup"><span data-stu-id="49430-110">Before passing any samples, you must set the writer to accept them by calling [**IWMWriter::BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).</span></span>

<span data-ttu-id="49430-111">Чтобы передать пример в модуль записи, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="49430-111">To pass a sample to the writer, perform the following steps:</span></span>

1.  <span data-ttu-id="49430-112">Выделите буфер и получите указатель на интерфейс [**инссбуффер**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) , вызвав [**Ивмвритер:: аллокатесампле**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-allocatesample).</span><span class="sxs-lookup"><span data-stu-id="49430-112">Allocate a buffer and retrieve a pointer to the [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) interface by calling [**IWMWriter::AllocateSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-allocatesample).</span></span>
2.  <span data-ttu-id="49430-113">Извлеките адрес буфера, созданного на шаге 1, вызвав [**инссбуффер:: @ buffer**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-getbuffer).</span><span class="sxs-lookup"><span data-stu-id="49430-113">Retrieve the address of the buffer created in step 1 by calling [**INSSBuffer::GetBuffer**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-getbuffer).</span></span>
3.  <span data-ttu-id="49430-114">Скопируйте образец данных в буферное расположение, убедившись, что переданный образец будет помещаться в выделенный буфер.</span><span class="sxs-lookup"><span data-stu-id="49430-114">Copy your sample data to the buffer location, making sure that the sample passed will fit in the allocated buffer.</span></span> <span data-ttu-id="49430-115">Для копирования данных можно использовать любую функцию копирования памяти.</span><span class="sxs-lookup"><span data-stu-id="49430-115">You can use any memory copying function to copy your data.</span></span> <span data-ttu-id="49430-116">Распространенный выбор — memcpy, который включается в стандартную библиотеку времени выполнения C.</span><span class="sxs-lookup"><span data-stu-id="49430-116">A common choice is memcpy, which is included in the standard C run-time library.</span></span>
4.  <span data-ttu-id="49430-117">Обновите объем данных, используемых в буфере, чтобы отразить фактический размер образца путем вызова [**инссбуффер:: SetLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-setlength).</span><span class="sxs-lookup"><span data-stu-id="49430-117">Update the amount of data used in the buffer to reflect the actual size of the sample by calling [**INSSBuffer::SetLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-setlength).</span></span>
5.  <span data-ttu-id="49430-118">Передайте интерфейс буфера записи, а также входной номер и время выборки с помощью метода [**ивмвритер:: вритесампле**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) .</span><span class="sxs-lookup"><span data-stu-id="49430-118">Pass the buffer interface to the writer along with the input number and sample time using the [**IWMWriter::WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) method.</span></span> <span data-ttu-id="49430-119">Все звуковые примеры для входных данных представляют одинаковую длительность содержимого, поэтому можно определить время выборки, добавив длительность выборки в итоговое значение.</span><span class="sxs-lookup"><span data-stu-id="49430-119">All audio samples for an input represent the same duration of content, so you can figure the sample time by adding the sample duration to a running total.</span></span> <span data-ttu-id="49430-120">Для видео необходимо вычислить время на основе частоты кадров.</span><span class="sxs-lookup"><span data-stu-id="49430-120">For video, you need to calculate the time based on the frame rate.</span></span>

<span data-ttu-id="49430-121">**Вритесампле** работает асинхронно и может не завершить запись данных из буфера до того, как приложение будет готово к повторному вызову метода.</span><span class="sxs-lookup"><span data-stu-id="49430-121">**WriteSample** works asynchronously and might not finish writing the data from the buffer before your application is ready to call the method again.</span></span> <span data-ttu-id="49430-122">Поэтому важно вызывать **аллокатесампле** один раз для каждого вызова **вритесампле**.</span><span class="sxs-lookup"><span data-stu-id="49430-122">Therefore, it is important to call **AllocateSample** once for each call to **WriteSample**.</span></span> <span data-ttu-id="49430-123">Однако можно освободить интерфейс **инссбуффер** сразу после вызова **вритесампле**.</span><span class="sxs-lookup"><span data-stu-id="49430-123">However, you can release the **INSSBuffer** interface immediately after calling **WriteSample**.</span></span>

<span data-ttu-id="49430-124">После завершения передачи образцов вызовите [**ивмвритер:: ендвритинг**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-endwriting).</span><span class="sxs-lookup"><span data-stu-id="49430-124">When you have finished passing samples, call [**IWMWriter::EndWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-endwriting).</span></span>

<span data-ttu-id="49430-125">**Примечание** . Важно, чтобы образцы из всех потоков в файле передавались модулю записи при синхронизации друг с другом.</span><span class="sxs-lookup"><span data-stu-id="49430-125">**Note** It is important that samples from all streams in the file are passed to the writer in synchronization with one another.</span></span> <span data-ttu-id="49430-126">То есть каждый раз, когда это возможно, следует передавать образцы в модуль записи в порядке представления в пределах синхронизации, указанной в [**ивмвритерадванцед:: сетсинктолеранце**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-setsynctolerance).</span><span class="sxs-lookup"><span data-stu-id="49430-126">That is, whenever possible you should pass samples to the writer in presentation-time order within the sync tolerance specified in [**IWMWriterAdvanced::SetSyncTolerance**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-setsynctolerance).</span></span> <span data-ttu-id="49430-127">Наилучшие результаты достигаются, когда данные доставляются в каждый поток в единицах в одну секунду или меньше.</span><span class="sxs-lookup"><span data-stu-id="49430-127">Best results are achieved when data is delivered to each stream in units of one second or less.</span></span>

<span data-ttu-id="49430-128">Потоки также должны заканчиваться приблизительно в одно и то же время.</span><span class="sxs-lookup"><span data-stu-id="49430-128">Streams should also end at approximately the same time.</span></span> <span data-ttu-id="49430-129">Например, не следует писать файл со звуковым потоком, который составляет 45 секунд и длинный поток видео длиной 50 секунды.</span><span class="sxs-lookup"><span data-stu-id="49430-129">For example, you should not write a file with an audio stream that is 45 seconds long and a video stream that is 50 seconds long.</span></span> <span data-ttu-id="49430-130">Если вы кодируете такой файл с неизмененными входами, некоторые звуковые данные в конце потока будут удалены (даже если это более короткий поток).</span><span class="sxs-lookup"><span data-stu-id="49430-130">If you encode such a file with unaltered inputs, some of the audio data at the end of the stream will be dropped (even though it is the shorter stream).</span></span> <span data-ttu-id="49430-131">Чтобы кодировка файла работала, необходимо добавить 5 секунд тишины к входному звуку, чтобы один поток не закончит несколько секунд перед другим.</span><span class="sxs-lookup"><span data-stu-id="49430-131">To make the file encoding work, you should add 5 seconds of silence to the audio input so that one stream does not end several seconds before another.</span></span> <span data-ttu-id="49430-132">Для типов потоков с временными примерами, такими как потоки текста или изображений, необязательно устанавливать заполнение таким образом.</span><span class="sxs-lookup"><span data-stu-id="49430-132">It is not necessary for stream types with intermittent samples, like text or image streams, to be padded in this way.</span></span> <span data-ttu-id="49430-133">Потоки команд сценария также должны следовать всем этим правилам.</span><span class="sxs-lookup"><span data-stu-id="49430-133">Script command streams should also follow all these rules.</span></span>

## <a name="related-topics"></a><span data-ttu-id="49430-134">См. также</span><span class="sxs-lookup"><span data-stu-id="49430-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49430-135">**Интерфейс Инссбуффер**</span><span class="sxs-lookup"><span data-stu-id="49430-135">**INSSBuffer Interface**</span></span>](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer)
</dt> <dt>

[<span data-ttu-id="49430-136">**Интерфейс Ивмвритер**</span><span class="sxs-lookup"><span data-stu-id="49430-136">**IWMWriter Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[<span data-ttu-id="49430-137">**Запись файлов ASF**</span><span class="sxs-lookup"><span data-stu-id="49430-137">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




