---
title: Возможности джойстика
description: Возможности джойстика
ms.assetid: 910c7f1d-e20a-4a03-b512-9a7f8cb1e559
keywords:
- входные мультимедийные данные, джойстики
- Джойстики, перемещение с двух осей
- Джойстики, перемещение по оси с тремя осями
- Джойстики, кнопки
- Джойстики, диапазоны движения
- Джойстики, частота опроса
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b317d5a0c8deb48b49224fd051ecb7ce5a0bbced
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103791190"
---
# <a name="joystick-capabilities"></a><span data-ttu-id="0b896-109">Возможности джойстика</span><span class="sxs-lookup"><span data-stu-id="0b896-109">Joystick Capabilities</span></span>

<span data-ttu-id="0b896-110">Джойстики могут поддерживать перемещение с двух или трех осей, а также до четырех кнопок.</span><span class="sxs-lookup"><span data-stu-id="0b896-110">Joysticks can support two- or three-axis movement and up to four buttons.</span></span> <span data-ttu-id="0b896-111">Джойстики также поддерживают различные *диапазоны движения* и *частот опроса*.</span><span class="sxs-lookup"><span data-stu-id="0b896-111">Joysticks also support different *ranges of motion* and *polling frequencies*.</span></span> <span data-ttu-id="0b896-112">Диапазон движения — это расстояние, которое может перемещаться с помощью джойстика, начиная от его положения в его расположении.</span><span class="sxs-lookup"><span data-stu-id="0b896-112">The range of motion is the distance a joystick handle can move from its resting position to the position farthest from its resting position.</span></span> <span data-ttu-id="0b896-113">Периодичность опроса — это интервал времени между двумя запросами джойстика.</span><span class="sxs-lookup"><span data-stu-id="0b896-113">The polling frequency is the time interval between joystick queries.</span></span>

<span data-ttu-id="0b896-114">Драйверы джойстика могут поддерживать один или два джойстика.</span><span class="sxs-lookup"><span data-stu-id="0b896-114">Joystick drivers can support either one or two joysticks.</span></span> <span data-ttu-id="0b896-115">Число джойстиков, поддерживаемых драйвером джойстика, можно определить с помощью функции [**жойжетнумдевс**](/windows/win32/api/joystickapi/nf-joystickapi-joygetnumdevs) .</span><span class="sxs-lookup"><span data-stu-id="0b896-115">You can determine the number of joysticks supported by a joystick driver by using the [**joyGetNumDevs**](/windows/win32/api/joystickapi/nf-joystickapi-joygetnumdevs) function.</span></span> <span data-ttu-id="0b896-116">Эта функция возвращает целое число без знака, которое содержит число поддерживаемых джойстиков или нуль, если джойстик не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="0b896-116">This function returns an unsigned integer that contains the number of supported joysticks or zero if there is no joystick support.</span></span> <span data-ttu-id="0b896-117">Возвращаемое значение не указывает количество джойстиков, подключенных к системе.</span><span class="sxs-lookup"><span data-stu-id="0b896-117">The return value does not indicate the number of joysticks attached to the system.</span></span>

<span data-ttu-id="0b896-118">Определить, подключен ли джойстик к системе, можно с помощью функции [**жойжетпос**](/windows/win32/api/joystickapi/nf-joystickapi-joygetpos) .</span><span class="sxs-lookup"><span data-stu-id="0b896-118">You can determine if a joystick is attached to the system by using the [**joyGetPos**](/windows/win32/api/joystickapi/nf-joystickapi-joygetpos) function.</span></span> <span data-ttu-id="0b896-119">Эта функция возвращает ЖОЙЕРР \_ Error, если указанное устройство подключено.</span><span class="sxs-lookup"><span data-stu-id="0b896-119">This function returns JOYERR\_NOERROR if the specified device is attached.</span></span> <span data-ttu-id="0b896-120">В противном случае он возвращает ЖОЙЕРР \_ , не подключенный к сети.</span><span class="sxs-lookup"><span data-stu-id="0b896-120">Otherwise , it returns JOYERR\_UNPLUGGED.</span></span>

<span data-ttu-id="0b896-121">Каждый джойстик имеет несколько возможностей, доступных для приложения.</span><span class="sxs-lookup"><span data-stu-id="0b896-121">Each joystick has several capabilities that are available to your application.</span></span> <span data-ttu-id="0b896-122">Возможности джойстика можно получить с помощью функции [**жойжетдевкапс**](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps) .</span><span class="sxs-lookup"><span data-stu-id="0b896-122">You can retrieve the capabilities of a joystick by using the [**joyGetDevCaps**](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps) function.</span></span> <span data-ttu-id="0b896-123">Эта функция заполняет структуру [**жойкапс**](/windows/win32/api/joystickapi/ns-joystickapi-joycaps) с помощью таких возможностей джойстика, как минимальное и максимальное значения для своей системы координат, число кнопок на джойстике и минимальную и максимальную частоту опроса.</span><span class="sxs-lookup"><span data-stu-id="0b896-123">This function fills a [**JOYCAPS**](/windows/win32/api/joystickapi/ns-joystickapi-joycaps) structure with joystick capabilities such as the minimum and maximum values for its coordinate system, the number of buttons on the joystick, and the minimum and maximum polling frequencies.</span></span>

 

 