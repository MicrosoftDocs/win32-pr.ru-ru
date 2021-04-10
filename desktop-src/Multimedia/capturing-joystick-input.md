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
# <a name="capturing-joystick-input"></a>Запись входных данных джойстика

Большая часть кода, управляющего джойстиком, находится в главной функции окна. В следующей части обработчика сообщений приложение вызывает [**жойсеткаптуре**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) для записи входных данных из джойстика JOYSTICKID1.


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



 

 