---
description: В этом разделе описывается поддержка метаданных о создании образов, предоставляемая компонентом Windows Imaging Component (WIC).
ms.assetid: 35727810-3c4c-4c11-a4a2-3ae2cf3b8142
title: Общие сведения о метаданных компонента WIC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f00e3a77eb74a3fb4a00db05ef9e00028f02ecf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104570597"
---
# <a name="wic-metadata-overview"></a><span data-ttu-id="d4802-103">Общие сведения о метаданных компонента WIC</span><span class="sxs-lookup"><span data-stu-id="d4802-103">WIC Metadata Overview</span></span>

<span data-ttu-id="d4802-104">В этом разделе описывается поддержка метаданных о создании образов, предоставляемая компонентом Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="d4802-104">This topic introduces the imaging metadata support provided by the Windows Imaging Component (WIC).</span></span> <span data-ttu-id="d4802-105">Он содержит вводные сведения о чтении и записи метаданных изображений, языке запросов метаданных и расширяемости обработчика метаданных.</span><span class="sxs-lookup"><span data-stu-id="d4802-105">It provides an introduction to reading and writing image metadata, the metadata query language, and metadata handler extensibility.</span></span>

<span data-ttu-id="d4802-106">Метаданные образа — это данные, внедренные в файл изображения, который предоставляет дополнительные сведения о изображении, например устройство, используемое для записи изображения или размеры изображения.</span><span class="sxs-lookup"><span data-stu-id="d4802-106">Image metadata is data embedded inside an image file that provides additional information about the image, such as the device used to capture the image or the dimensions of the image.</span></span> <span data-ttu-id="d4802-107">Хотя он содержится в самом файле образа, эти метаданные не являются частью данных отрисовки.</span><span class="sxs-lookup"><span data-stu-id="d4802-107">Although it is contained within the image file itself, this metadata is not part of the rendering data.</span></span> <span data-ttu-id="d4802-108">Компонент WIC предоставляет интерфейсы, позволяющие считывать и записывать эти метаданные для нескольких распространенных форматов метаданных, в том числе расширяемой платформы метаданных (XMP), файла с обменом изображениями (EXIF) и текстовых данных PNG (текст).</span><span class="sxs-lookup"><span data-stu-id="d4802-108">WIC provides interfaces that enable you to read and write this metadata for several common metadata formats including Extensible Metadata Platform (XMP), Exchangeable Image File (EXIF), and Png Textual Data (tEXt).</span></span>

<span data-ttu-id="d4802-109">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="d4802-109">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="d4802-110">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="d4802-110">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="d4802-111">Введение</span><span class="sxs-lookup"><span data-stu-id="d4802-111">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="d4802-112">Чтение метаданных изображения</span><span class="sxs-lookup"><span data-stu-id="d4802-112">Reading Image Metadata</span></span>](#reading-image-metadata)
-   [<span data-ttu-id="d4802-113">Запись метаданных образа</span><span class="sxs-lookup"><span data-stu-id="d4802-113">Writing Image Metadata</span></span>](#writing-image-metadata)
-   [<span data-ttu-id="d4802-114">Расширяемость метаданных</span><span class="sxs-lookup"><span data-stu-id="d4802-114">Metadata Extensibility</span></span>](#metadata-extensibility)
-   [<span data-ttu-id="d4802-115">Поддерживаемые форматы метаданных</span><span class="sxs-lookup"><span data-stu-id="d4802-115">Supported Metadata Formats</span></span>](#supported-metadata-formats)
-   [<span data-ttu-id="d4802-116">Сводка компонента метаданных</span><span class="sxs-lookup"><span data-stu-id="d4802-116">Metadata Component Summary</span></span>](#metadata-component-summary)
-   [<span data-ttu-id="d4802-117">См. также</span><span class="sxs-lookup"><span data-stu-id="d4802-117">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="d4802-118">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="d4802-118">Prerequisites</span></span>

<span data-ttu-id="d4802-119">Чтобы понять этот раздел, необходимо ознакомиться с интерфейсами кодировщика и декодера WIC и связанных с ним компонентов модели COM, как описано в разделе [Общие сведения о компоненте создания образов Windows](-wic-about-windows-imaging-codec.md).</span><span class="sxs-lookup"><span data-stu-id="d4802-119">To understand this topic, you should be familiar with the WIC encoder and decoder interfaces and their related Component Object Model (COM) components, as described in the [Windows Imaging Component Overview](-wic-about-windows-imaging-codec.md).</span></span> <span data-ttu-id="d4802-120">Кроме того, он позволяет получить общее представление о некоторых используемых в настоящее время форматах метаданных образов.</span><span class="sxs-lookup"><span data-stu-id="d4802-120">It also helps to have a general familiarity with some of the imaging metadata formats in use today.</span></span>

## <a name="introduction"></a><span data-ttu-id="d4802-121">Введение</span><span class="sxs-lookup"><span data-stu-id="d4802-121">Introduction</span></span>

<span data-ttu-id="d4802-122">Метаданные предоставляют расширенные сведения о изображении.</span><span class="sxs-lookup"><span data-stu-id="d4802-122">Metadata provides extended information about an image.</span></span> <span data-ttu-id="d4802-123">Эти сведения можно использовать несколькими способами.</span><span class="sxs-lookup"><span data-stu-id="d4802-123">This information can be used in several ways.</span></span> <span data-ttu-id="d4802-124">Изображение может содержать такие метаданные, как описание, оценка, Теги категорий и сведения об авторских правах.</span><span class="sxs-lookup"><span data-stu-id="d4802-124">An image might contain metadata such as a description, rating, category tags, and copyright information.</span></span> <span data-ttu-id="d4802-125">Доступ к метаданным упрощает выполнение таких задач, как управление ресурсами, расположение файлов или определение сведений об авторских правах.</span><span class="sxs-lookup"><span data-stu-id="d4802-125">Accessing the metadata makes it easier to perform tasks such as asset management, file location, or determining copyright information.</span></span> <span data-ttu-id="d4802-126">Например, фотоальбом Windows в Windows Vista позволяет добавлять описания и Теги категорий к изображениям.</span><span class="sxs-lookup"><span data-stu-id="d4802-126">For example, the Windows Photo Gallery in Windows Vista enables you to add descriptions and category tags to images.</span></span> <span data-ttu-id="d4802-127">Это обеспечивает более эффективное обнаружение изображений и удобный способ классификации изображений.</span><span class="sxs-lookup"><span data-stu-id="d4802-127">This allows for better discoverability of images and a convenient way to categorize images.</span></span> <span data-ttu-id="d4802-128">Используя API-интерфейсы WIC и общие форматы метаданных, приложения могут легко записывать или читать метаданные этого типа в изображениях или из них.</span><span class="sxs-lookup"><span data-stu-id="d4802-128">Using the WIC APIs and common metadata formats, applications can easily write or read this type of metadata to or from images.</span></span>

<span data-ttu-id="d4802-129">На следующей диаграмме показано содержимое файла JPEG, содержащего внедренные блоки метаданных и элементы метаданных.</span><span class="sxs-lookup"><span data-stu-id="d4802-129">The following diagram illustrates the contents of a JPEG file that includes embedded metadata blocks and metadata items.</span></span>

![изображение JPEG с метаданными оценки](graphics/jpeg.png)

<span data-ttu-id="d4802-131">В этом примере изображения метаданные внедряются в файл изображения в кадре изображения.</span><span class="sxs-lookup"><span data-stu-id="d4802-131">In this example image, the metadata is embedded in the image file within an image frame.</span></span> <span data-ttu-id="d4802-132">Формат JPEG не поддерживает несколько кадров изображений, поэтому метаданные концептуально присоединяются к этому одному кадру.</span><span class="sxs-lookup"><span data-stu-id="d4802-132">The JPEG format does not support multiple image frames, so the metadata is conceptually attached to this single frame.</span></span> <span data-ttu-id="d4802-133">Форматы, поддерживающие несколько фреймов, например TIFF, могут иметь метаданные, присоединенные к каждому кадру изображения, как показано на этой схеме.</span><span class="sxs-lookup"><span data-stu-id="d4802-133">Formats that support multiple frames, such as TIFF, may have metadata attached to each image frame as this diagram shows.</span></span> <span data-ttu-id="d4802-134">Некоторые форматы изображений могут также поддерживать метаданные за пределами фрейма изображения, но не так часто и не поддерживаются в кодеках машинного кода.</span><span class="sxs-lookup"><span data-stu-id="d4802-134">Though not common today and not supported by the native image codecs, some image formats may also support metadata outside of an image frame.</span></span> <span data-ttu-id="d4802-135">Компонент WIC достаточно гибок для обработки метаданных и метаданных на уровне кадров за пределами отдельного кадра изображения.</span><span class="sxs-lookup"><span data-stu-id="d4802-135">WIC is flexible enough to handle both frame-level metadata and metadata outside of an image's individual frame.</span></span>

## <a name="reading-image-metadata"></a><span data-ttu-id="d4802-136">Чтение метаданных изображения</span><span class="sxs-lookup"><span data-stu-id="d4802-136">Reading Image Metadata</span></span>

<span data-ttu-id="d4802-137">API-интерфейсы WIC предоставляют компоненты COM, облегчающие приложениям чтение и запись метаданных образа.</span><span class="sxs-lookup"><span data-stu-id="d4802-137">The WIC APIs provide COM components that make it easy for applications to read and write image metadata.</span></span>

<span data-ttu-id="d4802-138">Основным способом чтения метаданных является использование средства чтения запросов метаданных ([**ивикметадатакуериреадер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)) для доступа к конкретным элементам метаданных.</span><span class="sxs-lookup"><span data-stu-id="d4802-138">The primary way to read metadata is to use a metadata query reader ([**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)) to access specific metadata items.</span></span> <span data-ttu-id="d4802-139">Компонент чтения запросов метаданных реализуется кодеком и доступен на уровне декодера или через отдельные кадры изображения, что является наиболее распространенным методом.</span><span class="sxs-lookup"><span data-stu-id="d4802-139">The metadata query reader component is implemented by the codec and can be accessed at the decoder level or through individual image frames, which is the more common method.</span></span> <span data-ttu-id="d4802-140">В следующем коде показано, как получить доступ к модулю чтения запросов для отдельного кадра с помощью метода **жетметадатакуериреадер** читателя запроса.</span><span class="sxs-lookup"><span data-stu-id="d4802-140">The following code demonstrates how to access a query reader for an individual frame by using the query reader's **GetMetadataQueryReader** method.</span></span>


```
// Get the query reader
if (SUCCEEDED(hr))
{
    hr = pFrameDecode->GetMetadataQueryReader(&pQueryReader);
}
```



<span data-ttu-id="d4802-141">Средство чтения запросов предоставляет методы для получения сведений о конкретных метаданных, а также средства для указания извлекаемого элемента метаданных.</span><span class="sxs-lookup"><span data-stu-id="d4802-141">A query reader provides methods to obtain information about specific metadata, and a means to specify a metadata item to retrieve.</span></span> <span data-ttu-id="d4802-142">В следующем коде выражение запроса используется для запроса определенного элемента метаданных в блоке каталога вложенных файлов изображений APP1 (IFD).</span><span class="sxs-lookup"><span data-stu-id="d4802-142">The following code uses a query expression to request a specific metadata item within the App1 nested image file directory (IFD) block.</span></span> <span data-ttu-id="d4802-143">Это делается с помощью метода **жетметадатабинаме** читателя запросов.</span><span class="sxs-lookup"><span data-stu-id="d4802-143">This is done by using the query reader's **GetMetadataByName** method.</span></span> <span data-ttu-id="d4802-144">Следующий код демонстрирует использование средства чтения запросов для получения значения рейтинга Микрософтфото.</span><span class="sxs-lookup"><span data-stu-id="d4802-144">The following code demonstrates using the query reader to obtain the MicrosoftPhoto rating value.</span></span>


```
PROPVARIANT value;
PropVariantInit(&value);

LPCWSTR pwzRatingQuery = L"/app1/ifd/{ushort=18249}";

if (SUCCEEDED(hr))
{
    hr = pQueryReader->GetMetadataByName(pwzRatingQuery, &value);
}
```



<span data-ttu-id="d4802-145">Переменная Пвзратингкуери в предыдущем примере представляет собой строку запроса для доступа к оценке элемента метаданных Микрософтфото.</span><span class="sxs-lookup"><span data-stu-id="d4802-145">The pwzRatingQuery variable in the preceding example is the query string to access the metadata item MicrosoftPhoto rating.</span></span> <span data-ttu-id="d4802-146">Эта строка создается с помощью языка запросов метаданных.</span><span class="sxs-lookup"><span data-stu-id="d4802-146">This string is created by using the metadata query language.</span></span> <span data-ttu-id="d4802-147">Чтобы создать эту строку, необходимо знание формата метаданных и языка запросов метаданных для получения отдельных элементов метаданных.</span><span class="sxs-lookup"><span data-stu-id="d4802-147">To create this string, knowledge of the metadata format and the metadata query language is needed to retrieve individual metadata items.</span></span> <span data-ttu-id="d4802-148">Дополнительные сведения о языке запросов метаданных см. в разделе [Общие сведения о языке запросов метаданных](-wic-codec-metadataquerylanguage.md).</span><span class="sxs-lookup"><span data-stu-id="d4802-148">For more information about the metadata query language, see the [Metadata Query Language Overview](-wic-codec-metadataquerylanguage.md).</span></span>

<span data-ttu-id="d4802-149">В фоновом режиме средство чтения запросов использует средство чтения метаданных ([**ивикметадатареадер**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)) для доступа к метаданным, описанным в выражении запроса.</span><span class="sxs-lookup"><span data-stu-id="d4802-149">Behind the scenes, a query reader uses a metadata reader ([**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)) to access the metadata described by the query expression.</span></span> <span data-ttu-id="d4802-150">Помимо использования средства чтения запросов, доступ к модулю чтения метаданных можно получить непосредственно для чтения метаданных.</span><span class="sxs-lookup"><span data-stu-id="d4802-150">In addition to using a query reader, you can also access a metadata reader directly to read metadata.</span></span> <span data-ttu-id="d4802-151">Средство чтения метаданных можно получить из декодера или отдельных кадров, запрашивая интерфейс модуля чтения блока ([**ивикметадатаблоккреадер**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)).</span><span class="sxs-lookup"><span data-stu-id="d4802-151">You can obtain a metadata reader from the decoder or individual frames by querying for a block reader ([**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)) interface.</span></span>

## <a name="writing-image-metadata"></a><span data-ttu-id="d4802-152">Запись метаданных образа</span><span class="sxs-lookup"><span data-stu-id="d4802-152">Writing Image Metadata</span></span>

<span data-ttu-id="d4802-153">Процесс написания метаданных аналогичен тому, как он читается, за исключением того, что используется средство записи запросов метаданных ([**ивикметадатакуеривритер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)).</span><span class="sxs-lookup"><span data-stu-id="d4802-153">The process of writing metadata is similar to the way it is read except that a metadata query writer ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)) is used.</span></span> <span data-ttu-id="d4802-154">Интерфейс модуля записи запросов реализуется кодировщиком изображений и, как в модуле чтения запросов, доступ к метаданным осуществляется как по кодировщику, так и к отдельным кадрам (в зависимости от поддержки формата изображения).</span><span class="sxs-lookup"><span data-stu-id="d4802-154">The query writer interface is implemented by the image encoder and, as in the query reader, metadata is accessed both on the encoder and on individual frames (depending on image format support).</span></span>

<span data-ttu-id="d4802-155">В следующем коде показано, как получить модуль записи запроса из кадра кодировщика и удалить значение рейтинга, которое было ранее считано.</span><span class="sxs-lookup"><span data-stu-id="d4802-155">The following code demonstrates how to obtain a query writer from an encoder frame and remove the rating value that was previously read.</span></span>


```
// Get the frame's query writer
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->GetMetadataQueryWriter(&pFrameQWriter);
}

if (SUCCEEDED(hr))
{
    hr = pFrameQWriter->RemoveMetadataByName(L"/app1/ifd/{ushort=18249}");
}
```



<span data-ttu-id="d4802-156">Другим способом записи метаданных является быстрое обновление метаданных.</span><span class="sxs-lookup"><span data-stu-id="d4802-156">Another way to write metadata is through fast metadata updates.</span></span> <span data-ttu-id="d4802-157">Быстрая кодировка метаданных — это способ записи метаданных образа без необходимости повторной кодировки файла изображения.</span><span class="sxs-lookup"><span data-stu-id="d4802-157">Fast metadata encoding is a way to write image metadata without having to re-encode an image file.</span></span> <span data-ttu-id="d4802-158">Это делается путем записи новых метаданных в дополненную область формата метаданных.</span><span class="sxs-lookup"><span data-stu-id="d4802-158">This is done by writing new metadata information to a padded region of the metadata format.</span></span> <span data-ttu-id="d4802-159">Кодировщик метаданных Fast ([**ивикфастметадатаенкодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)) получается из фабрики компонентов на основе декодера изображений.</span><span class="sxs-lookup"><span data-stu-id="d4802-159">The fast metadata encoder ([**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)) is obtained from the component factory, based on the image decoder.</span></span> <span data-ttu-id="d4802-160">Затем быстрый кодировщик метаданных получает модуль записи запроса, который используется для записи метаданных.</span><span class="sxs-lookup"><span data-stu-id="d4802-160">The fast metadata encoder then obtains a query writer that is used to write the metadata.</span></span> <span data-ttu-id="d4802-161">Наконец, быстрый кодировщик фиксирует изменения.</span><span class="sxs-lookup"><span data-stu-id="d4802-161">Finally, the fast encoder commits the change.</span></span>

<span data-ttu-id="d4802-162">В следующем коде показано, как получить кодировщик метаданных FAST и использовать его для записи значения Микрософтратинг.</span><span class="sxs-lookup"><span data-stu-id="d4802-162">The following code demonstrates how to obtain a fast metadata encoder and use it to write the MicrosoftRating value.</span></span>


```
if (SUCCEEDED(hr))
{
    IWICFastMetadataEncoder *pFME = NULL;
    IWICMetadataQueryWriter *pFMEQW = NULL;

    hr = pFactory->CreateFastMetadataEncoderFromFrameDecode(
        pFrameDecode,
        &pFME);

    if (SUCCEEDED(hr))
    {
        hr = pFME->GetMetadataQueryWriter(&pFMEQW);
    }

    if (SUCCEEDED(hr))
    {
        // Add additional metadata
        PROPVARIANT value;

        PropVariantInit(&value);

        value.vt = VT_UI4;
        value.uiVal = 99;
        hr = pFMEQW->SetMetadataByName(L"/app1/ifd/{ushort=18249}", &value);

        PropVariantClear(&value);
    }

    if (SUCCEEDED(hr))
    {
        hr = pFME->Commit();
    }
}
```



<span data-ttu-id="d4802-163">Не все форматы метаданных поддерживают быстрые метаданные.</span><span class="sxs-lookup"><span data-stu-id="d4802-163">Not all metadata formats support fast metadata.</span></span> <span data-ttu-id="d4802-164">Чтобы узнать, какие форматы в собственном формате поддерживают быстрое кодирование метаданных, см. таблицу в разделе [Поддерживаемые форматы метаданных](#supported-metadata-formats) далее в этом документе.</span><span class="sxs-lookup"><span data-stu-id="d4802-164">To see which natively supported formats support fast metadata encoding, see the table in the [Supported Metadata Formats](#supported-metadata-formats) section later in this document.</span></span>

<span data-ttu-id="d4802-165">В фоновом режиме средство записи запросов использует модуль записи метаданных ([**ивикметадатавритер**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)) для записи метаданных, описываемых выражением запроса.</span><span class="sxs-lookup"><span data-stu-id="d4802-165">Behind the scenes, a query writer uses a metadata writer ([**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)) to write the metadata described by the query expression.</span></span> <span data-ttu-id="d4802-166">Помимо использования средства чтения запросов, можно также получить доступ к модулю записи метаданных непосредственно для записи метаданных.</span><span class="sxs-lookup"><span data-stu-id="d4802-166">In addition to using a query reader, you can also access a metadata writer directly to write metadata.</span></span> <span data-ttu-id="d4802-167">Модуль записи метаданных можно получить из декодера или отдельных кадров, используя запросы к интерфейсу модуля записи блоков ([**ивикметадатаблокквритер**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter)).</span><span class="sxs-lookup"><span data-stu-id="d4802-167">You can obtain a metadata writer from the decoder or individual frames using querying for a block writer ([**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter)) interface.</span></span>

## <a name="metadata-extensibility"></a><span data-ttu-id="d4802-168">Расширяемость метаданных</span><span class="sxs-lookup"><span data-stu-id="d4802-168">Metadata Extensibility</span></span>

<span data-ttu-id="d4802-169">Как упоминалось ранее, компонент WIC предоставляет несколько обработчиков метаданных для чтения и записи метаданных для общих форматов метаданных.</span><span class="sxs-lookup"><span data-stu-id="d4802-169">As mentioned previously, WIC provides several metadata handlers to read and write metadata for common metadata formats.</span></span> <span data-ttu-id="d4802-170">Однако существуют некоторые форматы метаданных, которые изначально не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="d4802-170">However, there are some metadata formats that are not natively supported.</span></span> <span data-ttu-id="d4802-171">Таким образом, компонент WIC предоставляет API-интерфейсы для создания дополнительных обработчиков метаданных, которые могут расширять поддержку метаданных в другие форматы.</span><span class="sxs-lookup"><span data-stu-id="d4802-171">Therefore, WIC provides APIs for creating additional metadata handlers that can extend metadata support to other formats.</span></span>

<span data-ttu-id="d4802-172">Для полной поддержки других форматов метаданных необходимо разработать два типа обработчиков — средство чтения метаданных для чтения метаданных и модуль записи метаданных для записи метаданных.</span><span class="sxs-lookup"><span data-stu-id="d4802-172">To fully support other metadata formats, two types of handlers must be developed — a metadata reader to read metadata and a metadata writer to write metadata.</span></span> <span data-ttu-id="d4802-173">Хотя эти два обработчика обычно реализуются в парах для определенного формата, это не обязательно.</span><span class="sxs-lookup"><span data-stu-id="d4802-173">Although these two handlers are usually implemented in pairs for a specific format, that is not a requirement.</span></span> <span data-ttu-id="d4802-174">Возможно, в некоторых случаях требуется только возможность чтения или только возможность записи.</span><span class="sxs-lookup"><span data-stu-id="d4802-174">There might be some cases in which only the read ability or only the write ability is needed.</span></span>

<span data-ttu-id="d4802-175">Дополнительные сведения о расширении метаданных с помощью API-интерфейсов WIC см. в разделе [Общие сведения о расширяемости метаданных](-wic-codec-metadatahandlers.md).</span><span class="sxs-lookup"><span data-stu-id="d4802-175">For more information on metadata extensibility using the WIC APIs, see the [Metadata Extensibility Overview](-wic-codec-metadatahandlers.md).</span></span>

## <a name="supported-metadata-formats"></a><span data-ttu-id="d4802-176">Поддерживаемые форматы метаданных</span><span class="sxs-lookup"><span data-stu-id="d4802-176">Supported Metadata Formats</span></span>

<span data-ttu-id="d4802-177">Компонент WIC обеспечивает поддержку нескольких распространенных форматов метаданных.</span><span class="sxs-lookup"><span data-stu-id="d4802-177">WIC provides support for several common metadata formats.</span></span> <span data-ttu-id="d4802-178">В следующей таблице перечислены поддерживаемые форматы метаданных, их версии, форматы изображений, поддерживающие формат метаданных, а также указывается, поддерживает ли формат метаданных быструю кодировку метаданных.</span><span class="sxs-lookup"><span data-stu-id="d4802-178">The following table lists the supported metadata formats, their versions, the image formats that support the metadata format, and whether the metadata format supports fast metadata encoding.</span></span> <span data-ttu-id="d4802-179">Дополнительные сведения о быстрых кодировках метаданных см. в разделе [запись метаданных образа](#writing-image-metadata) ранее в этом документе.</span><span class="sxs-lookup"><span data-stu-id="d4802-179">For more information about fast metadata encoding, see the [Writing Image Metadata](#writing-image-metadata) section earlier in this document.</span></span>



| <span data-ttu-id="d4802-180">Поддерживаемые форматы метаданных</span><span class="sxs-lookup"><span data-stu-id="d4802-180">Supported metadata formats</span></span> | <span data-ttu-id="d4802-181">Версия спецификации метаданных</span><span class="sxs-lookup"><span data-stu-id="d4802-181">Metadata specification version</span></span> | <span data-ttu-id="d4802-182">Поддержка формата изображения</span><span class="sxs-lookup"><span data-stu-id="d4802-182">Image format support</span></span> | <span data-ttu-id="d4802-183">Поддерживает быструю кодировку метаданных</span><span class="sxs-lookup"><span data-stu-id="d4802-183">Supports fast metadata encoding</span></span> |
|----------------------------|--------------------------------|----------------------|---------------------------------|
| <span data-ttu-id="d4802-184">App0</span><span class="sxs-lookup"><span data-stu-id="d4802-184">App0</span></span>                       | <span data-ttu-id="d4802-185">JFIF 1,02</span><span class="sxs-lookup"><span data-stu-id="d4802-185">JFIF 1.02</span></span>                      | <span data-ttu-id="d4802-186">JPEG</span><span class="sxs-lookup"><span data-stu-id="d4802-186">JPEG</span></span>                 | <span data-ttu-id="d4802-187">Нет</span><span class="sxs-lookup"><span data-stu-id="d4802-187">No</span></span>                              |
| <span data-ttu-id="d4802-188">Приложение 1</span><span class="sxs-lookup"><span data-stu-id="d4802-188">App1</span></span>                       | <span data-ttu-id="d4802-189">JFIF 1,02</span><span class="sxs-lookup"><span data-stu-id="d4802-189">JFIF 1.02</span></span>                      | <span data-ttu-id="d4802-190">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="d4802-190">JPEG, TIFF</span></span>           | <span data-ttu-id="d4802-191">Нет</span><span class="sxs-lookup"><span data-stu-id="d4802-191">No</span></span>                              |
| <span data-ttu-id="d4802-192">App13</span><span class="sxs-lookup"><span data-stu-id="d4802-192">App13</span></span>                      | <span data-ttu-id="d4802-193">Неизвестно</span><span class="sxs-lookup"><span data-stu-id="d4802-193">Unknown</span></span>                        | <span data-ttu-id="d4802-194">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="d4802-194">JPEG, TIFF</span></span>           | <span data-ttu-id="d4802-195">Нет</span><span class="sxs-lookup"><span data-stu-id="d4802-195">No</span></span>                              |
| <span data-ttu-id="d4802-196">IFD</span><span class="sxs-lookup"><span data-stu-id="d4802-196">IFD</span></span>                        | <span data-ttu-id="d4802-197">TIFF 6,0</span><span class="sxs-lookup"><span data-stu-id="d4802-197">TIFF 6.0</span></span>                       | <span data-ttu-id="d4802-198">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="d4802-198">JPEG, TIFF</span></span>           | <span data-ttu-id="d4802-199">Да</span><span class="sxs-lookup"><span data-stu-id="d4802-199">Yes</span></span>                             |
| <span data-ttu-id="d4802-200">ирб</span><span class="sxs-lookup"><span data-stu-id="d4802-200">IRB</span></span>                        | <span data-ttu-id="d4802-201">Неизвестно</span><span class="sxs-lookup"><span data-stu-id="d4802-201">Unknown</span></span>                        | <span data-ttu-id="d4802-202">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="d4802-202">JPEG, TIFF</span></span>           | <span data-ttu-id="d4802-203">Нет</span><span class="sxs-lookup"><span data-stu-id="d4802-203">No</span></span>                              |
| <span data-ttu-id="d4802-204">Exif</span><span class="sxs-lookup"><span data-stu-id="d4802-204">Exif</span></span>                       | <span data-ttu-id="d4802-205">EXIF 2,2</span><span class="sxs-lookup"><span data-stu-id="d4802-205">Exif 2.2</span></span>                       | <span data-ttu-id="d4802-206">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="d4802-206">JPEG, TIFF</span></span>           | <span data-ttu-id="d4802-207">Да</span><span class="sxs-lookup"><span data-stu-id="d4802-207">Yes</span></span>                             |
| <span data-ttu-id="d4802-208">ПОДДЕРЖИВАЮЩ</span><span class="sxs-lookup"><span data-stu-id="d4802-208">XMP</span></span>                        | <span data-ttu-id="d4802-209">XMP 1,0 (Сентябрь 2005)</span><span class="sxs-lookup"><span data-stu-id="d4802-209">XMP 1.0 (Sept 2005)</span></span>            | <span data-ttu-id="d4802-210">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="d4802-210">JPEG, TIFF</span></span>           | <span data-ttu-id="d4802-211">Да</span><span class="sxs-lookup"><span data-stu-id="d4802-211">Yes</span></span>                             |
| <span data-ttu-id="d4802-212">GPS</span><span class="sxs-lookup"><span data-stu-id="d4802-212">GPS</span></span>                        | <span data-ttu-id="d4802-213">EXIF 2,2</span><span class="sxs-lookup"><span data-stu-id="d4802-213">Exif 2.2</span></span>                       | <span data-ttu-id="d4802-214">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="d4802-214">JPEG, TIFF</span></span>           | <span data-ttu-id="d4802-215">Да</span><span class="sxs-lookup"><span data-stu-id="d4802-215">Yes</span></span>                             |
| <span data-ttu-id="d4802-216">IPTC</span><span class="sxs-lookup"><span data-stu-id="d4802-216">IPTC</span></span>                       | <span data-ttu-id="d4802-217">IPTC 4,0</span><span class="sxs-lookup"><span data-stu-id="d4802-217">IPTC 4.0</span></span>                       | <span data-ttu-id="d4802-218">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="d4802-218">JPEG, TIFF</span></span>           | <span data-ttu-id="d4802-219">Да</span><span class="sxs-lookup"><span data-stu-id="d4802-219">Yes</span></span>                             |
| <span data-ttu-id="d4802-220">полнотекстовым</span><span class="sxs-lookup"><span data-stu-id="d4802-220">tEXt</span></span>                       | <span data-ttu-id="d4802-221">PNG 1,2</span><span class="sxs-lookup"><span data-stu-id="d4802-221">PNG 1.2</span></span>                        | <span data-ttu-id="d4802-222">PNG</span><span class="sxs-lookup"><span data-stu-id="d4802-222">PNG</span></span>                  | <span data-ttu-id="d4802-223">Нет</span><span class="sxs-lookup"><span data-stu-id="d4802-223">No</span></span>                              |



 

> [!Note]  
> <span data-ttu-id="d4802-224">IPTC поддерживает FME только при увеличении размера блоков, так как IPTC не поддерживает заполнение.</span><span class="sxs-lookup"><span data-stu-id="d4802-224">IPTC only supports FME if the blocks grow in size, as IPTC does not support padding.</span></span>

 

## <a name="metadata-component-summary"></a><span data-ttu-id="d4802-225">Сводка компонента метаданных</span><span class="sxs-lookup"><span data-stu-id="d4802-225">Metadata Component Summary</span></span>

<span data-ttu-id="d4802-226">В следующей таблице описаны интерфейсы WIC, поддерживающие метаданные, и соответствующие им компоненты.</span><span class="sxs-lookup"><span data-stu-id="d4802-226">The following table describes the WIC interfaces that support metadata, and their corresponding components.</span></span> <span data-ttu-id="d4802-227">Эти компоненты предоставляют доступ к метаданным образа.</span><span class="sxs-lookup"><span data-stu-id="d4802-227">These components provide the access to an image's metadata.</span></span> <span data-ttu-id="d4802-228">Дополнительные сведения об этих компонентах см. в разделе [Общие сведения о компоненте создания образов Windows](-wic-about-windows-imaging-codec.md).</span><span class="sxs-lookup"><span data-stu-id="d4802-228">For more information about these components, see the [Windows Imaging Component Overview](-wic-about-windows-imaging-codec.md).</span></span> 

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d4802-229">Компонент</span><span class="sxs-lookup"><span data-stu-id="d4802-229">Component</span></span></th>
<th><span data-ttu-id="d4802-230">Описание</span><span class="sxs-lookup"><span data-stu-id="d4802-230">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d4802-231">Декодер точечных рисунков (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder"><strong>ивикбитмапдекодер</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="d4802-231">Bitmap Decoder (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder"><strong>IWICBitmapDecoder</strong></a>)</span></span></td>
<td><ul>
<li><span data-ttu-id="d4802-232">Считывает поток изображения и создает пригодный для использования исходный точечный рисунок.</span><span class="sxs-lookup"><span data-stu-id="d4802-232">Reads an image stream and produces a usable bitmap source.</span></span> <span data-ttu-id="d4802-233">Связан с форматом контейнера, таким как TIFF или Объединенная группа экспертов (JPEG).</span><span class="sxs-lookup"><span data-stu-id="d4802-233">Associated with a container format such as Tagged Image File Format (TIFF) or Joint Photographic Experts Group (JPEG).</span></span></li>
<li><span data-ttu-id="d4802-234">Реализует интерфейс <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>ивикметадатаблоккреадер</strong></a> для перечисления всех блоков метаданных в потоке данных декодера, не находящихся внутри рамки.</span><span class="sxs-lookup"><span data-stu-id="d4802-234">Implements an <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a> interface to enumerate all of the metadata blocks in the decoder's data stream that are not inside a frame.</span></span></li>
<li><span data-ttu-id="d4802-235">Предоставляет средство чтения запросов для чтения метаданных, связанных с изображением, которое не находится внутри рамки.</span><span class="sxs-lookup"><span data-stu-id="d4802-235">Exposes a query reader to read the metadata associated with the image that is not inside a frame.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4802-236">Декодирование кадров точечного рисунка (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode"><strong>IWICBitmapFrameDecode</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="d4802-236">Bitmap Frame Decode (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode"><strong>IWICBitmapFrameDecode</strong></a>)</span></span></td>
<td><ul>
<li><span data-ttu-id="d4802-237">Обращается к отдельным кадрам из потока изображений, удерживаемого декодером.</span><span class="sxs-lookup"><span data-stu-id="d4802-237">Accesses individual frames from the image stream held by the decoder.</span></span></li>
<li><span data-ttu-id="d4802-238">Реализует интерфейс <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>ивикметадатаблоккреадер</strong></a> для перечисления всех блоков метаданных в потоке данных кадра.</span><span class="sxs-lookup"><span data-stu-id="d4802-238">Implements an <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a> interface to enumerate all of the metadata blocks in the frame's data stream.</span></span></li>
<li><span data-ttu-id="d4802-239">Предоставляет средство чтения запросов для чтения метаданных, связанных с кадром, с помощью выражений запросов.</span><span class="sxs-lookup"><span data-stu-id="d4802-239">Exposes a query reader to read the metadata associated with the frame, using query expressions.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4802-240">Растровый кодировщик (<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder"><strong>ивикбитмапенкодер</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="d4802-240">Bitmap Encoder (<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder"><strong>IWICBitmapEncoder</strong></a>)</span></span></td>
<td><ul>
<li><span data-ttu-id="d4802-241">Записывает источник растрового изображения в поток изображений.</span><span class="sxs-lookup"><span data-stu-id="d4802-241">Writes a bitmap source to an image stream.</span></span> <span data-ttu-id="d4802-242">Связан с форматом контейнера, например TIFF или JPEG.</span><span class="sxs-lookup"><span data-stu-id="d4802-242">Associated with a container format such as TIFF or JPEG.</span></span></li>
<li><span data-ttu-id="d4802-243">Реализует интерфейс <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>ивикметадатаблокквритер</strong></a> для создания списка блоков метаданных для записи в поток данных кодировщика.</span><span class="sxs-lookup"><span data-stu-id="d4802-243">Implements an <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a> interface to build up a list of metadata blocks to write into the data stream of the encoder.</span></span></li>
<li><span data-ttu-id="d4802-244">Предоставляет средство записи запроса для записи метаданных, связанных с изображением, с помощью выражений запросов.</span><span class="sxs-lookup"><span data-stu-id="d4802-244">Exposes a query writer to write the metadata associated with the image, using query expressions.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4802-245">Кодировка кадра битма (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode"><strong>ивикбитмапфраминкоде</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="d4802-245">Bitma Frame Encode (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode"><strong>IWICBitmapFrameEncode</strong></a>)</span></span></td>
<td><ul>
<li><span data-ttu-id="d4802-246">Создает кадр, который будет кодироваться в поток, удерживаемый кодировщиком.</span><span class="sxs-lookup"><span data-stu-id="d4802-246">Creates a frame that will be encoded into the stream held by the encoder.</span></span></li>
<li><span data-ttu-id="d4802-247">Реализует интерфейс <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>ивикметадатаблокквритер</strong></a> для создания списка блоков метаданных для записи в поток данных кадра.</span><span class="sxs-lookup"><span data-stu-id="d4802-247">Implements an <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a> interface to build up a list of metadata blocks to write into the frame's data stream.</span></span></li>
<li><span data-ttu-id="d4802-248">Предоставляет средство записи запроса для записи метаданных, связанных с кадром, с помощью выражений запросов.</span><span class="sxs-lookup"><span data-stu-id="d4802-248">Exposes a query writer to write the metadata associated with the frame, using query expressions.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="d4802-249">В следующей таблице описаны компоненты метаданных компонента WIC.</span><span class="sxs-lookup"><span data-stu-id="d4802-249">The following table describes the WIC metadata components.</span></span> <span data-ttu-id="d4802-250">Эти компоненты позволяют считывать и записывать метаданные в образ, предоставляемый компонентами, перечисленными в предыдущей таблице.</span><span class="sxs-lookup"><span data-stu-id="d4802-250">These components enable you to read and write the metadata in an image exposed by the components listed in the previous table.</span></span> 

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d4802-251">Компонент</span><span class="sxs-lookup"><span data-stu-id="d4802-251">Component</span></span></th>
<th><span data-ttu-id="d4802-252">Описание</span><span class="sxs-lookup"><span data-stu-id="d4802-252">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d4802-253">Средство чтения запросов метаданных (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader"><strong>ивикметадатакуериреадер</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="d4802-253">Metadata Query Reader (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader"><strong>IWICMetadataQueryReader</strong></a>)</span></span></td>
<td><ul>
<li><span data-ttu-id="d4802-254">Принимает строку запроса и выполняет навигацию по базовой иерархии метаданных для получения метаданных.</span><span class="sxs-lookup"><span data-stu-id="d4802-254">Takes a query string and navigates the underlying metadata hierarchy to get metadata.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4802-255">Средство записи запросов метаданных (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter"><strong>ивикметадатакуеривритер</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="d4802-255">Metadata Query Writer (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter"><strong>IWICMetadataQueryWriter</strong></a>)</span></span></td>
<td><ul>
<li><span data-ttu-id="d4802-256">Принимает строку запроса и выполняет навигацию по базовой иерархии метаданных для получения, установки и удаления метаданных.</span><span class="sxs-lookup"><span data-stu-id="d4802-256">Takes a query string and navigates the underlying metadata hierarchy to get, set, and remove metadata.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4802-257">Считыватель блоков метаданных (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>ивикметадатаблоккреадер</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="d4802-257">Metadata Block Reader (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a>)</span></span></td>
<td><ul>
<li><span data-ttu-id="d4802-258">Управляет коллекцией объектов <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader"><strong>ивикметадатареадер</strong></a> , доступную только для чтения, в верхней части иерархии метаданных и включает перечисление всех блоков метаданных.</span><span class="sxs-lookup"><span data-stu-id="d4802-258">Manages a read-only collection of <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader"><strong>IWICMetadataReader</strong></a> objects at the top of the metadata hierarchy and enables enumeration of all metadata blocks.</span></span></li>
<li><span data-ttu-id="d4802-259">Реализуется растровым декодером и декодированным кадром точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="d4802-259">Implemented by a bitmap decoder and a decoded bitmap frame.</span></span></li>
<li><span data-ttu-id="d4802-260">Реализован сторонними разработчиками компонентов для пользовательских кодеков.</span><span class="sxs-lookup"><span data-stu-id="d4802-260">Implemented by third-party component developers for custom codecs.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4802-261">Модуль записи блоков метаданных (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>ивикметадатаблокквритер</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="d4802-261">Metadata Block Writer (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a>)</span></span></td>
<td><ul>
<li><span data-ttu-id="d4802-262">Управляет коллекцией объектов <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter"><strong>ивикметадатавритер</strong></a> , предназначенных для чтения и записи, в верхней части иерархии метаданных.</span><span class="sxs-lookup"><span data-stu-id="d4802-262">Manages a read and write collection of <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter"><strong>IWICMetadataWriter</strong></a> objects at the top of the metadata hierarchy.</span></span></li>
<li><span data-ttu-id="d4802-263">Реализуется кодировщиком растрового изображения и кодированием кадра растрового изображения.</span><span class="sxs-lookup"><span data-stu-id="d4802-263">Implemented by a bitmap encoder and a bitmap frame encode.</span></span></li>
<li><span data-ttu-id="d4802-264">Реализован сторонними разработчиками компонентов для пользовательских кодеков.</span><span class="sxs-lookup"><span data-stu-id="d4802-264">Implemented by third-party component developers for custom codecs.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4802-265">Средство чтения метаданных (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader"><strong>ивикметадатареадер</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="d4802-265">Metadata Reader (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader"><strong>IWICMetadataReader</strong></a>)</span></span></td>
<td><ul>
<li><span data-ttu-id="d4802-266">Анализирует поток метаданных и управляет коллекцией элементов метаданных, доступную только для чтения.</span><span class="sxs-lookup"><span data-stu-id="d4802-266">Parses a stream of metadata and manages a read-only collection of the metadata items.</span></span> <span data-ttu-id="d4802-267">Связан с форматом метаданных, например EXIF, IFD и XMP.</span><span class="sxs-lookup"><span data-stu-id="d4802-267">Associated with a metadata format such as EXIF, IFD, and XMP.</span></span></li>
<li><span data-ttu-id="d4802-268">Выступает в качестве словаря и возвращает значение при наличии пары форматов и ИДЕНТИФИКАТОРов.</span><span class="sxs-lookup"><span data-stu-id="d4802-268">Acts as a dictionary, returning a value when given a format and ID pair.</span></span></li>
<li><span data-ttu-id="d4802-269">Реализован сторонними разработчиками компонентов для пользовательских типов метаданных.</span><span class="sxs-lookup"><span data-stu-id="d4802-269">Implemented by third-party component developers for custom metadata types.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4802-270">Модуль записи метаданных (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter"><strong>ивикметадатавритер</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="d4802-270">Metadata Writer (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter"><strong>IWICMetadataWriter</strong></a>)</span></span></td>
<td><ul>
<li><span data-ttu-id="d4802-271">Анализирует и сериализует поток метаданных и управляет коллекцией элементов метаданных, предназначенной для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="d4802-271">Parses and serializes a stream of metadata and manages a read/write collection of metadata items.</span></span></li>
<li><span data-ttu-id="d4802-272">Реализован сторонними разработчиками компонентов для пользовательских типов метаданных.</span><span class="sxs-lookup"><span data-stu-id="d4802-272">Implemented by third-party component developers for custom metadata types.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4802-273">Быстрый кодировщик метаданных<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder"><strong>ивикфастметадатаенкодер</strong></a></span><span class="sxs-lookup"><span data-stu-id="d4802-273">Fast Metadata Encoder<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder"><strong>IWICFastMetadataEncoder</strong></a></span></span></td>
<td><ul>
<li><span data-ttu-id="d4802-274">Предоставляет семантику для записи в иерархии метаданных, которая будет обновлять метаданные на месте без повторной кодировки изображения.</span><span class="sxs-lookup"><span data-stu-id="d4802-274">Exposes semantics for writing on a metadata hierarchy that will update metadata in place without re-encoding the image.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="d4802-275">См. также</span><span class="sxs-lookup"><span data-stu-id="d4802-275">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="d4802-276">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="d4802-276">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d4802-277">Общие сведения о компоненте создания образов Windows</span><span class="sxs-lookup"><span data-stu-id="d4802-277">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="d4802-278">Общие сведения о языке запросов метаданных</span><span class="sxs-lookup"><span data-stu-id="d4802-278">Metadata Query Language Overview</span></span>](-wic-codec-metadataquerylanguage.md)
</dt> <dt>

[<span data-ttu-id="d4802-279">Общие сведения о чтении и записи метаданных изображений</span><span class="sxs-lookup"><span data-stu-id="d4802-279">Overview of Reading and Writing Image Metadata</span></span>](-wic-codec-readingwritingmetadata.md)
</dt> <dt>

[<span data-ttu-id="d4802-280">Общие сведения о расширяемости метаданных</span><span class="sxs-lookup"><span data-stu-id="d4802-280">Metadata Extensibility Overview</span></span>](-wic-codec-metadatahandlers.md)
</dt> <dt>

[<span data-ttu-id="d4802-281">Пошаговое руководство. повторное кодирование изображения JPEG с помощью метаданных</span><span class="sxs-lookup"><span data-stu-id="d4802-281">How-to: Re-encode a JPEG Image with Metadata</span></span>](-wic-codec-jpegmetadataencoding.md)
</dt> </dl>

 

 



