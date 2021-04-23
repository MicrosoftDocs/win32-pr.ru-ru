---
title: Поиск по номеру кадра с помощью синхронного модуля чтения
description: Поиск по номеру кадра с помощью синхронного модуля чтения
ms.assetid: 755e0124-de57-4699-af8e-c594567b5523
keywords:
- Расширенный формат систем (ASF), поиск по номерам кадров
- ASF (Расширенный системный формат), поиск по номерам кадров
- Расширенный формат систем (ASF), синхронные средства чтения
- ASF (Расширенный системный формат), синхронные средства чтения
- синхронные читатели, поиск по номерам кадров
- видеопотокы, поиск по номерам кадров
- потоки видео, синхронные читатели
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c26711d2d839e47279e7e52a50f5dc82c6e81da
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104336319"
---
# <a name="to-seek-by-frame-number-using-the-synchronous-reader"></a><span data-ttu-id="93a54-110">Поиск по номеру кадра с помощью синхронного модуля чтения</span><span class="sxs-lookup"><span data-stu-id="93a54-110">To Seek By Frame Number Using the Synchronous Reader</span></span>

<span data-ttu-id="93a54-111">Чтобы найти данные по номеру кадра с помощью синхронного модуля чтения, укажите диапазон для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="93a54-111">To seek for data by frame number using the synchronous reader, you specify a range for playback.</span></span> <span data-ttu-id="93a54-112">Диапазон определяется начальным номером кадра в указанном видеопотоке и числом кадров для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="93a54-112">A range is defined by a starting frame number in a specific video stream and a number of frames to play.</span></span>

<span data-ttu-id="93a54-113">Чтобы найти данные в файле ASF по номеру кадра с помощью синхронного модуля чтения, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="93a54-113">To seek data in an ASF file by frame number using the synchronous reader, perform the following steps.</span></span>

1.  <span data-ttu-id="93a54-114">Установите начальный номер кадра и число кадров, которые считываются для примера доставки, вызвав [**ивмсинкреадер:: сетранжебифраме**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrangebyframe).</span><span class="sxs-lookup"><span data-stu-id="93a54-114">Set the starting frame number and number of frames to read for sample delivery by calling [**IWMSyncReader::SetRangeByFrame**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrangebyframe).</span></span> <span data-ttu-id="93a54-115">Необходимо указать номер потока для видеопотока с индексированием кадров.</span><span class="sxs-lookup"><span data-stu-id="93a54-115">You must specify the stream number of a frame-indexed video stream.</span></span> <span data-ttu-id="93a54-116">Модуль чтения синхронизирует остальные выходные данные с временем представления указанного кадра указанного потока и начинает доставку выходных данных.</span><span class="sxs-lookup"><span data-stu-id="93a54-116">The reader will synchronize the rest of the outputs to the presentation time of the specified frame of the specified stream and begin delivering output samples.</span></span>
2.  <span data-ttu-id="93a54-117">Начало извлечения образцов с вызовами метода [**ивмсинкреадер:: жетнекстсампле**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample).</span><span class="sxs-lookup"><span data-stu-id="93a54-117">Begin retrieving samples with calls to [**IWMSyncReader::GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample).</span></span> <span data-ttu-id="93a54-118">Продолжайте работу, как обычно с синхронным модулем чтения.</span><span class="sxs-lookup"><span data-stu-id="93a54-118">Proceed as you normally would with the synchronous reader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="93a54-119">См. также</span><span class="sxs-lookup"><span data-stu-id="93a54-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="93a54-120">**Интерфейс Ивмсинкреадер**</span><span class="sxs-lookup"><span data-stu-id="93a54-120">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[<span data-ttu-id="93a54-121">**Чтение файлов с помощью синхронного модуля чтения**</span><span class="sxs-lookup"><span data-stu-id="93a54-121">**Reading Files with the Synchronous Reader**</span></span>](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




