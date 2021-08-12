---
description: Windows GDI+ предоставляет различные уровни качества для рисования текста. Как правило, отрисовка более высокого качества требует больше времени на обработку, чем более низкое качество визуализации.
ms.assetid: 780d97ec-f446-4d19-837f-517a7d6dd27d
title: Сглаживание текста
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9411206351340f58b63196ff880745743ad92325918b112ad2ddb5bcb8591e9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118249928"
---
# <a name="antialiasing-with-text"></a>Сглаживание текста

Windows GDI+ предоставляет различные уровни качества для рисования текста. Как правило, отрисовка более высокого качества требует больше времени на обработку, чем более низкое качество визуализации.

Уровень качества является свойством класса [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . Чтобы задать уровень качества, вызовите метод [**Graphics:: сеттекстрендерингхинт**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-settextrenderinghint) объекта **Graphics** . Метод **Graphics:: сеттекстрендерингхинт** получает один из элементов перечисления [**текстрендерингхинт**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint) , который объявлен в гдиплусенумс. h.

GDI+ обеспечивает традиционную сглаживание и новый тип сглаживания на основе технологии Microsoft ClearType, которая доступна только в Windows XP и Windows Server 2003 и более поздних версиях Windows. Сглаживание ClearType повышает удобочитаемость на цветных ЖК-мониторах с цифровым интерфейсом, например мониторами ноутбуков и высококачественным дисплеем с плоским настольным компьютером. Удобочитаемость на экранах CRT также немного улучшена.

Технология ClearType зависит от ориентации и порядка полос LCD. В настоящее время технология ClearType реализована только для вертикальных полос, которые упорядочиваются по RGB. Это может быть проблемой, если вы используете планшетный ПК, где дисплей может быть ориентирован в любом направлении, или если вы используете экран, который может быть включен в альбомную ориентацию.

В следующем примере рисуется текст с двумя различными параметрами качества:


```
FontFamily  fontFamily(L"Times New Roman");
Font        font(&fontFamily, 32, FontStyleRegular, UnitPixel);
SolidBrush  solidBrush(Color(255, 0, 0, 255));
WCHAR       string1[] = L"SingleBitPerPixel";
WCHAR       string2[] = L"AntiAlias";

graphics.SetTextRenderingHint(TextRenderingHintSingleBitPerPixel);
graphics.DrawString(string1, -1, &font, PointF(10.0f, 10.0f), &solidBrush);

graphics.SetTextRenderingHint(TextRenderingHintAntiAlias);
graphics.DrawString(string2, -1, &font, PointF(10.0f, 60.0f), &solidBrush);
            
```



На следующем рисунке показаны выходные данные предыдущего кода.

![снимок экрана со строкой, символы которой имеют зубчатые края, напротив одной с гладкими краями](images/fontstext10.png)

 

 



