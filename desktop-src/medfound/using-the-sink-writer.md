---
description: Использование модуля записи приемника
ms.assetid: BE89E2E0-711F-4BD5-BB86-AA4CCA2D3E7F
title: Использование модуля записи приемника
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa4fa472bd1a5121454b3ffb06def7082508432b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110492"
---
# <a name="using-the-sink-writer"></a><span data-ttu-id="f852b-103">Использование модуля записи приемника</span><span class="sxs-lookup"><span data-stu-id="f852b-103">Using the Sink Writer</span></span>

## <a name="overview"></a><span data-ttu-id="f852b-104">Обзор</span><span class="sxs-lookup"><span data-stu-id="f852b-104">Overview</span></span>

### <a name="file-container-types"></a><span data-ttu-id="f852b-105">Типы контейнеров файлов</span><span class="sxs-lookup"><span data-stu-id="f852b-105">File Container Types</span></span>

<span data-ttu-id="f852b-106">Модуль записи приемников имеет встроенную поддержку нескольких типов контейнеров файлов.</span><span class="sxs-lookup"><span data-stu-id="f852b-106">The sink writer has built-in support for several file container types.</span></span> <span data-ttu-id="f852b-107">Полный список см. в разделе [MF \_ \_ контаинертипе](mf-transcode-containertype.md).</span><span class="sxs-lookup"><span data-stu-id="f852b-107">For a complete list, see [MF\_TRANSCODE\_CONTAINERTYPE](mf-transcode-containertype.md).</span></span> <span data-ttu-id="f852b-108">Вы можете поддерживать дополнительные типы контейнеров, написав пользовательский [приемник мультимедиа](media-sinks.md).</span><span class="sxs-lookup"><span data-stu-id="f852b-108">You can support additional container types by writing a custom [media sink](media-sinks.md).</span></span> <span data-ttu-id="f852b-109">Файловый контейнер указывается при создании нового экземпляра модуля записи приемника.</span><span class="sxs-lookup"><span data-stu-id="f852b-109">The file container is specified when you create a new instance of the sink writer.</span></span>

### <a name="stream-formats"></a><span data-ttu-id="f852b-110">Форматы потоков</span><span class="sxs-lookup"><span data-stu-id="f852b-110">Stream Formats</span></span>

<span data-ttu-id="f852b-111">Для каждого потока приложение должно указать следующее.</span><span class="sxs-lookup"><span data-stu-id="f852b-111">For each stream, the application must specify the following.</span></span>

-   <span data-ttu-id="f852b-112">*Формат входных данных* — это формат, который приложение отправляет в модуль записи приемника.</span><span class="sxs-lookup"><span data-stu-id="f852b-112">The *input format* is the format that the application sends to the sink writer.</span></span>
-   <span data-ttu-id="f852b-113">*Формат выходных данных* — это формат, который будет записан в файл.</span><span class="sxs-lookup"><span data-stu-id="f852b-113">The *output format* is the format that will be written to the file.</span></span>

<span data-ttu-id="f852b-114">Форматы входных и выходных данных могут быть либо сжатыми, либо несжатыми.</span><span class="sxs-lookup"><span data-stu-id="f852b-114">The input and output formats can be either compressed or uncompressed.</span></span> <span data-ttu-id="f852b-115">Модуль записи приемника поддерживает следующие сочетания:</span><span class="sxs-lookup"><span data-stu-id="f852b-115">The sink writer supports the following combinations:</span></span>

-   <span data-ttu-id="f852b-116">Несжатые входные данные с сжатыми выходными данными.</span><span class="sxs-lookup"><span data-stu-id="f852b-116">Uncompressed input with compressed output.</span></span> <span data-ttu-id="f852b-117">Это типичный случай и используется для сценариев кодирования или кодирования.</span><span class="sxs-lookup"><span data-stu-id="f852b-117">This is the typical case, and is used for encoding or transcoding scenarios.</span></span> <span data-ttu-id="f852b-118">Должен быть доступен кодировщик Microsoft Media Foundation, который принимает входной тип и кодирует в выходной тип.</span><span class="sxs-lookup"><span data-stu-id="f852b-118">A Microsoft Media Foundation encoder must be available that accepts the input type and encodes to the output type.</span></span>
-   <span data-ttu-id="f852b-119">Сжатые входные данные с одинаковыми выходными данными.</span><span class="sxs-lookup"><span data-stu-id="f852b-119">Compressed input with identical output.</span></span> <span data-ttu-id="f852b-120">Используйте это сочетание для ремукс файла без перекодирования.</span><span class="sxs-lookup"><span data-stu-id="f852b-120">Use this combination to remux a file without transcoding.</span></span>
-   <span data-ttu-id="f852b-121">Несжатые входные данные с одинаковыми выходными данными.</span><span class="sxs-lookup"><span data-stu-id="f852b-121">Uncompressed input with identical output.</span></span> <span data-ttu-id="f852b-122">Используйте это сочетание для записи несжатого аудио-или видеофайла в контейнер файлов.</span><span class="sxs-lookup"><span data-stu-id="f852b-122">Use this combination to write uncompressed audio or video to a file container.</span></span>

<span data-ttu-id="f852b-123">Модуль записи приемника не поддерживает изменение размера видео, преобразование кадров или интерполяцию звука, если только эти функции не предоставляются кодировщиком.</span><span class="sxs-lookup"><span data-stu-id="f852b-123">The sink writer does not support video resizing, frame-rate conversion, or audio resampling, unless these functions are provided by the encoder.</span></span> <span data-ttu-id="f852b-124">В противном случае приложение может использовать [обработчики цифровых сигналов](windowsmediadigitalsignalprocessors.md) для преобразования входных данных перед их отправкой в</span><span class="sxs-lookup"><span data-stu-id="f852b-124">Otherwise, the application can use [Digital Signal Processors](windowsmediadigitalsignalprocessors.md) to convert the input data, before sending the data to the</span></span>

## <a name="creating-the-sink-writer"></a><span data-ttu-id="f852b-125">Создание модуля записи приемника</span><span class="sxs-lookup"><span data-stu-id="f852b-125">Creating the Sink Writer</span></span>

<span data-ttu-id="f852b-126">Существует две функции, которые создают модуль записи приемника:</span><span class="sxs-lookup"><span data-stu-id="f852b-126">There are two functions that create the sink writer:</span></span>

-   <span data-ttu-id="f852b-127">[**Мфкреатесинквритерфромурл**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) принимает URL-адрес выходного файла или указатель на байтовый поток.</span><span class="sxs-lookup"><span data-stu-id="f852b-127">[**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) takes the URL of an output file or a pointer to a byte stream.</span></span> <span data-ttu-id="f852b-128">Эта функция создает приемник мультимедиа внутренним образом.</span><span class="sxs-lookup"><span data-stu-id="f852b-128">This function creates the media sink internally.</span></span>
-   <span data-ttu-id="f852b-129">[**Мфкреатесинквритерфроммедиасинк**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink) принимает указатель на приемник мультимедиа, который уже был создан приложением.</span><span class="sxs-lookup"><span data-stu-id="f852b-129">[**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink) takes a pointer to a media sink that has already been created by the application.</span></span>

<span data-ttu-id="f852b-130">Если вы используете один из встроенных приемников носителей, лучше использовать функцию [**мфкреатесинквритерфромурл**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) , так как вызывающему объекту не нужно настраивать приемник мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="f852b-130">If you are using one of the built-in media sinks, the [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) function is preferable, because the caller does not need to configure the media sink.</span></span>

<span data-ttu-id="f852b-131">Метод [**мфкреатесинквритерфромурл**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) предоставляет несколько параметров для указания типа контейнера файлов.</span><span class="sxs-lookup"><span data-stu-id="f852b-131">The [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) method provides several options for specifying the type of file container.</span></span> <span data-ttu-id="f852b-132">В самом простом случае функция использует расширение имени файла в URL-адресе для выбора контейнера файлов.</span><span class="sxs-lookup"><span data-stu-id="f852b-132">In the simplest case, the function uses the file name extension in the URL to select the file container.</span></span> <span data-ttu-id="f852b-133">Дополнительные сведения см. на странице справки по функциям.</span><span class="sxs-lookup"><span data-stu-id="f852b-133">For details, refer to the function reference page.</span></span>

<span data-ttu-id="f852b-134">Например, следующий код задает имя файла Output. WMV для URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="f852b-134">For example, the following code specifies the file name "output.wmv" for the URL.</span></span> <span data-ttu-id="f852b-135">На основе расширения имени файла модуль записи приемника загрузит [приемник мультимедиа ASF](asf-media-sinks.md) для создания файла ASF.</span><span class="sxs-lookup"><span data-stu-id="f852b-135">Based on the file name extension, the sink writer will load the [ASF Media Sink](asf-media-sinks.md) to create an Advanced Systems Format (ASF) file.</span></span>


```C++
    HRESULT hr = MFCreateSinkWriterFromURL(L"output.wmv", NULL, NULL, &pSinkWriter);
```



<span data-ttu-id="f852b-136">В случае с [**мфкреатесинквритерфроммедиасинк**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)тип файла определяется приемником мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="f852b-136">In the case of [**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink), the file type is determined by the media sink.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f852b-137">Связанные разделы</span><span class="sxs-lookup"><span data-stu-id="f852b-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f852b-138">Модуль записи приемников</span><span class="sxs-lookup"><span data-stu-id="f852b-138">Sink Writer</span></span>](sink-writer.md)
</dt> </dl>

 

 



