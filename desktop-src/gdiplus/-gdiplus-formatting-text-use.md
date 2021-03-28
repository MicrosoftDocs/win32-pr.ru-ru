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
# <a name="formatting-text-gdi"></a><span data-ttu-id="19df0-103">Форматирование текста (GDI+)</span><span class="sxs-lookup"><span data-stu-id="19df0-103">Formatting Text (GDI+)</span></span>

<span data-ttu-id="19df0-104">Чтобы применить специальное форматирование к тексту, инициализируйте объект [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) и передайте адрес этого объекта в метод [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) класса [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="19df0-104">To apply special formatting to text, initialize a [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) object and pass the address of that object to the [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) method of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span>

<span data-ttu-id="19df0-105">Для рисования форматированного текста в прямоугольнике требуются объекты [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics), [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily), [**Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font), [**ректф**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rectf), [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat)и [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) .</span><span class="sxs-lookup"><span data-stu-id="19df0-105">To draw formatted text in a rectangle, you need [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics), [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily), [**Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font), [**RectF**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rectf), [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat), and [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) objects.</span></span>

-   [<span data-ttu-id="19df0-106">Выровняйте текст</span><span class="sxs-lookup"><span data-stu-id="19df0-106">Aligning Text</span></span>](#aligning-text)
-   [<span data-ttu-id="19df0-107">Установка позиции табуляции</span><span class="sxs-lookup"><span data-stu-id="19df0-107">Setting Tab Stops</span></span>](#setting-tab-stops)
-   [<span data-ttu-id="19df0-108">Рисование вертикального текста</span><span class="sxs-lookup"><span data-stu-id="19df0-108">Drawing Vertical Text</span></span>](#drawing-vertical-text)

## <a name="aligning-text"></a><span data-ttu-id="19df0-109">Выровняйте текст</span><span class="sxs-lookup"><span data-stu-id="19df0-109">Aligning Text</span></span>

<span data-ttu-id="19df0-110">В следующем примере текст рисуется в прямоугольнике.</span><span class="sxs-lookup"><span data-stu-id="19df0-110">The following example draws text in a rectangle.</span></span> <span data-ttu-id="19df0-111">Каждая строка текста выравнивается по центру (боковая сторона), а весь блок текста выравнивается по центру (сверху вниз) в прямоугольнике.</span><span class="sxs-lookup"><span data-stu-id="19df0-111">Each line of text is centered (side to side), and the entire block of text is centered (top to bottom) in the rectangle.</span></span>


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



<span data-ttu-id="19df0-112">На следующем рисунке показан прямоугольник и центрированный текст.</span><span class="sxs-lookup"><span data-stu-id="19df0-112">The following illustration shows the rectangle and the centered text.</span></span>

![снимок экрана: окно, содержащее прямоугольник, содержащий шесть строк текста, горизонтально по центру](images/fontstext3.png)

<span data-ttu-id="19df0-114">Приведенный выше код вызывает два метода объекта [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) : [**StringFormat:: сеталигнмент**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-setalignment) и [**StringFormat:: сетлинеалигнмент**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-setlinealignment).</span><span class="sxs-lookup"><span data-stu-id="19df0-114">The preceding code calls two methods of the [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) object: [**StringFormat::SetAlignment**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-setalignment) and [**StringFormat::SetLineAlignment**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-setlinealignment).</span></span> <span data-ttu-id="19df0-115">Вызов **StringFormat:: сеталигнмент** указывает, что каждая строка текста выравнивается по центру прямоугольника, заданного третьим аргументом, передаваемым в метод [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) .</span><span class="sxs-lookup"><span data-stu-id="19df0-115">The call to **StringFormat::SetAlignment** specifies that each line of text is centered in the rectangle given by the third argument passed to the [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) method.</span></span> <span data-ttu-id="19df0-116">Вызов **StringFormat:: сетлинеалигнмент** указывает, что блок текста выравнивается по центру (сверху вниз) в прямоугольнике.</span><span class="sxs-lookup"><span data-stu-id="19df0-116">The call to **StringFormat::SetLineAlignment** specifies that the block of text is centered (top to bottom) in the rectangle.</span></span>

<span data-ttu-id="19df0-117">Значение [\* \* \* \* стрингалигнментцентер \*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-stringalignment) \* \* \* является элементом перечисления **стрингалигнмент** , который объявлен в гдиплусенумс. h.</span><span class="sxs-lookup"><span data-stu-id="19df0-117">The value [\*\*\*\*StringAlignmentCenter\*\*\*\*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-stringalignment) is an element of the **StringAlignment** enumeration, which is declared in Gdiplusenums.h.</span></span>

## <a name="setting-tab-stops"></a><span data-ttu-id="19df0-118">Установка позиции табуляции</span><span class="sxs-lookup"><span data-stu-id="19df0-118">Setting Tab Stops</span></span>

<span data-ttu-id="19df0-119">Можно задать позиции табуляции для текста, вызвав метод [**StringFormat:: сеттабстопс**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-settabstops) объекта [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) , а затем передав адрес этого **StringFormat** объекта методу [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) класса [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="19df0-119">You can set tab stops for text by calling the [**StringFormat::SetTabStops**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-settabstops) method of a [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) object and then passing the address of that **StringFormat** object to the [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) method of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span>

<span data-ttu-id="19df0-120">В следующем примере задаются позиции табуляции в 150, 250 и 350.</span><span class="sxs-lookup"><span data-stu-id="19df0-120">The following example sets tab stops at 150, 250, and 350.</span></span> <span data-ttu-id="19df0-121">Затем в коде отображается список имен и оценок теста с вкладками.</span><span class="sxs-lookup"><span data-stu-id="19df0-121">Then the code displays a tabbed list of names and test scores.</span></span>


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



<span data-ttu-id="19df0-122">На следующем рисунке показан текст с вкладками.</span><span class="sxs-lookup"><span data-stu-id="19df0-122">The following illustration shows the tabbed text.</span></span>

![Иллюстрация прямоугольника, содержащего четыре столбца текста; Каждый столбец является левым — аллигнед](images/fontstext4.png)

<span data-ttu-id="19df0-124">Предыдущий код передает три аргумента методу [**StringFormat:: сеттабстопс**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-settabstops) .</span><span class="sxs-lookup"><span data-stu-id="19df0-124">The preceding code passes three arguments to the [**StringFormat::SetTabStops**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-settabstops) method.</span></span> <span data-ttu-id="19df0-125">Третьим аргументом является адрес массива, содержащего смещения табуляции.</span><span class="sxs-lookup"><span data-stu-id="19df0-125">The third argument is the address of an array containing the tab offsets.</span></span> <span data-ttu-id="19df0-126">Второй аргумент указывает, что в этом массиве имеется три смещения.</span><span class="sxs-lookup"><span data-stu-id="19df0-126">The second argument indicates that there are three offsets in that array.</span></span> <span data-ttu-id="19df0-127">Первый аргумент, передаваемый в **StringFormat:: сеттабстопс** , равен 0, что означает, что первое смещение в массиве измеряется от позиции 0, левого края ограничивающего прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="19df0-127">The first argument passed to **StringFormat::SetTabStops** is 0, which indicates that the first offset in the array is measured from position 0, the left edge of the bounding rectangle.</span></span>

## <a name="drawing-vertical-text"></a><span data-ttu-id="19df0-128">Рисование вертикального текста</span><span class="sxs-lookup"><span data-stu-id="19df0-128">Drawing Vertical Text</span></span>

<span data-ttu-id="19df0-129">Можно использовать объект [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) , чтобы указать, что текст должен отображаться вертикально, а не горизонтально.</span><span class="sxs-lookup"><span data-stu-id="19df0-129">You can use a [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) object to specify that text be drawn vertically rather than horizontally.</span></span>

<span data-ttu-id="19df0-130">Следующий пример передает значение [\* \* \* \* стрингформатфлагсдиректионвертикал \*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-stringformatflags) \* \* \* в метод [**StringFormat:: сетформатфлагс**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-setformatflags) объекта [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) .</span><span class="sxs-lookup"><span data-stu-id="19df0-130">The following example passes the value [\*\*\*\*StringFormatFlagsDirectionVertical\*\*\*\*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-stringformatflags) to the [**StringFormat::SetFormatFlags**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-setformatflags) method of a [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) object.</span></span> <span data-ttu-id="19df0-131">Адрес этого объекта **StringFormat** передается в метод [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) класса [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="19df0-131">The address of that **StringFormat** object is passed to the [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) method of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span> <span data-ttu-id="19df0-132">Значение [\* \* \* \* стрингформатфлагсдиректионвертикал \*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-stringformatflags) \* \* \* является элементом перечисления **стрингформатфлагс** , который объявлен в гдиплусенумс. h.</span><span class="sxs-lookup"><span data-stu-id="19df0-132">The value [\*\*\*\*StringFormatFlagsDirectionVertical\*\*\*\*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-stringformatflags) is an element of the **StringFormatFlags** enumeration, which is declared in Gdiplusenums.h.</span></span>


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



<span data-ttu-id="19df0-133">На следующем рисунке показан вертикальный текст.</span><span class="sxs-lookup"><span data-stu-id="19df0-133">The following illustration shows the vertical text.</span></span>

![Иллюстрация, показывающая, что окно содержит текст, повернутый на 90 градусов по часовой стрелке](images/fontstext5.png)

 

 



