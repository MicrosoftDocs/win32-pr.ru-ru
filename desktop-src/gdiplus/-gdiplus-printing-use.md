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
# <a name="printing-gdi"></a><span data-ttu-id="62954-103">Печать (GDI+)</span><span class="sxs-lookup"><span data-stu-id="62954-103">Printing (GDI+)</span></span>

<span data-ttu-id="62954-104">После внесения незначительных изменений в код можно отправить выходные данные Windows GDI+ на принтер, а не на экран.</span><span class="sxs-lookup"><span data-stu-id="62954-104">With a few minor adjustments to your code, you can send Windows GDI+ output to a printer rather than to a screen.</span></span> <span data-ttu-id="62954-105">Чтобы рисовать на принтере, получите маркер контекста устройства для принтера и передайте этот обработчик [**графическому**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) конструктору.</span><span class="sxs-lookup"><span data-stu-id="62954-105">To draw on a printer, obtain a device context handle for the printer and pass that handle to a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) constructor.</span></span> <span data-ttu-id="62954-106">Размещайте команды GDI+ Drawing между вызовами [стартдок](/windows/win32/api/wingdi/nf-wingdi-startdocw) и [енддок](/windows/win32/api/wingdi/nf-wingdi-enddoc).</span><span class="sxs-lookup"><span data-stu-id="62954-106">Place your GDI+ drawing commands in between calls to [StartDoc](/windows/win32/api/wingdi/nf-wingdi-startdocw) and [EndDoc](/windows/win32/api/wingdi/nf-wingdi-enddoc).</span></span>

<span data-ttu-id="62954-107">В следующих разделах более подробно рассматривается отправка выходных данных GDI+ на принтеры.</span><span class="sxs-lookup"><span data-stu-id="62954-107">The following topics cover sending GDI+ output to printers in more detail:</span></span>

-   [<span data-ttu-id="62954-108">Отправка выходных данных GDI+ на принтер</span><span class="sxs-lookup"><span data-stu-id="62954-108">Sending GDI+ Output to a Printer</span></span>](-gdiplus-sending-gdi-output-to-a-printer-use.md)
-   [<span data-ttu-id="62954-109">Отображение диалогового окна «Печать»</span><span class="sxs-lookup"><span data-stu-id="62954-109">Displaying a Print Dialog Box</span></span>](-gdiplus-displaying-a-print-dialog-box-use.md)
-   [<span data-ttu-id="62954-110">Оптимизация печати через дескриптор принтера</span><span class="sxs-lookup"><span data-stu-id="62954-110">Optimizing Printing by Providing a Printer Handle</span></span>](-gdiplus-optimizing-printing-by-providing-a-printer-handle-use.md)

 

 



