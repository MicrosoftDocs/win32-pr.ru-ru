---
description: Реализация Ивикбитмапсаурцетрансформ
ms.assetid: 6a3e682c-55c6-4728-9d14-5eb0290f3dcc
title: Реализация Ивикбитмапсаурцетрансформ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0809e1e56fe3c05c8803bb70106c4a24a466eafe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347185"
---
# <a name="implementing-iwicbitmapsourcetransform"></a><span data-ttu-id="f3a3d-103">Реализация Ивикбитмапсаурцетрансформ</span><span class="sxs-lookup"><span data-stu-id="f3a3d-103">Implementing IWICBitmapSourceTransform</span></span>

## <a name="iwicbitmapsourcetransform"></a><span data-ttu-id="f3a3d-104">ивикбитмапсаурцетрансформ</span><span class="sxs-lookup"><span data-stu-id="f3a3d-104">IWICBitmapSourceTransform</span></span>

<span data-ttu-id="f3a3d-105">Хотя это необязательно, настоятельно рекомендуется, чтобы каждый декодер реализовал этот интерфейс для класса декодирования на уровне кадров, так как он может предоставить значительные преимущества для повышения производительности.</span><span class="sxs-lookup"><span data-stu-id="f3a3d-105">Though optional, we highly recommend that every decoder implement this interface on your frame-level decoding class, because it can provide major performance benefits.</span></span> <span data-ttu-id="f3a3d-106">Когда приложение запрашивает конкретный регион, размер, ориентацию или формат пикселей, вместо простого декодирования всего изображения при полном разрешении и последующего применения запрошенных преобразований компонент Windows Imaging Component (WIC) вызывает [IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) для этого интерфейса в объекте [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) .</span><span class="sxs-lookup"><span data-stu-id="f3a3d-106">When an application requests a specific region of interest, size, orientation, or pixel format, instead of just decoding the whole image at full resolution and then applying the requested transforms, Windows Imaging Component (WIC) calls [IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) for this interface on the [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) object.</span></span> <span data-ttu-id="f3a3d-107">Если декодер кадров поддерживает его, то WIC вызывает соответствующий метод или методы, чтобы определить, может ли декодер кадров выполнить запрошенное преобразование, или определить ближайший размер или формат пикселей, который декодер может предоставить для запрошенного.</span><span class="sxs-lookup"><span data-stu-id="f3a3d-107">If the frame decoder supports it, WIC calls the appropriate method or methods to determine whether the frame decoder can perform the requested transform or determine the closest size or pixel format the decoder can provide to the one requested.</span></span> <span data-ttu-id="f3a3d-108">Если декодер может выполнить запрошенное преобразование или преобразования, WIC вызывает [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) с соответствующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="f3a3d-108">If the decoder can perform the requested transform or transforms, WIC invokes [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) with the appropriate parameters.</span></span> <span data-ttu-id="f3a3d-109">Если декодер может выполнять некоторые, но не все запрошенные преобразования, WIC запрашивает у декодера, что они могут, и использует объекты преобразования WIC ([**ивикбитмапскалер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler), [**ивикбитмапклиппер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper), [**ивикбитмапфлипротатор**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)и [**ивикформатконвертер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)) для выполнения оставшихся преобразований, которые не могут быть выполнены декодером кадров в результате вызова **CopyPixels** .</span><span class="sxs-lookup"><span data-stu-id="f3a3d-109">If the decoder can perform some, but not all of the requested transforms, WIC asks the decoder to perform those that it can, and uses the WIC transform objects ([**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler), [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper), [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator), and [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)) to perform the remaining transforms that could not be performed by the frame decoder on the result of the **CopyPixels** call.</span></span> <span data-ttu-id="f3a3d-110">Если декодер не поддерживает [**ивикбитмапсаурцетрансформ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform), компонент WIC должен использовать объекты Transform для выполнения всех преобразований.</span><span class="sxs-lookup"><span data-stu-id="f3a3d-110">If the decoder doesn’t support [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform), then WIC must use the transform objects to perform all of the transforms.</span></span> <span data-ttu-id="f3a3d-111">Обычно гораздо эффективнее сделать так, чтобы декодер выполнял преобразования в процессе декодирования, чем декодировать все изображение, а затем выполнять преобразования.</span><span class="sxs-lookup"><span data-stu-id="f3a3d-111">It’s usually much more efficient for the decoder to perform transforms during the decoding process than it is to decode the entire image and then perform the transforms.</span></span> <span data-ttu-id="f3a3d-112">Это особенно справедливо для таких операций, как масштабирование до значительно меньшего размера или преобразований формата пикселей.</span><span class="sxs-lookup"><span data-stu-id="f3a3d-112">This is especially true for operations such as scaling to a much smaller size or pixel format conversions.</span></span>


```C++
interface IWICBitmapSourceTransform : IUnknown
{
   // Required methods
   HRESULT DoesSupportTransform ( WICTransformOptions dstTransform,
              BOOL *pfIsSupported);
   HRESULT CopyPixels ( WICRect *prcSrc, 
      UINT uiWidth, 
      UINT uiHeight,
      WICPixelFormatGUID * pguidDstFormat,
      WICBitmapTransformOptions dstTransform, 
      UINT nStride, 
      UINT cbBufferSize, 
      BYTE *pbBuffer );

   // Optional methods
   HRESULT GetClosestSize ( UINT *puiWidth,
              UINT *puiHeight);
   HRESULT GetClosestPixelFormat ( WICPixelFormatGUID *pguidDstFormat);
}
```



-   [<span data-ttu-id="f3a3d-113">доессуппорттрансформ</span><span class="sxs-lookup"><span data-stu-id="f3a3d-113">DoesSupportTransform</span></span>](#doessupporttransform)
-   [<span data-ttu-id="f3a3d-114">CopyPixels</span><span class="sxs-lookup"><span data-stu-id="f3a3d-114">CopyPixels</span></span>](#copypixels)
-   [<span data-ttu-id="f3a3d-115">жетклосестсизе</span><span class="sxs-lookup"><span data-stu-id="f3a3d-115">GetClosestSize</span></span>](#getclosestsize)
-   [<span data-ttu-id="f3a3d-116">жетклосестпикселформат</span><span class="sxs-lookup"><span data-stu-id="f3a3d-116">GetClosestPixelFormat</span></span>](#getclosestpixelformat)

### <a name="doessupporttransform"></a><span data-ttu-id="f3a3d-117">доессуппорттрансформ</span><span class="sxs-lookup"><span data-stu-id="f3a3d-117">DoesSupportTransform</span></span>

<span data-ttu-id="f3a3d-118">[**Доессуппорттрансформ**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-doessupporttransform) спрашивает, поддерживает ли декодер запрошенную операцию вращения или зеркального отражения.</span><span class="sxs-lookup"><span data-stu-id="f3a3d-118">[**DoesSupportTransform**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-doessupporttransform) asks whether the decoder supports the requested rotation or flipping operation.</span></span> <span data-ttu-id="f3a3d-119">[**Викбитмаптрансформоптионс**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) , которые могут быть запрошены:</span><span class="sxs-lookup"><span data-stu-id="f3a3d-119">The [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) that may be requested are:</span></span>


```C++
enum WICBitmapTransformOptions
{   
   WICBitmapTransformRotate0,
   WICBitmapTransformRotate90,
   WICBitmapTransformRotate180,
   WICBitmapTransformRotate270,
   WICBitmapTransformFlipHorizontal,
   WICBitmapTransformFlipVertical
}
```



### <a name="copypixels"></a><span data-ttu-id="f3a3d-120">CopyPixels</span><span class="sxs-lookup"><span data-stu-id="f3a3d-120">CopyPixels</span></span>

<span data-ttu-id="f3a3d-121">[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) выполняет фактическую работу декодирования битов изображения, например метода [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) в интерфейсе [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) , но метод [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) в [**ивикбитмапсаурцетрансформ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) является гораздо более мощным и может значительно повысить производительность обработки изображений.</span><span class="sxs-lookup"><span data-stu-id="f3a3d-121">[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) performs the actual work of decoding the image bits, such as the [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) method on the [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) interface, but the [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) method on [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) is much more powerful, and can improve image processing performance significantly.</span></span>

<span data-ttu-id="f3a3d-122">При запросе нескольких операций преобразования результат зависит от порядка, в котором выполняются операции.</span><span class="sxs-lookup"><span data-stu-id="f3a3d-122">When multiple transform operations are requested, the result is dependent on the order in which the operations are performed.</span></span> <span data-ttu-id="f3a3d-123">Чтобы обеспечить предсказуемость и согласованность в кодеках, важно, чтобы все кодеки выполняли эти операции в том же порядке.</span><span class="sxs-lookup"><span data-stu-id="f3a3d-123">To ensure predictability and consistency across codecs, it’s important that all codecs perform these operations in the same order.</span></span> <span data-ttu-id="f3a3d-124">Это канонический порядок выполнения этих операций.</span><span class="sxs-lookup"><span data-stu-id="f3a3d-124">This is the canonical order for performing these operations.</span></span>

1.  <span data-ttu-id="f3a3d-125">Масштабирование</span><span class="sxs-lookup"><span data-stu-id="f3a3d-125">Scale</span></span>
2.  <span data-ttu-id="f3a3d-126">Crop</span><span class="sxs-lookup"><span data-stu-id="f3a3d-126">Crop</span></span>
3.  <span data-ttu-id="f3a3d-127">Rotate</span><span class="sxs-lookup"><span data-stu-id="f3a3d-127">Rotate</span></span>

<span data-ttu-id="f3a3d-128">Преобразование формата пикселей можно выполнить в любое время, так как оно не влияет на другие преобразования.</span><span class="sxs-lookup"><span data-stu-id="f3a3d-128">Pixel format conversion can be performed at any time, because it has no effect on the other transforms.</span></span>

<span data-ttu-id="f3a3d-129">Первый параметр, *прксрк*, используется для указания области интересов для обрезки изображения.</span><span class="sxs-lookup"><span data-stu-id="f3a3d-129">The first parameter, *prcSrc*, is used to specify the region of interest for clipping the image.</span></span> <span data-ttu-id="f3a3d-130">Поскольку масштабирование выполняется до усечения по соглашению, если изображение должно масштабироваться, а также обрезано, необходимо определить интересующую область после масштабирования изображения.</span><span class="sxs-lookup"><span data-stu-id="f3a3d-130">Because scaling is performed before clipping by convention, if the image is to be scaled as well as clipped, the region of interest should be determined after the image has been scaled.</span></span>

<span data-ttu-id="f3a3d-131">Второй и третий параметры указывают размер, до которого будет масштабироваться изображение.</span><span class="sxs-lookup"><span data-stu-id="f3a3d-131">The second and third parameters indicate the size to which to scale the image.</span></span>

<span data-ttu-id="f3a3d-132">Параметр *пгуиддстформат* указывает запрошенный формат пикселей для декодированного изображения.</span><span class="sxs-lookup"><span data-stu-id="f3a3d-132">The *pguidDstFormat* parameter indicates the requested pixel format for the decoded image.</span></span> <span data-ttu-id="f3a3d-133">Так как WIC уже вызвал [**жетклосестпикселформат**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestpixelformat), это должен быть формат пикселей, который декодер указал, что он поддерживает.</span><span class="sxs-lookup"><span data-stu-id="f3a3d-133">Because WIC has already called [**GetClosestPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestpixelformat), this should be a pixel format that the decoder has indicated that it supports.</span></span>

<span data-ttu-id="f3a3d-134">Параметр *дсттрансформ* указывает запрошенный угол вращения и необходимость перелистывания изображения по вертикали, горизонтали или обоим.</span><span class="sxs-lookup"><span data-stu-id="f3a3d-134">The *dstTransform* parameter indicates the requested rotation angle, and whether to flip the image vertically, horizontally, or both.</span></span> <span data-ttu-id="f3a3d-135">Опять же, поскольку компонент WIC уже назывался [**доессуппорттрансформ**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-doessupporttransform), запрошенное преобразование должно быть одним, что декодер уже указал, что он поддерживает.</span><span class="sxs-lookup"><span data-stu-id="f3a3d-135">Again, because WIC will have already called [**DoesSupportTransform**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-doessupporttransform), the requested transform should be one that the decoder has already indicated that it supports.</span></span> <span data-ttu-id="f3a3d-136">Помните, что вращение всегда должно выполняться после масштабирования и обрезки.</span><span class="sxs-lookup"><span data-stu-id="f3a3d-136">Remember that rotation should always be performed after scaling and clipping.</span></span>

### <a name="getclosestsize"></a><span data-ttu-id="f3a3d-137">жетклосестсизе</span><span class="sxs-lookup"><span data-stu-id="f3a3d-137">GetClosestSize</span></span>

<span data-ttu-id="f3a3d-138">[**Жетклосестсизе**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestsize) принимает два параметра in/out.</span><span class="sxs-lookup"><span data-stu-id="f3a3d-138">[**GetClosestSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestsize) takes two in/out parameters.</span></span> <span data-ttu-id="f3a3d-139">Вызывающий объект использует параметры *пуивидс* и *пуихеигхт* для указания размера, в котором вызывающий объект предпочитает декодировать изображение.</span><span class="sxs-lookup"><span data-stu-id="f3a3d-139">The caller uses the *puiWidth* and *puiHeight* parameters to specify the size at which that the caller prefers the image to be decoded.</span></span> <span data-ttu-id="f3a3d-140">Однако декодер может декодировать изображение только до размера, кратного размеру его ДКТ, а различные форматы изображений могут иметь различные размеры ДКТ.</span><span class="sxs-lookup"><span data-stu-id="f3a3d-140">However, a decoder can decode an image only to a size that’s a multiple of its DCT size, and different image formats can have different DCT sizes.</span></span> <span data-ttu-id="f3a3d-141">Декодер должен определить, на основе собственного размера ДКТ, ближайший к запрошенному размеру, и установить для этих измерений *пуивидс* и *пуихеигхт* .</span><span class="sxs-lookup"><span data-stu-id="f3a3d-141">The decoder should determine, based on its own DCT size, the closest it can come to the requested size, and set the *puiWidth* and *puiHeight* to those dimensions on return.</span></span> <span data-ttu-id="f3a3d-142">Если запрашивается больший размер, но кодек не поддерживает масштабирование, исходный объект должен быть возвращен.</span><span class="sxs-lookup"><span data-stu-id="f3a3d-142">If a larger size is requested, but the codec doesn’t support upscaling, the original should be returned.</span></span>

### <a name="getclosestpixelformat"></a><span data-ttu-id="f3a3d-143">жетклосестпикселформат</span><span class="sxs-lookup"><span data-stu-id="f3a3d-143">GetClosestPixelFormat</span></span>

<span data-ttu-id="f3a3d-144">[**Жетклосестпикселформат**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestpixelformat) используется для определения наиболее близкого формата пикселей к запрошенному формату пикселей, который декодер может предоставить без потери данных.</span><span class="sxs-lookup"><span data-stu-id="f3a3d-144">[**GetClosestPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestpixelformat) is used to determine the closest pixel format to the requested pixel format that the decoder can provide without loss of data.</span></span> <span data-ttu-id="f3a3d-145">Всегда рекомендуется преобразовывать в более широкий формат пикселей, чем на более узкую, несмотря на увеличение размера изображения, поскольку при необходимости его всегда можно преобразовать в более ограничивающий формат.</span><span class="sxs-lookup"><span data-stu-id="f3a3d-145">It’s always preferable to convert to a wider pixel format than a narrower one, even though it will increase the size of the image, because it can always be reconverted to a more restrictive format if necessary.</span></span> <span data-ttu-id="f3a3d-146">Однако после потери данных восстановить их будет невозможно.</span><span class="sxs-lookup"><span data-stu-id="f3a3d-146">However, after the data is lost, it can’t be recovered.</span></span>

## <a name="continued-reading"></a><span data-ttu-id="f3a3d-147">Продолжение чтения</span><span class="sxs-lookup"><span data-stu-id="f3a3d-147">Continued Reading</span></span>

<span data-ttu-id="f3a3d-148">Дополнительные сведения о создании кодеков с поддержкой WIC см. в разделе [Реализация ивикдевелоправ](-wic-imp-iwicdevelopraw.md).</span><span class="sxs-lookup"><span data-stu-id="f3a3d-148">To learn more about how to create a WIC-enabled codec, see [Implementing IWICDevelopRaw](-wic-imp-iwicdevelopraw.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f3a3d-149">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="f3a3d-149">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="f3a3d-150">**Reference**</span><span class="sxs-lookup"><span data-stu-id="f3a3d-150">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f3a3d-151">**ивикбитмапсаурцетрансформ**</span><span class="sxs-lookup"><span data-stu-id="f3a3d-151">**IWICBitmapSourceTransform**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)
</dt> <dt>

[<span data-ttu-id="f3a3d-152">**ивикметадатаблоккреадер**</span><span class="sxs-lookup"><span data-stu-id="f3a3d-152">**IWICMetadataBlockReader**</span></span>](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)
</dt> <dt>

<span data-ttu-id="f3a3d-153">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="f3a3d-153">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f3a3d-154">Реализация Ивикметадатаблоккреадер</span><span class="sxs-lookup"><span data-stu-id="f3a3d-154">Implementing IWICMetadataBlockReader</span></span>](-wic-imp-iwicmetadatablockreader.md)
</dt> <dt>

[<span data-ttu-id="f3a3d-155">Реализация Ивикдевелоправ</span><span class="sxs-lookup"><span data-stu-id="f3a3d-155">Implementing IWICDevelopRaw</span></span>](-wic-imp-iwicdevelopraw.md)
</dt> <dt>

[<span data-ttu-id="f3a3d-156">Написание WIC-Enabled КОДЕка</span><span class="sxs-lookup"><span data-stu-id="f3a3d-156">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="f3a3d-157">Общие сведения о компоненте создания образов Windows</span><span class="sxs-lookup"><span data-stu-id="f3a3d-157">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
