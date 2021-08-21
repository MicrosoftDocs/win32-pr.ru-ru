---
description: Вместо того, чтобы рисовать линию или кривую сплошным цветом, можно рисовать текстурой.
ms.assetid: 326170a5-d21f-49d6-9f60-10b9bc8d97b4
title: Рисование линии, заполненной текстурой
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a13cc8f93adee4792836c4166d5787e20d9c54040448d3a7efde36ff6a580d8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119467044"
---
# <a name="drawing-a-line-filled-with-a-texture"></a>Рисование линии, заполненной текстурой

Вместо того, чтобы рисовать линию или кривую сплошным цветом, можно рисовать текстурой. Чтобы нарисовать линии и кривые с текстурой, создайте объект [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) и передайте адрес этого объекта **TextureBrush** конструктору [**пера**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) . Изображение, связанное с текстурной кистью, используется для мозаичного заполнения плоскости (незаметно), а когда перо рисует линию или кривую, штрих пера обнаруживает определенные Пиксели мозаичной текстуры.

В следующем примере объект [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) создается на основе файла Texture1.jpg. Этот образ используется для создания объекта [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) , а объект **TextureBrush** используется для создания объекта [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) . Вызов [**Graphics::D равимаже**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inint_inint_inint_inint)) рисует изображение с его верхним левым углом в точке (0, 0). Вызов [**Graphics::D равеллипсе**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) использует объект **Pen** для рисования текстурированного эллипса.


```
Image         image(L"Texture1.jpg");
TextureBrush  tBrush(&image);
Pen           texturedPen(&tBrush, 30);

graphics.DrawImage(&image, 0, 0, image.GetWidth(), image.GetHeight());
graphics.DrawEllipse(&texturedPen, 100, 20, 200, 100);
```



На следующем рисунке показано изображение и текстурированный эллипс.

![Иллюстрация, показывающая небольшое прямоугольное изображение, а сегмент эллиптической линии заполняется исходным изображением](images/pens7.png)

 

 
