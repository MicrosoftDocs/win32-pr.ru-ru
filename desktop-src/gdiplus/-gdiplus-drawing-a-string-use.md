---
description: В разделе Рисование линии показано, как написать приложение Windows, которое использует Windows GDI+ для рисования линии.
ms.assetid: fcf45b19-456c-4551-8901-d587a73a5638
title: Рисование строки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a88e76fd38dd640a402edf202dc6cdbd3008a76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264068"
---
# <a name="drawing-a-string"></a><span data-ttu-id="8832f-103">Рисование строки</span><span class="sxs-lookup"><span data-stu-id="8832f-103">Drawing a String</span></span>

<span data-ttu-id="8832f-104">В разделе [Рисование линии](-gdiplus-drawing-a-line-use.md) показано, как написать приложение Windows, которое использует Windows GDI+ для рисования линии.</span><span class="sxs-lookup"><span data-stu-id="8832f-104">The topic [Drawing a Line](-gdiplus-drawing-a-line-use.md) shows how to write a Windows application that uses Windows GDI+ to draw a line.</span></span> <span data-ttu-id="8832f-105">Чтобы нарисовать строку, замените функцию **onpain** , показанную в этом разделе, на следующую функцию **onpain** :</span><span class="sxs-lookup"><span data-stu-id="8832f-105">To draw a string, replace the **OnPaint** function shown in that topic with the following **OnPaint** function:</span></span>


```
VOID OnPaint(HDC hdc)
{
   Graphics    graphics(hdc);
   SolidBrush  brush(Color(255, 0, 0, 255));
   FontFamily  fontFamily(L"Times New Roman");
   Font        font(&fontFamily, 24, FontStyleRegular, UnitPixel);
   PointF      pointF(10.0f, 20.0f);
   
   graphics.DrawString(L"Hello World!", -1, &font, pointF, &brush);
}
```



<span data-ttu-id="8832f-106">Предыдущий код создает несколько объектов GDI+.</span><span class="sxs-lookup"><span data-stu-id="8832f-106">The previous code creates several GDI+ objects.</span></span> <span data-ttu-id="8832f-107">Объект [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) предоставляет метод [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) , который выполняет фактическое рисование.</span><span class="sxs-lookup"><span data-stu-id="8832f-107">The [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object provides the [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) method, which does the actual drawing.</span></span> <span data-ttu-id="8832f-108">Объект [**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) задает цвет строки.</span><span class="sxs-lookup"><span data-stu-id="8832f-108">The [**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) object specifies the color of the string.</span></span>

<span data-ttu-id="8832f-109">Конструктор [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) получает один строковый аргумент, идентифицирующий семейство шрифтов.</span><span class="sxs-lookup"><span data-stu-id="8832f-109">The [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) constructor receives a single, string argument that identifies the font family.</span></span> <span data-ttu-id="8832f-110">Адрес объекта **FontFamily** является первым аргументом, передаваемым конструктору [**Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) .</span><span class="sxs-lookup"><span data-stu-id="8832f-110">The address of the **FontFamily** object is the first argument passed to the [**Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) constructor.</span></span> <span data-ttu-id="8832f-111">Второй аргумент, передаваемый конструктору [Font](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(constfont_)) , задает размер шрифта, а третий аргумент задает стиль.</span><span class="sxs-lookup"><span data-stu-id="8832f-111">The second argument passed to the [Font](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(constfont_)) constructor specifies the font size, and the third argument specifies the style.</span></span> <span data-ttu-id="8832f-112">Значение **фонтстилерегулар** является членом перечисления [**FontStyle**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-fontstyle) , который объявлен в гдиплусенумс. h.</span><span class="sxs-lookup"><span data-stu-id="8832f-112">The value **FontStyleRegular** is a member of the [**FontStyle**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-fontstyle) enumeration, which is declared in Gdiplusenums.h.</span></span> <span data-ttu-id="8832f-113">Последний аргумент в конструкторе **Font** указывает, что размер шрифта (в данном случае 24) измеряется в пикселях.</span><span class="sxs-lookup"><span data-stu-id="8832f-113">The last argument to the **Font** constructor indicates that the size of the font (24 in this case) is measured in pixels.</span></span> <span data-ttu-id="8832f-114">Значение **унитпиксел** является членом перечисления [**Unit**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-unit) .</span><span class="sxs-lookup"><span data-stu-id="8832f-114">The value **UnitPixel** is a member of the [**Unit**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-unit) enumeration.</span></span>

<span data-ttu-id="8832f-115">Первым аргументом, передаваемым в метод [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) , является адрес строки расширенных символов.</span><span class="sxs-lookup"><span data-stu-id="8832f-115">The first argument passed to the [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) method is the address of a wide-character string.</span></span> <span data-ttu-id="8832f-116">Второй аргумент – 1 указывает, что строка завершается нулем.</span><span class="sxs-lookup"><span data-stu-id="8832f-116">The second argument, –1, specifies that the string is null terminated.</span></span> <span data-ttu-id="8832f-117">(Если строка не завершается нулем, во втором аргументе должно быть указано количество расширенных символов в строке.) Третьим аргументом является адрес объекта [**Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) .</span><span class="sxs-lookup"><span data-stu-id="8832f-117">(If the string is not null terminated, the second argument should specify the number of wide characters in the string.) The third argument is the address of the [**Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) object.</span></span> <span data-ttu-id="8832f-118">Четвертый аргумент — это ссылка на объект [**PointF**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-pointf) , указывающий расположение, в котором будет отображаться строка.</span><span class="sxs-lookup"><span data-stu-id="8832f-118">The fourth argument is a reference to a [**PointF**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-pointf) object that specifies the location where the string will be drawn.</span></span> <span data-ttu-id="8832f-119">Последний аргумент — это адрес объекта [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) , указывающий цвет строки.</span><span class="sxs-lookup"><span data-stu-id="8832f-119">The last argument is the address of the [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) object, which specifies the color of the string.</span></span>

 

 
