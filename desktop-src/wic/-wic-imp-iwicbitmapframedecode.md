---
description: Реализация IWICBitmapFrameDecode
ms.assetid: 7dc626ad-1158-4b67-8ca7-47b4cf88e278
title: Реализация IWICBitmapFrameDecode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 394b5858ec5eee37ef1c7f52b766806c4a0c1a92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816096"
---
# <a name="implementing-iwicbitmapframedecode"></a><span data-ttu-id="58773-103">Реализация IWICBitmapFrameDecode</span><span class="sxs-lookup"><span data-stu-id="58773-103">Implementing IWICBitmapFrameDecode</span></span>

## <a name="iwicbitmapframedecode"></a><span data-ttu-id="58773-104">IWICBitmapFrameDecode</span><span class="sxs-lookup"><span data-stu-id="58773-104">IWICBitmapFrameDecode</span></span>

<span data-ttu-id="58773-105">[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) — это интерфейс уровня кадров, предоставляющий доступ к реальным битам изображения.</span><span class="sxs-lookup"><span data-stu-id="58773-105">[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) is the frame-level interface that provides access to the actual image bits.</span></span> <span data-ttu-id="58773-106">Этот интерфейс реализуется для класса декодирования на уровне кадров.</span><span class="sxs-lookup"><span data-stu-id="58773-106">You implement this interface on your frame-level decoding class.</span></span> <span data-ttu-id="58773-107">Так как он является производным от [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource), ваша реализация **IWICBitmapFrameDecode** будет включать реализацию методов **IWICBitmapSource** .</span><span class="sxs-lookup"><span data-stu-id="58773-107">Because it’s derived from [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource), your implementation of **IWICBitmapFrameDecode** will include an implementation of the **IWICBitmapSource** methods.</span></span> <span data-ttu-id="58773-108">Дополнительные методы в **IWICBitmapFrameDecode** обеспечивают доступ к эскизу на уровне кадров, любому цветному контексту для изображения и считывателю запросов метаданных для рамки.</span><span class="sxs-lookup"><span data-stu-id="58773-108">The additional methods on **IWICBitmapFrameDecode** provide access to the frame-level thumbnail, any color contexts for the image, and the metadata query reader for the frame.</span></span>

``` syntax
interface IWICBitmapFrameDecode : IWICBitmapSource
{
// Required methods
HRESULT GetThumbnail ( IWICBitmapSource **ppIThumbnail );
HRESULT GetColorContexts ( UINT cCount, 
IWICColorContext **ppIColorContexts, UINT *pcActualCount );
HRESULT GetMetadataQueryReader ( IWICMetadataQueryReader **ppIMetadataQueryReader );

// Methods inherited from IWICBitmapSource
HRESULT GetSize ( UINT *puiWidth, UINT *puiHeight );
HRESULT GetPixelFormat ( WICPixelFormatGUID *pPixelFormat );
HRESULT GetResolution ( double *pDpiX, double *pDpiY );
HRESULT CopyPixels ( const WICRect *prc, 
   UINT cbStride,
   UINT cbBufferSize, 
   BYTE *pbBuffer );
// Optional method
HRESULT CopyPalette ( IWICPalette *pIPalette );
}
```

-   [<span data-ttu-id="58773-109">GetThumbnail</span><span class="sxs-lookup"><span data-stu-id="58773-109">GetThumbnail</span></span>](#getthumbnail)
-   [<span data-ttu-id="58773-110">жетколорконтекстс</span><span class="sxs-lookup"><span data-stu-id="58773-110">GetColorContexts</span></span>](#getcolorcontexts)
-   [<span data-ttu-id="58773-111">жетметадатакуериреадер</span><span class="sxs-lookup"><span data-stu-id="58773-111">GetMetadataQueryReader</span></span>](#getmetadataqueryreader)
-   [<span data-ttu-id="58773-112">Метод Жетпикселформат и метод.</span><span class="sxs-lookup"><span data-stu-id="58773-112">GetSize, GetPixelFormat, and GetResolution</span></span>](#getsize-getpixelformat-and-getresolution)
-   [<span data-ttu-id="58773-113">CopyPixels</span><span class="sxs-lookup"><span data-stu-id="58773-113">CopyPixels</span></span>](#copypixels)
-   [<span data-ttu-id="58773-114">копипалетте</span><span class="sxs-lookup"><span data-stu-id="58773-114">CopyPalette</span></span>](#copypalette)

### <a name="getthumbnail"></a><span data-ttu-id="58773-115">GetThumbnail</span><span class="sxs-lookup"><span data-stu-id="58773-115">GetThumbnail</span></span>

<span data-ttu-id="58773-116">Параметр " [**эскиз**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) " возвращает эскиз текущего кадра.</span><span class="sxs-lookup"><span data-stu-id="58773-116">[**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) returns the thumbnail for the current frame.</span></span> <span data-ttu-id="58773-117">По соображениям производительности эскизы чаще всего кодируются в формате JPEG.</span><span class="sxs-lookup"><span data-stu-id="58773-117">For performance reasons, thumbnails are most commonly encoded in a JPEG format.</span></span> <span data-ttu-id="58773-118">Точно так же, как и в предварительной версии декодера, не обязательно и не рекомендуется предоставлять собственный декодер JPEG для эскизов.</span><span class="sxs-lookup"><span data-stu-id="58773-118">Just as with the Preview on the decoder, it is not necessary or recommended to provide your own JPEG decoder for thumbnails.</span></span> <span data-ttu-id="58773-119">Вместо этого следует делегировать декодеру JPEG, предоставляемому компонентом Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="58773-119">Instead, you should delegate to the JPEG decoder provided by Windows Imaging Component (WIC).</span></span>

<span data-ttu-id="58773-120">Дополнительные сведения о эскизах см. в описании метода [сетсумбнаил](-wic-imp-iwicbitmapframeencode.md) для [реализации ивикбитмапфраминкоде](-wic-imp-iwicbitmapframeencode.md).</span><span class="sxs-lookup"><span data-stu-id="58773-120">For more information on thumbnails, see the [SetThumbnail](-wic-imp-iwicbitmapframeencode.md) method on [Implementing IWICBitmapFrameEncode](-wic-imp-iwicbitmapframeencode.md).</span></span>

### <a name="getcolorcontexts"></a><span data-ttu-id="58773-121">жетколорконтекстс</span><span class="sxs-lookup"><span data-stu-id="58773-121">GetColorContexts</span></span>

<span data-ttu-id="58773-122">[**Жетколорконтекстс**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts) возвращает допустимые контексты цвета (также известные как цветовые профили), связанные с изображением в этом кадре.</span><span class="sxs-lookup"><span data-stu-id="58773-122">[**GetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts) returns the valid color contexts (also known as color profiles) associated with the image in this frame.</span></span> <span data-ttu-id="58773-123">В большинстве случаев это будет только один, но бывают случаи, когда есть два или, редко и больше.</span><span class="sxs-lookup"><span data-stu-id="58773-123">In most cases, this will only be one, but there could be cases where there are two or, rarely, more.</span></span> <span data-ttu-id="58773-124">Вызывающий объект передаст один или несколько объектов [**ивикколорконтекст**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) , устанавливая параметр *учетная запись* , чтобы указать, сколько их передается.</span><span class="sxs-lookup"><span data-stu-id="58773-124">The caller will pass in one or more [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) objects, setting the *cCount* parameter to indicate how many they are passing in.</span></span> <span data-ttu-id="58773-125">Этот метод заполняет объекты **ивикколорконтекст** фактическими данными контекста цвета для цветовых профилей, связанных с изображением.</span><span class="sxs-lookup"><span data-stu-id="58773-125">This method populates the **IWICColorContext** objects with the actual color context data for the color profiles associated with the image.</span></span> <span data-ttu-id="58773-126">Задайте для параметра *пкактуалкаунт* фактическое количество цветовых контекстов, связанных с изображением, даже если оно больше числа, которое можно вернуть.</span><span class="sxs-lookup"><span data-stu-id="58773-126">Set the *pcActualCount* parameter to the actual number of color contexts associated with the image, even if this is greater than the number you can return.</span></span> <span data-ttu-id="58773-127">(В случае, если доступно больше контекстов, чем количество объектов **ивикколорконтекст** , переданных вызывающей стороной, это указывает вызывающей стороне, что есть доступ к одному или нескольким другим.)</span><span class="sxs-lookup"><span data-stu-id="58773-127">(In the case where more color contexts are available than the number of **IWICColorContext** objects passed in by the caller, this tells the caller there are one or more others available.)</span></span>

### <a name="getmetadataqueryreader"></a><span data-ttu-id="58773-128">жетметадатакуериреадер</span><span class="sxs-lookup"><span data-stu-id="58773-128">GetMetadataQueryReader</span></span>

<span data-ttu-id="58773-129">[**Жетметадатакуериреадер**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) возвращает [**ивикметадатакуериреадер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) , который приложение может использовать для получения метаданных из фрейма изображения.</span><span class="sxs-lookup"><span data-stu-id="58773-129">[**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) returns an [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) that an application can use to retrieve metadata from the image frame.</span></span> <span data-ttu-id="58773-130">Этот интерфейс реализуется обработчиком метаданных и позволяет приложению запрашивать определенные свойства метаданных, принадлежащие определенному формату метаданных.</span><span class="sxs-lookup"><span data-stu-id="58773-130">This interface is implemented by a metadata handler, and allows an application to query for specific metadata properties belonging to a particular metadata format.</span></span> <span data-ttu-id="58773-131">Дополнительные сведения см. в разделе [Реализация ивикметадатаблоккреадер](-wic-imp-iwicmetadatablockreader.md).</span><span class="sxs-lookup"><span data-stu-id="58773-131">For more information, see [Implementing IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md).</span></span>

<span data-ttu-id="58773-132">Чтобы создать экземпляр [**ивикметадатакуериреадер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader), вызовите [**креатекуериреадерфромблоккреадер**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createqueryreaderfromblockreader) в [**ивиккомпонентфактори**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory).</span><span class="sxs-lookup"><span data-stu-id="58773-132">To instantiate an [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader), call [**CreateQueryReaderFromBlockReader**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createqueryreaderfromblockreader) on the [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory).</span></span>


```C++
IWICMetadataQueryReader* pQueryReader = NULL;
HRESULT hr;

hr = m_pComponentFactory->CreateQueryReaderFromBlockReader( 
  static_cast<IWICMetadataBlockWriter*>(this),
  &pQueryReader);
```



### <a name="getsize-getpixelformat-and-getresolution"></a><span data-ttu-id="58773-133">Метод Жетпикселформат и метод.</span><span class="sxs-lookup"><span data-stu-id="58773-133">GetSize, GetPixelFormat, and GetResolution</span></span>

<span data-ttu-id="58773-134">Метод [**жетпикселформат**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getpixelformat) [**и метод**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getsize)- [**разрешение**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getresolution) говорят сами за себя и возвращают запрошенные свойства изображения.</span><span class="sxs-lookup"><span data-stu-id="58773-134">[**GetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getsize), [**GetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getpixelformat), and [**GetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getresolution) are self-explanatory, and return the requested properties of the image.</span></span>

### <a name="copypixels"></a><span data-ttu-id="58773-135">CopyPixels</span><span class="sxs-lookup"><span data-stu-id="58773-135">CopyPixels</span></span>

<span data-ttu-id="58773-136">[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) — это метод, который вызывается приложением, когда требуется создать точечный рисунок в памяти, который может быть визуализирован на дисплее или на принтере.</span><span class="sxs-lookup"><span data-stu-id="58773-136">[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) is the method an application calls when it wants to create a bitmap in memory that can be rendered to the display or printer.</span></span> <span data-ttu-id="58773-137">Это метод, который выполняет фактическое декодирование битов изображения.</span><span class="sxs-lookup"><span data-stu-id="58773-137">This is the method that does the actual decoding of the image bits.</span></span> <span data-ttu-id="58773-138">Параметры — это прямоугольник, который представляет область, представляющую интерес в исходном изображении для копирования в память; шаг, указывающий число байтов в одной строке просмотра; Размер буфера в памяти, выделенного приложением; и указатель на буфер, в который должны копироваться запрошенные биты изображения.</span><span class="sxs-lookup"><span data-stu-id="58773-138">The parameters are a rectangle, which represents the region of interest in the source image to copy into memory; the stride, which specifies the number of bytes in one scan line; the size of the buffer in memory that has been allocated by the application; and a pointer to the buffer into which the requested image bits should be copied.</span></span> <span data-ttu-id="58773-139">(Чтобы предотвратить потенциальные переполнения буфера от внедрения уязвимостей безопасности, необходимо скопировать в буфер только столько данных образа, сколько указывает параметр *кббуфферсизе* .)</span><span class="sxs-lookup"><span data-stu-id="58773-139">(To prevent potential buffer overruns from introducing security vulnerabilities, be sure to copy only as much image data into the buffer as the *cbBufferSize* parameter specifies.)</span></span>

### <a name="copypalette"></a><span data-ttu-id="58773-140">копипалетте</span><span class="sxs-lookup"><span data-stu-id="58773-140">CopyPalette</span></span>

<span data-ttu-id="58773-141">Только кодеки, имеющие Индексированные форматы пикселей, должны реализовывать метод [**копипалетте**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypalette) .</span><span class="sxs-lookup"><span data-stu-id="58773-141">Only codecs that have indexed pixel formats must implement the [**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypalette) method.</span></span> <span data-ttu-id="58773-142">Если изображение использует индексированный формат, используйте этот метод для возврата палитры цветов, используемых в изображении.</span><span class="sxs-lookup"><span data-stu-id="58773-142">If an image uses an indexed format, use this method to return the palette of colors used in the image.</span></span> <span data-ttu-id="58773-143">Если у кодека нет индексированного формата, возвратите ВИНКОДЕК \_ Err \_ палеттеунаваилабле.</span><span class="sxs-lookup"><span data-stu-id="58773-143">If your codec doesn’t have an indexed format, return WINCODEC\_ERR\_PALETTEUNAVAILABLE.</span></span>

## <a name="related-topics"></a><span data-ttu-id="58773-144">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="58773-144">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="58773-145">**Reference**</span><span class="sxs-lookup"><span data-stu-id="58773-145">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="58773-146">**IWICBitmapSource**</span><span class="sxs-lookup"><span data-stu-id="58773-146">**IWICBitmapSource**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)
</dt> <dt>

[<span data-ttu-id="58773-147">**ивикбитмапдекодер**</span><span class="sxs-lookup"><span data-stu-id="58773-147">**IWICBitmapDecoder**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)
</dt> <dt>

[<span data-ttu-id="58773-148">**IWICBitmapFrameDecode**</span><span class="sxs-lookup"><span data-stu-id="58773-148">**IWICBitmapFrameDecode**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)
</dt> <dt>

<span data-ttu-id="58773-149">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="58773-149">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="58773-150">Реализация IWICBitmapSource</span><span class="sxs-lookup"><span data-stu-id="58773-150">Implementing IWICBitmapSource</span></span>](-wic-imp-iwicbitmapsource.md)
</dt> <dt>

[<span data-ttu-id="58773-151">Реализация Ивикметадатаблоккреадер</span><span class="sxs-lookup"><span data-stu-id="58773-151">Implementing IWICMetadataBlockReader</span></span>](-wic-imp-iwicmetadatablockreader.md)
</dt> <dt>

[<span data-ttu-id="58773-152">Написание WIC-Enabled КОДЕка</span><span class="sxs-lookup"><span data-stu-id="58773-152">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="58773-153">Общие сведения о компоненте создания образов Windows</span><span class="sxs-lookup"><span data-stu-id="58773-153">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



