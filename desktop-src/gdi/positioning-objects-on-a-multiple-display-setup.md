---
description: В следующем примере кода показано, как приложения могут правильно позиционировать объекты на несколько экранов. Обратите внимание, что значение RECT основано на источнике (0, 0).
ms.assetid: 1144abfc-ca0a-4d59-aa18-b245ba4b1bc3
title: Размещение объектов при настройке нескольких дисплеев
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd7e00104ea2d48e984fa6898f6e07f23509a6fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344645"
---
# <a name="positioning-objects-on-a-multiple-display-setup"></a><span data-ttu-id="0baef-104">Размещение объектов при настройке нескольких дисплеев</span><span class="sxs-lookup"><span data-stu-id="0baef-104">Positioning Objects on a Multiple Display Setup</span></span>

<span data-ttu-id="0baef-105">В следующем примере кода показано, как приложения могут правильно позиционировать объекты на несколько экранов.</span><span class="sxs-lookup"><span data-stu-id="0baef-105">The following sample code demonstrates how applications can correctly position objects on multiple displays.</span></span> <span data-ttu-id="0baef-106">Обратите внимание, что значение RECT основано на источнике (0, 0).</span><span class="sxs-lookup"><span data-stu-id="0baef-106">Note, do not assume that the RECT is based on the origin (0,0).</span></span>


```C++
#include <windows.h>
#include "multimon.h"    

#define MONITOR_CENTER     0x0001        // center rect to monitor 
#define MONITOR_CLIP     0x0000        // clip rect to monitor 
#define MONITOR_WORKAREA 0x0002        // use monitor work area 
#define MONITOR_AREA     0x0000        // use monitor entire area 

// 
//  ClipOrCenterRectToMonitor 
// 
//  The most common problem apps have when running on a 
//  multimonitor system is that they "clip" or "pin" windows 
//  based on the SM_CXSCREEN and SM_CYSCREEN system metrics. 
//  Because of app compatibility reasons these system metrics 
//  return the size of the primary monitor. 
// 
//  This shows how you use the multi-monitor functions 
//  to do the same thing. 
// 
void ClipOrCenterRectToMonitor(LPRECT prc, UINT flags)
{
    HMONITOR hMonitor;
    MONITORINFO mi;
    RECT        rc;
    int         w = prc->right  - prc->left;
    int         h = prc->bottom - prc->top;

    // 
    // get the nearest monitor to the passed rect. 
    // 
    hMonitor = MonitorFromRect(prc, MONITOR_DEFAULTTONEAREST);

    // 
    // get the work area or entire monitor rect. 
    // 
    mi.cbSize = sizeof(mi);
    GetMonitorInfo(hMonitor, &mi);

    if (flags & MONITOR_WORKAREA)
        rc = mi.rcWork;
    else
        rc = mi.rcMonitor;

    // 
    // center or clip the passed rect to the monitor rect 
    // 
    if (flags & MONITOR_CENTER)
    {
        prc->left   = rc.left + (rc.right  - rc.left - w) / 2;
        prc->top    = rc.top  + (rc.bottom - rc.top  - h) / 2;
        prc->right  = prc->left + w;
        prc->bottom = prc->top  + h;
    }
    else
    {
        prc->left   = max(rc.left, min(rc.right-w,  prc->left));
        prc->top    = max(rc.top,  min(rc.bottom-h, prc->top));
        prc->right  = prc->left + w;
        prc->bottom = prc->top  + h;
    }
}

void ClipOrCenterWindowToMonitor(HWND hwnd, UINT flags)
{
    RECT rc;
    GetWindowRect(hwnd, &rc);
    ClipOrCenterRectToMonitor(&rc, flags);
    SetWindowPos(hwnd, NULL, rc.left, rc.top, 0, 0, SWP_NOSIZE | SWP_NOZORDER | SWP_NOACTIVATE);
}
```



 

 



