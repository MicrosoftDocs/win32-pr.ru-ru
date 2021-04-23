---
description: В этом разделе описываются требования к созданию пользовательских обработчиков метаданных для компонента Windows Imaging Component (WIC), включая средства чтения и записи метаданных.
ms.assetid: 08f1872b-6e4d-44ee-abc7-48685e435acc
title: Общие сведения о расширяемости метаданных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6576585f7f35628432504086695dd6c64091d3b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265298"
---
# <a name="metadata-extensibility-overview"></a><span data-ttu-id="b739a-103">Общие сведения о расширяемости метаданных</span><span class="sxs-lookup"><span data-stu-id="b739a-103">Metadata Extensibility Overview</span></span>

<span data-ttu-id="b739a-104">В этом разделе описываются требования к созданию пользовательских обработчиков метаданных для компонента Windows Imaging Component (WIC), включая средства чтения и записи метаданных.</span><span class="sxs-lookup"><span data-stu-id="b739a-104">This topic introduces the requirements for creating custom metadata handlers for the Windows Imaging Component (WIC), including both metadata readers and writers.</span></span> <span data-ttu-id="b739a-105">Также обсуждаются требования к расширению обнаружения компонентов во время выполнения компонента WIC для включения пользовательских обработчиков метаданных.</span><span class="sxs-lookup"><span data-stu-id="b739a-105">It also discusses the requirements for extending WIC run-time component discovery to include your custom metadata handlers.</span></span>

<span data-ttu-id="b739a-106">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="b739a-106">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="b739a-107">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="b739a-107">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="b739a-108">Введение</span><span class="sxs-lookup"><span data-stu-id="b739a-108">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="b739a-109">Создание средства чтения метаданных</span><span class="sxs-lookup"><span data-stu-id="b739a-109">Creating a Metadata Reader</span></span>](#creating-a-metadata-reader)
    -   [<span data-ttu-id="b739a-110">Интерфейс Ивикметадатареадер</span><span class="sxs-lookup"><span data-stu-id="b739a-110">IWICMetadataReader Interface</span></span>](#iwicmetadatareader-interface)
    -   [<span data-ttu-id="b739a-111">Интерфейс Ивикперсистстреам</span><span class="sxs-lookup"><span data-stu-id="b739a-111">IWICPersistStream Interface</span></span>](#iwicpersiststream-interface)
    -   [<span data-ttu-id="b739a-112">Интерфейс Ивикстреампровидер</span><span class="sxs-lookup"><span data-stu-id="b739a-112">IWICStreamProvider Interface</span></span>](#iwicstreamprovider-interface)
-   [<span data-ttu-id="b739a-113">Создание модуля записи метаданных</span><span class="sxs-lookup"><span data-stu-id="b739a-113">Creating a Metadata Writer</span></span>](#creating-a-metadata-writer)
    -   [<span data-ttu-id="b739a-114">Интерфейс Ивикметадатавритер</span><span class="sxs-lookup"><span data-stu-id="b739a-114">IWICMetadataWriter Interface</span></span>](#iwicmetadatawriter-interface)
    -   [<span data-ttu-id="b739a-115">Интерфейс Ивикперсистстреам</span><span class="sxs-lookup"><span data-stu-id="b739a-115">IWICPersistStream Interface</span></span>](#iwicpersiststream-interface)
    -   [<span data-ttu-id="b739a-116">Интерфейс Ивикстреампровидер</span><span class="sxs-lookup"><span data-stu-id="b739a-116">IWICStreamProvider Interface</span></span>](#iwicstreamprovider-interface)
-   [<span data-ttu-id="b739a-117">Установка и регистрация обработчика метаданных</span><span class="sxs-lookup"><span data-stu-id="b739a-117">Installing and Registering a Metadata Handler</span></span>](#installing-and-registering-a-metadata-handler)
    -   [<span data-ttu-id="b739a-118">Разделы реестра обработчика метаданных</span><span class="sxs-lookup"><span data-stu-id="b739a-118">Metadata Handler Registry Keys</span></span>](#metadata-handler-registry-keys)
    -   [<span data-ttu-id="b739a-119">Читатели метаданных</span><span class="sxs-lookup"><span data-stu-id="b739a-119">Metadata Readers</span></span>](#metadata-readers)
    -   [<span data-ttu-id="b739a-120">Записи метаданных</span><span class="sxs-lookup"><span data-stu-id="b739a-120">Metadata Writers</span></span>](#metadata-writers)
    -   [<span data-ttu-id="b739a-121">Подписывание обработчика метаданных</span><span class="sxs-lookup"><span data-stu-id="b739a-121">Signing a Metadata Handler</span></span>](#signing-a-metadata-handler)
-   [<span data-ttu-id="b739a-122">Особые рекомендации</span><span class="sxs-lookup"><span data-stu-id="b739a-122">Special Considerations</span></span>](#special-considerations)
    -   [<span data-ttu-id="b739a-123">пропвариантс</span><span class="sxs-lookup"><span data-stu-id="b739a-123">PROPVARIANTS</span></span>](#propvariants)
    -   [<span data-ttu-id="b739a-124">Обработчики 8BIM</span><span class="sxs-lookup"><span data-stu-id="b739a-124">8BIM Handlers</span></span>](#8bim-handlers)
-   [<span data-ttu-id="b739a-125">См. также</span><span class="sxs-lookup"><span data-stu-id="b739a-125">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="b739a-126">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="b739a-126">Prerequisites</span></span>

<span data-ttu-id="b739a-127">Чтобы разобраться в этом разделе, необходимо иметь глубокое представление о компонентах WIC, его компонентах и метаданных для изображений.</span><span class="sxs-lookup"><span data-stu-id="b739a-127">To understand this topic you should have an in-depth understanding of WIC, its components, and metadata for images.</span></span> <span data-ttu-id="b739a-128">Дополнительные сведения о метаданных WIC см. в статье [Общие сведения о метаданных WIC](-wic-about-metadata.md).</span><span class="sxs-lookup"><span data-stu-id="b739a-128">For more information on WIC metadata, see the [WIC Metadata Overview](-wic-about-metadata.md).</span></span> <span data-ttu-id="b739a-129">Дополнительные сведения о компонентах WIC см. в статье [Обзор компонента создания образов Windows](-wic-about-windows-imaging-codec.md).</span><span class="sxs-lookup"><span data-stu-id="b739a-129">For more information on WIC components, see the [Windows Imaging Component Overview](-wic-about-windows-imaging-codec.md).</span></span>

## <a name="introduction"></a><span data-ttu-id="b739a-130">Введение</span><span class="sxs-lookup"><span data-stu-id="b739a-130">Introduction</span></span>

<span data-ttu-id="b739a-131">Как обсуждалось в [обзоре метаданных WIC](-wic-about-metadata.md), часто встречается несколько блоков метаданных в изображении, каждый из которых предоставляет различные типы данных в различных форматах метаданных.</span><span class="sxs-lookup"><span data-stu-id="b739a-131">As discussed in the [WIC Metadata Overview](-wic-about-metadata.md), there are often multiple blocks of metadata within an image, each exposing different types of information in different metadata formats.</span></span> <span data-ttu-id="b739a-132">Для взаимодействия с форматом метаданных, внедренным в образ, приложение должно использовать соответствующий обработчик метаданных.</span><span class="sxs-lookup"><span data-stu-id="b739a-132">To interact with a metadata format embedded within an image, an application must use an appropriate metadata handler.</span></span> <span data-ttu-id="b739a-133">Компонент WIC предоставляет несколько обработчиков метаданных (средств чтения и записи метаданных), которые позволяют считывать и записывать определенные типы метаданных, например EXIF или XMP.</span><span class="sxs-lookup"><span data-stu-id="b739a-133">WIC provides several metadata handlers (both metadata readers and writers) that enable you to read and write specific types of metadata such as Exif or XMP.</span></span>

<span data-ttu-id="b739a-134">Помимо предоставленных собственных обработчиков, компонент WIC предоставляет интерфейсы API, позволяющие создавать новые обработчики метаданных, участвующие в обнаружении компонентов компонента WIC во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="b739a-134">In addition to the native handlers provided, WIC provides APIs that enable you to create new metadata handlers that participate in WIC's run-time component discovery.</span></span> <span data-ttu-id="b739a-135">Это позволяет приложениям, использующим WIC, считывать и записывать пользовательские форматы метаданных.</span><span class="sxs-lookup"><span data-stu-id="b739a-135">This enables applications that use WIC to read and write your custom metadata formats.</span></span>

<span data-ttu-id="b739a-136">Следующие шаги позволяют обработчикам метаданных участвовать в обнаружении метаданных во время выполнения компонента WIC.</span><span class="sxs-lookup"><span data-stu-id="b739a-136">The following steps enable your metadata handlers to participate in WIC's run-time metadata discovery.</span></span>

-   <span data-ttu-id="b739a-137">Реализуйте класс обработчика метаданных ([**ивикметадатареадер**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)), который предоставляет необходимые интерфейсы WIC для чтения пользовательского формата метаданных.</span><span class="sxs-lookup"><span data-stu-id="b739a-137">Implement a metadata-reader handler class ([**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)) that exposes the required WIC interfaces for reading your custom metadata format.</span></span> <span data-ttu-id="b739a-138">Это позволяет приложениям на основе WIC считывать формат метаданных так же, как они считывают собственные форматы метаданных.</span><span class="sxs-lookup"><span data-stu-id="b739a-138">This enables WIC-based applications to read your metadata format the same way they read native metadata formats.</span></span>
-   <span data-ttu-id="b739a-139">Реализуйте класс обработчика записи метаданных ([**ивикметадатавритер**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)), который предоставляет необходимые интерфейсы WIC для кодирования пользовательского формата метаданных.</span><span class="sxs-lookup"><span data-stu-id="b739a-139">Implement a metadata-writer handler class ([**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)) that exposes the required WIC interfaces for encoding your custom metadata format.</span></span> <span data-ttu-id="b739a-140">Это позволяет приложениям на основе WIC сериализовать формат метаданных в Поддерживаемые форматы изображений.</span><span class="sxs-lookup"><span data-stu-id="b739a-140">This enables WIC-based applications to serialize your metadata format into supported image formats.</span></span>
-   <span data-ttu-id="b739a-141">Цифровая подпись и регистрация обработчиков метаданных.</span><span class="sxs-lookup"><span data-stu-id="b739a-141">Digitally sign and register your metadata handlers.</span></span> <span data-ttu-id="b739a-142">Это позволяет обнаруживать обработчики метаданных во время выполнения путем сопоставления идентифицирующего шаблона в реестре с шаблоном, внедренным в файл изображения.</span><span class="sxs-lookup"><span data-stu-id="b739a-142">This enables your metadata handlers to be discovered at run time by matching the identifying pattern in the registry with the pattern embedded in the image file.</span></span>

## <a name="creating-a-metadata-reader"></a><span data-ttu-id="b739a-143">Создание средства чтения метаданных</span><span class="sxs-lookup"><span data-stu-id="b739a-143">Creating a Metadata Reader</span></span>

<span data-ttu-id="b739a-144">Основным доступом к блокам метаданных внутри кодека является интерфейс [**ивикметадатаблоккреадер**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) , реализуемый каждым кодеком WIC.</span><span class="sxs-lookup"><span data-stu-id="b739a-144">The main access to metadata blocks within a codec is through the [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) interface that each WIC codec implements.</span></span> <span data-ttu-id="b739a-145">Этот интерфейс перечисляет все блоки метаданных, внедренные в формат изображения, чтобы можно было обнаружить и создать экземпляры соответствующего обработчика метаданных для каждого блока.</span><span class="sxs-lookup"><span data-stu-id="b739a-145">This interface enumerates each of the metadata blocks embedded in an image format so that the appropriate metadata handler can be discovered and instantiated for each block.</span></span> <span data-ttu-id="b739a-146">Блоки метаданных, не распознаваемые WIC, считаются неизвестными и определяются как GUID CLSID \_ викункновнметадатареадер.</span><span class="sxs-lookup"><span data-stu-id="b739a-146">The metadata blocks that are not recognized by WIC are considered unknown and are defined as the GUID CLSID\_WICUnknownMetadataReader.</span></span> <span data-ttu-id="b739a-147">Чтобы формат метаданных был распознан компонентом WIC, необходимо создать класс, реализующий три интерфейса: [**ивикметадатареадер**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader), [**ивикперсистстреам**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream)и [**ивикстреампровидер**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider).</span><span class="sxs-lookup"><span data-stu-id="b739a-147">To have your metadata format recognized by WIC, you must create a class that implements three interfaces: [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader), [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream), and [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider).</span></span>

> [!Note]  
> <span data-ttu-id="b739a-148">Если формат метаданных имеет ограничения, которые отображают некоторые методы требуемых интерфейсов, такие методы должны возвращать ВИНКОДЕК \_ Err \_ унсуппортедоператион.</span><span class="sxs-lookup"><span data-stu-id="b739a-148">If your metadata format has restrictions that render some methods of the required interfaces inappropriate, such methods should return WINCODEC\_ERR\_UNSUPPORTEDOPERATION.</span></span>

 

### <a name="iwicmetadatareader-interface"></a><span data-ttu-id="b739a-149">Интерфейс Ивикметадатареадер</span><span class="sxs-lookup"><span data-stu-id="b739a-149">IWICMetadataReader Interface</span></span>

<span data-ttu-id="b739a-150">При создании средства чтения метаданных должен быть реализован интерфейс [**ивикметадатареадер**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader) .</span><span class="sxs-lookup"><span data-stu-id="b739a-150">The [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader) interface must be implemented when creating a metadata reader.</span></span> <span data-ttu-id="b739a-151">Этот интерфейс предоставляет доступ к элементам метаданных ундерлинг в потоке данных в формате метаданных.</span><span class="sxs-lookup"><span data-stu-id="b739a-151">This interface provides access to the underling metadata items within the data stream of a metadata format.</span></span>

<span data-ttu-id="b739a-152">В следующем коде показано определение интерфейса средства чтения метаданных, как определено в файле винкодексдк. idl.</span><span class="sxs-lookup"><span data-stu-id="b739a-152">The following code shows the definition of the metadata reader interface as defined in the wincodecsdk.idl file.</span></span>

``` syntax
interface IWICMetadataReader : IUnknown
{
    HRESULT GetMetadataFormat(
        [out] GUID *pguidMetadataFormat
        );

    HRESULT GetMetadataHandlerInfo(
        [out] IWICMetadataHandlerInfo **ppIHandler
        );

    HRESULT GetCount(
        [out] UINT *pcCount
        );

    HRESULT GetValueByIndex(
        [in] UINT nIndex,
        [in, out, unique] PROPVARIANT *pvarSchema,
        [in, out, unique] PROPVARIANT *pvarId,
        [in, out, unique] PROPVARIANT *pvarValue
        );

    HRESULT GetValue(
        [in, unique] const PROPVARIANT *pvarSchema,
        [in] const PROPVARIANT *pvarId,
        [in, out, unique] PROPVARIANT *pvarValue
        );

    HRESULT GetEnumerator(
        [out] IWICEnumMetadataItem **ppIEnumMetadata
        );
};
```

<span data-ttu-id="b739a-153">Метод **жетметадатаформат** возвращает идентификатор GUID вашего формата метаданных.</span><span class="sxs-lookup"><span data-stu-id="b739a-153">The **GetMetadataFormat** method returns the GUID of your metadata format.</span></span>

<span data-ttu-id="b739a-154">Метод **жетметадатахандлеринфо** возвращает интерфейс [**ивикметадатахандлеринфо**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatahandlerinfo) , предоставляющий сведения о обработчике метаданных.</span><span class="sxs-lookup"><span data-stu-id="b739a-154">The **GetMetadataHandlerInfo** method returns an [**IWICMetadataHandlerInfo**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatahandlerinfo) interface that provides information about your metadata handler.</span></span> <span data-ttu-id="b739a-155">Сюда входят такие сведения, как форматы изображений, поддерживающие формат метаданных, и требуется ли для читателя метаданных доступ к полному потоку метаданных.</span><span class="sxs-lookup"><span data-stu-id="b739a-155">This includes information such as what image formats support the metadata format and whether your metadata reader requires access to the full metadata stream.</span></span>

<span data-ttu-id="b739a-156">Метод **NOCOUNT** возвращает количество отдельных элементов метаданных (включая внедренные блоки метаданных), найденных в потоке метаданных.</span><span class="sxs-lookup"><span data-stu-id="b739a-156">The **GetCount** method returns the number of individual metadata items (including embedded metadata blocks) found within the metadata stream.</span></span>

<span data-ttu-id="b739a-157">Метод **жетвалуебиндекс** Возвращает элемент метаданных по значению индекса.</span><span class="sxs-lookup"><span data-stu-id="b739a-157">The **GetValueByIndex** method returns a metadata item by an index value.</span></span> <span data-ttu-id="b739a-158">Этот метод позволяет приложениям циклически проходить по каждому элементу метаданных в блоке метаданных.</span><span class="sxs-lookup"><span data-stu-id="b739a-158">This method enables applications to loop through each metadata item in a metadata block.</span></span> <span data-ttu-id="b739a-159">В следующем коде показано, как приложение может использовать этот метод для извлечения каждого элемента метаданных в блоке метаданных.</span><span class="sxs-lookup"><span data-stu-id="b739a-159">The following code demonstrates how an application can use this method to retrieve each metadata item in a metadata block.</span></span>


```C++
PROPVARIANT readerValue;
IWICMetadataBlockReader *blockReader = NULL;
IWICMetadataReader *reader = NULL;

PropVariantInit(&readerValue);

hr = pFrameDecode->QueryInterface(IID_IWICMetadataBlockReader, (void**)&blockReader);

if (SUCCEEDED(hr))
{
    // Retrieve the third block in the image. This is image specific and
    // ideally you should call this by retrieving the reader count
    // first.
    hr = blockReader->GetReaderByIndex(2, &reader);
}

if (SUCCEEDED(hr))
{
    UINT numValues = 0;

    hr = reader->GetCount(&numValues);

    // Loop through each item and retrieve by index
    for (UINT i = 0; SUCCEEDED(hr) && i < numValues; i++)
    {
        PROPVARIANT id, value;

        PropVariantInit(&id);
        PropVariantInit(&value);

        hr = reader->GetValueByIndex(i, NULL, &id, &value);

        if (SUCCEEDED(hr))
        {
            // Do something with the metadata item.
            //...
        }
        PropVariantClear(&id);
        PropVariantClear(&value);
    }               
}
```



<span data-ttu-id="b739a-160">Метод **GetValue** извлекает конкретный элемент метаданных по схеме и (или) идентификатору.</span><span class="sxs-lookup"><span data-stu-id="b739a-160">The **GetValue** method retrieves a specific metadata item by schema and/or ID.</span></span> <span data-ttu-id="b739a-161">Этот метод аналогичен методу **жетвалуебиндекс** , за исключением того, что он извлекает элемент метаданных с определенной схемой или идентификатором.</span><span class="sxs-lookup"><span data-stu-id="b739a-161">This method is similar to the **GetValueByIndex** method except that it retrieves a metadata item that has a specific schema or ID.</span></span>

<span data-ttu-id="b739a-162">Метод **GetEnumerator** Возвращает перечислитель каждого элемента метаданных в блоке метаданных.</span><span class="sxs-lookup"><span data-stu-id="b739a-162">The **GetEnumerator** method returns an enumerator of each metadata item in the metadata block.</span></span> <span data-ttu-id="b739a-163">Это позволяет приложениям использовать перечислитель для навигации по формату метаданных.</span><span class="sxs-lookup"><span data-stu-id="b739a-163">This enables applications to use an enumerator to navigate your metadata format.</span></span>

<span data-ttu-id="b739a-164">Если формат метаданных не имеет представления о схемах для элементов метаданных, то параметр GetValue... методы должны игнорировать это свойство.</span><span class="sxs-lookup"><span data-stu-id="b739a-164">If your metadata format does not have a notion of schemas for metadata items, the GetValue... methods should ignore this property.</span></span> <span data-ttu-id="b739a-165">Однако если ваш формат поддерживает именование схемы, необходимо предусмотреть значение **null** .</span><span class="sxs-lookup"><span data-stu-id="b739a-165">If, however, your format supports schema naming, you should anticipate a **NULL** value.</span></span>

<span data-ttu-id="b739a-166">Если элемент метаданных является внедренным блоком метаданных, создайте обработчик метаданных из подпотока внедренного содержимого и возвратите новый обработчик метаданных.</span><span class="sxs-lookup"><span data-stu-id="b739a-166">If a metadata item is an embedded metadata block, create a metadata handler from the substream of the embedded content and return the new metadata handler.</span></span> <span data-ttu-id="b739a-167">Если для вложенного блока нет доступного модуля чтения метаданных, создайте экземпляр и возвратите неизвестный модуль чтения метаданных.</span><span class="sxs-lookup"><span data-stu-id="b739a-167">If there is no metadata reader available for the nested block, instantiate and return an unknown metadata reader.</span></span> <span data-ttu-id="b739a-168">Чтобы создать новый модуль чтения метаданных для внедренного блока, вызовите методы **креатеметадатареадерфромконтаинер** или **креатеметадатареадер** фабрики компонентов или вызовите функцию [**викматчметадатаконтент**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicmatchmetadatacontent) .</span><span class="sxs-lookup"><span data-stu-id="b739a-168">To create a new metadata reader for the embedded block, call the component factory's **CreateMetadataReaderFromContainer** or **CreateMetadataReader** methods, or call the [**WICMatchMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicmatchmetadatacontent) function.</span></span>

<span data-ttu-id="b739a-169">Если поток метаданных содержит содержимое с обратным порядком байтов, модуль чтения метаданных отвечает за обмен всеми обрабатываемыми им значениями данных.</span><span class="sxs-lookup"><span data-stu-id="b739a-169">If the metadata stream contains big-endian content, the metadata reader is responsible for swapping any data values it processes.</span></span> <span data-ttu-id="b739a-170">Он также отвечает за уведомление всех вложенных модулей чтения метаданных о том, что они работают с потоком данных с обратным порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="b739a-170">It is also responsible for informing any nested metadata readers that they are working with big-endian data stream.</span></span> <span data-ttu-id="b739a-171">Однако все значения должны возвращаться в формате с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="b739a-171">However, all values should be returned in little-endian format.</span></span>

<span data-ttu-id="b739a-172">Реализация поддержки для навигации по пространству имен путем поддержки запросов, где идентификатор элемента метаданных — это `VT_CLSID` (GUID), соответствующий формату метаданных.</span><span class="sxs-lookup"><span data-stu-id="b739a-172">Implement support for namespace navigation by supporting queries where the metadata item ID is a `VT_CLSID` (a GUID) corresponding to a metadata format.</span></span> <span data-ttu-id="b739a-173">Если во время синтаксического анализа определяется вложенный модуль чтения метаданных для этого формата, он должен быть возвращен.</span><span class="sxs-lookup"><span data-stu-id="b739a-173">If a nested metadata reader for that format is identified during parsing, it must be returned.</span></span> <span data-ttu-id="b739a-174">Это позволяет приложениям использовать средство чтения запросов метаданных для поиска в формате метаданных.</span><span class="sxs-lookup"><span data-stu-id="b739a-174">This enables applications to use a metadata query reader to search your metadata format.</span></span>

<span data-ttu-id="b739a-175">При получении элемента метаданных по ИДЕНТИФИКАТОРу следует использовать [функцию пропвариантчанжетипе](/windows/win32/api/propvarutil/nf-propvarutil-propvariantchangetype) для ПРИВЕДЕНия идентификатора к ожидаемому типу.</span><span class="sxs-lookup"><span data-stu-id="b739a-175">When getting a metadata item by ID, you should use [PropVariantChangeType Function](/windows/win32/api/propvarutil/nf-propvarutil-propvariantchangetype) to coerce the ID into the expected type.</span></span> <span data-ttu-id="b739a-176">Например, средство чтения IFD приводит идентификатор к типу `VT_UI2` , совпадающему с типом данных ТЕГА IFD с идентификатором ushort.</span><span class="sxs-lookup"><span data-stu-id="b739a-176">For example, the IFD reader will coerce an ID to type `VT_UI2` to coincide with the data type of an IFD tag ID USHORT.</span></span> <span data-ttu-id="b739a-177">Для этого тип входных данных и ожидаемый тип должны быть [пропвариант](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .</span><span class="sxs-lookup"><span data-stu-id="b739a-177">The input type and expected type must both be [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) to do this.</span></span> <span data-ttu-id="b739a-178">Это не является обязательным, но выполнение этого приведения упрощает код, который вызывает модуль чтения для запроса элементов метаданных.</span><span class="sxs-lookup"><span data-stu-id="b739a-178">This is not required, but doing this coercion simplifies code that calls the reader to query for metadata items.</span></span>

### <a name="iwicpersiststream-interface"></a><span data-ttu-id="b739a-179">Интерфейс Ивикперсистстреам</span><span class="sxs-lookup"><span data-stu-id="b739a-179">IWICPersistStream Interface</span></span>

<span data-ttu-id="b739a-180">Интерфейс [**ивикперсистстреам**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) наследует от класса **IPersistStream** и предоставляет дополнительные методы для сохранения и загрузки объектов с помощью перечисления [**викперсистоптионс**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) .</span><span class="sxs-lookup"><span data-stu-id="b739a-180">The [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) interface inherits from **IPersistStream** and provides additional methods for saving and loading objects by using the [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) enumeration.</span></span>

<span data-ttu-id="b739a-181">В следующем коде показано определение интерфейса [**ивикперсистстреам**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) , как определено в файле винкодексдк. idl.</span><span class="sxs-lookup"><span data-stu-id="b739a-181">The following code shows the definition of the [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) interface as defined in the wincodecsdk.idl file.</span></span>

``` syntax
interface IWICPersistStream : IPersistStream
{
    HRESULT LoadEx(
        [in, unique] IStream *pIStream,
        [in, unique] const GUID *pguidPreferredVendor,
        [in] DWORD dwPersistOptions
        );

    HRESULT SaveEx(
        [in] IStream *pIStream,
        [in] DWORD dwPersistOptions,
        [in] BOOL fClearDirty
        );
};
```

<span data-ttu-id="b739a-182">Метод **лоадекс** предоставляет модулю чтения метаданных поток данных, содержащий блок метаданных.</span><span class="sxs-lookup"><span data-stu-id="b739a-182">The **LoadEx** method provides your metadata reader with a data stream containing your metadata block.</span></span> <span data-ttu-id="b739a-183">Модуль чтения анализирует этот поток для доступа к базовым элементам метаданных.</span><span class="sxs-lookup"><span data-stu-id="b739a-183">Your reader parses this stream to access the underlying metadata items.</span></span> <span data-ttu-id="b739a-184">Модуль чтения метаданных инициализируется с помощью подпотока, расположенного в начале необработанного содержимого метаданных.</span><span class="sxs-lookup"><span data-stu-id="b739a-184">Your metadata reader is initialized with a substream that is positioned at the beginning of the raw metadata content.</span></span> <span data-ttu-id="b739a-185">Если модулю чтения не требуется полный поток, подпоток ограничен в пределах диапазона только содержимым блока метаданных. в противном случае полный поток метаданных предоставляется вместе с положением, заданным в начале блока метаданных.</span><span class="sxs-lookup"><span data-stu-id="b739a-185">If your reader does not require the full stream, the substream is limited in range to only the content of the metadata block; otherwise, the full metadata stream is provided with the position set at the beginning of your metadata block.</span></span>

<span data-ttu-id="b739a-186">Метод **Савикс** используется модулями записи метаданных для сериализации блока метаданных.</span><span class="sxs-lookup"><span data-stu-id="b739a-186">The **SaveEx** method is used by metadata writers to serialize your metadata block.</span></span> <span data-ttu-id="b739a-187">Если **Савикс** используется в модуле чтения метаданных, он должен возвращать винкодек \_ Err \_ унсуппортедоператион.</span><span class="sxs-lookup"><span data-stu-id="b739a-187">When **SaveEx** is used in a metadata reader, it should return WINCODEC\_ERR\_UNSUPPORTEDOPERATION.</span></span>

### <a name="iwicstreamprovider-interface"></a><span data-ttu-id="b739a-188">Интерфейс Ивикстреампровидер</span><span class="sxs-lookup"><span data-stu-id="b739a-188">IWICStreamProvider Interface</span></span>

<span data-ttu-id="b739a-189">Интерфейс [**ивикстреампровидер**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider) позволяет модулю чтения метаданных предоставлять ссылки на его поток содержимого, предоставлять сведения о потоке и обновлять кэшированные версии потока.</span><span class="sxs-lookup"><span data-stu-id="b739a-189">The [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider) interface enables your metadata reader to provide references to its content stream, provide information about the stream, and refresh cached versions of the stream.</span></span>

<span data-ttu-id="b739a-190">В следующем коде показано определение интерфейса [**ивикстреампровидер**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider) , как определено в файле винкодексдк. idl.</span><span class="sxs-lookup"><span data-stu-id="b739a-190">The following code shows the definition of the [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider) interface as defined in the wincodecsdk.idl file.</span></span>

``` syntax
interface IWICStreamProvider : IUnknown
{
    HRESULT GetStream(
        [out] IStream **ppIStream
        );

    HRESULT GetPersistOptions(
        [out] DWORD *pdwPersistOptions
        );

    HRESULT GetPreferredVendorGUID(
        [out] GUID *pguidPreferredVendor
        );

    HRESULT RefreshStream(
        );
};
```

<span data-ttu-id="b739a-191">Метод **WebMethod извлекает** ссылку на поток метаданных.</span><span class="sxs-lookup"><span data-stu-id="b739a-191">The **GetStream** method retrieves a reference to your metadata stream.</span></span> <span data-ttu-id="b739a-192">Возвращаемый поток должен вернуть указатель потока к начальной позиции.</span><span class="sxs-lookup"><span data-stu-id="b739a-192">The stream you return should have the stream pointer reset to the start position.</span></span> <span data-ttu-id="b739a-193">Если формат метаданных требует полного доступа к потоку, начальное расположение должно быть началом блока метаданных.</span><span class="sxs-lookup"><span data-stu-id="b739a-193">If your metadata format requires full stream access, the start position should be the start of your metadata block.</span></span>

<span data-ttu-id="b739a-194">Метод **жетперсистоптионс** возвращает текущие параметры потока из перечисления [**викперсистоптионс**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) .</span><span class="sxs-lookup"><span data-stu-id="b739a-194">The **GetPersistOptions** method returns the stream's current options from the [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) enumeration.</span></span>

<span data-ttu-id="b739a-195">Метод **жетпреферредвендоргуид** возвращает идентификатор GUID поставщика средства чтения метаданных.</span><span class="sxs-lookup"><span data-stu-id="b739a-195">The **GetPreferredVendorGUID** method returns the GUID of the vendor of the metadata reader.</span></span>

<span data-ttu-id="b739a-196">Метод **рефрешстреам** обновляет поток метаданных.</span><span class="sxs-lookup"><span data-stu-id="b739a-196">The **RefreshStream** method refreshes the metadata stream.</span></span> <span data-ttu-id="b739a-197">Этот метод должен вызывать **лоадекс** с **нулевым** потоком для любых вложенных блоков метаданных.</span><span class="sxs-lookup"><span data-stu-id="b739a-197">This method must call **LoadEx** with a **NULL** stream for any nested metadata blocks.</span></span> <span data-ttu-id="b739a-198">Это необходимо потому, что вложенные блоки метаданных и их элементы могут больше не существовать из-за редактирования на месте.</span><span class="sxs-lookup"><span data-stu-id="b739a-198">This is necessary because nested metadata blocks and their items may no longer exist, due to in-place editing.</span></span>

## <a name="creating-a-metadata-writer"></a><span data-ttu-id="b739a-199">Создание модуля записи метаданных</span><span class="sxs-lookup"><span data-stu-id="b739a-199">Creating a Metadata Writer</span></span>

<span data-ttu-id="b739a-200">Модуль записи метаданных — это тип обработчика метаданных, который предоставляет способ сериализации блока метаданных в кадр изображения или за пределы отдельного кадра, если формат изображения поддерживает его.</span><span class="sxs-lookup"><span data-stu-id="b739a-200">A metadata writer is a type of metadata handler that provides a way to serialize a metadata block to an image frame, or outside an individual frame if the image format supports it.</span></span> <span data-ttu-id="b739a-201">Основным доступом к модулям записи метаданных внутри кодека является интерфейс [**ивикметадатаблокквритер**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) , реализуемый каждым кодировщиком WIC.</span><span class="sxs-lookup"><span data-stu-id="b739a-201">The main access to the metadata writers within a codec is through the [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) interface that each WIC encoder implements.</span></span> <span data-ttu-id="b739a-202">Этот интерфейс позволяет приложениям перечислять каждый из блоков метаданных, внедренных в образ, чтобы можно было обнаружить и создать экземпляры соответствующего модуля записи метаданных для каждого блока метаданных.</span><span class="sxs-lookup"><span data-stu-id="b739a-202">This interface enables applications to enumerate each of the metadata blocks embedded in an image so that the appropriate metadata writer can be discovered and instantiated for each metadata block.</span></span> <span data-ttu-id="b739a-203">Блоки метаданных, у которых нет соответствующего модуля записи метаданных, считаются неизвестными и определяются как GUID CLSID \_ викункновнметадатареадер.</span><span class="sxs-lookup"><span data-stu-id="b739a-203">Metadata blocks that do not have a corresponding metadata writer are considered unknown, and are defined as the GUID CLSID\_WICUnknownMetadataReader.</span></span> <span data-ttu-id="b739a-204">Чтобы разрешить приложениям с поддержкой WIC сериализацию и запись формата метаданных, необходимо создать класс, реализующий следующие интерфейсы: [**ивикметадатавритер**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter), [**ивикметадатареадер**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader), [**ивикперсистстреам**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream)и [**ивикстреампровидер**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider).</span><span class="sxs-lookup"><span data-stu-id="b739a-204">To enable WIC enabled applications to serialize and write your metadata format, you must create a class that implements the following interfaces: [**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter), [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader), [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream), and [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider).</span></span>

> [!Note]  
> <span data-ttu-id="b739a-205">Если формат метаданных имеет ограничения, которые отображают некоторые методы требуемых интерфейсов, такие методы должны возвращать ВИНКОДЕК \_ Err \_ унсуппортедоператион.</span><span class="sxs-lookup"><span data-stu-id="b739a-205">If your metadata format has restrictions that render some methods of the required interfaces inappropriate, such methods should return WINCODEC\_ERR\_UNSUPPORTEDOPERATION.</span></span>

 

### <a name="iwicmetadatawriter-interface"></a><span data-ttu-id="b739a-206">Интерфейс Ивикметадатавритер</span><span class="sxs-lookup"><span data-stu-id="b739a-206">IWICMetadataWriter Interface</span></span>

<span data-ttu-id="b739a-207">Интерфейс [**ивикметадатавритер**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter) должен быть реализован модулем записи метаданных.</span><span class="sxs-lookup"><span data-stu-id="b739a-207">The [**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter) interface must be implemented by your metadata writer.</span></span> <span data-ttu-id="b739a-208">Кроме того, поскольку **ивикметадатавритер** наследует от [**ивикметадатареадер**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader), необходимо также реализовать все методы **ивикметадатареадер**.</span><span class="sxs-lookup"><span data-stu-id="b739a-208">Additionally, because **IWICMetadataWriter** inherits from [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader), you must also implement all the methods of **IWICMetadataReader**.</span></span> <span data-ttu-id="b739a-209">Так как для обоих типов обработчиков требуется одинаковое наследование интерфейса, может потребоваться создать один класс, предоставляющий функции чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="b739a-209">Because both handler types require the same interface inheritance, you might want to create a single class that provides both reading and writing functionality.</span></span>

<span data-ttu-id="b739a-210">В следующем коде показано определение интерфейса модуля записи метаданных, как определено в файле винкодексдк. idl.</span><span class="sxs-lookup"><span data-stu-id="b739a-210">The following code shows the definition of the metadata writer interface as defined in the wincodecsdk.idl file.</span></span>

``` syntax
interface IWICMetadataWriter : IWICMetadataReader
{
    HRESULT SetValue(
        [in, unique] const PROPVARIANT *pvarSchema,
        [in] const PROPVARIANT *pvarId,
        [in] const PROPVARIANT *pvarValue
        );

    HRESULT SetValueByIndex(
        [in] UINT nIndex,
        [in, unique] const PROPVARIANT *pvarSchema,
        [in] const PROPVARIANT *pvarId,
        [in] const PROPVARIANT *pvarValue
        );

    HRESULT RemoveValue(
        [in, unique] const PROPVARIANT *pvarSchema,
        [in] const PROPVARIANT *pvarId
        );

    HRESULT RemoveValueByIndex(
        [in] UINT nIndex
        );
};
```

<span data-ttu-id="b739a-211">Метод **SetValue** записывает заданный элемент метаданных в поток метаданных.</span><span class="sxs-lookup"><span data-stu-id="b739a-211">The **SetValue** method writes the specified metadata item to the metadata stream.</span></span>

<span data-ttu-id="b739a-212">Метод **сетвалуебиндекс** записывает указанный элемент метаданных в указанный индекс в потоке метаданных.</span><span class="sxs-lookup"><span data-stu-id="b739a-212">The **SetValueByIndex** method writes the specified metadata item to the specified index in the metadata stream.</span></span> <span data-ttu-id="b739a-213">Индекс не ссылается на идентификатор, а на позицию элемента в блоке метаданных.</span><span class="sxs-lookup"><span data-stu-id="b739a-213">The index does not refer to the ID but to the position of the item within the metadata block.</span></span>

<span data-ttu-id="b739a-214">Метод **ремовевалуе** удаляет указанный элемент метаданных из потока метаданных.</span><span class="sxs-lookup"><span data-stu-id="b739a-214">The **RemoveValue** method removes the specified metadata item from the metadata stream.</span></span>

<span data-ttu-id="b739a-215">Метод **ремовевалуебиндекс** удаляет элемент метаданных по указанному индексу из потока метаданных.</span><span class="sxs-lookup"><span data-stu-id="b739a-215">The **RemoveValueByIndex** method removes the metadata item at the specified index from the metadata stream.</span></span> <span data-ttu-id="b739a-216">После удаления элемента ожидается, что остальные элементы метаданных будут занимать освобожденный индекс, если индекс не является последним индексом.</span><span class="sxs-lookup"><span data-stu-id="b739a-216">After removing an item, it is expected that the remaining metadata items will occupy the vacated index if the index is not the last index.</span></span> <span data-ttu-id="b739a-217">Также ожидается, что счетчик будет изменяться после удаления элемента.</span><span class="sxs-lookup"><span data-stu-id="b739a-217">It is also expected that the count will change after the item is removed.</span></span>

<span data-ttu-id="b739a-218">Это обязанность модуля записи метаданных для преобразования элементов [пропвариант](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) в базовую структуру, необходимую для вашего формата.</span><span class="sxs-lookup"><span data-stu-id="b739a-218">It is the metadata writer's responsibility to convert the [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) items to the underlying structure required by your format.</span></span> <span data-ttu-id="b739a-219">Однако, в отличие от средства чтения метаданных, типы VARIANT обычно не следует приводить к разным типам, так как вызывающий объект явно указывает, какой тип данных следует использовать.</span><span class="sxs-lookup"><span data-stu-id="b739a-219">However, unlike the metadata reader, VARIANT types should not normally be coerced to different types as the caller is specifically indicating what data type to use.</span></span>

<span data-ttu-id="b739a-220">Модуль записи метаданных должен зафиксировать все элементы метаданных в потоке изображений, включая скрытые или нераспознанные значения.</span><span class="sxs-lookup"><span data-stu-id="b739a-220">Your metadata writer must commit all metadata items to the image stream, including hidden or unrecognized values.</span></span> <span data-ttu-id="b739a-221">Сюда входят неизвестные вложенные блоки метаданных.</span><span class="sxs-lookup"><span data-stu-id="b739a-221">This includes unknown nested metadata blocks.</span></span> <span data-ttu-id="b739a-222">Тем не менее, прежде чем инициировать операцию сохранения, необходимо, чтобы кодировщик установил все критические элементы метаданных.</span><span class="sxs-lookup"><span data-stu-id="b739a-222">However, it is the encoder's responsibility to set any critical metadata items prior to initiating the save operation.</span></span>

<span data-ttu-id="b739a-223">Если поток метаданных содержит содержимое с обратным порядком байтов, то модуль записи метаданных отвечает за обмен обрабатываемыми им значениями данных.</span><span class="sxs-lookup"><span data-stu-id="b739a-223">If the metadata stream contains big-endian content, the metadata writer is responsible for swapping any data values it processes.</span></span> <span data-ttu-id="b739a-224">Он также отвечает за уведомление всех вложенных модулей записи метаданных о том, что они работают с потоком данных с обратным порядком байтов при сохранении.</span><span class="sxs-lookup"><span data-stu-id="b739a-224">It is also responsible for informing any nested metadata writers that they are working with a big-endian data stream when they save.</span></span>

<span data-ttu-id="b739a-225">Реализуйте поддержку создания и удаления пространства имен путем поддержки операций Set и Remove для элементов метаданных с типом `VT_CLSID` (GUID), соответствующим формату метаданных.</span><span class="sxs-lookup"><span data-stu-id="b739a-225">Implement support for namespace creation and removal by supporting set and remove operations on metadata items with a type of `VT_CLSID` (a GUID) corresponding to a metadata format.</span></span> <span data-ttu-id="b739a-226">Модуль записи метаданных вызывает функцию [**виксериализеметадатаконтент**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicserializemetadatacontent) для правильного внедрения вложенного содержимого модуля записи метаданных в родительский модуль записи метаданных.</span><span class="sxs-lookup"><span data-stu-id="b739a-226">The metadata writer calls the [**WICSerializeMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicserializemetadatacontent) function to properly embed the nested metadata writer content into the parent metadata writer.</span></span>

<span data-ttu-id="b739a-227">Если ваш формат метаданных поддерживает кодирование на месте, вы несете ответственность за управление обязательным заполнением.</span><span class="sxs-lookup"><span data-stu-id="b739a-227">If your metadata format supports in-place encoding, you are responsible for managing the required padding.</span></span> <span data-ttu-id="b739a-228">Дополнительные сведения о кодировке на месте см. в разделе [Общие сведения о метаданных WIC](-wic-about-metadata.md) и [Обзор чтения и записи метаданных изображения](-wic-codec-readingwritingmetadata.md).</span><span class="sxs-lookup"><span data-stu-id="b739a-228">For more information on in-place encoding, see [WIC Metadata Overview](-wic-about-metadata.md) and [Overview of Reading and Writing Image Metadata](-wic-codec-readingwritingmetadata.md).</span></span>

### <a name="iwicpersiststream-interface"></a><span data-ttu-id="b739a-229">Интерфейс Ивикперсистстреам</span><span class="sxs-lookup"><span data-stu-id="b739a-229">IWICPersistStream Interface</span></span>

<span data-ttu-id="b739a-230">Интерфейс [**ивикперсистстреам**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) наследует от класса **IPersistStream** и предоставляет дополнительные методы для сохранения и загрузки объектов с помощью перечисления [**викперсистоптионс**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) .</span><span class="sxs-lookup"><span data-stu-id="b739a-230">The [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) interface inherits from **IPersistStream** and provides additional methods for saving and loading objects by using the [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) enumeration.</span></span>

<span data-ttu-id="b739a-231">В следующем коде показано определение интерфейса [**ивикперсистстреам**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) , как определено в файле винкодексдк. idl.</span><span class="sxs-lookup"><span data-stu-id="b739a-231">The following code shows the definition of the [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) interface as defined in the wincodecsdk.idl file.</span></span>

``` syntax
interface IWICPersistStream : IPersistStream
{
    HRESULT LoadEx(
        [in, unique] IStream *pIStream,
        [in, unique] const GUID *pguidPreferredVendor,
        [in] DWORD dwPersistOptions
        );

    HRESULT SaveEx(
        [in] IStream *pIStream,
        [in] DWORD dwPersistOptions,
        [in] BOOL fClearDirty
        );
};
```

<span data-ttu-id="b739a-232">Метод **лоадекс** предоставляет обработчик метаданных с потоком данных, содержащим блок метаданных.</span><span class="sxs-lookup"><span data-stu-id="b739a-232">The **LoadEx** method provides your metadata handler with a data stream containing your metadata block.</span></span>

<span data-ttu-id="b739a-233">Метод **Савикс** сериализует метаданные в поток.</span><span class="sxs-lookup"><span data-stu-id="b739a-233">The **SaveEx** method serializes the metadata into a stream.</span></span> <span data-ttu-id="b739a-234">Если предоставленный поток совпадает с потоком инициализации, необходимо выполнить кодирование на месте.</span><span class="sxs-lookup"><span data-stu-id="b739a-234">If the provided stream is the same as initialization stream, you should perform in-place encoding.</span></span> <span data-ttu-id="b739a-235">Если поддерживается кодировка на месте, этот метод должен возвращать ВИНКОДЕК \_ Err \_ тумучметадата, если для выполнения кодирования на месте недостаточно заполнения.</span><span class="sxs-lookup"><span data-stu-id="b739a-235">If in-place encoding is supported, this method should return WINCODEC\_ERR\_TOOMUCHMETADATA when there is insufficient padding to perform in-place encoding.</span></span> <span data-ttu-id="b739a-236">Если кодировка на месте не поддерживается, этот метод должен возвращать ВИНКОДЕК \_ Err \_ унсуппортедоператион.</span><span class="sxs-lookup"><span data-stu-id="b739a-236">If in-place encoding is not supported, this method should return WINCODEC\_ERR\_UNSUPPORTEDOPERATION.</span></span>

<span data-ttu-id="b739a-237">Метод **IPersistStream:: жетсиземакс** должен быть реализован и должен возвращать точный размер содержимого метаданных, которое будет записано при последующем сохранении.</span><span class="sxs-lookup"><span data-stu-id="b739a-237">The **IPersistStream::GetSizeMax** method must be implemented and must return the exact size of the metadata content that would be written in subsequent save.</span></span>

<span data-ttu-id="b739a-238">Метод **IPersistStream:: IsDirty** должен быть реализован, если модуль записи метаданных инициализируется через поток, чтобы образ мог надежно определить, изменилось ли его содержимое.</span><span class="sxs-lookup"><span data-stu-id="b739a-238">The **IPersistStream::IsDirty** method should be implemented if the metadata writer is initialized through a stream, so that an image can reliably determine whether its content has changed.</span></span>

<span data-ttu-id="b739a-239">Если формат метаданных поддерживает вложенные блоки метаданных, то модуль записи метаданных должен делегировать вложенным средствам записи метаданных сериализацию его содержимого при сохранении в поток.</span><span class="sxs-lookup"><span data-stu-id="b739a-239">If your metadata format supports nested metadata blocks, your metadata writer should delegate to the nested metadata writers the serializing of its content when saving to a stream.</span></span>

### <a name="iwicstreamprovider-interface"></a><span data-ttu-id="b739a-240">Интерфейс Ивикстреампровидер</span><span class="sxs-lookup"><span data-stu-id="b739a-240">IWICStreamProvider Interface</span></span>

<span data-ttu-id="b739a-241">Реализация интерфейса [**ивикстреампровидер**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider) для модуля записи метаданных аналогична реализации средства чтения метаданных.</span><span class="sxs-lookup"><span data-stu-id="b739a-241">The implementation of the [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider) interface for a metadata writer is the same as that of a metadata reader.</span></span> <span data-ttu-id="b739a-242">Дополнительные сведения см. в разделе Создание модуля чтения метаданных в этом документе.</span><span class="sxs-lookup"><span data-stu-id="b739a-242">For more information, see Creating a Metadata Reader section in this document.</span></span>

## <a name="installing-and-registering-a-metadata-handler"></a><span data-ttu-id="b739a-243">Установка и регистрация обработчика метаданных</span><span class="sxs-lookup"><span data-stu-id="b739a-243">Installing and Registering a Metadata Handler</span></span>

<span data-ttu-id="b739a-244">Чтобы установить обработчик метаданных, необходимо предоставить сборку обработчика и зарегистрировать ее в системном реестре.</span><span class="sxs-lookup"><span data-stu-id="b739a-244">To install a metadata handler, you must provide the handler assembly and register it in the system registry.</span></span> <span data-ttu-id="b739a-245">Вы можете решить, как и когда будут заполнены разделы реестра.</span><span class="sxs-lookup"><span data-stu-id="b739a-245">You can decide how and when the registry keys are populated.</span></span>

> [!Note]  
> <span data-ttu-id="b739a-246">Для удобства чтения фактические шестнадцатеричные идентификаторы GUID не отображаются в разделах реестра, приведенных в следующих разделах этого документа.</span><span class="sxs-lookup"><span data-stu-id="b739a-246">For readability, the actual hexadecimal GUIDs are not shown in the registry keys shown in the following sections of this document.</span></span> <span data-ttu-id="b739a-247">Чтобы найти шестнадцатеричное значение для указанного понятного имени, см. файлы винкодек. idl и винкодексдк. idl.</span><span class="sxs-lookup"><span data-stu-id="b739a-247">To find the hexadecimal value for a specified friendly name, see the wincodec.idl and wincodecsdk.idl files.</span></span>

 

### <a name="metadata-handler-registry-keys"></a><span data-ttu-id="b739a-248">Разделы реестра обработчика метаданных</span><span class="sxs-lookup"><span data-stu-id="b739a-248">Metadata Handler Registry Keys</span></span>

<span data-ttu-id="b739a-249">Каждый обработчик метаданных идентифицируется уникальным идентификатором CLSID, и каждый обработчик должен зарегистрировать его CLSID в идентификаторе GUID идентификатора категории обработчика метаданных.</span><span class="sxs-lookup"><span data-stu-id="b739a-249">Each metadata handler is identified by a unique CLSID, and each handler is required to register its CLSID under the metadata handler's category ID GUID.</span></span> <span data-ttu-id="b739a-250">Идентификатор категории каждого типа обработчика определяется в винкодек. idl; имя идентификатора категории для читателей — CATID \_ викметадатареадер, а имя идентификатора категории для модулей записи — CATID \_ викметадатавритер.</span><span class="sxs-lookup"><span data-stu-id="b739a-250">Each handler type's category ID is defined in the wincodec.idl; the category ID name for readers is CATID\_WICMetadataReader, and the category ID name for writers is CATID\_WICMetadataWriter.</span></span>

<span data-ttu-id="b739a-251">Каждый обработчик метаданных идентифицируется уникальным идентификатором CLSID, и каждый обработчик должен зарегистрировать его CLSID в идентификаторе GUID идентификатора категории обработчика метаданных.</span><span class="sxs-lookup"><span data-stu-id="b739a-251">Each metadata handler is identified by a unique CLSID, and each handler is required to register its CLSID under the metadata handler's category ID GUID.</span></span> <span data-ttu-id="b739a-252">Идентификатор категории каждого типа обработчика определяется в винкодек. idl; имя идентификатора категории для читателей — CATID \_ викметадатареадер, а имя идентификатора категории для модулей записи — CATID \_ викметадатавритер.</span><span class="sxs-lookup"><span data-stu-id="b739a-252">Each handler type's category ID is defined in the wincodec.idl; the category ID name for readers is CATID\_WICMetadataReader, and the category ID name for writers is CATID\_WICMetadataWriter.</span></span>

> [!Note]  
> <span data-ttu-id="b739a-253">В следующих листингах разделов реестра {Reader CLSID} относится к уникальному идентификатору CLSID, предоставленному для средства чтения метаданных.</span><span class="sxs-lookup"><span data-stu-id="b739a-253">In the following registry key listings, {Reader CLSID} refers to the unique CLSID that you provide for your metadata reader.</span></span> <span data-ttu-id="b739a-254">{Writer CLSID} относится к уникальному идентификатору CLSID, предоставленному для модуля записи метаданных.</span><span class="sxs-lookup"><span data-stu-id="b739a-254">{Writer CLSID} refers to the unique CLSID that you provide for your metadata writer.</span></span> <span data-ttu-id="b739a-255">{Handler CLSID} относится к CLSID модуля чтения, CLSID модуля записи или к обоим, в зависимости от предоставляемых обработчиков.</span><span class="sxs-lookup"><span data-stu-id="b739a-255">{Handler CLSID} refers to the reader's CLSID, the writer's CLSID, or both, depending on which handlers you are providing.</span></span> <span data-ttu-id="b739a-256">{Контейнер GUID} относится к объекту контейнера (формат изображения или формат метаданных), который может содержать блок метаданных.</span><span class="sxs-lookup"><span data-stu-id="b739a-256">{Container GUID} refers to the container object (image format or metadata format) that can contain the metadata block.</span></span>

 

<span data-ttu-id="b739a-257">Следующие разделы реестра регистрируют обработчик метаданных с другими доступными обработчиками метаданных:</span><span class="sxs-lookup"><span data-stu-id="b739a-257">The following registry keys register your metadata handler with the other metadata handlers available:</span></span>

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{CATID_WICMetadataReaders}\Instance\{Reader CLSID}]
CLSID={Reader CLSID}
Friendly Name="Reader Name"

[HKEY_CLASSES_ROOT\CLSID\{CATID_ WICMetadataWriters}\Instance\{Writer CLSID}]
CLSID={Writer CLSID}
Friendly Name="Writer Name"
```

<span data-ttu-id="b739a-258">Кроме регистрации обработчиков в соответствующих категориях, необходимо также зарегистрировать дополнительные ключи, предоставляющие сведения, относящиеся к обработчику.</span><span class="sxs-lookup"><span data-stu-id="b739a-258">In addition to registering your handlers in their respective categories, you must also register additional keys that provide information specific to the handler.</span></span> <span data-ttu-id="b739a-259">Читатели и модули записи имеют аналогичные требования к разделам реестра.</span><span class="sxs-lookup"><span data-stu-id="b739a-259">Readers and writers share similar registry key requirements.</span></span> <span data-ttu-id="b739a-260">В следующем синтаксисе показано, как зарегистрировать обработчик.</span><span class="sxs-lookup"><span data-stu-id="b739a-260">The following syntax shows how to register a handler.</span></span> <span data-ttu-id="b739a-261">Обработчик чтения и обработчик записи должны быть зарегистрированы таким образом, используя соответствующие идентификаторы CLSID:</span><span class="sxs-lookup"><span data-stu-id="b739a-261">Both the reader handler and writer handler must be registered in this way, using their respective CLSIDs:</span></span>

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{CLSID}]
"Vendor"={VendorGUID}
"Date"="yyyy-mm-dd"
"Version"="Major.Minor.Build.Number"
"SpecVersion"="Major.Minor.Build.Number"
"MetadataFormat"={MetadataFormatGUID}
"RequiresFullStream"=dword:1|0
"SupportsPadding"= dword:1|0
"FixedSize"=0

[HKEY_CLASSES_ROOT\CLSID\{CLSID}\InProcServer32]
@="drive:\path\yourdll.dll"
"ThreadingModel"="Apartment"

[HKEY_CLASSES_ROOT\CLSID\{CLSID}\{LCID}]
Author="Author's Name"
Description = " Metadata Description"
DeviceManufacturer ="Manufacturer Name"
DeviceModels="Device,Device"
FriendlyName="Friendly Name"
```

### <a name="metadata-readers"></a><span data-ttu-id="b739a-262">Читатели метаданных</span><span class="sxs-lookup"><span data-stu-id="b739a-262">Metadata Readers</span></span>

<span data-ttu-id="b739a-263">Регистрация модуля чтения метаданных также включает ключи, описывающие, как читатель может быть внедрен в формат контейнера.</span><span class="sxs-lookup"><span data-stu-id="b739a-263">The metadata reader registration also includes keys that describe how the reader can be embedded in a container format.</span></span> <span data-ttu-id="b739a-264">Форматом контейнера может быть формат изображения, например TIFF или JPEG; Он также может быть другим форматом метаданных, таким как блок метаданных IFD.</span><span class="sxs-lookup"><span data-stu-id="b739a-264">A container format can be an image format such as TIFF or JPEG; it can also be another metadata format such as an IFD metadata block.</span></span> <span data-ttu-id="b739a-265">Собственные Поддерживаемые форматы контейнеров изображений перечислены в винкодек. idl; Каждый формат контейнера изображений определяется как GUID с именем, которое начинается с GUID \_ контаинерформат.</span><span class="sxs-lookup"><span data-stu-id="b739a-265">Natively supported image container formats are listed in wincodec.idl; each image container format is defined as a GUID with a name that begins with GUID\_ContainerFormat.</span></span> <span data-ttu-id="b739a-266">Изначально поддерживаемые форматы контейнеров метаданных перечислены в винкодексдк. idl; Каждый формат контейнера метаданных определяется как GUID с именем, которое начинается с GUID \_ метадатаформат.</span><span class="sxs-lookup"><span data-stu-id="b739a-266">Natively supported metadata container formats are listed in wincodecsdk.idl; each metadata container format is defined as a GUID with a name that begins with GUID\_MetadataFormat.</span></span>

<span data-ttu-id="b739a-267">Следующие ключи регистрируют контейнер, который поддерживает модуль чтения метаданных, и данные, необходимые для чтения из этого контейнера.</span><span class="sxs-lookup"><span data-stu-id="b739a-267">The following keys register a container that the metadata reader supports, and the data needed to read from that container.</span></span> <span data-ttu-id="b739a-268">Каждый контейнер, поддерживаемый модулем чтения, должен быть зарегистрирован таким образом.</span><span class="sxs-lookup"><span data-stu-id="b739a-268">Each container supported by the reader must be registered in this way.</span></span>

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{Reader CLSID}\Containers\{Container GUID}\0]
"Position"=dword:00000000
"Pattern"=hex:ff,ff,ff,...
"Mask"=hex:ff,ff,ff,...
"DataOffset"=dword:00000006
```

<span data-ttu-id="b739a-269">Ключ шаблона описывает двоичный шаблон, который используется для сопоставления блока метаданных с модулем чтения.</span><span class="sxs-lookup"><span data-stu-id="b739a-269">The Pattern key describes the binary pattern that is used to match the metadata block to the reader.</span></span> <span data-ttu-id="b739a-270">При определении шаблона для модуля чтения метаданных он должен быть достаточно надежным, что положительное соответствие означает, что читатель метаданных может понять метаданные в обрабатываемом блоке метаданных.</span><span class="sxs-lookup"><span data-stu-id="b739a-270">When defining a pattern for your metadata reader, it should be reliable enough that a positive match means the metadata reader can understand the metadata in the metadata block being processed.</span></span>

<span data-ttu-id="b739a-271">Ключ СМЕЩ описывает фиксированное смещение метаданных из заголовка блока.</span><span class="sxs-lookup"><span data-stu-id="b739a-271">The DataOffset key describes the fixed offset of the metadata from the block header.</span></span> <span data-ttu-id="b739a-272">Этот ключ является необязательным и, если он не указан, означает, что фактические метаданные не могут быть найдены с помощью фиксированного смещения из заголовка блока.</span><span class="sxs-lookup"><span data-stu-id="b739a-272">This key is optional and, if not specified, means that the actual metadata cannot be located using a fixed offset from the block header.</span></span>

### <a name="metadata-writers"></a><span data-ttu-id="b739a-273">Записи метаданных</span><span class="sxs-lookup"><span data-stu-id="b739a-273">Metadata Writers</span></span>

<span data-ttu-id="b739a-274">Регистрация модуля записи метаданных также включает ключи, описывающие, как записать заголовок перед содержимым метаданных, внедренным в формат контейнера.</span><span class="sxs-lookup"><span data-stu-id="b739a-274">The metadata writer registration also includes keys that describe how to write out the header preceding the metadata content embedded in a container format.</span></span> <span data-ttu-id="b739a-275">Как и в случае с модулем чтения, формат контейнера может быть форматом изображения или другим блоком метаданных.</span><span class="sxs-lookup"><span data-stu-id="b739a-275">As with the reader, a container format can be an image format or another metadata block.</span></span>

<span data-ttu-id="b739a-276">Следующие ключи регистрируют контейнер, который поддерживает модуль записи метаданных, и данные, необходимые для записи заголовка и метаданных.</span><span class="sxs-lookup"><span data-stu-id="b739a-276">The following keys register a container that the metadata writer supports, and the data needed to write the header and metadata.</span></span> <span data-ttu-id="b739a-277">Каждый контейнер, поддерживаемый модулем записи, должен быть зарегистрирован таким образом.</span><span class="sxs-lookup"><span data-stu-id="b739a-277">Each container supported by the writer must be registered in this way.</span></span>

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{Writer CLSID}\Containers\{Container GUID}]
"WritePosition"=dword:00000000
"WriteHeader"=hex:ff,ff,ff,...
"WriteOffset"=dword:00000000
```

<span data-ttu-id="b739a-278">Ключ Вритехеадер описывает двоичный шаблон заголовков блоков метаданных для написания.</span><span class="sxs-lookup"><span data-stu-id="b739a-278">The WriteHeader key describes the binary pattern of the metadata block header to be written.</span></span> <span data-ttu-id="b739a-279">Этот двоичный шаблон совпадает с ключом шаблона считывания в формате метаданных.</span><span class="sxs-lookup"><span data-stu-id="b739a-279">This binary pattern coincides with the metadata format's reader Pattern key.</span></span>

<span data-ttu-id="b739a-280">Ключ Вритеоффсет описывает фиксированное смещение в заголовке блока, в котором должны быть записаны метаданные.</span><span class="sxs-lookup"><span data-stu-id="b739a-280">The WriteOffset key describes the fixed offset from the block header at which the metadata should be written.</span></span> <span data-ttu-id="b739a-281">Этот ключ является необязательным и, если он не указан, означает, что фактические метаданные не должны записываться вместе с заголовком.</span><span class="sxs-lookup"><span data-stu-id="b739a-281">This key is optional and, if not specified, means that the actual metadata should not be written out with the header.</span></span>

### <a name="signing-a-metadata-handler"></a><span data-ttu-id="b739a-282">Подписывание обработчика метаданных</span><span class="sxs-lookup"><span data-stu-id="b739a-282">Signing a Metadata Handler</span></span>

<span data-ttu-id="b739a-283">Все обработчики метаданных должны иметь цифровую подпись для участия в процессе обнаружения WIC.</span><span class="sxs-lookup"><span data-stu-id="b739a-283">All metadata handlers must be digitally signed to participate in the WIC discovery process.</span></span> <span data-ttu-id="b739a-284">Компонент WIC не будет загружать обработчик, не подписанный доверенным центром сертификации.</span><span class="sxs-lookup"><span data-stu-id="b739a-284">WIC will not load any handler that is not signed by a trusted certificate authority.</span></span> <span data-ttu-id="b739a-285">Дополнительные сведения о цифровой подписи см. в статье [Введение в подписывание кода](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b739a-285">For more information on digital signing, see [Introduction to Code Signing](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)).</span></span>

## <a name="special-considerations"></a><span data-ttu-id="b739a-286">Особые рекомендации</span><span class="sxs-lookup"><span data-stu-id="b739a-286">Special Considerations</span></span>

<span data-ttu-id="b739a-287">В следующих разделах содержатся дополнительные сведения, которые необходимо учитывать при создании собственных обработчиков метаданных.</span><span class="sxs-lookup"><span data-stu-id="b739a-287">The following sections include additional information you must consider when creating your own metadata handlers.</span></span>

### <a name="propvariants"></a><span data-ttu-id="b739a-288">пропвариантс</span><span class="sxs-lookup"><span data-stu-id="b739a-288">PROPVARIANTS</span></span>

<span data-ttu-id="b739a-289">Компонент WIC использует [пропвариант](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) для представления элемента метаданных как для чтения, так и для записи.</span><span class="sxs-lookup"><span data-stu-id="b739a-289">WIC uses a [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) to represent a metadata item for both reading and writing.</span></span> <span data-ttu-id="b739a-290">ПРОПВАРИАНТ предоставляет тип данных и значение данных для элемента метаданных, используемого в формате метаданных.</span><span class="sxs-lookup"><span data-stu-id="b739a-290">A PROPVARIANT provides a data type and data value for a metadata item used within a metadata format.</span></span> <span data-ttu-id="b739a-291">Как средство записи обработчика метаданных, вы получаете множество гибкости в том, как данные хранятся в формате метаданных и как данные представлены в блоке метаданных.</span><span class="sxs-lookup"><span data-stu-id="b739a-291">As the writer of a metadata handler, you have a lot of flexibility on how data is stored in the metadata format and how data is represented within a metadata block.</span></span> <span data-ttu-id="b739a-292">В следующей таблице приведены рекомендации по выбору подходящего типа ПРОПВАРИАНТ для использования в различных ситуациях.</span><span class="sxs-lookup"><span data-stu-id="b739a-292">The following table provides guidelines to help you decide on the appropriate PROPVARIANT type to use in different situations.</span></span>



| <span data-ttu-id="b739a-293">Тип метаданных —...</span><span class="sxs-lookup"><span data-stu-id="b739a-293">Metadata type is...</span></span>          | <span data-ttu-id="b739a-294">Использовать тип ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="b739a-294">Use PROPVARIANT type</span></span>      | <span data-ttu-id="b739a-295">ПРОПВАРИАНТ, свойство</span><span class="sxs-lookup"><span data-stu-id="b739a-295">PROPVARIANT Property</span></span>                                                                                                                                                                                                                                                           |
|------------------------------|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b739a-296">Пустой или не существует.</span><span class="sxs-lookup"><span data-stu-id="b739a-296">Empty or non-existent.</span></span>       | <span data-ttu-id="b739a-297">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="b739a-297">VT\_EMPTY</span></span>                 | <span data-ttu-id="b739a-298">Не применяется</span><span class="sxs-lookup"><span data-stu-id="b739a-298">Not applicable.</span></span>                                                                                                                                                                                                                                                                |
| <span data-ttu-id="b739a-299">Не определено.</span><span class="sxs-lookup"><span data-stu-id="b739a-299">Undefined.</span></span>                   | <span data-ttu-id="b739a-300">\_большой двоичный объект VT</span><span class="sxs-lookup"><span data-stu-id="b739a-300">VT\_BLOB</span></span>                  | <span data-ttu-id="b739a-301">Свойство BLOB используется для установки размера и указателя на объект большого двоичного объекта, выделенный с помощью функции CoTaskMemAlloc.</span><span class="sxs-lookup"><span data-stu-id="b739a-301">Use the blob property to set the size and pointer to the BLOB object allocated using CoTaskMemAlloc.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="b739a-302">Блок метаданных.</span><span class="sxs-lookup"><span data-stu-id="b739a-302">A metadata block.</span></span>            | <span data-ttu-id="b739a-303">VT \_ Unknown</span><span class="sxs-lookup"><span data-stu-id="b739a-303">VT\_UNKNOWN</span></span>               | <span data-ttu-id="b739a-304">Этот тип использует свойство Пунквал.</span><span class="sxs-lookup"><span data-stu-id="b739a-304">This type uses the punkVal property.</span></span>                                                                                                                                                                                                                                           |
| <span data-ttu-id="b739a-305">Массив типов.</span><span class="sxs-lookup"><span data-stu-id="b739a-305">An array of types.</span></span>           | <span data-ttu-id="b739a-306">VT \_ вектор \| VT \_ {Type}</span><span class="sxs-lookup"><span data-stu-id="b739a-306">VT\_VECTOR \| VT\_{type}</span></span>  | <span data-ttu-id="b739a-307">Используйте свойство CA {Type}, чтобы задать число и указатель на массив, выделенный с помощью функции CoTaskMemAlloc.</span><span class="sxs-lookup"><span data-stu-id="b739a-307">Use the ca{type} property to set the count and pointer to the array allocated using CoTaskMemAlloc.</span></span>                                                                                                                                                                            |
| <span data-ttu-id="b739a-308">Массив блоков метаданных.</span><span class="sxs-lookup"><span data-stu-id="b739a-308">An array of metadata blocks.</span></span> | <span data-ttu-id="b739a-309">VT \_ Векторный \| \_ вариант VT</span><span class="sxs-lookup"><span data-stu-id="b739a-309">VT\_VECTOR \| VT\_VARIANT</span></span> | <span data-ttu-id="b739a-310">Чтобы задать массив вариантов, используйте свойство капропвар.</span><span class="sxs-lookup"><span data-stu-id="b739a-310">Use the capropvar property to set the array of variants.</span></span>                                                                                                                                                                                                                       |
| <span data-ttu-id="b739a-311">Рациональное значение со знаком.</span><span class="sxs-lookup"><span data-stu-id="b739a-311">A signed rational value.</span></span>     | <span data-ttu-id="b739a-312">VT \_ i8</span><span class="sxs-lookup"><span data-stu-id="b739a-312">VT\_I8</span></span>                    | <span data-ttu-id="b739a-313">Чтобы задать значение, используйте свойство Хвал.</span><span class="sxs-lookup"><span data-stu-id="b739a-313">Use the hVal property to set the value.</span></span> <span data-ttu-id="b739a-314">Задайте в качестве максимального слова знаменатель и нижнее слово в числителе.</span><span class="sxs-lookup"><span data-stu-id="b739a-314">Set the high word to the denominator and the low word to the numerator.</span></span>                                                                                                                                                                |
| <span data-ttu-id="b739a-315">Рациональное значение.</span><span class="sxs-lookup"><span data-stu-id="b739a-315">A rational value.</span></span>            | <span data-ttu-id="b739a-316">VT \_ UI8</span><span class="sxs-lookup"><span data-stu-id="b739a-316">VT\_UI8</span></span>                   | <span data-ttu-id="b739a-317">Чтобы задать значение, используйте свойство Ухвал.</span><span class="sxs-lookup"><span data-stu-id="b739a-317">Use the uhVal property to set the value.</span></span> <span data-ttu-id="b739a-318">Задайте для Хигхпарт знаменатель и Ловпарт в числителе.</span><span class="sxs-lookup"><span data-stu-id="b739a-318">Set the HighPart to the denominator and the LowPart to the numerator.</span></span> <span data-ttu-id="b739a-319">Обратите внимание, что Ловпарт — это целое число без знака. Числитель должен быть преобразован из целого числа без знака в тип int, чтобы обеспечить сохранение бита знака при его наличии.</span><span class="sxs-lookup"><span data-stu-id="b739a-319">Note that the LowPart is an unsigned int. The numerator should be converted from an unsigned int to an int to ensure that the sign bit is preserved if present.</span></span> |



 

<span data-ttu-id="b739a-320">Чтобы избежать избыточности в представлении элементов массива, не используйте надежные массивы. Используйте только простые массивы.</span><span class="sxs-lookup"><span data-stu-id="b739a-320">To avoid redundancy in representing array items, do not use safe arrays; use only simple arrays.</span></span> <span data-ttu-id="b739a-321">Это сокращает объем работы, которую приложение должно выполнить при интерпретации типов [пропвариант](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .</span><span class="sxs-lookup"><span data-stu-id="b739a-321">This reduces the work an application needs to perform when interpreting [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) types.</span></span>

<span data-ttu-id="b739a-322">Старайтесь не использовать `VT_BYREF` и хранить значения встроенным, когда это возможно.</span><span class="sxs-lookup"><span data-stu-id="b739a-322">Avoid using `VT_BYREF` and store values inline whenever possible.</span></span> <span data-ttu-id="b739a-323">`VT_BYREF` неэффективно для небольших типов (общих для элементов метаданных) и не предоставляет сведений о размере.</span><span class="sxs-lookup"><span data-stu-id="b739a-323">`VT_BYREF` is inefficient for small types (common for metadata items) and does not provide size information.</span></span>

<span data-ttu-id="b739a-324">Перед использованием [пропвариант](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)всегда вызывайте **пропвариантинит** для инициализации значения.</span><span class="sxs-lookup"><span data-stu-id="b739a-324">Before using a [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant), always call **PropVariantInit** to initialize the value.</span></span> <span data-ttu-id="b739a-325">По завершении работы с ПРОПВАРИАНТ всегда вызывайте **пропвариантклеар** , чтобы освободить память, выделенную для переменной.</span><span class="sxs-lookup"><span data-stu-id="b739a-325">When you are finished with the PROPVARIANT, always call **PropVariantClear** to release any memory allocated for the variable.</span></span>

### <a name="8bim-handlers"></a><span data-ttu-id="b739a-326">Обработчики 8BIM</span><span class="sxs-lookup"><span data-stu-id="b739a-326">8BIM Handlers</span></span>

<span data-ttu-id="b739a-327">При записи обработчика метаданных для блока метаданных 8BIM необходимо использовать сигнатуру, которая инкапсулирует сигнатуру 8BIM и идентификатор.</span><span class="sxs-lookup"><span data-stu-id="b739a-327">When writing a metadata handler for an 8BIM metadata block, you must use a signature that encapsulates both the 8BIM signature and the ID.</span></span> <span data-ttu-id="b739a-328">Например, модуль чтения метаданных собственного 8BIMIPTC предоставляет следующие сведения о реестре для обнаружения модуля чтения:</span><span class="sxs-lookup"><span data-stu-id="b739a-328">For example, the native 8BIMIPTC metadata reader provides the following registry information for reader discovery:</span></span>

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{0010668C-0801-4DA6-A4A4-826522B6D28F}\Containers\{16100D66-8570-4BB9-B92D-FDA4B23ECE67}\0]
"Position"=dword:00000000
"Pattern"=hex:38,42,49,4d,04,04
"Mask"=hex:ff,ff,ff,ff,ff,ff
"DataOffset"=dword:00000006
```

<span data-ttu-id="b739a-329">Модуль чтения 8BIMIPTC имеет зарегистрированный шаблон 0x38, 0x42, 0x49, 0x4D, 0x04, 0x04.</span><span class="sxs-lookup"><span data-stu-id="b739a-329">The 8BIMIPTC reader has a registered pattern of 0x38, 0x42, 0x49, 0x4D, 0x04, 0x04.</span></span> <span data-ttu-id="b739a-330">Первые четыре байта (0x38, 0x42, 0x49, 0x4D) являются сигнатурой 8BIM, а последние два байта (0x04, 0x04) — идентификатор записи IPTC.</span><span class="sxs-lookup"><span data-stu-id="b739a-330">The first four bytes (0x38, 0x42, 0x49, 0x4D) are the 8BIM signature, and the last two bytes (0x04, 0x04) are the ID for the IPTC record.</span></span>

<span data-ttu-id="b739a-331">Таким образом, чтобы написать средство чтения метаданных 8BIM для получения сведений о разрешении, потребуется зарегистрированный шаблон 0x38, 0x42, 0x49, 0x4D, 0x03, 0xED.</span><span class="sxs-lookup"><span data-stu-id="b739a-331">So, to write an 8BIM metadata reader for resolution information, you would need a registered pattern of 0x38, 0x42, 0x49, 0x4D, 0x03, 0xED.</span></span> <span data-ttu-id="b739a-332">Опять же, первые четыре байта (0x38, 0x42, 0x49, 0x4D) являются сигнатурой 8BIM.</span><span class="sxs-lookup"><span data-stu-id="b739a-332">Again, the first four bytes (0x38, 0x42, 0x49, 0x4D) are the 8BIM signature.</span></span> <span data-ttu-id="b739a-333">Последние два байта (0x03, 0xED), однако, являются ИДЕНТИФИКАТОРом сведений о разрешении, как определено в формате PSD.</span><span class="sxs-lookup"><span data-stu-id="b739a-333">The last two bytes (0x03, 0xED), however, are the resolution information ID as defined by the PSD format.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b739a-334">См. также</span><span class="sxs-lookup"><span data-stu-id="b739a-334">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="b739a-335">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="b739a-335">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b739a-336">Общие сведения о компоненте создания образов Windows</span><span class="sxs-lookup"><span data-stu-id="b739a-336">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="b739a-337">Общие сведения о метаданных компонента WIC</span><span class="sxs-lookup"><span data-stu-id="b739a-337">WIC Metadata Overview</span></span>](-wic-about-metadata.md)
</dt> <dt>

[<span data-ttu-id="b739a-338">Общие сведения о языке запросов метаданных</span><span class="sxs-lookup"><span data-stu-id="b739a-338">Metadata Query Language Overview</span></span>](-wic-codec-metadataquerylanguage.md)
</dt> <dt>

[<span data-ttu-id="b739a-339">Общие сведения о чтении и записи метаданных изображений</span><span class="sxs-lookup"><span data-stu-id="b739a-339">Overview of Reading and Writing Image Metadata</span></span>](-wic-codec-readingwritingmetadata.md)
</dt> <dt>

[<span data-ttu-id="b739a-340">Пошаговое руководство. повторное кодирование изображения JPEG с помощью метаданных</span><span class="sxs-lookup"><span data-stu-id="b739a-340">How-to: Re-encode a JPEG Image with Metadata</span></span>](-wic-codec-jpegmetadataencoding.md)
</dt> <dt>

<span data-ttu-id="b739a-341">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="b739a-341">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="b739a-342">Написание WIC-Enabled КОДЕка</span><span class="sxs-lookup"><span data-stu-id="b739a-342">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 
