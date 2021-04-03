---
title: Уведомления Time-Based
description: Уведомления Time-Based
ms.assetid: cf7bc0d4-f3bd-4416-b85f-0ff51a0efbbc
keywords:
- Джойстики, уведомления
- Джойстики, сообщения
- Джойстики, уведомления на основе времени
- уведомления на основе времени джойстика
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15dff2a6140bd993157f20e92488afce1b646e20
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103987367"
---
# <a name="time-based-notifications"></a><span data-ttu-id="170a4-107">Уведомления Time-Based</span><span class="sxs-lookup"><span data-stu-id="170a4-107">Time-Based Notifications</span></span>

<span data-ttu-id="170a4-108">Вы можете уведомить операционную систему, чтобы отправлять сообщения джойстика в приложение через регулярные интервалы времени, установив для параметра *Фчанжед* [**жойсеткаптуре**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) **значение false** и указав длину интервала между последовательными сообщениями.</span><span class="sxs-lookup"><span data-stu-id="170a4-108">You can notify the operating system to send joystick messages to an application at regular time intervals by setting the *fChanged* parameter of [**joySetCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) to **FALSE** and by specifying the interval length between successive messages.</span></span> <span data-ttu-id="170a4-109">Для этого назначьте параметру *упериод* значение между минимальной и максимальной частотой опроса для джойстика.</span><span class="sxs-lookup"><span data-stu-id="170a4-109">To do this, assign the *uPeriod* parameter a value between the minimum and maximum polling frequencies for the joystick.</span></span> <span data-ttu-id="170a4-110">Этот диапазон можно определить с помощью функции [**жойжетдевкапс**](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps) , которая заполняет элементы **впериодмин** и **впериодмакс** в структуре [**жойкапс**](/windows/win32/api/joystickapi/ns-joystickapi-joycaps) .</span><span class="sxs-lookup"><span data-stu-id="170a4-110">You can determine this range by using the [**joyGetDevCaps**](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps) function, which fills the **wPeriodMin** and **wPeriodMax** members in the [**JOYCAPS**](/windows/win32/api/joystickapi/ns-joystickapi-joycaps) structure.</span></span> <span data-ttu-id="170a4-111">Если значение *упериод* находится за пределами диапазона допустимых частот опроса для джойстика, драйвер джойстика использует минимальную или максимальную частоту опроса, в зависимости от значения *упериод* .</span><span class="sxs-lookup"><span data-stu-id="170a4-111">If the *uPeriod* value is outside the range of valid polling frequencies for the joystick, the joystick driver uses the minimum or maximum polling frequency, whichever is closer to the *uPeriod* value.</span></span>

> [!Note]  
> <span data-ttu-id="170a4-112">Windows настраивает событие таймера при каждом вызове **жойсеткаптуре**.</span><span class="sxs-lookup"><span data-stu-id="170a4-112">Windows sets up a timer event with each call to **joySetCapture**.</span></span>

 

 

 