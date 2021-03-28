---
description: Метод DrawString класса Graphics можно использовать для рисования текста в указанном месте или в пределах указанного прямоугольника.
ms.assetid: a873c132-f232-4144-bcc3-ca200055074c
title: Рисование текста (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e16ed49a5ab92380b42ed3316346ac547f95be9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156194"
---
# <a name="drawing-text-gdi"></a>Рисование текста (GDI+)

Метод [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) класса [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) можно использовать для рисования текста в указанном месте или в пределах указанного прямоугольника.

-   [Рисование текста в указанном месте](#drawing-text-at-a-specified-location)
-   [Рисование текста в прямоугольнике](#drawing-text-in-a-rectangle)

## <a name="drawing-text-at-a-specified-location"></a>Рисование текста в указанном месте

Для рисования текста в указанном месте требуются объекты [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics), [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily), [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font), [**PointF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf)и [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) .

В следующем примере строка "Hello" рисуется в месте (30, 10). Семейство шрифтов — Times New Roman. Шрифт, который является отдельным элементом семейства шрифтов, представляет собой Times New Roman, размер 24 пикселя, обычный стиль. Предположим, что **Graphics** — существующий объект [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .

```
FontFamily  fontFamily(L"Times New Roman");
Font        font(&fontFamily, 24, FontStyleRegular, UnitPixel);
PointF      pointF(30.0f, 10.0f);
SolidBrush  solidBrush(Color(255, 0, 0, 255));

graphics.DrawString(L"Hello", -1, &font, pointF, &solidBrush);

```

На следующем рисунке показаны выходные данные предыдущего кода.

![снимок экрана с небольшим окном, содержащим текст "Hello"](images/fontstext1.png)

В предыдущем примере конструктор [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) получает строку, идентифицирующую семейство шрифтов. Адрес объекта **FontFamily** передается в качестве первого аргумента в конструктор [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) . Второй аргумент, передаваемый конструктору **Font** , определяет размер шрифта, измеряемого в единицах, заданных четвертым аргументом. Третий аргумент задает стиль шрифта (обычный, полужирный, курсив и т. д.).

Метод [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) принимает пять аргументов. Первый аргумент — это строка, которая должна быть выведена, а второй аргумент — длина строки (в символах, а не байтах). Если строка завершается нулем, для длины можно передать значение – 1. Третьим аргументом является адрес объекта [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) , который был создан ранее. Четвертый аргумент — это объект [**PointF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf) , содержащий координаты левого верхнего угла строки. Пятый аргумент — это адрес объекта [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) , который будет использоваться для заполнения символов строки.

## <a name="drawing-text-in-a-rectangle"></a>Рисование текста в прямоугольнике

Один из методов [**DrawString**](https://www.bing.com/search?q=**DrawString**) класса [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) имеет параметр *ректф* . Вызывая этот метод **DrawString** , можно нарисовать текст, который переносится в указанный прямоугольник. Для рисования текста в прямоугольнике требуются объекты **Graphics**, [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily), [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font), [**ректф**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf)и [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) .

В следующем примере создается прямоугольник с верхним левым углом (30, 10), шириной 100 и высотой 122. Затем код рисует строку внутри этого прямоугольника. Строка ограничена прямоугольником и переносится в оболочку таким образом, что отдельные слова не нарушаются.

```
WCHAR string[] = 
   L"Draw text in a rectangle by passing a RectF to the DrawString method.";

FontFamily   fontFamily(L"Arial");
Font         font(&fontFamily, 12, FontStyleBold, UnitPoint);
RectF        rectF(30.0f, 10.0f, 100.0f, 122.0f);
SolidBrush   solidBrush(Color(255, 0, 0, 255));

graphics.DrawString(string, -1, &font, rectF, NULL, &solidBrush);

Pen pen(Color(255, 0, 0, 0));
graphics.DrawRectangle(&pen, rectF);
```

На следующем рисунке показан текст, нарисованный в прямоугольнике.

![снимок экрана: небольшое окно, содержащее рекангле, в котором находится первая часть предложения](images/fontstext2.png)

В предыдущем примере четвертый аргумент, передаваемый в метод [**DrawString**](https://www.bing.com/search?q=**DrawString**) , — это объект [**ректф**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf) , указывающий ограничивающий прямоугольник для текста. Пятый параметр имеет тип [**StringFormat**](/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat)— аргумент равен **null** , так как не требуется специального форматирования строки.
