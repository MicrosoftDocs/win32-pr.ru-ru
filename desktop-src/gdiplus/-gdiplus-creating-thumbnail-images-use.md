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
# <a name="creating-thumbnail-images"></a>Создание эскизов изображений

Эскиз изображения — это небольшая версия изображения. Можно создать эскиз изображения, вызвав метод **жетсумбнаилимаже** объекта [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) .

В следующем примере объект [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) создается на основе файла Compass.bmp. Исходное изображение имеет ширину 640 пикселей и высоту 479 пикселей. Код создает эскиз эскиза с шириной 100 пикселей и высотой 100 пикселей.


```
Image image(L"Compass.bmp");
Image* pThumbnail = image.GetThumbnailImage(100, 100, NULL, NULL);
graphics.DrawImage(pThumbnail, 10, 10, 
   pThumbnail->GetWidth(), pThumbnail->GetHeight());
```



На следующем рисунке показан эскиз изображения.

![Иллюстрация небольшого рисунка, показывающего компас](images/thumbnail1.png)

 

 



