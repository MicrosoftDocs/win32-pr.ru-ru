---
description: Windows GDI+ группирует шрифты с одинаковым шрифтом, но различными стилями в семейства шрифтов.
ms.assetid: 57428fae-6af4-47a5-a499-717dc378767a
title: Создание семейств шрифтов и шрифтов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2761923847a15be6b1ad51eec0d683129b70b349
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997515"
---
# <a name="constructing-font-families-and-fonts"></a>Создание семейств шрифтов и шрифтов

Windows GDI+ группирует шрифты с одинаковым шрифтом, но различными стилями в семейства шрифтов. Например, семейство шрифтов Arial содержит следующие шрифты:

-   Arial Regular
-   Arial Bold
-   Arial курсив
-   Arial полужирный курсив

GDI+ использует четыре стиля для формирования семейств: обычный, полужирный, курсив и полужирный курсив. Прилагательные, такие как *Narrow* и *Round* , не считаются стилями. скорее, они являются частью имени семейства. Например, Arial Narrow — это семейство шрифтов, элементы которого следующие:

-   Arial — узкие обычные
-   Arial Narrow
-   Arial — узкий курсив
-   Arial Narrow полужирный курсив

Прежде чем можно будет рисовать текст с помощью GDI+, необходимо создать объект [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) и объект [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) . Объекты **FontFamily** определяют гарнитуру шрифта (например, Arial), а объект **Font** определяет размер, стиль и единицы измерения.

В следующем примере создается шрифт Arial с обычным начертанием и размером 16 пикселей:


```
FontFamily fontFamily(L"Arial");
Font font(&fontFamily, 16, FontStyleRegular, UnitPixel);
            
```



В приведенном выше коде первый аргумент, передаваемый конструктору [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) , является адресом объекта [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) . Второй аргумент определяет размер шрифта, измеряемого в единицах, определяемых четвертым аргументом. Третий аргумент определяет стиль.

[* * * * Унитпиксел * * * *](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-unit) является членом перечисления **единиц измерения** , а [* * * * фонтстилерегулар *](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-fontstyle) * * * является членом перечисления **FontStyle** . Оба перечисления объявляются в Гдиплусенумс. h.

 

 



