---
description: 'Возможны ситуации, когда необходимо создать экран, который имеет следующие характеристики:'
ms.assetid: 2a7590ce-daf4-4892-a838-603e3f89b1bb
title: Использование режима компоновки для управления альфа-смешением
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db54c71ac9687a1ddf28db09b922b7799d0ebaa3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985116"
---
# <a name="using-compositing-mode-to-control-alpha-blending"></a>Использование режима компоновки для управления альфа-смешением

Возможны ситуации, когда необходимо создать экран, который имеет следующие характеристики:

-   Цвета имеют альфа-значения менее 255.
-   Цвета не смешиваются с альфа-смешением при создании точечного рисунка.
-   При отображении готового точечного рисунка цвета в точечном рисунке смешиваются с цветами фона на устройстве вывода.

Чтобы создать такой точечный рисунок, создайте пустой [**растровый**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) объект, а затем создайте [**графический**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объект на основе этого растрового изображения. Установите режим компоновки объекта **Graphics** равным компоситингмодесаурцекопи.

В следующем примере создается [**графический**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объект на основе объекта [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) . Код использует объект **Graphics** вместе с двумя полупрозрачными кистями (альфа = 160) для рисования на точечном рисунке. Код заполняет красный эллипс и зеленый эллипс с помощью полупрозрачных кистей. Зеленый эллипс пересекается с красным эллипсом, но зеленый не смешивается с красным, так как режим композиции объекта **Graphics** имеет значение компоситингмодесаурцекопи.

Далее код готовится к рисованию на экране путем вызова [бегинпаинт](/windows/win32/api/winuser/nf-winuser-beginpaint) и создания [**графического**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объекта на основе контекста устройства. Код рисует растровое изображение на экране дважды: один раз на белом фоне и один раз в многоцветном фоне. Пиксели точечного рисунка, являющиеся частью двух эллипсов, имеют альфа-компонент 160, поэтому эллипсы смешиваются с фоновыми цветами на экране.


```
// Create a blank bitmap.
Bitmap bitmap(180, 100);
// Create a Graphics object that can be used to draw on the bitmap.
Graphics bitmapGraphics(&bitmap);
// Create a red brush and a green brush, each with an alpha value of 160.
SolidBrush redBrush(Color(210, 255, 0, 0));
SolidBrush greenBrush(Color(210, 0, 255, 0));
// Set the compositing mode so that when overlapping ellipses are drawn,
// the colors of the ellipses are not blended.
bitmapGraphics.SetCompositingMode(CompositingModeSourceCopy);
// Fill an ellipse using a red brush that has an alpha value of 160.
bitmapGraphics.FillEllipse(&redBrush, 0, 0, 150, 70);
// Fill a second ellipse using green brush that has an alpha value of 160. 
// The green ellipse overlaps the red ellipse, but the green is not 
// blended with the red.
bitmapGraphics.FillEllipse(&greenBrush, 30, 30, 150, 70);
// Prepare to draw on the screen.
hdc = BeginPaint(hWnd, &ps);
Graphics* pGraphics = new Graphics(hdc);
pGraphics->SetCompositingQuality(CompositingQualityGammaCorrected);
// Draw a multicolored background.
SolidBrush brush(Color((ARGB)Color::Aqua));
pGraphics->FillRectangle(&brush, 200, 0, 60, 100);
brush.SetColor(Color((ARGB)Color::Yellow));
pGraphics->FillRectangle(&brush, 260, 0, 60, 100);
brush.SetColor(Color((ARGB)Color::Fuchsia));
pGraphics->FillRectangle(&brush, 320, 0, 60, 100);
   
// Display the bitmap on a white background.
pGraphics->DrawImage(&bitmap, 0, 0);
// Display the bitmap on a multicolored background.
pGraphics->DrawImage(&bitmap, 200, 0);
delete pGraphics;
EndPaint(hWnd, &ps);
```



На следующем рисунке показаны выходные данные предыдущего кода. Обратите внимание, что эллипсы смешиваются с фоном, но они не смешиваются друг с другом.

![Иллюстрация, демонстрирующая два различных цветных эллипса, каждый из которых смешивается с многоцветным фоном](images/sourcecopy.png)

В предыдущем примере кода содержится следующая инструкция:


```
bitmapGraphics.SetCompositingMode(CompositingModeSourceCopy);
```



Если нужно смешивать эллипсы друг с другом, а также с фоном, измените эту инструкцию следующим образом:


```
bitmapGraphics.SetCompositingMode(CompositingModeSourceOver);
```



На следующем рисунке показаны выходные данные измененного кода.

![Использование режима компоновки для управления иллюстрацией альфа-смешения](images/sourceover.png)

 

 



