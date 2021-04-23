---
title: Автоматизация воспроизведения для МЦивнд
description: Автоматизация воспроизведения для МЦивнд
ms.assetid: 7e38e8b1-f56d-4008-83a7-4fba8333e328
keywords:
- Макрос МЦивндкреате
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b9224cfa4f5a93488f226d1aefa83201b8b0637
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332136"
---
# <a name="automating-playback-for-mciwnd"></a><span data-ttu-id="3326b-104">Автоматизация воспроизведения для МЦивнд</span><span class="sxs-lookup"><span data-stu-id="3326b-104">Automating Playback for MCIWnd</span></span>

<span data-ttu-id="3326b-105">Можно автоматизировать воспроизведение для МЦивнд, указав определенные стили окна в функции [**мЦивндкреате**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) .</span><span class="sxs-lookup"><span data-stu-id="3326b-105">You can automate playback for MCIWnd by specifying certain window styles in the [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) function.</span></span> <span data-ttu-id="3326b-106">Для воспроизведения устройства в окне требуется родительское окно для обработки сообщений уведомления, область воспроизведения для воспроизведения AVI-файлов и уведомление об изменениях режима устройства, чтобы выяснить, когда воспроизведение останавливается.</span><span class="sxs-lookup"><span data-stu-id="3326b-106">To play the device, the window needs a parent window to process notification messages, a playback area to play AVI files, and notification of device mode changes to identify when playback stops.</span></span> <span data-ttu-id="3326b-107">Для окна не нужна панель инструментов.</span><span class="sxs-lookup"><span data-stu-id="3326b-107">The window does not need a toolbar.</span></span> <span data-ttu-id="3326b-108">Эти характеристики можно задать, указав соответствующие стили в **мЦивндкреате**.</span><span class="sxs-lookup"><span data-stu-id="3326b-108">You can set these characteristics by specifying the appropriate styles in **MCIWndCreate**.</span></span>

<span data-ttu-id="3326b-109">В следующем примере команды меню используются для создания окна МЦивнд для воспроизведения содержимого с нескольких различных типов устройств.</span><span class="sxs-lookup"><span data-stu-id="3326b-109">The following example uses menu commands to create an MCIWnd window to play content from several different types of devices.</span></span> <span data-ttu-id="3326b-110">Функция **мЦивндкреате** создает окно мЦивнд, а устройства и файлы загружаются с помощью макроса [**мЦивндопен**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen) в командах, относящихся к конкретному устройству.</span><span class="sxs-lookup"><span data-stu-id="3326b-110">The **MCIWndCreate** function creates the MCIWnd window, and devices and files are loaded by using the [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen) macro in the device-specific commands.</span></span> <span data-ttu-id="3326b-111">После завершения воспроизведения устройство закрывается с помощью перехвата сообщения [**мЦивндм \_ нотифимоде**](mciwndm-notifymode.md) и выдачи макроса [**мЦивндклосе**](/windows/desktop/api/Vfw/nf-vfw-mciwndclose) .</span><span class="sxs-lookup"><span data-stu-id="3326b-111">When a device finishes playing, you close the device by trapping the [**MCIWNDM\_NOTIFYMODE**](mciwndm-notifymode.md) message and issuing the [**MCIWndClose**](/windows/desktop/api/Vfw/nf-vfw-mciwndclose) macro.</span></span>


```C++
case WM_COMMAND: 
    switch (wParam) 
    { 
        case IDM_CREATEMCIWND: 
            dwMCIWndStyle = WS_CHILD |     // child window
                WS_VISIBLE |               // visible
                MCIWNDF_NOTIFYMODE |       // notifies of mode changes
                MCIWNDF_NOPLAYBAR;            // hides toolbar 
            g_hwndMCIWnd = MCIWndCreate(hwnd, 
                g_hinst, dwMCIWndStyle, NULL); 
            break; 
        case IDM_PLAYCDA: 
            LoadNGoMCIWnd(hwnd, "CDAudio"); 
            break; 
        case IDM_PLAYWAVE: 
            LoadNGoMCIWnd(hwnd, "SoundWave.WAV"); 
            break; 
        case IDM_PLAYMIDI: 
            LoadNGoMCIWnd(hwnd, "MIDIFile.MID"); 
            break; 
        case IDM_PLAYAVI: 
            LoadNGoMCIWnd(hwnd, "AVIFile.AVI"); 
            break; 
        case IDM_EXIT: 
            MCIWndDestroy(g_hwndMCIWnd); 
            DestroyWindow(hwnd); 
            break; 
    } 
    break; 
 
case MCIWNDM_NOTIFYMODE: 
    if (lParam == MCI_MODE_STOP)  // device stopped
    { 
        MessageBox(hwnd,"","Closing Device",MB_OK); 
        MCIWndClose(g_hwndMCIWnd); 
    } 
    break; 

// Handle other messages here. 
 
// LoadNGoMCIWnd - automatically loads and plays a multimedia device 
// 
// hwnd -  handle to the parent window 
// lpstr - pointer to device or filename played by device 
// 
// Global variable 
// extern HINSTANCE g_hwndMCIWnd;  instance handle to MCIWnd window 
 
VOID LoadNGoMCIWnd(HWND hwnd, LPSTR lpstr) 
{ 
    MessageBox(hwnd, lpstr, "Loading Device", MB_OK); 
    MCIWndOpen(g_hwndMCIWnd, lpstr, NULL);   // new device in window 
    MCIWndPlay(g_hwndMCIWnd);                // plays device 
} 
```



 

 




