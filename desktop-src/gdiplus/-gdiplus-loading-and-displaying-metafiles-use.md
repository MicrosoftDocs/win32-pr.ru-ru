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
# <a name="loading-and-displaying-metafiles"></a>Загрузка и отображение метафайлов

Класс [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) предоставляет базовые методы для загрузки и отображения растровых изображений и векторных изображений. Класс [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) , который наследует от класса **Image** , предоставляет более специализированные методы записи, отображения и проверки векторных изображений.

Для отображения векторного изображения (метафайла) на экране необходим объект [**изображения**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) и [**графический**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объект. Передайте имя файла (или указатель на поток) в конструктор **изображений** . После создания объекта **Image** передайте адрес этого объекта **изображения** методу **DrawImage** **графического** объекта.

В следующем примере создается объект [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) из файла EMF (расширенный метафайл), а затем изображение рисуется с помощью левого верхнего угла в (60, 10):


```
Image image(L"SampleMetafile.emf");
graphics.DrawImage(&image, 60, 10);
```



На следующем рисунке показано изображение, отображаемое в указанном месте.

![снимок экрана окна, содержащего изображение и указывающее точку отсчета](images/imageposition2.png)

 

 



