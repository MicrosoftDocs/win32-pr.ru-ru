---
description: Требования к необработанным кодекам для Windows 7
ms.assetid: 3f8bd336-ba03-4ffb-9aa2-ea55a276e3bc
title: Требования к необработанным кодекам для Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e0c4d04175eab1b6e68ac87ed18a648fa4655b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683776"
---
# <a name="raw-codec-requirements-for-windows-7"></a><span data-ttu-id="bba34-103">Требования к необработанным кодекам для Windows 7</span><span class="sxs-lookup"><span data-stu-id="bba34-103">RAW Codec Requirements for Windows 7</span></span>

<span data-ttu-id="bba34-104">Следующие функции кодека необходимы как минимум:</span><span class="sxs-lookup"><span data-stu-id="bba34-104">The following codec features are required at a minimum:</span></span>

<span data-ttu-id="bba34-105">Все функции, необходимые для поддержки оболочки Windows Vista и фотоальбома: эскиз, предварительный просмотр и (сохраненный) поворот.</span><span class="sxs-lookup"><span data-stu-id="bba34-105">All functionality that is required for Windows Vista shell and Photo Gallery support: thumbnail, preview, and (persisted) rotation.</span></span> <span data-ttu-id="bba34-106">Обработка необработанных значений по умолчанию должна соответствовать параметрам-снимкам.</span><span class="sxs-lookup"><span data-stu-id="bba34-106">RAW processing should default to appropriate as-shot settings.</span></span>

<span data-ttu-id="bba34-107">Поддержка основных метаданных (как для чтения, так и для записи), не для EXIF, а также для метаданных EXIF, должна сохраняться в форматах необработанных файлов без использования файлов расширения.</span><span class="sxs-lookup"><span data-stu-id="bba34-107">Support for core metadata (both read and write), Non-EXIF metadata, as well as EXIF metadata, should be persisted inside RAW file formats without use of sidecar files.</span></span>

<span data-ttu-id="bba34-108">Поддержка интерфейса [**ивикдевелоправ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) .</span><span class="sxs-lookup"><span data-stu-id="bba34-108">Support for the [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) interface.</span></span> <span data-ttu-id="bba34-109">Для Windows 7 компонент WIC компонента Windows Imaging требует, чтобы были реализованы все интерфейсы параметров, предоставляемые [**ивикдевелоправ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) .</span><span class="sxs-lookup"><span data-stu-id="bba34-109">For Windows 7, Windows Imaging Component (WIC)WIC requires that all parameter interfaces exposed by [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) be implemented.</span></span>

<span data-ttu-id="bba34-110">Поддержка состояния ориентации:</span><span class="sxs-lookup"><span data-stu-id="bba34-110">Orientation state support:</span></span>

-   <span data-ttu-id="bba34-111">90. повороты изображений шага следует применять с помощью метода [**ивикдевелоправ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**сетротатион**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) .</span><span class="sxs-lookup"><span data-stu-id="bba34-111">90 degree-step Image rotations should be applied by using the [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**SetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) method.</span></span> <span data-ttu-id="bba34-112">Приложения и Windows используют этот метод для смены изображений (а также кэшированных эскизов и предварительных версий).</span><span class="sxs-lookup"><span data-stu-id="bba34-112">Applications and Windows use this method to rotate the images (and cached thumbnails and previews).</span></span>
-   <span data-ttu-id="bba34-113">Применение поворота с помощью этого API также должно сохраняться кодеком (см. ранее в этом документе).</span><span class="sxs-lookup"><span data-stu-id="bba34-113">Application of rotation by using this API should also be persisted by the codec (see earlier in this paper).</span></span>
-   <span data-ttu-id="bba34-114">Приложения могут использовать возможности вращения API [**ивикбитмапсаурцетрансформ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) , но кодек не будет выполнять сериализацию параметров вращения для этого API, поэтому вращение, выполненные с помощью [**ивикбитмапсаурцетрансформ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) , не будут сохранены.</span><span class="sxs-lookup"><span data-stu-id="bba34-114">Applications can use the rotation capabilities of the [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) API, but the codec will not serialize any rotation settings on this API, so rotations done using [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) will not be persisted.</span></span>

<span data-ttu-id="bba34-115">Поддержка высокоскоростного просмотра эскизов и извлечения.</span><span class="sxs-lookup"><span data-stu-id="bba34-115">High-speed thumbnail and preview extraction support.</span></span> <span data-ttu-id="bba34-116">Если максимальный размер измерения в пикселях (ширина или высота) для предварительного просмотра меньше 1024 пикселей, Windows Vista запросит визуализацию для предварительного просмотра экрана:</span><span class="sxs-lookup"><span data-stu-id="bba34-116">If the preview maximum pixel dimension (width or height) is less than 1024 pixels in size, Windows Vista will request a render for screen preview:</span></span>

-   <span data-ttu-id="bba34-117">Метод [**ивикдевелоправ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**сетрендермоде**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) должен поддерживать как минимум режимы [**викраврендеркуалитидрафтмоде**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrendermode) и [**викраврендеркуалитибесткуалити**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrendermode) , чтобы обеспечить более быструю визуализацию эскизов и предварительного просмотра, чем режим полного качества.</span><span class="sxs-lookup"><span data-stu-id="bba34-117">The [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**SetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) method should support at least the [**WICRawRenderQualityDraftMode**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrendermode) and [**WICRawRenderQualityBestQuality**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrendermode) modes to allow faster rendering of thumbnails and previews than the full-quality mode.</span></span>
-   <span data-ttu-id="bba34-118">Windows выполнит вызов [**ивикбитмапсаурцетрансформ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)::[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) с запрошенным размером разрешения экрана.</span><span class="sxs-lookup"><span data-stu-id="bba34-118">Windows will call [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)::[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) with the requested screen resolution size.</span></span>
-   <span data-ttu-id="bba34-119">Размеры разрешения экрана должны поддерживаться в приведенном выше API.</span><span class="sxs-lookup"><span data-stu-id="bba34-119">Screen resolution sizes must be supported in the above API.</span></span>
-   <span data-ttu-id="bba34-120">Требуется последовательная обработка изображений эскизов эскиза, предварительного просмотра и полных битов изображений из [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) .</span><span class="sxs-lookup"><span data-stu-id="bba34-120">Consistent image processing of thumbnail, preview, and full-image bits from [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) is required.</span></span>

<span data-ttu-id="bba34-121">Форматы пикселей с высоким динамическим диапазоном (HDR).</span><span class="sxs-lookup"><span data-stu-id="bba34-121">High dynamic range (HDR) pixel formats.</span></span>

<span data-ttu-id="bba34-122">Печать в формате XPS.</span><span class="sxs-lookup"><span data-stu-id="bba34-122">XML Paper Specification (XPS) printing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bba34-123">См. также</span><span class="sxs-lookup"><span data-stu-id="bba34-123">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="bba34-124">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="bba34-124">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="bba34-125">Общие сведения о компоненте создания образов Windows</span><span class="sxs-lookup"><span data-stu-id="bba34-125">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="bba34-126">Рекомендации по WIC для форматов необработанных изображений Camera</span><span class="sxs-lookup"><span data-stu-id="bba34-126">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="bba34-127">Написание WIC-Enabled КОДЕка</span><span class="sxs-lookup"><span data-stu-id="bba34-127">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



