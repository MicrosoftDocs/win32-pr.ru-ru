---
title: Сообщения уведомления джойстика
description: Сообщения уведомления джойстика
ms.assetid: 9e8ccc1b-85a9-44bf-b561-6ad4c10cddd1
keywords:
- Джойстики, уведомления
- Джойстики, сообщения
- Джойстики, расположение
- Джойстики, кнопки
- Сообщения MM_JOY1
- Сообщения MM_JOY2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 698f999dab49ea6684e9184f6ed5c46286518b97
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105672037"
---
# <a name="joystick-notification-messages"></a><span data-ttu-id="4b094-109">Сообщения уведомления джойстика</span><span class="sxs-lookup"><span data-stu-id="4b094-109">Joystick Notification Messages</span></span>

<span data-ttu-id="4b094-110">Джойстик сообщений уведомляет приложение о том, что джойстик изменил расположение или что одна из ее кнопок изменила состояние.</span><span class="sxs-lookup"><span data-stu-id="4b094-110">Joystick messages notify your application that a joystick has changed position or that one of its buttons has changed states.</span></span> <span data-ttu-id="4b094-111">Сообщения, начинающиеся с MM \_ JOY1, отправляются в функцию, если приложение запрашивает входные данные из джойстика с помощью идентификатора JOYSTICKID1, а mm \_ JOY2 отправляет сообщения, если приложение запрашивает входные данные из джойстика с помощью идентификатора JOYSTICKID2.</span><span class="sxs-lookup"><span data-stu-id="4b094-111">Messages beginning with MM\_JOY1 are sent to the function if your application requests input from the joystick using the identifier JOYSTICKID1, and MM\_JOY2 messages are sent if your application requests input from the joystick using the identifier JOYSTICKID2.</span></span>

<span data-ttu-id="4b094-112">Сообщения в следующей таблице указывают состояние кнопок джойстика:</span><span class="sxs-lookup"><span data-stu-id="4b094-112">The messages in the following table identify the status of the joystick buttons:</span></span>



| <span data-ttu-id="4b094-113">Сообщение</span><span class="sxs-lookup"><span data-stu-id="4b094-113">Message</span></span>                                         | <span data-ttu-id="4b094-114">Описание</span><span class="sxs-lookup"><span data-stu-id="4b094-114">Description</span></span>                                                     |
|-------------------------------------------------|-----------------------------------------------------------------|
| [<span data-ttu-id="4b094-115">**\_JOY1BUTTONDOWN мм**</span><span class="sxs-lookup"><span data-stu-id="4b094-115">**MM\_JOY1BUTTONDOWN**</span></span>](mm-joy1buttondown.md) | <span data-ttu-id="4b094-116">Была нажата кнопка на джойстике JOYSTICKID1.</span><span class="sxs-lookup"><span data-stu-id="4b094-116">A button on joystick JOYSTICKID1 has been pressed.</span></span>              |
| [<span data-ttu-id="4b094-117">**\_JOY1BUTTONUP мм**</span><span class="sxs-lookup"><span data-stu-id="4b094-117">**MM\_JOY1BUTTONUP**</span></span>](mm-joy1buttonup.md)     | <span data-ttu-id="4b094-118">Была снята кнопка на джойстике JOYSTICKID1.</span><span class="sxs-lookup"><span data-stu-id="4b094-118">A button on joystick JOYSTICKID1 has been released.</span></span>             |
| [<span data-ttu-id="4b094-119">**\_JOY1MOVE мм**</span><span class="sxs-lookup"><span data-stu-id="4b094-119">**MM\_JOY1MOVE**</span></span>](mm-joy1move.md)             | <span data-ttu-id="4b094-120">Джойстик JOYSTICKID1 измененное расположение в направлении x или y.</span><span class="sxs-lookup"><span data-stu-id="4b094-120">Joystick JOYSTICKID1 changed position in the x- or y-direction.</span></span> |
| [<span data-ttu-id="4b094-121">**\_JOY1ZMOVE мм**</span><span class="sxs-lookup"><span data-stu-id="4b094-121">**MM\_JOY1ZMOVE**</span></span>](mm-joy1zmove.md)           | <span data-ttu-id="4b094-122">Джойстик JOYSTICKID1 измененное расположение в z-направлении.</span><span class="sxs-lookup"><span data-stu-id="4b094-122">Joystick JOYSTICKID1 changed position in the z-direction.</span></span>       |
| [<span data-ttu-id="4b094-123">**\_JOY2BUTTONDOWN мм**</span><span class="sxs-lookup"><span data-stu-id="4b094-123">**MM\_JOY2BUTTONDOWN**</span></span>](mm-joy2buttondown.md) | <span data-ttu-id="4b094-124">Была нажата кнопка на джойстике JOYSTICKID2.</span><span class="sxs-lookup"><span data-stu-id="4b094-124">A button on joystick JOYSTICKID2 has been pressed.</span></span>              |
| [<span data-ttu-id="4b094-125">**\_JOY2BUTTONUP мм**</span><span class="sxs-lookup"><span data-stu-id="4b094-125">**MM\_JOY2BUTTONUP**</span></span>](mm-joy2buttonup.md)     | <span data-ttu-id="4b094-126">Была снята кнопка на джойстике JOYSTICKID2.</span><span class="sxs-lookup"><span data-stu-id="4b094-126">A button on joystick JOYSTICKID2 has been released.</span></span>             |
| [<span data-ttu-id="4b094-127">**\_JOY2MOVE мм**</span><span class="sxs-lookup"><span data-stu-id="4b094-127">**MM\_JOY2MOVE**</span></span>](mm-joy2move.md)             | <span data-ttu-id="4b094-128">Расположение джойстика JOYSTICKID2 изменено в направлении x или y</span><span class="sxs-lookup"><span data-stu-id="4b094-128">Joystick JOYSTICKID2 changed position in the x- or y-direction</span></span>  |
| [<span data-ttu-id="4b094-129">**\_JOY2ZMOVE мм**</span><span class="sxs-lookup"><span data-stu-id="4b094-129">**MM\_JOY2ZMOVE**</span></span>](mm-joy2zmove.md)           | <span data-ttu-id="4b094-130">Джойстик JOYSTICKID2 измененное расположение в z-направлении.</span><span class="sxs-lookup"><span data-stu-id="4b094-130">Joystick JOYSTICKID2 changed position in the z-direction.</span></span>       |



 

<span data-ttu-id="4b094-131">Все сообщения сообщают о несуществующих кнопках как освобожденных.</span><span class="sxs-lookup"><span data-stu-id="4b094-131">All messages report nonexistent buttons as released.</span></span>

 

 




