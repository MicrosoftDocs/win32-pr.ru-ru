---
title: Запрос устройств MIDI
description: Запрос устройств MIDI
ms.assetid: 0c9882a7-b5cb-41d1-a52e-003112225035
keywords:
- Цифровой интерфейс музыкальных инструментов (MIDI), запросы устройств
- MIDI (цифровой интерфейс музыкального инструмента), запросы устройств
- Службы MIDI, запросы устройств
- запрос устройств MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 066648d6e9ce89e03b26940cb27f3b62b6a03c07
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412828"
---
# <a name="querying-midi-devices"></a><span data-ttu-id="a76fe-107">Запрос устройств MIDI</span><span class="sxs-lookup"><span data-stu-id="a76fe-107">Querying MIDI Devices</span></span>

<span data-ttu-id="a76fe-108">Перед воспроизведением или записью данных MIDI необходимо определить возможности оборудования MIDI, присутствующего в системе.</span><span class="sxs-lookup"><span data-stu-id="a76fe-108">Before playing or recording MIDI data, you must determine the capabilities of the MIDI hardware present in the system.</span></span> <span data-ttu-id="a76fe-109">Возможность MIDI может изменяться от одного компьютера мультимедиа к другому; приложения не должны делать предположения об оборудовании, присутствующем в данной системе.</span><span class="sxs-lookup"><span data-stu-id="a76fe-109">MIDI capability can vary from one multimedia computer to the next; applications should not make assumptions about the hardware present in a given system.</span></span>

<span data-ttu-id="a76fe-110">Windows предоставляет следующие функции для определения того, сколько устройств MIDI доступно для ввода или вывода в заданной системе.</span><span class="sxs-lookup"><span data-stu-id="a76fe-110">Windows provides the following functions to determine how many MIDI devices are available for input or output in a given system.</span></span>



| <span data-ttu-id="a76fe-111">Значение</span><span class="sxs-lookup"><span data-stu-id="a76fe-111">Value</span></span>                                          | <span data-ttu-id="a76fe-112">Значение</span><span class="sxs-lookup"><span data-stu-id="a76fe-112">Meaning</span></span>                                                            |
|------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="a76fe-113">**мидиинжетнумдевс**</span><span class="sxs-lookup"><span data-stu-id="a76fe-113">**midiInGetNumDevs**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiingetnumdevs)   | <span data-ttu-id="a76fe-114">Возвращает число устройств ввода MIDI, имеющихся в системе.</span><span class="sxs-lookup"><span data-stu-id="a76fe-114">Retrieves the number of MIDI input devices present in the system.</span></span>  |
| [<span data-ttu-id="a76fe-115">**мидиаутжетнумдевс**</span><span class="sxs-lookup"><span data-stu-id="a76fe-115">**midiOutGetNumDevs**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetnumdevs) | <span data-ttu-id="a76fe-116">Возвращает число устройств вывода MIDI, имеющихся в системе.</span><span class="sxs-lookup"><span data-stu-id="a76fe-116">Retrieves the number of MIDI output devices present in the system.</span></span> |



 

<span data-ttu-id="a76fe-117">Как и другие звуковые устройства, устройства MIDI идентифицируются по идентификатору устройства, который определяется неявно на основе числа устройств, имеющихся в данной системе.</span><span class="sxs-lookup"><span data-stu-id="a76fe-117">Like other audio devices, MIDI devices are identified by a device identifier, which is determined implicitly from the number of devices present in a given system.</span></span> <span data-ttu-id="a76fe-118">Идентификаторы устройств находятся в диапазоне от нуля до числа имеющихся устройств, минус единицу.</span><span class="sxs-lookup"><span data-stu-id="a76fe-118">Device identifiers range from zero to the number of devices present, minus one.</span></span> <span data-ttu-id="a76fe-119">Например, если в системе есть два выходных устройства MIDI, допустимые идентификаторы устройств: 0 и 1.</span><span class="sxs-lookup"><span data-stu-id="a76fe-119">For example, if there are two MIDI output devices in a system, valid device identifiers are 0 and 1.</span></span>

<span data-ttu-id="a76fe-120">После определения количества входных и выходных устройств MIDI в системе можно запросить возможности каждого устройства.</span><span class="sxs-lookup"><span data-stu-id="a76fe-120">After you determine how many MIDI input or output devices are present in a system, you can inquire about the capabilities of each device.</span></span> <span data-ttu-id="a76fe-121">Windows предоставляет следующие функции для определения возможностей звуковых устройств.</span><span class="sxs-lookup"><span data-stu-id="a76fe-121">Windows provides the following functions to determine the capabilities of audio devices.</span></span>



| <span data-ttu-id="a76fe-122">Значение</span><span class="sxs-lookup"><span data-stu-id="a76fe-122">Value</span></span>                                          | <span data-ttu-id="a76fe-123">Значение</span><span class="sxs-lookup"><span data-stu-id="a76fe-123">Meaning</span></span>                                                                                                                                   |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a76fe-124">**мидиинжетдевкапс**</span><span class="sxs-lookup"><span data-stu-id="a76fe-124">**midiInGetDevCaps**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiingetdevcaps)   | <span data-ttu-id="a76fe-125">Получает возможности данного устройства ввода MIDI и помещает эти сведения в структуру [**мидиинкапс**](/windows/win32/api/mmeapi/ns-mmeapi-midiincaps) .</span><span class="sxs-lookup"><span data-stu-id="a76fe-125">Retrieves the capabilities of a given MIDI input device and places this information in the [**MIDIINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-midiincaps) structure.</span></span>    |
| [<span data-ttu-id="a76fe-126">**мидиаутжетдевкапс**</span><span class="sxs-lookup"><span data-stu-id="a76fe-126">**midiOutGetDevCaps**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetdevcaps) | <span data-ttu-id="a76fe-127">Получает возможности заданного выходного устройства MIDI и помещает эти сведения в структуру [**мидиауткапс**](/windows/win32/api/mmeapi/ns-mmeapi-midioutcaps) .</span><span class="sxs-lookup"><span data-stu-id="a76fe-127">Retrieves the capabilities of a given MIDI output device and places this information in the [**MIDIOUTCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-midioutcaps) structure.</span></span> |



 

<span data-ttu-id="a76fe-128">Каждая из этих функций имеет параметр, указывающий адрес структуры, которую функция заполняет данными о возможностях указанного устройства.</span><span class="sxs-lookup"><span data-stu-id="a76fe-128">Each of these functions has a parameter specifying the address of a structure that the function fills with information about the capabilities of a specified device.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a76fe-129">См. также</span><span class="sxs-lookup"><span data-stu-id="a76fe-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a76fe-130">Службы MIDI</span><span class="sxs-lookup"><span data-stu-id="a76fe-130">MIDI Services</span></span>](midi-services.md)
</dt> </dl>

 

 