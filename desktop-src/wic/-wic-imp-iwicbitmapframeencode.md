---
description: Реализация Ивикбитмапфраминкоде
ms.assetid: 509fa49c-c90d-4270-a338-6ce638ccd89a
title: Реализация Ивикбитмапфраминкоде
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5d2a5ea0412ea4a45ea329618d00443c1755391
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265863"
---
# <a name="implementing-iwicbitmapframeencode"></a><span data-ttu-id="06c5e-103">Реализация Ивикбитмапфраминкоде</span><span class="sxs-lookup"><span data-stu-id="06c5e-103">Implementing IWICBitmapFrameEncode</span></span>

## <a name="iwicbitmapframeencode"></a><span data-ttu-id="06c5e-104">ивикбитмапфраминкоде</span><span class="sxs-lookup"><span data-stu-id="06c5e-104">IWICBitmapFrameEncode</span></span>

<span data-ttu-id="06c5e-105">[**Ивикбитмапфраминкоде**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) — это аналог кодировщика для интерфейса [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) .</span><span class="sxs-lookup"><span data-stu-id="06c5e-105">[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) is the encoder’s counterpart to the [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) interface.</span></span> <span data-ttu-id="06c5e-106">Этот интерфейс можно реализовать для класса кодирования на уровне кадров, который представляет собой класс, который выполняет фактическую кодировку битов изображения для каждого кадра.</span><span class="sxs-lookup"><span data-stu-id="06c5e-106">You can implement this interface on your frame-level encoding class, which is the class that does the actual encoding of the image bits for each frame.</span></span>


```C++
interface IWICBitmapFrameEncode : public IUnknown
{
   // Required methods
   HRESULT Initialize ( IPropertyBag2 *pIEncoderOptions );
   HRESULT SetSize ( UINT width,
               UINT height );
   HRESULT SetResolution ( double dpiX,
               double dpiY );
   HRESULT SetPixelFormat (WICPixelFormatGUID *pPixelFormat);
   HRESULT SetColorContexts ( UINT cCount,
               IWICColorContext **ppIColorContext );
   HRESULT GetMetadataQueryWriter ( IWICMetadataQueryWriter 
               **ppIMetadataQueryWriter );
   HRESULT SetThumbnail ( IWICBitmapSource *pIThumbnail );
   HRESULT WritePixels ( UINT lineCount,
               UINT cbStride,
               UINT cbBufferSize,
               BYTE *pbPixels );
   HRESULT WriteSource ( IWICBitmapSource *pIWICBitmapSource,
               WICRect *prc );
   HRESULT Commit ( void );

// Optional method
   HRESULT SetPalette ( IWICPalette *pIPalette );
};
```



-   [<span data-ttu-id="06c5e-107">Инициализация</span><span class="sxs-lookup"><span data-stu-id="06c5e-107">Initialize</span></span>](#initialize)
-   [<span data-ttu-id="06c5e-108">SetSize и Сетресолутион</span><span class="sxs-lookup"><span data-stu-id="06c5e-108">SetSize and SetResolution</span></span>](#setsize-and-setresolution)
-   [<span data-ttu-id="06c5e-109">сетпикселформат</span><span class="sxs-lookup"><span data-stu-id="06c5e-109">SetPixelFormat</span></span>](#setpixelformat)
-   [<span data-ttu-id="06c5e-110">сетколорконтекстс</span><span class="sxs-lookup"><span data-stu-id="06c5e-110">SetColorContexts</span></span>](#setcolorcontexts)
-   [<span data-ttu-id="06c5e-111">жетметадатакуеривритер</span><span class="sxs-lookup"><span data-stu-id="06c5e-111">GetMetadataQueryWriter</span></span>](#getmetadataquerywriter)
-   [<span data-ttu-id="06c5e-112">сетсумбнаил</span><span class="sxs-lookup"><span data-stu-id="06c5e-112">SetThumbnail</span></span>](#setthumbnail)
-   [<span data-ttu-id="06c5e-113">WritePixels</span><span class="sxs-lookup"><span data-stu-id="06c5e-113">WritePixels</span></span>](#writepixels)
-   [<span data-ttu-id="06c5e-114">вритесаурце</span><span class="sxs-lookup"><span data-stu-id="06c5e-114">WriteSource</span></span>](#writesource)
-   [<span data-ttu-id="06c5e-115">Фиксация</span><span class="sxs-lookup"><span data-stu-id="06c5e-115">Commit</span></span>](#commit)
-   [<span data-ttu-id="06c5e-116">сетпалетте</span><span class="sxs-lookup"><span data-stu-id="06c5e-116">SetPalette</span></span>](#setpalette)

### <a name="initialize"></a><span data-ttu-id="06c5e-117">Инициализация</span><span class="sxs-lookup"><span data-stu-id="06c5e-117">Initialize</span></span>

<span data-ttu-id="06c5e-118">[**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-initialize) — это первый метод, вызываемый для объекта [**ивикбитмапфраминкоде**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) после создания экземпляра.</span><span class="sxs-lookup"><span data-stu-id="06c5e-118">[**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-initialize) is the first method invoked on an [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object after it has been instantiated.</span></span> <span data-ttu-id="06c5e-119">Этот метод имеет один параметр, который может иметь значение **null**.</span><span class="sxs-lookup"><span data-stu-id="06c5e-119">This method has one parameter, which may be set to **NULL**.</span></span> <span data-ttu-id="06c5e-120">Этот параметр представляет параметры кодировщика и является тем же экземпляром [IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) , который был создан в методе [**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) в декодере на уровне контейнера, и передается обратно вызывающему объекту в параметре пиенкодероптионс этого метода.</span><span class="sxs-lookup"><span data-stu-id="06c5e-120">This parameter represents the encoder options, and is the same [IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) instance that you created in the [**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) method on the container-level decoder, and passed back to the caller in the pIEncoderOptions parameter of that method.</span></span> <span data-ttu-id="06c5e-121">В это время вы заполнили структуру IPropertyBag2 свойствами, которые представляют параметры кодирования, поддерживаемые кодировщиком на уровне кадров.</span><span class="sxs-lookup"><span data-stu-id="06c5e-121">At that time, you populated the IPropertyBag2 struct with properties that represent the encoding options supported by your frame-level encoder.</span></span> <span data-ttu-id="06c5e-122">Теперь вызывающий объект предоставил значения для этих свойств, чтобы указать определенные параметры параметров кодировки, и передает один и тот же объект обратно в инициализацию объекта **ивикбитмапфраминкоде** .</span><span class="sxs-lookup"><span data-stu-id="06c5e-122">The caller has now provided values for those properties to indicate certain encoding option parameters, and is passing the same object back to you to initialize the **IWICBitmapFrameEncode** object.</span></span> <span data-ttu-id="06c5e-123">При кодировании битов изображения следует применять указанные параметры.</span><span class="sxs-lookup"><span data-stu-id="06c5e-123">You should apply the specified options when encoding the image bits.</span></span>

### <a name="setsize-and-setresolution"></a><span data-ttu-id="06c5e-124">SetSize и Сетресолутион</span><span class="sxs-lookup"><span data-stu-id="06c5e-124">SetSize and SetResolution</span></span>

<span data-ttu-id="06c5e-125">[**SetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setsize) и [**сетресолутион**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setresolution) говорят сами за себя.</span><span class="sxs-lookup"><span data-stu-id="06c5e-125">[**SetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setsize) and [**SetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setresolution) are self-explanatory.</span></span> <span data-ttu-id="06c5e-126">Вызывающий объект использует эти методы для указания размера и разрешения закодированного изображения.</span><span class="sxs-lookup"><span data-stu-id="06c5e-126">The caller uses these methods to specify the size and resolution for the encoded image.</span></span>

### <a name="setpixelformat"></a><span data-ttu-id="06c5e-127">сетпикселформат</span><span class="sxs-lookup"><span data-stu-id="06c5e-127">SetPixelFormat</span></span>

<span data-ttu-id="06c5e-128">[**Сетпикселформат**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setpixelformat) используется для запроса формата пикселей, в котором кодируется изображение.</span><span class="sxs-lookup"><span data-stu-id="06c5e-128">[**SetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setpixelformat) is used to request a pixel format in which to encode the image.</span></span> <span data-ttu-id="06c5e-129">Если запрошенный формат пикселей не поддерживается, следует вернуть идентификатор GUID ближайшего формата пикселей, поддерживаемого в *ппикселформат*, который является параметром in/out.</span><span class="sxs-lookup"><span data-stu-id="06c5e-129">If the requested pixel format is not supported, you should return the GUID of the closest pixel format that is supported in *pPixelFormat*, which is an in/out parameter.</span></span>

### <a name="setcolorcontexts"></a><span data-ttu-id="06c5e-130">сетколорконтекстс</span><span class="sxs-lookup"><span data-stu-id="06c5e-130">SetColorContexts</span></span>

<span data-ttu-id="06c5e-131">[**Сетколорконтекстс**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setcolorcontexts) используется для указания одного или нескольких допустимых контекстов цвета (также известных как цветовые профили) для этого изображения.</span><span class="sxs-lookup"><span data-stu-id="06c5e-131">[**SetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setcolorcontexts) is used to specify one or more valid color contexts (also known as color profiles) for this image.</span></span> <span data-ttu-id="06c5e-132">Важно указать контексты цвета, поэтому приложение, которое будет декодировать образ в дальнейшем, может преобразовать исходный цветовой профиль в целевой профиль устройства, используемого для отображения или печати изображения.</span><span class="sxs-lookup"><span data-stu-id="06c5e-132">It’s important to specify the color contexts, so an application that decodes the image at a later time can convert from the source color profile to the destination profile of the device being used to display or print the image.</span></span> <span data-ttu-id="06c5e-133">Без цветового профиля невозможно получить согласованные цвета на разных устройствах.</span><span class="sxs-lookup"><span data-stu-id="06c5e-133">Without a color profile, it is not possible to get consistent colors across different devices.</span></span> <span data-ttu-id="06c5e-134">Это может оказаться неприятной для конечных пользователей, когда фотографии выглядят по-разному на разных мониторах, и они не могут получить печать в соответствии с отображаемыми на экране.</span><span class="sxs-lookup"><span data-stu-id="06c5e-134">This can be frustrating for end users when their photos look different on different monitors, and they can’t get the prints to match what they see on screen.</span></span>

### <a name="getmetadataquerywriter"></a><span data-ttu-id="06c5e-135">жетметадатакуеривритер</span><span class="sxs-lookup"><span data-stu-id="06c5e-135">GetMetadataQueryWriter</span></span>

<span data-ttu-id="06c5e-136">[**Жетметадатакуеривритер**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) возвращает [**ивикметадатакуеривритер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) , который приложение может использовать для вставки или изменения конкретных свойств метаданных в блоке метаданных в кадре изображения.</span><span class="sxs-lookup"><span data-stu-id="06c5e-136">[**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) returns an [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) that an application can use to insert or edit specific metadata properties in a metadata block on the image frame.</span></span>

<span data-ttu-id="06c5e-137">Создать экземпляр [**ивикметадатакуеривритер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) из [**ивиккомпонентфактори**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) можно несколькими способами.</span><span class="sxs-lookup"><span data-stu-id="06c5e-137">You can instantiate an [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) from the [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) in several ways.</span></span> <span data-ttu-id="06c5e-138">Вы можете создать его из [**ивикметадатаблокквритер**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter), так же как [**ивикметадатакуериреадер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) был создан из [**ивикметадатаблоккреадер**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) в методе [**жетметадатакуериреадер**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) в интерфейсе [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) .</span><span class="sxs-lookup"><span data-stu-id="06c5e-138">You can either create it from your [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter), the same way [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) was created from an [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) in the [**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) method on the [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) interface.</span></span>


```C++
IWICMetadataQueryWriter* piMetadataQueryWriter = NULL;
HRESULT hr;

hr = m_piComponentFactory->CreateQueryWriterFromBlockWriter( 
      static_cast<IWICMetadataBlockWriter*>(this), 
      &piMetadataQueryWriter);

```



<span data-ttu-id="06c5e-139">Его также можно создать из существующего [**ивикметадатакуериреадер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader), например, полученного с помощью предыдущего метода.</span><span class="sxs-lookup"><span data-stu-id="06c5e-139">You can also create it from an existing [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader), such as the one obtained using the previous method.</span></span>


```C++
hr = m_piComponentFactory->CreateQueryWriterFromReader( 
      piMetadataQueryReader, pguidVendor, &piMetadataQueryWriter);
```



<span data-ttu-id="06c5e-140">Параметр *пгуидвендор* позволяет указать конкретного поставщика, который должен использовать модуль записи запросов при создании экземпляра модуля записи метаданных.</span><span class="sxs-lookup"><span data-stu-id="06c5e-140">The *pguidVendor* parameter allows you to specify a particular vendor for the query writer to use when instantiating a metadata writer.</span></span> <span data-ttu-id="06c5e-141">Например, при предоставлении собственных модулей записи метаданных может потребоваться указать собственный идентификатор GUID поставщика.</span><span class="sxs-lookup"><span data-stu-id="06c5e-141">For example, if you provide your own metadata writers, you may want to specify your own vendor GUID.</span></span> <span data-ttu-id="06c5e-142">Если у вас нет предпочтений, в этот параметр можно передать **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="06c5e-142">You can pass **NULL** to this parameter if you don’t have a preference.</span></span>

### <a name="setthumbnail"></a><span data-ttu-id="06c5e-143">сетсумбнаил</span><span class="sxs-lookup"><span data-stu-id="06c5e-143">SetThumbnail</span></span>

<span data-ttu-id="06c5e-144">[**Сетсумбнаил**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail) используется для создания эскиза.</span><span class="sxs-lookup"><span data-stu-id="06c5e-144">[**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail) is used to provide a thumbnail.</span></span> <span data-ttu-id="06c5e-145">Все изображения должны предоставлять эскизы глобально, в каждом фрейме или в обоих кадрах.</span><span class="sxs-lookup"><span data-stu-id="06c5e-145">All images should provide a thumbnail either globally, on each frame, or both.</span></span> <span data-ttu-id="06c5e-146">Методы  WebMethod и **сетсумбнаил** являются необязательными на уровне контейнера, но, если кодек возвращает винкодек \_ Err \_ Кодекносумбнаил из метода, [](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) компонент Windows Imaging Component (WIC) вызовет метод для кадра 0 [](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) .</span><span class="sxs-lookup"><span data-stu-id="06c5e-146">The **GetThumbnail** and **SetThumbnail** methods are optional at the container-level but, if a codec returns WINCODEC\_ERR\_CODECNOTHUMBNAIL from the [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) method, Windows Imaging Component (WIC) will invoke the [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) method for Frame 0.</span></span> <span data-ttu-id="06c5e-147">Если в любом месте эскиз не найден, компонент WIC должен декодировать полное изображение и масштабировать его до размера эскиза, что может привести к значительному снижению производительности для больших изображений.</span><span class="sxs-lookup"><span data-stu-id="06c5e-147">If no thumbnail is found in either place, WIC must decode the full image and scale it to thumbnail size, which could incur a large performance penalty for larger images.</span></span>

<span data-ttu-id="06c5e-148">Эскиз должен иметь размер и разрешение, что позволяет быстро декодировать и отображать их.</span><span class="sxs-lookup"><span data-stu-id="06c5e-148">The thumbnail should be of a size and resolution that makes it quick to decode and display.</span></span> <span data-ttu-id="06c5e-149">По этой причине эскизы — это наиболее распространенные изображения JPEG.</span><span class="sxs-lookup"><span data-stu-id="06c5e-149">For this reason, thumbnails are most commonly JPEG images.</span></span> <span data-ttu-id="06c5e-150">Обратите внимание, что при использовании JPEG для эскизов вам не нужно писать кодировщик JPEG для их кодирования или декодер JPEG для декодирования.</span><span class="sxs-lookup"><span data-stu-id="06c5e-150">Note that, if you use JPEG for your thumbnails, you don’t have to write a JPEG encoder to encode them, or a JPEG decoder to decode them.</span></span> <span data-ttu-id="06c5e-151">Всегда следует делегировать кодеку JPEG, поставляемому с платформой WIC, для кодирования и декодирования эскизов.</span><span class="sxs-lookup"><span data-stu-id="06c5e-151">You should always delegate to the JPEG codec that ships with the WIC platform for encoding and decoding thumbnails.</span></span>

### <a name="writepixels"></a><span data-ttu-id="06c5e-152">WritePixels</span><span class="sxs-lookup"><span data-stu-id="06c5e-152">WritePixels</span></span>

<span data-ttu-id="06c5e-153">[**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels) — это метод, используемый для передачи строк просмотра из точечного рисунка в памяти для кодирования.</span><span class="sxs-lookup"><span data-stu-id="06c5e-153">[**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels) is the method used to pass in scan lines from a bitmap in memory for encoding.</span></span> <span data-ttu-id="06c5e-154">Метод будет вызываться повторно до тех пор, пока не будут переданы все строки просмотра.</span><span class="sxs-lookup"><span data-stu-id="06c5e-154">The method will be called repeatedly until all of the scan lines have been passed in.</span></span> <span data-ttu-id="06c5e-155">Параметр *линекаунт* указывает, сколько строк проверки должно быть написано в этом вызове.</span><span class="sxs-lookup"><span data-stu-id="06c5e-155">The *lineCount* parameter indicates how many scan lines are to be written in this call.</span></span> <span data-ttu-id="06c5e-156">Параметр *кбстриде* указывает число байтов на каждую строку развертки.</span><span class="sxs-lookup"><span data-stu-id="06c5e-156">The *cbStride* parameter indicates the number of bytes per scan line.</span></span> <span data-ttu-id="06c5e-157">*кббуфферсизе* указывает размер буфера, переданного в параметре пбпикселс, который содержит фактические биты изображения для кодирования.</span><span class="sxs-lookup"><span data-stu-id="06c5e-157">*cbBufferSize* indicates the size of the buffer passed in the pbPixels parameter, which contains the actual image bits to be encoded.</span></span> <span data-ttu-id="06c5e-158">Если Объединенная высота строк просмотра из совокупных вызовов превышает высоту, указанную в методе [**SetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setsize) , то возвращается винкодек \_ Err \_ туманисканлинес.</span><span class="sxs-lookup"><span data-stu-id="06c5e-158">If the combined height of the scan lines from cumulative calls is greater than the height specified in [**SetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setsize) method, return WINCODEC\_ERR\_TOOMANYSCANLINES.</span></span>

<span data-ttu-id="06c5e-159">Если [**викбитмапенкодеркачеоптион**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapencodercacheoption) имеет значение **викбитмапенкодеркачеинмемори**, строки просмотра должны быть помещены в кэш в памяти до тех пор, пока не будут переданы все строки проверки.</span><span class="sxs-lookup"><span data-stu-id="06c5e-159">When the [**WICBitmapEncoderCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapencodercacheoption) is **WICBitmapEncoderCacheInMemory**, the scan lines should be cached in memory until all scan lines have been passed in.</span></span> <span data-ttu-id="06c5e-160">Если параметр кэша кодировщика имеет значение **викбитмапенкодеркачетемпфиле**, строки просмотра должны кэшироваться во временном файле, созданном при инициализации объекта.</span><span class="sxs-lookup"><span data-stu-id="06c5e-160">If the encoder cache option is **WICBitmapEncoderCacheTempFile**, the scan lines should be cached in a temporary file, created when initializing the object.</span></span> <span data-ttu-id="06c5e-161">В любом из этих случаев образ не должен кодироваться до тех пор, пока вызывающий объект не вызовет [**commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit).</span><span class="sxs-lookup"><span data-stu-id="06c5e-161">In either of these cases, the image should not be encoded until the caller calls [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit).</span></span> <span data-ttu-id="06c5e-162">Если параметр Cache имеет значение **викбитмапенкодернокаче**, кодировщик должен по возможности кодировать строки сканирования по мере их получения.</span><span class="sxs-lookup"><span data-stu-id="06c5e-162">In the case where the cache option is **WICBitmapEncoderNoCache**, the encoder should encode the scan lines as they’re received, if possible.</span></span> <span data-ttu-id="06c5e-163">(В некоторых форматах это невозможно, и строки просмотра должны быть кэшированы до тех пор, пока не будет вызвана фиксация.)</span><span class="sxs-lookup"><span data-stu-id="06c5e-163">(In some formats, this is not possible, and the scan lines must be cached until Commit is called.)</span></span>

<span data-ttu-id="06c5e-164">Большинство необработанных кодеков не реализуют [**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels), так как они не поддерживают изменение битов изображения в необработанном файле.</span><span class="sxs-lookup"><span data-stu-id="06c5e-164">Most raw codecs will not implement [**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels), because they don’t support altering the image bits in the raw file.</span></span> <span data-ttu-id="06c5e-165">Однако необработанные кодеки должны по-прежнему реализовывать **WritePixels**, но, поскольку при добавлении метаданных размер файла может увеличиться, при этом файл должен быть переписан на диске.</span><span class="sxs-lookup"><span data-stu-id="06c5e-165">Raw codecs should still implement **WritePixels**, however, because when metadata is added, it may increase the size of the file, requiring the file to be rewritten on the disk.</span></span> <span data-ttu-id="06c5e-166">В этом случае необходимо иметь возможность копировать существующие биты образа, что делает метод **WritePixels** .</span><span class="sxs-lookup"><span data-stu-id="06c5e-166">In that case, it’s necessary to be able to copy the existing image bits, which is what the **WritePixels** method does.</span></span>

### <a name="writesource"></a><span data-ttu-id="06c5e-167">вритесаурце</span><span class="sxs-lookup"><span data-stu-id="06c5e-167">WriteSource</span></span>

<span data-ttu-id="06c5e-168">[**Вритесаурце**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) используется для кодирования объекта [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) .</span><span class="sxs-lookup"><span data-stu-id="06c5e-168">[**WriteSource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) is used to encode an [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) object.</span></span> <span data-ttu-id="06c5e-169">Первый параметр является указателем на объект **IWICBitmapSource** .</span><span class="sxs-lookup"><span data-stu-id="06c5e-169">The first parameter is a pointer to an **IWICBitmapSource** object.</span></span> <span data-ttu-id="06c5e-170">Второй параметр — это Викрект, указывающий интересующую область.</span><span class="sxs-lookup"><span data-stu-id="06c5e-170">The second parameter is a WICRect that specifies the region of interest to encode.</span></span> <span data-ttu-id="06c5e-171">Этот метод может вызываться несколько раз подряд, если ширина каждого прямоугольника равна ширине окончательного изображения для кодирования.</span><span class="sxs-lookup"><span data-stu-id="06c5e-171">This method may be called multiple times in succession, as long as the width of each rectangle is the same width of the final image to be encoded.</span></span> <span data-ttu-id="06c5e-172">Если ширина прямоугольника, переданного в параметре PRC, отличается от ширины, указанной в методе SetSize, то возвращается ВИНКОДЕК \_ Err \_ саурцеректдоеснотматчдименсионс.</span><span class="sxs-lookup"><span data-stu-id="06c5e-172">If the width of the rectangle passed in the prc parameter is different than the width specified in the SetSize method, return WINCODEC\_ERR\_SOURCERECTDOESNOTMATCHDIMENSIONS.</span></span> <span data-ttu-id="06c5e-173">Если Объединенная высота строк просмотра из совокупных вызовов превышает высоту, указанную в методе SetSize, то возвращается ВИНКОДЕК \_ Err \_ туманисканлинес.</span><span class="sxs-lookup"><span data-stu-id="06c5e-173">If the combined height of the scan lines from cumulative calls is greater than the height specified in SetSize method, return WINCODEC\_ERR\_TOOMANYSCANLINES.</span></span>

<span data-ttu-id="06c5e-174">Параметры кэширования работают так же, как и метод [**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels) , описанный ранее.</span><span class="sxs-lookup"><span data-stu-id="06c5e-174">The cache options work the same way with this method as with the [**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels) method described previously.</span></span>

### <a name="commit"></a><span data-ttu-id="06c5e-175">Commit</span><span class="sxs-lookup"><span data-stu-id="06c5e-175">Commit</span></span>

<span data-ttu-id="06c5e-176">[**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) — это метод, который сериализует закодированные биты изображения в файловый поток и выполняет перебор всех модулей записи метаданных для фрейма, запрашивающего их, для сериализации своих метаданных в поток.</span><span class="sxs-lookup"><span data-stu-id="06c5e-176">[**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) is the method that serializes the encoded image bits to the file stream, and iterates through all the metadata writers for the frame requesting them to serialize their metadata to the stream.</span></span> <span data-ttu-id="06c5e-177">В случае, когда параметр кэша кодировщика имеет значение Викбитмапенкодеркачеинмемори или Викбитмапенкодеркачетемпфиле, этот метод также отвечает за кодирование изображения, а если параметр Cache имеет значение Викбитмапенкодеркачетемпфиле, то метод **commit** также должен удалить временный файл, используемый для кэширования данных изображения перед кодированием.</span><span class="sxs-lookup"><span data-stu-id="06c5e-177">In the case where the encoder cache option is WICBitmapEncoderCacheInMemory or WICBitmapEncoderCacheTempFile, this method is also responsible for encoding the image, and when the cache option is WICBitmapEncoderCacheTempFile, the **Commit** method should also delete the temporary file used to cache the image data before encoding.</span></span>

<span data-ttu-id="06c5e-178">Этот метод всегда вызывается после передачи всех строк просмотра или прямоугольников, составляющих изображение, с помощью метода [**commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) или [**вритесаурце**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) .</span><span class="sxs-lookup"><span data-stu-id="06c5e-178">This method is always invoked after all the scan lines or rectangles that make up the image have been passed in using either the [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) or [**WriteSource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) method.</span></span> <span data-ttu-id="06c5e-179">Размер завершающего прямоугольника, состоящего из накопленных вызовов WritePixels или Вритесаурце, должен иметь тот же размер, что и в методе SetSize.</span><span class="sxs-lookup"><span data-stu-id="06c5e-179">The size of the final rectangle that is composed through the accumulated calls to WritePixels or WriteSource must be the same size as was specified in the SetSize method.</span></span> <span data-ttu-id="06c5e-180">Если размер не соответствует ожидаемому размеру, этот метод должен возвращать ВИНКОДЕЦЕРРОР \_ унекспектедсизе.</span><span class="sxs-lookup"><span data-stu-id="06c5e-180">If the size does not match the expected size, this method should return WINCODECERROR\_UNEXPECTEDSIZE.</span></span>

<span data-ttu-id="06c5e-181">Чтобы выполнить итерацию модулей записи метаданных и сообщить каждому модулю записи метаданных о необходимости сериализации своих метаданных, необходимо вызвать Жетвритербиндекс для прохода по модулям записи для каждого блока и вызвать Ивикперсистстреам. Save в каждом модуле записи метаданных.</span><span class="sxs-lookup"><span data-stu-id="06c5e-181">To iterate through the metadata writers and tell each metadata writer to serialize its metadata go the stream, invoke GetWriterByIndex to iterate through the writers for each block, and invoke IWICPersistStream.Save on each metadata writer.</span></span>


```C++
IWICMetadataWriter* piMetadataWRiter = NULL;
IWICPersistStream* piPersistStream = NULL;
HRESULT hr;

for (UINT x=0; x < m_blockCount; x++) 
{
    hr = GetWriterByIndex(x, & piMetadataWriter);
hr = piMetadataWriter->QueryInterface(
IID_IWICPersistStream,(void**)&piPersistStream);

hr = piPersistStream->Save(m_piStream, 
WICPersistOptions.WicPersistOptionDefault, 
true);
...
}
```



### <a name="setpalette"></a><span data-ttu-id="06c5e-182">сетпалетте</span><span class="sxs-lookup"><span data-stu-id="06c5e-182">SetPalette</span></span>

<span data-ttu-id="06c5e-183">Только кодеки, имеющие Индексированные форматы, должны реализовывать метод [**сетпалетте**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setpalette) .</span><span class="sxs-lookup"><span data-stu-id="06c5e-183">Only codecs that have indexed formats need to implement the [**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setpalette) method.</span></span> <span data-ttu-id="06c5e-184">Если изображение использует индексированный формат, используйте этот метод для указания палитры цветов, используемых в изображении.</span><span class="sxs-lookup"><span data-stu-id="06c5e-184">If an image uses an indexed format, use this method to specify the palette of colors used in the image.</span></span> <span data-ttu-id="06c5e-185">Если у кодека нет индексированного формата, возвратите ВИНКОДЕК \_ Err \_ палеттеунаваилабле из этого метода.</span><span class="sxs-lookup"><span data-stu-id="06c5e-185">If your codec doesn’t have an indexed format, return WINCODEC\_ERR\_PALETTEUNAVAILABLE from this method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="06c5e-186">См. также</span><span class="sxs-lookup"><span data-stu-id="06c5e-186">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="06c5e-187">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="06c5e-187">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="06c5e-188">Реализация Ивикбитмапкодекпрогресснотификатион (кодировщик)</span><span class="sxs-lookup"><span data-stu-id="06c5e-188">Implementing IWICBitmapCodecProgressNotification (Encoder)</span></span>](-wic-imp-iwicbitmapcodecprogressnotification-encoder.md)
</dt> <dt>

[<span data-ttu-id="06c5e-189">Реализация Ивикметадатаблокквритер</span><span class="sxs-lookup"><span data-stu-id="06c5e-189">Implementing IWICMetadataBlockWriter</span></span>](-wic-imp-iwicmetadatablockwriter.md)
</dt> <dt>

[<span data-ttu-id="06c5e-190">Написание WIC-Enabled КОДЕка</span><span class="sxs-lookup"><span data-stu-id="06c5e-190">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="06c5e-191">Общие сведения о компоненте создания образов Windows</span><span class="sxs-lookup"><span data-stu-id="06c5e-191">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
