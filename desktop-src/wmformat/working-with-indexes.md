---
title: Работа с индексами
description: Работа с индексами
ms.assetid: 7daa4b29-0597-462d-ad65-135d0ef7362d
keywords:
- Пакет SDK для формата Windows Media, индексы
- Расширенный системный формат (ASF), индексы
- ASF (Расширенный системный формат), индексы
- индексы, сведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34057046223daf2e16950e0e38b1b0db5df32c4a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888000"
---
# <a name="working-with-indexes"></a><span data-ttu-id="c58ba-107">Работа с индексами</span><span class="sxs-lookup"><span data-stu-id="c58ba-107">Working with Indexes</span></span>

<span data-ttu-id="c58ba-108">Пакет SDK для формата Windows Media поддерживает поиск и стридинг содержимого.</span><span class="sxs-lookup"><span data-stu-id="c58ba-108">The Windows Media Format SDK supports seeking and striding through content.</span></span> <span data-ttu-id="c58ba-109">Поиск позволяет указать место на временной шкале файла, чтобы начать воспроизведение.</span><span class="sxs-lookup"><span data-stu-id="c58ba-109">Seeking enables you to specify a place on the file's timeline to begin playback.</span></span> <span data-ttu-id="c58ba-110">Стридинг позволяет быстро пересылать и перематывать выходные данные файла.</span><span class="sxs-lookup"><span data-stu-id="c58ba-110">Striding enables you to fast-forward and rewind the output of a file.</span></span> <span data-ttu-id="c58ba-111">Чтобы воспользоваться преимуществами этих функций, необходимо индексировать файлы.</span><span class="sxs-lookup"><span data-stu-id="c58ba-111">Files must be indexed to take advantage of these features.</span></span> <span data-ttu-id="c58ba-112">Индекс представляет собой ряд значений, представляющих позиции в файле (время презентации, Номера кадров или коды времени SMTP) с соответствующими смещениями в разделе данных файла для каждого.</span><span class="sxs-lookup"><span data-stu-id="c58ba-112">An index is a series of values representing positions in the file (either presentation times, frame numbers, or SMTPE time codes) with corresponding offsets into the data section of the file for each.</span></span> <span data-ttu-id="c58ba-113">Индексация наиболее важна для видеопотоков, так как можно легко оценить время презентации в виде звукового потока.</span><span class="sxs-lookup"><span data-stu-id="c58ba-113">Indexing is most important for video streams, as audio stream presentation time can be easily estimated.</span></span> <span data-ttu-id="c58ba-114">Однако для некоторых звуковых потоков также могут потребоваться индексы.</span><span class="sxs-lookup"><span data-stu-id="c58ba-114">However, some audio streams may require indexes as well.</span></span> <span data-ttu-id="c58ba-115">По умолчанию модуль записи будет индексировать каждый новый ASF файл.</span><span class="sxs-lookup"><span data-stu-id="c58ba-115">By default, the writer will index every new ASF file.</span></span> <span data-ttu-id="c58ba-116">Если в содержимое файла вносятся изменения, необходимо вручную обновить индекс с помощью объекта индексатора.</span><span class="sxs-lookup"><span data-stu-id="c58ba-116">If changes are made to the content of a file, you must refresh the index yourself using the indexer object.</span></span>

<span data-ttu-id="c58ba-117">Индексатор поддерживает как временные, так и основанные на кадрах индексирование, а также индексирование на основе кодов времени SMPTE (если они есть).</span><span class="sxs-lookup"><span data-stu-id="c58ba-117">The indexer supports both temporal and frame-based indexing as well as indexing based on SMPTE time codes (if present).</span></span> <span data-ttu-id="c58ba-118">Модуль записи по умолчанию создаст временный индекс для каждого нового видеопотока, закодированного в файл.</span><span class="sxs-lookup"><span data-stu-id="c58ba-118">The writer will create a temporal index by default for every new video stream encoded to a file.</span></span> <span data-ttu-id="c58ba-119">Необходимо явно настроить и вызвать индексатор, чтобы создать индекс кода времени на основе кадров или SMPTE.</span><span class="sxs-lookup"><span data-stu-id="c58ba-119">You must explicitly configure and call the indexer to create a frame-based or SMPTE time code index.</span></span>

<span data-ttu-id="c58ba-120">При внесении изменений в содержимое файла ASF его необходимо индексировать повторно.</span><span class="sxs-lookup"><span data-stu-id="c58ba-120">When changes are made to the content of an ASF file, it must be indexed again.</span></span>

<span data-ttu-id="c58ba-121">В следующих разделах приведен пример кода для выполнения стандартных задач индексирования.</span><span class="sxs-lookup"><span data-stu-id="c58ba-121">The following sections present example code for performing common indexing tasks.</span></span>

-   [<span data-ttu-id="c58ba-122">Отключение автоматического индексирования</span><span class="sxs-lookup"><span data-stu-id="c58ba-122">To Disable Automatic Indexing</span></span>](to-disable-automatic-indexing.md)
-   [<span data-ttu-id="c58ba-123">Настройка индексатора</span><span class="sxs-lookup"><span data-stu-id="c58ba-123">To Configure the Indexer</span></span>](to-configure-the-indexer.md)
-   [<span data-ttu-id="c58ba-124">Индексирование файла ASF</span><span class="sxs-lookup"><span data-stu-id="c58ba-124">To Index an ASF File</span></span>](to-index-an-asf-file.md)
-   [<span data-ttu-id="c58ba-125">Завершение индексирования</span><span class="sxs-lookup"><span data-stu-id="c58ba-125">To Stop Indexing in Progress</span></span>](to-stop-indexing-in-progress.md)

<span data-ttu-id="c58ba-126">Кроме того, пример приложения Дскопи иллюстрирует использование индексатора.</span><span class="sxs-lookup"><span data-stu-id="c58ba-126">In addition, the DSCopy sample application illustrates the use of the indexer.</span></span> <span data-ttu-id="c58ba-127">Дополнительные сведения см. в разделе [примеры приложений](sample-applications.md).</span><span class="sxs-lookup"><span data-stu-id="c58ba-127">For more information, see [Sample Applications](sample-applications.md).</span></span>

 

 




