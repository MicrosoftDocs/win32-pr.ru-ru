---
description: Windows GDI+ предоставляет несколько классов, образующих основу для рисования текста.
ms.assetid: 12bc38c3-5fbc-4d7b-902c-92a5f5057473
title: Использование текста и шрифтов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f28ec157888dcf45b309237eb0f7eefff17808c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541434"
---
# <a name="using-text-and-fonts"></a>Использование текста и шрифтов

Windows GDI+ предоставляет несколько классов, образующих основу для рисования текста. Класс [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) имеет несколько методов [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) , позволяющих задавать различные функции текста, такие как расположение, ограничивающий прямоугольник, шрифт и формат. В число других классов, участвующих в отрисовке текста, входят [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily), [**Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font), [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat), [**инсталледфонтколлектион**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-installedfontcollection)и [**приватефонтколлектион**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection).

В следующих разделах текст и шрифты рассматриваются более подробно:

-   [Создание семейств шрифтов и шрифтов](-gdiplus-constructing-font-families-and-fonts-use.md)
-   [Рисование текста](-gdiplus-drawing-text-use.md)
-   [Форматирование текста](-gdiplus-formatting-text-use.md)
-   [Перечисление установленных шрифтов](-gdiplus-enumerating-installed-fonts-use.md)
-   [Создание частной коллекции шрифтов](-gdiplus-creating-a-private-font-collection-use.md)
-   [Получение метрик шрифтов](-gdiplus-obtaining-font-metrics-use.md)
-   [Сглаживание текста](-gdiplus-antialiasing-with-text-use.md)

 

 



