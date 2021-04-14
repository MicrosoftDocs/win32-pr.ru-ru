---
description: После внесения незначительных изменений в код можно отправить выходные данные Windows GDI+ на принтер, а не на экран.
ms.assetid: be6286e9-d125-40ad-b33e-b4e734ac2709
title: Печать (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e3b60010bcb63c553a96c5d70826f3fe0d3d4aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985137"
---
# <a name="printing-gdi"></a>Печать (GDI+)

После внесения незначительных изменений в код можно отправить выходные данные Windows GDI+ на принтер, а не на экран. Чтобы рисовать на принтере, получите маркер контекста устройства для принтера и передайте этот обработчик [**графическому**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) конструктору. Размещайте команды GDI+ Drawing между вызовами [стартдок](/windows/win32/api/wingdi/nf-wingdi-startdocw) и [енддок](/windows/win32/api/wingdi/nf-wingdi-enddoc).

В следующих разделах более подробно рассматривается отправка выходных данных GDI+ на принтеры.

-   [Отправка выходных данных GDI+ на принтер](-gdiplus-sending-gdi-output-to-a-printer-use.md)
-   [Отображение диалогового окна «Печать»](-gdiplus-displaying-a-print-dialog-box-use.md)
-   [Оптимизация печати через дескриптор принтера](-gdiplus-optimizing-printing-by-providing-a-printer-handle-use.md)

 

 



