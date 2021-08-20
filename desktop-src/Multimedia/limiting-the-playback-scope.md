---
title: Ограничение области воспроизведения
description: Ограничение области воспроизведения
ms.assetid: 080ab96f-1cb5-48d4-ac0a-8fd9ba68a31a
keywords:
- Макрос МЦивндплайфром
- Макрос МЦивндплайто
- Макрос МЦивндплайфромто
- Команды воспроизведения MCI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 064f62e913c33bef0582efaa950ee376e31a5b06a54d0e70674192e31a679a9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118139487"
---
# <a name="limiting-the-playback-scope"></a>Ограничение области воспроизведения

Управление воспроизведением начинается с макроса [**мЦивндплай**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) , который воспроизводит содержимое или файл, связанный с окном мЦивнд, от текущего расположения воспроизведения до конца содержимого. Если требуется ограничить воспроизведение только определенной частью содержимого или файла, можно выбрать другой макрос МЦивнд воспроизведения: [**мЦивндплайфром**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom), [**мЦивндплайто**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto)и [**мЦивндплайфромто**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto).

Также необходимо задать соответствующий формат времени. Формат времени определяет, измеряется ли содержимое в кадрах, миллисекундах, дорожках или других единицах.

В следующем примере создается окно МЦивнд и предоставляются команды меню для воспроизведения последней третьей, первой третьей или средней трети содержимого. Эти команды меню используют **мЦивндплайфром**, **мЦивндплайто** и **мЦивндплайфромто** для воспроизведения сегментов содержимого. В примере также используются макросы [**мЦивнджетстарт**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart) и [**мЦивнджетенд**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend) для обнаружения начала и конца содержимого, а для перемещения положения воспроизведения в начало содержимого используется макрос [**мЦивндхоме**](/windows/desktop/api/Vfw/nf-vfw-mciwndhome) .

Функция [**мЦивндкреате**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) использует \_ стили WS Caption и мЦивндф \_ SHOWALL в дополнение к стандартным стилям окна для вывода имени файла, режима и текущего расположения воспроизведения в заголовке окна мЦивнд.


```C++
case WM_COMMAND: 
    switch (wParam) 
    { 
        case IDM_CREATEMCIWND: 
            g_hwndMCIWnd = MCIWndCreate(hwnd, 
                g_hinst, 
                WS_CHILD | WS_VISIBLE | WS_CAPTION | 
                MCIWNDF_SHOWALL, 
                "sample.avi"); 
            break;
        case IDM_PLAYFROM:                // plays last third of clip 
            MCIWndUseTime(g_hwndMCIWnd);  // millisecond format 
 
        // Get media start and end positions. 
            lStart = MCIWndGetStart(g_hwndMCIWnd); 
            lEnd = MCIWndGetEnd(g_hwndMCIWnd); 
 
        // Determine playback end position. 
            lPlayStart = 2 * (lEnd - lStart) / 3 + lStart; 
 
            MCIWndPlayFrom(g_hwndMCIWnd, lPlayStart); 
            break; 
        case IDM_PLAYTO:                  // plays first third of clip 
            MCIWndUseTime(g_hwndMCIWnd);  // millisecond format 
 
        // Get media start and end positions. 
            lStart = MCIWndGetStart(g_hwndMCIWnd); 
            lEnd = MCIWndGetEnd(g_hwndMCIWnd); 
 
        // Determine playback start position. 
            lPlayEnd = (lEnd - lStart) / 3 + lStart;
 
            MCIWndHome(g_hwndMCIWnd); 
            MCIWndPlayTo(g_hwndMCIWnd, lPlayEnd); 
            break; 
        case IDM_PLAYSOME:               // plays middle third of clip 
            MCIWndUseTime(g_hwndMCIWnd); // millisecond format 
 
        // Get media start and end positions. 
            lStart = MCIWndGetStart(g_hwndMCIWnd); 
            lEnd = MCIWndGetEnd(g_hwndMCIWnd); 
 
        // Determine playback start and end positions. 
            lPlayStart = (lEnd - lStart) / 3 + lStart;
            lPlayEnd = 2 * (lEnd - lStart) / 3 + lStart; 
 
            MCIWndPlayFromTo(g_hwndMCIWnd, lPlayStart, lPlayEnd); 
            break; 
    
    // Handle other commands here. 
    } 
```



 

 




