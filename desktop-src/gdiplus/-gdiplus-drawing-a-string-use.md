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
# <a name="drawing-a-string"></a>Рисование строки

В разделе [Рисование линии](-gdiplus-drawing-a-line-use.md) показано, как написать приложение Windows, которое использует Windows GDI+ для рисования линии. Чтобы нарисовать строку, замените функцию **onpain** , показанную в этом разделе, на следующую функцию **onpain** :


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



Предыдущий код создает несколько объектов GDI+. Объект [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) предоставляет метод [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) , который выполняет фактическое рисование. Объект [**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) задает цвет строки.

Конструктор [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) получает один строковый аргумент, идентифицирующий семейство шрифтов. Адрес объекта **FontFamily** является первым аргументом, передаваемым конструктору [**Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) . Второй аргумент, передаваемый конструктору [Font](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(constfont_)) , задает размер шрифта, а третий аргумент задает стиль. Значение **фонтстилерегулар** является членом перечисления [**FontStyle**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-fontstyle) , который объявлен в гдиплусенумс. h. Последний аргумент в конструкторе **Font** указывает, что размер шрифта (в данном случае 24) измеряется в пикселях. Значение **унитпиксел** является членом перечисления [**Unit**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-unit) .

Первым аргументом, передаваемым в метод [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) , является адрес строки расширенных символов. Второй аргумент – 1 указывает, что строка завершается нулем. (Если строка не завершается нулем, во втором аргументе должно быть указано количество расширенных символов в строке.) Третьим аргументом является адрес объекта [**Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) . Четвертый аргумент — это ссылка на объект [**PointF**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-pointf) , указывающий расположение, в котором будет отображаться строка. Последний аргумент — это адрес объекта [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) , указывающий цвет строки.

 

 
