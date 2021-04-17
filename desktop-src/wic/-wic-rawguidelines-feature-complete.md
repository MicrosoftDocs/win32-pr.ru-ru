---
description: 'Полнота компонентов: Рекомендуемые интерфейсы'
ms.assetid: 759bf253-7450-4895-a550-9f81f3498f79
title: 'Полнота компонентов: Рекомендуемые интерфейсы'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1dba4bcc029b2205985afb443526376c0eecb16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693396"
---
# <a name="feature-completeness-recommended-interfaces"></a><span data-ttu-id="ff683-103">Полнота компонентов: Рекомендуемые интерфейсы</span><span class="sxs-lookup"><span data-stu-id="ff683-103">Feature Completeness: Recommended Interfaces</span></span>

<span data-ttu-id="ff683-104">В следующей таблице перечислены интерфейсы компонента обработки изображений Windows (WIC), которые должны быть реализованы в коде.</span><span class="sxs-lookup"><span data-stu-id="ff683-104">The following table lists the Windows Imaging Component (WIC) interfaces RAW codecs should implement.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ff683-105">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="ff683-105">Interface</span></span></th>
<th><span data-ttu-id="ff683-106">Обязательно для:</span><span class="sxs-lookup"><span data-stu-id="ff683-106">Required for</span></span></th>
<th><span data-ttu-id="ff683-107">Описание</span><span class="sxs-lookup"><span data-stu-id="ff683-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ff683-108"><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder"><strong>ивикбитмапдекодер</strong></a></span><span class="sxs-lookup"><span data-stu-id="ff683-108"><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder"><strong>IWICBitmapDecoder</strong></a></span></span></td>
<td><span data-ttu-id="ff683-109">Декодеров</span><span class="sxs-lookup"><span data-stu-id="ff683-109">Decoders</span></span></td>
<td><span data-ttu-id="ff683-110">Представляет начальную точку для декодирования файла изображения.</span><span class="sxs-lookup"><span data-stu-id="ff683-110">Represents the starting point for decoding an image file.</span></span> <span data-ttu-id="ff683-111">Предоставляет доступ к свойствам уровня контейнера, таким как эскизы, фреймы и палитра.</span><span class="sxs-lookup"><span data-stu-id="ff683-111">Provides access to container-level properties like thumbnails, frames, and palette.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ff683-112"><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode"><strong>IWICBitmapFrameDecode</strong></a></span><span class="sxs-lookup"><span data-stu-id="ff683-112"><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode"><strong>IWICBitmapFrameDecode</strong></a></span></span></td>
<td><span data-ttu-id="ff683-113">Декодеров</span><span class="sxs-lookup"><span data-stu-id="ff683-113">Decoders</span></span></td>
<td><span data-ttu-id="ff683-114">Представляет конкретный кадр изображения в контейнере, который предоставляет доступ к свойствам на уровне фрейма.</span><span class="sxs-lookup"><span data-stu-id="ff683-114">Represents a specific image frame within the container that provides access to frame-level properties.</span></span> <span data-ttu-id="ff683-115">Это интерфейс, который декодирует фактические биты изображения.</span><span class="sxs-lookup"><span data-stu-id="ff683-115">This is the interface that decodes the actual image bits.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ff683-116"><a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>ивикметадатаблоккреадер</strong></a></span><span class="sxs-lookup"><span data-stu-id="ff683-116"><a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a></span></span></td>
<td><span data-ttu-id="ff683-117">Декодеров</span><span class="sxs-lookup"><span data-stu-id="ff683-117">Decoders</span></span></td>
<td><span data-ttu-id="ff683-118">Требуется для перечисления и итерации блоков метаданных и вызова соответствующих средств чтения метаданных при чтении из файла изображения.</span><span class="sxs-lookup"><span data-stu-id="ff683-118">Required for enumerating and iterating through metadata blocks and invoking the appropriate metadata readers when reading from an image file.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="ff683-119">Если Необработанный формат контейнера совместим с TIFF или использует стандартные IFD или Ирбс для хранения метаданных EXIF или XMP, авторы кодеков могут выбрать вызов встроенных средств чтения метаданных, а не писать их самостоятельно.</span><span class="sxs-lookup"><span data-stu-id="ff683-119">If the RAW container format is TIFF compatible or uses standard IFDs or IRBs to store EXIF or XMP metadata, codec authors can choose to invoke the built-in metadata readers rather than writing their own.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ff683-120"><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform"><strong>ивикбитмапсаурцетрансформ</strong></a></span><span class="sxs-lookup"><span data-stu-id="ff683-120"><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform"><strong>IWICBitmapSourceTransform</strong></a></span></span></td>
<td><span data-ttu-id="ff683-121">Декодеров</span><span class="sxs-lookup"><span data-stu-id="ff683-121">Decoders</span></span></td>
<td><span data-ttu-id="ff683-122">Позволяет вызывающему объекту указать требуемое масштабирование, обрезку, поворот или формат пикселей для декодированного изображения, что может значительно повысить производительность декодера.</span><span class="sxs-lookup"><span data-stu-id="ff683-122">Allows the caller to specify desired scaling, cropping, rotation, or pixel format for the decoded image, which can significantly improve decoder performance.</span></span> <span data-ttu-id="ff683-123">Например, декодеры в формате JPEG и беспроводной связи (формате WDP) корпорации Майкрософт используют схему оптимизации пирамиды для ускорения декодирования, если целевой точечный рисунок меньше исходного растрового изображения.</span><span class="sxs-lookup"><span data-stu-id="ff683-123">For example, Microsoft's JPEG and Wireless Datagram Protocol (WDP) decoders use a pyramid optimization scheme to achieve faster decoding when the target bitmap is smaller than the source bitmap.</span></span> <span data-ttu-id="ff683-124">В Windows Vista (и более поздних версиях) будет предпринята попытка использовать этот интерфейс для извлечения &quot; быстрого &quot; предварительного просмотра из необработанного образа при отсутствии или менее чем 1 024 пикселей в самом большом измерении.</span><span class="sxs-lookup"><span data-stu-id="ff683-124">Windows Vista (and later) will attempt to use this interface to extract a &quot;fast&quot; preview from a RAW image whenever the embedded preview is missing or less than 1,024 pixels in its largest dimension.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ff683-125"><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw"><strong>ивикдевелоправ</strong></a></span><span class="sxs-lookup"><span data-stu-id="ff683-125"><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw"><strong>IWICDevelopRaw</strong></a></span></span></td>
<td><span data-ttu-id="ff683-126">Декодеров</span><span class="sxs-lookup"><span data-stu-id="ff683-126">Decoders</span></span></td>
<td><span data-ttu-id="ff683-127">Требуется для необработанных форматов.</span><span class="sxs-lookup"><span data-stu-id="ff683-127">Required for RAW formats.</span></span> <span data-ttu-id="ff683-128">Предоставляет параметры, характерные для обработки необработанных изображений.</span><span class="sxs-lookup"><span data-stu-id="ff683-128">Exposes parameters that are specific to RAW image processing.</span></span> <span data-ttu-id="ff683-129">Необработанные кодеки должны поддерживать столько же параметров, сколько применяется к кодеку.</span><span class="sxs-lookup"><span data-stu-id="ff683-129">RAW codecs should support as many of these parameters as apply to the codec.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ff683-130"><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder"><strong>ивикбитмапенкодер</strong></a></span><span class="sxs-lookup"><span data-stu-id="ff683-130"><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder"><strong>IWICBitmapEncoder</strong></a></span></span></td>
<td><span data-ttu-id="ff683-131">Кодировщики</span><span class="sxs-lookup"><span data-stu-id="ff683-131">Encoders</span></span></td>
<td><span data-ttu-id="ff683-132">Представляет отправную точку для кодирования файла изображения.</span><span class="sxs-lookup"><span data-stu-id="ff683-132">Represents the starting point for encoding an image file.</span></span> <span data-ttu-id="ff683-133">Этот интерфейс используется для задания свойств уровня контейнера, таких как эскизы, кадры и палитра.</span><span class="sxs-lookup"><span data-stu-id="ff683-133">This interface is used for setting container-level properties, such as thumbnails, frames, and palette.</span></span> <span data-ttu-id="ff683-134">Также необходимо вызвать модуль записи метаданных, чтобы включить сохраняемость метаданных в файле изображения.</span><span class="sxs-lookup"><span data-stu-id="ff683-134">It is also required to invoke a metadata writer to enable metadata persistence to the image file.</span></span> <span data-ttu-id="ff683-135">По этим причинам этот интерфейс необходим даже в том случае, если кодирование первичного точечного рисунка в Необработанный формат не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ff683-135">For these reasons, this interface is necessary even if encoding the primary bitmap to the RAW format is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ff683-136"><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode"><strong>ивикбитмапфраминкоде</strong></a></span><span class="sxs-lookup"><span data-stu-id="ff683-136"><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode"><strong>IWICBitmapFrameEncode</strong></a></span></span></td>
<td><span data-ttu-id="ff683-137">Кодировщики</span><span class="sxs-lookup"><span data-stu-id="ff683-137">Encoders</span></span></td>
<td><span data-ttu-id="ff683-138">Представляет конкретный кадр изображения в контейнере.</span><span class="sxs-lookup"><span data-stu-id="ff683-138">Represents a specific image frame within the container.</span></span> <span data-ttu-id="ff683-139">Этот интерфейс используется для кодирования фактических битов изображения и для задания метаданных и свойств каждого кадра.</span><span class="sxs-lookup"><span data-stu-id="ff683-139">This interface is used to encode the actual image bits and to set per-frame metadata and properties.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ff683-140"><a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>ивикметадатаблокквритер</strong></a></span><span class="sxs-lookup"><span data-stu-id="ff683-140"><a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a></span></span></td>
<td><span data-ttu-id="ff683-141">Кодировщики</span><span class="sxs-lookup"><span data-stu-id="ff683-141">Encoders</span></span></td>
<td><span data-ttu-id="ff683-142">Требуется для прохода по блокам метаданных и вызова соответствующих модулей записи метаданных при сериализации файла изображения.</span><span class="sxs-lookup"><span data-stu-id="ff683-142">Required for iterating through metadata blocks and invoking the appropriate metadata writers when serializing an image file.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="ff683-143">Если Необработанный формат контейнера совместим с TIFF, авторы кодеков могут выбрать вызов встроенных модулей записи метаданных, а не писать их самостоятельно.</span><span class="sxs-lookup"><span data-stu-id="ff683-143">If the RAW container format is TIFF-compatible, codec authors can choose to invoke the built-in metadata writers rather than writing their own.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="ff683-144">См. также</span><span class="sxs-lookup"><span data-stu-id="ff683-144">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="ff683-145">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="ff683-145">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ff683-146">Общие сведения о компоненте создания образов Windows</span><span class="sxs-lookup"><span data-stu-id="ff683-146">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="ff683-147">Рекомендации по WIC для форматов необработанных изображений Camera</span><span class="sxs-lookup"><span data-stu-id="ff683-147">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="ff683-148">Написание WIC-Enabled КОДЕка</span><span class="sxs-lookup"><span data-stu-id="ff683-148">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 




