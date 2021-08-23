---
description: В этом разделе перечислены методы Сетклип класса Graphics. Полный список методов для класса Graphics см. в разделе Graphics.
ms.assetid: e8348373-da79-4d33-8bea-d594985493d4
title: Методы Graphics. Сетклип
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 616a78aa7dd251e888bba1186a3583c5d7f62d188dcc6313560f651ec6558827
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119037192"
---
# <a name="graphicssetclip-methods"></a>Методы Graphics. Сетклип

В этом разделе перечислены методы Сетклип класса [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . Полный список методов для класса **Graphics** см. в разделе [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics).

### <a name="overload-list"></a>Список перегрузок



| Метод                                                                                                     | Описание                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|:-----------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Сетклип (ХРГН, CombineMode)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inhrgn_incombinemode))                     | Метод [**Graphics:: сетклип**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inhrgn_incombinemode)) обновляет область обрезки этого [**графического**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объекта на регион, являющийся сочетанием самого себя и области GDI.<br/>                                                                                                                                                                                                          |
| [**Сетклип (Rect&, CombineMode)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstrect__incombinemode))   | Метод [**Graphics:: сетклип**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstrect__incombinemode)) обновляет область обрезки этого [**графического**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объекта на регион, являющийся сочетанием самого себя и прямоугольника.<br/>                                                                                                                                                                                          |
| [**Сетклип (Ректф&, CombineMode)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstrectf__incombinemode)) | Метод [**Graphics:: сетклип**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstrectf__incombinemode)) обновляет область обрезки этого [**графического**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объекта на регион, являющийся сочетанием самого себя и прямоугольника.<br/>                                                                                                                                                                                         |
| [**Сетклип (регион \* , CombineMode)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstregion_incombinemode))               | Метод [**Graphics:: сетклип**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstregion_incombinemode)) обновляет область обрезки этого [**графического**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объекта на регион, являющийся сочетанием самого себя и региона, заданного объектом [**Region**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-region) .<br/>                                                                                                                                      |
| [**Сетклип (графика \* , CombineMode)**](/previous-versions//ms535823(v=vs.85))                  | Метод [**Graphics:: сетклип**](/previous-versions//ms535823(v=vs.85)) обновляет область обрезки этого [**графического**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объекта на область, которая является сочетанием самого себя и вырезанной области другого **графического** объекта.<br/>                                                                                                                                                                       |
| [**Сетклип (GraphicsPath \* , CombineMode)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstgraphicspath_incombinemode))           | Метод [**Graphics:: сетклип**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstgraphicspath_incombinemode)) обновляет область обрезки этого [**графического**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объекта на регион, являющийся сочетанием самого себя и региона, заданного графическим контуром. Если фигура в пути не закрыта, этот метод рассматривает незамкнутую фигуру так, как будто она была закрыта прямой линией, соединяющей начальную и конечную точки фигуры.<br/> |



 

 
