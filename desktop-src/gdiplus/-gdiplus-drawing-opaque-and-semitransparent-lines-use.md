---
description: При рисовании линии необходимо передать адрес объекта Pen методу DrawLine класса Graphics.
ms.assetid: 4524908f-f9c2-4807-b045-eb9e43a6668b
title: Рисование непрозрачных и частично прозрачных линий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14cdf31a80be9ac2a0cf61a2a8eb82f530dc3558c876cba9190a79f42ac35baa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036762"
---
# <a name="drawing-opaque-and-semitransparent-lines"></a>Рисование непрозрачных и частично прозрачных линий

При рисовании линии необходимо передать адрес объекта [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) методу [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) класса [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . Одним из параметров конструктора **пера** является объект [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) . Чтобы нарисовать непрозрачную линию, установите альфа-компонент цвета равным 255. Чтобы нарисовать полупрозрачную линию, установите значение альфа-компонента в диапазоне от 1 до 254.

При рисовании полупрозрачной линии на некотором фоне цвет линии смешивается с цветами фона. Альфа-компонент указывает, как цвета линий и фона смешиваются. Альфа-значения рядом с 0 помещают больший вес на цвета фона, а альфа-значения около 255 помещают больше на цвет линии.

В следующем примере рисуется изображение, а затем выводится три линии, которые используют изображение в качестве фона. Цвет первой линии имеет альфа-компонент, равный 255, поэтому она является непрозрачной. Для второй и третьей линий используется альфа-компонент, равный 128, поэтому они являются полупрозрачными и сквозь них можно видеть фоновое изображение. Вызов [**Graphics:: сеткомпоситингкуалити**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingquality) приводит к тому, что смешение третьей линии выполняется вместе с гаммой коррекцией.


```
Image image(L"Texture1.jpg");
graphics.DrawImage(&image, 10, 5, image.GetWidth(), image.GetHeight());
Pen opaquePen(Color(255, 0, 0, 255), 15);
Pen semiTransPen(Color(128, 0, 0, 255), 15);
graphics.DrawLine(&opaquePen, 0, 20, 100, 20);
graphics.DrawLine(&semiTransPen, 0, 40, 100, 40);
graphics.SetCompositingQuality(CompositingQualityGammaCorrected);
graphics.DrawLine(&semiTransPen, 0, 60, 100, 60);
```



На следующем рисунке показаны выходные данные предыдущего кода.

![Иллюстрация, показывающая изображение, наложенное тремя широкими линиями: один непрозрачный, один немного прозрачный и один очень прозрачный](images/compqualline.png)

 

 



