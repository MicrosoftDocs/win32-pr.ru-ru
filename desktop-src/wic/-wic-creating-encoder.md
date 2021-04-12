---
description: Кодировщик записывает данные изображения в поток. Кодировщики могут сжимать, шифровать и изменять пиксели изображения несколькими способами перед их записью в поток.
ms.assetid: e1e3a9d9-209b-46a6-92da-5570476507cf
title: Общие сведения о кодировке
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3be46aa73082071deb69fdd402f42866b18ef0aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272302"
---
# <a name="encoding-overview"></a><span data-ttu-id="e2954-104">Общие сведения о кодировке</span><span class="sxs-lookup"><span data-stu-id="e2954-104">Encoding Overview</span></span>

<span data-ttu-id="e2954-105">Кодировщик записывает данные изображения в поток.</span><span class="sxs-lookup"><span data-stu-id="e2954-105">An encoder writes image data to a stream.</span></span> <span data-ttu-id="e2954-106">Кодировщики могут сжимать, шифровать и изменять пиксели изображения несколькими способами перед их записью в поток.</span><span class="sxs-lookup"><span data-stu-id="e2954-106">Encoders can compress, encrypt, and alter the image pixels in a number of ways prior to writing them to the stream.</span></span> <span data-ttu-id="e2954-107">Использование некоторых кодировщиков приводит к компромиссам (например, JPEG), который меняет цветовую информацию для улучшения сжатия.</span><span class="sxs-lookup"><span data-stu-id="e2954-107">Using some encoders results in tradeoffs—for example, JPEG, which trades off color information for better compression.</span></span> <span data-ttu-id="e2954-108">Другие кодировщики не приводят к таким потерям, например к точечному рисунку (BMP).</span><span class="sxs-lookup"><span data-stu-id="e2954-108">Other encoders do not result in such losses—for example, bitmap (BMP).</span></span> <span data-ttu-id="e2954-109">Так как многие кодеки используют собственные технологии для достижения лучшего сжатия и точности изображений, сведения о кодировании образа являются разработчиком кодека.</span><span class="sxs-lookup"><span data-stu-id="e2954-109">Because many codecs use proprietary technology to achieve better compression and image fidelity, the details on how an image gets encoded are up to the codec developer.</span></span>

<span data-ttu-id="e2954-110">Этот раздел включает следующие подразделы:</span><span class="sxs-lookup"><span data-stu-id="e2954-110">This topic includes the following sections.</span></span>

-   [<span data-ttu-id="e2954-111">ивикбитмапенкодер</span><span class="sxs-lookup"><span data-stu-id="e2954-111">IWICBitmapEncoder</span></span>](#iwicbitmapencoder)
-   [<span data-ttu-id="e2954-112">ивикбитмапфраминкоде</span><span class="sxs-lookup"><span data-stu-id="e2954-112">IWICBitmapFrameEncode</span></span>](#iwicbitmapframeencode)
-   [<span data-ttu-id="e2954-113">Пример кодировки TIFF</span><span class="sxs-lookup"><span data-stu-id="e2954-113">TIFF Encoding Example</span></span>](#tiff-encoding-example)
-   [<span data-ttu-id="e2954-114">Использование параметров кодировщика</span><span class="sxs-lookup"><span data-stu-id="e2954-114">Encoder Options Usage</span></span>](#encoder-options-usage)
-   [<span data-ttu-id="e2954-115">Параметры кодировщика</span><span class="sxs-lookup"><span data-stu-id="e2954-115">Encoder Options</span></span>](#encoder-options-usage)
-   [<span data-ttu-id="e2954-116">Примеры параметров кодировщика</span><span class="sxs-lookup"><span data-stu-id="e2954-116">Encoder Options Examples</span></span>](#encoder-options-examples)
-   [<span data-ttu-id="e2954-117">См. также</span><span class="sxs-lookup"><span data-stu-id="e2954-117">Related topics</span></span>](#related-topics)

## <a name="iwicbitmapencoder"></a><span data-ttu-id="e2954-118">ивикбитмапенкодер</span><span class="sxs-lookup"><span data-stu-id="e2954-118">IWICBitmapEncoder</span></span>

<span data-ttu-id="e2954-119">[**Ивикбитмапенкодер**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) является основным интерфейсом для кодирования изображения в целевой формат и используется для сериализации компонентов изображения, таких как Thumbnail ([**сетсумбнаил**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail)) и Frames ([**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe)), в файл изображения.</span><span class="sxs-lookup"><span data-stu-id="e2954-119">[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) is the main interface for encoding an image to the target format and used to serialize an image's components, such as thumbnail ([**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail)) and frames ([**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe)), to the image file.</span></span>

<span data-ttu-id="e2954-120">Как и когда происходит сериализация, остается разработчиком кодека.</span><span class="sxs-lookup"><span data-stu-id="e2954-120">How and when serialization occurs is left up to the codec developer.</span></span> <span data-ttu-id="e2954-121">Каждый отдельный блок данных в целевом формате файла должен быть задан независимо от порядка, но опять же, это решение разработчика кодека.</span><span class="sxs-lookup"><span data-stu-id="e2954-121">Each individual block of data within the target file format should be able to set independent of order, but again, this is the codec developer's decision.</span></span> <span data-ttu-id="e2954-122">Однако после вызова метода [**commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit) изменения в образ не должны быть разрешены и поток должен быть закрыт.</span><span class="sxs-lookup"><span data-stu-id="e2954-122">Once the [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit) method is called however, changes to the image should not be allowed and the stream should be closed.</span></span>

## <a name="iwicbitmapframeencode"></a><span data-ttu-id="e2954-123">ивикбитмапфраминкоде</span><span class="sxs-lookup"><span data-stu-id="e2954-123">IWICBitmapFrameEncode</span></span>

<span data-ttu-id="e2954-124">[**Ивикбитмапфраминкоде**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) — это интерфейс для кодирования отдельных кадров изображения.</span><span class="sxs-lookup"><span data-stu-id="e2954-124">[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) is the interface for encoding the individual frames of an image.</span></span> <span data-ttu-id="e2954-125">Он предоставляет методы для установки отдельных компонентов создания образов кадров, например эскизов и кадров, а также размеров изображений, точек на дюйм и форматов пикселей.</span><span class="sxs-lookup"><span data-stu-id="e2954-125">It provides methods for setting individual frame imaging components, such as thumbnails and frames, as well as image dimensions, DPI, and pixel formats.</span></span>

<span data-ttu-id="e2954-126">Отдельные кадры могут быть закодированы с помощью метаданных, связанных с кадром, поэтому [**ивикбитмапфраминкоде**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) предоставляет доступ к модулю записи метаданных с помощью метода [**жетметадатакуеривритер**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) .</span><span class="sxs-lookup"><span data-stu-id="e2954-126">Individual frames may be encoded with frame-specific metadata so [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) provides access to a metadata writer through the [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) method.</span></span>

<span data-ttu-id="e2954-127">Метод [**commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) кадра фиксирует все изменения в отдельном кадре и указывает, что изменения в этом кадре больше не должны приниматься.</span><span class="sxs-lookup"><span data-stu-id="e2954-127">The frame's [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) method commits all changes to the individual frame and indicates that changes to that frame should no longer be accepted.</span></span>

## <a name="tiff-encoding-example"></a><span data-ttu-id="e2954-128">Пример кодировки TIFF</span><span class="sxs-lookup"><span data-stu-id="e2954-128">TIFF Encoding Example</span></span>

<span data-ttu-id="e2954-129">В следующем примере изображение в формате TIFF кодируется с помощью [**ивикбитмапенкодер**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) и [**ивикбитмапфраминкоде**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode).</span><span class="sxs-lookup"><span data-stu-id="e2954-129">In the following example, a Tagged Image File Format (TIFF) image is encoded using [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) and an [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode).</span></span> <span data-ttu-id="e2954-130">Выход TIFF настраивается с помощью [**виктиффкомпрессионоптион**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) , а кадр растрового изображения инициализируется с использованием заданных параметров.</span><span class="sxs-lookup"><span data-stu-id="e2954-130">The TIFF output is customized using the [**WICTiffCompressionOption**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) and the bitmap frame is initialized using the given options.</span></span> <span data-ttu-id="e2954-131">После создания образа с помощью [**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels)кадр фиксируется путем [**фиксации**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) , а образ сохраняется с помощью [**commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit).</span><span class="sxs-lookup"><span data-stu-id="e2954-131">Once the image has been created using [**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels), the frame is committed by way of [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) and the image is saved using [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit).</span></span>


```C++
IWICImagingFactory *piFactory = NULL;
IWICBitmapEncoder *piEncoder = NULL;
IWICBitmapFrameEncode *piBitmapFrame = NULL;
IPropertyBag2 *pPropertybag = NULL;

IWICStream *piStream = NULL;
UINT uiWidth = 640;
UINT uiHeight = 480;

HRESULT hr = CoCreateInstance(
                CLSID_WICImagingFactory,
                NULL,
                CLSCTX_INPROC_SERVER,
                IID_IWICImagingFactory,
                (LPVOID*) &piFactory);

if (SUCCEEDED(hr))
{
    hr = piFactory->CreateStream(&piStream);
}

if (SUCCEEDED(hr))
{
    hr = piStream->InitializeFromFilename(L"output.tif", GENERIC_WRITE);
}

if (SUCCEEDED(hr))
{
   hr = piFactory->CreateEncoder(GUID_ContainerFormatTiff, NULL, &piEncoder);
}

if (SUCCEEDED(hr))
{
    hr = piEncoder->Initialize(piStream, WICBitmapEncoderNoCache);
}

if (SUCCEEDED(hr))
{
    hr = piEncoder->CreateNewFrame(&piBitmapFrame, &pPropertybag);
}

if (SUCCEEDED(hr))
{        
    // This is how you customize the TIFF output.
    PROPBAG2 option = { 0 };
    option.pstrName = L"TiffCompressionMethod";
    VARIANT varValue;    
    VariantInit(&varValue);
    varValue.vt = VT_UI1;
    varValue.bVal = WICTiffCompressionZIP;      
    hr = pPropertybag->Write(1, &option, &varValue);        
    if (SUCCEEDED(hr))
    {
        hr = piBitmapFrame->Initialize(pPropertybag);
    }
}

if (SUCCEEDED(hr))
{
    hr = piBitmapFrame->SetSize(uiWidth, uiHeight);
}

WICPixelFormatGUID formatGUID = GUID_WICPixelFormat24bppBGR;
if (SUCCEEDED(hr))
{
    hr = piBitmapFrame->SetPixelFormat(&formatGUID);
}

if (SUCCEEDED(hr))
{
    // We're expecting to write out 24bppRGB. Fail if the encoder cannot do it.
    hr = IsEqualGUID(formatGUID, GUID_WICPixelFormat24bppBGR) ? S_OK : E_FAIL;
}

if (SUCCEEDED(hr))
{
    UINT cbStride = (uiWidth * 24 + 7)/8/***WICGetStride**_/;
    UINT cbBufferSize = uiHeight _ cbStride;

    BYTE *pbBuffer = new BYTE[cbBufferSize];

    if (pbBuffer != NULL)
    {
        for (UINT i = 0; i < cbBufferSize; i++)
        {
            pbBuffer[i] = static_cast<BYTE>(rand());
        }

        hr = piBitmapFrame->WritePixels(uiHeight, cbStride, cbBufferSize, pbBuffer);

        delete[] pbBuffer;
    }
    else
    {
        hr = E_OUTOFMEMORY;
    }
}

if (SUCCEEDED(hr))
{
    hr = piBitmapFrame->Commit();
}    

if (SUCCEEDED(hr))
{
    hr = piEncoder->Commit();
}

if (piFactory)
    piFactory->Release();

if (piEncoder)
    piEncoder->Release();

if (piBitmapFrame)
    piBitmapFrame->Release();

if (pPropertybag)
    pPropertybag->Release();

if (piStream)
    piStream->Release();

return hr;
```



## <a name="encoder-options-usage"></a><span data-ttu-id="e2954-132">Использование параметров кодировщика</span><span class="sxs-lookup"><span data-stu-id="e2954-132">Encoder Options Usage</span></span>

<span data-ttu-id="e2954-133">Различные кодировщики для разных форматов должны предоставлять различные параметры кодирования изображения.</span><span class="sxs-lookup"><span data-stu-id="e2954-133">Different encoders for different formats need to expose different options for how an image is encoded.</span></span> <span data-ttu-id="e2954-134">Компонент Windows Imaging Component (WIC) предоставляет единообразный механизм, позволяющий определить, требуются ли параметры кодировки, не требуя, чтобы приложения работали с несколькими кодировщиками, не зная определенного формата.</span><span class="sxs-lookup"><span data-stu-id="e2954-134">Windows Imaging Component (WIC) provides a consistent mechanism for expressing whether encoding options are required while still enabling applications to work with multiple encoders without requiring knowledge of a particular format.</span></span> <span data-ttu-id="e2954-135">Это достигается путем предоставления параметра [ипропертибаг](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768196(v=vs.85)) для метода [**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) и метода [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-initialize) .</span><span class="sxs-lookup"><span data-stu-id="e2954-135">This is accomplished by providing an [IPropertyBag](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768196(v=vs.85)) parameter on the [**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) method and the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-initialize) method.</span></span>

<span data-ttu-id="e2954-136">Фабрика компонентов предоставляет простую точку для создания контейнера свойств параметров кодировщика.</span><span class="sxs-lookup"><span data-stu-id="e2954-136">The component factory provides an easy creation point for creating an encoder options property bag.</span></span> <span data-ttu-id="e2954-137">Кодеки могут использовать эту службу, если необходимо предоставить простой, интуитивно понятный и неконфликтующий набор параметров кодировщика.</span><span class="sxs-lookup"><span data-stu-id="e2954-137">Codecs can use this service if they need to provide a simple, intuitive and non-conflicting set of encoder options.</span></span> <span data-ttu-id="e2954-138">Во время создания контейнер свойств Imaging должен быть инициализирован во всех параметрах кодировщика, относящихся к этому кодеку.</span><span class="sxs-lookup"><span data-stu-id="e2954-138">The imaging property bag must be initialized during creation with all the encoder options relevant to that codec.</span></span> <span data-ttu-id="e2954-139">Для параметров кодировщика из канонического набора диапазон значений будет применен при записи.</span><span class="sxs-lookup"><span data-stu-id="e2954-139">For encoder options from the canonical set, the value range will be enforced on Write.</span></span> <span data-ttu-id="e2954-140">Для более сложных потребностей кодеки должны написать собственную реализацию контейнера свойств.</span><span class="sxs-lookup"><span data-stu-id="e2954-140">For more advanced needs, codecs should write their own property bag implementation.</span></span>

<span data-ttu-id="e2954-141">Приложению предоставляется набор параметров кодировщика во время создания кадра и перед инициализацией фрейма кодировщика должны быть настроены все значения.</span><span class="sxs-lookup"><span data-stu-id="e2954-141">An application is given the encoder options bag during frame creation and must configure any values prior to initializing the encoder frame.</span></span> <span data-ttu-id="e2954-142">Для приложения, управляемого пользовательским интерфейсом, оно может предоставлять стандартный пользовательский интерфейс для канонических параметров кодировщика и расширенное представление для остальных параметров.</span><span class="sxs-lookup"><span data-stu-id="e2954-142">For a UI-driven application, it can offer a fixed UI for the canonical encoder options and an advanced view for remaining options.</span></span> <span data-ttu-id="e2954-143">Изменения могут выполняться по одному за раз с помощью метода Write, и любая ошибка будет передаваться через Иеррорлог.</span><span class="sxs-lookup"><span data-stu-id="e2954-143">Changes can be made one at a time through the Write method and any error will be reported through IErrorLog.</span></span> <span data-ttu-id="e2954-144">Приложение пользовательского интерфейса всегда должно повторно считаться и отображать все параметры после внесения изменений в случае, если изменение привело к каскадному применению.</span><span class="sxs-lookup"><span data-stu-id="e2954-144">The UI application should always re-read and display all options after making a change in case the change caused a cascade effect.</span></span> <span data-ttu-id="e2954-145">Приложение должно быть подготовлено к обработке ошибок инициализации кадров для кодеков, которые предоставляют минимальный отчет об ошибках через контейнер свойств.</span><span class="sxs-lookup"><span data-stu-id="e2954-145">An application should be prepared to handle failed frame initialization for codecs that only provide minimal error reporting through their property bag.</span></span>

## <a name="encoder-options"></a><span data-ttu-id="e2954-146">Параметры кодировщика</span><span class="sxs-lookup"><span data-stu-id="e2954-146">Encoder Options</span></span>

<span data-ttu-id="e2954-147">Приложение может столкнуться со следующим набором параметров кодировщика.</span><span class="sxs-lookup"><span data-stu-id="e2954-147">An application can expect to encounter the following set of encoder options.</span></span> <span data-ttu-id="e2954-148">Параметры кодировщика соответствуют возможностям кодировщика и базовому формату контейнера, поэтому их характер не зависит от кодека.</span><span class="sxs-lookup"><span data-stu-id="e2954-148">Encoder options reflect the capabilities of an encoder and the underlying container format, and therefore are by their nature not really codec-agnostic.</span></span> <span data-ttu-id="e2954-149">По возможности новые параметры должны быть нормализованы, чтобы их можно было применить к новым кодекам.</span><span class="sxs-lookup"><span data-stu-id="e2954-149">When possible, new options should be normalized so they can be applied to new codecs that emerge.</span></span>



| <span data-ttu-id="e2954-150">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="e2954-150">Property Name</span></span>      | <span data-ttu-id="e2954-151">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="e2954-151">VARTYPE</span></span>  | <span data-ttu-id="e2954-152">Значение</span><span class="sxs-lookup"><span data-stu-id="e2954-152">Value</span></span>                                                                     | <span data-ttu-id="e2954-153">Применимые кодеки</span><span class="sxs-lookup"><span data-stu-id="e2954-153">Applicable Codecs</span></span> |
|--------------------|----------|---------------------------------------------------------------------------|-------------------|
| <span data-ttu-id="e2954-154">ImageQuality</span><span class="sxs-lookup"><span data-stu-id="e2954-154">ImageQuality</span></span>       | <span data-ttu-id="e2954-155">VT \_ R4</span><span class="sxs-lookup"><span data-stu-id="e2954-155">VT\_R4</span></span>   | <span data-ttu-id="e2954-156">0 – 1,0</span><span class="sxs-lookup"><span data-stu-id="e2954-156">0-1.0</span></span>                                                                     | <span data-ttu-id="e2954-157">JPEG, Хдфото</span><span class="sxs-lookup"><span data-stu-id="e2954-157">JPEG, HDPhoto</span></span>     |
| <span data-ttu-id="e2954-158">CompressionQuality</span><span class="sxs-lookup"><span data-stu-id="e2954-158">CompressionQuality</span></span> | <span data-ttu-id="e2954-159">VT \_ R4</span><span class="sxs-lookup"><span data-stu-id="e2954-159">VT\_R4</span></span>   | <span data-ttu-id="e2954-160">0 – 1,0</span><span class="sxs-lookup"><span data-stu-id="e2954-160">0-1.0</span></span>                                                                     | <span data-ttu-id="e2954-161">TIFF</span><span class="sxs-lookup"><span data-stu-id="e2954-161">TIFF</span></span>              |
| <span data-ttu-id="e2954-162">Lossless</span><span class="sxs-lookup"><span data-stu-id="e2954-162">Lossless</span></span>           | <span data-ttu-id="e2954-163">Логическое значение VT \_</span><span class="sxs-lookup"><span data-stu-id="e2954-163">VT\_BOOL</span></span> | <span data-ttu-id="e2954-164">**true**, **false**</span><span class="sxs-lookup"><span data-stu-id="e2954-164">**TRUE**, **FALSE**</span></span>                                                       | <span data-ttu-id="e2954-165">хдфото</span><span class="sxs-lookup"><span data-stu-id="e2954-165">HDPhoto</span></span>           |
| <span data-ttu-id="e2954-166">битмаптрансформ</span><span class="sxs-lookup"><span data-stu-id="e2954-166">BitmapTransform</span></span>    | <span data-ttu-id="e2954-167">VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="e2954-167">VT\_UI1</span></span>  | [<span data-ttu-id="e2954-168">**викбитмаптрансформоптионс**</span><span class="sxs-lookup"><span data-stu-id="e2954-168">**WICBitmapTransformOptions**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) | <span data-ttu-id="e2954-169">JPEG</span><span class="sxs-lookup"><span data-stu-id="e2954-169">JPEG</span></span>              |



 

<span data-ttu-id="e2954-170">Имажекуалти в 0,0 означает наименьшую возможную точность и 1,0 означает максимальную достоверность, которая может также означать потери данных в зависимости от кодека.</span><span class="sxs-lookup"><span data-stu-id="e2954-170">ImageQualty of 0.0 means the lowest possible fidelity rendition and 1.0 means the highest fidelity, which may also imply lossless depending on the codec.</span></span>

<span data-ttu-id="e2954-171">Компрессионкуалити 0,0 означает, что наименее эффективная доступная схема сжатия, как правило, приводит к быстрой кодировке, но большему результату.</span><span class="sxs-lookup"><span data-stu-id="e2954-171">CompressionQuality of 0.0 means the least efficient compression scheme available, typically resulting in a fast encode but larger output.</span></span> <span data-ttu-id="e2954-172">Значение 1,0 означает, что самая эффективная схема доступна, обычно занимает больше времени для кодирования, но создает небольшие выходные данные.</span><span class="sxs-lookup"><span data-stu-id="e2954-172">A value of 1.0 means the most efficient scheme available, typically taking more time to encode but producing smaller output.</span></span> <span data-ttu-id="e2954-173">В зависимости от возможностей кодека этот диапазон может быть сопоставлен с дискретным набором доступных методов сжатия.</span><span class="sxs-lookup"><span data-stu-id="e2954-173">Depending on the capabilities of the codec, this range may be mapped onto a discrete set of available compression methods.</span></span>

<span data-ttu-id="e2954-174">Без потерь означает, что кодек кодирует изображение как безотносительное без потери данных изображения.</span><span class="sxs-lookup"><span data-stu-id="e2954-174">Lossless means that the codec encodes the image as lossless with no image data loss.</span></span> <span data-ttu-id="e2954-175">Если включено безпотерь, Имажекуалити игнорируется.</span><span class="sxs-lookup"><span data-stu-id="e2954-175">If Lossless is enabled, ImageQuality is ignored.</span></span>

<span data-ttu-id="e2954-176">В дополнение к приведенным выше универсальным параметрам кодировщика кодеки, предоставляемые с помощью WIC, поддерживают следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="e2954-176">In addition to the above generic encoder options, codecs supplied with WIC support the following options.</span></span> <span data-ttu-id="e2954-177">Если кодек должен поддерживать параметр, который согласуется с использованием этих кодеков, рекомендуется сделать это.</span><span class="sxs-lookup"><span data-stu-id="e2954-177">If a codec has a need to support an option that is consistent with the usage in these supplied codecs, it is encouraged to do so.</span></span>



| <span data-ttu-id="e2954-178">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="e2954-178">Property Name</span></span>           | <span data-ttu-id="e2954-179">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="e2954-179">VARTYPE</span></span>           | <span data-ttu-id="e2954-180">Значение</span><span class="sxs-lookup"><span data-stu-id="e2954-180">Value</span></span>                                                                             | <span data-ttu-id="e2954-181">Применимые кодеки</span><span class="sxs-lookup"><span data-stu-id="e2954-181">Applicable Codecs</span></span> |
|-------------------------|-------------------|-----------------------------------------------------------------------------------|-------------------|
| <span data-ttu-id="e2954-182">InterlaceOption</span><span class="sxs-lookup"><span data-stu-id="e2954-182">InterlaceOption</span></span>         | <span data-ttu-id="e2954-183">Логическое значение VT \_</span><span class="sxs-lookup"><span data-stu-id="e2954-183">VT\_BOOL</span></span>          | <span data-ttu-id="e2954-184">Вкл./выкл.</span><span class="sxs-lookup"><span data-stu-id="e2954-184">On/Off</span></span>                                                                            | <span data-ttu-id="e2954-185">PNG</span><span class="sxs-lookup"><span data-stu-id="e2954-185">PNG</span></span>               |
| <span data-ttu-id="e2954-186">FilterOption</span><span class="sxs-lookup"><span data-stu-id="e2954-186">FilterOption</span></span>            | <span data-ttu-id="e2954-187">VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="e2954-187">VT\_UI1</span></span>           | [<span data-ttu-id="e2954-188">**викпнгфилтероптион**</span><span class="sxs-lookup"><span data-stu-id="e2954-188">**WICPngFilterOption**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption)                       | <span data-ttu-id="e2954-189">PNG</span><span class="sxs-lookup"><span data-stu-id="e2954-189">PNG</span></span>               |
| <span data-ttu-id="e2954-190">TiffCompressionMethod</span><span class="sxs-lookup"><span data-stu-id="e2954-190">TiffCompressionMethod</span></span>   | <span data-ttu-id="e2954-191">VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="e2954-191">VT\_UI1</span></span>           | [<span data-ttu-id="e2954-192">**виктиффкомпрессионоптион**</span><span class="sxs-lookup"><span data-stu-id="e2954-192">**WICTiffCompressionOption**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption)           | <span data-ttu-id="e2954-193">TIFF</span><span class="sxs-lookup"><span data-stu-id="e2954-193">TIFF</span></span>              |
| <span data-ttu-id="e2954-194">Luminance</span><span class="sxs-lookup"><span data-stu-id="e2954-194">Luminance</span></span>               | <span data-ttu-id="e2954-195">VT \_ UI4/VT \_</span><span class="sxs-lookup"><span data-stu-id="e2954-195">VT\_UI4/VT\_ARRAY</span></span> | <span data-ttu-id="e2954-196">64 записей (ДКТ)</span><span class="sxs-lookup"><span data-stu-id="e2954-196">64 Entries (DCT)</span></span>                                                                  | <span data-ttu-id="e2954-197">JPEG</span><span class="sxs-lookup"><span data-stu-id="e2954-197">JPEG</span></span>              |
| <span data-ttu-id="e2954-198">Chrominance</span><span class="sxs-lookup"><span data-stu-id="e2954-198">Chrominance</span></span>             | <span data-ttu-id="e2954-199">VT \_ UI4/VT \_</span><span class="sxs-lookup"><span data-stu-id="e2954-199">VT\_UI4/VT\_ARRAY</span></span> | <span data-ttu-id="e2954-200">64 записей (ДКТ)</span><span class="sxs-lookup"><span data-stu-id="e2954-200">64 Entries (DCT)</span></span>                                                                  | <span data-ttu-id="e2954-201">JPEG</span><span class="sxs-lookup"><span data-stu-id="e2954-201">JPEG</span></span>              |
| <span data-ttu-id="e2954-202">JpegYCrCbSubsampling</span><span class="sxs-lookup"><span data-stu-id="e2954-202">JpegYCrCbSubsampling</span></span>    | <span data-ttu-id="e2954-203">VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="e2954-203">VT\_UI1</span></span>           | [<span data-ttu-id="e2954-204">**викжпегикркбсубсамплингоптион**</span><span class="sxs-lookup"><span data-stu-id="e2954-204">**WICJpegYCrCbSubsamplingOption**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) | <span data-ttu-id="e2954-205">JPEG</span><span class="sxs-lookup"><span data-stu-id="e2954-205">JPEG</span></span>              |
| <span data-ttu-id="e2954-206">SuppressApp0</span><span class="sxs-lookup"><span data-stu-id="e2954-206">SuppressApp0</span></span>            | <span data-ttu-id="e2954-207">Логическое значение VT \_</span><span class="sxs-lookup"><span data-stu-id="e2954-207">VT\_BOOL</span></span>          |                                                                                   | <span data-ttu-id="e2954-208">JPEG</span><span class="sxs-lookup"><span data-stu-id="e2954-208">JPEG</span></span>              |
| <span data-ttu-id="e2954-209">EnableV5Header32bppBGRA</span><span class="sxs-lookup"><span data-stu-id="e2954-209">EnableV5Header32bppBGRA</span></span> | <span data-ttu-id="e2954-210">Логическое значение VT \_</span><span class="sxs-lookup"><span data-stu-id="e2954-210">VT\_BOOL</span></span>          | <span data-ttu-id="e2954-211">Вкл./выкл.</span><span class="sxs-lookup"><span data-stu-id="e2954-211">On/Off</span></span>                                                                            | <span data-ttu-id="e2954-212">BMP</span><span class="sxs-lookup"><span data-stu-id="e2954-212">BMP</span></span>               |



 

<span data-ttu-id="e2954-213">Используйте **VT \_ Empty** , чтобы **\* не задавать \*** значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e2954-213">Use **VT\_EMPTY** to indicate **\*not set\*** as the default.</span></span> <span data-ttu-id="e2954-214">Если дополнительные свойства заданы, но не поддерживаются, кодировщику следует игнорировать их. Это позволяет приложениям создавать код с меньшей логикой, если требуется возможность, которая может отсутствовать или отсутствовать.</span><span class="sxs-lookup"><span data-stu-id="e2954-214">If additional properties are set but not supported, the encoder should ignore them; this allows applications to code less logic if they want a capability that may or may not be present.</span></span>

## <a name="encoder-options-examples"></a><span data-ttu-id="e2954-215">Примеры параметров кодировщика</span><span class="sxs-lookup"><span data-stu-id="e2954-215">Encoder Options Examples</span></span>

<span data-ttu-id="e2954-216">В приведенном выше [примере кодировки TIFF](#tiff-encoding-example) задан параметр кодировщика.</span><span class="sxs-lookup"><span data-stu-id="e2954-216">In the [TIFF Encoding Example](#tiff-encoding-example) above, a specific encoder option is set.</span></span> <span data-ttu-id="e2954-217">Элементу *пстрнаме* структуры PROPBAG2 присваивается соответствующее имя свойства, а для варианта устанавливается соответствующий VarType и требуемое значение — в данном случае является членом перечисления [**виктиффкомпрессионоптион**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) .</span><span class="sxs-lookup"><span data-stu-id="e2954-217">The *pstrName* member of the PROPBAG2 structure is set to the appropriate property name, and the VARIANT is set to the corresponding VARTYPE and the desired value—in this case, a member of the [**WICTiffCompressionOption**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) enumeration.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = piEncoder->CreateNewFrame(&piBitmapFrame, &pPropertybag);
}

if (SUCCEEDED(hr))
{        
    // This is how you customize the TIFF output.
    PROPBAG2 option = { 0 };
    option.pstrName = L"TiffCompressionMethod";
    VARIANT varValue;    
    VariantInit(&varValue);
    varValue.vt = VT_UI1;
    varValue.bVal = WICTiffCompressionZIP;      
    hr = pPropertybag->Write(1, &option, &varValue);        
    if (SUCCEEDED(hr))
    {
        hr = piBitmapFrame->Initialize(pPropertybag);
    }
}
```



<span data-ttu-id="e2954-218">Чтобы использовать параметры кодировщика по умолчанию, просто инициализируйте кадр точечного рисунка с контейнером свойств, возвращенным при создании кадра.</span><span class="sxs-lookup"><span data-stu-id="e2954-218">To use the default encoder options, simply initialize the bitmap frame with the property bag returned when the frame was created.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = piEncoder->CreateNewFrame(&piBitmapFrame, &pPropertybag);
}

if (SUCCEEDED(hr))
{        
    // Accept the default encoder options.
    if (SUCCEEDED(hr))
    {
        hr = piBitmapFrame->Initialize(pPropertybag);
    }
}
```



<span data-ttu-id="e2954-219">Кроме того, можно исключить контейнер свойств, когда не будут рассматриваться параметры кодировщика.</span><span class="sxs-lookup"><span data-stu-id="e2954-219">It is also possible to eliminate the property bag when no encoder options are being considered.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = piEncoder->CreateNewFrame(&piBitmapFrame, 0);
}

if (SUCCEEDED(hr))
{        
    // No encoder options.
    if (SUCCEEDED(hr))
    {
        hr = piBitmapFrame->Initialize(0);
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="e2954-220">См. также</span><span class="sxs-lookup"><span data-stu-id="e2954-220">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="e2954-221">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="e2954-221">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e2954-222">Общие сведения о компоненте создания образов Windows</span><span class="sxs-lookup"><span data-stu-id="e2954-222">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="e2954-223">Общие сведения о декодировании</span><span class="sxs-lookup"><span data-stu-id="e2954-223">Decoding Overview</span></span>](-wic-creating-decoder.md)
</dt> <dt>

<span data-ttu-id="e2954-224">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="e2954-224">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="e2954-225">Написание WIC-Enabled КОДЕка</span><span class="sxs-lookup"><span data-stu-id="e2954-225">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 
