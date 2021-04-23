---
title: Обработка сообщений джойстика
description: Обработка сообщений джойстика
ms.assetid: d21a9d49-1fc0-4899-9083-87c3cf4e0e62
keywords:
- Джойстики, сообщения
- Сообщение MM_JOY1MOVE
- Сообщение MM_JOY1BUTTONDOWN
- Сообщение MM_JOY1BUTTONUP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f2337d392c0104dcb49839b19c5fb615481ee2a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067776"
---
# <a name="processing-joystick-messages"></a><span data-ttu-id="d649a-107">Обработка сообщений джойстика</span><span class="sxs-lookup"><span data-stu-id="d649a-107">Processing Joystick Messages</span></span>

<span data-ttu-id="d649a-108">В следующем примере показано, как приложение может реагировать на перемещения джойстика и изменения в состояниях кнопок.</span><span class="sxs-lookup"><span data-stu-id="d649a-108">The following example illustrates how an application could respond to joystick movements and changes in the button states.</span></span> <span data-ttu-id="d649a-109">Когда джойстик меняет позицию, приложение перемещает курсор и, если нажата какая-либо кнопка, выводит на Рабочий стол отверстие маркера.</span><span class="sxs-lookup"><span data-stu-id="d649a-109">When the joystick changes position, the application moves the cursor and, if either button is pressed, draws a bullet hole on the desktop.</span></span> <span data-ttu-id="d649a-110">При нажатии кнопки джойстика приложение рисует отверстие на рабочем столе и воспроизводит звук непрерывно до тех пор, пока не будет снята кнопка.</span><span class="sxs-lookup"><span data-stu-id="d649a-110">When a joystick button is pressed, the application draws a hole on the desktop and plays a sound continuously until a button is released.</span></span> <span data-ttu-id="d649a-111">Сообщения для отслеживания: [**mm \_ JOY1MOVE**](mm-joy1move.md), [**mm \_ JOY1BUTTONDOWN**](mm-joy1buttondown.md)и [**mm \_ JOY1BUTTONUP**](mm-joy1buttonup.md).</span><span class="sxs-lookup"><span data-stu-id="d649a-111">The messages to watch are [**MM\_JOY1MOVE**](mm-joy1move.md), [**MM\_JOY1BUTTONDOWN**](mm-joy1buttondown.md), and [**MM\_JOY1BUTTONUP**](mm-joy1buttonup.md).</span></span>


```C++
case MM_JOY1MOVE :                     // changed position 
    if((UINT) wParam & (JOY_BUTTON1 | JOY_BUTTON2)) 
        DrawFire(hWnd); 
    DrawSight(lParam);                 // calculates new cursor position 
    break; 
case MM_JOY1BUTTONDOWN :               // button is down 
    if((UINT) wParam & JOY_BUTTON1) 
    { 
        PlaySound(lpButton1, SND_LOOP | SND_ASYNC | SND_MEMORY); 
        DrawFire(hWnd); 
    } 
    else if((UINT) wParam & JOY_BUTTON2) 
    { 
        PlaySound(lpButton2, SND_ASYNC | SND_MEMORY |  SND_LOOP); 
        DrawFire(hWnd); 
    } 
    break; 
case MM_JOY1BUTTONUP :                 // button is up 
    sndPlaySound(NULL, 0);             // stops the sound 
    break; 

```



 

 




