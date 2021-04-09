---
title: Уведомления джойстика
description: Уведомления джойстика
ms.assetid: 523dfae3-bbd5-4955-96f3-1710e29d003f
keywords:
- Джойстики, уведомления
- Джойстики, сообщения
- Захваченные джойстики
- неподключенные джойстики
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2791f8da14107d50afe90d8efbdbfe79acba3093
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104069964"
---
# <a name="joystick-notifications"></a><span data-ttu-id="b906e-107">Уведомления джойстика</span><span class="sxs-lookup"><span data-stu-id="b906e-107">Joystick Notifications</span></span>

<span data-ttu-id="b906e-108">Можно записать прямые джойстики для отправки в функцию с помощью функции [**жойсеткаптуре**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) .</span><span class="sxs-lookup"><span data-stu-id="b906e-108">You can capture direct joystick messages to be sent to a function by using the [**joySetCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) function.</span></span> <span data-ttu-id="b906e-109">Только одно приложение за раз может записывать сообщения с джойстика, но вы можете запросить джойстик из другого приложения с помощью функции [**жойжетпос**](/windows/win32/api/joystickapi/nf-joystickapi-joygetpos) или [**жойжетпосекс**](/windows/win32/api/joystickapi/nf-joystickapi-joygetposex) .</span><span class="sxs-lookup"><span data-stu-id="b906e-109">Only one application at a time can capture messages from a joystick, but you can query the joystick from another application by using the [**joyGetPos**](/windows/win32/api/joystickapi/nf-joystickapi-joygetpos) or [**joyGetPosEx**](/windows/win32/api/joystickapi/nf-joystickapi-joygetposex) function.</span></span>

> [!Note]  
> <span data-ttu-id="b906e-110">Возможно, джойстику не удается связаться с приложением, которое записало джойстик, если второе приложение использует **жойжетпос** или **жойжетпосекс** для отправки запросов к джойстику примерно в то же время, когда отправляется сообщение.</span><span class="sxs-lookup"><span data-stu-id="b906e-110">A joystick message can fail to reach the application that captured the joystick if a second application uses **joyGetPos** or **joyGetPosEx** to query the joystick at approximately the same time that the message is sent.</span></span> <span data-ttu-id="b906e-111">В этом случае второе приложение может перехватить сообщение.</span><span class="sxs-lookup"><span data-stu-id="b906e-111">In this case, the second application could intercept the message.</span></span>

 

<span data-ttu-id="b906e-112">Если вы хотите записывать сообщения из двух джойстиков, подключенных к системе, используйте [**жойсеткаптуре**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) дважды, по одному разу для каждого джойстика.</span><span class="sxs-lookup"><span data-stu-id="b906e-112">If you want to capture messages from two joysticks attached to the system, use [**joySetCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) twice, once for each joystick.</span></span> <span data-ttu-id="b906e-113">Окно получает отдельные и отдельные сообщения для каждого устройства.</span><span class="sxs-lookup"><span data-stu-id="b906e-113">Your window receives separate and distinct messages for each device.</span></span>

<span data-ttu-id="b906e-114">Захваченный джойстик можно освободить с помощью функции [**жойрелеасекаптуре**](/windows/win32/api/joystickapi/nf-joystickapi-joyreleasecapture) .</span><span class="sxs-lookup"><span data-stu-id="b906e-114">You can release a captured joystick by using the [**joyReleaseCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joyreleasecapture) function.</span></span> <span data-ttu-id="b906e-115">Если приложение не освобождает джойстик перед завершением, джойстик автоматически выпустится вскоре после уничтожения окна сбора данных.</span><span class="sxs-lookup"><span data-stu-id="b906e-115">If an application does not release the joystick before ending, the joystick is automatically released shortly after the capture window is destroyed.</span></span>

<span data-ttu-id="b906e-116">Невозможно захватить неподключенный джойстик.</span><span class="sxs-lookup"><span data-stu-id="b906e-116">You cannot capture an unplugged joystick.</span></span> <span data-ttu-id="b906e-117">Функция **жойсеткаптуре** возвращает жойерр \_ , не подключенную, если указанное устройство не подключено.</span><span class="sxs-lookup"><span data-stu-id="b906e-117">The **joySetCapture** function returns JOYERR\_UNPLUGGED if the specified device is unplugged.</span></span>

 

 