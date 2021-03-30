---
title: Мониторинг хода выполнения программы сжатия и распаковки
description: Мониторинг хода выполнения программы сжатия и распаковки
ms.assetid: 7c87c688-75b6-4d3e-9dd5-5f509ff2e473
keywords:
- Диспетчер сжатия видео (ВКМ), мониторинг
- ВКМ (диспетчер сжатия видео), мониторинг
- Функция Иксетстатуспрок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beb86a40bb653380dc93e758ada1b2eef6ec9ca7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067853"
---
# <a name="monitoring-compressor-and-decompressor-progress"></a><span data-ttu-id="cb992-106">Мониторинг хода выполнения программы сжатия и распаковки</span><span class="sxs-lookup"><span data-stu-id="cb992-106">Monitoring Compressor and Decompressor Progress</span></span>

<span data-ttu-id="cb992-107">В следующем примере показано, как использовать функцию [**иксетстатуспрок**](/windows/desktop/api/Vfw/nf-vfw-icsetstatusproc) для информирования программы сжатия или декомпрессора адреса функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="cb992-107">The following example shows how the [**ICSetStatusProc**](/windows/desktop/api/Vfw/nf-vfw-icsetstatusproc) function is used to inform the compressor or decompressor of the callback function address:</span></span>


```C++
ICSetStatusProc(compvars.hic, 0, (LPARAM) (UINT) hwndApp, 
    &PreviewStatusProc); 
 
```



<span data-ttu-id="cb992-108">В следующем примере показана функция обратного вызова, установленная предыдущим фрагментом:</span><span class="sxs-lookup"><span data-stu-id="cb992-108">The following example shows the callback function installed by the previous fragment:</span></span>


```C++
LONG CALLBACK export PreviewStatusProc(LPARAM lParam, 
    UINT message, LONG l) 
{ 
    switch (message) 
    { 
        MSG msg; 
        case ICSTATUS_START: 
         
        // Create and display status dialog box. 
         
            break; 
        case ICSTATUS_STATUS: 
            ProSetBarPos((int) l); // sets status bar positions 
 
        // Watch for abort message 
            while(PeekMessage(&msg, NULL, 0, 0, PM_REMOVE)) 
            { 
                if (msg.message == WM_KEYDOWN && msg.wParam == 
                    VK_ESCAPE) 
                    return 1; 
                if (msg.message == WM_SYSCOMMAND && 
                    (msg.wParam & 0xFFF0) == SC_CLOSE) 
                    return 1; 
 
                TranslateMessage(&msg); 
                DispatchMessage(&msg); 
            } 
            break; 
        case ICSTATUS_END: 
         
        // Close and destroy status dialog box. 
         
            break; 
        case ICSTATUS_YIELD: 
         
         
         
            break; 
    } 
    return 0; 
} 
 
```



 

 




