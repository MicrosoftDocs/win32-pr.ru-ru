---
description: Различные стили типов в семействе шрифтов могут иметь разную ширину.
ms.assetid: d21613ef-1ba4-40bb-b922-afe287556441
title: Рисование текста из различных шрифтов на одной строке
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2eae2a7a332bd929b9a965462ce802734679f9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263684"
---
# <a name="drawing-text-from-different-fonts-on-the-same-line"></a><span data-ttu-id="835c1-103">Рисование текста из различных шрифтов на одной строке</span><span class="sxs-lookup"><span data-stu-id="835c1-103">Drawing Text from Different Fonts on the Same Line</span></span>

<span data-ttu-id="835c1-104">Различные стили типов в семействе шрифтов могут иметь разную ширину.</span><span class="sxs-lookup"><span data-stu-id="835c1-104">Different type styles within a font family can have different widths.</span></span> <span data-ttu-id="835c1-105">Например, полужирный и курсивный стили семейства всегда шире, чем стиль латиницы для указанного кегля.</span><span class="sxs-lookup"><span data-stu-id="835c1-105">For example, bold and italic styles of a family are always wider than the roman style for a specified point size.</span></span> <span data-ttu-id="835c1-106">При отображении или печати нескольких стилей типов в одной строке необходимо отследить ширину линии, чтобы не отображать или печатать символы поверх другой.</span><span class="sxs-lookup"><span data-stu-id="835c1-106">When you display or print several type styles on a single line, you must keep track of the width of the line to avoid having characters displayed or printed on top of one another.</span></span>

<span data-ttu-id="835c1-107">Для получения ширины (или экстента) текста в текущем шрифте можно использовать две функции.</span><span class="sxs-lookup"><span data-stu-id="835c1-107">You can use two functions to retrieve the width (or extent) of text in the current font.</span></span> <span data-ttu-id="835c1-108">Функция [жеттаббедтекстекстент](/windows/desktop/api/Winuser/nf-winuser-gettabbedtextextenta) вычислит ширину и высоту символьной строки.</span><span class="sxs-lookup"><span data-stu-id="835c1-108">The [GetTabbedTextExtent](/windows/desktop/api/Winuser/nf-winuser-gettabbedtextextenta) function computes the width and height of a character string.</span></span> <span data-ttu-id="835c1-109">Если строка содержит один или несколько символов табуляции, то ширина строки основывается на указанном массиве позиций табуляции.</span><span class="sxs-lookup"><span data-stu-id="835c1-109">If the string contains one or more tab characters, the width of the string is based upon a specified array of tab-stop positions.</span></span> <span data-ttu-id="835c1-110">Функция [GetTextExtentPoint32](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a) вычислит ширину и высоту строки текста.</span><span class="sxs-lookup"><span data-stu-id="835c1-110">The [GetTextExtentPoint32](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a) function computes the width and height of a line of text.</span></span>

<span data-ttu-id="835c1-111">При необходимости система синтезирована шрифт, изменяя точечные рисунки символов.</span><span class="sxs-lookup"><span data-stu-id="835c1-111">When necessary, the system synthesizes a font by changing the character bitmaps.</span></span> <span data-ttu-id="835c1-112">Чтобы выполнить синтезирование символа полужирным шрифтом, система рисует символ дважды: в начальной точке и снова на один пиксель справа от начальной точки.</span><span class="sxs-lookup"><span data-stu-id="835c1-112">To synthesize a character in a bold font, the system draws the character twice: at the starting point, and again one pixel to the right of the starting point.</span></span> <span data-ttu-id="835c1-113">Чтобы выполнить синтезирование символа курсивом, система рисует две строки пикселей в нижней части ячейки символов, перемещает начальную точку вправо на один пиксель, рисует следующие две строки и продолжается до прорисовки символа.</span><span class="sxs-lookup"><span data-stu-id="835c1-113">To synthesize a character in an italic font, the system draws two rows of pixels at the bottom of the character cell, moves the starting point one pixel to the right, draws the next two rows, and continues until the character has been drawn.</span></span> <span data-ttu-id="835c1-114">При сдвиге пикселов каждый символ расрезается вправо.</span><span class="sxs-lookup"><span data-stu-id="835c1-114">By shifting pixels, each character appears to be sheared to the right.</span></span> <span data-ttu-id="835c1-115">Величина сдвига является функцией высоты символа.</span><span class="sxs-lookup"><span data-stu-id="835c1-115">The amount of shear is a function of the height of the character.</span></span>

<span data-ttu-id="835c1-116">Одним из способов записи строки текста, содержащей несколько шрифтов, является использование функции [**GetTextExtentPoint32**](/windows/win32/api/wingdi/nf-wingdi-gettextextentpoint32a) после каждого вызова метода [Text](/windows/desktop/api/Wingdi/nf-wingdi-textouta) и добавления длины в текущую точку.</span><span class="sxs-lookup"><span data-stu-id="835c1-116">One way to write a line of text that contains multiple fonts is to use the [**GetTextExtentPoint32**](/windows/win32/api/wingdi/nf-wingdi-gettextextentpoint32a) function after each call to [TextOut](/windows/desktop/api/Wingdi/nf-wingdi-textouta) and add the length to a current position.</span></span> <span data-ttu-id="835c1-117">В следующем примере записывается строка «это пример строки».</span><span class="sxs-lookup"><span data-stu-id="835c1-117">The following example writes the line "This is a sample string."</span></span> <span data-ttu-id="835c1-118">Использование полужирных символов для "this-a", переключение на курсивные символы для "Sample" и возврат к полужирным символам для "String".</span><span class="sxs-lookup"><span data-stu-id="835c1-118">using bold characters for "This is a", switches to italic characters for "sample", then returns to bold characters for "string."</span></span> <span data-ttu-id="835c1-119">После печати всех строк она восстанавливает системные символы по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="835c1-119">After printing all the strings, it restores the system default characters.</span></span>


```C++
int XIncrement; 
int YStart; 
TEXTMETRIC tm; 
HFONT hfntDefault, hfntItalic, hfntBold; 
SIZE sz; 
LPSTR lpszString1 = "This is a "; 
LPSTR lpszString2 = "sample "; 
LPSTR lpszString3 = "string."; 
HRESULT hr;
size_t * pcch;
 
// Create a bold and an italic logical font.  
 
hfntItalic = MyCreateFont(); 
hfntBold = MyCreateFont(); 
 
 
// Select the bold font and draw the first string  
// beginning at the specified point (XIncrement, YStart).  
 
XIncrement = 10; 
YStart = 50; 
hfntDefault = SelectObject(hdc, hfntBold); 
hr = StringCchLength(lpszString1, 11, pcch);
        if (FAILED(hr))
        {
        // TODO: write error handler 
        }
TextOut(hdc, XIncrement, YStart, lpszString1, *pcch); 
 
// Compute the length of the first string and add  
// this value to the x-increment that is used for the  
// text-output operation.  

hr = StringCchLength(lpszString1, 11, pcch);
        if (FAILED(hr))
        {
        // TODO: write error handler 
        } 
GetTextExtentPoint32(hdc, lpszString1, *pcch, &sz); 
XIncrement += sz.cx; 
 
// Retrieve the overhang value from the TEXTMETRIC  
// structure and subtract it from the x-increment.  
// (This is only necessary for non-TrueType raster  
// fonts.)  
 
GetTextMetrics(hdc, &tm); 
XIncrement -= tm.tmOverhang; 
 
// Select an italic font and draw the second string  
// beginning at the point (XIncrement, YStart).  
 
hfntBold = SelectObject(hdc, hfntItalic); 
GetTextMetrics(hdc, &tm); 
XIncrement -= tm.tmOverhang;
hr = StringCchLength(lpszString2, 8, pcch);
        if (FAILED(hr))
        {
        // TODO: write error handler 
        } 
TextOut(hdc, XIncrement, YStart, lpszString2, *pcch); 
 
// Compute the length of the second string and add  
// this value to the x-increment that is used for the  
// text-output operation.  

hr = StringCchLength(lpszString2, 8, pcch);
        if (FAILED(hr))
        {
        // TODO: write error handler 
        }  
GetTextExtentPoint32(hdc, lpszString2, *pcch, &sz); 
XIncrement += sz.cx; 
 
// Reselect the bold font and draw the third string  
// beginning at the point (XIncrement, YStart).  
 
SelectObject(hdc, hfntBold);
hr = StringCchLength(lpszString3, 8, pcch);
        if (FAILED(hr))
        {
        // TODO: write error handler 
        }  
TextOut(hdc, XIncrement - tm.tmOverhang, YStart, lpszString3, 
            *pcch); 
 
// Reselect the original font.  
 
SelectObject(hdc, hfntDefault); 
 
// Delete the bold and italic fonts.  
 
DeleteObject(hfntItalic); 
DeleteObject(hfntBold); 
```



<span data-ttu-id="835c1-120">В этом примере функция [GetTextExtentPoint32](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a) инициализирует элементы структуры [размера](/previous-versions//dd145106(v=vs.85)) с длиной и высотой указанной строки.</span><span class="sxs-lookup"><span data-stu-id="835c1-120">In this example, the [GetTextExtentPoint32](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a) function initializes the members of a [SIZE](/previous-versions//dd145106(v=vs.85)) structure with the length and height of the specified string.</span></span> <span data-ttu-id="835c1-121">Функция [жеттекстметрикс](/windows/desktop/api/Wingdi/nf-wingdi-gettextmetrics) получает выступ для текущего шрифта.</span><span class="sxs-lookup"><span data-stu-id="835c1-121">The [GetTextMetrics](/windows/desktop/api/Wingdi/nf-wingdi-gettextmetrics) function retrieves the overhang for the current font.</span></span> <span data-ttu-id="835c1-122">Так как в качестве шрифта используется шрифт TrueType, значение выступа не изменяет размещение строки.</span><span class="sxs-lookup"><span data-stu-id="835c1-122">Because the overhang is zero if the font is a TrueType font, the overhang value does not change the string placement.</span></span> <span data-ttu-id="835c1-123">Однако для растровых шрифтов важно использовать значение выступа.</span><span class="sxs-lookup"><span data-stu-id="835c1-123">For raster fonts, however, it is important to use the overhang value.</span></span>

<span data-ttu-id="835c1-124">Выступ вычитается из строки полужирным шрифтом один раз, чтобы последующий символ ближе к концу строки, если шрифт является растровым.</span><span class="sxs-lookup"><span data-stu-id="835c1-124">The overhang is subtracted from the bold string once, to bring subsequent characters closer to the end of the string if the font is a raster font.</span></span> <span data-ttu-id="835c1-125">Поскольку выступ влияет как на начало, так и на конец курсивной строки в растровом шрифте, глифы начинаются справа от указанного расположения и заканчиваются слева от конечной точки последней символьной ячейки.</span><span class="sxs-lookup"><span data-stu-id="835c1-125">Because overhang affects both the beginning and end of the italic string in a raster font, the glyphs start at the right of the specified location and end at the left of the endpoint of the last character cell.</span></span> <span data-ttu-id="835c1-126">(Функция [**GetTextExtentPoint32**](/windows/win32/api/wingdi/nf-wingdi-gettextextentpoint32a) извлекает экстент ячеек символов, а не экстенты.) Чтобы учитывать выступ в виде растровой курсивной строки, этот пример вычитает выступ перед помещением строки и вычитает его снова перед тем, как помещать последующие символы.</span><span class="sxs-lookup"><span data-stu-id="835c1-126">(The [**GetTextExtentPoint32**](/windows/win32/api/wingdi/nf-wingdi-gettextextentpoint32a) function retrieves the extent of the character cells, not the extent of the glyphs.) To account for the overhang in the raster italic string, the example subtracts the overhang before placing the string and subtracts it again before placing subsequent characters.</span></span>

<span data-ttu-id="835c1-127">Функция [сеттекстжустификатион](/windows/desktop/api/Wingdi/nf-wingdi-settextjustification) добавляет дополнительное пространство к символам разрыва строки текста.</span><span class="sxs-lookup"><span data-stu-id="835c1-127">The [SetTextJustification](/windows/desktop/api/Wingdi/nf-wingdi-settextjustification) function adds extra space to the break characters in a line of text.</span></span> <span data-ttu-id="835c1-128">Для определения экстента строки можно использовать функцию [жеттекстекстентпоинт](/windows/desktop/api/WinGdi/nf-wingdi-gettextextentpointa) , а затем вычесть этот экстент из общего объема пространства, занимаемого данной строкой, и использовать функцию [**сеттекстжустификатион**](/windows/win32/api/wingdi/nf-wingdi-settextjustification) для распределения дополнительного пространства между символами разрыва в строке.</span><span class="sxs-lookup"><span data-stu-id="835c1-128">You can use the [GetTextExtentPoint](/windows/desktop/api/WinGdi/nf-wingdi-gettextextentpointa) function to determine the extent of a string, then subtract that extent from the total amount of space the line should occupy, and use the [**SetTextJustification**](/windows/win32/api/wingdi/nf-wingdi-settextjustification) function to distribute the extra space among the break characters in the string.</span></span> <span data-ttu-id="835c1-129">Функция [сеттекстчарактерекстра](/windows/desktop/api/Wingdi/nf-wingdi-settextcharacterextra) добавляет дополнительное пространство к каждой ячейке символа в выбранном шрифте, включая символ разрыва.</span><span class="sxs-lookup"><span data-stu-id="835c1-129">The [SetTextCharacterExtra](/windows/desktop/api/Wingdi/nf-wingdi-settextcharacterextra) function adds extra space to every character cell in the selected font, including the break character.</span></span> <span data-ttu-id="835c1-130">(Для определения текущего объема дополнительного пространства, добавляемого в ячейки символов, можно использовать функцию [жеттекстчарактерекстра](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharacterextra) ; значение по умолчанию — нуль.)</span><span class="sxs-lookup"><span data-stu-id="835c1-130">(You can use the [GetTextCharacterExtra](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharacterextra) function to determine the current amount of extra space being added to the character cells; the default setting is zero.)</span></span>

<span data-ttu-id="835c1-131">Можно разместить символы с большей точностью с помощью функции [GetCharWidth32](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidth32a) или [жетчарабквидсс](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsa) , чтобы получить ширину отдельных символов в шрифте.</span><span class="sxs-lookup"><span data-stu-id="835c1-131">You can place characters with greater precision by using the [GetCharWidth32](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidth32a) or [GetCharABCWidths](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsa) function to retrieve the widths of individual characters in a font.</span></span> <span data-ttu-id="835c1-132">Функция [**жетчарабквидсс**](/windows/win32/api/wingdi/nf-wingdi-getcharabcwidthsa) более точна, чем функция [**GetCharWidth32**](/windows/win32/api/wingdi/nf-wingdi-getcharwidth32a) , но ее можно использовать только со шрифтами TrueType.</span><span class="sxs-lookup"><span data-stu-id="835c1-132">The [**GetCharABCWidths**](/windows/win32/api/wingdi/nf-wingdi-getcharabcwidthsa) function is more accurate than the [**GetCharWidth32**](/windows/win32/api/wingdi/nf-wingdi-getcharwidth32a) function, but it can only be used with TrueType fonts.</span></span>

<span data-ttu-id="835c1-133">Расстояния ABC также позволяют приложению выполнять очень точное выравнивание текста.</span><span class="sxs-lookup"><span data-stu-id="835c1-133">ABC spacing also allows an application to perform very accurate text alignment.</span></span> <span data-ttu-id="835c1-134">Например, если приложение по правому краю использует растровый шрифт Roman без использования пробелов, ширина аванса вычисляется как ширина символа.</span><span class="sxs-lookup"><span data-stu-id="835c1-134">For example, when the application right aligns a raster roman font without using ABC spacing, the advance width is calculated as the character width.</span></span> <span data-ttu-id="835c1-135">Это означает, что пробел справа от глифа в растровом изображении является согласованным, а не самим глифом.</span><span class="sxs-lookup"><span data-stu-id="835c1-135">This means the white space to the right of the glyph in the bitmap is aligned, not the glyph itself.</span></span> <span data-ttu-id="835c1-136">С помощью ширины ABC приложения имеют большую гибкость при размещении и удалении пробелов при выводе текста, так как они позволяют контролировать межзнаковые интервалы.</span><span class="sxs-lookup"><span data-stu-id="835c1-136">By using ABC widths, applications have more flexibility in the placement and removal of white space when aligning text, because they have information that allows them to finely control intercharacter spacing.</span></span>

 

 
