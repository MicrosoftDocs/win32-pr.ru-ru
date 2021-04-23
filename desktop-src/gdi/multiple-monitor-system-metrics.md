---
description: Функция Жетсистемметрикс возвращает значения для основного монитора, за исключением SM \_ кксмакстракк и SM \_ цимакстракк, которые ссылаются на весь рабочий стол.
ms.assetid: d0105363-1895-4e10-8a33-648a6fc4c20a
title: Метрики системы с несколькими мониторами
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 149f4da5c687df28817105e1ec3876ffd1ab5649
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155602"
---
# <a name="multiple-monitor-system-metrics"></a><span data-ttu-id="74bc3-103">Метрики системы с несколькими мониторами</span><span class="sxs-lookup"><span data-stu-id="74bc3-103">Multiple Monitor System Metrics</span></span>

<span data-ttu-id="74bc3-104">Функция [**жетсистемметрикс**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) возвращает значения для основного монитора, за исключением SM \_ кксмакстракк и SM \_ цимакстракк, которые ссылаются на весь рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="74bc3-104">The [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) function returns values for the primary monitor, except for SM\_CXMAXTRACK and SM\_CYMAXTRACK, which refer to the entire desktop.</span></span> <span data-ttu-id="74bc3-105">Следующие метрики одинаковы для всех драйверов устройств: SM \_ ккскурсор, SM \_ ЦИКУРСОР, SM \_ кксикон, смциикон.</span><span class="sxs-lookup"><span data-stu-id="74bc3-105">The following metrics are the same for all device drivers: SM\_CXCURSOR, SM\_CYCURSOR, SM\_CXICON, SMCYICON.</span></span> <span data-ttu-id="74bc3-106">Следующие возможности экрана одинаковы для всех мониторов: ЛОГПИКСЕЛСКС, ЛОГПИКСЕЛСИ, ДЕСТОФОРЗРЕС, ДЕСКТОПВЕРТРЕС.</span><span class="sxs-lookup"><span data-stu-id="74bc3-106">The following display capabilities are the same for all monitors: LOGPIXELSX, LOGPIXELSY, DESTOPHORZRES, DESKTOPVERTRES.</span></span>

<span data-ttu-id="74bc3-107">[**Жетсистемметрикс**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) также содержит константы, которые ссылаются только на систему с несколькими мониторами.</span><span class="sxs-lookup"><span data-stu-id="74bc3-107">[**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) also has constants that refer only to a Multiple Monitor system.</span></span> <span data-ttu-id="74bc3-108">SM \_ ксвиртуалскрин и SM \_ ивиртуалскрин определяют левый верхний угол виртуального экрана, SM \_ кксвиртуалскрин и SM \_ цивиртуалскрин являются вертикальными и горизонтальными измерениями виртуального экрана, SM \_ кмониторс — число мониторов, подключенных к рабочему столу, и SM \_ самедисплайформат указывает, имеют ли все мониторы на рабочем столе одинаковый цветовой формат.</span><span class="sxs-lookup"><span data-stu-id="74bc3-108">SM\_XVIRTUALSCREEN and SM\_YVIRTUALSCREEN identify the upper-left corner of the virtual screen, SM\_CXVIRTUALSCREEN and SM\_CYVIRTUALSCREEN are the vertical and horizontal measurements of the virtual screen, SM\_CMONITORS is the number of monitors attached to the desktop, and SM\_SAMEDISPLAYFORMAT indicates whether all the monitors on the desktop have the same color format.</span></span>

<span data-ttu-id="74bc3-109">Чтобы получить сведения о одном мониторе отображения или всех мониторах монитора на рабочем столе, используйте Енумдисплаймониторс.</span><span class="sxs-lookup"><span data-stu-id="74bc3-109">To get information about a single display monitor or all of the display monitors in a desktop, use EnumDisplayMonitors.</span></span> <span data-ttu-id="74bc3-110">Прямоугольник окна рабочего стола, возвращаемый функцией [**жетвиндоврект**](/windows/win32/api/winuser/nf-winuser-getwindowrect) или [**жетклиентрект**](/windows/win32/api/winuser/nf-winuser-getclientrect) , всегда равен прямоугольнику основного монитора для совместимости с существующими приложениями.</span><span class="sxs-lookup"><span data-stu-id="74bc3-110">The rectangle of the desktop window returned by [**GetWindowRect**](/windows/win32/api/winuser/nf-winuser-getwindowrect) or [**GetClientRect**](/windows/win32/api/winuser/nf-winuser-getclientrect) is always equal to the rectangle of the primary monitor, for compatibility with existing applications.</span></span> <span data-ttu-id="74bc3-111">Таким образом, результат</span><span class="sxs-lookup"><span data-stu-id="74bc3-111">Thus, the result of</span></span>


```C++
GetWindowRect(GetDesktopWindow(), &rc);
```



<span data-ttu-id="74bc3-112">будет:</span><span class="sxs-lookup"><span data-stu-id="74bc3-112">will be:</span></span>


```C++
rc.left = 0; 
rc.top = 0; 
rc.right = GetSystemMetrics (SM_CXSCREEN); 
rc.bottom = GetSystemMetrics (SM_CYSCREEN);
```



<span data-ttu-id="74bc3-113">Чтобы изменить рабочую область монитора, вызовите [**системпараметерсинфо**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) с SPI \_ сетворкареа и *пвпарам* , указывающим на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) , которая находится на нужном мониторе.</span><span class="sxs-lookup"><span data-stu-id="74bc3-113">To change the work area of a monitor, call [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) with SPI\_SETWORKAREA and *pvParam* pointing to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that is on the desired monitor.</span></span> <span data-ttu-id="74bc3-114">Если *пвпарам* имеет **значение NULL**, изменяется Рабочая область основного монитора.</span><span class="sxs-lookup"><span data-stu-id="74bc3-114">If *pvParam* is **NULL**, the work area of the primary monitor is modified.</span></span> <span data-ttu-id="74bc3-115">Использование SPI \_ жетворкареа всегда возвращает рабочую область основного монитора.</span><span class="sxs-lookup"><span data-stu-id="74bc3-115">Using SPI\_GETWORKAREA always returns the work area of the primary monitor.</span></span> <span data-ttu-id="74bc3-116">Чтобы получить рабочую область монитора, отличного от основного, вызовите [**жетмониторинфо**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa).</span><span class="sxs-lookup"><span data-stu-id="74bc3-116">To get the work area of a monitor other than the primary monitor, call [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa).</span></span>

 

 
