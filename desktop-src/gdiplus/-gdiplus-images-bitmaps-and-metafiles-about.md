---
description: Windows GDI+ предоставляет класс Image для работы с растровыми изображениями (точечными рисунками) и векторными изображениями (метафайлы).
ms.assetid: ddde257c-41a6-4f6e-8d81-10d66c60085c
title: Работа с растровыми и векторными изображениями с использованием классов Image, Bitmap и Metafile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75c3c0e88226bc32619a8f0fc03f8c25f2963cd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080633"
---
# <a name="images-bitmaps-and-metafiles"></a><span data-ttu-id="f9a94-103">Работа с растровыми и векторными изображениями с использованием классов Image, Bitmap и Metafile</span><span class="sxs-lookup"><span data-stu-id="f9a94-103">Images, Bitmaps, and Metafiles</span></span>

<span data-ttu-id="f9a94-104">Windows GDI+ предоставляет класс [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) для работы с растровыми изображениями (точечными рисунками) и векторными изображениями (метафайлы).</span><span class="sxs-lookup"><span data-stu-id="f9a94-104">Windows GDI+ provides the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class for working with raster images (bitmaps) and vector images (metafiles).</span></span> <span data-ttu-id="f9a94-105">Класс [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) и класс [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) наследуют от класса **Image** .</span><span class="sxs-lookup"><span data-stu-id="f9a94-105">The [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) class and the [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) class both inherit from the **Image** class.</span></span> <span data-ttu-id="f9a94-106">Класс **Bitmap** расширяет возможности класса **Image** , предоставляя дополнительные методы для загрузки, сохранения и манипулирования растровыми изображениями.</span><span class="sxs-lookup"><span data-stu-id="f9a94-106">The **Bitmap** class expands on the capabilities of the **Image** class by providing additional methods for loading, saving, and manipulating raster images.</span></span> <span data-ttu-id="f9a94-107">Класс **Metafile** расширяет возможности класса **Image** , предоставляя дополнительные методы для записи и проверки векторных изображений.</span><span class="sxs-lookup"><span data-stu-id="f9a94-107">The **Metafile** class expands on the capabilities of the **Image** class by providing additional methods for recording and examining vector images.</span></span>

-   [<span data-ttu-id="f9a94-108">Типы точечных рисунков</span><span class="sxs-lookup"><span data-stu-id="f9a94-108">Types of Bitmaps</span></span>](-gdiplus-types-of-bitmaps-about.md)
-   [<span data-ttu-id="f9a94-109">Метафайлы</span><span class="sxs-lookup"><span data-stu-id="f9a94-109">Metafiles</span></span>](-gdiplus-metafiles-about.md)
-   [<span data-ttu-id="f9a94-110">Отрисовка, позиционирование и клонирование изображений</span><span class="sxs-lookup"><span data-stu-id="f9a94-110">Drawing, Positioning, and Cloning Images</span></span>](-gdiplus-drawing-positioning-and-cloning-images-about.md)
-   [<span data-ttu-id="f9a94-111">Обрезка и масштабирование изображений</span><span class="sxs-lookup"><span data-stu-id="f9a94-111">Cropping and Scaling Images</span></span>](-gdiplus-cropping-and-scaling-images-about.md)

 

 



