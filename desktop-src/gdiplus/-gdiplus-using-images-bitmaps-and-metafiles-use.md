---
description: Windows GDI+ предоставляет класс Image для работы с растровыми изображениями (точечными рисунками) и векторными изображениями (метафайлы).
ms.assetid: 57e3bf33-5490-4f4a-addf-356ef8f1aeed
title: Использование изображений, точечных рисунков и метафайлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 445b37caa488fa4b83bcfb7792eb83f6ee1e6e75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080628"
---
# <a name="using-images-bitmaps-and-metafiles"></a><span data-ttu-id="af6d2-103">Использование изображений, точечных рисунков и метафайлов</span><span class="sxs-lookup"><span data-stu-id="af6d2-103">Using Images, Bitmaps, and Metafiles</span></span>

<span data-ttu-id="af6d2-104">Windows GDI+ предоставляет класс [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) для работы с растровыми изображениями (точечными рисунками) и векторными изображениями (метафайлы).</span><span class="sxs-lookup"><span data-stu-id="af6d2-104">Windows GDI+ provides the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class for working with raster images (bitmaps) and vector images (metafiles).</span></span> <span data-ttu-id="af6d2-105">Класс [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) и класс [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) наследуют от класса **Image** .</span><span class="sxs-lookup"><span data-stu-id="af6d2-105">The [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) class and the [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) class both inherit from the **Image** class.</span></span> <span data-ttu-id="af6d2-106">Класс **Bitmap** расширяет возможности класса **Image** , предоставляя дополнительные методы для загрузки, сохранения и манипулирования растровыми изображениями.</span><span class="sxs-lookup"><span data-stu-id="af6d2-106">The **Bitmap** class expands on the capabilities of the **Image** class by providing additional methods for loading, saving, and manipulating raster images.</span></span> <span data-ttu-id="af6d2-107">Класс **Metafile** расширяет возможности класса **Image** , предоставляя дополнительные методы для записи и проверки векторных изображений.</span><span class="sxs-lookup"><span data-stu-id="af6d2-107">The **Metafile** class expands on the capabilities of the **Image** class by providing additional methods for recording and examining vector images.</span></span>

<span data-ttu-id="af6d2-108">В следующих разделах рассматриваются классы [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image), [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap)и [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) более подробно:</span><span class="sxs-lookup"><span data-stu-id="af6d2-108">The following topics cover the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image), [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap), and [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) classes in more detail:</span></span>

-   [<span data-ttu-id="af6d2-109">Загрузка и отображение растровых изображений</span><span class="sxs-lookup"><span data-stu-id="af6d2-109">Loading and Displaying Bitmaps</span></span>](-gdiplus-loading-and-displaying-bitmaps-use.md)
-   [<span data-ttu-id="af6d2-110">Загрузка и отображение метафайлов</span><span class="sxs-lookup"><span data-stu-id="af6d2-110">Loading and Displaying Metafiles</span></span>](-gdiplus-loading-and-displaying-metafiles-use.md)
-   [<span data-ttu-id="af6d2-111">Запись метафайлов</span><span class="sxs-lookup"><span data-stu-id="af6d2-111">Recording Metafiles</span></span>](-gdiplus-recording-metafiles-use.md)
-   [<span data-ttu-id="af6d2-112">Обрезка и масштабирование изображений</span><span class="sxs-lookup"><span data-stu-id="af6d2-112">Cropping and Scaling Images</span></span>](-gdiplus-cropping-and-scaling-images-use.md)
-   [<span data-ttu-id="af6d2-113">Вращение, отражение и наклон изображений</span><span class="sxs-lookup"><span data-stu-id="af6d2-113">Rotating, Reflecting, and Skewing Images</span></span>](-gdiplus-rotating-reflecting-and-skewing-images-use.md)
-   [<span data-ttu-id="af6d2-114">Использование режима интерполяции для управления качеством изображения во время масштабирования</span><span class="sxs-lookup"><span data-stu-id="af6d2-114">Using Interpolation Mode to Control Image Quality During Scaling</span></span>](-gdiplus-using-interpolation-mode-to-control-image-quality-during-scaling-use.md)
-   [<span data-ttu-id="af6d2-115">Создание эскизов изображений</span><span class="sxs-lookup"><span data-stu-id="af6d2-115">Creating Thumbnail Images</span></span>](-gdiplus-creating-thumbnail-images-use.md)
-   [<span data-ttu-id="af6d2-116">Использование кэшированного точечного рисунка для повышения производительности</span><span class="sxs-lookup"><span data-stu-id="af6d2-116">Using a Cached Bitmap to Improve Performance</span></span>](-gdiplus-using-a-cached-bitmap-to-improve-performance-use.md)
-   [<span data-ttu-id="af6d2-117">Повышение производительности за счет предотвращения автоматического масштабирования</span><span class="sxs-lookup"><span data-stu-id="af6d2-117">Improving Performance by Avoiding Automatic Scaling</span></span>](-gdiplus-improving-performance-by-avoiding-automatic-scaling-use.md)
-   [<span data-ttu-id="af6d2-118">Чтение и запись метаданных</span><span class="sxs-lookup"><span data-stu-id="af6d2-118">Reading and Writing Metadata</span></span>](-gdiplus-reading-and-writing-metadata-use.md)

 

 



