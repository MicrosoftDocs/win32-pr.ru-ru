---
description: Интерфейс C++ к Windows GDI+ содержит около 40 классов, перечислений 50 и 6 структур. Также существует несколько функций, не являющихся членами какого-либо класса.
ms.assetid: 46051bfa-b842-4e4e-bda8-e9003b5b5da4
title: Структура интерфейса на основе классов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2627d695330c316a57c2593e75233d73b27a1524
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997238"
---
# <a name="the-structure-of-the-class-based-interface"></a>Структура интерфейса на основе классов

Интерфейс C++ к Windows GDI+ содержит около 40 классов, перечислений 50 и 6 структур. Также существует несколько функций, не являющихся членами какого-либо класса.

Необходимо указать, что пространство имен GDIPLUS используется перед вызовом любых функций GDI+. Следующая инструкция указывает, что пространство имен GDIPLUS используется в приложении.

`using namespace Gdiplus;`

Класс [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) является ЯДРОМ интерфейса GDI+. Это класс, который фактически рисует линии, кривые, цифры, изображения и текст.

Многие классы работают вместе с классом [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . Например, метод [Graphics::D равлине](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) получает указатель на объект [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) , который содержит атрибуты (цвет, ширина, тип штриха и т. д.) рисуемой линии. Метод [Graphics:: филлректангле](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(inconstbrush_inconstrectf_)) может получить указатель на объект [**LinearGradientBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) , который работает с **графическим** объектом для заполнения прямоугольника с постепенно изменяющимся цветом. Объекты [**Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) и [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) влияют на способ рисования текста **графическим** объектом. Объект [**Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) хранит и манипулирует универсальным преобразованием **графического** объекта, который используется для вращения, масштабирования и отражения изображений.

Некоторые классы служат в основном как структурированные типы данных. Некоторые из этих классов (например, [**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect), [**Point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point)и [**size**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-size)) предназначены для общих целей. Другие предназначены для специализированных целей и считаются вспомогательными классами. Например, класс [**BitmapData**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-bitmapdata) является вспомогательным классом для класса [**Bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) , а класс [**пасдата**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-pathdata) — вспомогательным классом для класса [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) . GDI+ также определяет несколько структур, используемых для организации данных. Например, структура [**колормап**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) содержит пару объектов [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) , образующих одну запись в таблице преобразования цветов.

GDI+ определяет несколько перечислений, которые представляют собой коллекции связанных констант. Например, перечисление [**линежоин**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-linejoin) содержит элементы [* * * * линежоинбевел * *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-linejoin)* *, [* * * * линежоинмитер * *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-linejoin)* * и [* * * * линежоинраунд *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-linejoin)* * *, которые определяют стили, которые можно использовать для объединения двух строк.

Интерфейс GDI+ предоставляет несколько функций, которые не являются частью какого-либо класса. Две из этих функций — [**гдиплусстартуп**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) и [**гдиплусшутдовн**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusshutdown). Необходимо вызвать **гдиплусстартуп** , прежде чем выполнять любые другие вызовы GDI+, и после завершения использования GDI+ необходимо вызвать **гдиплусшутдовн** .

 

 
