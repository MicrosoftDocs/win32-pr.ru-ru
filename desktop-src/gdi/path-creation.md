---
description: Чтобы создать путь и выбрать его в контроллере домена, сначала необходимо определить точки, которые его описывают.
ms.assetid: 3691c3ab-f634-476d-a56b-1c187cb12120
title: Создание пути
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caec86d5d7ca5548d021e3c959eac93633f8880c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263663"
---
# <a name="path-creation"></a>Создание пути

Чтобы создать путь и выбрать его в контроллере домена, сначала необходимо определить точки, которые его описывают. Это делается путем вызова функции [**бегинпас**](/windows/desktop/api/Wingdi/nf-wingdi-beginpath) , указания соответствующих функций рисования, а затем путем вызова функции [**ендпас**](/windows/desktop/api/Wingdi/nf-wingdi-endpath) . Это сочетание функций (**бегинпас**, Drawing functions и **ендпас**) образует *квадратную скобку пути*. Ниже приведен список функций рисования, которые можно использовать.

-   [**англеарк**](/windows/desktop/api/Wingdi/nf-wingdi-anglearc)
-   [**Arc**](/windows/desktop/api/Wingdi/nf-wingdi-arc)
-   [**аркто**](/windows/desktop/api/Wingdi/nf-wingdi-arcto)
-   [**Хордовая диаграмма**](/windows/desktop/api/Wingdi/nf-wingdi-chord)
-   [**клосефигуре**](/windows/desktop/api/Wingdi/nf-wingdi-closefigure)
-   [**Эллипс**](/windows/desktop/api/Wingdi/nf-wingdi-ellipse)
-   [**ExtTextOut**](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta)
-   [**LineTo**](/windows/desktop/api/Wingdi/nf-wingdi-lineto)
-   [**моветоекс**](/windows/desktop/api/Wingdi/nf-wingdi-movetoex)
-   [**Круговая**](/windows/desktop/api/Wingdi/nf-wingdi-pie)
-   [**PolyBezierSegment**](/windows/desktop/api/Wingdi/nf-wingdi-polybezier)
-   [**полибезиерто**](/windows/desktop/api/Wingdi/nf-wingdi-polybezierto)
-   [**Рисование**](/windows/desktop/api/Wingdi/nf-wingdi-polydraw)
-   [**Многоугольник**](/windows/desktop/api/Wingdi/nf-wingdi-polygon)
-   [**Линию**](/windows/desktop/api/Wingdi/nf-wingdi-polyline)
-   [**Для в. lineTo**](/windows/desktop/api/Wingdi/nf-wingdi-polylineto)
-   [**Многоугольник**](/windows/desktop/api/Wingdi/nf-wingdi-polypolygon)
-   [**Ломаная линия**](/windows/desktop/api/Wingdi/nf-wingdi-polypolyline)
-   [**Углами**](/windows/desktop/api/Wingdi/nf-wingdi-rectangle)
-   [**раундрект**](/windows/desktop/api/Wingdi/nf-wingdi-roundrect)
-   [**TextOut**](/windows/desktop/api/Wingdi/nf-wingdi-textouta)

Когда приложение вызывает [**ендпас**](/windows/desktop/api/Wingdi/nf-wingdi-endpath), система выбирает связанный путь в УКАЗАНном контроллере домена. (Если в контроллере домена ранее был выбран другой путь, система удалит этот путь без сохранения.) После того как система выберет путь к контроллеру домена, приложение может использовать путь одним из следующих способов.

-   Рисование контура контура (с помощью текущего пера).
-   Заполните внутреннюю часть контура (используя текущую кисть).
-   Нарисуйте контур и заливку внутренней части контура.
-   Измените путь (преобразуя кривые в сегменты линии).
-   Преобразуйте путь в путь обрезки.
-   Преобразуйте путь в регион.
-   Сведение пути путем преобразования каждой кривой в контуре в ряд сегментов линии.
-   Получение координат линий и кривых, образующих контур.

 

 



