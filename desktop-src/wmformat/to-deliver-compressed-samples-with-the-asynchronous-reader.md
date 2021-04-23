---
title: Доставка сжатых образцов с помощью асинхронного модуля чтения
description: Доставка сжатых образцов с помощью асинхронного модуля чтения
ms.assetid: 488baa3c-8863-4afc-89b2-fe55823e5db9
keywords:
- Расширенный формат систем (ASF), Доставка сжатых образцов
- ASF (Расширенный системный формат), Доставка сжатых образцов
- Расширенный системный формат (ASF), асинхронный читатель
- ASF (Расширенный системный формат), асинхронный читатель
- Расширенный формат систем (ASF), сжатые образцы
- ASF (Расширенный системный формат), сжатые образцы
- асинхронные модули чтения, Доставка сжатых образцов
- асинхронные модули чтения, сжатые образцы
- сжатые образцы, Доставка
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4ce835075f5bd760014a3b1b776ba3627adb076
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "103788791"
---
# <a name="to-deliver-compressed-samples-with-the-asynchronous-reader"></a><span data-ttu-id="343a8-112">Доставка сжатых образцов с помощью асинхронного модуля чтения</span><span class="sxs-lookup"><span data-stu-id="343a8-112">To Deliver Compressed Samples with the Asynchronous Reader</span></span>

<span data-ttu-id="343a8-113">Асинхронный читатель может доставлять сжатые образцы из потоков в файлах ASF.</span><span class="sxs-lookup"><span data-stu-id="343a8-113">The asynchronous reader can deliver compressed samples from streams in ASF files.</span></span> <span data-ttu-id="343a8-114">Обычно приложения предоставляют сжатые образцы при копировании потока из одного файла в другой.</span><span class="sxs-lookup"><span data-stu-id="343a8-114">Applications usually deliver compressed samples when copying a stream from one file to another.</span></span> <span data-ttu-id="343a8-115">Не рекомендуется повторно сжимать данные, которые были перестроены из сжатого потока, так как данные теряются в процессе кодирования.</span><span class="sxs-lookup"><span data-stu-id="343a8-115">It is not advisable to recompress data that has been reconstructed from a compressed stream, because data is lost in the encoding process.</span></span> <span data-ttu-id="343a8-116">Цифровые носители, сжатые более одного раза, имеют заметное снижение качества.</span><span class="sxs-lookup"><span data-stu-id="343a8-116">Digital media that has been compressed more than once will have a noticeable decrease in quality.</span></span>

<span data-ttu-id="343a8-117">Пакет SDK для формата Windows Media не предоставляет методы для декодирования данных после их извлечения из файла ASF.</span><span class="sxs-lookup"><span data-stu-id="343a8-117">The Windows Media Format SDK does not provide any methods for decoding data after it has been extracted from an ASF file.</span></span> <span data-ttu-id="343a8-118">Если вы получаете сжатые примеры и в дальнейшем хотите распаковать их, вам потребуется предоставить собственный код.</span><span class="sxs-lookup"><span data-stu-id="343a8-118">If you receive compressed samples and later want to decompress them, you will have to provide your own code to do so.</span></span> <span data-ttu-id="343a8-119">Одним из способов обойти это ограничение является запись сжатых образцов в новый ASF-файл и их повторное считывание в обычные, несжатые образцы.</span><span class="sxs-lookup"><span data-stu-id="343a8-119">One way to get around this limitation is to write the compressed samples to a new ASF file and then re-read them into normal, uncompressed samples.</span></span>

<span data-ttu-id="343a8-120">Чтобы получить сжатые образцы с помощью асинхронного модуля чтения, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="343a8-120">To receive compressed samples with the asynchronous reader, perform the following steps.</span></span>

1.  <span data-ttu-id="343a8-121">Реализуйте обратный вызов [**ивмреадеркаллбаккадванцед:: онстреамсампле**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample) .</span><span class="sxs-lookup"><span data-stu-id="343a8-121">Implement the [**IWMReaderCallbackAdvanced::OnStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample) callback.</span></span> <span data-ttu-id="343a8-122">Этот обратный вызов по сути идентичен функции [**ивмреадеркаллбакк:: OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) , за исключением того, что он доставляет выборки по номеру потока, а образцы по-прежнему сжимаются.</span><span class="sxs-lookup"><span data-stu-id="343a8-122">This callback is basically identical in function to [**IWMReaderCallback::OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) except that it delivers samples by stream number and the samples are still compressed.</span></span>
2.  <span data-ttu-id="343a8-123">Перед запуском воспроизведения получите указатель на интерфейс [**ивмреадерадванцед**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) объекта Reader, вызвав **Ивмреадер:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="343a8-123">Before starting playback, obtain a pointer to the [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) interface of the reader object by calling **IWMReader::QueryInterface**.</span></span>
3.  <span data-ttu-id="343a8-124">Настройте модуль чтения для доставки сжатых образцов для нужного потока путем вызова [**ивмреадерадванцед:: сетрецеивестреамсамплес**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setreceivestreamsamples).</span><span class="sxs-lookup"><span data-stu-id="343a8-124">Configure the reader to deliver compressed samples for the desired stream by calling [**IWMReaderAdvanced::SetReceiveStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setreceivestreamsamples).</span></span>
4.  <span data-ttu-id="343a8-125">Повторите шаг 3 для каждого потока, для которого требуется сжатый пример доставки.</span><span class="sxs-lookup"><span data-stu-id="343a8-125">Repeat step 3 for each stream for which compressed sample delivery is desired.</span></span>

> [!Note]  
> <span data-ttu-id="343a8-126">Потоки изображений недопустимы для доставки сжатых потоков.</span><span class="sxs-lookup"><span data-stu-id="343a8-126">Image streams are not valid for compressed stream delivery.</span></span> <span data-ttu-id="343a8-127">При копировании потока изображений из одного файла в другой он не будет работать в новом файле.</span><span class="sxs-lookup"><span data-stu-id="343a8-127">If you copy an image stream from one file to another, it will not work in the new file.</span></span> <span data-ttu-id="343a8-128">Чтобы скопировать поток изображений из файла в файл, извлеките образцы потока изображений по номеру выхода и включите их в новый файл, как если бы он включал новый поток изображений.</span><span class="sxs-lookup"><span data-stu-id="343a8-128">To copy an image stream from file to file, retrieve the image stream samples by output number and include them in the new file as if including a new image stream.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="343a8-129">См. также</span><span class="sxs-lookup"><span data-stu-id="343a8-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="343a8-130">**Интерфейс Ивмреадеркаллбаккадванцед**</span><span class="sxs-lookup"><span data-stu-id="343a8-130">**IWMReaderCallbackAdvanced Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallbackadvanced)
</dt> <dt>

[<span data-ttu-id="343a8-131">**Чтение файлов с помощью асинхронного модуля чтения**</span><span class="sxs-lookup"><span data-stu-id="343a8-131">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> </dl>

 

 




