---
title: Настройка окна воспроизведения
description: Настройка окна воспроизведения
ms.assetid: 4cf27099-e5e5-48f8-8d61-0a3d0e0d9499
keywords:
- Функция МЦисендкомманд
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13ed74a133f112935f9ff2ad451e84e3819cee6c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105681608"
---
# <a name="setting-up-the-playback-window"></a><span data-ttu-id="b7b9a-104">Настройка окна воспроизведения</span><span class="sxs-lookup"><span data-stu-id="b7b9a-104">Setting Up the Playback Window</span></span>

<span data-ttu-id="b7b9a-105">В следующем примере выполняется поиск измерений, необходимых для воспроизведения AVI-файла, создается окно, соответствующее этому размеру, и файл воспроизводится в окне с помощью драйвера МЦИАВИ.</span><span class="sxs-lookup"><span data-stu-id="b7b9a-105">The following example finds the dimensions needed to play an AVI file, creates a window corresponding to that size, and plays the file in the window by using the MCIAVI driver.</span></span> <span data-ttu-id="b7b9a-106">В нем используется функция [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b7b9a-106">It uses the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function</span></span>


```C++
HWND hwnd; 
MCI_DGV_RECT_PARMS mciRect; 
 
// Get the movie dimensions with MCI_WHERE. 
 
mciSendCommand(wDeviceID, MCI_WHERE, MCI_DGV_WHERE_SOURCE, 
    (DWORD)(LPSTR)&mciRect); 
 
// Create the playback window. Make it bigger for the border. 
// Note that the right and bottom members of RECT structures in MCI 
// are unusual; rc.right is set to the rectangle's width, and 
// rc.bottom is set to the rectangle's height.

hwndMovie = CreateWindow("mywindow", "Playback", 
    WS_CHILD|WS_BORDER, 0,0, 
    mciRect.rc.right+(2*GetSystemMetric(SM_CXBORDER)),
    mciRect.rc.bottom+(2*GetSystemMetric(SM_CYBORDER)), 
    hwndParent, hInstApp, NULL); 
 
if (hwndMovie){ 
    // Window created OK; make it the playback window. 
 
    MCI_DGV_WINDOW_PARMS mciWindow; 
 
    mciWindow.hWnd = hwndMovie; 
    mciSendCommand(wDeviceID, MCI_WINDOW, MCI_DGV_WINDOW_HWND, 
        (DWORD)(LPSTR)&mciWindow); 
 
} 
```



 

 