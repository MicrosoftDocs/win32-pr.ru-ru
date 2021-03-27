---
description: Система автоматически обрабатывает рисование в контексте устройства (DC), охватывающем более одного монитора, даже если у мониторов разная глубина цвета.
ms.assetid: 2f03f612-293a-4a42-a13b-1e08e49d9e54
title: Рисование на нескольких мониторах монитора
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09b6a3e3699000399c61e641137a951ed321fd9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811908"
---
# <a name="painting-on-multiple-display-monitors"></a><span data-ttu-id="28226-103">Рисование на нескольких мониторах монитора</span><span class="sxs-lookup"><span data-stu-id="28226-103">Painting on Multiple Display Monitors</span></span>

<span data-ttu-id="28226-104">Система автоматически обрабатывает рисование в контексте устройства (DC), охватывающем более одного монитора, даже если у мониторов разная глубина цвета.</span><span class="sxs-lookup"><span data-stu-id="28226-104">The system automatically handles painting into a device context (DC) that spans more than one monitor, even when the monitors have different color depths.</span></span> <span data-ttu-id="28226-105">Обычно это дает хорошие результаты, но может быть неоптимальной.</span><span class="sxs-lookup"><span data-stu-id="28226-105">Usually this produces good results, but it may not be optimal.</span></span> <span data-ttu-id="28226-106">Например, окно на двух мониторах с значительно отличающимися глубиной цвета может иметь неплохое представление цвета.</span><span class="sxs-lookup"><span data-stu-id="28226-106">For example, a window on two monitors of vastly different color depths could have poor color rendition.</span></span> <span data-ttu-id="28226-107">Кроме того, мониторы с одинаковой глубиной цвета могут иметь разный цвет форматсфор, например, цвета могут быть закодированы с разной количеством битов или находиться в разных местах в значении цвета пикселя.</span><span class="sxs-lookup"><span data-stu-id="28226-107">Also, monitors with the same color depth may have different color formatsfor example, colors could be encoded with different numbers of bits, or be located in different places in a pixel's color value.</span></span>

<span data-ttu-id="28226-108">Чтобы получить лучшие результаты для каждого монитора в контроллере домена, который охватывает несколько дисплеев, вызовите [**енумдисплаймониторс**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) для перечисления мониторов, которые пересекают контроллер домена, и закрасьте пересекающуюся область в каждом из них в соответствии с атрибутами отображения для этого монитора.</span><span class="sxs-lookup"><span data-stu-id="28226-108">To get the best results for each of the monitors in a DC that spans more than one display, call [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) to enumerate the monitors that intersect your DC and paint the intersecting area in each of them separately according to the display attributes for that monitor.</span></span> <span data-ttu-id="28226-109">См. пример [рисования на контроллере домена, охватывающем несколько экранов](painting-on-a-dc-that-spans-multiple-displays.md).</span><span class="sxs-lookup"><span data-stu-id="28226-109">See the example in [Painting on a DC That Spans Multiple Displays](painting-on-a-dc-that-spans-multiple-displays.md).</span></span>

<span data-ttu-id="28226-110">Если вы выполняете все действия в коде **WM \_ Paint** , и если ваш код **\_ рисования WM** обрабатывает все различные видеорежимы, то вы должны иметь возможность разместить код **мониторенумпрока** **WM в \_** [**енумдисплаймониторс**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) с несколькими изменениями.</span><span class="sxs-lookup"><span data-stu-id="28226-110">If you do all of your drawing in your **WM\_PAINT** code and if your **WM\_PAINT** code handles all of the various video modes, then you should be able to place your **WM\_PAINT** code in the **MonitorEnumProc** of [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) with only a few modifications.</span></span>

 

 



