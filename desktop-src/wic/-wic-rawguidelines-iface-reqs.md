---
description: Требования к методам интерфейса
ms.assetid: 8c2afeb3-3e0b-4f8a-a2f4-df7c9ce4b098
title: Требования к методам интерфейса
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9cabe02900fa789773f4104cf282ab326bd4930
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647547"
---
# <a name="interface-method-requirements"></a><span data-ttu-id="1d22c-103">Требования к методам интерфейса</span><span class="sxs-lookup"><span data-stu-id="1d22c-103">Interface Method Requirements</span></span>

<span data-ttu-id="1d22c-104">Не каждый метод в каждом интерфейсе должен иметь реализацию.</span><span class="sxs-lookup"><span data-stu-id="1d22c-104">Not every method on every interface must have an implementation.</span></span> <span data-ttu-id="1d22c-105">Например, некоторые кодеки имеют глобальные метаданные, эскизы или цветовые контексты, тогда как другие кодеки предоставляют их только для отдельных кадров.</span><span class="sxs-lookup"><span data-stu-id="1d22c-105">For example, some codecs have global metadata, thumbnails, or color contexts, whereas other codecs provide these only on a per-frame basis.</span></span> <span data-ttu-id="1d22c-106">Если авторы кодека предоставляют их только для каждого фрейма, им нужно только реализовать [**Get**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) / [**сетсумбнаил**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) или колорконтекстс или реализовать методы [**жетметадатакуериреадер**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) или [**жетметадатакуеривритер**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) в [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) и [**ивикбитмапфраминкоде**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) , а не в [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) и [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder).</span><span class="sxs-lookup"><span data-stu-id="1d22c-106">If codec authors provide these only on a per-frame basis, they need only implement the [**Get**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail)/[**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) or ColorContexts, or implement the [**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) or [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) methods on the [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) and [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) rather than on the [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) and [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder).</span></span> <span data-ttu-id="1d22c-107">Аналогично, некоторые кодеки не используют Индексированные форматы, поэтому не требуется реализовывать методы [**копипалетте**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-copypalette) и [**сетпалетте**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpalette) .</span><span class="sxs-lookup"><span data-stu-id="1d22c-107">Likewise, some codecs do not use indexed formats and so are not required to implement the [**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-copypalette) and [**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpalette) methods.</span></span> <span data-ttu-id="1d22c-108">Таким образом, эти методы являются необязательными и остаются на усмотрение создателя кодека.</span><span class="sxs-lookup"><span data-stu-id="1d22c-108">These methods are therefore optional and are left to the discretion of the codec creator.</span></span> <span data-ttu-id="1d22c-109">Большинство других методов являются обязательными.</span><span class="sxs-lookup"><span data-stu-id="1d22c-109">Most other methods are required.</span></span>

<span data-ttu-id="1d22c-110">Для Windows 7 [**Get**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) / [**сетпревиев**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpreview) и [**Get**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) / [**сетсумбнаил**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) являются обязательными и должны быть реализованы в классах на уровне вложения или в классах уровня кадров.</span><span class="sxs-lookup"><span data-stu-id="1d22c-110">For Windows 7 [**Get**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview)/[**SetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpreview) and [**Get**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail)/[**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) are required and must be implemented on either the contain-level classes or on the frame-level classes.</span></span> <span data-ttu-id="1d22c-111">Если формат файла изображения не поддерживает предварительный просмотр или эскизы в любом из этих расположений, следует изменить формат файла изображения, чтобы обеспечить такую поддержку.</span><span class="sxs-lookup"><span data-stu-id="1d22c-111">If your image file format doesn't support previews or thumbnails in either of these locations, then you should revise your image file format to provide such support.</span></span>

<span data-ttu-id="1d22c-112">Если метод не реализован, важно вернуть соответствующую ошибку, чтобы вызывающий объект мог определить, что запрошенная функция не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="1d22c-112">When a method is not implemented, it is important to return an appropriate error so the caller can determine that the requested feature is not supported.</span></span> <span data-ttu-id="1d22c-113">Например, если авторы кодека не поддерживают эскизы на уровне контейнера, они должны возвращать [винкодек \_ Err \_ кодекносумбнаил](-wic-codec-error-codes.md) , когда приложение вызывает метод- [**эскиз**](-wic-codec-iwicbitmapdecoder-getthumbnail-proxy.md), и если у них нет палитры, они должны возвращать [винкодек \_ Err \_ палеттеунаваилабле](-wic-codec-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="1d22c-113">For example, if codec authors do not support container-level thumbnails, they should return [WINCODEC\_ERR\_CODECNOTHUMBNAIL](-wic-codec-error-codes.md) when an application calls [**GetThumbnail**](-wic-codec-iwicbitmapdecoder-getthumbnail-proxy.md), and if they don't have a palette, they should return [WINCODEC\_ERR\_PALETTEUNAVAILABLE](-wic-codec-error-codes.md).</span></span> <span data-ttu-id="1d22c-114">Если подходящий код [ \_ Err винкодек](-wic-codec-error-codes.md) не существует, кодек должен вернуть E \_ нотимпл для нереализованных методов.</span><span class="sxs-lookup"><span data-stu-id="1d22c-114">If no suitable [WINCODEC\_ERR](-wic-codec-error-codes.md) code exists, then the codec should return E\_NOTIMPL for unimplemented methods.</span></span>

<span data-ttu-id="1d22c-115">В следующих таблицах перечислены обязательные и необязательные методы для каждого интерфейса компонента Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="1d22c-115">The following tables list the required and optional methods for each Windows Imaging Component (WIC) interfaces.</span></span>

[<span data-ttu-id="1d22c-116">**ивикбитмапдекодер**</span><span class="sxs-lookup"><span data-stu-id="1d22c-116">**IWICBitmapDecoder**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)



<span data-ttu-id="1d22c-117">Обязательно</span><span class="sxs-lookup"><span data-stu-id="1d22c-117">Required</span></span>

[<span data-ttu-id="1d22c-118">**куерикапабилити**</span><span class="sxs-lookup"><span data-stu-id="1d22c-118">**QueryCapability**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-querycapability)

[<span data-ttu-id="1d22c-119">**Инициализация**</span><span class="sxs-lookup"><span data-stu-id="1d22c-119">**Initialize**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-initialize)

[<span data-ttu-id="1d22c-120">**жетконтаинерформат**</span><span class="sxs-lookup"><span data-stu-id="1d22c-120">**GetContainerFormat**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcontainerformat)

[<span data-ttu-id="1d22c-121">**жетдекодеринфо**</span><span class="sxs-lookup"><span data-stu-id="1d22c-121">**GetDecoderInfo**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getdecoderinfo)

[<span data-ttu-id="1d22c-122">**жетфрамекаунт**</span><span class="sxs-lookup"><span data-stu-id="1d22c-122">**GetFrameCount**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframecount)

[<span data-ttu-id="1d22c-123">**GetFrame**</span><span class="sxs-lookup"><span data-stu-id="1d22c-123">**GetFrame**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe)

<span data-ttu-id="1d22c-124">Необязательно</span><span class="sxs-lookup"><span data-stu-id="1d22c-124">Optional</span></span>

<span data-ttu-id="1d22c-125">[**OnPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview)¹</span><span class="sxs-lookup"><span data-stu-id="1d22c-125">[**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview)¹</span></span>

<span data-ttu-id="1d22c-126">[**Эскиз**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail)²</span><span class="sxs-lookup"><span data-stu-id="1d22c-126">[**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail)²</span></span>

[<span data-ttu-id="1d22c-127">**жетколорконтекстс**</span><span class="sxs-lookup"><span data-stu-id="1d22c-127">**GetColorContexts**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcolorcontexts)

[<span data-ttu-id="1d22c-128">**жетметадатакуериреадер**</span><span class="sxs-lookup"><span data-stu-id="1d22c-128">**GetMetadataQueryReader**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getmetadataqueryreader)

[<span data-ttu-id="1d22c-129">**копипалетте**</span><span class="sxs-lookup"><span data-stu-id="1d22c-129">**CopyPalette**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-copypalette)



 

<span data-ttu-id="1d22c-130">¹ требуется, если формат файла изображения поддерживает предварительные версии уровня контейнера.</span><span class="sxs-lookup"><span data-stu-id="1d22c-130">¹Required if your image file format supports container-level previews.</span></span> <span data-ttu-id="1d22c-131">Если это не так, настоятельно рекомендуется изменить формат файла изображения для поддержки этой ситуации.</span><span class="sxs-lookup"><span data-stu-id="1d22c-131">If this is not the case you are strongly encouraged to revise your image file format to support this.</span></span> <span data-ttu-id="1d22c-132">Если реализуется здесь, то для класса кодирования на уровне контейнера требуется соответствующий [**сетпревиев**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpreview) .</span><span class="sxs-lookup"><span data-stu-id="1d22c-132">If implemented here, then a corresponding [**SetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpreview) is required on the container-level encode class.</span></span>

<span data-ttu-id="1d22c-133">в зависимости от того, где в формате файла изображения хранятся эскизы, необходимо ввести ² или на класс декодирования на уровне кадров.</span><span class="sxs-lookup"><span data-stu-id="1d22c-133">²Required either here, or on the frame-level decode class, depending on where your image file format stores thumbnails.</span></span> <span data-ttu-id="1d22c-134">Если реализуется здесь, то для класса кодирования на уровне контейнера требуется соответствующий [**сетсумбнаил**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) .</span><span class="sxs-lookup"><span data-stu-id="1d22c-134">If implemented here, then a corresponding [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) is required on the container-level encode class.</span></span>

[<span data-ttu-id="1d22c-135">**IWICBitmapFrameDecode**</span><span class="sxs-lookup"><span data-stu-id="1d22c-135">**IWICBitmapFrameDecode**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)



<span data-ttu-id="1d22c-136">Обязательно</span><span class="sxs-lookup"><span data-stu-id="1d22c-136">Required</span></span>

[<span data-ttu-id="1d22c-137">**жетколорконтекстс**</span><span class="sxs-lookup"><span data-stu-id="1d22c-137">**GetColorContexts**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts)

[<span data-ttu-id="1d22c-138">**жетметадатакуериреадер**</span><span class="sxs-lookup"><span data-stu-id="1d22c-138">**GetMetadataQueryReader**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader)

[<span data-ttu-id="1d22c-139">**GetSize**</span><span class="sxs-lookup"><span data-stu-id="1d22c-139">**GetSize**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getsize)

[<span data-ttu-id="1d22c-140">**жетпикселформат**</span><span class="sxs-lookup"><span data-stu-id="1d22c-140">**GetPixelFormat**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getpixelformat)

[<span data-ttu-id="1d22c-141">**Решение с высоким разрешением**</span><span class="sxs-lookup"><span data-stu-id="1d22c-141">**GetResolution**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getresolution)

[<span data-ttu-id="1d22c-142">**CopyPixels**</span><span class="sxs-lookup"><span data-stu-id="1d22c-142">**CopyPixels**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels)

<span data-ttu-id="1d22c-143">Необязательно</span><span class="sxs-lookup"><span data-stu-id="1d22c-143">Optional</span></span>

<span data-ttu-id="1d22c-144">[**Эскиз**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail)¹</span><span class="sxs-lookup"><span data-stu-id="1d22c-144">[**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail)¹</span></span>

[<span data-ttu-id="1d22c-145">**копипалетте**</span><span class="sxs-lookup"><span data-stu-id="1d22c-145">**CopyPalette**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-copypalette)



 

<span data-ttu-id="1d22c-146">¹, требуемое здесь, или на классе декодирования на уровне контейнера, в зависимости от того, в каком месте изображения хранятся эскизы форматов файлов.</span><span class="sxs-lookup"><span data-stu-id="1d22c-146">¹Required either here, or on the container-level decode class, depending on where you image file format stores thumbnails.</span></span> <span data-ttu-id="1d22c-147">При реализации здесь для класса кодировщика на уровне кадров требуется соответствующий [**сетсумбнаил**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail) .</span><span class="sxs-lookup"><span data-stu-id="1d22c-147">If implemented here, then a corresponding [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail) is required on the frame-level encoder class.</span></span>

[<span data-ttu-id="1d22c-148">**ивикметадатаблоккреадер**</span><span class="sxs-lookup"><span data-stu-id="1d22c-148">**IWICMetadataBlockReader**</span></span>](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)



<span data-ttu-id="1d22c-149">Обязательно</span><span class="sxs-lookup"><span data-stu-id="1d22c-149">Required</span></span>

[<span data-ttu-id="1d22c-150">**жетконтаинерформат**</span><span class="sxs-lookup"><span data-stu-id="1d22c-150">**GetContainerFormat**</span></span>](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcontainerformat)

[<span data-ttu-id="1d22c-151">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="1d22c-151">**GetCount**</span></span>](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcount)

[<span data-ttu-id="1d22c-152">**жетреадербиндекс**</span><span class="sxs-lookup"><span data-stu-id="1d22c-152">**GetReaderByIndex**</span></span>](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getreaderbyindex)

[<span data-ttu-id="1d22c-153">**GetEnumerator**</span><span class="sxs-lookup"><span data-stu-id="1d22c-153">**GetEnumerator**</span></span>](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getenumerator)



 

[<span data-ttu-id="1d22c-154">**ивикбитмапсаурцетрансформ**</span><span class="sxs-lookup"><span data-stu-id="1d22c-154">**IWICBitmapSourceTransform**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)



<span data-ttu-id="1d22c-155">Обязательно</span><span class="sxs-lookup"><span data-stu-id="1d22c-155">Required</span></span>

[<span data-ttu-id="1d22c-156">**доессуппорттрансформ**</span><span class="sxs-lookup"><span data-stu-id="1d22c-156">**DoesSupportTransform**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-doessupporttransform)

[<span data-ttu-id="1d22c-157">**CopyPixels**</span><span class="sxs-lookup"><span data-stu-id="1d22c-157">**CopyPixels**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels)

<span data-ttu-id="1d22c-158">Необязательно</span><span class="sxs-lookup"><span data-stu-id="1d22c-158">Optional</span></span>

[<span data-ttu-id="1d22c-159">**жетклосестсизе**</span><span class="sxs-lookup"><span data-stu-id="1d22c-159">**GetClosestSize**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestsize)

[<span data-ttu-id="1d22c-160">**жетклосестпикселформат**</span><span class="sxs-lookup"><span data-stu-id="1d22c-160">**GetClosestPixelFormat**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestpixelformat)



 

[<span data-ttu-id="1d22c-161">**ивикдевелоправ**</span><span class="sxs-lookup"><span data-stu-id="1d22c-161">**IWICDevelopRaw**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)

<span data-ttu-id="1d22c-162">См. раздел [Поддержка ивикдевелоправ](./-wic-rawguidelines-iwicdevelopraw.md)далее в этом документе.</span><span class="sxs-lookup"><span data-stu-id="1d22c-162">See [Support for IWICDevelopRaw](./-wic-rawguidelines-iwicdevelopraw.md), later in this document.</span></span>

[<span data-ttu-id="1d22c-163">**ивикбитмапенкодер**</span><span class="sxs-lookup"><span data-stu-id="1d22c-163">**IWICBitmapEncoder**</span></span>](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)



<span data-ttu-id="1d22c-164">Обязательно</span><span class="sxs-lookup"><span data-stu-id="1d22c-164">Required</span></span>

[<span data-ttu-id="1d22c-165">**Инициализация**</span><span class="sxs-lookup"><span data-stu-id="1d22c-165">**Initialize**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize)

[<span data-ttu-id="1d22c-166">**жетконтаинерформат**</span><span class="sxs-lookup"><span data-stu-id="1d22c-166">**GetContainerFormat**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getcontainerformat)

[<span data-ttu-id="1d22c-167">**жетенкодеринфо**</span><span class="sxs-lookup"><span data-stu-id="1d22c-167">**GetEncoderInfo**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getencoderinfo)

[<span data-ttu-id="1d22c-168">**CreateNewFrame**</span><span class="sxs-lookup"><span data-stu-id="1d22c-168">**CreateNewFrame**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe)

[<span data-ttu-id="1d22c-169">**Сохраните**</span><span class="sxs-lookup"><span data-stu-id="1d22c-169">**Commit**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit)

<span data-ttu-id="1d22c-170">Необязательно</span><span class="sxs-lookup"><span data-stu-id="1d22c-170">Optional</span></span>

<span data-ttu-id="1d22c-171">[**Сетпревиев**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpreview)¹</span><span class="sxs-lookup"><span data-stu-id="1d22c-171">[**SetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpreview)¹</span></span>

<span data-ttu-id="1d22c-172">[**Сетсумбнаил**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail)²</span><span class="sxs-lookup"><span data-stu-id="1d22c-172">[**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail)²</span></span>

[<span data-ttu-id="1d22c-173">**сетколорконтекстс**</span><span class="sxs-lookup"><span data-stu-id="1d22c-173">**SetColorContexts**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setcolorcontexts)

[<span data-ttu-id="1d22c-174">**жетметадатакуеривритер**</span><span class="sxs-lookup"><span data-stu-id="1d22c-174">**GetMetadataQueryWriter**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getmetadataquerywriter)

[<span data-ttu-id="1d22c-175">**сетпалетте**</span><span class="sxs-lookup"><span data-stu-id="1d22c-175">**SetPalette**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-setpalette)



 

<span data-ttu-id="1d22c-176">¹ требуется, если формат файла изображения поддерживает предварительный просмотр на уровне кадров.</span><span class="sxs-lookup"><span data-stu-id="1d22c-176">¹Required if your image file format supports frame-level previews.</span></span>

<span data-ttu-id="1d22c-177">в зависимости от того, где в формате файла изображения хранятся эскизы, требуется ², или для класса кодирования на уровне кадров.</span><span class="sxs-lookup"><span data-stu-id="1d22c-177">²Required either here, or on the frame-level encode class, depending on where your image file format stores thumbnails.</span></span> <span data-ttu-id="1d22c-178">Если реализуется здесь, то для класса декодирования на уровне контейнера [**требуется соответствующий параметр ","**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) .</span><span class="sxs-lookup"><span data-stu-id="1d22c-178">If implemented here, then a corresponding [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) is required on the container-level decode class.</span></span>

[<span data-ttu-id="1d22c-179">**ивикбитмапфраминкоде**</span><span class="sxs-lookup"><span data-stu-id="1d22c-179">**IWICBitmapFrameEncode**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)



<span data-ttu-id="1d22c-180">Обязательно</span><span class="sxs-lookup"><span data-stu-id="1d22c-180">Required</span></span>

[<span data-ttu-id="1d22c-181">**Инициализация**</span><span class="sxs-lookup"><span data-stu-id="1d22c-181">**Initialize**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize)

[<span data-ttu-id="1d22c-182">**сетколорконтекстс**</span><span class="sxs-lookup"><span data-stu-id="1d22c-182">**SetColorContexts**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setcolorcontexts)

[<span data-ttu-id="1d22c-183">**сетколорконтекстс**</span><span class="sxs-lookup"><span data-stu-id="1d22c-183">**SetColorContexts**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setcolorcontexts)

[<span data-ttu-id="1d22c-184">**SetSize**</span><span class="sxs-lookup"><span data-stu-id="1d22c-184">**SetSize**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setsize)

[<span data-ttu-id="1d22c-185">**сетпикселформат**</span><span class="sxs-lookup"><span data-stu-id="1d22c-185">**SetPixelFormat**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setpixelformat)

[<span data-ttu-id="1d22c-186">**сетресолутион**</span><span class="sxs-lookup"><span data-stu-id="1d22c-186">**SetResolution**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setresolution)

[<span data-ttu-id="1d22c-187">**WritePixels**</span><span class="sxs-lookup"><span data-stu-id="1d22c-187">**WritePixels**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels)

[<span data-ttu-id="1d22c-188">**вритесаурце**</span><span class="sxs-lookup"><span data-stu-id="1d22c-188">**WriteSource**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource)

[<span data-ttu-id="1d22c-189">**Сохраните**</span><span class="sxs-lookup"><span data-stu-id="1d22c-189">**Commit**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit)

<span data-ttu-id="1d22c-190">Необязательно</span><span class="sxs-lookup"><span data-stu-id="1d22c-190">Optional</span></span>

<span data-ttu-id="1d22c-191">[**Сетсумбнаил**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail)¹</span><span class="sxs-lookup"><span data-stu-id="1d22c-191">[**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail)¹</span></span>

[<span data-ttu-id="1d22c-192">**копипалетте**</span><span class="sxs-lookup"><span data-stu-id="1d22c-192">**CopyPalette**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypalette)



 

<span data-ttu-id="1d22c-193">¹, требуемое здесь, или в классе кодирования уровня контейнера, в зависимости от того, где хранятся эскизы в формате файлов изображений.</span><span class="sxs-lookup"><span data-stu-id="1d22c-193">¹Required either here, or on the container-level encode class, depending on where your image file format stores thumbnails.</span></span> <span data-ttu-id="1d22c-194">Если реализуется здесь, то для класса декодирования на уровне кадров [**требуется соответствующий параметр**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) «NOFRAMES».</span><span class="sxs-lookup"><span data-stu-id="1d22c-194">If implemented here, then a corresponding [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) is required on the frame-level decode class.</span></span>

[<span data-ttu-id="1d22c-195">**ивикметадатаблоккреадер**</span><span class="sxs-lookup"><span data-stu-id="1d22c-195">**IWICMetadataBlockReader**</span></span>](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)



<span data-ttu-id="1d22c-196">Обязательно</span><span class="sxs-lookup"><span data-stu-id="1d22c-196">Required</span></span>

[<span data-ttu-id="1d22c-197">**инитиализефромблоккреадер**</span><span class="sxs-lookup"><span data-stu-id="1d22c-197">**InitializeFromBlockReader**</span></span>](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-initializefromblockreader)

[<span data-ttu-id="1d22c-198">**аддвритер**</span><span class="sxs-lookup"><span data-stu-id="1d22c-198">**AddWriter**</span></span>](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-addwriter)

[<span data-ttu-id="1d22c-199">**жетвритербиндекс**</span><span class="sxs-lookup"><span data-stu-id="1d22c-199">**GetWriterByIndex**</span></span>](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-getwriterbyindex)

[<span data-ttu-id="1d22c-200">**сетвритербиндекс**</span><span class="sxs-lookup"><span data-stu-id="1d22c-200">**SetWriterByIndex**</span></span>](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-setwriterbyindex)

[<span data-ttu-id="1d22c-201">**ремовевритербиндекс**</span><span class="sxs-lookup"><span data-stu-id="1d22c-201">**RemoveWriterByIndex**</span></span>](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-removewriterbyindex)



 

## <a name="related-topics"></a><span data-ttu-id="1d22c-202">См. также</span><span class="sxs-lookup"><span data-stu-id="1d22c-202">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="1d22c-203">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="1d22c-203">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1d22c-204">Общие сведения о компоненте создания образов Windows</span><span class="sxs-lookup"><span data-stu-id="1d22c-204">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="1d22c-205">Рекомендации по WIC для форматов необработанных изображений Camera</span><span class="sxs-lookup"><span data-stu-id="1d22c-205">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="1d22c-206">Написание WIC-Enabled КОДЕка</span><span class="sxs-lookup"><span data-stu-id="1d22c-206">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 
