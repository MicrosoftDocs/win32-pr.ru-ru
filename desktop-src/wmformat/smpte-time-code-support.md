---
title: Поддержка кода времени SMPTE
description: Поддержка кода времени SMPTE
ms.assetid: 047bda0d-142d-4eed-9b59-c0c36b97ed45
keywords:
- Windows Media Format SDK, коды времени SMPTE
- Расширенный формат систем (ASF), коды времени SMPTE
- ASF (Расширенный системный формат), коды времени SMPTE
- Windows Media Format SDK, интерфейс Ивмреадертимекоде
- Расширенный системный формат (ASF), интерфейс Ивмреадертимекоде
- ASF (Расширенный системный формат), интерфейс Ивмреадертимекоде
- Коды времени SMPTE, сведения
- ивмреадертимекоде
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ecf8ef9da7d0fb0ee7d973cf21129f307066bc9
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104532993"
---
# <a name="smpte-time-code-support"></a><span data-ttu-id="f9792-111">Поддержка кода времени SMPTE</span><span class="sxs-lookup"><span data-stu-id="f9792-111">SMPTE Time Code Support</span></span>

<span data-ttu-id="f9792-112">Пакет SDK для формата Windows Media обеспечивает ограниченную поддержку кода времени SMPTE, который является стандартным форматом кода времени для фильмов и телевизоров.</span><span class="sxs-lookup"><span data-stu-id="f9792-112">The Windows Media Format SDK provides limited support for SMPTE time code, which is a standard time code format for movies and television.</span></span> <span data-ttu-id="f9792-113">В качестве расширений модулей данных можно включить данные кода времени SMPTE с примерами.</span><span class="sxs-lookup"><span data-stu-id="f9792-113">You can include SMPTE time code data with samples as data unit extensions.</span></span> <span data-ttu-id="f9792-114">Часть данных расширения — это структура [**\_ \_ \_ данных расширения времени ВМТ**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data) , содержащая информацию из исходной метки SMPTE Time.</span><span class="sxs-lookup"><span data-stu-id="f9792-114">The data portion of the extension is a [**WMT\_TIMECODE\_EXTENSION\_DATA**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data) structure containing the information from the original SMPTE time stamp.</span></span>

<span data-ttu-id="f9792-115">Поддержание кода времени SMPTE в файлах ASF имеет ограничения производительности.</span><span class="sxs-lookup"><span data-stu-id="f9792-115">Maintaining SMPTE time code in your ASF files comes with performance limits.</span></span> <span data-ttu-id="f9792-116">Каждому образцу с соответствующей отметкой времени SMPTE требуется транспорт 14 байт в структуре метки времени.</span><span class="sxs-lookup"><span data-stu-id="f9792-116">Each sample with an associated SMPTE time stamp requires transport of the 14 bytes in the time stamp structure.</span></span> <span data-ttu-id="f9792-117">В сценарии потоковой передачи это увеличение требований к пропускной способности может быть разрушительным.</span><span class="sxs-lookup"><span data-stu-id="f9792-117">In a streaming scenario, this increased bandwidth requirement could be catastrophic.</span></span> <span data-ttu-id="f9792-118">В результате мы рекомендуем, чтобы коды времени SMPTE сохранялись только в файлах ASF в процессе редактирования видео, что обычно выполняется с локальными файлами.</span><span class="sxs-lookup"><span data-stu-id="f9792-118">As a result, it is suggested that SMPTE time codes only be persisted in ASF files during the video editing process, which is typically done with local files.</span></span> <span data-ttu-id="f9792-119">При создании окончательного файла следует удалить расширения модулей данных.</span><span class="sxs-lookup"><span data-stu-id="f9792-119">When the final file is created, you should remove the data unit extensions.</span></span>

<span data-ttu-id="f9792-120">Вы можете считывать метки времени SMPTE так же, как и любые другие расширения единиц обработки данных, но объекты чтения предоставляют интегрированную поддержку поиска по коду времени SMPTE.</span><span class="sxs-lookup"><span data-stu-id="f9792-120">You can read SMPTE time stamps just as you would read any other data unit extension, but the reading objects provide integrated support for searching by SMPTE time code.</span></span> <span data-ttu-id="f9792-121">Чтобы иметь возможность искать метки времени SMPTE, необходимо сначала индексировать файл, SMPTE код времени.</span><span class="sxs-lookup"><span data-stu-id="f9792-121">To be able to search for SMPTE time stamps, you must first index the file by SMPTE time code.</span></span> <span data-ttu-id="f9792-122">Вы можете настроить индексатор для индексирования кодов времени с помощью метода [**IWMIndexer2:: Configure**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer2-configure) .</span><span class="sxs-lookup"><span data-stu-id="f9792-122">You can configure the indexer to index time codes by using the [**IWMIndexer2::Configure**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer2-configure) method.</span></span>

<span data-ttu-id="f9792-123">С помощью асинхронного модуля чтения можно перемещаться по файлу, SMPTE отметки времени с помощью методов интерфейса [**ивмреадертимекоде**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadertimecode) и метода [**IWMReaderAdvanced3:: стартатпоситион**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced3-startatposition) .</span><span class="sxs-lookup"><span data-stu-id="f9792-123">Using the asynchronous reader, you can navigate a file by SMPTE time stamps using the methods of the [**IWMReaderTimecode**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadertimecode) interface and the [**IWMReaderAdvanced3::StartAtPosition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced3-startatposition) method.</span></span> <span data-ttu-id="f9792-124">В синхронном модуле чтения используйте [**IWMSyncReader2:: сетранжебитимекоде**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setrangebytimecode).</span><span class="sxs-lookup"><span data-stu-id="f9792-124">With the synchronous reader, use [**IWMSyncReader2::SetRangeByTimecode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setrangebytimecode).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f9792-125">См. также</span><span class="sxs-lookup"><span data-stu-id="f9792-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9792-126">**Функции файлов ASF**</span><span class="sxs-lookup"><span data-stu-id="f9792-126">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="f9792-127">**Настройка расширений модуля данных**</span><span class="sxs-lookup"><span data-stu-id="f9792-127">**Configuring Data Unit Extensions**</span></span>](configuring-data-unit-extensions.md)
</dt> </dl>

 

 




