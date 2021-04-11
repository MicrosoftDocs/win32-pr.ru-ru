---
description: Пример Асфпарсер
ms.assetid: 6be1e12f-7d4a-4564-88ae-14fd71fd2cf9
title: Пример Асфпарсер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c159b481e22d77b0bee9adccbbb74073398c12b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262823"
---
# <a name="asfparser-sample"></a><span data-ttu-id="da538-103">Пример Асфпарсер</span><span class="sxs-lookup"><span data-stu-id="da538-103">ASFParser Sample</span></span>

<span data-ttu-id="da538-104">Показывает, как анализировать данные из ASF-файла с помощью компонентов ASF нижнего уровня в Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="da538-104">Shows how to parse data from an Advanced Systems Format (ASF) file by using the low-level ASF components in Media Foundation.</span></span> <span data-ttu-id="da538-105">В этом примере демонстрируются следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="da538-105">The sample demonstrates the following tasks:</span></span>

-   <span data-ttu-id="da538-106">Перечисление потоков аудио и видео в файле ASF.</span><span class="sxs-lookup"><span data-stu-id="da538-106">Enumerating the audio and video streams in an ASF file.</span></span>
-   <span data-ttu-id="da538-107">Выбор аудио-или видеопотока для анализа.</span><span class="sxs-lookup"><span data-stu-id="da538-107">Selecting an audio or a video stream for parsing.</span></span>
-   <span data-ttu-id="da538-108">Поиск пакета в требуемое время воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="da538-108">Seeking to a packet at a desired playback time.</span></span>
-   <span data-ttu-id="da538-109">Создание сжатых образцов для выбранного потока.</span><span class="sxs-lookup"><span data-stu-id="da538-109">Generating compressed samples for the selected stream.</span></span>
-   <span data-ttu-id="da538-110">Декодирование образцов аудио и видео.</span><span class="sxs-lookup"><span data-stu-id="da538-110">Decoding audio and video samples.</span></span>

## <a name="apis-demonstrated"></a><span data-ttu-id="da538-111">Продемонстрированные API</span><span class="sxs-lookup"><span data-stu-id="da538-111">APIs Demonstrated</span></span>

<span data-ttu-id="da538-112">В этом образце демонстрируются следующие интерфейсы Microsoft Media Foundation:</span><span class="sxs-lookup"><span data-stu-id="da538-112">This sample demonstrates the following Microsoft Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="da538-113">**имфасфконтентинфо**</span><span class="sxs-lookup"><span data-stu-id="da538-113">**IMFASFContentInfo**</span></span>](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo)
-   [<span data-ttu-id="da538-114">**имфасфиндексер**</span><span class="sxs-lookup"><span data-stu-id="da538-114">**IMFASFIndexer**</span></span>](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer)
-   [<span data-ttu-id="da538-115">**имфасфсплиттер**</span><span class="sxs-lookup"><span data-stu-id="da538-115">**IMFASFSplitter**</span></span>](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter)

## <a name="usage"></a><span data-ttu-id="da538-116">Использование</span><span class="sxs-lookup"><span data-stu-id="da538-116">Usage</span></span>

1.  <span data-ttu-id="da538-117">Чтобы открыть файл ASF, нажмите кнопку " **Открыть файл мультимедиа...** ".</span><span class="sxs-lookup"><span data-stu-id="da538-117">To open an ASF file, click the **Open Media File...** button.</span></span>
2.  <span data-ttu-id="da538-118">Выберите файл ASF и нажмите кнопку **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="da538-118">Select an ASF file and click **Open**.</span></span> <span data-ttu-id="da538-119">Сведения о файле отображаются на **информационной** панели.</span><span class="sxs-lookup"><span data-stu-id="da538-119">Information about the file is shown on the **Information** pane.</span></span>
3.  <span data-ttu-id="da538-120">В разделе **Конфигурация средства синтаксического анализа** выберите поток для синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="da538-120">Under **Parser Configuration**, select a stream to parse.</span></span>
4.  <span data-ttu-id="da538-121">Чтобы создать образцы в обратную, выберите **обратить**.</span><span class="sxs-lookup"><span data-stu-id="da538-121">To generate samples in reverse, select **Reverse**.</span></span>
5.  <span data-ttu-id="da538-122">Чтобы указать начальную точку, перетащите ползунок в нужное место.</span><span class="sxs-lookup"><span data-stu-id="da538-122">To specify the start point, drag the slider to the desired location.</span></span>
6.  <span data-ttu-id="da538-123">Чтобы начать анализ, нажмите кнопку **создать образцы** .</span><span class="sxs-lookup"><span data-stu-id="da538-123">To begin parsing, click the **Generate Samples** button.</span></span> <span data-ttu-id="da538-124">Сведения о примерах показаны на **информационной** панели.</span><span class="sxs-lookup"><span data-stu-id="da538-124">Information about the samples is shown on the **Information** pane.</span></span>
7.  <span data-ttu-id="da538-125">Чтобы проверить образцы для аудиопотока, нажмите кнопку **тестовый звук** .</span><span class="sxs-lookup"><span data-stu-id="da538-125">To test the samples for the audio stream, click the **Test Audio** button.</span></span>
8.  <span data-ttu-id="da538-126">Чтобы проверить образцы для видеопотока, нажмите кнопку **Показывать растровое изображение** .</span><span class="sxs-lookup"><span data-stu-id="da538-126">To test the samples for the video stream, click the **Show Bitmap** button.</span></span>

## <a name="requirements"></a><span data-ttu-id="da538-127">Требования</span><span class="sxs-lookup"><span data-stu-id="da538-127">Requirements</span></span>



| <span data-ttu-id="da538-128">Продукт</span><span class="sxs-lookup"><span data-stu-id="da538-128">Product</span></span>                                                        | <span data-ttu-id="da538-129">Version</span><span class="sxs-lookup"><span data-stu-id="da538-129">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="da538-130">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="da538-130">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="da538-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="da538-131">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="da538-132">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="da538-132">Downloading the Sample</span></span>

<span data-ttu-id="da538-133">Этот пример доступен в [репозитории GitHub с классическими примерами Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/asfparser).</span><span class="sxs-lookup"><span data-stu-id="da538-133">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/asfparser).</span></span>

## <a name="related-topics"></a><span data-ttu-id="da538-134">См. также</span><span class="sxs-lookup"><span data-stu-id="da538-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da538-135">Примеры пакетов SDK Media Foundation</span><span class="sxs-lookup"><span data-stu-id="da538-135">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

[<span data-ttu-id="da538-136">Поддержка ASF в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="da538-136">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="da538-137">Руководство. чтение файла ASF</span><span class="sxs-lookup"><span data-stu-id="da538-137">Tutorial: Reading an ASF File</span></span>](tutorial--reading-an-asf-file.md)
</dt> <dt>

[<span data-ttu-id="da538-138">Компоненты ASF Вмконтаинер</span><span class="sxs-lookup"><span data-stu-id="da538-138">WMContainer ASF Components</span></span>](wmcontainer-asf-components.md)
</dt> </dl>

 

 



