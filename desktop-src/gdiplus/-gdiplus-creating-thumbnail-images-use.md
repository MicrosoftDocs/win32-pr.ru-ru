---
description: Эскиз изображения — это небольшая версия изображения. Можно создать эскиз изображения, вызвав метод Жетсумбнаилимаже объекта Image.
ms.assetid: 96f95d00-6f96-4b8a-b84b-010203433d74
title: Создание эскизов изображений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30ac737a49bad85ecc25eeeef1266a02cdeb408f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104571515"
---
# <a name="creating-thumbnail-images"></a><span data-ttu-id="5b9ac-104">Создание эскизов изображений</span><span class="sxs-lookup"><span data-stu-id="5b9ac-104">Creating Thumbnail Images</span></span>

<span data-ttu-id="5b9ac-105">Эскиз изображения — это небольшая версия изображения.</span><span class="sxs-lookup"><span data-stu-id="5b9ac-105">A thumbnail image is a small version of an image.</span></span> <span data-ttu-id="5b9ac-106">Можно создать эскиз изображения, вызвав метод **жетсумбнаилимаже** объекта [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) .</span><span class="sxs-lookup"><span data-stu-id="5b9ac-106">You can create a thumbnail image by calling the **GetThumbnailImage** method of an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object.</span></span>

<span data-ttu-id="5b9ac-107">В следующем примере объект [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) создается на основе файла Compass.bmp.</span><span class="sxs-lookup"><span data-stu-id="5b9ac-107">The following example constructs an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object from the file Compass.bmp.</span></span> <span data-ttu-id="5b9ac-108">Исходное изображение имеет ширину 640 пикселей и высоту 479 пикселей.</span><span class="sxs-lookup"><span data-stu-id="5b9ac-108">The original image has a width of 640 pixels and a height of 479 pixels.</span></span> <span data-ttu-id="5b9ac-109">Код создает эскиз эскиза с шириной 100 пикселей и высотой 100 пикселей.</span><span class="sxs-lookup"><span data-stu-id="5b9ac-109">The code creates a thumbnail image that has a width of 100 pixels and a height of 100 pixels.</span></span>


```
Image image(L"Compass.bmp");
Image* pThumbnail = image.GetThumbnailImage(100, 100, NULL, NULL);
graphics.DrawImage(pThumbnail, 10, 10, 
   pThumbnail->GetWidth(), pThumbnail->GetHeight());
```



<span data-ttu-id="5b9ac-110">На следующем рисунке показан эскиз изображения.</span><span class="sxs-lookup"><span data-stu-id="5b9ac-110">The following illustration shows the thumbnail image.</span></span>

![Иллюстрация небольшого рисунка, показывающего компас](images/thumbnail1.png)

 

 



