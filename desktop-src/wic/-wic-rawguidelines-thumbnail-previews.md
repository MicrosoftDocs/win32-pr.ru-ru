---
description: Эскизы и предварительные версии
ms.assetid: e45f025e-a1ac-47c8-b794-ab1402ab35fb
title: Эскизы и предварительные версии
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e279da9771a43eb75bb94faff23d2e6aa29c4ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105656662"
---
# <a name="thumbnails-and-previews"></a><span data-ttu-id="f2209-103">Эскизы и предварительные версии</span><span class="sxs-lookup"><span data-stu-id="f2209-103">Thumbnails and Previews</span></span>

<span data-ttu-id="f2209-104">Windows Vista и фотоальбом Windows используют компонент Windows Imaging Component (WIC) для визуализации быстрых эскизов и предварительного просмотра изображений.</span><span class="sxs-lookup"><span data-stu-id="f2209-104">Windows Vista and the Windows Photo Gallery rely on Windows Imaging Component (WIC) to render fast thumbnails and previews of images.</span></span> <span data-ttu-id="f2209-105">Для поддержки быстрой отрисовки и просмотра изображений необработанные кодеки должны реализовывать [**интерфейсы WIC с**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) интерфейсом и [**предварительным просмотром**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) .</span><span class="sxs-lookup"><span data-stu-id="f2209-105">To support fast thumbnail and preview rendering, RAW codecs must implement the WIC [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) and [**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) interfaces.</span></span> <span data-ttu-id="f2209-106">Для поддержки реагирования на запросы пользователей настоятельно рекомендуется, чтобы эти интерфейсы возвращали [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) вызывающей стороне в течение 200 миллисекунд или меньше.</span><span class="sxs-lookup"><span data-stu-id="f2209-106">To support a responsive user experience, it is highly desirable that these interfaces return an [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) to the caller in 200 milliseconds or less.</span></span>

<span data-ttu-id="f2209-107">Корпорация Майкрософт настоятельно рекомендует владельцам формата необработанных файлов создавать предварительно подготовленный Просмотр и кэшировать его в файле изображения.</span><span class="sxs-lookup"><span data-stu-id="f2209-107">Microsoft strongly recommends that RAW file format owners generate a prerendered preview and cache this in the image file.</span></span> <span data-ttu-id="f2209-108">Для формата в устройстве это обычно делается во время записи.</span><span class="sxs-lookup"><span data-stu-id="f2209-108">For an in-device format, this is usually done at capture time.</span></span> <span data-ttu-id="f2209-109">Однако предварительные версии также могут быть повторно созданы и сохранены в файле изображения при каждом изменении свойств интерфейса [**ивикдевелоправ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) , если это не требует слишком большого объема работы.</span><span class="sxs-lookup"><span data-stu-id="f2209-109">However, previews could also be regenerated and stored in the image file whenever [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) interface properties are changed-if it does not take too much work to do so.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f2209-110">См. также</span><span class="sxs-lookup"><span data-stu-id="f2209-110">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="f2209-111">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="f2209-111">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f2209-112">Общие сведения о компоненте создания образов Windows</span><span class="sxs-lookup"><span data-stu-id="f2209-112">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="f2209-113">Рекомендации по WIC для форматов необработанных изображений Camera</span><span class="sxs-lookup"><span data-stu-id="f2209-113">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="f2209-114">Написание WIC-Enabled КОДЕка</span><span class="sxs-lookup"><span data-stu-id="f2209-114">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



