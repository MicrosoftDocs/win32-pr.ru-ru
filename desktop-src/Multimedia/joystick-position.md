---
title: Расположение джойстика
description: Расположение джойстика
ms.assetid: db0d1125-e39f-445b-bd65-373633cad578
keywords:
- Джойстики, расположение
- Джойстики, кнопки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bcdc187cfba244bb2b8c28c37e3677593f99870
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104260776"
---
# <a name="joystick-position"></a><span data-ttu-id="66d09-105">Расположение джойстика</span><span class="sxs-lookup"><span data-stu-id="66d09-105">Joystick Position</span></span>

<span data-ttu-id="66d09-106">Вы можете запросить в джойстике сведения о положении и кнопке с помощью функции [**жойжетпос**](/windows/win32/api/joystickapi/nf-joystickapi-joygetpos) .</span><span class="sxs-lookup"><span data-stu-id="66d09-106">You can query a joystick for position and button information by using the [**joyGetPos**](/windows/win32/api/joystickapi/nf-joystickapi-joygetpos) function.</span></span> <span data-ttu-id="66d09-107">Например, приложение может отправлять запросы к джойстику для значений расположения базовых показателей.</span><span class="sxs-lookup"><span data-stu-id="66d09-107">For example, an application can query the joystick for baseline position values.</span></span> <span data-ttu-id="66d09-108">Страница свойств панели управления джойстика использует этот метод при калибровке джойстика.</span><span class="sxs-lookup"><span data-stu-id="66d09-108">The Joystick Control Panel property sheet uses this technique when calibrating the joystick.</span></span>

<span data-ttu-id="66d09-109">Вы также можете запросить джойстик или другое устройство с расширенными возможностями с помощью функции [**жойжетпосекс**](/windows/win32/api/joystickapi/nf-joystickapi-joygetposex) .</span><span class="sxs-lookup"><span data-stu-id="66d09-109">You can also query a joystick or other device that has extended capabilities by using the [**joyGetPosEx**](/windows/win32/api/joystickapi/nf-joystickapi-joygetposex) function.</span></span>

 

 