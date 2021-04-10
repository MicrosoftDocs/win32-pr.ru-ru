---
description: В этом разделе рассказывается о новой схеме с расширенной платформой метаданных (XMP) и свойстве Photo. photo. Пеопленамес Windows 7, которая позволяет размечать людей в цифровой фотографии.
ms.assetid: 557c3e9a-1756-4abb-8465-b12195ecbc91
title: Общие сведения о разметке пользователей
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e64f2080e51d4d340474e0610fcce9512fc72429
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156739"
---
# <a name="people-tagging-overview"></a><span data-ttu-id="70d7a-103">Общие сведения о разметке пользователей</span><span class="sxs-lookup"><span data-stu-id="70d7a-103">People Tagging Overview</span></span>

<span data-ttu-id="70d7a-104">В этом разделе рассказывается о новой схеме с расширенной платформой метаданных (XMP) и свойстве Photo [. photo. Пеопленамес](../properties/props-system-photo-peoplenames.md) Windows 7, которая позволяет размечать людей в цифровой фотографии.</span><span class="sxs-lookup"><span data-stu-id="70d7a-104">This topic introduces the new Extensible Metadata Platform (XMP) schema and the Windows 7 photo property [System.Photo.PeopleNames](../properties/props-system-photo-peoplenames.md) that enables the tagging of individuals in a digital photo.</span></span> <span data-ttu-id="70d7a-105">В этом разделе также обсуждается использование API компонента Windows Imaging Component (WIC) для чтения и записи метаданных, необходимых для добавления тегов к пользователям.</span><span class="sxs-lookup"><span data-stu-id="70d7a-105">This topic also discusses how to use the Windows Imaging Component (WIC) API to both read and write the metadata needed for people tagging.</span></span>

<span data-ttu-id="70d7a-106">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="70d7a-106">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="70d7a-107">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="70d7a-107">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="70d7a-108">Введение</span><span class="sxs-lookup"><span data-stu-id="70d7a-108">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="70d7a-109">Теги для людей</span><span class="sxs-lookup"><span data-stu-id="70d7a-109">People Tagging</span></span>](#people-tagging-overview)
    -   [<span data-ttu-id="70d7a-110">Имена людей</span><span class="sxs-lookup"><span data-stu-id="70d7a-110">People Names</span></span>](#people-names)
    -   [<span data-ttu-id="70d7a-111">Прямоугольники людей</span><span class="sxs-lookup"><span data-stu-id="70d7a-111">People Rectangles</span></span>](#people-rectangles)
-   [<span data-ttu-id="70d7a-112">Справочник по схемам</span><span class="sxs-lookup"><span data-stu-id="70d7a-112">Schema Reference</span></span>](#schema-reference)
    -   [<span data-ttu-id="70d7a-113">Схема Microsoft Photo 1,2</span><span class="sxs-lookup"><span data-stu-id="70d7a-113">Microsoft Photo 1.2 Schema</span></span>](#microsoft-photo-12-schema)
    -   [<span data-ttu-id="70d7a-114">Схема Microsoft Photo RegionInfo</span><span class="sxs-lookup"><span data-stu-id="70d7a-114">Microsoft Photo RegionInfo Schema</span></span>](#microsoft-photo-regioninfo-schema)
    -   [<span data-ttu-id="70d7a-115">Схема области фотографии (Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="70d7a-115">Microsoft Photo Region Schema</span></span>](#microsoft-photo-regioninfo-schema)
    -   [<span data-ttu-id="70d7a-116">Образцы метаданных</span><span class="sxs-lookup"><span data-stu-id="70d7a-116">Sample Metadata</span></span>](#sample-metadata)
-   [<span data-ttu-id="70d7a-117">См. также</span><span class="sxs-lookup"><span data-stu-id="70d7a-117">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="70d7a-118">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="70d7a-118">Prerequisites</span></span>

<span data-ttu-id="70d7a-119">Чтобы понять этот раздел, необходимо ознакомиться с интерфейсами декодера WIC и связанными с ним компонентами модели COM, как описано в разделе [Общие сведения о компоненте создания образов Windows](-wic-about-windows-imaging-codec.md).</span><span class="sxs-lookup"><span data-stu-id="70d7a-119">To understand this topic, you should be familiar with the WIC decoder interfaces and its related Component Object Model (COM) components, as described in the [Windows Imaging Component Overview](-wic-about-windows-imaging-codec.md).</span></span> <span data-ttu-id="70d7a-120">Кроме того, он позволяет получить общее представление о метаданных изображений, особенно XMP.</span><span class="sxs-lookup"><span data-stu-id="70d7a-120">It also helps to have a general familiarity with imaging metadata, especially XMP.</span></span>

## <a name="introduction"></a><span data-ttu-id="70d7a-121">Введение</span><span class="sxs-lookup"><span data-stu-id="70d7a-121">Introduction</span></span>

<span data-ttu-id="70d7a-122">Корпорация Майкрософт создала новую схему XMP для тегирования людей в цифровом изображении.</span><span class="sxs-lookup"><span data-stu-id="70d7a-122">Microsoft has created a new XMP schema for tagging people within a digital image.</span></span> <span data-ttu-id="70d7a-123">Эта схема позволяет приложениям хранить имена и расположения пользователей, которые находятся в образе, в виде метаданных в образе.</span><span class="sxs-lookup"><span data-stu-id="70d7a-123">This schema enables applications to store the names and locations of individuals who are in the image as metadata within the image.</span></span> <span data-ttu-id="70d7a-124">В дополнение к новой схеме в Windows 7 доступно новое свойство Photo [System. photo. пеопленамес](../properties/props-system-photo-peoplenames.md) .</span><span class="sxs-lookup"><span data-stu-id="70d7a-124">In addition to the new schema, the new photo property [System.Photo.PeopleNames](../properties/props-system-photo-peoplenames.md) is available in Windows 7.</span></span> <span data-ttu-id="70d7a-125">Это новое свойство позволяет приложениям считывать имена отдельных пользователей, хранящиеся в метаданных образа.</span><span class="sxs-lookup"><span data-stu-id="70d7a-125">This new property enables applications to read the individual's names stored in the image metadata.</span></span> <span data-ttu-id="70d7a-126">WIC использует эти новые функции, позволяя приложениям легко считывать и записывать в цифровые фотографии метаданные тегов.</span><span class="sxs-lookup"><span data-stu-id="70d7a-126">WIC utilizes these new features by enabling applications to easily read and write people tagging metadata to digital photos.</span></span>

## <a name="people-tagging"></a><span data-ttu-id="70d7a-127">Теги для людей</span><span class="sxs-lookup"><span data-stu-id="70d7a-127">People Tagging</span></span>

<span data-ttu-id="70d7a-128">Компонент WIC предоставляет разработчикам приложений COM-компоненты, считывающие данные изображений, а также метаданные изображений.</span><span class="sxs-lookup"><span data-stu-id="70d7a-128">WIC provides application developers with COM components which read image data as well as image metadata.</span></span> <span data-ttu-id="70d7a-129">Для чтения и записи метаданных, таких как новая функция тегирования людей, компонент WIC предоставляет интерфейсы [**ивикметадатакуериреадер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) и [**ивикметадатакуеривритер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) .</span><span class="sxs-lookup"><span data-stu-id="70d7a-129">For reading and writing metadata, such as the new people tagging feature, WIC provides the [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) and [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) interfaces.</span></span> <span data-ttu-id="70d7a-130">Эти интерфейсы позволяют приложениям использовать [язык запросов метаданных](-wic-codec-metadataquerylanguage.md) для записи метаданных в отдельные кадры изображения.</span><span class="sxs-lookup"><span data-stu-id="70d7a-130">These interfaces enable applications to use the [metadata query language](-wic-codec-metadataquerylanguage.md) to write metadata to the individual frames of an image.</span></span> <span data-ttu-id="70d7a-131">В следующем разделе показано, как считывать и записывать метаданные тегов людей в метаданные изображения с помощью средств чтения и записи запросов WIC.</span><span class="sxs-lookup"><span data-stu-id="70d7a-131">The following section demonstrates how to read and write the people-tagging metadata into an image's metadata by using WIC query readers and writers.</span></span>

### <a name="people-names"></a><span data-ttu-id="70d7a-132">Имена людей</span><span class="sxs-lookup"><span data-stu-id="70d7a-132">People Names</span></span>

<span data-ttu-id="70d7a-133">Часть функции тегирования людей — это возможность просто получить список имен людей, помеченных в изображении.</span><span class="sxs-lookup"><span data-stu-id="70d7a-133">Part of the people-tagging feature is the ability to simply get a list the names of the people tagged within the image.</span></span> <span data-ttu-id="70d7a-134">Эта часть функции поддерживается обработчиками метаданных [System. photo. пеопленамес](../properties/props-system-photo-peoplenames.md) и WIC.</span><span class="sxs-lookup"><span data-stu-id="70d7a-134">This part of the feature is supported by the [System.Photo.PeopleNames](../properties/props-system-photo-peoplenames.md) and WIC's metadata handlers.</span></span> <span data-ttu-id="70d7a-135">Интерфейс [**ивикметадатакуериреадер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) в сочетании со свойством System. photo. пеопленамес используется для чтения имен людей, определенных в образе и хранимых в метаданных образа.</span><span class="sxs-lookup"><span data-stu-id="70d7a-135">The [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) interface, in conjunction with the System.Photo.PeopleNames property, are used to read the names of people identified in an image and stored in the image metadata.</span></span>

<span data-ttu-id="70d7a-136">В следующем примере кода показано, как средство чтения запросов, полученное из кадра изображения, запрашивает метаданные изображения для именованных тегов свойства [System. photo. пеопленамес](../properties/props-system-photo-peoplenames.md) .</span><span class="sxs-lookup"><span data-stu-id="70d7a-136">The following code example demonstrates a query reader obtained from an image frame to query an image's metadata for tagged names of the [System.Photo.PeopleNames](../properties/props-system-photo-peoplenames.md) property.</span></span>


```C++
// Not shown: image decoding, retrieving an image frame. 
...
PROPVARIANT value;
IWICMetadataQueryReader *pQueryReader = NULL;
...
// Get the query reader.
if (SUCCEEDED(hr))
{
    hr = pFrameDecode->GetMetadataQueryReader(&pQueryReader);
}

// Query for the System.Photo.PeopleNames property.
if (SUCCEEDED(hr))
{
    // Get the property metadata by property name.
    hr = pQueryReader->GetMetadataByName(L"System.Photo.PeopleNames", &value);
}
```



<span data-ttu-id="70d7a-137">Выражение запроса System. photo. Пеопленамес запрашивает кадр для свойства.</span><span class="sxs-lookup"><span data-stu-id="70d7a-137">The query expression "System.Photo.PeopleNames" queries the frame for the property.</span></span> <span data-ttu-id="70d7a-138">Если метаданные тегов людей существуют и содержат имена людей, значение [пропвариант](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) будет установлено VT \_ LPWSTR, а значение данных будет содержать список имен с тегами.</span><span class="sxs-lookup"><span data-stu-id="70d7a-138">If the people-tagging metadata exists and contains people's names, the [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) value will be set to VT\_LPWSTR and the data value will contain the list of tagged names.</span></span> <span data-ttu-id="70d7a-139">Дополнительные сведения о чтении метаданных изображения см. в разделе [Общие сведения о чтении и записи метаданных изображения](-wic-codec-readingwritingmetadata.md).</span><span class="sxs-lookup"><span data-stu-id="70d7a-139">For more information on reading image metadata, see [Overview of Reading and Writing Image Metadata](-wic-codec-readingwritingmetadata.md).</span></span>

<span data-ttu-id="70d7a-140">Запрос к тегу "имена людей" полезен только в том случае, если изображение фактически содержит метаданные тегов для людей.</span><span class="sxs-lookup"><span data-stu-id="70d7a-140">Querying for the people names tag is only useful if the image actually contains the people-tagging metadata.</span></span> <span data-ttu-id="70d7a-141">Чтобы это произошло, приложение должно сначала записать его.</span><span class="sxs-lookup"><span data-stu-id="70d7a-141">For this to occur, an application must first have written it.</span></span> <span data-ttu-id="70d7a-142">Чтобы записать метаданные имен людей, используйте [**ивикметадатакуеривритер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) и ЯВНЫЙ путь XMP к метаданным.</span><span class="sxs-lookup"><span data-stu-id="70d7a-142">To write the people names metadata, use an [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) and the explicit XMP path of the metadata.</span></span> <span data-ttu-id="70d7a-143">В следующем примере кода показано использование средства записи запроса для записи имени в путь запроса.</span><span class="sxs-lookup"><span data-stu-id="70d7a-143">The following code example demonstrates using a query writer to write a name to the query path.</span></span>


```C++
// Not shown: image encoding, retrieving/creating the image frame,
// creating the IWICImagingFactory 
...
IWICImagingFactory *pFactory = NULL;
IWICMetadataQueryWriter *pQueryWriter = NULL;
...
// Get the query writer from the image frame.
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->GetMetadataQueryWriter(&pQueryWriter);
}

// A query writer specifically for this person's XMP struct
IWICMetadataQueryWriter *pXMPStructQueryWriter = NULL;

// Create a query writer specifically for an XMP Struct
hr = pFactory->CreateQueryWriter(
    GUID_MetadataFormatXMPStruct,
    NULL,
    &pXMPStructQueryWriter
    );

// Create a variant representing the structure created above
PROPVARIANT xmpStruct;
PropVariantInit(&xmpStruct);

// VT_UNKNOWN indicates that we're setting a COM object, in this case a XMPStruct
// which will hold the name and rectangle
xmpStruct.vt = VT_UNKNOWN; 
xmpStruct.punkVal = pXMPStructQueryWriter;

if(SUCCEEDED(hr))
{
    // WIC will automatically create the xmp base, the RegionInfo struct, and the Regions
    // bag (an unordered array) but structs within that bag need to be explicitly created.
    // The {ulong=0} in the query means to insert the new struct at the start of the bag,
    // {} could also be used to insert at the end of the bag.
    hr = pQueryWriter->SetMetadataByName(
        L"/xmp/<xmpstruct>MP:RegionInfo/<xmpbag>MPRI:Regions/{ulong=0}",
        &xmpStruct
        );
}

// Set up the PROPVARIANT with the name information
PROPVARIANT personName;
PropVariantInit(&personName);
personName.vt = VT_LPWSTR;
personName.pwszVal = L"John Doe";

if(SUCCEEDED(hr))
{
    // Set the name metadata
    hr = pQueryWriter->SetMetadataByName(
        L"/xmp/MP:RegionInfo/MPRI:Regions/{ulong=0}/MPReg:PersonDisplayName",
        &personName
        );  
}
```



<span data-ttu-id="70d7a-144">Обратите внимание на шаг, создающий структуру XMP и задавая ее в разделе `MPRI:Regions/{ulong=0}` .</span><span class="sxs-lookup"><span data-stu-id="70d7a-144">Note the step constructing the XMP structure and setting it under `MPRI:Regions/{ulong=0}`.</span></span> <span data-ttu-id="70d7a-145">Без этого шага компонент WIC не сможет выяснить, где разместить `PersonDisplayName` позже.</span><span class="sxs-lookup"><span data-stu-id="70d7a-145">Without this step, the WIC can't identify where to place the `PersonDisplayName` later on.</span></span> <span data-ttu-id="70d7a-146">Также обратите внимание, что вместо [System. photo. пеопленамес](-wic-photoprop-system-photo-peoplenames.md)используется явный путь запроса, политика метаданных которой не поддерживает запись метаданных.</span><span class="sxs-lookup"><span data-stu-id="70d7a-146">Also note that the explicit query path is used instead of [System.Photo.PeopleNames](-wic-photoprop-system-photo-peoplenames.md), whose metadata policy does not support writing metadata.</span></span>

### <a name="people-rectangles"></a><span data-ttu-id="70d7a-147">Прямоугольники людей</span><span class="sxs-lookup"><span data-stu-id="70d7a-147">People Rectangles</span></span>

<span data-ttu-id="70d7a-148">Однако имена людей являются только частью функции добавления тегов.</span><span class="sxs-lookup"><span data-stu-id="70d7a-148">People's names however, are only part of the people-tagging feature.</span></span> <span data-ttu-id="70d7a-149">В дополнение к хранению имен людей в метаданных схема также поддерживает сведения о регионах, определяющие конкретную область (прямоугольник), которую пользователь показывает в изображении.</span><span class="sxs-lookup"><span data-stu-id="70d7a-149">In addition to storing people's names in the metadata, the schema also supports region information that identifies the specific area (a rectangle) the person is shown in the image.</span></span>

<span data-ttu-id="70d7a-150">Сведения о прямоугольнике представлены четырьмя десятичными значениями, разделенными запятой, например "0,25, 0,25, 0,25, 0,25".</span><span class="sxs-lookup"><span data-stu-id="70d7a-150">The rectangle information is represented by four comma-delimited decimal values, such as "0.25, 0.25, 0.25, 0.25".</span></span> <span data-ttu-id="70d7a-151">Первые два значения указывают координату верхнего левого угла; последние два указывают высоту и ширину прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="70d7a-151">The first two values specify the top-left coordinate; the final two specify the height and width of the rectangle.</span></span> <span data-ttu-id="70d7a-152">Размеры изображения в целях определения прямоугольников людей нормализованы до 1, что означает, что в примере "0,25, 0,25, 0,25, 0,25" прямоугольник начинается с 1/4 расстояния от верхнего края и от 1/4 на расстоянии от левого края изображения.</span><span class="sxs-lookup"><span data-stu-id="70d7a-152">The dimensions of the image for the purposes of defining people rectangles are normalized to 1, which means that in the "0.25, 0.25, 0.25, 0.25" example, the rectangle starts 1/4 of the distance from the top and 1/4 of the distance from the left of the image.</span></span> <span data-ttu-id="70d7a-153">Высота и ширина прямоугольника равна 1/4 размера соответствующих размеров изображения.</span><span class="sxs-lookup"><span data-stu-id="70d7a-153">Both the height and width of the rectangle are 1/4 of the size of their respective image dimensions.</span></span>

<span data-ttu-id="70d7a-154">Сведения о прямоугольнике, определяющие отдельных лиц, записываются так же, как и имена пользователей в одной и той же структуре.</span><span class="sxs-lookup"><span data-stu-id="70d7a-154">The rectangle information that identifies individuals is written in the same way people's names are written, within the same structure.</span></span> <span data-ttu-id="70d7a-155">Чтобы записать метаданные прямоугольника, используйте [**ивикметадатакуеривритер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) и ЯВНЫЙ путь XMP к метаданным.</span><span class="sxs-lookup"><span data-stu-id="70d7a-155">To write the rectangle metadata, use an [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) and the explicit XMP path of the metadata.</span></span> <span data-ttu-id="70d7a-156">Следующий пример кода возобновляет предыдущий пример и добавляет прямоугольник, представляющий "John Петрова", в метаданные изображения.</span><span class="sxs-lookup"><span data-stu-id="70d7a-156">The following code example continues the previous example and adds a rectangle representing 'John Doe' to the image's metadata.</span></span> <span data-ttu-id="70d7a-157">Обратите внимание, что он использует тот же `{ulong=0}` индекс для связывания этого прямоугольника с "Джон Петров".</span><span class="sxs-lookup"><span data-stu-id="70d7a-157">Note that it uses the same `{ulong=0}` index to associate this rectangle with 'John Doe'.</span></span>


```C++
// Set up the PROPVARIANT with the rectangle information
PROPVARIANT rectangle;
PropVariantInit(&rectangle);
rectangle.vt = VT_LPWSTR;
rectangle.pwszVal = L"0.0,0.0,0.25,0.25";

if(SUCCEEDED(hr))
{
    // Set the rectangle metadata
    hr = pQueryWriter->SetMetadataByName(
        L"/xmp/MP:RegionInfo/MPRI:Regions/{ulong=0}/MPReg:Rectangle",
        &rectangle
        );
}
```



## <a name="schema-reference"></a><span data-ttu-id="70d7a-158">Справочник по схеме</span><span class="sxs-lookup"><span data-stu-id="70d7a-158">Schema Reference</span></span>

<span data-ttu-id="70d7a-159">Схемы Microsoft XMP для тегирования пользователей определяют набор свойств для обозначения лиц в цифровых фотографиях.</span><span class="sxs-lookup"><span data-stu-id="70d7a-159">The Microsoft XMP schemas for people tagging define a set of properties to tag individuals in digital photos.</span></span>

<span data-ttu-id="70d7a-160">В следующих разделах приводятся определения схемы, необходимые для добавления тегов к пользователям.</span><span class="sxs-lookup"><span data-stu-id="70d7a-160">The following sections provide the schema definitions needed for people tagging.</span></span> <span data-ttu-id="70d7a-161">Там, где это возможно, определения схемы используют соглашения, предоставляемые [спецификациями расширяемой платформы метаданных (XMP) Adobe](https://www.adobe.com/devnet/xmp/).</span><span class="sxs-lookup"><span data-stu-id="70d7a-161">Wherever possible, the schema definitions use the conventions provided by [Adobe's Extensible Metadata Platform (XMP) Specifications](https://www.adobe.com/devnet/xmp/).</span></span> <span data-ttu-id="70d7a-162">Определения схемы в этом разделе показывают универсальный код ресурса (URI) пространства имен XML, который идентифицирует схему и префикс пространства имен предпочтительной схемы, за которым следует таблица со списком всех свойств, определенных для схемы.</span><span class="sxs-lookup"><span data-stu-id="70d7a-162">The schema definitions in this topic show the XML namespace Uniform Resource Identifier (URI) that identifies the schema and the preferred schema namespace prefix, followed by a table that lists all properties defined for the schema.</span></span> <span data-ttu-id="70d7a-163">Каждая таблица содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="70d7a-163">Each table has the following columns:</span></span>

-   <span data-ttu-id="70d7a-164">**Property** — имя свойства, включая предпочтительный префикс пространства имен.</span><span class="sxs-lookup"><span data-stu-id="70d7a-164">**Property** - The name of the property, including the preferred namespace prefix.</span></span>

-   <span data-ttu-id="70d7a-165">**Тип значения** — тип значения свойства.</span><span class="sxs-lookup"><span data-stu-id="70d7a-165">**Value type** - The value type of the property.</span></span> <span data-ttu-id="70d7a-166">Схемы поддержки тегов людей используют типы значений XMP везде, где это возможно, включая дату и текст.</span><span class="sxs-lookup"><span data-stu-id="70d7a-166">The people-tagging support schemas use the XMP value types whenever possible, including Date and Text.</span></span> <span data-ttu-id="70d7a-167">Перед типами массивов следует тип контейнера: `alt` , `bag` или `seq` .</span><span class="sxs-lookup"><span data-stu-id="70d7a-167">Array types are preceded by the container type: `alt`, `bag`, or `seq`.</span></span>

-   <span data-ttu-id="70d7a-168">**Категория** — свойства схемы являются внутренними или внешними:</span><span class="sxs-lookup"><span data-stu-id="70d7a-168">**Category** - Schema properties are internal or external:</span></span>

    -   <span data-ttu-id="70d7a-169">Внутренние метаданные должны быть заданы приложением.</span><span class="sxs-lookup"><span data-stu-id="70d7a-169">Internal metadata must be set by the application.</span></span>

    -   <span data-ttu-id="70d7a-170">Внешние метаданные должны быть заданы пользователем и не зависеть от содержимого документа.</span><span class="sxs-lookup"><span data-stu-id="70d7a-170">External metadata must be set by the user and is independent of the contents of the document.</span></span>

-   <span data-ttu-id="70d7a-171">**Описание** — описание свойства.</span><span class="sxs-lookup"><span data-stu-id="70d7a-171">**Description** - The description of the property.</span></span>

### <a name="microsoft-photo-12-schema"></a><span data-ttu-id="70d7a-172">Схема Microsoft Photo 1,2</span><span class="sxs-lookup"><span data-stu-id="70d7a-172">Microsoft Photo 1.2 Schema</span></span>

<span data-ttu-id="70d7a-173">Схема Microsoft Photo 1,2 предоставляет набор свойств для областей изображения.</span><span class="sxs-lookup"><span data-stu-id="70d7a-173">The Microsoft Photo 1.2 schema provides a set of properties for image regions.</span></span>

-   <span data-ttu-id="70d7a-174">URI-код пространства имен схемы — `https://ns.microsoft.com/photo/1.2/` .</span><span class="sxs-lookup"><span data-stu-id="70d7a-174">The schema namespace URI is `https://ns.microsoft.com/photo/1.2/`.</span></span>
-   <span data-ttu-id="70d7a-175">Предпочтительным префиксом пространства имен схемы является `MP` .</span><span class="sxs-lookup"><span data-stu-id="70d7a-175">The preferred schema namespace prefix is `MP`.</span></span>



| <span data-ttu-id="70d7a-176">Свойство</span><span class="sxs-lookup"><span data-stu-id="70d7a-176">Property</span></span>      | <span data-ttu-id="70d7a-177">Тип значения</span><span class="sxs-lookup"><span data-stu-id="70d7a-177">Value type</span></span> | <span data-ttu-id="70d7a-178">Категория</span><span class="sxs-lookup"><span data-stu-id="70d7a-178">Category</span></span> | <span data-ttu-id="70d7a-179">Описание</span><span class="sxs-lookup"><span data-stu-id="70d7a-179">Description</span></span>                                                                                                                     |
|---------------|------------|----------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70d7a-180">Пакет управления: RegionInfo</span><span class="sxs-lookup"><span data-stu-id="70d7a-180">MP:RegionInfo</span></span> | <span data-ttu-id="70d7a-181">RegionInfo</span><span class="sxs-lookup"><span data-stu-id="70d7a-181">RegionInfo</span></span> | <span data-ttu-id="70d7a-182">Внутренние</span><span class="sxs-lookup"><span data-stu-id="70d7a-182">Internal</span></span> | <span data-ttu-id="70d7a-183">**обязательный** : сохраняет корень метаданных тегов людей.</span><span class="sxs-lookup"><span data-stu-id="70d7a-183">**required** : Stores the root of the people-tagging metadata.</span></span> <span data-ttu-id="70d7a-184">См. раздел Схема фотоколлажа Майкрософт, который приведен ниже.</span><span class="sxs-lookup"><span data-stu-id="70d7a-184">See the Microsoft Photo RegionInfo Schema section which follows.</span></span> |



 

### <a name="microsoft-photo-regioninfo-schema"></a><span data-ttu-id="70d7a-185">Схема Microsoft Photo RegionInfo</span><span class="sxs-lookup"><span data-stu-id="70d7a-185">Microsoft Photo RegionInfo Schema</span></span>

<span data-ttu-id="70d7a-186">Схема Microsoft Photo RegionInfo 1,2 содержит набор свойств для сведений о регионе.</span><span class="sxs-lookup"><span data-stu-id="70d7a-186">The Microsoft Photo RegionInfo 1.2 schema provides a set of properties for region info.</span></span>

-   <span data-ttu-id="70d7a-187">URI-код пространства имен схемы — `https://ns.microsoft.com/photo/1.2/t/RegionInfo#` .</span><span class="sxs-lookup"><span data-stu-id="70d7a-187">The schema namespace URI is `https://ns.microsoft.com/photo/1.2/t/RegionInfo#`.</span></span>
-   <span data-ttu-id="70d7a-188">Предпочтительным префиксом пространства имен схемы является `MPRI` .</span><span class="sxs-lookup"><span data-stu-id="70d7a-188">The preferred schema namespace prefix is `MPRI`.</span></span>



| <span data-ttu-id="70d7a-189">Свойство</span><span class="sxs-lookup"><span data-stu-id="70d7a-189">Property</span></span>              | <span data-ttu-id="70d7a-190">Тип значения</span><span class="sxs-lookup"><span data-stu-id="70d7a-190">Value type</span></span> | <span data-ttu-id="70d7a-191">Категория</span><span class="sxs-lookup"><span data-stu-id="70d7a-191">Category</span></span> | <span data-ttu-id="70d7a-192">Описание</span><span class="sxs-lookup"><span data-stu-id="70d7a-192">Description</span></span>                                                                                                    |
|-----------------------|------------|----------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70d7a-193">МПРИ: Датерегионсвалид</span><span class="sxs-lookup"><span data-stu-id="70d7a-193">MPRI:DateRegionsValid</span></span> | <span data-ttu-id="70d7a-194">Дата</span><span class="sxs-lookup"><span data-stu-id="70d7a-194">Date</span></span>       | <span data-ttu-id="70d7a-195">External</span><span class="sxs-lookup"><span data-stu-id="70d7a-195">External</span></span> | <span data-ttu-id="70d7a-196">**необязательно** : Дата создания последней области.</span><span class="sxs-lookup"><span data-stu-id="70d7a-196">**optional** : Date that the last region was created.</span></span>                                                          |
| <span data-ttu-id="70d7a-197">МПРИ: регионы</span><span class="sxs-lookup"><span data-stu-id="70d7a-197">MPRI:Regions</span></span>          | <span data-ttu-id="70d7a-198">Регион сумки</span><span class="sxs-lookup"><span data-stu-id="70d7a-198">bag Region</span></span> | <span data-ttu-id="70d7a-199">External</span><span class="sxs-lookup"><span data-stu-id="70d7a-199">External</span></span> | <span data-ttu-id="70d7a-200">**Обязательное** : сохраняет области тегов пользователей.</span><span class="sxs-lookup"><span data-stu-id="70d7a-200">**required** : Stores the people tagging regions.</span></span> <span data-ttu-id="70d7a-201">См. раздел Схема области фотографии Майкрософт, который приведен ниже.</span><span class="sxs-lookup"><span data-stu-id="70d7a-201">See the Microsoft Photo Region Schema section which follows.</span></span> |



 

### <a name="microsoft-photo-region-schema"></a><span data-ttu-id="70d7a-202">Схема области фотографии (Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="70d7a-202">Microsoft Photo Region Schema</span></span>

<span data-ttu-id="70d7a-203">Схема Microsoft Photo Region 1,2 содержит набор свойств для областей изображения.</span><span class="sxs-lookup"><span data-stu-id="70d7a-203">The Microsoft Photo Region 1.2 schema provides a set of properties for image regions.</span></span>

-   <span data-ttu-id="70d7a-204">URI-код пространства имен схемы — `https://ns.microsoft.com/photo/1.2/t/Region#` .</span><span class="sxs-lookup"><span data-stu-id="70d7a-204">The schema namespace URI is `https://ns.microsoft.com/photo/1.2/t/Region#`.</span></span>
-   <span data-ttu-id="70d7a-205">Предпочтительным префиксом пространства имен схемы является `MPReg` .</span><span class="sxs-lookup"><span data-stu-id="70d7a-205">The preferred schema namespace prefix is `MPReg`.</span></span>



| <span data-ttu-id="70d7a-206">Мпрег: свойство</span><span class="sxs-lookup"><span data-stu-id="70d7a-206">MPReg:Property</span></span>          | <span data-ttu-id="70d7a-207">Тип значения</span><span class="sxs-lookup"><span data-stu-id="70d7a-207">Value type</span></span> | <span data-ttu-id="70d7a-208">Категория</span><span class="sxs-lookup"><span data-stu-id="70d7a-208">Category</span></span> | <span data-ttu-id="70d7a-209">Описание</span><span class="sxs-lookup"><span data-stu-id="70d7a-209">Description</span></span>                                                                                                                                                                                                                                                                                                     |
|-------------------------|------------|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70d7a-210">Мпрег: Персондисплайнаме</span><span class="sxs-lookup"><span data-stu-id="70d7a-210">MPReg:PersonDisplayName</span></span> | <span data-ttu-id="70d7a-211">Текст</span><span class="sxs-lookup"><span data-stu-id="70d7a-211">Text</span></span>       | <span data-ttu-id="70d7a-212">External</span><span class="sxs-lookup"><span data-stu-id="70d7a-212">External</span></span> | <span data-ttu-id="70d7a-213">**обязательный** : хранит имя пользователя в заданном прямоугольнике.</span><span class="sxs-lookup"><span data-stu-id="70d7a-213">**required** : Stores the name of the person in the given rectangle.</span></span>                                                                                                                                                                                                                                            |
| <span data-ttu-id="70d7a-214">Мпрег: прямоугольник</span><span class="sxs-lookup"><span data-stu-id="70d7a-214">MPReg:Rectangle</span></span>         | <span data-ttu-id="70d7a-215">Текст</span><span class="sxs-lookup"><span data-stu-id="70d7a-215">Text</span></span>       | <span data-ttu-id="70d7a-216">External</span><span class="sxs-lookup"><span data-stu-id="70d7a-216">External</span></span> | <span data-ttu-id="70d7a-217">( **необязательно** .) содержит прямоугольник, идентифицирующий пользователя в фотографии.</span><span class="sxs-lookup"><span data-stu-id="70d7a-217">**optional** : Stores the rectangle that identifies the person within the photo.</span></span> <span data-ttu-id="70d7a-218">Прямоугольник хранится в виде четырех десятичных значений с разделителями-запятыми.</span><span class="sxs-lookup"><span data-stu-id="70d7a-218">The rectangle is stored as four comma-delimited decimal values.</span></span> <span data-ttu-id="70d7a-219">Первые два значения указывают верхнюю левую координату. последние два указывают высоту и ширину прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="70d7a-219">The first two values specify the top left coordinate; the final two specify the height and width of the rectangle.</span></span> <span data-ttu-id="70d7a-220">Десятичные значения должны быть нормализованы до 1.</span><span class="sxs-lookup"><span data-stu-id="70d7a-220">The decimal values must be normalized to 1.</span></span> |
| <span data-ttu-id="70d7a-221">Мпрег: Персонемаилдижест</span><span class="sxs-lookup"><span data-stu-id="70d7a-221">MPReg:PersonEmailDigest</span></span> | <span data-ttu-id="70d7a-222">Текст</span><span class="sxs-lookup"><span data-stu-id="70d7a-222">Text</span></span>       | <span data-ttu-id="70d7a-223">External</span><span class="sxs-lookup"><span data-stu-id="70d7a-223">External</span></span> | <span data-ttu-id="70d7a-224">( **необязательно** .) хранит хэш зашифрованного сообщения SHA-1 для адреса электронной почты пользователя.</span><span class="sxs-lookup"><span data-stu-id="70d7a-224">**optional** : Stores the SHA-1 encrypted message hash of the person's Live e-mail address.</span></span>                                                                                                                                                                                                                     |
| <span data-ttu-id="70d7a-225">Мпрег: ПерсонливеидЦид</span><span class="sxs-lookup"><span data-stu-id="70d7a-225">MPReg:PersonLiveIdCID</span></span>   | <span data-ttu-id="70d7a-226">Текст</span><span class="sxs-lookup"><span data-stu-id="70d7a-226">Text</span></span>       | <span data-ttu-id="70d7a-227">External</span><span class="sxs-lookup"><span data-stu-id="70d7a-227">External</span></span> | <span data-ttu-id="70d7a-228">**необязательно** : сохраняет десятичное представление целого числа со знаком для действительной CID, 64-разрядное целое число, которое общедоступно определяет действующее удостоверение.</span><span class="sxs-lookup"><span data-stu-id="70d7a-228">**optional** :Stores the signed decimal representation of the person's Live CID, a 64-bit integer that publicly identifies a Live identity.</span></span>                                                                                                                                                                     |



 

### <a name="sample-metadata"></a><span data-ttu-id="70d7a-229">Образцы метаданных</span><span class="sxs-lookup"><span data-stu-id="70d7a-229">Sample Metadata</span></span>

<span data-ttu-id="70d7a-230">Ниже приведено представление метаданных XMP для тегов пользователей.</span><span class="sxs-lookup"><span data-stu-id="70d7a-230">The following is a representation of the XMP metadata for people tagging.</span></span>

``` syntax
<rdf:Description rdf:about="" xmlns:MP="https://ns.microsoft.com/photo/1.2/">
<MP:RegionInfo> 
<rdf:Description xmlns:MPRI="https://ns.microsoft.com/photo/1.2/t/RegionInfo#">
   <MPRI:Regions> 
       <rdf:Bag> 
          <rdf:li> 
       <rdf:Description xmlns:MPReg="https://ns.microsoft.com/photo/1.2/t/Region#"> 
           <MPReg:Rectangle>0.790650, 0.441734, 0.209350, 0.279133
           </MPReg:Rectangle>
           <MPReg:PersonDisplayName>John Doe</MPReg:PersonDisplayName> 
           <MPReg:PersonEmailDigest>2FD4E1C67A2D28FCED849EE1BB76E7391B93EB13</MPReg:PersonEmailDigest> 
           <MPReg:PersonLiveIdCID>1234567890123456789</MPReg:PersonLiveIdCID> 
       </rdf:Description> 
         </rdf:li> 
         <rdf:li>
             <rdf:Description xmlns:MPReg="https://ns.microsoft.com/photo/1.2/t/Region#">
                  <MPReg:Rectangle>0.222656, 0.302083, 0.378906, 0.505208</MPReg:Rectangle> 
                  <MPReg:PersonDisplayName>Jane Doe</MPReg:PersonDisplayName> 
              </rdf:Description> 
         </rdf:li> 
<!-- Addition Regions --> ... 
<rdf:li>...
</rdf:li> 
</rdf:Bag> 
</MPRI:Regions> </rdf:Description> </MP:RegionInfo> </rdf:Description>
```

## <a name="related-topics"></a><span data-ttu-id="70d7a-231">См. также</span><span class="sxs-lookup"><span data-stu-id="70d7a-231">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="70d7a-232">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="70d7a-232">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="70d7a-233">Общие сведения о компоненте создания образов Windows</span><span class="sxs-lookup"><span data-stu-id="70d7a-233">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="70d7a-234">Общие сведения о метаданных компонента WIC</span><span class="sxs-lookup"><span data-stu-id="70d7a-234">WIC Metadata Overview</span></span>](-wic-about-metadata.md)
</dt> <dt>

[<span data-ttu-id="70d7a-235">Общие сведения о чтении и записи метаданных изображений</span><span class="sxs-lookup"><span data-stu-id="70d7a-235">Overview of Reading and Writing Image Metadata</span></span>](-wic-codec-readingwritingmetadata.md)
</dt> <dt>

[<span data-ttu-id="70d7a-236">Общие сведения о языке запросов метаданных</span><span class="sxs-lookup"><span data-stu-id="70d7a-236">Metadata Query Language Overview</span></span>](-wic-codec-metadataquerylanguage.md)
</dt> </dl>

 

 
