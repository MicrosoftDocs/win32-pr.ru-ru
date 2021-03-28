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
# <a name="drawing-text-gdi"></a><span data-ttu-id="4960b-103">Рисование текста (GDI+)</span><span class="sxs-lookup"><span data-stu-id="4960b-103">Drawing Text (GDI+)</span></span>

<span data-ttu-id="4960b-104">Метод [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) класса [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) можно использовать для рисования текста в указанном месте или в пределах указанного прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="4960b-104">You can use the [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) method of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class to draw text at a specified location or within a specified rectangle.</span></span>

-   [<span data-ttu-id="4960b-105">Рисование текста в указанном месте</span><span class="sxs-lookup"><span data-stu-id="4960b-105">Drawing Text at a Specified Location</span></span>](#drawing-text-at-a-specified-location)
-   [<span data-ttu-id="4960b-106">Рисование текста в прямоугольнике</span><span class="sxs-lookup"><span data-stu-id="4960b-106">Drawing Text in a Rectangle</span></span>](#drawing-text-in-a-rectangle)

## <a name="drawing-text-at-a-specified-location"></a><span data-ttu-id="4960b-107">Рисование текста в указанном месте</span><span class="sxs-lookup"><span data-stu-id="4960b-107">Drawing Text at a Specified Location</span></span>

<span data-ttu-id="4960b-108">Для рисования текста в указанном месте требуются объекты [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics), [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily), [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font), [**PointF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf)и [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) .</span><span class="sxs-lookup"><span data-stu-id="4960b-108">To draw text at a specified location, you need [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics), [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily), [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font), [**PointF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf), and [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) objects.</span></span>

<span data-ttu-id="4960b-109">В следующем примере строка "Hello" рисуется в месте (30, 10).</span><span class="sxs-lookup"><span data-stu-id="4960b-109">The following example draws the string "Hello" at location (30, 10).</span></span> <span data-ttu-id="4960b-110">Семейство шрифтов — Times New Roman.</span><span class="sxs-lookup"><span data-stu-id="4960b-110">The font family is Times New Roman.</span></span> <span data-ttu-id="4960b-111">Шрифт, который является отдельным элементом семейства шрифтов, представляет собой Times New Roman, размер 24 пикселя, обычный стиль.</span><span class="sxs-lookup"><span data-stu-id="4960b-111">The font, which is an individual member of the font family, is Times New Roman, size 24 pixels, regular style.</span></span> <span data-ttu-id="4960b-112">Предположим, что **Graphics** — существующий объект [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="4960b-112">Assume that **graphics** is an existing [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span>

```
FontFamily  fontFamily(L"Times New Roman");
Font        font(&fontFamily, 24, FontStyleRegular, UnitPixel);
PointF      pointF(30.0f, 10.0f);
SolidBrush  solidBrush(Color(255, 0, 0, 255));

graphics.DrawString(L"Hello", -1, &font, pointF, &solidBrush);

```

<span data-ttu-id="4960b-113">На следующем рисунке показаны выходные данные предыдущего кода.</span><span class="sxs-lookup"><span data-stu-id="4960b-113">The following illustration shows the output of the preceding code.</span></span>

![снимок экрана с небольшим окном, содержащим текст "Hello"](images/fontstext1.png)

<span data-ttu-id="4960b-115">В предыдущем примере конструктор [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) получает строку, идентифицирующую семейство шрифтов.</span><span class="sxs-lookup"><span data-stu-id="4960b-115">In the preceding example, the [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) constructor receives a string that identifies the font family.</span></span> <span data-ttu-id="4960b-116">Адрес объекта **FontFamily** передается в качестве первого аргумента в конструктор [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) .</span><span class="sxs-lookup"><span data-stu-id="4960b-116">The address of the **FontFamily** object is passed as the first argument to the [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) constructor.</span></span> <span data-ttu-id="4960b-117">Второй аргумент, передаваемый конструктору **Font** , определяет размер шрифта, измеряемого в единицах, заданных четвертым аргументом.</span><span class="sxs-lookup"><span data-stu-id="4960b-117">The second argument passed to the **Font** constructor specifies the size of the font measured in units given by the fourth argument.</span></span> <span data-ttu-id="4960b-118">Третий аргумент задает стиль шрифта (обычный, полужирный, курсив и т. д.).</span><span class="sxs-lookup"><span data-stu-id="4960b-118">The third argument specifies the style (regular, bold, italic, and so on) of the font.</span></span>

<span data-ttu-id="4960b-119">Метод [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) принимает пять аргументов.</span><span class="sxs-lookup"><span data-stu-id="4960b-119">The [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) method receives five arguments.</span></span> <span data-ttu-id="4960b-120">Первый аргумент — это строка, которая должна быть выведена, а второй аргумент — длина строки (в символах, а не байтах).</span><span class="sxs-lookup"><span data-stu-id="4960b-120">The first argument is the string to be drawn, and the second argument is the length (in characters, not bytes) of that string.</span></span> <span data-ttu-id="4960b-121">Если строка завершается нулем, для длины можно передать значение – 1.</span><span class="sxs-lookup"><span data-stu-id="4960b-121">If the string is null-terminated, you can pass –1 for the length.</span></span> <span data-ttu-id="4960b-122">Третьим аргументом является адрес объекта [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) , который был создан ранее.</span><span class="sxs-lookup"><span data-stu-id="4960b-122">The third argument is the address of the [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) object that was constructed previously.</span></span> <span data-ttu-id="4960b-123">Четвертый аргумент — это объект [**PointF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf) , содержащий координаты левого верхнего угла строки.</span><span class="sxs-lookup"><span data-stu-id="4960b-123">The fourth argument is a [**PointF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf) object that contains the coordinates of the upper-left corner of the string.</span></span> <span data-ttu-id="4960b-124">Пятый аргумент — это адрес объекта [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) , который будет использоваться для заполнения символов строки.</span><span class="sxs-lookup"><span data-stu-id="4960b-124">The fifth argument is the address of a [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) object that will be used to fill the characters of the string.</span></span>

## <a name="drawing-text-in-a-rectangle"></a><span data-ttu-id="4960b-125">Рисование текста в прямоугольнике</span><span class="sxs-lookup"><span data-stu-id="4960b-125">Drawing Text in a Rectangle</span></span>

<span data-ttu-id="4960b-126">Один из методов [**DrawString**](https://www.bing.com/search?q=**DrawString**) класса [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) имеет параметр *ректф* .</span><span class="sxs-lookup"><span data-stu-id="4960b-126">One of the [**DrawString**](https://www.bing.com/search?q=**DrawString**) methods of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class has a *RectF* parameter.</span></span> <span data-ttu-id="4960b-127">Вызывая этот метод **DrawString** , можно нарисовать текст, который переносится в указанный прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="4960b-127">By calling that **DrawString** method, you can draw text that wraps in a specified rectangle.</span></span> <span data-ttu-id="4960b-128">Для рисования текста в прямоугольнике требуются объекты **Graphics**, [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily), [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font), [**ректф**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf)и [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) .</span><span class="sxs-lookup"><span data-stu-id="4960b-128">To draw text in a rectangle, you need **Graphics**, [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily), [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font), [**RectF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf), and [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) objects.</span></span>

<span data-ttu-id="4960b-129">В следующем примере создается прямоугольник с верхним левым углом (30, 10), шириной 100 и высотой 122.</span><span class="sxs-lookup"><span data-stu-id="4960b-129">The following example creates a rectangle with upper-left corner (30, 10), width 100, and height 122.</span></span> <span data-ttu-id="4960b-130">Затем код рисует строку внутри этого прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="4960b-130">Then the code draws a string inside that rectangle.</span></span> <span data-ttu-id="4960b-131">Строка ограничена прямоугольником и переносится в оболочку таким образом, что отдельные слова не нарушаются.</span><span class="sxs-lookup"><span data-stu-id="4960b-131">The string is restricted to the rectangle and wraps in such a way that individual words are not broken.</span></span>

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

<span data-ttu-id="4960b-132">На следующем рисунке показан текст, нарисованный в прямоугольнике.</span><span class="sxs-lookup"><span data-stu-id="4960b-132">The following illustration shows the text drawn in the rectangle.</span></span>

![снимок экрана: небольшое окно, содержащее рекангле, в котором находится первая часть предложения](images/fontstext2.png)

<span data-ttu-id="4960b-134">В предыдущем примере четвертый аргумент, передаваемый в метод [**DrawString**](https://www.bing.com/search?q=**DrawString**) , — это объект [**ректф**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf) , указывающий ограничивающий прямоугольник для текста.</span><span class="sxs-lookup"><span data-stu-id="4960b-134">In the preceding example, the fourth argument passed to the [**DrawString**](https://www.bing.com/search?q=**DrawString**) method is a [**RectF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf) object that specifies the bounding rectangle for the text.</span></span> <span data-ttu-id="4960b-135">Пятый параметр имеет тип [**StringFormat**](/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat)— аргумент равен **null** , так как не требуется специального форматирования строки.</span><span class="sxs-lookup"><span data-stu-id="4960b-135">The fifth parameter is of type [**StringFormat**](/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat)— the argument is **NULL** because no special string formatting is required.</span></span>
