---
description: Реализация Ивикбитмапдекодер
ms.assetid: 9e316bdd-803a-47af-b004-7675478eb829
title: Реализация Ивикбитмапдекодер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b31bca377828606fe1beb68d6f1d95d290e01407
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104080859"
---
# <a name="implementing-iwicbitmapdecoder"></a><span data-ttu-id="393be-103">Реализация Ивикбитмапдекодер</span><span class="sxs-lookup"><span data-stu-id="393be-103">Implementing IWICBitmapDecoder</span></span>

## <a name="iwicbitmapdecoder"></a><span data-ttu-id="393be-104">ивикбитмапдекодер</span><span class="sxs-lookup"><span data-stu-id="393be-104">IWICBitmapDecoder</span></span>

<span data-ttu-id="393be-105">Когда приложение запрашивает декодер, первая точка взаимодействия с кодеком осуществляется через интерфейс [**ивикбитмапдекодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) .</span><span class="sxs-lookup"><span data-stu-id="393be-105">When an application requests a decoder, the first point of interaction with the codec is through the [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) interface.</span></span> <span data-ttu-id="393be-106">Это интерфейс уровня контейнера, который предоставляет доступ к свойствам верхнего уровня контейнера и, что самое важное, к кадрам, которые он содержит.</span><span class="sxs-lookup"><span data-stu-id="393be-106">This is the container-level interface that provides access to the top-level properties of the container and, most importantly, the frames it contains.</span></span> <span data-ttu-id="393be-107">Это основной интерфейс класса декодера уровня контейнера.</span><span class="sxs-lookup"><span data-stu-id="393be-107">This is the primary interface on your container-level decoder class.</span></span>

``` syntax
interface IWICBitmapDecoder : IUnknown
{
// Required methods
   HRESULT QueryCapability (IStream *pIStream, 
      DWORD *pdwCapabilities );
   HRESULT Initialize ( IStream *pIStream,
      WICDecodeOptions cacheOptions );
   HRESULT GetContainerFormat ( GUID *pguidContainerFormat );
   HRESULT GetDecoderInfo ( IWICBitmapDecoderInfo **pIDecoderInfo );
   HRESULT GetFrameCount ( UINT *pCount );
   HRESULT GetFrame ( UINT index, 
      IWICBitmapFrameDecode **ppIBitmapFrame );

// Optional methods
   HRESULT GetPreview ( IWICBitmapSource **ppIPreview );
   HRESULT GetThumbnail ( IWICBitmapSource **ppIThumbnail );
   HRESULT GetColorContexts ( UINT cCount, 
      IWICColorContext **ppIColorContexts, 
      UINT *pcActualCount );
   HRESULT GetMetadataQueryReader ( IWICMetadataQueryReader **ppIMetadataQueryReader);
   HRESULT CopyPalette ( IWICPalette *pIPalette );
}
```

<span data-ttu-id="393be-108">Некоторые форматы изображений имеют глобальные эскизы, цветовые контексты или метаданные, а многие форматы изображений предоставляют их только для отдельных кадров.</span><span class="sxs-lookup"><span data-stu-id="393be-108">Some image formats have global thumbnails, color contexts, or metadata, while many image formats provide these only on a per-frame basis.</span></span> <span data-ttu-id="393be-109">Методы доступа к этим элементам являются необязательными для [**ивикбитмапдекодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder), но требуются для [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode).</span><span class="sxs-lookup"><span data-stu-id="393be-109">The methods for accessing these items are optional on [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder), but are required on [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode).</span></span> <span data-ttu-id="393be-110">Аналогичным образом, некоторые кодеки не используют Индексированные форматы пикселей, поэтому не нужно реализовывать методы [копипалетте](-wic-imp-iwicbitmapframedecode.md) в любом интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="393be-110">Likewise, some codecs do not use indexed pixel formats and so do not need to implement the [CopyPalette](-wic-imp-iwicbitmapframedecode.md) methods on either interface.</span></span> <span data-ttu-id="393be-111">Дополнительные сведения о необязательных методах **ивикбитмапдекодер** см. в разделе [Реализация IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md), где они чаще всего реализуются.</span><span class="sxs-lookup"><span data-stu-id="393be-111">For more information on the optional **IWICBitmapDecoder** methods, see [Implementing IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md), where they are most commonly implemented.</span></span>

### <a name="querycapability"></a><span data-ttu-id="393be-112">куерикапабилити</span><span class="sxs-lookup"><span data-stu-id="393be-112">QueryCapability</span></span>

<span data-ttu-id="393be-113">[**Куерикапабилити**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-querycapability) — это метод, используемый для арбитража кодека.</span><span class="sxs-lookup"><span data-stu-id="393be-113">[**QueryCapability**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-querycapability) is the method used for codec arbitration.</span></span> <span data-ttu-id="393be-114">(См. раздел [Обнаружение и арбитраж](-wic-howwicworks.md) в разделе [Working of Windows Imaging Component](-wic-howwicworks.md) .</span><span class="sxs-lookup"><span data-stu-id="393be-114">(See [Discovery and Arbitration](-wic-howwicworks.md) in the [How The Windows Imaging Component Works](-wic-howwicworks.md) topic).</span></span> <span data-ttu-id="393be-115">Если два кодека способны декодировать один и тот же формат изображения или если возникает конфликт шаблонов, в котором два кодека используют один и тот же идентифицирующий шаблон, этот метод позволяет выбрать кодек, который наилучшим образом будет обрабатывать любые конкретные изображения.</span><span class="sxs-lookup"><span data-stu-id="393be-115">If two codecs are capable of decoding the same image format, or if a pattern collision occurs in which two codecs use the same identifying pattern, this method allows you to select the codec that can best handle any specific image.</span></span>

<span data-ttu-id="393be-116">При вызове этого метода компонент Windows Imaging Component (WIC) передает фактический поток, содержащий изображение.</span><span class="sxs-lookup"><span data-stu-id="393be-116">When invoking this method, Windows Imaging Component (WIC) passes you the actual stream containing the image.</span></span> <span data-ttu-id="393be-117">Необходимо проверить, можно ли декодировать каждый кадр в изображении и перечислить блоки метаданных, чтобы точно объявить возможности этого декодера относительно конкретного переданного в него потока файлов.</span><span class="sxs-lookup"><span data-stu-id="393be-117">You must verify whether you can decode each frame within the image and enumerate through the metadata blocks, to accurately declare what capabilities this decoder has with respect to the specific file stream passed to it.</span></span> <span data-ttu-id="393be-118">Это важно для всех декодеров, но особенно важно для форматов изображений, основанных на контейнерах формата TIFF.</span><span class="sxs-lookup"><span data-stu-id="393be-118">This is important for all decoders, but particularly important for image formats based on Tagged Image File Format (TIFF) containers.</span></span> <span data-ttu-id="393be-119">Процесс обнаружения выполняется путем сопоставления шаблонов, связанных с декодерами в реестре, с шаблонами в фактическом файле изображения.</span><span class="sxs-lookup"><span data-stu-id="393be-119">The discovery process works by matching patterns associated with decoders in the registry to patterns in the actual image file.</span></span> <span data-ttu-id="393be-120">Объявление идентифицирующего шаблона в реестре гарантирует, что декодер будет всегда обнаруживаться для изображений в вашем формате изображения.</span><span class="sxs-lookup"><span data-stu-id="393be-120">Declaring your identifying pattern in the registry guarantees that your decoder will always be detected for images in your image format.</span></span> <span data-ttu-id="393be-121">Однако декодер по-прежнему может быть обнаружен для изображений в других форматах.</span><span class="sxs-lookup"><span data-stu-id="393be-121">However, your decoder could still be detected for images in other formats.</span></span> <span data-ttu-id="393be-122">Например, все контейнеры TIFF включают шаблон TIFF, который является допустимым идентифицирующим шаблоном для формата изображения TIFF.</span><span class="sxs-lookup"><span data-stu-id="393be-122">For example, all TIFF containers include the TIFF pattern, which is a valid identifying pattern for the TIFF image format.</span></span> <span data-ttu-id="393be-123">Это означает, что во время обнаружения в файлах изображений будут найдены по крайней мере два идентифицирующих шаблона для любого формата изображений, основанного на контейнере в стиле TIFF.</span><span class="sxs-lookup"><span data-stu-id="393be-123">This means that, during discovery, at least two identifying patterns will be found in image files for any image format that’s based on a TIFF-style container.</span></span> <span data-ttu-id="393be-124">Один из них будет шаблоном TIFF, а другой — фактическим шаблоном формата изображения.</span><span class="sxs-lookup"><span data-stu-id="393be-124">One will be the TIFF pattern and the other will be the actual image format pattern.</span></span> <span data-ttu-id="393be-125">Хотя это и менее вероятно, возможны конфликты шаблонов между другими несвязанными форматами изображений.</span><span class="sxs-lookup"><span data-stu-id="393be-125">While less likely, there could be pattern collisions between other unrelated image formats as well.</span></span> <span data-ttu-id="393be-126">Именно поэтому обнаружение и арбитраж являются процессом, сооснованным на двух стадиях.</span><span class="sxs-lookup"><span data-stu-id="393be-126">This is why discovery and arbitration is a two-stage process.</span></span> <span data-ttu-id="393be-127">Всегда проверяйте, что поток изображения, переданный в [**куерикапабилити**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-querycapability) , действительно является допустимым экземпляром собственного формата изображения.</span><span class="sxs-lookup"><span data-stu-id="393be-127">Always verify that the image stream passed to [**QueryCapability**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-querycapability) is actually a valid instance of your own image format.</span></span> <span data-ttu-id="393be-128">Кроме того, если кодек декодирует формат изображения, для которого вы не владеете спецификацией, ваша реализация **куерикапабилити** должна проверить наличие любой функции, которая может быть допустимой в соответствии со спецификацией формата изображения, которую кодек не реализует.</span><span class="sxs-lookup"><span data-stu-id="393be-128">Also, if your codec decodes an image format for which you don’t own the specification, your **QueryCapability** implementation should check for the presence of any feature that may be valid under the image format specification that your codec doesn’t implement.</span></span> <span data-ttu-id="393be-129">Это гарантирует, что пользователи не будут испытывать ненужные ошибки декодирования или получить непредвиденные результаты с помощью кодека.</span><span class="sxs-lookup"><span data-stu-id="393be-129">This will ensure that users do not experience unnecessary decoding failures or get unexpected results with your codec.</span></span>

<span data-ttu-id="393be-130">Перед выполнением какой бы то ни было операции с изображением необходимо сохранить текущее расположение потока, чтобы его можно было восстановить в исходное расположение перед возвратом из метода.</span><span class="sxs-lookup"><span data-stu-id="393be-130">Before performing any operation on the image, you must save the current position of the stream, so you can restore it to its original position before returning from the method.</span></span> <span data-ttu-id="393be-131">Перечисление [**викбитмапдекодеркапабилитиес**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdecodercapabilities) , указывающее возможности, определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="393be-131">The [**WICBitmapDecoderCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdecodercapabilities) enumeration that specifies the capabilities is defined as follows:</span></span>

``` syntax
enum WICBitmapDecoderCapabilities
{   
   WICBitmapDecoderCapabilitySameEncoder,
   WICBitmapDecoderCapabilityCanDecodeAllImages,
   WICBitmapDecoderCapabilityCanDecodeSomeImages,
   WICBitmapDecoderCapabilityCanEnumerateMetadata,
   WICBitmapDecoderCapabilityCanDecodeThumbnail
}
```

<span data-ttu-id="393be-132">Следует объявлять **викбитмапдекодеркапабилитисаминкодер** , только если кодировщик использовал тот, который кодирует изображение.</span><span class="sxs-lookup"><span data-stu-id="393be-132">You should declare **WICBitmapDecoderCapabilitySameEncoder** only if your encoder was the one that encoded the image.</span></span> <span data-ttu-id="393be-133">После проверки возможности декодирования каждого кадра в контейнере следует объявить **викбитмапдекодеркапабилитикандекодесомеимажес** , если вы можете декодировать некоторые, но не все фреймы, **викбитмапдекодеркапабилитикандекодеаллимажес** , если вы можете декодировать все кадры, или ни одного, если вы не можете декодировать их.</span><span class="sxs-lookup"><span data-stu-id="393be-133">After verifying whether you can decode each frame in the container, declare either **WICBitmapDecoderCapabilityCanDecodeSomeImages** if you can decode some but not all of the frames, **WICBitmapDecoderCapabilityCanDecodeAllImages** if you can decode all of the frames, or neither if you cannot decode any of them.</span></span> <span data-ttu-id="393be-134">(Эти два перечисления являются взаимоисключающими; если возвращается **викбитмапдекодеркапабилитикандекодеаллимажес**, **викбитмапдекодеркапабилитикандекодесомеимажес** будет игнорироваться.) Объявите **викбитмапдекодеркапабилитиканенумератеметадата** после проверки, что можно перечислить блоки метаданных в контейнере Image.</span><span class="sxs-lookup"><span data-stu-id="393be-134">(These two enums are mutually exclusive; if you return **WICBitmapDecoderCapabilityCanDecodeAllImages**, **WICBitmapDecoderCapabilityCanDecodeSomeImages** will be ignored.) Declare **WICBitmapDecoderCapabilityCanEnumerateMetadata** after verifying that you can enumerate through the metadata blocks in the image container.</span></span> <span data-ttu-id="393be-135">Не нужно проверять эскиз в каждом кадре.</span><span class="sxs-lookup"><span data-stu-id="393be-135">You don’t have to check for a thumbnail in every frame.</span></span> <span data-ttu-id="393be-136">Если имеется глобальный эскиз, который можно декодировать, можно объявить **викбитмапдекодеркапабилитикандекодесумбнаил**.</span><span class="sxs-lookup"><span data-stu-id="393be-136">If there is a global thumbnail and you can decode it, you can declare **WICBitmapDecoderCapabilityCanDecodeThumbnail**.</span></span> <span data-ttu-id="393be-137">Если глобальный эскиз отсутствует, попытайтесь декодировать эскиз для кадра 0.</span><span class="sxs-lookup"><span data-stu-id="393be-137">If there is no global thumbnail, then attempt to decode the thumbnail for Frame 0.</span></span> <span data-ttu-id="393be-138">Если в любом из этих мест нет эскиза, не объявляйте эту возможность.</span><span class="sxs-lookup"><span data-stu-id="393be-138">If there is no thumbnail in either of these places, do not declare this capability.</span></span>

<span data-ttu-id="393be-139">Определив возможности декодера по отношению к потоку изображения, переданному этому методу, выполните операцию или с [**викбитмапдекодеркапабилитиес**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdecodercapabilities) , проверив, что этот декодер может выполняться на этом изображении, и возвратит результат.</span><span class="sxs-lookup"><span data-stu-id="393be-139">After determining the capabilities of the decoder with respect to the image stream passed to this method, perform an OR operation with the [**WICBitmapDecoderCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdecodercapabilities) you have verified that this decoder can perform on this image, and return the result.</span></span> <span data-ttu-id="393be-140">Не забудьте восстановить исходное расположение потока перед возвратом.</span><span class="sxs-lookup"><span data-stu-id="393be-140">Remember to restore the stream to its original position before returning.</span></span>

### <a name="initialize"></a><span data-ttu-id="393be-141">Инициализация</span><span class="sxs-lookup"><span data-stu-id="393be-141">Initialize</span></span>

<span data-ttu-id="393be-142">[**Инициализация**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-initialize) вызывается приложением после выбора декодера для декодирования определенного изображения.</span><span class="sxs-lookup"><span data-stu-id="393be-142">[**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-initialize) is invoked by an application after a decoder has been selected to decode a specific image.</span></span> <span data-ttu-id="393be-143">Поток изображения передается декодеру, и вызывающий объект может дополнительно указать параметр кэша [**викдекодеоптионс**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) для работы с метаданными в файле.</span><span class="sxs-lookup"><span data-stu-id="393be-143">The image stream is passed to the decoder, and a caller may optionally specify the [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) cache option for dealing with the metadata in the file.</span></span>

``` syntax
enum WICDecodeOptions
{
   WICDecodeMetadataCacheOnDemand,
   WICDecodeMetadataCacheOnLoad
}
```

<span data-ttu-id="393be-144">Некоторые приложения используют метаданные больше, чем другие.</span><span class="sxs-lookup"><span data-stu-id="393be-144">Some applications use metadata more than others.</span></span> <span data-ttu-id="393be-145">Большинству приложений не требуется доступ ко всем метаданным в файле изображения и запрос конкретных метаданных по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="393be-145">Most applications don’t need to access all the metadata in an image file, and will request specific metadata as they need it.</span></span> <span data-ttu-id="393be-146">Другие приложения, скорее всего, будут кэшировать все метаданные заранее, чем удерживать файловый поток и выполнять операции дискового ввода-вывода каждый раз, когда им нужно получить доступ к метаданным.</span><span class="sxs-lookup"><span data-stu-id="393be-146">Other applications would rather cache all the metadata up front than keep the file stream open and perform disk I/O every time they need to access metadata.</span></span> <span data-ttu-id="393be-147">Если вызывающий объект не указывает параметр кэша метаданных, поведение кэширования по умолчанию должно кэшироваться по запросу.</span><span class="sxs-lookup"><span data-stu-id="393be-147">If the caller doesn’t specify a metadata cache option, the default caching behavior should be cache on demand.</span></span> <span data-ttu-id="393be-148">Это означает, что метаданные не должны загружаться в память до тех пор, пока приложение не выдает конкретный запрос для этих метаданных.</span><span class="sxs-lookup"><span data-stu-id="393be-148">This means no metadata should be loaded into memory until the application makes a specific request for that metadata.</span></span> <span data-ttu-id="393be-149">Если приложение указывает **WICDecodeMetadataCacheOnLoad**, метаданные должны загружаться в память немедленно и в кэше.</span><span class="sxs-lookup"><span data-stu-id="393be-149">If the application specifies **WICDecodeMetadataCacheOnLoad**, the metadata should be loaded in memory immediately and cached.</span></span> <span data-ttu-id="393be-150">При кэшировании метаданных при загрузке файловый поток может быть освобожден после кэширования метаданных.</span><span class="sxs-lookup"><span data-stu-id="393be-150">When metadata is cached on load, the file stream may be released after the metadata has been cached.</span></span>

### <a name="getcontainerformat"></a><span data-ttu-id="393be-151">жетконтаинерформат</span><span class="sxs-lookup"><span data-stu-id="393be-151">GetContainerFormat</span></span>

<span data-ttu-id="393be-152">Чтобы реализовать [**жетконтаинерформат**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcontainerformat), просто ВОЗВРАТИТЕ идентификатор GUID формата изображения, для которого создается экземпляр декодера.</span><span class="sxs-lookup"><span data-stu-id="393be-152">To implement [**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcontainerformat), just return the GUID of the image format of the image for which the decoder is instantiated.</span></span> <span data-ttu-id="393be-153">Этот метод также реализован в [**ивикметадатаблоккреадер**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) и [**ивикбитмапенкодер**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder).</span><span class="sxs-lookup"><span data-stu-id="393be-153">This method is also implemented on [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) and [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder).</span></span>

### <a name="getdecoderinfo"></a><span data-ttu-id="393be-154">жетдекодеринфо</span><span class="sxs-lookup"><span data-stu-id="393be-154">GetDecoderInfo</span></span>

<span data-ttu-id="393be-155">[**Жетдекодеринфо**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getdecoderinfo) возвращает объект [**ивикбитмапдекодеринфо**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoderinfo) .</span><span class="sxs-lookup"><span data-stu-id="393be-155">[**GetDecoderInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getdecoderinfo) returns an [**IWICBitmapDecoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoderinfo) object.</span></span> <span data-ttu-id="393be-156">Чтобы получить объект **ивикбитмапдекодеринфо** , просто передайте идентификатор GUID декодера в метод [**креатекомпонентинфо**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createcomponentinfo) в [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory), а затем запросите в нем интерфейс **ивикбитмапдекодеринфо** , как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="393be-156">To get the **IWICBitmapDecoderInfo** object, just pass the GUID of your decoder to the [**CreateComponentInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createcomponentinfo) method on [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory), and then request the **IWICBitmapDecoderInfo** interface on it, as shown in the following example.</span></span>


```C++
IWICComponentInfo* pComponentInfo = NULL;
HRESULT hr;
 
hr = m_pImagingFactory->CreateComponentInfo(CLSID_This, &pComponentInfo);

hr = pComponentInfo->QueryInterface(IID_IWICBitmapDecoderInfo, (void**)ppIDecoderInfo);

```



### <a name="getframecount"></a><span data-ttu-id="393be-157">жетфрамекаунт</span><span class="sxs-lookup"><span data-stu-id="393be-157">GetFrameCount</span></span>

<span data-ttu-id="393be-158">[**Жетфрамекаунт**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframecount) просто возвращает количество кадров в контейнере.</span><span class="sxs-lookup"><span data-stu-id="393be-158">[**GetFrameCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframecount) just returns the number of frames in the container.</span></span> <span data-ttu-id="393be-159">Некоторые форматы контейнеров поддерживают несколько кадров, а другие поддерживают только один кадр на контейнер.</span><span class="sxs-lookup"><span data-stu-id="393be-159">Some container formats support multiple frames, and others support only one frame per container.</span></span>

### <a name="getframe"></a><span data-ttu-id="393be-160">GetFrame</span><span class="sxs-lookup"><span data-stu-id="393be-160">GetFrame</span></span>

<span data-ttu-id="393be-161">Метод noframes является важным методом в интерфейсе [**ивикбитмапдекодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) , поскольку кадр содержит фактические биты изображения, а объект декодера кадров, возвращаемый этим методом [**, является объектом**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe) , который выполняет фактическое декодирование запрошенного изображения.</span><span class="sxs-lookup"><span data-stu-id="393be-161">[**GetFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe) is an important method on the [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) interface because the frame contains the actual image bits, and the frame decoder object returned from this method is the object that does the actual decoding of the requested image.</span></span> <span data-ttu-id="393be-162">Это другой объект, который необходимо реализовать при написании декодера.</span><span class="sxs-lookup"><span data-stu-id="393be-162">That is the other object you need to implement when writing a decoder.</span></span> <span data-ttu-id="393be-163">Дополнительные сведения о декодерах кадров см. в разделе [Реализация IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md).</span><span class="sxs-lookup"><span data-stu-id="393be-163">For more information on frame decoders, see [Implementing IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md).</span></span>

### <a name="getpreview"></a><span data-ttu-id="393be-164">Предварительная версия</span><span class="sxs-lookup"><span data-stu-id="393be-164">GetPreview</span></span>

<span data-ttu-id="393be-165">Функция [**OnPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) возвращает предварительный просмотр изображения.</span><span class="sxs-lookup"><span data-stu-id="393be-165">[**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) returns a preview of the image.</span></span> <span data-ttu-id="393be-166">Подробное описание предварительных версий см. в разделе [Реализация метода ивикбитмапенкодер](-wic-imp-iwicbitmapencoder.md) в [реализующем](-wic-imp-iwicbitmapencoder.md) интерфейсе ивикбитмапенкодер.</span><span class="sxs-lookup"><span data-stu-id="393be-166">For a detailed discussion of previews, see the [Implementing IWICBitmapEncoder](-wic-imp-iwicbitmapencoder.md) method on the [Implementing IWICBitmapEncoder](-wic-imp-iwicbitmapencoder.md) interface.</span></span>

<span data-ttu-id="393be-167">Если формат изображения содержит внедренный предварительный просмотр JPEG, настоятельно рекомендуется, чтобы вместо написания декодера JPEG для его декодирования вы делегирулись к декодеру JPEG, который поставляется вместе с платформой WIC для расшифровки предварительных версий и эскизов.</span><span class="sxs-lookup"><span data-stu-id="393be-167">If your image format contains an embedded JPEG preview, it is strongly recommend that, instead of writing a JPEG decoder to decode it, you delegate to the JPEG decoder that ships with the WIC platform for decoding previews and thumbnails.</span></span> <span data-ttu-id="393be-168">Для этого следует перейти к началу данных предварительного просмотра изображения в потоке и вызвать метод [**креатедекодерфромстреам**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) в [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory).</span><span class="sxs-lookup"><span data-stu-id="393be-168">To do this, seek to the beginning of the preview image data in the stream and invoke the [**CreateDecoderFromStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) method on the [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory).</span></span>


```C++
IWICBitmapDecoder* pPreviewDecoder = NULL;
IWICBitmapFrameDecode* pPreviewFrame = NULL;
IWICBitmapSource* pPreview = NULL;
HRESULT hr;

hr = m_pImagingFactory->CreateDecoderFromStream(
                               m_pStream, NULL, 
                               WICDecodeMetadataCacheOnDemand, &pPreviewDecoder);
hr = pPreviewDecoder->GetFrame(0, pPreviewFrame);
hr = pPreviewFrame->QueryInterface(IID_IWICBitmapSource, (void**)&pPreview);

```



## <a name="related-topics"></a><span data-ttu-id="393be-169">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="393be-169">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="393be-170">**Reference**</span><span class="sxs-lookup"><span data-stu-id="393be-170">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="393be-171">**ивикбитмапдекодер**</span><span class="sxs-lookup"><span data-stu-id="393be-171">**IWICBitmapDecoder**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)
</dt> <dt>

[<span data-ttu-id="393be-172">**IWICBitmapFrameDecode**</span><span class="sxs-lookup"><span data-stu-id="393be-172">**IWICBitmapFrameDecode**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)
</dt> <dt>

<span data-ttu-id="393be-173">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="393be-173">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="393be-174">Интерфейсы декодера</span><span class="sxs-lookup"><span data-stu-id="393be-174">Decoder Interfaces</span></span>](-wic-decoderinterfaces.md)
</dt> <dt>

[<span data-ttu-id="393be-175">Реализация Ивикбитмапкодекпрогресснотификатион (декодер)</span><span class="sxs-lookup"><span data-stu-id="393be-175">Implementing IWICBitmapCodecProgressNotification (Decoder)</span></span>](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md)
</dt> <dt>

[<span data-ttu-id="393be-176">Написание WIC-Enabled КОДЕка</span><span class="sxs-lookup"><span data-stu-id="393be-176">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="393be-177">Общие сведения о компоненте создания образов Windows</span><span class="sxs-lookup"><span data-stu-id="393be-177">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



