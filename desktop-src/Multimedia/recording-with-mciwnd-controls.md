---
title: Запись с помощью элементов управления МЦивнд
description: Запись с помощью элементов управления МЦивнд
ms.assetid: 65a57400-aeea-4a27-8d51-37d3d9e9bd55
keywords:
- Функция МЦивндкреате
- Макрос МЦивнднев
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 814bd9f92b895c03ccbb073f830dbf31dcd2e3c2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986189"
---
# <a name="recording-with-mciwnd-controls"></a><span data-ttu-id="13993-105">Запись с помощью элементов управления МЦивнд</span><span class="sxs-lookup"><span data-stu-id="13993-105">Recording with MCIWnd Controls</span></span>

<span data-ttu-id="13993-106">В следующем примере записывается звук звукозаписи с помощью встроенных элементов управления окна МЦивнд.</span><span class="sxs-lookup"><span data-stu-id="13993-106">The following example records waveform audio using the built-in controls of the MCIWnd window.</span></span> <span data-ttu-id="13993-107">В примере создается окно МЦивнд с помощью \_ стиля окна записи мЦивндф с функцией [**мЦивндкреате**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) для добавления кнопки **записи** на панель инструментов.</span><span class="sxs-lookup"><span data-stu-id="13993-107">The example creates an MCIWnd window by using the MCIWNDF\_RECORD window style with the [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) function to add a **Record** button to the toolbar.</span></span> <span data-ttu-id="13993-108">Макрос [**мЦивнднев**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew) указывает, что новый файл связан с окном мЦивнд и что устройство аудио аудио будет предоставлять свое содержимое.</span><span class="sxs-lookup"><span data-stu-id="13993-108">The [**MCIWndNew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew) macro indicates a new file is associated with the MCIWnd window and that a waveform-audio device will provide its content.</span></span> <span data-ttu-id="13993-109">Вторая команда меню, IDM \_ савемЦивнд, позволяет пользователю сохранить запись и выбрать имя файла с помощью макроса [**мЦивндсаведиалог**](/windows/desktop/api/Vfw/nf-vfw-mciwndsavedialog) .</span><span class="sxs-lookup"><span data-stu-id="13993-109">A second menu command, IDM\_SAVEMCIWND, lets the user save the recording and select a filename by using the [**MCIWndSaveDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndsavedialog) macro.</span></span>


```C++
case WM_COMMAND: 
    switch (wParam) { 
    case IDM_CREATEMCIWND: 
        g_hwndMCIWnd = MCIWndCreate(hwnd, g_hinst, 
            WS_VISIBLE | MCIWNDF_RECORD, NULL); 
        MCIWndNew(g_hwndMCIWnd, "waveaudio"); 
        break;    
    case IDM_SAVEMCIWND: 
        MCIWndSaveDialog(g_hwndMCIWnd); 
        break; 
    } 
```



 

 




