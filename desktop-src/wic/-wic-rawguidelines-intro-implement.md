---
description: Общие рекомендации по реализации необработанных кодеков
ms.assetid: 47b3b226-4642-41d2-b05c-bc12583047aa
title: Общие рекомендации по реализации необработанных кодеков
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f774e5d254330e3274daccb6062f35baa443144
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265853"
---
# <a name="general-guidelines-for-implementing-raw-codecs"></a><span data-ttu-id="b3fba-103">Общие рекомендации по реализации необработанных кодеков</span><span class="sxs-lookup"><span data-stu-id="b3fba-103">General Guidelines for Implementing RAW Codecs</span></span>

<span data-ttu-id="b3fba-104">По сравнению с необработанными типами изображений, такими как JPEG или TIFF, существуют два существенных отличия в том, как предполагается, что форматы RAW-изображений работают в Windows:</span><span class="sxs-lookup"><span data-stu-id="b3fba-104">Compared to non-RAW image types such as JPEG or TIFF, there are two notable differences in how RAW image formats are expected to behave in Windows:</span></span>

-   <span data-ttu-id="b3fba-105">Большинство форматов необработанных изображений предполагается «только для чтения» и, возможно, не будет поддерживать кодирование пикселей в Необработанный формат.</span><span class="sxs-lookup"><span data-stu-id="b3fba-105">Most RAW image formats are presumed to be "read only" and probably will not support pixel encoding to RAW format.</span></span> <span data-ttu-id="b3fba-106">Однако, поскольку компоненту обработки изображений Windows (WIC) требуется кодировщик для поддержки обратной записи метаданных, авторы необработанных кодеков должны запланировать реализацию как минимум каркаса класса кодировщика.</span><span class="sxs-lookup"><span data-stu-id="b3fba-106">However, because Windows Imaging Component (WIC) requires an encoder to support metadata write-back, RAW codec authors should plan to implement at least a skeleton encoder class.</span></span>
-   <span data-ttu-id="b3fba-107">Декодирование необработанного образа в полном размере может занять много времени по сравнению с другими форматами.</span><span class="sxs-lookup"><span data-stu-id="b3fba-107">Decoding a full-size RAW image can take a long time compared to other formats.</span></span> <span data-ttu-id="b3fba-108">По этой причине корпорация Майкрософт рекомендует принять определенные подходы к уменьшению задержки декодирования и обеспечить поддержку таких сценариев, как быстрое отображение эскизов и предварительных версий.</span><span class="sxs-lookup"><span data-stu-id="b3fba-108">For this reason, Microsoft recommends that certain approaches be taken to minimize decoding latency and to ensure support for scenarios such as rapid rendering of thumbnails and previews.</span></span>

    <span data-ttu-id="b3fba-109">Например, все авторы необработанного кодека должны реализовать интерфейс [**ивикбитмапсаурцетрансформ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) , который предоставляет механизм для уведомления декодера заранее до размера целевого растрового изображения, что позволяет оптимизировать декодирование до меньшего размера выходного изображения.</span><span class="sxs-lookup"><span data-stu-id="b3fba-109">For example, all RAW codec authors must implement the [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) interface, which provides a mechanism to notify the decoder in advance of the target bitmap size, thus enabling optimized decoding to a smaller output image size.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b3fba-110">См. также</span><span class="sxs-lookup"><span data-stu-id="b3fba-110">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="b3fba-111">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="b3fba-111">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b3fba-112">Общие сведения о компоненте создания образов Windows</span><span class="sxs-lookup"><span data-stu-id="b3fba-112">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="b3fba-113">Рекомендации по WIC для форматов необработанных изображений Camera</span><span class="sxs-lookup"><span data-stu-id="b3fba-113">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="b3fba-114">Написание WIC-Enabled КОДЕка</span><span class="sxs-lookup"><span data-stu-id="b3fba-114">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



