---
title: Открытие и закрытие микшерных устройств
description: Открытие и закрытие микшерных устройств
ms.assetid: b1943308-3778-485e-80f3-6d80cb583e00
keywords:
- мультимедийные аудио, открытие микшерных устройств
- звук, открытие микшерных устройств
- аудио миксерс, открытие
- миксерс, открытие
- мультимедиа аудио, закрытие микшерных устройств
- звук, закрытие микшерных устройств
- аудио миксерс, закрытие
- миксерс, закрытие
- Открытие микшерных устройств
- Закрытие микшерных устройств
- идентификаторы устройств и дескрипторы устройств
- аудио миксерс, идентификаторы устройств и дескрипторы устройств
- миксерс, идентификаторы устройств и дескрипторы устройств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea2be7fcc0563508aabfd957109d62c7dbfe1c1a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104069852"
---
# <a name="opening-and-closing-mixer-devices"></a><span data-ttu-id="c9c7c-116">Открытие и закрытие микшерных устройств</span><span class="sxs-lookup"><span data-stu-id="c9c7c-116">Opening and Closing Mixer Devices</span></span>

<span data-ttu-id="c9c7c-117">Если вы хотите использовать микшерное устройство, можно либо просто начать его использование, либо явно открыть устройство перед его использованием.</span><span class="sxs-lookup"><span data-stu-id="c9c7c-117">When you want to use a mixer device, you can either simply begin using it or you can explicitly open the device before using it.</span></span> <span data-ttu-id="c9c7c-118">Явное открытие микшера предоставляет два основных преимущества:</span><span class="sxs-lookup"><span data-stu-id="c9c7c-118">Explicitly opening a mixer device offers two main benefits:</span></span>

-   <span data-ttu-id="c9c7c-119">Он гарантирует непрерывное существование этого устройства микшера.</span><span class="sxs-lookup"><span data-stu-id="c9c7c-119">It guarantees the continued existence of that mixer device.</span></span>
-   <span data-ttu-id="c9c7c-120">Она позволяет получить уведомления о звуковой линии и управлении изменениями.</span><span class="sxs-lookup"><span data-stu-id="c9c7c-120">It lets you receive notification of audio line and control changes.</span></span>

<span data-ttu-id="c9c7c-121">Функцию [**миксеропен**](/windows/win32/api/mmeapi/nf-mmeapi-mixeropen) можно использовать для явного открытия микшера устройства.</span><span class="sxs-lookup"><span data-stu-id="c9c7c-121">You can use the [**mixerOpen**](/windows/win32/api/mmeapi/nf-mmeapi-mixeropen) function to explicitly open a mixer device.</span></span> <span data-ttu-id="c9c7c-122">Эта функция принимает в качестве параметров идентификатор устройства, указатель на расположение в памяти и другие значения, уникальные для каждого типа устройства.</span><span class="sxs-lookup"><span data-stu-id="c9c7c-122">This function takes as parameters a device identifier, a pointer to a memory location, and other values unique to each type of device.</span></span> <span data-ttu-id="c9c7c-123">Область памяти заполняется с помощью маркера устройства.</span><span class="sxs-lookup"><span data-stu-id="c9c7c-123">The memory location is filled with a device handle.</span></span> <span data-ttu-id="c9c7c-124">Используйте этот маркер устройства для обнаружения устройства открытия микшера при вызове других функций микшера звука.</span><span class="sxs-lookup"><span data-stu-id="c9c7c-124">Use this device handle to identify the open mixer device when calling other audio mixer functions.</span></span> <span data-ttu-id="c9c7c-125">Пока существует маркер устройства микшера, устройство остается в системе.</span><span class="sxs-lookup"><span data-stu-id="c9c7c-125">As long as a handle of a mixer device exists, the device continues to exist in the system.</span></span> <span data-ttu-id="c9c7c-126">Если на устройстве микшера происходит изменение конфигурации, которое не было явно открыто, приложение может внезапно получить доступ к нему.</span><span class="sxs-lookup"><span data-stu-id="c9c7c-126">If a configuration change occurs to the mixer device and it hasn't been explicitly opened, your application might suddenly be unable to access it.</span></span>

> [!Note]  
> <span data-ttu-id="c9c7c-127">Разница между идентификаторами устройств и дескрипторами устройств важна.</span><span class="sxs-lookup"><span data-stu-id="c9c7c-127">The difference between device identifiers and device handles is important.</span></span> <span data-ttu-id="c9c7c-128">Дескрипторы устройств возвращаются при открытии драйвера устройства с помощью **миксеропен**.</span><span class="sxs-lookup"><span data-stu-id="c9c7c-128">Device handles are returned when you open a device driver by using **mixerOpen**.</span></span> <span data-ttu-id="c9c7c-129">Идентификаторы устройств определяются неявно с учетом количества устройств, имеющихся в системе; Это число получается с помощью функции [**миксержетнумдевс**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetnumdevs) .</span><span class="sxs-lookup"><span data-stu-id="c9c7c-129">Device identifiers are determined implicitly from the number of devices present in a system; this number is obtained by using the [**mixerGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetnumdevs) function.</span></span>

 

<span data-ttu-id="c9c7c-130">Вы можете использовать функцию [**миксерклосе**](/windows/win32/api/mmeapi/nf-mmeapi-mixerclose) для закрытия микшера устройства.</span><span class="sxs-lookup"><span data-stu-id="c9c7c-130">You can use the [**mixerClose**](/windows/win32/api/mmeapi/nf-mmeapi-mixerclose) function to close a mixer device.</span></span> <span data-ttu-id="c9c7c-131">После завершения использования устройства следует закрыть его.</span><span class="sxs-lookup"><span data-stu-id="c9c7c-131">You should close the device after you finish using it.</span></span>

 

 