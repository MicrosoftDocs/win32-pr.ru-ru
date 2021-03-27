---
description: 'Класс FontFamily предоставляет следующие методы, которые извлекают различные метрики для определенного сочетания семейства или стиля:'
ms.assetid: 3be485d0-9e0d-43e0-813e-668102ebc010
title: Получение метрик шрифтов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 800fcee7dd1729a6fd5e59bb5dd636af89670776
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072729"
---
# <a name="obtaining-font-metrics"></a>Получение метрик шрифтов

Класс [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) предоставляет следующие методы, которые извлекают различные метрики для определенного сочетания семейства или стиля:

-   [**FontFamily:: жетемхеигхт**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getemheight)(FontStyle)
-   [**FontFamily:: жетцелласцент**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getcellascent)(FontStyle)
-   [**FontFamily:: жетцеллдесцент**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getcelldescent)(FontStyle)
-   [**FontFamily:: жетлинеспаЦинг**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getlinespacing)(FontStyle)

Числа, возвращаемые этими методами, находятся в единицах дизайна шрифта, поэтому они не зависят от размера и единиц конкретного объекта [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) .

На следующем рисунке показано изменение, спуск и разрыв строки.

![схема двух символов на смежных строках с воспроизведением ячейки, спуском клетки и межстрочным промежутком](images/fontstext7a.png)

В следующем примере показаны метрики для обычного стиля семейства шрифтов Arial. Код также создает объект [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) (на основе семейства Arial) с размером 16 пикселей и отображает метрики (в пикселях) для конкретного объекта **Font** .


```
#define INFO_STRING_SIZE 100  // one line of output including null terminator
WCHAR infoString[INFO_STRING_SIZE] = L"";
UINT  ascent;                 // font family ascent in design units
REAL  ascentPixel;            // ascent converted to pixels
UINT  descent;                // font family descent in design units
REAL  descentPixel;           // descent converted to pixels
UINT  lineSpacing;            // font family line spacing in design units
REAL  lineSpacingPixel;       // line spacing converted to pixels
                       
FontFamily   fontFamily(L"Arial");
Font         font(&fontFamily, 16, FontStyleRegular, UnitPixel);
PointF       pointF(10.0f, 10.0f);
SolidBrush   solidBrush(Color(255, 0, 0, 0));

// Display the font size in pixels.
StringCchPrintf(
   infoString, 
   INFO_STRING_SIZE, 
   L"font.GetSize() returns %f.", font.GetSize());

graphics.DrawString(
   infoString, -1, &font, pointF, &solidBrush);

// Move down one line.
pointF.Y += font.GetHeight(0.0);

// Display the font family em height in design units.
StringCchPrintf(
   infoString, 
   INFO_STRING_SIZE, 
   L"fontFamily.GetEmHeight() returns %d.", 
   fontFamily.GetEmHeight(FontStyleRegular));

graphics.DrawString(infoString, -1, &font, pointF, &solidBrush);

// Move down two lines.
pointF.Y += 2.0f * font.GetHeight(0.0f);

// Display the ascent in design units and pixels.
ascent = fontFamily.GetCellAscent(FontStyleRegular);

// 14.484375 = 16.0 * 1854 / 2048
ascentPixel = 
   font.GetSize() * ascent / fontFamily.GetEmHeight(FontStyleRegular);

StringCchPrintf(
   infoString,
   INFO_STRING_SIZE,
   L"The ascent is %d design units, %f pixels.",
   ascent, 
   ascentPixel);

graphics.DrawString(infoString, -1, &font, pointF, &solidBrush);

// Move down one line.
pointF.Y += font.GetHeight(0.0f);

// Display the descent in design units and pixels.
descent = fontFamily.GetCellDescent(FontStyleRegular);

// 3.390625 = 16.0 * 434 / 2048
descentPixel = 
   font.GetSize() * descent / fontFamily.GetEmHeight(FontStyleRegular);

StringCchPrintf(
   infoString, 
   INFO_STRING_SIZE,
   L"The descent is %d design units, %f pixels.",
   descent, 
   descentPixel);

graphics.DrawString(infoString, -1, &font, pointF, &solidBrush);

// Move down one line.
pointF.Y += font.GetHeight(0.0f);

// Display the line spacing in design units and pixels.
lineSpacing = fontFamily.GetLineSpacing(FontStyleRegular);

// 18.398438 = 16.0 * 2355 / 2048
lineSpacingPixel = 
   font.GetSize() * lineSpacing / fontFamily.GetEmHeight(FontStyleRegular);

StringCchPrintf(
   infoString, 
   INFO_STRING_SIZE,
   L"The line spacing is %d design units, %f pixels.",
   lineSpacing, 
   lineSpacingPixel);

graphics.DrawString(infoString, -1, &font, pointF, &solidBrush);
            
```



На следующем рисунке показаны выходные данные предыдущего кода.

![снимок экрана окна с текстом, в котором указаны размер и высота шрифта, а также расположение, спуск и интервал между строками](images/fontstext8.png)

Обратите внимание на первые две строки выходных данных на предыдущем рисунке. Объект [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) возвращает размер 16, а объект [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) Возвращает высоту em 2 048. Эти два числа (16 и 2 048) являются ключом к преобразованию между единицами дизайна шрифта и единицами (в данном случае в пикселях) объекта **Font** .

Например, можно преобразовать восхождение из единиц проектирования в пиксели следующим образом:

![уравнение, которое умножает 1854 единиц проектирования на 16 пикселей, деленную на единицы проектирования 2048, равное 14,484375 пикселов](images/fontstext9.png)

Предыдущий код позиционирует текст по вертикали, устанавливая элемент данных *y* объекта [**PointF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf) . Координата y увеличивается на единицу `font.GetHeight(0.0f)` для каждой новой строки текста. Метод [**font::**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-getheight(inreal)) GetObject объекта [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) Возвращает междустрочный шаг (в пикселях) для данного объекта **Font** . В этом примере число, возвращенное **font::-Height** , равно 18,398438. Обратите внимание, что это то же самое, что и число, полученное путем преобразования метрики расстояния между строками в пиксели.

 

 
