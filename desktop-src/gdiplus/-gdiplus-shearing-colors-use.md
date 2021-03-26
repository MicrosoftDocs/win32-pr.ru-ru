---
description: Наклон увеличивает или уменьшает компонент цвета на величину, пропорциональную другому компоненту цвета.
ms.assetid: 12f83f35-33f1-4ac9-b45d-f8700e54053a
title: Наклон цветов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4d632fded9f2b4d1e4682ae9f8ffbfedee85a46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156178"
---
# <a name="shearing-colors"></a>Наклон цветов

Наклон увеличивает или уменьшает компонент цвета на величину, пропорциональную другому компоненту цвета. Например, рассмотрим преобразование, при котором красный компонент увеличивается на одну половину значения синего компонента. При таком преобразовании цвет (0,2, 0,5, 1) станет равен (0,7, 0,5, 1). Новый красный компонент — 0,2 + (1/2) (1) = 0,7.

В следующем примере объект [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) создается на основе файла ColorBars4.bmp. Затем код применяет преобразование «наклонное», описанное в предыдущем абзаце, к каждому пикселу изображения.


```
Image            image(L"ColorBars4.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();

ColorMatrix colorMatrix = {
   1.0f, 0.0f, 0.0f, 0.0f, 0.0f,
   0.0f, 1.0f, 0.0f, 0.0f, 0.0f,
   0.5f, 0.0f, 1.0f, 0.0f, 0.0f,
   0.0f, 0.0f, 0.0f, 1.0f, 0.0f,
   0.0f, 0.0f, 0.0f, 0.0f, 1.0f};
   
imageAttributes.SetColorMatrix(
   &colorMatrix, 
   ColorMatrixFlagsDefault,
   ColorAdjustTypeBitmap);
   
graphics.DrawImage(&image, 10, 10, width, height);

graphics.DrawImage(
   &image, 
   Rect(150, 10, width, height),  // destination rectangle 
   0, 0,        // upper-left corner of source rectangle 
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel,
   &imageAttributes);
```



На следующем рисунке показано исходное изображение слева и наклонное изображение справа.

![Иллюстрация, на которой показаны четыре цветные полосы, а затем те же линии с разными цветами](images/colortrans6.png)

В следующей таблице показаны цветовые векторы для четырех полос до и после преобразования «наклон».



| До преобразования           | С наклоном            |
|--------------------|--------------------|
| (0, 0, 1, 1)       | (0.5, 0, 1, 1)     |
| (0.5, 1, 0.5, 1)   | (0.75, 1, 0.5, 1)  |
| (1, 1, 0, 1)       | (1, 1, 0, 1)       |
| (0.4, 0.4, 0.4, 1) | (0.6, 0.4, 0.4, 1) |



 

 

 



