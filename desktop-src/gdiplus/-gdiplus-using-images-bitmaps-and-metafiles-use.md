---
description: Сведения об использовании изображений, точечных рисунков и метафайлов. Windows GDI+ предоставляет класс Image для работы с растровыми изображениями (точечными рисунками) и векторными изображениями (метафайлы).
ms.assetid: 57e3bf33-5490-4f4a-addf-356ef8f1aeed
title: Использование изображений, точечных рисунков и метафайлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49d0603c8a428c45feac8cdeb47a46b61dc5e3bd
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395539"
---
# <a name="using-images-bitmaps-and-metafiles"></a><span data-ttu-id="4e7b1-104">Использование изображений, точечных рисунков и метафайлов</span><span class="sxs-lookup"><span data-stu-id="4e7b1-104">Using Images, Bitmaps, and Metafiles</span></span>

<span data-ttu-id="4e7b1-105">Windows GDI+ предоставляет класс [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) для работы с растровыми изображениями (точечными рисунками) и векторными изображениями (метафайлы).</span><span class="sxs-lookup"><span data-stu-id="4e7b1-105">Windows GDI+ provides the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class for working with raster images (bitmaps) and vector images (metafiles).</span></span> <span data-ttu-id="4e7b1-106">Класс [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) и класс [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) наследуют от класса **Image** .</span><span class="sxs-lookup"><span data-stu-id="4e7b1-106">The [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) class and the [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) class both inherit from the **Image** class.</span></span> <span data-ttu-id="4e7b1-107">Класс **Bitmap** расширяет возможности класса **Image** , предоставляя дополнительные методы для загрузки, сохранения и манипулирования растровыми изображениями.</span><span class="sxs-lookup"><span data-stu-id="4e7b1-107">The **Bitmap** class expands on the capabilities of the **Image** class by providing additional methods for loading, saving, and manipulating raster images.</span></span> <span data-ttu-id="4e7b1-108">Класс **Metafile** расширяет возможности класса **Image** , предоставляя дополнительные методы для записи и проверки векторных изображений.</span><span class="sxs-lookup"><span data-stu-id="4e7b1-108">The **Metafile** class expands on the capabilities of the **Image** class by providing additional methods for recording and examining vector images.</span></span>

<span data-ttu-id="4e7b1-109">В следующих разделах рассматриваются классы [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image), [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap)и [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) более подробно:</span><span class="sxs-lookup"><span data-stu-id="4e7b1-109">The following topics cover the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image), [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap), and [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) classes in more detail:</span></span>

-   [<span data-ttu-id="4e7b1-110">Загрузка и отображение растровых изображений</span><span class="sxs-lookup"><span data-stu-id="4e7b1-110">Loading and Displaying Bitmaps</span></span>](-gdiplus-loading-and-displaying-bitmaps-use.md)
-   [<span data-ttu-id="4e7b1-111">Загрузка и отображение метафайлов</span><span class="sxs-lookup"><span data-stu-id="4e7b1-111">Loading and Displaying Metafiles</span></span>](-gdiplus-loading-and-displaying-metafiles-use.md)
-   [<span data-ttu-id="4e7b1-112">Запись метафайлов</span><span class="sxs-lookup"><span data-stu-id="4e7b1-112">Recording Metafiles</span></span>](-gdiplus-recording-metafiles-use.md)
-   [<span data-ttu-id="4e7b1-113">Обрезка и масштабирование изображений</span><span class="sxs-lookup"><span data-stu-id="4e7b1-113">Cropping and Scaling Images</span></span>](-gdiplus-cropping-and-scaling-images-use.md)
-   [<span data-ttu-id="4e7b1-114">Вращение, отражение и наклон изображений</span><span class="sxs-lookup"><span data-stu-id="4e7b1-114">Rotating, Reflecting, and Skewing Images</span></span>](-gdiplus-rotating-reflecting-and-skewing-images-use.md)
-   [<span data-ttu-id="4e7b1-115">Использование режима интерполяции для управления качеством изображения во время масштабирования</span><span class="sxs-lookup"><span data-stu-id="4e7b1-115">Using Interpolation Mode to Control Image Quality During Scaling</span></span>](-gdiplus-using-interpolation-mode-to-control-image-quality-during-scaling-use.md)
-   [<span data-ttu-id="4e7b1-116">Создание эскизов изображений</span><span class="sxs-lookup"><span data-stu-id="4e7b1-116">Creating Thumbnail Images</span></span>](-gdiplus-creating-thumbnail-images-use.md)
-   [<span data-ttu-id="4e7b1-117">Использование кэшированного точечного рисунка для повышения производительности</span><span class="sxs-lookup"><span data-stu-id="4e7b1-117">Using a Cached Bitmap to Improve Performance</span></span>](-gdiplus-using-a-cached-bitmap-to-improve-performance-use.md)
-   [<span data-ttu-id="4e7b1-118">Повышение производительности за счет предотвращения автоматического масштабирования</span><span class="sxs-lookup"><span data-stu-id="4e7b1-118">Improving Performance by Avoiding Automatic Scaling</span></span>](-gdiplus-improving-performance-by-avoiding-automatic-scaling-use.md)
-   [<span data-ttu-id="4e7b1-119">Чтение и запись метаданных</span><span class="sxs-lookup"><span data-stu-id="4e7b1-119">Reading and Writing Metadata</span></span>](-gdiplus-reading-and-writing-metadata-use.md)

 

 



