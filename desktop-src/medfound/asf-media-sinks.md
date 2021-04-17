---
description: Приемник мультимедиа ASF — это последний компонент в конвейере кодирования, позволяющий приложению записать файл ASF.
ms.assetid: 65bb8822-5eb0-46a3-ab9e-c55ae466e982
title: Приемники мультимедиа ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d6bcd3e6b91403185342607e8c4374eb32069c7
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105674551"
---
# <a name="asf-media-sinks"></a><span data-ttu-id="caa11-103">Приемники мультимедиа ASF</span><span class="sxs-lookup"><span data-stu-id="caa11-103">ASF Media Sinks</span></span>

<span data-ttu-id="caa11-104">Приемник мультимедиа ASF — это последний компонент в конвейере кодирования, позволяющий приложению записать файл ASF.</span><span class="sxs-lookup"><span data-stu-id="caa11-104">The ASF media sink is the final component in the encoding pipeline that enables an application to write an ASF file.</span></span>

<span data-ttu-id="caa11-105">Media Foundation предоставляет два типа приемников мультимедиа ASF:</span><span class="sxs-lookup"><span data-stu-id="caa11-105">Media Foundation provides two types of ASF media sinks:</span></span>

-   <span data-ttu-id="caa11-106">*Приемник файлов* ASF используется для архивации данных ASF Media в файл.</span><span class="sxs-lookup"><span data-stu-id="caa11-106">*ASF file sink* is used to archive ASF media data to a file.</span></span>
-   <span data-ttu-id="caa11-107">*Приемник потоковой передачи ASF* используется для записи содержимого ASF в байтовый поток, который можно передавать по сети.</span><span class="sxs-lookup"><span data-stu-id="caa11-107">*ASF streaming sink* is used to write ASF content in a byte stream that can be streamed across the network.</span></span>

<span data-ttu-id="caa11-108">Приемники мультимедиа ASF содержат один или несколько приемников потоков, которые представляют данные для записи для каждого потока в выходном файле ASF.</span><span class="sxs-lookup"><span data-stu-id="caa11-108">ASF media sinks contain one or more stream sinks, which represents the data to write for each stream in the output ASF file.</span></span> <span data-ttu-id="caa11-109">Для кодирования приложений, работающих в Windows Vista, необходимо вручную настроить топологию кодирования, создав и настроив приемник ASF Media, а затем добавив его в топологию.</span><span class="sxs-lookup"><span data-stu-id="caa11-109">For encoding applications that run on Windows Vista, you must manually configure the encoding topology by creating and configuring the ASF media sink and then adding it to the topology.</span></span> <span data-ttu-id="caa11-110">В Windows 7, если для создания топологии используются объекты быстрого перекодирования, вы не создаете приемник мультимедиа напрямую и приложение не вызывает никаких методов приемника носителя или любого приемника потока.</span><span class="sxs-lookup"><span data-stu-id="caa11-110">In Windows 7, if you are using the fast transcode objects to create the topology, you do not have create the media sink directly and the application does not call any methods on the media sink or any of the stream sinks.</span></span> <span data-ttu-id="caa11-111">Объекты быстрого перекодирования создают необходимые приемники носителей и добавляют их в топологию перед возвратом ссылки на вызывающее приложение.</span><span class="sxs-lookup"><span data-stu-id="caa11-111">The fast transcode objects instantiate the required media sinks and add it to the topology before returning a reference to the caller application.</span></span> <span data-ttu-id="caa11-112">Однако для быстрого преобразования объектов существуют некоторые ограничения, применяемые в зависимости от типа кодировки.</span><span class="sxs-lookup"><span data-stu-id="caa11-112">However for fast transcode objects, there are some restrictions that apply depending on the type of encoding.</span></span>

-   [<span data-ttu-id="caa11-113">Объектная модель приемника ASF Media</span><span class="sxs-lookup"><span data-stu-id="caa11-113">ASF Media Sink Object Model</span></span>](#asf-media-sink-object-model)
-   [<span data-ttu-id="caa11-114">Приемник файлов ASF</span><span class="sxs-lookup"><span data-stu-id="caa11-114">ASF File Sink</span></span>](#asf-file-sink)
-   [<span data-ttu-id="caa11-115">См. также</span><span class="sxs-lookup"><span data-stu-id="caa11-115">Related topics</span></span>](#related-topics)

## <a name="asf-media-sink-object-model"></a><span data-ttu-id="caa11-116">Объектная модель приемника ASF Media</span><span class="sxs-lookup"><span data-stu-id="caa11-116">ASF Media Sink Object Model</span></span>

<span data-ttu-id="caa11-117">Приемники мультимедиа ASF реализуют интерфейс [**имфмедиасинк**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) и предоставляют следующие интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="caa11-117">ASF media sinks implement the [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) interface and exposes the following interfaces.</span></span> <span data-ttu-id="caa11-118">Приложение может получить ссылку на эти интерфейсы, вызвав [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) в приемнике ASF Media, который используется для создания выходных образцов.</span><span class="sxs-lookup"><span data-stu-id="caa11-118">An application can get a reference to these interfaces by calling [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the ASF media sink it is using for generating output samples.</span></span>



| <span data-ttu-id="caa11-119">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="caa11-119">Interface</span></span>                                                  | <span data-ttu-id="caa11-120">Описание</span><span class="sxs-lookup"><span data-stu-id="caa11-120">Description</span></span>                                                                                                                                                                                            |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="caa11-121">**имфмедиасинк**</span><span class="sxs-lookup"><span data-stu-id="caa11-121">**IMFMediaSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)                       | <span data-ttu-id="caa11-122">Требуется для всех приемников мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="caa11-122">Required for all media sinks.</span></span>                                                                                                                                                                          |
| [<span data-ttu-id="caa11-123">**имффинализаблемедиасинк**</span><span class="sxs-lookup"><span data-stu-id="caa11-123">**IMFFinalizableMediaSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imffinalizablemediasink) | <span data-ttu-id="caa11-124">Реализуется приемником файлов ASF, который записывает сгенерированное мультимедийное содержимое в файл.</span><span class="sxs-lookup"><span data-stu-id="caa11-124">Implemented by the ASF file sink that writes the generated media content to a file.</span></span> <span data-ttu-id="caa11-125">Можно использовать методы этого интерфейса для сброса данных и обновления объекта заголовка ASF для окончательного выходного файла.</span><span class="sxs-lookup"><span data-stu-id="caa11-125">You can use the methods on this interface to flush data and update the ASF Header Object of the final output file.</span></span> |
| [<span data-ttu-id="caa11-126">**имфклоккстатесинк**</span><span class="sxs-lookup"><span data-stu-id="caa11-126">**IMFClockStateSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)             | <span data-ttu-id="caa11-127">Получает уведомления об изменении состояния с часов презентации.</span><span class="sxs-lookup"><span data-stu-id="caa11-127">Receives state-change notifications from the presentation clock.</span></span>                                                                                                                                       |
| [<span data-ttu-id="caa11-128">**имфасфконтентинфо**</span><span class="sxs-lookup"><span data-stu-id="caa11-128">**IMFASFContentInfo**</span></span>](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo)             | <span data-ttu-id="caa11-129">Объект ASF Контентинфо — это объект уровня Вмконтаинер, в основном хранящий сведения о объекте заголовка ASF.</span><span class="sxs-lookup"><span data-stu-id="caa11-129">The ASF ContentInfo object is a WMContainer level object that mainly stores ASF Header Object information.</span></span> <span data-ttu-id="caa11-130">Используется для создания приемников мультимедиа ASF.</span><span class="sxs-lookup"><span data-stu-id="caa11-130">This is used to create ASF media sinks.</span></span>                                                     |
| [<span data-ttu-id="caa11-131">**имфметадата**</span><span class="sxs-lookup"><span data-stu-id="caa11-131">**IMFMetadata**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata)                         | <span data-ttu-id="caa11-132">Используется для описания метаданных файла ASF.</span><span class="sxs-lookup"><span data-stu-id="caa11-132">Used to describe the metadata for the ASF file.</span></span>                                                                                                                                                        |
| [<span data-ttu-id="caa11-133">**имфметадатапровидер**</span><span class="sxs-lookup"><span data-stu-id="caa11-133">**IMFMetadataProvider**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider)         | <span data-ttu-id="caa11-134">Извлекает коллекцию метаданных либо для всей презентации, либо для одного потока в презентации.</span><span class="sxs-lookup"><span data-stu-id="caa11-134">Retrieves a collection of metadata, either for an entire presentation, or for one stream in the presentation.</span></span>                                                                                          |



 

## <a name="asf-file-sink"></a><span data-ttu-id="caa11-135">Приемник файлов ASF</span><span class="sxs-lookup"><span data-stu-id="caa11-135">ASF File Sink</span></span>

<span data-ttu-id="caa11-136">Приемник ASF-файлов — это реализация [**имфмедиасинк**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) , предоставляемая Media Foundation, которую приложение может использовать для архивации данных ASF Media в файл.</span><span class="sxs-lookup"><span data-stu-id="caa11-136">The ASF file sink is an implementation of [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) provided by Media Foundation that an application can use to archive ASF media data to a file.</span></span>

<span data-ttu-id="caa11-137">Необходимо создать, настроить и вызвать методы для приемника файла или любого из его приемников потока, если вы используете объекты уровня конвейера для записи нового ASF-файла.</span><span class="sxs-lookup"><span data-stu-id="caa11-137">You need to create, configure, and call methods on the file sink or any of its stream sinks if you are using the pipeline layer objects to write a new ASF file.</span></span> <span data-ttu-id="caa11-138">После настройки приемника файла его можно добавить в конвейер кодирования.</span><span class="sxs-lookup"><span data-stu-id="caa11-138">After configuring the file sink you can then add it to the encoding pipeline.</span></span>

<span data-ttu-id="caa11-139">Ниже приведены общие действия по использованию приемника файлов ASF.</span><span class="sxs-lookup"><span data-stu-id="caa11-139">Here are the general steps for using the ASF file sink:</span></span>

1.  <span data-ttu-id="caa11-140">Создайте приемник файлов в процессе или вне процесса.</span><span class="sxs-lookup"><span data-stu-id="caa11-140">Create the file sink in-process or out-of-process.</span></span>
2.  <span data-ttu-id="caa11-141">Настройте приемник файлов со всеми потоками, свойствами кодировки и метаданными.</span><span class="sxs-lookup"><span data-stu-id="caa11-141">Configure the file sink with all the streams, encoding properties, and metadata information.</span></span>
3.  <span data-ttu-id="caa11-142">Свяжите приемник файла с узлом выходной топологии либо путем перечисления приемников потока, либо путем отслеживания номеров потоков в приемнике.</span><span class="sxs-lookup"><span data-stu-id="caa11-142">Associate the file sink with the output topology node either by enumerating the stream sinks or by keeping track of the stream numbers with in the sink.</span></span>

<span data-ttu-id="caa11-143">В следующих разделах содержатся подробные сведения о работе с приемником файлов ASF.</span><span class="sxs-lookup"><span data-stu-id="caa11-143">The following topics contain detailed information about working with the ASF file sink:</span></span>

-   [<span data-ttu-id="caa11-144">Создание приемника файлов ASF</span><span class="sxs-lookup"><span data-stu-id="caa11-144">Creating the ASF File Sink</span></span>](creating-the-asf-file-sink.md)
-   [<span data-ttu-id="caa11-145">Добавление потоковой информации в приемник файлов ASF</span><span class="sxs-lookup"><span data-stu-id="caa11-145">Adding Stream Information to the ASF File Sink</span></span>](adding-stream-information-to-the-asf-file-sink.md)
-   [<span data-ttu-id="caa11-146">Задание свойств в приемнике файла</span><span class="sxs-lookup"><span data-stu-id="caa11-146">Setting Properties in the File Sink</span></span>](setting-properties-in-the-file-sink.md)
-   [<span data-ttu-id="caa11-147">Добавление метаданных в приемник файлов</span><span class="sxs-lookup"><span data-stu-id="caa11-147">Adding Metadata to the File Sink</span></span>](adding-metadata-to-the-file-sink.md)
-   [<span data-ttu-id="caa11-148">Модель буфера для контейнера утечки</span><span class="sxs-lookup"><span data-stu-id="caa11-148">The Leaky Bucket Buffer Model</span></span>](the-leaky-bucket-buffer-model.md)

## <a name="related-topics"></a><span data-ttu-id="caa11-149">См. также</span><span class="sxs-lookup"><span data-stu-id="caa11-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="caa11-150">Компоненты ASF уровня конвейера</span><span class="sxs-lookup"><span data-stu-id="caa11-150">Pipeline Layer ASF Components</span></span>](pipeline-layer-asf-components.md)
</dt> <dt>

[<span data-ttu-id="caa11-151">Поддержка ASF в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="caa11-151">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 
