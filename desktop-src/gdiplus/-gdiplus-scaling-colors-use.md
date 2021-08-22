---
description: Преобразование «масштабирование» умножает один или несколько четырех компонентов цвета на число. В следующей таблице приведены записи цветовой матрицы, представляющие масштабирование.
ms.assetid: 08347831-7100-4220-a83b-693bb7b98ccb
title: Масштабирование цветов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7877db07ff1a11dcb985f8b0ca8ec3cc017f25fe45f00e989c9108891f8ff1ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036372"
---
# <a name="scaling-colors"></a>Масштабирование цветов

Преобразование «масштабирование» умножает один или несколько четырех компонентов цвета на число. В следующей таблице приведены записи цветовой матрицы, представляющие масштабирование.



| Масштабируемый компонент | Запись матрицы |
|------------------------|--------------|
| Красный                    | \[0 \] \[ 0\]   |
| Зеленый                  | \[1 \] \[ 1\]   |
| Синий                   | \[2 \] \[ 2\]   |
| Коэффициент альфа                  | \[3 \] \[ 3\]   |



 

В следующем примере объект [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) создается на основе файла ColorBars2.bmp. Затем код масштабирует синий компонент каждого пикселя изображения на коэффициент, равный 2. Исходное изображение отображается вместе с преобразованным изображением.


```
Image            image(L"ColorBars2.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();

ColorMatrix colorMatrix = {
   1.0f, 0.0f, 0.0f, 0.0f, 0.0f,
   0.0f, 1.0f, 0.0f, 0.0f, 0.0f,
   0.0f, 0.0f, 2.0f, 0.0f, 0.0f,
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



На следующем рисунке показано исходное изображение слева и масштабированное изображение справа.

![Показывает четыре цветные полосы, а затем те же линии с разными цветами.](images/colortrans3.png)

В следующей таблице показаны цветовые векторы для четырех полос до и после синего масштабирования. Обратите внимание, что синий компонент на четвертой цветовой полосе перешел с 0,8 на 0,6. это связано с тем, что GDI+ оставляет только дробную часть результата. Например, (2) (0,8) = 1,6, а дробная часть 1,6 — 0,6. Сохранение только дробной части гарантирует, что результат всегда находится в диапазоне \[ 0, 1 \] .



| Исходное значение           | Масштабировать             |
|--------------------|--------------------|
| (0.4, 0.4, 0.4, 1) | (0.4, 0.4, 0.8, 1) |
| (0.4, 0.2, 0.2, 1) | (0.4, 0.2, 0.4, 1) |
| (0.2, 0.4, 0.2, 1) | (0.2, 0.4, 0.4, 1) |
| (0.4, 0.4, 0.8, 1) | (0.4, 0.4, 0.6, 1) |



 

В следующем примере объект [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) создается на основе файла ColorBars2.bmp. Затем код масштабирует красный, зеленый и синий компоненты каждого пикселя в изображении. Красные компоненты масштабируются на 25 процентов, а зеленые — на 35 процентов, а синие — на 50 процентов.


```
Image            image(L"ColorBars.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();

ColorMatrix colorMatrix = {
   0.75f, 0.0f,  0.0f, 0.0f, 0.0f,
   0.0f,  0.65f, 0.0f, 0.0f, 0.0f,
   0.0f,  0.0f,  0.5f, 0.0f, 0.0f,
   0.0f,  0.0f,  0.0f, 1.0f, 0.0f,
   0.0f,  0.0f,  0.0f, 0.0f, 1.0f};
   
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



На следующем рисунке показано исходное изображение слева и масштабированное изображение справа.

![Иллюстрация с четырьмя цветовыми полосами, а затем с разными цветами](images/colortrans4.png)

В следующей таблице показаны цветовые векторы для четырех полос до и после красного, зеленого и синего масштабирования.



| Исходное значение           | Масштабировать               |
|--------------------|----------------------|
| (0.6, 0.6, 0.6, 1) | (0.45, 0.39, 0.3, 1) |
| (0, 1, 1, 1)       | (0, 0.65, 0.5, 1)    |
| (1, 1, 0, 1)       | (0.75, 0.65, 0, 1)   |
| (1, 0, 1, 1)       | (0.75, 0, 0.5, 1)    |



 

 

 



