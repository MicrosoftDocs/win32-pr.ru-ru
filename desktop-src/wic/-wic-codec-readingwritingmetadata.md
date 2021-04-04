---
description: В этом разделе приводятся общие сведения об использовании интерфейсов API компонента Windows Imaging Component (WIC) для чтения и записи метаданных, внедренных в файлы изображений.
ms.assetid: b1e0b936-a13a-42dd-8470-957ba1d90423
title: Общие сведения о чтении и записи метаданных изображений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 484d562b71184c20adf054f1de2a4203878da9b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998703"
---
# <a name="overview-of-reading-and-writing-image-metadata"></a><span data-ttu-id="5fce6-103">Общие сведения о чтении и записи метаданных изображений</span><span class="sxs-lookup"><span data-stu-id="5fce6-103">Overview of Reading and Writing Image Metadata</span></span>

<span data-ttu-id="5fce6-104">В этом разделе приводятся общие сведения об использовании интерфейсов API компонента Windows Imaging Component (WIC) для чтения и записи метаданных, внедренных в файлы изображений.</span><span class="sxs-lookup"><span data-stu-id="5fce6-104">This topic provides an overview of how you can use the Windows Imaging Component (WIC) APIs to read and write metadata that is embedded in image files.</span></span>

<span data-ttu-id="5fce6-105">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="5fce6-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="5fce6-106">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="5fce6-106">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="5fce6-107">Введение</span><span class="sxs-lookup"><span data-stu-id="5fce6-107">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="5fce6-108">Чтение Метададата с помощью средства чтения запросов</span><span class="sxs-lookup"><span data-stu-id="5fce6-108">Reading Metadadata Using a Query Reader</span></span>](#reading-metadadata-using-a-query-reader)
    -   [<span data-ttu-id="5fce6-109">Получение средства чтения запросов</span><span class="sxs-lookup"><span data-stu-id="5fce6-109">Obtaining a Query Reader</span></span>](#obtaining-a-query-reader)
    -   [<span data-ttu-id="5fce6-110">Чтение метаданных</span><span class="sxs-lookup"><span data-stu-id="5fce6-110">Reading Metadata</span></span>](#reading-metadata)
    -   [<span data-ttu-id="5fce6-111">Дополнительные методы чтения запросов</span><span class="sxs-lookup"><span data-stu-id="5fce6-111">Additional Query Reader Methods</span></span>](#additional-query-reader-methods)
-   [<span data-ttu-id="5fce6-112">Запись метаданных с помощью модуля записи запроса</span><span class="sxs-lookup"><span data-stu-id="5fce6-112">Writing Metadata Using a Query Writer</span></span>](#writing-metadata-using-a-query-writer)
    -   [<span data-ttu-id="5fce6-113">Получение модуля записи запроса</span><span class="sxs-lookup"><span data-stu-id="5fce6-113">Obtaining a Query Writer</span></span>](#obtaining-a-query-writer)
    -   [<span data-ttu-id="5fce6-114">Добавление метаданных</span><span class="sxs-lookup"><span data-stu-id="5fce6-114">Adding Metadata</span></span>](#adding-metadata)
    -   [<span data-ttu-id="5fce6-115">Удаление метаданных</span><span class="sxs-lookup"><span data-stu-id="5fce6-115">Removing Metadata</span></span>](#removing-metadata)
    -   [<span data-ttu-id="5fce6-116">Копирование метаданных для повторной кодировки</span><span class="sxs-lookup"><span data-stu-id="5fce6-116">Copying Metadata for Re-encoding</span></span>](#copying-metadata-for-re-encoding)
-   [<span data-ttu-id="5fce6-117">Быстрая кодировка метаданных</span><span class="sxs-lookup"><span data-stu-id="5fce6-117">Fast Metadata Encoding</span></span>](#fast-metadata-encoding)
    -   [<span data-ttu-id="5fce6-118">Добавление заполнения в блоки метаданных</span><span class="sxs-lookup"><span data-stu-id="5fce6-118">Adding Padding to Metadata Blocks</span></span>](#adding-padding-to-metadata-blocks)
    -   [<span data-ttu-id="5fce6-119">Получение высокоскоростного кодировщика метаданных</span><span class="sxs-lookup"><span data-stu-id="5fce6-119">Obtaining a Fast Metadata Encoder</span></span>](#obtaining-a-fast-metadata-encoder)
    -   [<span data-ttu-id="5fce6-120">Использование кодировщика быстрых метаданных</span><span class="sxs-lookup"><span data-stu-id="5fce6-120">Using the Fast Metadata Encoder</span></span>](#using-the-fast-metadata-encoder)
-   [<span data-ttu-id="5fce6-121">См. также</span><span class="sxs-lookup"><span data-stu-id="5fce6-121">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="5fce6-122">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="5fce6-122">Prerequisites</span></span>

<span data-ttu-id="5fce6-123">Чтобы понять этот раздел, необходимо ознакомиться с системой метаданных WIC, как описано в [обзоре метаданных WIC](-wic-about-metadata.md).</span><span class="sxs-lookup"><span data-stu-id="5fce6-123">To understand this topic, you should be familiar with the WIC metadata system as described in the [WIC Metadata Overview](-wic-about-metadata.md).</span></span> <span data-ttu-id="5fce6-124">Также следует ознакомиться с языком запросов, используемым для чтения и записи метаданных, как описано в разделе [Общие сведения о языке запросов метаданных](-wic-codec-metadataquerylanguage.md).</span><span class="sxs-lookup"><span data-stu-id="5fce6-124">You should also be familiar with the query language used to read and write metadata, as described in [Metadata Query Language Overview](-wic-codec-metadataquerylanguage.md).</span></span>

## <a name="introduction"></a><span data-ttu-id="5fce6-125">Введение</span><span class="sxs-lookup"><span data-stu-id="5fce6-125">Introduction</span></span>

<span data-ttu-id="5fce6-126">Компонент WIC предоставляет разработчикам приложений компоненты модели COM для чтения и записи метаданных, внедренных в файлы изображений.</span><span class="sxs-lookup"><span data-stu-id="5fce6-126">WIC provides application developers with Component Object Model (COM) components to read and write metadata embedded in image files.</span></span> <span data-ttu-id="5fce6-127">Существует два способа чтения и записи метаданных:</span><span class="sxs-lookup"><span data-stu-id="5fce6-127">There are two ways to read and write metadata:</span></span>

-   <span data-ttu-id="5fce6-128">Использование модуля чтения и записи запросов и выражения запроса для запроса блоков метаданных для вложенных блоков или конкретных метаданных в блоке.</span><span class="sxs-lookup"><span data-stu-id="5fce6-128">Using a query reader/writer and a query expression to query metadata blocks for nested blocks or specific metadata within a block.</span></span>
-   <span data-ttu-id="5fce6-129">Использование обработчика метаданных (средства чтения метаданных или модуля записи метаданных) для доступа к вложенным блокам метаданных или конкретным метаданным в блоках метаданных.</span><span class="sxs-lookup"><span data-stu-id="5fce6-129">Using a metadata handler (a metadata reader or a metadata writer) to access the nested metadata blocks or specific metadata within the metadata blocks.</span></span>

<span data-ttu-id="5fce6-130">Проще всего использовать для доступа к метаданным модуль чтения/записи запроса и выражение запроса.</span><span class="sxs-lookup"><span data-stu-id="5fce6-130">The easiest of these is to use a query reader/writer and a query expression to access the metadata.</span></span> <span data-ttu-id="5fce6-131">Средство чтения запросов ([**ивикметадатакуериреадер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)) используется для чтения метаданных, пока для записи метаданных используется модуль записи запроса ([**ивикметадатакуеривритер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)).</span><span class="sxs-lookup"><span data-stu-id="5fce6-131">A query reader ([**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)) is used to read metadata while a query writer ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)) is used to write metadata.</span></span> <span data-ttu-id="5fce6-132">В обоих случаях используется выражение запроса для чтения или записи нужных метаданных.</span><span class="sxs-lookup"><span data-stu-id="5fce6-132">Both of these use a query expression to read or write the desired metadata.</span></span> <span data-ttu-id="5fce6-133">В фоновом режиме средство чтения запросов (и модуль записи) использует обработчик метаданных для доступа к метаданным, описанным в выражении запроса.</span><span class="sxs-lookup"><span data-stu-id="5fce6-133">Behind the scenes, a query reader (and writer) uses a metadata handler to access the metadata described by the query expression.</span></span>

<span data-ttu-id="5fce6-134">Более продвинутый метод — прямой доступ к обработчикам метаданных.</span><span class="sxs-lookup"><span data-stu-id="5fce6-134">The more advanced method is to directly access the metadata handlers.</span></span> <span data-ttu-id="5fce6-135">Обработчик метаданных извлекается из отдельных кадров с помощью модуля чтения блока ([**ивикметадатаблоккреадер**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)) или модуля записи блока ([**ивикметадатаблокквритер**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter)).</span><span class="sxs-lookup"><span data-stu-id="5fce6-135">A metadata handler is obtained from the individual frames using a block reader ([**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)) or a block writer ([**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter)).</span></span> <span data-ttu-id="5fce6-136">Доступны два типа обработчиков метаданных: средство чтения метаданных ([**ивикметадатареадер**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)) и модуль записи метаданных ([**ивикметадатавритер**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)).</span><span class="sxs-lookup"><span data-stu-id="5fce6-136">The two types of metadata handlers available are the metadata reader ([**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)) and the metadata writer ([**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)).</span></span>

<span data-ttu-id="5fce6-137">Следующая схема содержимого файла изображения JPEG используется во всех примерах этого раздела.</span><span class="sxs-lookup"><span data-stu-id="5fce6-137">The following diagram of the contents of a JPEG image file is used throughout the examples in this topic.</span></span> <span data-ttu-id="5fce6-138">Изображение, представленное этой схемой, было создано с помощью Microsoft Paint; метаданные оценки были добавлены с помощью фотоальбома Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5fce6-138">The image represented by this diagram was created by using Microsoft Paint; the rating metadata was added by using the Photo Gallery feature of Windows Vista.</span></span>

![Иллюстрация изображения JPEG с метаданными оценки](graphics/jpeg.png)

## <a name="reading-metadadata-using-a-query-reader"></a><span data-ttu-id="5fce6-140">Чтение Метададата с помощью средства чтения запросов</span><span class="sxs-lookup"><span data-stu-id="5fce6-140">Reading Metadadata Using a Query Reader</span></span>

<span data-ttu-id="5fce6-141">Самый простой способ прочитать метаданные — использовать интерфейс средства чтения запросов [**ивикметадатакуериреадер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader).</span><span class="sxs-lookup"><span data-stu-id="5fce6-141">The easiest way to read metadata is to use the query reader interface, [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader).</span></span> <span data-ttu-id="5fce6-142">Средство чтения запросов позволяет считывать блоки метаданных и элементы в блоках метаданных с помощью выражения запроса.</span><span class="sxs-lookup"><span data-stu-id="5fce6-142">The query reader enables you to read metadata blocks and items within metadata blocks using a query expression.</span></span>

<span data-ttu-id="5fce6-143">Существует три способа получить читателя запросов: с помощью декодера точечных рисунков ([**ивикбитмапдекодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)) через отдельные кадры ([**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)) или через модуль записи запросов ([**ивикметадатакуеривритер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)).</span><span class="sxs-lookup"><span data-stu-id="5fce6-143">There are three ways to obtain a query reader: through a bitmap decoder ([**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)), through its individual frames ([**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)), or through a query writer ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)).</span></span>

### <a name="obtaining-a-query-reader"></a><span data-ttu-id="5fce6-144">Получение средства чтения запросов</span><span class="sxs-lookup"><span data-stu-id="5fce6-144">Obtaining a Query Reader</span></span>

<span data-ttu-id="5fce6-145">В следующем примере кода показано, как получить декодер битовой карты из фабрики изображений и получить отдельный кадр точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="5fce6-145">The following example code shows how to obtain a bitmap decoder from the imaging factory and retrieve an individual bitmap frame.</span></span> <span data-ttu-id="5fce6-146">Этот код также выполняет настройку, необходимую для получения средства чтения запросов из декодированного фрейма.</span><span class="sxs-lookup"><span data-stu-id="5fce6-146">This code also performs setup work needed to obtain a query reader from a decoded frame.</span></span>


```
IWICImagingFactory *pFactory = NULL;
IWICBitmapDecoder *pDecoder = NULL;
IWICBitmapFrameDecode *pFrameDecode = NULL;
IWICMetadataQueryReader *pQueryReader = NULL;
IWICMetadataQueryReader *pEmbedReader = NULL;
PROPVARIANT value;

// Initialize COM
CoInitialize(NULL);

// Initialize PROPVARIANT
PropVariantInit(&value);

//Create the COM imaging factory
HRESULT hr = CoCreateInstance(
    CLSID_WICImagingFactory,
    NULL,
    CLSCTX_INPROC_SERVER,
    IID_IWICImagingFactory,
    (LPVOID*)&pFactory);

// Create the decoder
if (SUCCEEDED(hr))
{
    hr = pFactory->CreateDecoderFromFilename(
        L"test.jpg",
        NULL,
        GENERIC_READ,
        WICDecodeMetadataCacheOnDemand,
        &pDecoder);
}

// Get a single frame from the image
if (SUCCEEDED(hr))
{
    hr = pDecoder->GetFrame(
         0,  //JPEG has only one frame.
         &pFrameDecode); 
}
```



<span data-ttu-id="5fce6-147">Декодер точечных рисунков для файла test.jpg получается с помощью метода **креатедекодерфромфиленаме** фабрики изображений.</span><span class="sxs-lookup"><span data-stu-id="5fce6-147">The bitmap decoder for the test.jpg file is obtained by using the **CreateDecoderFromFilename** method of the imaging factory.</span></span> <span data-ttu-id="5fce6-148">В этом методе четвертый параметр устанавливается в значение WICDecodeMetadataCacheOnDemand из перечисления [**викдекодеоптионс**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) .</span><span class="sxs-lookup"><span data-stu-id="5fce6-148">In this method, the fourth parameter is set to the value WICDecodeMetadataCacheOnDemand from the [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) enumeration.</span></span> <span data-ttu-id="5fce6-149">Это означает, что декодер кэширует метаданные, когда требуются метаданные. либо путем получения читателя запросов, либо базового средства чтения метаданных.</span><span class="sxs-lookup"><span data-stu-id="5fce6-149">This tells the decoder to cache the metadata when the metadata is needed; either by obtaining a query reader or the underlying metadata reader.</span></span> <span data-ttu-id="5fce6-150">Использование этого параметра позволяет хранить поток в метаданных, необходимых для быстрой кодировки метаданных, и позволяет без потерь раскодировать изображение JPEG.</span><span class="sxs-lookup"><span data-stu-id="5fce6-150">Using this option enables you to retain the stream to the metadata required for fast metadata encoding and enables lossless decoding of the JPEG image.</span></span> <span data-ttu-id="5fce6-151">Кроме того, можно использовать другое значение **викдекодеоптионс** , WICDecodeMetadataCacheOnLoad, которое кэширует внедренные метаданные изображения сразу после загрузки изображения.</span><span class="sxs-lookup"><span data-stu-id="5fce6-151">Alternatively, you could use the other **WICDecodeOptions** value, WICDecodeMetadataCacheOnLoad, which caches the embedded image metadata as soon as the image is loaded.</span></span>

<span data-ttu-id="5fce6-152">Чтобы получить средство чтения запросов кадра, выполните простой вызов метода **жетметадатакуериреадер** в кадре.</span><span class="sxs-lookup"><span data-stu-id="5fce6-152">To obtain the frame's query reader, make a simple call to the frame's **GetMetadataQueryReader** method.</span></span> <span data-ttu-id="5fce6-153">Этот вызов демонстрируется в следующем коде.</span><span class="sxs-lookup"><span data-stu-id="5fce6-153">The following code demonstrates this call.</span></span>


```
// Get the query reader
if (SUCCEEDED(hr))
{
    hr = pFrameDecode->GetMetadataQueryReader(&pQueryReader);
}
```



<span data-ttu-id="5fce6-154">Аналогичным образом средство чтения запросов также может быть получено на уровне декодера.</span><span class="sxs-lookup"><span data-stu-id="5fce6-154">Similarly, a query reader can also be obtained at the decoder level.</span></span> <span data-ttu-id="5fce6-155">Простой вызов метода **жетметадатакуериреадер** декодера получает средство чтения запросов декодера.</span><span class="sxs-lookup"><span data-stu-id="5fce6-155">A simple call to the decoder's **GetMetadataQueryReader** method gets the decoder's query reader.</span></span> <span data-ttu-id="5fce6-156">Средство чтения запросов декодера, в отличие от средства чтения запросов кадра, считывает метаданные для изображения, находящегося за пределами отдельных кадров.</span><span class="sxs-lookup"><span data-stu-id="5fce6-156">An decoder's query reader, unlike a frame's query reader, reads metadata for an image that is outside of the individual frames.</span></span> <span data-ttu-id="5fce6-157">Однако этот сценарий не является распространенным, и форматы образов в машинном код не поддерживают эту возможность.</span><span class="sxs-lookup"><span data-stu-id="5fce6-157">However, this scenario is not common, and the native image formats do not support this capability.</span></span> <span data-ttu-id="5fce6-158">КОДЕки машинных образов, предоставляемые компонентом WIC, считывают и записывают метаданные на уровне фрейма даже для однокадровых форматов, таких как JPEG.</span><span class="sxs-lookup"><span data-stu-id="5fce6-158">The native image CODECS provided by WIC read and write metadata at the frame level even for single-frame formats such as JPEG.</span></span>

### <a name="reading-metadata"></a><span data-ttu-id="5fce6-159">Чтение метаданных</span><span class="sxs-lookup"><span data-stu-id="5fce6-159">Reading Metadata</span></span>

<span data-ttu-id="5fce6-160">Прежде чем перейти к фактической прочтению метаданных, ознакомьтесь со следующей схемой файла JPEG, включающего в себя внедренные блоки метаданных и реальные данные для извлечения.</span><span class="sxs-lookup"><span data-stu-id="5fce6-160">Before you move on to actually reading metadata, look at the following diagram of a JPEG file that includes embedded metadata blocks and actual data to retrieve.</span></span> <span data-ttu-id="5fce6-161">Эта диаграмма предоставляет выноски для конкретных блоков метаданных и элементов внутри изображения, предоставляющего выражение запроса метаданных каждому блоку или элементу.</span><span class="sxs-lookup"><span data-stu-id="5fce6-161">This diagram provides callouts to specific metadata blocks and items within the image providing the metadata query expression to each block or item.</span></span>

![Иллюстрация изображения JPEG с выносками метаданных](graphics/jpegwithcallouts.png)

<span data-ttu-id="5fce6-163">Чтобы запросить внедренные блоки метаданных или определенные элементы по имени, вызовите метод **жетметадатабинаме** .</span><span class="sxs-lookup"><span data-stu-id="5fce6-163">To query for embedded metadata blocks or specific items by name, call the **GetMetadataByName** method.</span></span> <span data-ttu-id="5fce6-164">Этот метод принимает выражение запроса и [пропвариант](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) , в котором возвращается элемент метаданных.</span><span class="sxs-lookup"><span data-stu-id="5fce6-164">This method takes a query expression and a [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) in which the metadata item is returned.</span></span> <span data-ttu-id="5fce6-165">Следующий код запрашивает вложенный блок метаданных и преобразует компонент [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) , предоставленный значением пропвариант, в средство чтения запросов, если оно найдено.</span><span class="sxs-lookup"><span data-stu-id="5fce6-165">The following code queries for a nested metadata block and converts the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) component provided by the PROPVARIANT value to a query reader if found.</span></span>


```
if (SUCCEEDED(hr))
{
    // Get the nested IFD reader
    hr = pQueryReader->GetMetadataByName(L"/app1/ifd", &value);
    if (value.vt == VT_UNKNOWN)
    {
        hr = value.punkVal->QueryInterface(IID_IWICMetadataQueryReader, (void **)&pEmbedReader);
    }
    PropVariantClear(&value); // Clear value for new query
}
```



<span data-ttu-id="5fce6-166">Выражение запроса "/APP1/IFD" запрашивает блок IFD, вложенный в блок App1.</span><span class="sxs-lookup"><span data-stu-id="5fce6-166">The query expression "/app1/ifd" is querying for the IFD block nested in the App1 block.</span></span> <span data-ttu-id="5fce6-167">Файл изображения JPEG содержит вложенный блок метаданных IFD, поэтому [пропвариант](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) возвращается с типом переменной (VT) `VT_UNKNOWN` и указателем на интерфейс [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) (пунквал).</span><span class="sxs-lookup"><span data-stu-id="5fce6-167">The JPEG image file contains the IFD nested metadata block, so the [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) is returned with a variable type (vt) of `VT_UNKNOWN` and a pointer to an [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface (punkVal).</span></span> <span data-ttu-id="5fce6-168">Затем вы запрашиваете интерфейс IUnknown для читателя запросов.</span><span class="sxs-lookup"><span data-stu-id="5fce6-168">You then query the IUnknown interface for a query reader.</span></span>

<span data-ttu-id="5fce6-169">В следующем коде показан новый запрос, основанный на новом модуле чтения запросов, относительно вложенного блока IFD.</span><span class="sxs-lookup"><span data-stu-id="5fce6-169">The following code demonstrates a new query based on the new query reader relative to the nested IFD block.</span></span>


```
if (SUCCEEDED(hr))
{
    hr = pEmbedReader->GetMetadataByName(L"/{ushort=18249}", &value);
    PropVariantClear(&value); // Clear value for new query
}
```



<span data-ttu-id="5fce6-170">Выражение запроса "/{ушорт = 18249}" запрашивает блок IFD для рейтинга Микрософтфото, внедренного в тег 18249.</span><span class="sxs-lookup"><span data-stu-id="5fce6-170">The query expression "/{ushort=18249}" queries the IFD block for the MicrosoftPhoto rating embedded under tag 18249.</span></span> <span data-ttu-id="5fce6-171">Значение [пропвариант](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) теперь будет содержать тип значения `VT_UI2` и значение данных 50.</span><span class="sxs-lookup"><span data-stu-id="5fce6-171">The [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) value will now contain a value type of `VT_UI2` and a data value of 50.</span></span>

<span data-ttu-id="5fce6-172">Однако нет необходимости получать вложенный блок перед запросом конкретных значений данных.</span><span class="sxs-lookup"><span data-stu-id="5fce6-172">However, it is not necessary to obtain a nested block before querying for specific data values.</span></span> <span data-ttu-id="5fce6-173">Например, вместо запроса вложенной IFD, а затем для оценки Микрософтфото можно использовать корневой блок метаданных и запрос, показанный в следующем коде, для получения той же информации.</span><span class="sxs-lookup"><span data-stu-id="5fce6-173">For instance, instead of querying for the nested IFD and then for the MicrosoftPhoto rating, you can instead use the root metadata block and the query shown in the following code to obtain the same information.</span></span>


```
if (SUCCEEDED(hr))
{
    hr = pQueryReader->GetMetadataByName(L"/app1/ifd/{ushort=18249}", &value);
    PropVariantClear(&value);
}
```



<span data-ttu-id="5fce6-174">Помимо запроса конкретных элементов метаданных в блоке метаданных, можно также перечислить все элементы метаданных в блоке метаданных (не включая элементы метаданных во вложенных блоках метаданных).</span><span class="sxs-lookup"><span data-stu-id="5fce6-174">In addition to querying for specific metadata items in a metadata block, you can also enumerate all the metadata items in a metadata block (not including metadata items in nested metadata blocks).</span></span> <span data-ttu-id="5fce6-175">Для перечисления элементов метаданных в текущем блоке **используется метод GetEnumerator** средства чтения запросов.</span><span class="sxs-lookup"><span data-stu-id="5fce6-175">To enumerate the metadata items in the current block, the query reader's **GetEnumeration** method is used.</span></span> <span data-ttu-id="5fce6-176">Этот метод получает интерфейс **иенумстринг** , заполненный элементами метаданных в текущем блоке.</span><span class="sxs-lookup"><span data-stu-id="5fce6-176">This method obtains an **IEnumString** interface populated with the metadata items in the current block.</span></span> <span data-ttu-id="5fce6-177">Например, следующий код выполняет перечисление оценки XMP и Микрософтфото для вложенного блока IFD, полученного ранее.</span><span class="sxs-lookup"><span data-stu-id="5fce6-177">For example, the following code enumerates the XMP rating and MicrosoftPhoto rating for the nested IFD block that was obtained earlier.</span></span>


```
IEnumString *metadataItems = NULL;

if (SUCCEEDED(hr))
{
    hr = pEmbedReader->GetEnumerator(&metadataItems);
}
```



<span data-ttu-id="5fce6-178">Дополнительные сведения об определении подходящих тегов для различных форматов изображений и форматов метаданных см. в разделе [запросы метаданных в формате образа в машинном код](-wic-native-image-format-metadata-queries.md).</span><span class="sxs-lookup"><span data-stu-id="5fce6-178">For more information on identifying appropriate tags for various image formats and metadata formats, see [Native Image Format Metadata Queries](-wic-native-image-format-metadata-queries.md).</span></span>

### <a name="additional-query-reader-methods"></a><span data-ttu-id="5fce6-179">Дополнительные методы чтения запросов</span><span class="sxs-lookup"><span data-stu-id="5fce6-179">Additional Query Reader Methods</span></span>

<span data-ttu-id="5fce6-180">Помимо чтения метаданных можно также получить дополнительные сведения о средстве чтения запросов и получить метаданные с помощью других средств.</span><span class="sxs-lookup"><span data-stu-id="5fce6-180">In addition to reading metadata, you can also obtain additional information about the query reader and obtain metadata through other means.</span></span> <span data-ttu-id="5fce6-181">Средство чтения запросов предоставляет два метода, которые предоставляют сведения о модуле чтения и **жетконтаинерформат** запросов **.**</span><span class="sxs-lookup"><span data-stu-id="5fce6-181">The query reader provides two methods that provide information about the query reader, **GetContainerFormat** and **GetLocation**.</span></span>

<span data-ttu-id="5fce6-182">С помощью встроенного средства чтения запросов можно использовать **жетконтаинерформат** , чтобы определить тип блока метаданных, и можно вызвать метод **OnLocation** , чтобы получить путь относительно корневого блока метаданных.</span><span class="sxs-lookup"><span data-stu-id="5fce6-182">With the embedded query reader, you can use **GetContainerFormat** to determine the type of metadata block, and you can call **GetLocation** to obtain the path relative to the root metadata block.</span></span> <span data-ttu-id="5fce6-183">Следующий код запрашивает у встроенного модуля чтения запросов для своего расположения.</span><span class="sxs-lookup"><span data-stu-id="5fce6-183">The following code queries the embedded query reader for its location.</span></span>


```
// Determine the metadata block format

if (SUCCEEDED(hr))
{
    hr = pEmbedReader->GetContainerFormat(&containerGUID);
}

// Determine the query reader's location
if (SUCCEEDED(hr))
{
    UINT length;
    WCHAR readerNamespace[100];
    hr = pEmbedReader->GetLocation(100, readerNamespace, &length);
}
```



<span data-ttu-id="5fce6-184">Вызов **жетконтаинерформат** для встроенного средства чтения запросов возвращает идентификатор GUID формата метаданных IFD.</span><span class="sxs-lookup"><span data-stu-id="5fce6-184">The call to **GetContainerFormat** for the embedded query reader returns the IFD metadata format GUID.</span></span> <span data-ttu-id="5fce6-185">Вызов метода **OnLocation** Возвращает пространство имен "/APP1/IFD"; предоставляя относительный путь, из которого будут выполняться последующие запросы к новому модулю чтения запросов.</span><span class="sxs-lookup"><span data-stu-id="5fce6-185">The call to **GetLocation** returns a namespace of "/app1/ifd"; providing you with the relative path from which subsequent queries to the new query reader will be executed.</span></span> <span data-ttu-id="5fce6-186">Разумеется, приведенный выше код не очень полезен, но в нем демонстрируется использование метода методического **размещения** для поиска вложенных блоков метаданных.</span><span class="sxs-lookup"><span data-stu-id="5fce6-186">Of course, the preceding code isn't very useful, but it does demonstrate how to use the **GetLocation** method for finding nested metadata blocks.</span></span>

## <a name="writing-metadata-using-a-query-writer"></a><span data-ttu-id="5fce6-187">Запись метаданных с помощью модуля записи запроса</span><span class="sxs-lookup"><span data-stu-id="5fce6-187">Writing Metadata Using a Query Writer</span></span>

> [!Note]  
> <span data-ttu-id="5fce6-188">Некоторые примеры кода, приведенные в этом разделе, не показаны в контексте фактических шагов, необходимых для записи метаданных.</span><span class="sxs-lookup"><span data-stu-id="5fce6-188">Some of the code examples provided in this section are not shown in the context of the actual steps required to write metadata.</span></span> <span data-ttu-id="5fce6-189">Примеры кода в контексте рабочего примера см. в статье руководство. повторное кодирование образа с помощью метаданных.</span><span class="sxs-lookup"><span data-stu-id="5fce6-189">To view the code examples in the context of a working sample, see the How-to: Re-encode an Image with Metadata tutorial.</span></span>

 

<span data-ttu-id="5fce6-190">Основным компонентом для записи метаданных является модуль записи запросов ([**ивикметадатакуеривритер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)).</span><span class="sxs-lookup"><span data-stu-id="5fce6-190">The main component for writing metadata is the query writer ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)).</span></span> <span data-ttu-id="5fce6-191">Модуль записи запросов позволяет устанавливать и удалять блоки метаданных и элементы в блоке метаданных.</span><span class="sxs-lookup"><span data-stu-id="5fce6-191">The query writer enables you to set and remove metadata blocks and items within a metadata block.</span></span>

<span data-ttu-id="5fce6-192">Как и средство чтения запросов, существует три способа получить модуль записи запроса: через растровый кодировщик ([**ивикбитмапенкодер**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)) через отдельные кадры ([**ивикбитмапфраминкоде**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)) или с помощью быстрого кодировщика метаданных ([**ивикфастметадатаенкодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)).</span><span class="sxs-lookup"><span data-stu-id="5fce6-192">Like the query reader, there are three ways to obtain a query writer: through a bitmap encoder ([**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)), through its individual frames ([**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)), or through a fast metadata encoder ([**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)).</span></span>

### <a name="obtaining-a-query-writer"></a><span data-ttu-id="5fce6-193">Получение модуля записи запроса</span><span class="sxs-lookup"><span data-stu-id="5fce6-193">Obtaining a Query Writer</span></span>

<span data-ttu-id="5fce6-194">Наиболее распространенный модуль записи запросов предназначен для отдельного кадра точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="5fce6-194">The most common query writer is for an individual frame of a bitmap.</span></span> <span data-ttu-id="5fce6-195">Этот модуль записи запросов задает и удаляет блоки и элементы метаданных фрейма изображения.</span><span class="sxs-lookup"><span data-stu-id="5fce6-195">This query writer sets and removes an image frame's metadata blocks and items.</span></span> <span data-ttu-id="5fce6-196">Чтобы получить модуль записи запроса кадра изображения, вызовите метод **жетметадатакуеривритер** в кадре.</span><span class="sxs-lookup"><span data-stu-id="5fce6-196">To obtain an image frame's query writer, call the frame's **GetMetadataQueryWriter** method.</span></span> <span data-ttu-id="5fce6-197">В следующем коде показан простой вызов метода для получения модуля записи запроса в кадре.</span><span class="sxs-lookup"><span data-stu-id="5fce6-197">The following code demonstrates the simple method call to obtain a frame's query writer.</span></span>


```
IWICMetadataQueryWriter &pFrameQWriter = NULL;

//Obtain a query writer from the frame.
hr = pFrameEncode->GetMetadataQueryWriter(&pFrameQWriter);
```



<span data-ttu-id="5fce6-198">Аналогичным образом для уровня кодировщика также может быть получен модуль записи запроса.</span><span class="sxs-lookup"><span data-stu-id="5fce6-198">Similarly, a query writer can also be obtained for the encoder level.</span></span> <span data-ttu-id="5fce6-199">Простой вызов метода **жетметадатакуеривритер** кодировщика получает модуль записи запроса кодировщика.</span><span class="sxs-lookup"><span data-stu-id="5fce6-199">A simple call to the encoder's **GetMetadataQueryWriter** method gets the encoder's query writer.</span></span> <span data-ttu-id="5fce6-200">Модуль записи запросов кодировщика, в отличие от модуля записи запроса кадра, записывает метаданные для изображения за пределами отдельного кадра.</span><span class="sxs-lookup"><span data-stu-id="5fce6-200">An encoder's query writer, unlike a frame's query writer, writes metadata for an image outside of the individual frame.</span></span> <span data-ttu-id="5fce6-201">Однако этот сценарий не является распространенным, и форматы образов в машинном код не поддерживают эту возможность.</span><span class="sxs-lookup"><span data-stu-id="5fce6-201">However, this scenario is not common, and the native image formats do not support this capability.</span></span> <span data-ttu-id="5fce6-202">Кодеки машинных образов, предоставляемые компонентом WIC, считывают и записывают метаданные на уровне фрейма даже для однокадровых форматов, таких как JPEG.</span><span class="sxs-lookup"><span data-stu-id="5fce6-202">The native image codecs provided by WIC read and write metadata at the frame level even for single-frame formats such as JPEG.</span></span>

<span data-ttu-id="5fce6-203">Кроме того, модуль записи запросов можно получить непосредственно из фабрики изображений ([**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)).</span><span class="sxs-lookup"><span data-stu-id="5fce6-203">You can also obtain a query writer directly from the imaging factory ([**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)).</span></span> <span data-ttu-id="5fce6-204">Существует два метода фабрики изображений, которые возвращают модуль записи запроса: **креатекуеривритер** и **креатекуеривритерфромреадер**.</span><span class="sxs-lookup"><span data-stu-id="5fce6-204">There are two imaging factory methods that return a query writer: **CreateQueryWriter** and **CreateQueryWriterFromReader**.</span></span>

<span data-ttu-id="5fce6-205">**Креатекуеривритер** создает модуль записи запроса для указанного формата метаданных и поставщика.</span><span class="sxs-lookup"><span data-stu-id="5fce6-205">**CreateQueryWriter** creates a query writer for the specified metadata format and vendor.</span></span> <span data-ttu-id="5fce6-206">Этот модуль записи запросов позволяет создавать метаданные для определенного формата метаданных и добавлять их в образ.</span><span class="sxs-lookup"><span data-stu-id="5fce6-206">This query writer enables you to write metadata for a specific metadata format and add it to the image.</span></span> <span data-ttu-id="5fce6-207">В следующем примере кода демонстрируется вызов **креатекуеривритер** для создания модуля записи запроса XMP.</span><span class="sxs-lookup"><span data-stu-id="5fce6-207">The following code demonstrates a **CreateQueryWriter** call to create an XMP query writer.</span></span>


```
IWICMetadataQueryWriter *pXMPWriter = NULL;

// Create XMP block
GUID vendor = GUID_VendorMicrosoft;
hr = pFactory->CreateQueryWriter(
        GUID_MetadataFormatXMP,
        &vendor,
        &pXMPWriter);
```



<span data-ttu-id="5fce6-208">В этом примере понятное имя `GUID_MetadataFormatXMP` используется в качестве параметра *гуидметадатаформат* .</span><span class="sxs-lookup"><span data-stu-id="5fce6-208">In this example, the friendly name `GUID_MetadataFormatXMP` is used as the *guidMetadataFormat* parameter.</span></span> <span data-ttu-id="5fce6-209">Он представляет идентификатор GUID формата метаданных XMP, а поставщик представляет обработчик, созданный корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="5fce6-209">It represents the XMP metadata format GUID, and vendor represents the Microsoft created handler.</span></span> <span data-ttu-id="5fce6-210">Кроме того, **значение NULL** может быть передано как параметр *пгуидвендор* с теми же результатами, если другие обработчики XMP не существуют.</span><span class="sxs-lookup"><span data-stu-id="5fce6-210">Alternatively, **NULL** can be passed as the *pguidVendor* parameter with the same results if no other XMP handler exists.</span></span> <span data-ttu-id="5fce6-211">Если пользовательский обработчик XMP устанавливается вместе с собственным обработчиком XMP, передача **значения NULL** для поставщика приведет к тому, что модуль записи с самым низким идентификатором GUID будет возвращен.</span><span class="sxs-lookup"><span data-stu-id="5fce6-211">If a custom XMP handler is installed alongside the native XMP handler, passing **NULL** for the vendor will result in the query writer with the lowest GUID being returned.</span></span>

<span data-ttu-id="5fce6-212">**Креатекуеривритерфромреадер** аналогичен методу **креатекуеривритер** , за исключением того, что он заполняет новый модуль записи запросов данными, предоставленными модулем чтения запросов.</span><span class="sxs-lookup"><span data-stu-id="5fce6-212">**CreateQueryWriterFromReader** is similar to the **CreateQueryWriter** method except that it prepopulates the new query writer with the data provided by the query reader.</span></span> <span data-ttu-id="5fce6-213">Это полезно для повторного кодирования образа с сохранением существующих метаданных или удаления ненужных метаданных.</span><span class="sxs-lookup"><span data-stu-id="5fce6-213">This is useful for re-encoding an image while maintaining the existing metadata, or for removing unwanted metadata.</span></span> <span data-ttu-id="5fce6-214">В следующем коде демонстрируется вызов **креатекуеривритерфромреадер** .</span><span class="sxs-lookup"><span data-stu-id="5fce6-214">The following code demonstrates a **CreateQueryWriterFromReader** call.</span></span>


```
hr = pFrameDecode->GetMetadataQueryReader(&pFrameQReader);

// Copy metadata using query readers
if(SUCCEEDED(hr) && pFrameQReader)
{
    IWICMetadataQueryWriter *pNewWriter = NULL;

    GUID vendor = GUID_VendorMicrosoft;
    hr = pFactory->CreateQueryWriterFromReader(
        pFrameQReader,
        &vendor,
        &pNewWriter);
```



### <a name="adding-metadata"></a><span data-ttu-id="5fce6-215">Добавление метаданных</span><span class="sxs-lookup"><span data-stu-id="5fce6-215">Adding Metadata</span></span>

<span data-ttu-id="5fce6-216">После получения модуля записи запроса его можно использовать для добавления блоков и элементов метаданных.</span><span class="sxs-lookup"><span data-stu-id="5fce6-216">After you obtain a query writer, you can use it to add metadata blocks and items.</span></span> <span data-ttu-id="5fce6-217">Для записи метаданных используется метод **сетметадатабинаме** модуля записи запроса.</span><span class="sxs-lookup"><span data-stu-id="5fce6-217">To write metadata, you use the query writer's **SetMetadataByName** method.</span></span> <span data-ttu-id="5fce6-218">**Сетметадатабинаме** принимает два параметра: выражение запроса (*взнаме*) и указатель на [пропвариант](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) (*сервер*).</span><span class="sxs-lookup"><span data-stu-id="5fce6-218">**SetMetadataByName** takes two parameters: a query expression (*wzName*) and a pointer to a [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) (*pvarValue*).</span></span> <span data-ttu-id="5fce6-219">Выражение запроса определяет блок или элемент, который необходимо задать, когда ПРОПВАРИАНТ предоставляет фактическое значение данных для установки.</span><span class="sxs-lookup"><span data-stu-id="5fce6-219">The query expression defines the block or item to set while the PROPVARIANT provides the actual data value to set.</span></span>

<span data-ttu-id="5fce6-220">В следующем примере показано, как добавить заголовок с помощью модуля записи запросов XMP, полученного ранее с помощью метода **креатекуеривритер** .</span><span class="sxs-lookup"><span data-stu-id="5fce6-220">The following example demonstrates how to add a title by using the XMP query writer previously obtained by using the **CreateQueryWriter** method.</span></span>


```
// Write metadata to the XMP writer
if (SUCCEEDED(hr))
{
    PROPVARIANT value;
    PropVariantInit(&value);

    value.vt = VT_LPWSTR;
    value.pwszVal = L"Metadata Test Image.";
   
    hr = pXMPWriter->SetMetadataByName(L"/dc:title", &value);

    PropVariantClear(&value);
}
```



<span data-ttu-id="5fce6-221">В этом примере тип значения (VT) имеет значение `VT_LPWSTR` , указывающее, что строка будет использоваться в качестве значения данных.</span><span class="sxs-lookup"><span data-stu-id="5fce6-221">In this example, value's type (vt) is set to `VT_LPWSTR`, indicating that a string will be used as the data value.</span></span> <span data-ttu-id="5fce6-222">Так как тип *значения*— это строка, *пвсзвал* используется для задания заголовка.</span><span class="sxs-lookup"><span data-stu-id="5fce6-222">Because *value*'s type is a string, *pwszVal* is used to set the title to use.</span></span> <span data-ttu-id="5fce6-223">Затем **сетметадатабинаме** вызывается с помощью выражения запроса "/DC: Title" и только что установленного [пропвариант](/windows/win32/api/propidlbase/ns-propidlbase-propvariant).</span><span class="sxs-lookup"><span data-stu-id="5fce6-223">**SetMetadataByName** is then called using the query expression "/dc:title" and the newly set [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant).</span></span> <span data-ttu-id="5fce6-224">Используемое выражение запроса указывает, что должно быть задано свойство Title в схеме цифровой камеры (DC).</span><span class="sxs-lookup"><span data-stu-id="5fce6-224">The query expression used indicates that the title property in the digital camera (dc) schema should be set.</span></span> <span data-ttu-id="5fce6-225">Обратите внимание, что выражение не имеет значение "/КСМП/ДК: Title"; Это связано с тем, что модуль записи запросов уже связан с XMP и не содержит внедренный блок XMP, который предложит «/КСМП/ДК: Title».</span><span class="sxs-lookup"><span data-stu-id="5fce6-225">Note that the expression is not "/xmp/dc:title"; this is because the query writer is already specific to XMP and does not contain an embedded XMP block, which "/xmp/dc:title" would suggest.</span></span>

<span data-ttu-id="5fce6-226">До этого момента вы не добавили метаданные в кадр изображения.</span><span class="sxs-lookup"><span data-stu-id="5fce6-226">Up to this point you haven't actually added any metadata to an image frame.</span></span> <span data-ttu-id="5fce6-227">Вы просто заполнили модуль записи запросов данными.</span><span class="sxs-lookup"><span data-stu-id="5fce6-227">You've simply populated a query writer with data.</span></span> <span data-ttu-id="5fce6-228">Чтобы добавить в кадр блок метаданных, представленный модулем записи запроса, снова вызовите **сетметадатабинаме** , используя модуль записи запроса в качестве значения [пропвариант](/windows/win32/api/propidlbase/ns-propidlbase-propvariant).</span><span class="sxs-lookup"><span data-stu-id="5fce6-228">To add to a frame a metadata block represented by the query writer, you again call **SetMetadataByName** using the query writer as the value of the [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant).</span></span> <span data-ttu-id="5fce6-229">Это эффективно копирует метаданные из модуля записи запроса в кадр изображения.</span><span class="sxs-lookup"><span data-stu-id="5fce6-229">This effectively copies the metadata in the query writer to the image frame.</span></span> <span data-ttu-id="5fce6-230">В следующем коде показано, как добавить метаданные в модуль записи запросов XMP, ранее полученный в корневой блок метаданных фрейма.</span><span class="sxs-lookup"><span data-stu-id="5fce6-230">The following code demonstrates how to add the metadata in the XMP query writer previously obtained to a frame's root metadata block.</span></span>


```
// Get the frame's query writer and write the XMP query writer to it
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->GetMetadataQueryWriter(&pFrameQWriter);

    // Copy the metadata in the XMP query writer to the frame
    if (SUCCEEDED(hr))
    {
        PROPVARIANT value;

        PropVariantInit(&value);
        value.vt = VT_UNKNOWN;
        value.punkVal = pXMPWriter;
        value.punkVal->AddRef();

        hr = pFrameQWriter->SetMetadataByName(L"/", &value);

        PropVariantClear(&value);
    }
}
```



<span data-ttu-id="5fce6-231">В этом примере используется тип значения (VT), `VT_UNKOWN` указывающий тип значения COM-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="5fce6-231">In this example, a value type (vt) of `VT_UNKOWN` is used; indicating a COM interface value type.</span></span> <span data-ttu-id="5fce6-232">Затем в качестве значения [пропвариант](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)используется модуль записи запросов XMP (пиксмпвритер), который добавляет ссылку на него с помощью метода AddRef.</span><span class="sxs-lookup"><span data-stu-id="5fce6-232">The XMP query writer (piXMPWriter) is then used as the value of the [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant), adding a reference to it by using the AddRef method.</span></span> <span data-ttu-id="5fce6-233">Наконец, модуль записи запросов XMP задается путем вызова метода **сетметадатабинаме** фрейма и передачи выражения запроса "/", указывающего на корневой блок, а также только что установленный пропвариант.</span><span class="sxs-lookup"><span data-stu-id="5fce6-233">Finally, the XMP query writer is set by calling the frame's **SetMetadataByName** method and passing the query expression "/", indicating the root block, and the newly set PROPVARIANT.</span></span>

> [!Note]  
> <span data-ttu-id="5fce6-234">Если в рамке уже содержится блок метаданных, который вы пытаетесь добавить, то добавляемые метаданные будут добавлены, а существующие метаданные перезаписаны.</span><span class="sxs-lookup"><span data-stu-id="5fce6-234">If the frame already contains the metadata block you are trying to add, the metadata you are adding will be added and existing metadata overwritten.</span></span>

 

### <a name="removing-metadata"></a><span data-ttu-id="5fce6-235">Удаление метаданных</span><span class="sxs-lookup"><span data-stu-id="5fce6-235">Removing Metadata</span></span>

<span data-ttu-id="5fce6-236">Кроме того, модуль записи запросов позволяет удалять метаданные путем вызова метода **ремовеметадатабинаме** .</span><span class="sxs-lookup"><span data-stu-id="5fce6-236">A query writer also enables you to remove metadata by calling the **RemoveMetadataByName** method.</span></span> <span data-ttu-id="5fce6-237">**Ремовеметадатабинаме** принимает выражение запроса и удаляет блок метаданных или элемент, если он существует.</span><span class="sxs-lookup"><span data-stu-id="5fce6-237">**RemoveMetadataByName** takes a query expression and removes the metadata block or item if it exists.</span></span> <span data-ttu-id="5fce6-238">В следующем коде показано, как удалить добавленный ранее заголовок.</span><span class="sxs-lookup"><span data-stu-id="5fce6-238">The following code demonstrates how to remove the title that was previously added.</span></span>


```
if (SUCCEEDED(hr))
{
    hr = pFrameQWriter->RemoveMetadataByName(L"/xmp/dc:title");
}
```



<span data-ttu-id="5fce6-239">В следующем коде показано, как удалить весь блок метаданных XMP.</span><span class="sxs-lookup"><span data-stu-id="5fce6-239">The following code demonstrates how to remove the entire XMP metadata block.</span></span>


```
if (SUCCEEDED(hr))
{
    hr = pFrameQWriter->RemoveMetadataByName(L"/xmp");
}
```



### <a name="copying-metadata-for-re-encoding"></a><span data-ttu-id="5fce6-240">Копирование метаданных для повторной кодировки</span><span class="sxs-lookup"><span data-stu-id="5fce6-240">Copying Metadata for Re-encoding</span></span>

> [!Note]  
> <span data-ttu-id="5fce6-241">Код в этом разделе действителен, только если форматы исходного и конечного изображений совпадают.</span><span class="sxs-lookup"><span data-stu-id="5fce6-241">The code in this section is valid only when the source and destination image formats are the same.</span></span> <span data-ttu-id="5fce6-242">Невозможно скопировать все метаданные изображения в одной операции при кодировании в другой формат изображения.</span><span class="sxs-lookup"><span data-stu-id="5fce6-242">You cannot copy all of an image's metadata in a single operation when encoding to a different image format.</span></span>

 

<span data-ttu-id="5fce6-243">Для сохранения метаданных при повторном кодировании изображения в тот же формат изображения существуют методы, доступные для копирования всех метаданных в одной операции.</span><span class="sxs-lookup"><span data-stu-id="5fce6-243">To preserve metadata while re-encoding an image to the same image format, there are methods available for copying all the metadata in a single operation.</span></span> <span data-ttu-id="5fce6-244">Каждая из этих операций соответствует аналогичному шаблону. Каждый из них устанавливает метаданные декодированного кадра непосредственно в новый закодированный кадр.</span><span class="sxs-lookup"><span data-stu-id="5fce6-244">Each of these operations follows a similar pattern; each sets the decoded frame's metadata directly into the new frame being encoded.</span></span>

<span data-ttu-id="5fce6-245">Предпочтительным методом копирования метаданных является инициализация модуля записи блока нового кадра с помощью модуля чтения блоков декодированного кадра.</span><span class="sxs-lookup"><span data-stu-id="5fce6-245">The preferred method to copy metadata is to initialize the new frame's block writer with the decoded frame's block reader.</span></span> <span data-ttu-id="5fce6-246">Этот метод показан в следующем коде.</span><span class="sxs-lookup"><span data-stu-id="5fce6-246">The following code demonstrates this method.</span></span>


```
if (SUCCEEDED(hr) && formatsEqual)
{
    // Copy metadata using metadata block reader/writer
    if (SUCCEEDED(hr))
    {
        pFrameDecode->QueryInterface(
            IID_IWICMetadataBlockReader,
            (void**)&pBlockReader);
    }
    if (SUCCEEDED(hr))
    {
        pFrameEncode->QueryInterface(
            IID_IWICMetadataBlockWriter,
            (void**)&pBlockWriter);
    }
    if (SUCCEEDED(hr))
    {
        pBlockWriter->InitializeFromBlockReader(pBlockReader);
    }
}
```



<span data-ttu-id="5fce6-247">В этом примере модуль чтения блока и модуль записи блока получаются из исходного фрейма и конечного фрейма соответственно.</span><span class="sxs-lookup"><span data-stu-id="5fce6-247">In this example, the block reader and the block writer are obtained from the source frame and destination frame, respectively.</span></span> <span data-ttu-id="5fce6-248">Затем модуль записи блока инициализируется модулем чтения блока.</span><span class="sxs-lookup"><span data-stu-id="5fce6-248">The block writer is then initialized from the block reader.</span></span> <span data-ttu-id="5fce6-249">При этом модуль чтения блока инициализируется предварительно заполненными метаданными модуля чтения блока.</span><span class="sxs-lookup"><span data-stu-id="5fce6-249">This initializes the block reader with the pre-populated metadata of the block reader.</span></span>

<span data-ttu-id="5fce6-250">Другим методом копирования метаданных является запись блока метаданных, на который ссылается средство чтения запросов, с помощью модуля записи запроса кодировщика.</span><span class="sxs-lookup"><span data-stu-id="5fce6-250">Another method to copy metadata is to write the metadata block referenced by the query reader using the encoder's query writer.</span></span> <span data-ttu-id="5fce6-251">Этот метод показан в следующем коде.</span><span class="sxs-lookup"><span data-stu-id="5fce6-251">The following code demonstrates this method.</span></span>


```
if (SUCCEEDED(hr) && formatsEqual)
{
    hr = pFrameDecode->GetMetadataQueryReader(&pFrameQReader);

    // Copy metadata using query readers
    if(SUCCEEDED(hr))
    {
        hr = pFrameEncode->GetMetadataQueryWriter(&pFrameQWriter);
        if (SUCCEEDED(hr))
        {
            PropVariantClear(&value);
            value.vt=VT_UNKNOWN;
            value.punkVal=pFrameQReader;
            value.punkVal->AddRef();
            hr = pFrameQWriter->SetMetadataByName(L"/", &value);
            PropVariantClear(&value);
        }
    }
}
```



<span data-ttu-id="5fce6-252">Здесь средство чтения запросов получается из декодированного фрейма, а затем используется в качестве значения свойства [пропвариант](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) с типом значения VT \_ Unknown.</span><span class="sxs-lookup"><span data-stu-id="5fce6-252">Here, a query reader is obtained from the decoded frame and then used as the property value of the [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) with a value type set to VT\_UNKNOWN.</span></span> <span data-ttu-id="5fce6-253">Модуль записи запроса для кодировщика получен, а выражение запроса "/" используется для задания метаданных по корневому пути навигации.</span><span class="sxs-lookup"><span data-stu-id="5fce6-253">The query writer for the encoder is obtained and the query expression "/" is used to set the metadata at the root navigation path.</span></span> <span data-ttu-id="5fce6-254">Этот метод также можно использовать при задании вложенных блоков метаданных путем настройки выражения запроса в нужное место.</span><span class="sxs-lookup"><span data-stu-id="5fce6-254">You can also use this method when setting nested metadata blocks, by adjusting the query expression to the desired location.</span></span>

<span data-ttu-id="5fce6-255">Аналогичным образом можно создать модуль записи запроса на основе средства чтения запросов декодированного кадра с помощью метода **креатекуеривритерфромреадер** фабрики изображений.</span><span class="sxs-lookup"><span data-stu-id="5fce6-255">Similarly, you can create a query writer based on the decoded frame's query reader by using the imaging factory's **CreateQueryWriterFromReader** method.</span></span> <span data-ttu-id="5fce6-256">Модуль записи запросов, созданный в этой операции, будет предварительно заполнен метаданными из средства чтения запросов и затем может быть задан в кадре.</span><span class="sxs-lookup"><span data-stu-id="5fce6-256">The query writer created in this operation will be prepopulated with the metadata from the query reader and can then be set in the frame.</span></span> <span data-ttu-id="5fce6-257">В следующем примере кода демонстрируется операция копирования **креатекуеривритерфромреадер** .</span><span class="sxs-lookup"><span data-stu-id="5fce6-257">The following code demonstrates the **CreateQueryWriterFromReader** copy operation.</span></span>


```
IWICMetadataQueryWriter *pNewWriter = NULL;

GUID vendor = GUID_VendorMicrosoft;
hr = pFactory->CreateQueryWriterFromReader(
    pFrameQReader,
    &vendor,
    &pNewWriter);

if (SUCCEEDED(hr))
{
    // Get the frame's query writer
    hr = pFrameEncode->GetMetadataQueryWriter(&pFrameQWriter);
}

// Set the query writer to the frame.
if (SUCCEEDED(hr))
{
    PROPVARIANT value;

    PropVariantInit(&value);
    value.vt = VT_UNKNOWN;
    value.punkVal = pNewWriter;
    value.punkVal->AddRef();
    hr = pFrameQWriter->SetMetadataByName(L"/",&value);
}
```



<span data-ttu-id="5fce6-258">В этом методе создается отдельный модуль записи запросов, основанный на данных средства чтения запросов.</span><span class="sxs-lookup"><span data-stu-id="5fce6-258">This method uses a separate query writer is created that is based on the data of the query reader.</span></span> <span data-ttu-id="5fce6-259">Этот новый модуль записи запросов, затем задается в кадре.</span><span class="sxs-lookup"><span data-stu-id="5fce6-259">This new query writer then set in the frame.</span></span>

<span data-ttu-id="5fce6-260">Опять же, эти операции копирования метаданных работают только в том случае, если исходные и конечные образы имеют одинаковый формат.</span><span class="sxs-lookup"><span data-stu-id="5fce6-260">Again, these operations to copy metadata only work when the source and destination images have the same format.</span></span> <span data-ttu-id="5fce6-261">Это обусловлено тем, что различные форматы изображений хранят блоки метаданных в разных местах.</span><span class="sxs-lookup"><span data-stu-id="5fce6-261">This is because different image formats store the metadata blocks in different locations.</span></span> <span data-ttu-id="5fce6-262">Например, JPEG и TIFF поддерживают блоки метаданных XMP.</span><span class="sxs-lookup"><span data-stu-id="5fce6-262">For instance, both JPEG and TIFF support XMP metadata blocks.</span></span> <span data-ttu-id="5fce6-263">В изображениях JPEG блок XMP находится в корневом блоке метаданных, как показано в разделе [Общие сведения о метаданных WIC](-wic-about-metadata.md).</span><span class="sxs-lookup"><span data-stu-id="5fce6-263">In JPEG images, the XMP block is at the root metadata block as illustrated in the [WIC Metadata Overview](-wic-about-metadata.md).</span></span> <span data-ttu-id="5fce6-264">Однако в изображении TIFF блок XMP вложен в корневой блок IFD.</span><span class="sxs-lookup"><span data-stu-id="5fce6-264">However, in a TIFF image, the XMP block is nested in a root IFD block.</span></span> <span data-ttu-id="5fce6-265">На следующей схеме показаны различия между изображением JPEG и изображением TIFF с одинаковыми метаданными рейтинга.</span><span class="sxs-lookup"><span data-stu-id="5fce6-265">The following diagram illustrates the differences between a JPEG image and a TIFF image with the same rating metadata.</span></span>

![Сравнение JPEG и TIFF.](graphics/jpgvstiff.png)

## <a name="fast-metadata-encoding"></a><span data-ttu-id="5fce6-267">Быстрая кодировка метаданных</span><span class="sxs-lookup"><span data-stu-id="5fce6-267">Fast Metadata Encoding</span></span>

<span data-ttu-id="5fce6-268">Не всегда требуется перекодировать образ для записи новых метаданных в него.</span><span class="sxs-lookup"><span data-stu-id="5fce6-268">It is not always necessary to re-encode an image to write new metadata to it.</span></span> <span data-ttu-id="5fce6-269">Метаданные также можно записать с помощью быстрого кодировщика метаданных.</span><span class="sxs-lookup"><span data-stu-id="5fce6-269">Metadata can also be written by using a fast metadata encoder.</span></span> <span data-ttu-id="5fce6-270">Быстрый кодировщик метаданных может записывать ограниченный объем метаданных в образ без повторной кодировки образа.</span><span class="sxs-lookup"><span data-stu-id="5fce6-270">A fast metadata encoder can write a limited amount of metadata to an image without re-encoding the image.</span></span> <span data-ttu-id="5fce6-271">Это достигается путем записи новых метаданных в пустое заполнение, предоставленное некоторыми форматами метаданных.</span><span class="sxs-lookup"><span data-stu-id="5fce6-271">This is accomplished by writing the new metadata within the empty padding provided by some metadata formats.</span></span> <span data-ttu-id="5fce6-272">Собственные форматы метаданных, поддерживающие заполнение метаданных, — это EXIF, IFD, GPS и XMP.</span><span class="sxs-lookup"><span data-stu-id="5fce6-272">The native metadata formats that support metadata padding are Exif, IFD, GPS and XMP.</span></span>

### <a name="adding-padding-to-metadata-blocks"></a><span data-ttu-id="5fce6-273">Добавление заполнения в блоки метаданных</span><span class="sxs-lookup"><span data-stu-id="5fce6-273">Adding Padding to Metadata Blocks</span></span>

<span data-ttu-id="5fce6-274">Прежде чем можно будет выполнять быструю кодировку метаданных, в блоке метаданных должно быть место для записи дополнительных метаданных.</span><span class="sxs-lookup"><span data-stu-id="5fce6-274">Before you can perform fast metadata encoding, there must be room within the metadata block to write more metadata.</span></span> <span data-ttu-id="5fce6-275">Если в рамках существующего заполнения не хватает места для записи новых метаданных, то Быстрая кодировка метаданных завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="5fce6-275">If there is not enough room within the existing padding to write the new metadata, the fast metadata encoding will fail.</span></span> <span data-ttu-id="5fce6-276">Чтобы добавить в изображение заполнение метаданных, необходимо повторно закодировать образ.</span><span class="sxs-lookup"><span data-stu-id="5fce6-276">To add metadata padding to an image, the image must be re-encoded.</span></span> <span data-ttu-id="5fce6-277">Можно добавить заполнение таким же образом, как и любой другой элемент метаданных, с помощью выражения запроса, если этот блок метаданных поддерживает заполнение.</span><span class="sxs-lookup"><span data-stu-id="5fce6-277">You can add padding the same way you would add any other metadata item, by using a query expression, if the metadata block you are padding supports it.</span></span> <span data-ttu-id="5fce6-278">В следующем примере показано, как добавить дополнение к блоку IFD, внедренному в блок App1.</span><span class="sxs-lookup"><span data-stu-id="5fce6-278">The following example demonstrates how to add padding to an IFD block embedded in an App1 block.</span></span>


```
if (SUCCEEDED(hr))
{
    // Add metadata padding
    PROPVARIANT padding;

    PropVariantInit(&padding);
    padding.vt = VT_UI4;
    padding.uiVal = 4096; // 4KB

    hr = pFrameQWriter->SetMetadataByName(L"/app1/ifd/PaddingSchema:padding", &padding);

    PropVariantClear(&padding);
}
```



<span data-ttu-id="5fce6-279">Чтобы добавить дополнение, создайте ПРОПВАРИАНТ типа VT \_ UI4 и значение, соответствующее числу байтов добавляемого дополнения.</span><span class="sxs-lookup"><span data-stu-id="5fce6-279">To add padding, create a PROPVARIANT of type VT\_UI4 and a value corresponding to the number of bytes of padding to add.</span></span> <span data-ttu-id="5fce6-280">Типичное значение — 4096 байт.</span><span class="sxs-lookup"><span data-stu-id="5fce6-280">A typical value is 4096 bytes.</span></span> <span data-ttu-id="5fce6-281">В этой таблице приведены запросы метаданных для JPEG, TIFF и JPEG-XR.</span><span class="sxs-lookup"><span data-stu-id="5fce6-281">The metadata queries for JPEG, TIFF, and JPEG-XR are in this table.</span></span>



| <span data-ttu-id="5fce6-282">Формат метаданных</span><span class="sxs-lookup"><span data-stu-id="5fce6-282">Metadata format</span></span> | <span data-ttu-id="5fce6-283">Запрос метаданных JPEG</span><span class="sxs-lookup"><span data-stu-id="5fce6-283">JPEG metadata query</span></span>                  | <span data-ttu-id="5fce6-284">TIFF, JPEG — запрос метаданных XR</span><span class="sxs-lookup"><span data-stu-id="5fce6-284">TIFF, JPEG-XR metadata query</span></span>    |
|-----------------|--------------------------------------|---------------------------------|
| <span data-ttu-id="5fce6-285">IFD</span><span class="sxs-lookup"><span data-stu-id="5fce6-285">IFD</span></span>             | <span data-ttu-id="5fce6-286">/app1/ifd/PaddingSchema: заполнение</span><span class="sxs-lookup"><span data-stu-id="5fce6-286">/app1/ifd/PaddingSchema:Padding</span></span>      | <span data-ttu-id="5fce6-287">/ИФД/паддингсчема: заполнение</span><span class="sxs-lookup"><span data-stu-id="5fce6-287">/ifd/PaddingSchema:Padding</span></span>      |
| <span data-ttu-id="5fce6-288">EXIF</span><span class="sxs-lookup"><span data-stu-id="5fce6-288">EXIF</span></span>            | <span data-ttu-id="5fce6-289">/app1/ifd/exif/PaddingSchema: заполнение</span><span class="sxs-lookup"><span data-stu-id="5fce6-289">/app1/ifd/exif/PaddingSchema:Padding</span></span> | <span data-ttu-id="5fce6-290">/ИФД/ексиф/паддингсчема: заполнение</span><span class="sxs-lookup"><span data-stu-id="5fce6-290">/ifd/exif/PaddingSchema:Padding</span></span> |
| <span data-ttu-id="5fce6-291">ПОДДЕРЖИВАЮЩ</span><span class="sxs-lookup"><span data-stu-id="5fce6-291">XMP</span></span>             | <span data-ttu-id="5fce6-292">/КСМП/паддингсчема: заполнение</span><span class="sxs-lookup"><span data-stu-id="5fce6-292">/xmp/PaddingSchema:Padding</span></span>           | <span data-ttu-id="5fce6-293">/ИФД/КСМП/паддингсчема: заполнение</span><span class="sxs-lookup"><span data-stu-id="5fce6-293">/ifd/xmp/PaddingSchema:Padding</span></span>  |
| <span data-ttu-id="5fce6-294">GPS</span><span class="sxs-lookup"><span data-stu-id="5fce6-294">GPS</span></span>             | <span data-ttu-id="5fce6-295">/app1/ifd/gps/PaddingSchema: заполнение</span><span class="sxs-lookup"><span data-stu-id="5fce6-295">/app1/ifd/gps/PaddingSchema:Padding</span></span>  | <span data-ttu-id="5fce6-296">/ИФД/ГПС/паддингсчема: заполнение</span><span class="sxs-lookup"><span data-stu-id="5fce6-296">/ifd/gps/PaddingSchema:Padding</span></span>  |



 

### <a name="obtaining-a-fast-metadata-encoder"></a><span data-ttu-id="5fce6-297">Получение высокоскоростного кодировщика метаданных</span><span class="sxs-lookup"><span data-stu-id="5fce6-297">Obtaining a Fast Metadata Encoder</span></span>

<span data-ttu-id="5fce6-298">При наличии изображения с заполнением метаданных можно получить быстрый кодировщик метаданных, используя методы фабрики изображений **креатефастметадатаенкодерфромдекодер** и **креатефастметадатаенкодерфромфрамедекоде**.</span><span class="sxs-lookup"><span data-stu-id="5fce6-298">When you have an image with metadata padding, a fast metadata encoder can be obtained by using the imaging factory methods **CreateFastMetadataEncoderFromDecoder** and **CreateFastMetadataEncoderFromFrameDecode**.</span></span>

<span data-ttu-id="5fce6-299">Как следует из названия, **креатефастметадатаенкодерфромдекодер** создает быстрый кодировщик метаданных для метаданных на уровне декодера.</span><span class="sxs-lookup"><span data-stu-id="5fce6-299">As the name implies, **CreateFastMetadataEncoderFromDecoder** creates a fast metadata encoder for decoder-level metadata.</span></span> <span data-ttu-id="5fce6-300">Форматы образов в машинном код, предоставляемые компонентом WIC, не поддерживают метаданные уровня декодера, но этот метод предоставляется в случае, когда формат изображения разрабатывается в будущем.</span><span class="sxs-lookup"><span data-stu-id="5fce6-300">The native image formats provided by WIC do not support decoder-level metadata but this method is provided in case such an image format is developed in the future.</span></span>

<span data-ttu-id="5fce6-301">Наиболее распространенным сценарием является получение кодировщика метаданных из кадра изображения с помощью **креатефастметадатаенкодерфромфрамедекоде**.</span><span class="sxs-lookup"><span data-stu-id="5fce6-301">The more common scenario is to obtain a fast metadata encoder from an image frame by using **CreateFastMetadataEncoderFromFrameDecode**.</span></span> <span data-ttu-id="5fce6-302">Следующий код получает кодировщик быстрых метаданных для декодированного кадра и изменяет значение рейтинга в блоке App1.</span><span class="sxs-lookup"><span data-stu-id="5fce6-302">The following code obtains a decoded frame's fast metadata encoder and changes the rating value in the App1 block.</span></span>


```
if (SUCCEEDED(hr))
{
    IWICFastMetadataEncoder *pFME = NULL;
    IWICMetadataQueryWriter *pFMEQW = NULL;

    hr = pFactory->CreateFastMetadataEncoderFromFrameDecode(
        pFrameDecode, 
        &pFME);
}
```



### <a name="using-the-fast-metadata-encoder"></a><span data-ttu-id="5fce6-303">Использование кодировщика быстрых метаданных</span><span class="sxs-lookup"><span data-stu-id="5fce6-303">Using the Fast Metadata Encoder</span></span>

<span data-ttu-id="5fce6-304">С помощью быстрого кодировщика метаданных можно получить модуль записи запроса.</span><span class="sxs-lookup"><span data-stu-id="5fce6-304">From the fast metadata encoder, you can obtain a query writer.</span></span> <span data-ttu-id="5fce6-305">Это позволяет создавать метаданные с помощью выражения запроса, как показано выше.</span><span class="sxs-lookup"><span data-stu-id="5fce6-305">This enables you to write metadata by using a query expression as previously demonstrated.</span></span> <span data-ttu-id="5fce6-306">После задания метаданных в модуле записи запроса зафиксируйте быстрый кодировщик метаданных, чтобы завершить обновление метаданных.</span><span class="sxs-lookup"><span data-stu-id="5fce6-306">After metadata has been set in the query writer, commit the fast metadata encoder to finalize the metadata update.</span></span> <span data-ttu-id="5fce6-307">В следующем примере кода показано задание и фиксация изменений метаданных</span><span class="sxs-lookup"><span data-stu-id="5fce6-307">The following code demonstrates setting and committing the metadata changes</span></span>


```
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



<span data-ttu-id="5fce6-308">Если **фиксация** завершается неудачей по какой-либо причине, необходимо повторно закодировать образ, чтобы новые метаданные добавлялись в образ.</span><span class="sxs-lookup"><span data-stu-id="5fce6-308">If **Commit** fails for any reason, you will need to re-encode the image to ensure the new metadata is added to the image.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5fce6-309">См. также</span><span class="sxs-lookup"><span data-stu-id="5fce6-309">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="5fce6-310">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="5fce6-310">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5fce6-311">Общие сведения о компоненте создания образов Windows</span><span class="sxs-lookup"><span data-stu-id="5fce6-311">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="5fce6-312">Общие сведения о метаданных компонента WIC</span><span class="sxs-lookup"><span data-stu-id="5fce6-312">WIC Metadata Overview</span></span>](-wic-about-metadata.md)
</dt> <dt>

[<span data-ttu-id="5fce6-313">Общие сведения о языке запросов метаданных</span><span class="sxs-lookup"><span data-stu-id="5fce6-313">Metadata Query Language Overview</span></span>](-wic-codec-metadataquerylanguage.md)
</dt> <dt>

[<span data-ttu-id="5fce6-314">Общие сведения о расширяемости метаданных</span><span class="sxs-lookup"><span data-stu-id="5fce6-314">Metadata Extensibility Overview</span></span>](-wic-codec-metadatahandlers.md)
</dt> <dt>

[<span data-ttu-id="5fce6-315">Пошаговое руководство. повторное кодирование изображения JPEG с помощью метаданных</span><span class="sxs-lookup"><span data-stu-id="5fce6-315">How-to: Re-encode a JPEG Image with Metadata</span></span>](-wic-codec-jpegmetadataencoding.md)
</dt> </dl>

 

 
