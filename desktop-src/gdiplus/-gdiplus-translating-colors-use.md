---
description: Перевод добавляет значение к одному или нескольким из четырех компонентов цвета. В следующей таблице приведены записи цветовой матрицы, представляющие переводы.
ms.assetid: a0d89989-9b98-42fb-8d87-206581e3c91e
title: Преобразование цветов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c769a24c02e977c3e32ff913852d4b6b8d54441
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104563684"
---
# <a name="translating-colors"></a>Преобразование цветов

Перевод добавляет значение к одному или нескольким из четырех компонентов цвета. В следующей таблице приведены записи цветовой матрицы, представляющие переводы.



| Преобразуемый компонент | Запись матрицы |
|----------------------------|--------------|
| Красный                        | \[4 \] \[ 0\]   |
| Зеленый                      | \[4 \] \[ 1\]   |
| Синий                       | \[4 \] \[ 2\]   |
| Коэффициент альфа                      | \[4 \] \[ 3\]   |



 

В следующем примере объект [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) создается на основе файла ColorBars.bmp. Затем код добавляет 0,75 к красному компоненту каждого пикселя в изображении. Исходное изображение отображается вместе с преобразованным изображением.


```
Image            image(L"ColorBars.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();

ColorMatrix colorMatrix = {
   1.0f,  0.0f, 0.0f, 0.0f, 0.0f,
   0.0f,  1.0f, 0.0f, 0.0f, 0.0f,
   0.0f,  0.0f, 1.0f, 0.0f, 0.0f,
   0.0f,  0.0f, 0.0f, 1.0f, 0.0f,
   0.75f, 0.0f, 0.0f, 0.0f, 1.0f};
   
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



На следующем рисунке показано исходное изображение слева и преобразованное изображение справа.

![Иллюстрация, на которой показаны четыре цветные полосы, а затем те же линии с разными цветами](images/colortrans2.png)

В следующей таблице перечислены цветовые векторы для четырех полос до и после Красной трансляции. Обратите внимание, что поскольку максимальное значение для компонента цвета равно 1, красный компонент во второй строке не изменяется. (Аналогичным образом, минимальное значение для компонента цвета равно 0.)



| До преобразования           | Переведенный текст      |
|--------------------|-----------------|
| Черный (0, 0, 0, 1) | (0.75, 0, 0, 1) |
| Красный (1, 0, 0, 1)   | (1, 0, 0, 1)    |
| Зеленый (0, 1, 0, 1) | (0.75, 1, 0, 1) |
| Blue (0, 0, 1, 1)  | (0.75, 0, 1, 1) |



 

 

 



