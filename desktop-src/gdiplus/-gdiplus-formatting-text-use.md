---
description: Чтобы применить специальное форматирование к тексту, инициализируйте объект StringFormat и передайте адрес этого объекта в метод DrawString класса Graphics.
ms.assetid: 4014a602-88f6-4fac-b4b2-3dafdcff8f33
title: Форматирование текста (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e6b2cc6109e7b946e9b4e98645c9445b8268bb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104557513"
---
# <a name="formatting-text-gdi"></a>Форматирование текста (GDI+)

Чтобы применить специальное форматирование к тексту, инициализируйте объект [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) и передайте адрес этого объекта в метод [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) класса [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .

Для рисования форматированного текста в прямоугольнике требуются объекты [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics), [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily), [**Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font), [**ректф**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rectf), [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat)и [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) .

-   [Выровняйте текст](#aligning-text)
-   [Установка позиции табуляции](#setting-tab-stops)
-   [Рисование вертикального текста](#drawing-vertical-text)

## <a name="aligning-text"></a>Выровняйте текст

В следующем примере текст рисуется в прямоугольнике. Каждая строка текста выравнивается по центру (боковая сторона), а весь блок текста выравнивается по центру (сверху вниз) в прямоугольнике.


```
WCHAR string[] = 
   L"Use StringFormat and RectF objects to center text in a rectangle.";
                       
FontFamily   fontFamily(L"Arial");
Font         font(&fontFamily, 12, FontStyleBold, UnitPoint);
RectF        rectF(30.0f, 10.0f, 120.0f, 140.0f);
StringFormat stringFormat;
SolidBrush   solidBrush(Color(255, 0, 0, 255));

// Center-justify each line of text.
stringFormat.SetAlignment(StringAlignmentCenter);

// Center the block of text (top to bottom) in the rectangle.
stringFormat.SetLineAlignment(StringAlignmentCenter);

graphics.DrawString(string, -1, &font, rectF, &stringFormat, &solidBrush);

Pen pen(Color(255, 0, 0, 0));
graphics.DrawRectangle(&pen, rectF);
            
```



На следующем рисунке показан прямоугольник и центрированный текст.

![снимок экрана: окно, содержащее прямоугольник, содержащий шесть строк текста, горизонтально по центру](images/fontstext3.png)

Приведенный выше код вызывает два метода объекта [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) : [**StringFormat:: сеталигнмент**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-setalignment) и [**StringFormat:: сетлинеалигнмент**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-setlinealignment). Вызов **StringFormat:: сеталигнмент** указывает, что каждая строка текста выравнивается по центру прямоугольника, заданного третьим аргументом, передаваемым в метод [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) . Вызов **StringFormat:: сетлинеалигнмент** указывает, что блок текста выравнивается по центру (сверху вниз) в прямоугольнике.

Значение [* * * * стрингалигнментцентер *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-stringalignment) * * * является элементом перечисления **стрингалигнмент** , который объявлен в гдиплусенумс. h.

## <a name="setting-tab-stops"></a>Установка позиции табуляции

Можно задать позиции табуляции для текста, вызвав метод [**StringFormat:: сеттабстопс**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-settabstops) объекта [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) , а затем передав адрес этого **StringFormat** объекта методу [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) класса [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .

В следующем примере задаются позиции табуляции в 150, 250 и 350. Затем в коде отображается список имен и оценок теста с вкладками.


```
WCHAR string[150] = 
   L"Name\tTest 1\tTest 2\tTest 3\n";

StringCchCatW(string, 150, L"Joe\t95\t88\t91\n");
StringCchCatW(string, 150, L"Mary\t98\t84\t90\n");
StringCchCatW(string, 150, L"Sam\t42\t76\t98\n");
StringCchCatW(string, 150, L"Jane\t65\t73\t92\n");
                       
FontFamily   fontFamily(L"Courier New");
Font         font(&fontFamily, 12, FontStyleRegular, UnitPoint);
RectF        rectF(10.0f, 10.0f, 450.0f, 100.0f);
StringFormat stringFormat;
SolidBrush   solidBrush(Color(255, 0, 0, 255));
REAL         tabs[] = {150.0f, 100.0f, 100.0f};

stringFormat.SetTabStops(0.0f, 3, tabs);

graphics.DrawString(string, -1, &font, rectF, &stringFormat, &solidBrush);

Pen pen(Color(255, 0, 0, 0));
graphics.DrawRectangle(&pen, rectF);
            
```



На следующем рисунке показан текст с вкладками.

![Иллюстрация прямоугольника, содержащего четыре столбца текста; Каждый столбец является левым — аллигнед](images/fontstext4.png)

Предыдущий код передает три аргумента методу [**StringFormat:: сеттабстопс**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-settabstops) . Третьим аргументом является адрес массива, содержащего смещения табуляции. Второй аргумент указывает, что в этом массиве имеется три смещения. Первый аргумент, передаваемый в **StringFormat:: сеттабстопс** , равен 0, что означает, что первое смещение в массиве измеряется от позиции 0, левого края ограничивающего прямоугольника.

## <a name="drawing-vertical-text"></a>Рисование вертикального текста

Можно использовать объект [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) , чтобы указать, что текст должен отображаться вертикально, а не горизонтально.

Следующий пример передает значение [* * * * стрингформатфлагсдиректионвертикал *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-stringformatflags) * * * в метод [**StringFormat:: сетформатфлагс**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-setformatflags) объекта [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) . Адрес этого объекта **StringFormat** передается в метод [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) класса [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . Значение [* * * * стрингформатфлагсдиректионвертикал *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-stringformatflags) * * * является элементом перечисления **стрингформатфлагс** , который объявлен в гдиплусенумс. h.


```
WCHAR string[] = L"Vertical text";
                     
FontFamily   fontFamily(L"Lucida Console");
Font         font(&fontFamily, 14, FontStyleRegular, UnitPoint);
PointF       pointF(40.0f, 10.0f);
StringFormat stringFormat;
SolidBrush   solidBrush(Color(255, 0, 0, 255));

stringFormat.SetFormatFlags(StringFormatFlagsDirectionVertical);

graphics.DrawString(string, -1, &font, pointF, &stringFormat, &solidBrush);
            
```



На следующем рисунке показан вертикальный текст.

![Иллюстрация, показывающая, что окно содержит текст, повернутый на 90 градусов по часовой стрелке](images/fontstext5.png)

 

 



