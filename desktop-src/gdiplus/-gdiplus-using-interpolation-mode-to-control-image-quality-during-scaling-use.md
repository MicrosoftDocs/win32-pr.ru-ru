---
description: Режим интерполяции объекта Graphics влияет на способ масштабирования изображений Windows GDI+ (растяжения и сжатие).
ms.assetid: 3aeead47-78da-4ab3-9126-2fbe9e341e48
title: Использование режима интерполяции для управления качеством изображения во время масштабирования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d34a829f2edf2f341f50bee771d909f7c4eef98e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984425"
---
# <a name="using-interpolation-mode-to-control-image-quality-during-scaling"></a>Использование режима интерполяции для управления качеством изображения во время масштабирования

Режим интерполяции объекта [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) влияет на способ масштабирования изображений Windows GDI+ (растяжения и сжатие). Перечисление [**интерполатионмоде**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-interpolationmode) в гдиплусенумс. h определяет несколько режимов интерполяции, некоторые из которых показаны в следующем списке:

-   интерполатионмоденеарестнеигхбор
-   интерполатионмодебилинеар
-   интерполатионмодехигхкуалитибилинеар
-   интерполатионмодебикубик
-   интерполатионмодехигхкуалитибикубик

Чтобы растянуть изображение, каждый пиксель в исходном изображении должен быть сопоставлен с группой пикселей в увеличенном изображении. Чтобы сжать изображение, группы пикселей в исходном изображении должны быть сопоставлены с отдельными пикселями в меньшем изображении. Эффективность алгоритмов, выполняющих эти сопоставления, определяет качество масштабируемого изображения. Алгоритмы, создающие масштабируемые изображения высокого качества, обычно занимают больше времени на обработку. В приведенном выше списке Интерполатионмоденеарестнеигхбор — это режим самого низкого качества, а Интерполатионмодехигхкуалитибикубик — режим самого высокого качества.

Чтобы задать режим интерполяции, передайте один из членов перечисления [**интерполатионмоде**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-interpolationmode) методу **сетинтерполатионмоде** объекта [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .

В следующем примере изображение рисуется, а затем сжимается с помощью трех различных режимов интерполяции:


```
Image image(L"GrapeBunch.bmp");
UINT width = image.GetWidth();
UINT height = image.GetHeight();
// Draw the image with no shrinking or stretching.
graphics.DrawImage(
   &image,
   Rect(10, 10, width, height),  // destination rectangle  
   0, 0,        // upper-left corner of source rectangle
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel);
// Shrink the image using low-quality interpolation. 
graphics.SetInterpolationMode(InterpolationModeNearestNeighbor);
graphics.DrawImage(
   &image,
   Rect(10, 250, 0.6*width, 0.6*height),  // destination rectangle 
   0, 0,        // upper-left corner of source rectangle
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel);
// Shrink the image using medium-quality interpolation.
graphics.SetInterpolationMode(InterpolationModeHighQualityBilinear);
graphics.DrawImage(
   &image,
   Rect(150, 250, 0.6 * width, 0.6 * height),  // destination rectangle 
   0, 0,        // upper-left corner of source rectangle
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel);
// Shrink the image using high-quality interpolation.
graphics.SetInterpolationMode(InterpolationModeHighQualityBicubic);
graphics.DrawImage(
   &image,
   Rect(290, 250, 0.6 * width, 0.6 * height),  // destination rectangle 
   0, 0,        // upper-left corner of source rectangle
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel);
```



На следующем рисунке показано исходное изображение и три изображения меньшего размера.

![Иллюстрация с большим исходным изображением и тремя мелкими изображениями разного качества](images/grapes1.png)

 

 



