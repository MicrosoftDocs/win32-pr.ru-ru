---
title: Уведомления Event-Based
description: Уведомления Event-Based
ms.assetid: bd483865-f983-416a-9b72-475fe9679cd1
keywords:
- Джойстики, уведомления
- Джойстики, сообщения
- Джойстики, уведомления на основе событий
- Джойстики, пороговое значение перемещения
- уведомления джойстика на основе событий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1aa36809942593cdbe21b61af0d4f07f02b186a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103789997"
---
# <a name="event-based-notifications"></a><span data-ttu-id="21369-108">Уведомления Event-Based</span><span class="sxs-lookup"><span data-stu-id="21369-108">Event-Based Notifications</span></span>

<span data-ttu-id="21369-109">Можно попросить систему отправить джойстику сообщения в приложение каждый раз, когда расположение джойстика изменится на значение, превышающее *порог перемещения* устройства.</span><span class="sxs-lookup"><span data-stu-id="21369-109">You can ask the system to send joystick messages to an application whenever the position of a joystick axis changes by a value greater than the *movement threshold* of the device.</span></span> <span data-ttu-id="21369-110">Пороговое значение перемещения — это расстояние, на которое джойстик необходимо переместить, прежде чем сообщение об изменении расположения джойстика будет отправлено в окно, в котором было захвачено устройство.</span><span class="sxs-lookup"><span data-stu-id="21369-110">The movement threshold is the distance the joystick must be moved before a joystick position change message is sent to a window that has captured the device.</span></span> <span data-ttu-id="21369-111">Дополнительные сведения см. в [**разделе \_ mm JOY1MOVE**](mm-joy1move.md), [**mm \_ JOY1ZMOVE**](mm-joy1zmove.md), [**mm \_ JOY2MOVE**](mm-joy2move.md)или [**mm \_ JOY2ZMOVE**](mm-joy2zmove.md).</span><span class="sxs-lookup"><span data-stu-id="21369-111">For more information, see [**MM\_JOY1MOVE**](mm-joy1move.md), [**MM\_JOY1ZMOVE**](mm-joy1zmove.md), [**MM\_JOY2MOVE**](mm-joy2move.md), or [**MM\_JOY2ZMOVE**](mm-joy2zmove.md).</span></span>

<span data-ttu-id="21369-112">Пороговое значение изначально равно нулю.</span><span class="sxs-lookup"><span data-stu-id="21369-112">The threshold is initially zero.</span></span> <span data-ttu-id="21369-113">Порог перемещения можно задать с помощью функции [**жойсетсрешолд**](/windows/win32/api/joystickapi/nf-joystickapi-joysetthreshold) .</span><span class="sxs-lookup"><span data-stu-id="21369-113">You can set the movement threshold by using the [**joySetThreshold**](/windows/win32/api/joystickapi/nf-joystickapi-joysetthreshold) function.</span></span> <span data-ttu-id="21369-114">Минимальную частоту опроса джойстика можно получить с помощью функции [**жойжетдевкапс**](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps) .</span><span class="sxs-lookup"><span data-stu-id="21369-114">You can retrieve the minimum polling frequency of the joystick by using the [**joyGetDevCaps**](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps) function.</span></span>

 

 