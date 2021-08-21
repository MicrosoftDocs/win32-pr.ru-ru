---
title: Сведения об обрезке и масштабировании изображений GDI+
description: Для рисования и позиционирования изображений можно использовать метод DrawImage класса Graphics.
ms.assetid: 81d20adc-0481-4b1b-80aa-ae218fdecd84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9e69adb7f817c36b955ed313290cf0b762c279b4296e06ad52aa6175ff2c467
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036842"
---
# <a name="about-cropping-and-scaling-gdi-images"></a>Сведения об обрезке и масштабировании изображений GDI+

Для рисования и позиционирования изображений можно использовать метод [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) класса [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . Метод DrawImage является перегруженным методом, поэтому его можно указать несколькими способами. Один из вариаций метода [**Graphics::D равимаже**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) получает адрес объекта [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) и ссылку на объект [**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) . Прямоугольник задает назначение для операции рисования. то есть он указывает прямоугольник, в котором будет нарисован изображение. Если размер конечного прямоугольника отличается от размера исходного изображения, изображение масштабируется в соответствии с конечным прямоугольником. В следующем примере один и тот же образ рисуется три раза: один раз без масштабирования, один раз с расширением и один раз с сжатием.


```
Bitmap myBitmap(L"Spiral.png");
Rect expansionRect(80, 10, 2 * myBitmap.GetWidth(), myBitmap.GetHeight());
Rect compressionRect(210, 10, myBitmap.GetWidth() / 2, 
   myBitmap.GetHeight() / 2);

myGraphics.DrawImage(&myBitmap, 10, 10);
myGraphics.DrawImage(&myBitmap, expansionRect);
myGraphics.DrawImage(&myBitmap, compressionRect);
```



Приведенный выше код, а также определенный файл Spiral.png, выдают следующие выходные данные.

![Иллюстрация, отображающая три версии изображения: обычная, растянута в ширину и сжата до половины исходного размера](images/aboutgdip03-art06.png)

Некоторые разновидности метода [**Graphics::D равимаже**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) имеют параметр исходного прямоугольника, а также параметр конечного прямоугольника. Исходный прямоугольник определяет часть исходного изображения, которая будет изображена. Прямоугольник назначения определяет, где будет отображаться эта часть изображения. Если размер конечного прямоугольника отличается от размера исходного прямоугольника, изображение масштабируется в соответствии с конечным прямоугольником.

В следующем примере объект [**Bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) создается из файла Runner.jpg. Изображение целиком рисуется без масштабирования в (0, 0). Затем небольшая часть изображения рисуется дважды: один раз с сжатием и один раз с расширением.


```
Bitmap myBitmap(L"Runner.jpg"); 

// The rectangle (in myBitmap) with upper-left corner (80, 70), 
// width 80, and height 45, encloses one of the runner's hands.

// Small destination rectangle for compressed hand.
Rect destRect1(200, 10, 20, 16);

// Large destination rectangle for expanded hand.
Rect destRect2(200, 40, 200, 160);

// Draw the original image at (0, 0).
myGraphics.DrawImage(&myBitmap, 0, 0);

// Draw the compressed hand.
myGraphics.DrawImage(
   &myBitmap, destRect1, 80, 70, 80, 45, UnitPixel);

// Draw the expanded hand. 
myGraphics.DrawImage(
   &myBitmap, destRect2, 80, 70, 80, 45, UnitPixel);
```



На следующем рисунке показано немасштабированное изображение, а также сжатые и развернутые фрагменты изображений.

![снимок экрана с изображением, затем частью сжатого изображения и той же развернутой частью](images/aboutgdip03-art07.png)

 

 



