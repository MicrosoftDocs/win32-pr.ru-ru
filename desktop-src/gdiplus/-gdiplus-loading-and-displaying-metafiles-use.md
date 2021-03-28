---
description: Класс Image предоставляет базовые методы для загрузки и отображения растровых изображений и векторных изображений. Класс Metafile, который наследует от класса Image, предоставляет более специализированные методы записи, отображения и проверки векторных изображений.
ms.assetid: 79b8df1b-6fc5-455b-9d08-57d64bf6bffa
title: Загрузка и отображение метафайлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5dafe6ef92e80e8487b43a22f50b44c5decd360
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072730"
---
# <a name="loading-and-displaying-metafiles"></a><span data-ttu-id="751a3-104">Загрузка и отображение метафайлов</span><span class="sxs-lookup"><span data-stu-id="751a3-104">Loading and Displaying Metafiles</span></span>

<span data-ttu-id="751a3-105">Класс [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) предоставляет базовые методы для загрузки и отображения растровых изображений и векторных изображений.</span><span class="sxs-lookup"><span data-stu-id="751a3-105">The [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class provides basic methods for loading and displaying raster images and vector images.</span></span> <span data-ttu-id="751a3-106">Класс [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) , который наследует от класса **Image** , предоставляет более специализированные методы записи, отображения и проверки векторных изображений.</span><span class="sxs-lookup"><span data-stu-id="751a3-106">The [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) class, which inherits from the **Image** class, provides more specialized methods for recording, displaying, and examining vector images.</span></span>

<span data-ttu-id="751a3-107">Для отображения векторного изображения (метафайла) на экране необходим объект [**изображения**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) и [**графический**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объект.</span><span class="sxs-lookup"><span data-stu-id="751a3-107">To display a vector image (metafile) on the screen, you need an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object and a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="751a3-108">Передайте имя файла (или указатель на поток) в конструктор **изображений** .</span><span class="sxs-lookup"><span data-stu-id="751a3-108">Pass the name of a file (or a pointer to a stream) to an **Image** constructor.</span></span> <span data-ttu-id="751a3-109">После создания объекта **Image** передайте адрес этого объекта **изображения** методу **DrawImage** **графического** объекта.</span><span class="sxs-lookup"><span data-stu-id="751a3-109">After you have created an **Image** object, pass the address of that **Image** object to the **DrawImage** method of a **Graphics** object.</span></span>

<span data-ttu-id="751a3-110">В следующем примере создается объект [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) из файла EMF (расширенный метафайл), а затем изображение рисуется с помощью левого верхнего угла в (60, 10):</span><span class="sxs-lookup"><span data-stu-id="751a3-110">The following example creates an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object from an EMF (enhanced metafile) file and then draws the image with its upper-left corner at (60, 10):</span></span>


```
Image image(L"SampleMetafile.emf");
graphics.DrawImage(&image, 60, 10);
```



<span data-ttu-id="751a3-111">На следующем рисунке показано изображение, отображаемое в указанном месте.</span><span class="sxs-lookup"><span data-stu-id="751a3-111">The following illustration shows the image drawn at the specified location.</span></span>

![снимок экрана окна, содержащего изображение и указывающее точку отсчета](images/imageposition2.png)

 

 



