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
ms.openlocfilehash: 465bcf7a7b6b5811de8413a1c89f7befcf81037f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888111"
---
# <a name="limiting-the-playback-scope"></a><span data-ttu-id="4a857-107">Ограничение области воспроизведения</span><span class="sxs-lookup"><span data-stu-id="4a857-107">Limiting the Playback Scope</span></span>

<span data-ttu-id="4a857-108">Управление воспроизведением начинается с макроса [**мЦивндплай**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) , который воспроизводит содержимое или файл, связанный с окном мЦивнд, от текущего расположения воспроизведения до конца содержимого.</span><span class="sxs-lookup"><span data-stu-id="4a857-108">Controlling playback begins with the [**MCIWndPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) macro, which plays the content or file associated with an MCIWnd window from the current playback position to the end of the content.</span></span> <span data-ttu-id="4a857-109">Если требуется ограничить воспроизведение только определенной частью содержимого или файла, можно выбрать другой макрос МЦивнд воспроизведения: [**мЦивндплайфром**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom), [**мЦивндплайто**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto)и [**мЦивндплайфромто**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto).</span><span class="sxs-lookup"><span data-stu-id="4a857-109">If you want to limit playback to a specific portion of the content or file, you can choose from the other playback MCIWnd macros: [**MCIWndPlayFrom**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom), [**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto), and [**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto).</span></span>

<span data-ttu-id="4a857-110">Также необходимо задать соответствующий формат времени.</span><span class="sxs-lookup"><span data-stu-id="4a857-110">You also need to set an appropriate time format.</span></span> <span data-ttu-id="4a857-111">Формат времени определяет, измеряется ли содержимое в кадрах, миллисекундах, дорожках или других единицах.</span><span class="sxs-lookup"><span data-stu-id="4a857-111">The time format determines whether the content is measured in frames, milliseconds, tracks, or some other units.</span></span>

<span data-ttu-id="4a857-112">В следующем примере создается окно МЦивнд и предоставляются команды меню для воспроизведения последней третьей, первой третьей или средней трети содержимого.</span><span class="sxs-lookup"><span data-stu-id="4a857-112">The following example creates an MCIWnd window and provides menu commands to play the last third, first third, or middle third of the content.</span></span> <span data-ttu-id="4a857-113">Эти команды меню используют **мЦивндплайфром**, **мЦивндплайто** и **мЦивндплайфромто** для воспроизведения сегментов содержимого.</span><span class="sxs-lookup"><span data-stu-id="4a857-113">These menu commands use **MCIWndPlayFrom**, **MCIWndPlayTo**, and **MCIWndPlayFromTo** to play the content segments.</span></span> <span data-ttu-id="4a857-114">В примере также используются макросы [**мЦивнджетстарт**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart) и [**мЦивнджетенд**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend) для обнаружения начала и конца содержимого, а для перемещения положения воспроизведения в начало содержимого используется макрос [**мЦивндхоме**](/windows/desktop/api/Vfw/nf-vfw-mciwndhome) .</span><span class="sxs-lookup"><span data-stu-id="4a857-114">The example also uses the [**MCIWndGetStart**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart) and [**MCIWndGetEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend) macros to identify the beginning and end of the content, and it uses the [**MCIWndHome**](/windows/desktop/api/Vfw/nf-vfw-mciwndhome) macro to move the playback position to the beginning of the content.</span></span>

<span data-ttu-id="4a857-115">Функция [**мЦивндкреате**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) использует \_ стили WS Caption и мЦивндф \_ SHOWALL в дополнение к стандартным стилям окна для вывода имени файла, режима и текущего расположения воспроизведения в заголовке окна мЦивнд.</span><span class="sxs-lookup"><span data-stu-id="4a857-115">The [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) function uses the WS\_CAPTION and MCIWNDF\_SHOWALL styles in addition to the standard window styles to display the filename, mode, and current playback position in the title bar of the MCIWnd window.</span></span>


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



 

 




