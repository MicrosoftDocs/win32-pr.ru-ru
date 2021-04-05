---
title: Настройка процесса записи
description: Настройка процесса записи
ms.assetid: 9453b9d3-ae9c-4f57-8dd6-f84b9a76618e
keywords:
- Функция МЦивндкреате
- Макрос МЦивнднев
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec46f61ef4624ba613025f01b081ccc1ebda1cad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986450"
---
# <a name="customizing-the-recording-process"></a><span data-ttu-id="4b618-105">Настройка процесса записи</span><span class="sxs-lookup"><span data-stu-id="4b618-105">Customizing the Recording Process</span></span>

<span data-ttu-id="4b618-106">Вы можете настроить процесс записи, полностью контролируя все, — от создания окна МЦивнд до сохранения записанных данных в файле.</span><span class="sxs-lookup"><span data-stu-id="4b618-106">You can customize the recording process, taking complete control of most everything — from creating the MCIWnd window to saving the recorded information in a file.</span></span> <span data-ttu-id="4b618-107">В следующем примере выполняется запрос к устройству MCI для записи и сохранения возможностей, а также команды меню для записи в начало или конец содержимого.</span><span class="sxs-lookup"><span data-stu-id="4b618-107">The following example queries the MCI device for recording and saving capabilities, and includes menu commands to record at the beginning or end of the content.</span></span>

<span data-ttu-id="4b618-108">В следующем примере функция [**мЦивндкреате**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) используется для создания нового окна и позволяет указать существующий файл для хранения записанных данных и макрос [**мЦивнднев**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew) , чтобы связать новый файл с окном.</span><span class="sxs-lookup"><span data-stu-id="4b618-108">The following example uses the [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) function to create a new window and allows you to specify an existing file to store the recorded data and the [**MCIWndNew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew) macro to associate a new file with the window.</span></span> <span data-ttu-id="4b618-109">Кроме того, для указания файла можно использовать макрос [**мЦивндопен**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen) или [**мЦивндопендиалог**](/windows/desktop/api/Vfw/nf-vfw-mciwndopendialog) .</span><span class="sxs-lookup"><span data-stu-id="4b618-109">Alternatively, you can use the [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen) or [**MCIWndOpenDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndopendialog) macro to specify a file.</span></span>

<span data-ttu-id="4b618-110">В примере используется макрос [**мЦивндканрекорд**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanrecord) , чтобы убедиться, что устройство может записать и макрос [**мЦивндкансаве**](/windows/desktop/api/Vfw/nf-vfw-mciwndcansave) , чтобы убедиться, что устройство сохраняет информацию.</span><span class="sxs-lookup"><span data-stu-id="4b618-110">The example uses the [**MCIWndCanRecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanrecord) macro to verify that the device can record and the [**MCIWndCanSave**](/windows/desktop/api/Vfw/nf-vfw-mciwndcansave) macro to verify that the device save information.</span></span> <span data-ttu-id="4b618-111">В примере текущая позицией воспроизведения задается с помощью макросов [**мЦивндхоме**](/windows/desktop/api/Vfw/nf-vfw-mciwndhome) и [**мЦивнденд**](/windows/desktop/api/Vfw/nf-vfw-mciwndend) .</span><span class="sxs-lookup"><span data-stu-id="4b618-111">The example sets the current playback position by using the [**MCIWndHome**](/windows/desktop/api/Vfw/nf-vfw-mciwndhome) and [**MCIWndEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndend) macros.</span></span> <span data-ttu-id="4b618-112">В примере начинается запись с помощью макроса [**мЦивндрекорд**](/windows/desktop/api/Vfw/nf-vfw-mciwndrecord) .</span><span class="sxs-lookup"><span data-stu-id="4b618-112">The example starts recording by using the [**MCIWndRecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndrecord) macro.</span></span> <span data-ttu-id="4b618-113">После записи данных в примере сохраняется с помощью макроса [**мЦивндсаведиалог**](/windows/desktop/api/Vfw/nf-vfw-mciwndsavedialog) .</span><span class="sxs-lookup"><span data-stu-id="4b618-113">After the information is recorded, the example saves it by using the [**MCIWndSaveDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndsavedialog) macro.</span></span>


```C++
case WM_COMMAND: 
    switch (wParam) 
    { 
        case IDM_CREATEMCIWND: 
            g_hwndMCIWnd = MCIWndCreate( hwnd, g_hinst, 
                WS_VISIBLE | WS_CHILD | 
                MCIWNDF_RECORD,                   // add Record button
                NULL ); 
 
            MCIWndNew(g_hwndMCIWnd, "waveaudio"); // new file 
 
            if( MCIWndCanRecord(g_hwndMCIWnd) ) 
            { 
                MessageBox( hwnd, 
                "Press the red button on the toolbar to record.", 
                "MCIWnd Record", 
                MB_OK ); 
            } 
            else 
            { 
                MessageBox( hwnd, 
                    "This device doesn't record.", 
                    "MCIWnd Record", 
                    MB_OK ); 
            } 
            break; 
        case IDM_RECORDATSTART: 
            if( MCIWndCanRecord(g_hwndMCIWnd) ) 
            { 
                MCIWndHome(g_hwndMCIWnd); 
                MCIWndRecord(g_hwndMCIWnd); 
            } 
            else 
            { 
                MessageBox( hwnd, 
                    "This device doesn't record.", 
                    "MCIWnd Record", 
                    MB_OK); 
            } 
            break; 
        case IDM_RECORDATEND: 
            if( MCIWndCanRecord(g_hwndMCIWnd) ) 
            { 
                MCIWndEnd(g_hwndMCIWnd); 
                MCIWndRecord(g_hwndMCIWnd); 
            } 
            else 
            { 
                MessageBox( hwnd, 
                    "This device doesn't record.", 
                    "MCIWnd Record", 
                    MB_OK); 
            } 
            break; 
        case IDM_SAVEMCIWND: 
            if( MCIWndCanSave(g_hwndMCIWnd) ) 
                MCIWndSaveDialog(g_hwndMCIWnd); 
    } 
    break; 
 
    // Handle other messages here. 
```



 

 




