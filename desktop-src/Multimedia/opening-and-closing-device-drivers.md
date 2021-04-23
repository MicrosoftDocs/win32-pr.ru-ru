---
title: Открытие и закрытие драйверов устройств
description: Открытие и закрытие драйверов устройств
ms.assetid: 441bc0ec-41c9-4595-92f9-4c2304b10f16
keywords:
- Цифровой интерфейс музыкальных инструментов (MIDI), открытие устройств
- MIDI (цифровой интерфейс музыкального инструмента), открытие устройств
- Службы MIDI, открытие устройств
- Открытие устройств MIDI
- Цифровой интерфейс MIDI, закрытие устройств
- MIDI (цифровой интерфейс музыкального инструмента), закрытие устройств
- Службы MIDI, закрытие устройств
- Закрытие устройств MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53d7035455baa067b81af7da980a4ae043500c7b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103789960"
---
# <a name="opening-and-closing-device-drivers"></a><span data-ttu-id="e90ac-111">Открытие и закрытие драйверов устройств</span><span class="sxs-lookup"><span data-stu-id="e90ac-111">Opening and Closing Device Drivers</span></span>

<span data-ttu-id="e90ac-112">Прежде чем использовать устройство MIDI, необходимо закрыть устройство, как только оно будет готово.</span><span class="sxs-lookup"><span data-stu-id="e90ac-112">You must open a MIDI device before using it, and you should close the device as soon as you finish using it.</span></span> <span data-ttu-id="e90ac-113">Windows предоставляет следующие функции для открытия и закрытия различных типов устройств MIDI.</span><span class="sxs-lookup"><span data-stu-id="e90ac-113">Windows provides the following functions to open and close different types of MIDI devices.</span></span>



| <span data-ttu-id="e90ac-114">Значение</span><span class="sxs-lookup"><span data-stu-id="e90ac-114">Value</span></span>                                | <span data-ttu-id="e90ac-115">Значение</span><span class="sxs-lookup"><span data-stu-id="e90ac-115">Meaning</span></span>                                            |
|--------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="e90ac-116">**мидиинклосе**</span><span class="sxs-lookup"><span data-stu-id="e90ac-116">**midiInClose**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose)   | <span data-ttu-id="e90ac-117">Закрывает указанное устройство ввода MIDI.</span><span class="sxs-lookup"><span data-stu-id="e90ac-117">Closes a specified MIDI input device.</span></span>              |
| [<span data-ttu-id="e90ac-118">**мидиинопен**</span><span class="sxs-lookup"><span data-stu-id="e90ac-118">**midiInOpen**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen)     | <span data-ttu-id="e90ac-119">Открывает указанное устройство ввода MIDI для записи.</span><span class="sxs-lookup"><span data-stu-id="e90ac-119">Opens a specified MIDI input device for recording.</span></span> |
| [<span data-ttu-id="e90ac-120">**мидиаутклосе**</span><span class="sxs-lookup"><span data-stu-id="e90ac-120">**midiOutClose**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose) | <span data-ttu-id="e90ac-121">Закрывает указанное устройство вывода MIDI.</span><span class="sxs-lookup"><span data-stu-id="e90ac-121">Closes a specified MIDI output device.</span></span>             |
| [<span data-ttu-id="e90ac-122">**мидиаутопен**</span><span class="sxs-lookup"><span data-stu-id="e90ac-122">**midiOutOpen**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen)   | <span data-ttu-id="e90ac-123">Открывает устройство вывода MIDI для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="e90ac-123">Opens a MIDI output device for playback.</span></span>           |



 

<span data-ttu-id="e90ac-124">Каждая функция, открывающая устройство MIDI, принимает в качестве параметров идентификатор устройства, адрес расположения в памяти и некоторые параметры, уникальные для устройств MIDI.</span><span class="sxs-lookup"><span data-stu-id="e90ac-124">Each function that opens a MIDI device takes as parameters a device identifier, an address of a memory location, and some parameters unique to MIDI devices.</span></span> <span data-ttu-id="e90ac-125">Область памяти заполняется маркером устройства, который используется для определения открытого звукового устройства при вызовах других функций аудио.</span><span class="sxs-lookup"><span data-stu-id="e90ac-125">The memory location is filled with a device handle, which is used to identify the open audio device in calls to other audio functions.</span></span>

<span data-ttu-id="e90ac-126">Многие функции MIDI могут принимать либо маркер устройства, либо идентификатор устройства.</span><span class="sxs-lookup"><span data-stu-id="e90ac-126">Many MIDI functions can accept either a device handle or a device identifier.</span></span> <span data-ttu-id="e90ac-127">Хотя вы можете использовать обработку устройства везде, где бы вы ни использовали идентификатор устройства, нельзя всегда использовать идентификатор устройства при вызове обработчика для.</span><span class="sxs-lookup"><span data-stu-id="e90ac-127">Although you can use a device handle wherever you would use a device identifier, you cannot always use a device identifier when a handle is called for.</span></span>

> [!Note]  
> <span data-ttu-id="e90ac-128">Устройства MIDI не обязательно могут совместно использоваться, поэтому определенное устройство может быть недоступно, когда пользователь запросит его.</span><span class="sxs-lookup"><span data-stu-id="e90ac-128">MIDI devices are not necessarily sharable, so a particular device may not be available when a user requests it.</span></span> <span data-ttu-id="e90ac-129">В этом случае приложение должно уведомить пользователя и разрешить пользователю повторить попытку открытия устройства.</span><span class="sxs-lookup"><span data-stu-id="e90ac-129">If this happens, the application should notify the user and allow the user to try to open the device again.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="e90ac-130">См. также</span><span class="sxs-lookup"><span data-stu-id="e90ac-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e90ac-131">Службы MIDI</span><span class="sxs-lookup"><span data-stu-id="e90ac-131">MIDI Services</span></span>](midi-services.md)
</dt> </dl>

 

 