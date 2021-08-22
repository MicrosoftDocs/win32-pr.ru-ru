---
description: Различные стили типов в семействе шрифтов могут иметь разную ширину.
ms.assetid: d21613ef-1ba4-40bb-b922-afe287556441
title: Рисование текста из различных шрифтов на одной строке
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad28f13c94e568073504f07e8722e5d688cb12aa1b376b0f52fad752574e6f8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119038052"
---
# <a name="drawing-text-from-different-fonts-on-the-same-line"></a>Рисование текста из различных шрифтов на одной строке

Различные стили типов в семействе шрифтов могут иметь разную ширину. Например, полужирный и курсивный стили семейства всегда шире, чем стиль латиницы для указанного кегля. При отображении или печати нескольких стилей типов в одной строке необходимо отследить ширину линии, чтобы не отображать или печатать символы поверх другой.

Для получения ширины (или экстента) текста в текущем шрифте можно использовать две функции. Функция [жеттаббедтекстекстент](/windows/desktop/api/Winuser/nf-winuser-gettabbedtextextenta) вычислит ширину и высоту символьной строки. Если строка содержит один или несколько символов табуляции, то ширина строки основывается на указанном массиве позиций табуляции. Функция [GetTextExtentPoint32](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a) вычислит ширину и высоту строки текста.

При необходимости система синтезирована шрифт, изменяя точечные рисунки символов. Чтобы выполнить синтезирование символа полужирным шрифтом, система рисует символ дважды: в начальной точке и снова на один пиксель справа от начальной точки. Чтобы выполнить синтезирование символа курсивом, система рисует две строки пикселей в нижней части ячейки символов, перемещает начальную точку вправо на один пиксель, рисует следующие две строки и продолжается до прорисовки символа. При сдвиге пикселов каждый символ расрезается вправо. Величина сдвига является функцией высоты символа.

Одним из способов записи строки текста, содержащей несколько шрифтов, является использование функции [**GetTextExtentPoint32**](/windows/win32/api/wingdi/nf-wingdi-gettextextentpoint32a) после каждого вызова метода [Text](/windows/desktop/api/Wingdi/nf-wingdi-textouta) и добавления длины в текущую точку. В следующем примере записывается строка «это пример строки». Использование полужирных символов для "this-a", переключение на курсивные символы для "Sample" и возврат к полужирным символам для "String". После печати всех строк она восстанавливает системные символы по умолчанию.


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



В этом примере функция [GetTextExtentPoint32](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a) инициализирует элементы структуры [размера](/previous-versions//dd145106(v=vs.85)) с длиной и высотой указанной строки. Функция [жеттекстметрикс](/windows/desktop/api/Wingdi/nf-wingdi-gettextmetrics) получает выступ для текущего шрифта. Так как в качестве шрифта используется шрифт TrueType, значение выступа не изменяет размещение строки. Однако для растровых шрифтов важно использовать значение выступа.

Выступ вычитается из строки полужирным шрифтом один раз, чтобы последующий символ ближе к концу строки, если шрифт является растровым. Поскольку выступ влияет как на начало, так и на конец курсивной строки в растровом шрифте, глифы начинаются справа от указанного расположения и заканчиваются слева от конечной точки последней символьной ячейки. (Функция [**GetTextExtentPoint32**](/windows/win32/api/wingdi/nf-wingdi-gettextextentpoint32a) извлекает экстент ячеек символов, а не экстенты.) Чтобы учитывать выступ в виде растровой курсивной строки, этот пример вычитает выступ перед помещением строки и вычитает его снова перед тем, как помещать последующие символы.

Функция [сеттекстжустификатион](/windows/desktop/api/Wingdi/nf-wingdi-settextjustification) добавляет дополнительное пространство к символам разрыва строки текста. Для определения экстента строки можно использовать функцию [жеттекстекстентпоинт](/windows/desktop/api/WinGdi/nf-wingdi-gettextextentpointa) , а затем вычесть этот экстент из общего объема пространства, занимаемого данной строкой, и использовать функцию [**сеттекстжустификатион**](/windows/win32/api/wingdi/nf-wingdi-settextjustification) для распределения дополнительного пространства между символами разрыва в строке. Функция [сеттекстчарактерекстра](/windows/desktop/api/Wingdi/nf-wingdi-settextcharacterextra) добавляет дополнительное пространство к каждой ячейке символа в выбранном шрифте, включая символ разрыва. (Для определения текущего объема дополнительного пространства, добавляемого в ячейки символов, можно использовать функцию [жеттекстчарактерекстра](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharacterextra) ; значение по умолчанию — нуль.)

Можно разместить символы с большей точностью с помощью функции [GetCharWidth32](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidth32a) или [жетчарабквидсс](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsa) , чтобы получить ширину отдельных символов в шрифте. Функция [**жетчарабквидсс**](/windows/win32/api/wingdi/nf-wingdi-getcharabcwidthsa) более точна, чем функция [**GetCharWidth32**](/windows/win32/api/wingdi/nf-wingdi-getcharwidth32a) , но ее можно использовать только со шрифтами TrueType.

Расстояния ABC также позволяют приложению выполнять очень точное выравнивание текста. Например, если приложение по правому краю использует растровый шрифт Roman без использования пробелов, ширина аванса вычисляется как ширина символа. Это означает, что пробел справа от глифа в растровом изображении является согласованным, а не самим глифом. С помощью ширины ABC приложения имеют большую гибкость при размещении и удалении пробелов при выводе текста, так как они позволяют контролировать межзнаковые интервалы.

 

 
