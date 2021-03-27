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
# <a name="obtaining-font-metrics"></a><span data-ttu-id="c3047-103">Получение метрик шрифтов</span><span class="sxs-lookup"><span data-stu-id="c3047-103">Obtaining Font Metrics</span></span>

<span data-ttu-id="c3047-104">Класс [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) предоставляет следующие методы, которые извлекают различные метрики для определенного сочетания семейства или стиля:</span><span class="sxs-lookup"><span data-stu-id="c3047-104">The [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) class provides the following methods that retrieve various metrics for a particular family/style combination:</span></span>

-   <span data-ttu-id="c3047-105">[**FontFamily:: жетемхеигхт**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getemheight)(FontStyle)</span><span class="sxs-lookup"><span data-stu-id="c3047-105">[**FontFamily::GetEmHeight**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getemheight)(FontStyle)</span></span>
-   <span data-ttu-id="c3047-106">[**FontFamily:: жетцелласцент**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getcellascent)(FontStyle)</span><span class="sxs-lookup"><span data-stu-id="c3047-106">[**FontFamily::GetCellAscent**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getcellascent)(FontStyle)</span></span>
-   <span data-ttu-id="c3047-107">[**FontFamily:: жетцеллдесцент**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getcelldescent)(FontStyle)</span><span class="sxs-lookup"><span data-stu-id="c3047-107">[**FontFamily::GetCellDescent**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getcelldescent)(FontStyle)</span></span>
-   <span data-ttu-id="c3047-108">[**FontFamily:: жетлинеспаЦинг**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getlinespacing)(FontStyle)</span><span class="sxs-lookup"><span data-stu-id="c3047-108">[**FontFamily::GetLineSpacing**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getlinespacing)(FontStyle)</span></span>

<span data-ttu-id="c3047-109">Числа, возвращаемые этими методами, находятся в единицах дизайна шрифта, поэтому они не зависят от размера и единиц конкретного объекта [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) .</span><span class="sxs-lookup"><span data-stu-id="c3047-109">The numbers returned by these methods are in font design units, so they are independent of the size and units of a particular [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) object.</span></span>

<span data-ttu-id="c3047-110">На следующем рисунке показано изменение, спуск и разрыв строки.</span><span class="sxs-lookup"><span data-stu-id="c3047-110">The following illustration shows ascent, descent, and line spacing.</span></span>

![схема двух символов на смежных строках с воспроизведением ячейки, спуском клетки и межстрочным промежутком](images/fontstext7a.png)

<span data-ttu-id="c3047-112">В следующем примере показаны метрики для обычного стиля семейства шрифтов Arial.</span><span class="sxs-lookup"><span data-stu-id="c3047-112">The following example displays the metrics for the regular style of the Arial font family.</span></span> <span data-ttu-id="c3047-113">Код также создает объект [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) (на основе семейства Arial) с размером 16 пикселей и отображает метрики (в пикселях) для конкретного объекта **Font** .</span><span class="sxs-lookup"><span data-stu-id="c3047-113">The code also creates a [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) object (based on the Arial family) with size 16 pixels and displays the metrics (in pixels) for that particular **Font** object.</span></span>


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



<span data-ttu-id="c3047-114">На следующем рисунке показаны выходные данные предыдущего кода.</span><span class="sxs-lookup"><span data-stu-id="c3047-114">The following illustration shows the output of the preceding code.</span></span>

![снимок экрана окна с текстом, в котором указаны размер и высота шрифта, а также расположение, спуск и интервал между строками](images/fontstext8.png)

<span data-ttu-id="c3047-116">Обратите внимание на первые две строки выходных данных на предыдущем рисунке.</span><span class="sxs-lookup"><span data-stu-id="c3047-116">Note the first two lines of output in the preceding illustration.</span></span> <span data-ttu-id="c3047-117">Объект [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) возвращает размер 16, а объект [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) Возвращает высоту em 2 048.</span><span class="sxs-lookup"><span data-stu-id="c3047-117">The [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) object returns a size of 16, and the [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) object returns an em height of 2,048.</span></span> <span data-ttu-id="c3047-118">Эти два числа (16 и 2 048) являются ключом к преобразованию между единицами дизайна шрифта и единицами (в данном случае в пикселях) объекта **Font** .</span><span class="sxs-lookup"><span data-stu-id="c3047-118">These two numbers (16 and 2,048) are the key to converting between font design units and the units (in this case pixels) of the **Font** object.</span></span>

<span data-ttu-id="c3047-119">Например, можно преобразовать восхождение из единиц проектирования в пиксели следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c3047-119">For example, you can convert the ascent from design units to pixels as follows:</span></span>

![уравнение, которое умножает 1854 единиц проектирования на 16 пикселей, деленную на единицы проектирования 2048, равное 14,484375 пикселов](images/fontstext9.png)

<span data-ttu-id="c3047-121">Предыдущий код позиционирует текст по вертикали, устанавливая элемент данных *y* объекта [**PointF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf) .</span><span class="sxs-lookup"><span data-stu-id="c3047-121">The preceding code positions text vertically by setting the *y* data member of a [**PointF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf) object.</span></span> <span data-ttu-id="c3047-122">Координата y увеличивается на единицу `font.GetHeight(0.0f)` для каждой новой строки текста.</span><span class="sxs-lookup"><span data-stu-id="c3047-122">The y-coordinate is increased by `font.GetHeight(0.0f)` for each new line of text.</span></span> <span data-ttu-id="c3047-123">Метод [**font::**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-getheight(inreal)) GetObject объекта [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) Возвращает междустрочный шаг (в пикселях) для данного объекта **Font** .</span><span class="sxs-lookup"><span data-stu-id="c3047-123">The [**Font::GetHeight**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-getheight(inreal)) method of a [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) object returns the line spacing (in pixels) for that particular **Font** object.</span></span> <span data-ttu-id="c3047-124">В этом примере число, возвращенное **font::-Height** , равно 18,398438.</span><span class="sxs-lookup"><span data-stu-id="c3047-124">In this example, the number returned by **Font::GetHeight** is 18.398438.</span></span> <span data-ttu-id="c3047-125">Обратите внимание, что это то же самое, что и число, полученное путем преобразования метрики расстояния между строками в пиксели.</span><span class="sxs-lookup"><span data-stu-id="c3047-125">Note that this is the same as the number obtained by converting the line spacing metric to pixels.</span></span>

 

 
