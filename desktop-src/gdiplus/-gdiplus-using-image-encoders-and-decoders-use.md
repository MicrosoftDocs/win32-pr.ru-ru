---
description: Windows GDI+ предоставляет класс Image и класс Bitmap для хранения изображений в памяти и манипуляции изображениями в памяти.
ms.assetid: f9a5b4b1-4e25-42c8-a96b-a3104841e5f3
title: Использование кодировщиков и декодеров изображений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40c55c75e00b3d624d27ba888ae26afb3a5ee0fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144854"
---
# <a name="using-image-encoders-and-decoders"></a><span data-ttu-id="b9fe2-103">Использование кодировщиков и декодеров изображений</span><span class="sxs-lookup"><span data-stu-id="b9fe2-103">Using Image Encoders and Decoders</span></span>

<span data-ttu-id="b9fe2-104">Windows GDI+ предоставляет класс [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) и класс [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) для хранения изображений в памяти и манипуляции изображениями в памяти.</span><span class="sxs-lookup"><span data-stu-id="b9fe2-104">Windows GDI+ provides the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class and the [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) class for storing images in memory and manipulating images in memory.</span></span> <span data-ttu-id="b9fe2-105">GDI+ записывает изображения на дисковые файлы с помощью кодировщиков изображений и загружает изображения с дисковых файлов с помощью декодеров изображений.</span><span class="sxs-lookup"><span data-stu-id="b9fe2-105">GDI+ writes images to disk files with the help of image encoders and loads images from disk files with the help of image decoders.</span></span> <span data-ttu-id="b9fe2-106">Кодировщик преобразует данные в **образе** или **растровом** объекте в указанный формат дискового файла.</span><span class="sxs-lookup"><span data-stu-id="b9fe2-106">An encoder translates the data in an **Image** or **Bitmap** object into a designated disk file format.</span></span> <span data-ttu-id="b9fe2-107">Декодер преобразует данные в файле на диске в формат, необходимый для **растровых** объектов **Image** и Bitmap.</span><span class="sxs-lookup"><span data-stu-id="b9fe2-107">A decoder translates the data in a disk file to the format required by the **Image** and **Bitmap** objects.</span></span> <span data-ttu-id="b9fe2-108">В GDI+ есть встроенные кодировщики и декодеры, поддерживающие файлы следующих типов:</span><span class="sxs-lookup"><span data-stu-id="b9fe2-108">GDI+ has built-in encoders and decoders that support the following file types:</span></span>

-   <span data-ttu-id="b9fe2-109">BMP</span><span class="sxs-lookup"><span data-stu-id="b9fe2-109">BMP</span></span>
-   <span data-ttu-id="b9fe2-110">GIF</span><span class="sxs-lookup"><span data-stu-id="b9fe2-110">GIF</span></span>
-   <span data-ttu-id="b9fe2-111">JPEG</span><span class="sxs-lookup"><span data-stu-id="b9fe2-111">JPEG</span></span>
-   <span data-ttu-id="b9fe2-112">PNG</span><span class="sxs-lookup"><span data-stu-id="b9fe2-112">PNG</span></span>
-   <span data-ttu-id="b9fe2-113">TIFF</span><span class="sxs-lookup"><span data-stu-id="b9fe2-113">TIFF</span></span>

<span data-ttu-id="b9fe2-114">В GDI+ также встроены встроенные декодеры, поддерживающие файлы следующих типов:</span><span class="sxs-lookup"><span data-stu-id="b9fe2-114">GDI+ also has built-in decoders that support the following file types:</span></span>

-   <span data-ttu-id="b9fe2-115">WMF</span><span class="sxs-lookup"><span data-stu-id="b9fe2-115">WMF</span></span>
-   <span data-ttu-id="b9fe2-116">EMF</span><span class="sxs-lookup"><span data-stu-id="b9fe2-116">EMF</span></span>
-   <span data-ttu-id="b9fe2-117">ЗНАЧОК</span><span class="sxs-lookup"><span data-stu-id="b9fe2-117">ICON</span></span>

<span data-ttu-id="b9fe2-118">В следующих разделах более подробно обсуждаются кодировщики и декодеры:</span><span class="sxs-lookup"><span data-stu-id="b9fe2-118">The following topics discuss encoders and decoders in more detail:</span></span>

-   [<span data-ttu-id="b9fe2-119">Список установленных кодировщиков</span><span class="sxs-lookup"><span data-stu-id="b9fe2-119">Listing Installed Encoders</span></span>](-gdiplus-listing-installed-encoders-use.md)
-   [<span data-ttu-id="b9fe2-120">Список установленных декодеров</span><span class="sxs-lookup"><span data-stu-id="b9fe2-120">Listing Installed Decoders</span></span>](-gdiplus-listing-installed-decoders-use.md)
-   [<span data-ttu-id="b9fe2-121">Получение идентификатора класса для кодировщика</span><span class="sxs-lookup"><span data-stu-id="b9fe2-121">Retrieving the Class Identifier for an Encoder</span></span>](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md)
-   [<span data-ttu-id="b9fe2-122">Определение параметров, поддерживаемых кодировщиком</span><span class="sxs-lookup"><span data-stu-id="b9fe2-122">Determining the Parameters Supported by an Encoder</span></span>](-gdiplus-determining-the-parameters-supported-by-an-encoder-use.md)
-   [<span data-ttu-id="b9fe2-123">Преобразование изображения BMP в изображение PNG</span><span class="sxs-lookup"><span data-stu-id="b9fe2-123">Converting a BMP Image to a PNG Image</span></span>](-gdiplus-converting-a-bmp-image-to-a-png-image-use.md)
-   [<span data-ttu-id="b9fe2-124">Задание уровня сжатия JPEG</span><span class="sxs-lookup"><span data-stu-id="b9fe2-124">Setting JPEG Compression Level</span></span>](-gdiplus-setting-jpeg-compression-level-use.md)
-   [<span data-ttu-id="b9fe2-125">Преобразование изображения JPEG без потери информации</span><span class="sxs-lookup"><span data-stu-id="b9fe2-125">Transforming a JPEG Image Without Loss of Information</span></span>](-gdiplus-transforming-a-jpeg-image-without-loss-of-information-use.md)
-   [<span data-ttu-id="b9fe2-126">Создание и сохранение многокадрового изображения</span><span class="sxs-lookup"><span data-stu-id="b9fe2-126">Creating and Saving a Multiple-Frame Image</span></span>](-gdiplus-creating-and-saving-a-multiple-frame-image-use.md)
-   [<span data-ttu-id="b9fe2-127">Копирование отдельных кадров из образа Multiple-Frame</span><span class="sxs-lookup"><span data-stu-id="b9fe2-127">Copying Individual Frames from a Multiple-Frame Image</span></span>](-gdiplus-copying-individual-frames-from-a-multiple-frame-image-use.md)

 

 



