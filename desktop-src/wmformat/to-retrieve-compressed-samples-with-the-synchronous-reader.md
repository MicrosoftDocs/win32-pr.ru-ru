---
title: Извлечение сжатых образцов с помощью синхронного модуля чтения
description: Извлечение сжатых образцов с помощью синхронного модуля чтения
ms.assetid: 1f6da1aa-c26a-486a-bb44-cc4305c71979
keywords:
- Расширенный формат систем (ASF), получение сжатых образцов
- ASF (Расширенный системный формат), получение сжатых образцов
- Расширенный формат систем (ASF), синхронные средства чтения
- ASF (Расширенный системный формат), синхронные средства чтения
- Расширенный формат систем (ASF), сжатые образцы
- ASF (Расширенный системный формат), сжатые образцы
- синхронные читатели, получение сжатых образцов
- синхронные читатели, сжатые образцы
- сжатые образцы, извлечение
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72f0051fc14a14500b2c6e69c5e32f7ec0c39a51
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104133491"
---
# <a name="to-retrieve-compressed-samples-with-the-synchronous-reader"></a><span data-ttu-id="c2784-112">Извлечение сжатых образцов с помощью синхронного модуля чтения</span><span class="sxs-lookup"><span data-stu-id="c2784-112">To Retrieve Compressed Samples with the Synchronous Reader</span></span>

<span data-ttu-id="c2784-113">Как и асинхронное средство чтения, синхронный читатель также может получать сжатые образцы.</span><span class="sxs-lookup"><span data-stu-id="c2784-113">Like the asynchronous reader, the synchronous reader can also retrieve compressed samples.</span></span> <span data-ttu-id="c2784-114">При копировании потоков из одного файла в другой следует использовать сжатые образцы.</span><span class="sxs-lookup"><span data-stu-id="c2784-114">Compressed samples should be used when copying streams from one file to another.</span></span>

<span data-ttu-id="c2784-115">Пакет SDK для формата Windows Media не предоставляет методы для декодирования данных после их извлечения из файла ASF.</span><span class="sxs-lookup"><span data-stu-id="c2784-115">The Windows Media Format SDK does not provide any methods for decoding data after it has been extracted from an ASF file.</span></span> <span data-ttu-id="c2784-116">Если вы получаете сжатые примеры и в дальнейшем хотите распаковать их, вам потребуется предоставить собственный код.</span><span class="sxs-lookup"><span data-stu-id="c2784-116">If you receive compressed samples and later want to decompress them, you will have to provide your own code to do so.</span></span> <span data-ttu-id="c2784-117">Одним из способов обойти это ограничение является запись сжатых образцов в новый ASF-файл и их повторное считывание в обычные, несжатые образцы.</span><span class="sxs-lookup"><span data-stu-id="c2784-117">One way to get around this limitation is to write the compressed samples to a new ASF file and then re-read them into normal, uncompressed samples.</span></span>

<span data-ttu-id="c2784-118">Чтобы получить сжатые образцы с помощью синхронного модуля чтения, вызовите [**ивмсинкреадер:: сетреадстреамсамплес**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setreadstreamsamples) до или во время воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="c2784-118">To receive compressed samples with the synchronous reader, call [**IWMSyncReader::SetReadStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setreadstreamsamples) before or during playback.</span></span> <span data-ttu-id="c2784-119">Передайте значение true для *фкомпрессед*.</span><span class="sxs-lookup"><span data-stu-id="c2784-119">Pass true for *fCompressed*.</span></span>

> [!Note]  
> <span data-ttu-id="c2784-120">Потоки изображений недопустимы для доставки сжатых потоков.</span><span class="sxs-lookup"><span data-stu-id="c2784-120">Image streams are not valid for compressed stream delivery.</span></span> <span data-ttu-id="c2784-121">При копировании потока изображений из одного файла в другой он не будет работать в новом файле.</span><span class="sxs-lookup"><span data-stu-id="c2784-121">If you copy an image stream from one file to another, it will not work in the new file.</span></span> <span data-ttu-id="c2784-122">Чтобы скопировать поток изображений из файла в файл, извлеките образцы потока изображений по номеру выхода и включите их в новый файл, как если бы он включал новый поток изображений.</span><span class="sxs-lookup"><span data-stu-id="c2784-122">To copy an image stream from file to file, retrieve the image stream samples by output number and include them in the new file as if including a new image stream.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="c2784-123">См. также</span><span class="sxs-lookup"><span data-stu-id="c2784-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2784-124">**Чтение файлов с помощью синхронного модуля чтения**</span><span class="sxs-lookup"><span data-stu-id="c2784-124">**Reading Files with the Synchronous Reader**</span></span>](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




