---
description: после внесения незначительных изменений в код можно отправить Windows GDI+ вывода на принтер, а не на экран.
ms.assetid: be6286e9-d125-40ad-b33e-b4e734ac2709
title: Печать (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49f5807c976ef3224bc4b66afc0bb8637d79d725f12cbdebd3199d9710ae529a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117885085"
---
# <a name="printing-gdi"></a>Печать (GDI+)

после внесения незначительных изменений в код можно отправить Windows GDI+ вывода на принтер, а не на экран. Чтобы рисовать на принтере, получите маркер контекста устройства для принтера и передайте этот обработчик [**графическому**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) конструктору. размещайте GDI+ команды рисования между вызовами [стартдок](/windows/win32/api/wingdi/nf-wingdi-startdocw) и [енддок](/windows/win32/api/wingdi/nf-wingdi-enddoc).

в следующих разделах рассматриваются более подробные сведения об отправке GDI+ вывода на принтеры.

-   [Отправка выходных данных GDI+ на принтер](-gdiplus-sending-gdi-output-to-a-printer-use.md)
-   [Отображение диалогового окна «Печать»](-gdiplus-displaying-a-print-dialog-box-use.md)
-   [Оптимизация печати через дескриптор принтера](-gdiplus-optimizing-printing-by-providing-a-printer-handle-use.md)

 

 



