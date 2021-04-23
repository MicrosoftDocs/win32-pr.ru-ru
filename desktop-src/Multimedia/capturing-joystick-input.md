---
title: Запись входных данных джойстика
description: Запись входных данных джойстика
ms.assetid: 1214fe5a-5a6a-4c6c-9b77-94eeb73f60da
keywords:
- Джойстики, запись входных данных
- запись входных данных джойстика
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b23fd3717ad09fd2e52f1a815f7d13b91963a13e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104133846"
---
# <a name="capturing-joystick-input"></a><span data-ttu-id="485c9-105">Запись входных данных джойстика</span><span class="sxs-lookup"><span data-stu-id="485c9-105">Capturing Joystick Input</span></span>

<span data-ttu-id="485c9-106">Большая часть кода, управляющего джойстиком, находится в главной функции окна.</span><span class="sxs-lookup"><span data-stu-id="485c9-106">Most of the code controlling the joystick is in the main window function.</span></span> <span data-ttu-id="485c9-107">В следующей части обработчика сообщений приложение вызывает [**жойсеткаптуре**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) для записи входных данных из джойстика JOYSTICKID1.</span><span class="sxs-lookup"><span data-stu-id="485c9-107">In the following portion of the message handler, the application calls [**joySetCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) to capture input from the joystick JOYSTICKID1.</span></span>


```C++
case WM_CREATE: 
    if(joySetCapture(hWnd, JOYSTICKID1, NULL, FALSE)) 
    { 
        MessageBeep(MB_ICONEXCLAMATION); 
        MessageBox(hWnd, "Couldn't capture the joystick.", NULL, 
            MB_OK | MB_ICONEXCLAMATION); 
        PostMessage(hWnd,WM_CLOSE,0,0L); 
    } 
    break; 
 
```



 

 