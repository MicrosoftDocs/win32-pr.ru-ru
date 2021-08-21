---
description: Графический объект предоставляет такие методы, как DrawLine, DrawImage и DrawString для отображения векторных изображений, растровых изображений и текста.
ms.assetid: 721d0c1c-d105-4d9f-b5e9-6ca407b28c4e
title: Использование графических контейнеров
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96292395113b80ec79f8b59d4ac7f203c3d1f2d892c2da62ce4957e49b81860d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036292"
---
# <a name="using-graphics-containers"></a>Использование графических контейнеров

[**Графический**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объект предоставляет такие методы, как [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)), [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint))и [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) для отображения векторных изображений, растровых изображений и текста. Объект **Graphics** также имеет несколько свойств, влияющих на качество и ориентацию рисуемых элементов. Например, свойство «режим сглаживания» определяет, применяется ли сглаживание к линиям и кривым, а свойство «мировое преобразование» влияет на расположение и поворот рисуемых элементов.

[**Графический**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объект часто связывается с конкретным устройством вывода. При использовании **графического** объекта для рисования в окне **графический** объект также связывается с этим конкретным окном.

Объект [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) можно рассматривать как контейнер, так как он содержит набор свойств, влияющих на прорисовку, и связан с информацией, относящейся к конкретному устройству. Вы можете создать дополнительный контейнер в существующем объекте **Graphics** , вызвав метод [бегинконтаинер](/previous-versions//ms535731(v=vs.85)) этого **графического** объекта.

В следующих разделах более подробно рассматриваются [**графические**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) объекты и вложенные контейнеры.

-   [Состояние графического объекта](-gdiplus-the-state-of-a-graphics-object-use.md)
-   [Вложенные графические контейнеры](-gdiplus-nested-graphics-containers-use.md)

 

 
