---
description: Компонент Windows Imaging Component (WIC) предоставляет API на основе модели COM для использования в C и C++.
ms.assetid: 74b14b5e-70e9-410f-a6e6-d8873a5f4fa4
title: Общие сведения об API WIC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f86e5a876010e52489adac9baa7ce57fdfdf80f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105719544"
---
# <a name="wic-api-overview"></a><span data-ttu-id="aec51-103">Общие сведения об API WIC</span><span class="sxs-lookup"><span data-stu-id="aec51-103">WIC API Overview</span></span>

<span data-ttu-id="aec51-104">Компонент Windows Imaging Component (WIC) предоставляет API на основе модели COM для использования в C и C++.</span><span class="sxs-lookup"><span data-stu-id="aec51-104">The Windows Imaging Component (WIC) provides a Component Object Model (COM) based API for use in C and C++.</span></span> <span data-ttu-id="aec51-105">API WIC предоставляет разнообразные функции, связанные с образами, в том числе:</span><span class="sxs-lookup"><span data-stu-id="aec51-105">The WIC API exposes a variety of image-related functionality, including:</span></span>

-   <span data-ttu-id="aec51-106">Встроенные кодеки для стандартных форматов веб-изображений.</span><span class="sxs-lookup"><span data-stu-id="aec51-106">Built-in codecs for the standard web image formats.</span></span>
-   <span data-ttu-id="aec51-107">Встроенная поддержка стандартных форматов метаданных.</span><span class="sxs-lookup"><span data-stu-id="aec51-107">Built-in support for standard metadata formats.</span></span>
-   <span data-ttu-id="aec51-108">Поддержка широкого диапазона поддерживаемых форматов пикселей.</span><span class="sxs-lookup"><span data-stu-id="aec51-108">Wide range of pixel format support.</span></span>
-   <span data-ttu-id="aec51-109">Поддержка высокого цвета; включая 30-разрядный расширенный диапазон, 30-разрядную с высокой точностью и 48-разрядный формат пикселей с высокой точностью и шириной в один цвет.</span><span class="sxs-lookup"><span data-stu-id="aec51-109">High-color support; including 30-bit extended range, 30-bit high precision, and 48-bit high precision and wide gamut pixel formats.</span></span>
-   <span data-ttu-id="aec51-110">Расширяемая платформа для кодеков изображений, форматов пикселей и форматов метаданных.</span><span class="sxs-lookup"><span data-stu-id="aec51-110">Extensible framework for image codecs, pixel formats, and metadata formats.</span></span>

<span data-ttu-id="aec51-111">Этот раздел содержит следующие разделы.</span><span class="sxs-lookup"><span data-stu-id="aec51-111">This topic contains the following topics.</span></span>

-   [<span data-ttu-id="aec51-112">Файлы заголовков WIC</span><span class="sxs-lookup"><span data-stu-id="aec51-112">WIC Header Files</span></span>](#wic-header-files)
-   [<span data-ttu-id="aec51-113">Файлы библиотек</span><span class="sxs-lookup"><span data-stu-id="aec51-113">Library Files</span></span>](#library-files)
-   [<span data-ttu-id="aec51-114">Фабрики классов</span><span class="sxs-lookup"><span data-stu-id="aec51-114">Class Factories</span></span>](#class-factories)
-   [<span data-ttu-id="aec51-115">Компоненты работы с образами</span><span class="sxs-lookup"><span data-stu-id="aec51-115">Imaging Components</span></span>](#imaging-components)
-   [<span data-ttu-id="aec51-116">См. также:</span><span class="sxs-lookup"><span data-stu-id="aec51-116">See Also</span></span>](#see-also)

## <a name="wic-header-files"></a><span data-ttu-id="aec51-117">Файлы заголовков WIC</span><span class="sxs-lookup"><span data-stu-id="aec51-117">WIC Header Files</span></span>

<span data-ttu-id="aec51-118">API-интерфейсы WIC определяются в следующих файлах в заголовке и на языке IDL:</span><span class="sxs-lookup"><span data-stu-id="aec51-118">The WIC APIs are defined in the following header and Interface Definition Language (IDL) files:</span></span>



| <span data-ttu-id="aec51-119">Файл</span><span class="sxs-lookup"><span data-stu-id="aec51-119">File</span></span>              | <span data-ttu-id="aec51-120">Описание</span><span class="sxs-lookup"><span data-stu-id="aec51-120">Description</span></span>                                          |
|-------------------|------------------------------------------------------|
| <span data-ttu-id="aec51-121">винкодек. h</span><span class="sxs-lookup"><span data-stu-id="aec51-121">wincodec.h</span></span>        | <span data-ttu-id="aec51-122">Определяет версии основных API-интерфейсов WIC для C и C++.</span><span class="sxs-lookup"><span data-stu-id="aec51-122">Defines C and C++ versions of the primary WIC APIs.</span></span>  |
| <span data-ttu-id="aec51-123">винкодек. idl</span><span class="sxs-lookup"><span data-stu-id="aec51-123">wincodec.idl</span></span>      | <span data-ttu-id="aec51-124">Определяет основные интерфейсы WIC.</span><span class="sxs-lookup"><span data-stu-id="aec51-124">Defines the primary WIC interfaces.</span></span>                  |
| <span data-ttu-id="aec51-125">винкодексдк. h</span><span class="sxs-lookup"><span data-stu-id="aec51-125">wincodecsdk.h</span></span>     | <span data-ttu-id="aec51-126">Определяет версии API WIC метаданных в C и C++.</span><span class="sxs-lookup"><span data-stu-id="aec51-126">Defines C and C++ versions of the metadata WIC APIs.</span></span> |
| <span data-ttu-id="aec51-127">винкодексдк. idl</span><span class="sxs-lookup"><span data-stu-id="aec51-127">wincodecsdk.idl</span></span>   | <span data-ttu-id="aec51-128">Определяет интерфейсы метаданных WIC.</span><span class="sxs-lookup"><span data-stu-id="aec51-128">Defines the WIC metadata interfaces.</span></span>                 |
| <span data-ttu-id="aec51-129">винкодек \_ -прокси. h</span><span class="sxs-lookup"><span data-stu-id="aec51-129">wincodec\_proxy.h</span></span> | <span data-ttu-id="aec51-130">Определяет экспорты прокси-сервера WIC.</span><span class="sxs-lookup"><span data-stu-id="aec51-130">Defines the WIC proxy exports.</span></span>                       |



 

<span data-ttu-id="aec51-131">Чтобы использовать WIC, приложения должны включать винкодек. h и (или) винкодексдк. h в зависимости от того, какой API требуется приложению.</span><span class="sxs-lookup"><span data-stu-id="aec51-131">To use WIC, your applications must include wincodec.h and/or wincodecsdk.h, depending on the API your application needs.</span></span>

## <a name="library-files"></a><span data-ttu-id="aec51-132">Файлы библиотек</span><span class="sxs-lookup"><span data-stu-id="aec51-132">Library Files</span></span>

<span data-ttu-id="aec51-133">Файлы библиотеки WIC:</span><span class="sxs-lookup"><span data-stu-id="aec51-133">The WIC library files:</span></span>



| <span data-ttu-id="aec51-134">Файл</span><span class="sxs-lookup"><span data-stu-id="aec51-134">File</span></span>              | <span data-ttu-id="aec51-135">Описание</span><span class="sxs-lookup"><span data-stu-id="aec51-135">Description</span></span>                                                            |
|-------------------|------------------------------------------------------------------------|
| <span data-ttu-id="aec51-136">виндовскодекс. lib</span><span class="sxs-lookup"><span data-stu-id="aec51-136">windowscodecs.lib</span></span> | <span data-ttu-id="aec51-137">Библиотека импорта, предоставляемая пакетом средств разработки программного обеспечения (SDK) для Windows.</span><span class="sxs-lookup"><span data-stu-id="aec51-137">Import library provided by the Windows Software Development Kit (SDK).</span></span> |
| <span data-ttu-id="aec51-138">windowscodecs.dll</span><span class="sxs-lookup"><span data-stu-id="aec51-138">windowscodecs.dll</span></span> | <span data-ttu-id="aec51-139">Библиотека реализации акции, предоставляемая операционной системой.</span><span class="sxs-lookup"><span data-stu-id="aec51-139">Stock implementation library provided by the operating system.</span></span>         |



 

<span data-ttu-id="aec51-140">Чтобы создать ссылку на API-интерфейсы WIC, приложение должно включать виндовскодек. lib в качестве дополнительной зависимости компоновщика.</span><span class="sxs-lookup"><span data-stu-id="aec51-140">To link to WIC APIs, your application must include windowscodec.lib as an additional linker dependency.</span></span>

## <a name="class-factories"></a><span data-ttu-id="aec51-141">Фабрики классов</span><span class="sxs-lookup"><span data-stu-id="aec51-141">Class Factories</span></span>

<span data-ttu-id="aec51-142">В следующей таблице описаны две фабрики классов COM, которые API-интерфейсы WIC предоставляют для создания компонентов WIC.</span><span class="sxs-lookup"><span data-stu-id="aec51-142">The following table describes the two COM class factories the WIC APIs provide for creating WIC components.</span></span>



| <span data-ttu-id="aec51-143">Фабричный интерфейс</span><span class="sxs-lookup"><span data-stu-id="aec51-143">Factory Interface</span></span>                                               | <span data-ttu-id="aec51-144">Описание</span><span class="sxs-lookup"><span data-stu-id="aec51-144">Description</span></span>                                                                                                                                             |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="aec51-145">**IWICImagingFactory**</span><span class="sxs-lookup"><span data-stu-id="aec51-145">**IWICImagingFactory**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)     | <span data-ttu-id="aec51-146">Основная фабрика классов для разработки приложений с помощью компонентов WIC.</span><span class="sxs-lookup"><span data-stu-id="aec51-146">Primary class factory for application development using WIC components.</span></span> <span data-ttu-id="aec51-147">Эта фабрика создает такие компоненты, как декодеры изображений, кодировщики и потоки.</span><span class="sxs-lookup"><span data-stu-id="aec51-147">This factory creates components such as image decoders, encoders and streams.</span></span>   |
| [<span data-ttu-id="aec51-148">**ивиккомпонентфактори**</span><span class="sxs-lookup"><span data-stu-id="aec51-148">**IWICComponentFactory**</span></span>](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) | <span data-ttu-id="aec51-149">Фабрика класса, предназначенная для разработчиков компонентов WIC.</span><span class="sxs-lookup"><span data-stu-id="aec51-149">Class factory targeted for WIC component developers.</span></span> <span data-ttu-id="aec51-150">Компоненты, созданные из этой фабрики, в основном используются в коде кодеков и обработчика метаданных.</span><span class="sxs-lookup"><span data-stu-id="aec51-150">Components created from this factory are primarily used in codec and metadata handler development.</span></span> |



 

<span data-ttu-id="aec51-151">Чтобы создать любую фабрику класса, используйте функцию [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) com.</span><span class="sxs-lookup"><span data-stu-id="aec51-151">To create either class factory, use the [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) COM function.</span></span> <span data-ttu-id="aec51-152">В следующем примере демонстрируется создание фабрики изображений WIC.</span><span class="sxs-lookup"><span data-stu-id="aec51-152">The following example demonstrates the creation of the WIC imaging factory.</span></span>


```C++
// Initialize COM
CoInitialize(NULL);

// The factory pointer
IWICImagingFactory *pFactory = NULL;

// Create the COM imaging factory
HRESULT hr = CoCreateInstance(
    CLSID_WICImagingFactory,
    NULL,
    CLSCTX_INPROC_SERVER,
    IID_PPV_ARGS(&pFactory)
);
```



## <a name="imaging-components"></a><span data-ttu-id="aec51-153">Компоненты работы с образами</span><span class="sxs-lookup"><span data-stu-id="aec51-153">Imaging Components</span></span>

<span data-ttu-id="aec51-154">API-интерфейсы WIC предоставляют несколько типов компонентов работы с образами.</span><span class="sxs-lookup"><span data-stu-id="aec51-154">The WIC APIs provide several types of imaging components.</span></span> <span data-ttu-id="aec51-155">В следующей таблице описаны некоторые распространенные компоненты WIC.</span><span class="sxs-lookup"><span data-stu-id="aec51-155">The following table describes some of the common WIC components.</span></span> <span data-ttu-id="aec51-156">Полный список доступных компонентов см. в разделе [интерфейсы WIC](-wic-codec-ifaces.md).</span><span class="sxs-lookup"><span data-stu-id="aec51-156">For a full list of available components, see [WIC interfaces](-wic-codec-ifaces.md).</span></span>



| <span data-ttu-id="aec51-157">Тип компонента</span><span class="sxs-lookup"><span data-stu-id="aec51-157">Component Type</span></span>                                                      | <span data-ttu-id="aec51-158">Описание</span><span class="sxs-lookup"><span data-stu-id="aec51-158">Description</span></span>                                                                                                   |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="aec51-159">**Bitmap**</span><span class="sxs-lookup"><span data-stu-id="aec51-159">**Bitmap**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)                             | <span data-ttu-id="aec51-160">Представляет доступное для записи представление [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)в памяти.</span><span class="sxs-lookup"><span data-stu-id="aec51-160">Represents a writable in-memory representation of an [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource).</span></span> |
| [<span data-ttu-id="aec51-161">**Показан**</span><span class="sxs-lookup"><span data-stu-id="aec51-161">**Decoder**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)                     | <span data-ttu-id="aec51-162">Используется для декодирования данных изображения из потока в формат, который удобен для обработки изображений.</span><span class="sxs-lookup"><span data-stu-id="aec51-162">Used to decode image data from a stream into a format that is useful for image processing.</span></span>                    |
| [<span data-ttu-id="aec51-163">**Кодировщик**</span><span class="sxs-lookup"><span data-stu-id="aec51-163">**Encoder**</span></span>](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)                     | <span data-ttu-id="aec51-164">Записывает данные изображения в поток.</span><span class="sxs-lookup"><span data-stu-id="aec51-164">Writes image data to a stream.</span></span>                                                                                |
| [<span data-ttu-id="aec51-165">**Stream**</span><span class="sxs-lookup"><span data-stu-id="aec51-165">**Stream**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream)                             | <span data-ttu-id="aec51-166">Используется для чтения и записи данных из файла, сетевого ресурса, блока памяти и т. д.</span><span class="sxs-lookup"><span data-stu-id="aec51-166">Used to read and write data from a file, network resource, a block of memory, and so on.</span></span>                      |
| [<span data-ttu-id="aec51-167">**Конвертер формата**</span><span class="sxs-lookup"><span data-stu-id="aec51-167">**Format Converter**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)          | <span data-ttu-id="aec51-168">Используется для преобразования из одного формата пикселей в другой.</span><span class="sxs-lookup"><span data-stu-id="aec51-168">Used to convert from one pixel format to another.</span></span>                                                             |
| [<span data-ttu-id="aec51-169">**Средство чтения запросов метаданных**</span><span class="sxs-lookup"><span data-stu-id="aec51-169">**Metadata Query Reader**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) | <span data-ttu-id="aec51-170">Используется для чтения метаданных изображения или кадра изображения.</span><span class="sxs-lookup"><span data-stu-id="aec51-170">Used to read metadata of an image or image frame.</span></span>                                                             |
| [<span data-ttu-id="aec51-171">**Модуль записи запросов метаданных**</span><span class="sxs-lookup"><span data-stu-id="aec51-171">**Metadata Query Writer**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) | <span data-ttu-id="aec51-172">Используется для записи метаданных в изображение или кадр изображения.</span><span class="sxs-lookup"><span data-stu-id="aec51-172">Used to write metadata to an image or image frame.</span></span>                                                            |



 

## <a name="see-also"></a><span data-ttu-id="aec51-173">См. также:</span><span class="sxs-lookup"><span data-stu-id="aec51-173">See Also</span></span>

[<span data-ttu-id="aec51-174">Справочные материалы</span><span class="sxs-lookup"><span data-stu-id="aec51-174">References</span></span>](-wic-codec-reference.md)


[<span data-ttu-id="aec51-175">Примеры и примеры кода</span><span class="sxs-lookup"><span data-stu-id="aec51-175">Samples and Code Examples</span></span>](-wic-samples.md)


 

 
