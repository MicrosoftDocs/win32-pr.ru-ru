---
description: Роли устройств
ms.assetid: aa787004-0d3e-448b-80dd-92055f841aee
title: Роли устройств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b7182e3af6bf76af500588546a1b7c0db9eea97
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141629"
---
# <a name="device-roles"></a><span data-ttu-id="74ac4-103">Роли устройств</span><span class="sxs-lookup"><span data-stu-id="74ac4-103">Device Roles</span></span>

<span data-ttu-id="74ac4-104">Если система содержит два или более конечных устройства для отрисовки звука, то одно устройство лучше подходит для воспроизведения одного типа звукового содержимого, а другое устройство может быть лучшим для воспроизведения другого типа содержимого.</span><span class="sxs-lookup"><span data-stu-id="74ac4-104">If a system contains two or more audio-rendering endpoint devices, then one device might be best for playing one type of audio content, and another device might be best for playing another type of content.</span></span> <span data-ttu-id="74ac4-105">Например, если в системе есть два устройства отрисовки, пользователь может воспроизводить музыку на одном устройстве и воспроизводить звуки системных уведомлений.</span><span class="sxs-lookup"><span data-stu-id="74ac4-105">For example, if a system has two rendering devices, the user might choose to play music on one device and to play system notification sounds on the other.</span></span>

<span data-ttu-id="74ac4-106">Аналогично, если система содержит два или более конечных устройства записи звука, то одно устройство может быть лучшим для захвата одного типа звукового содержимого, а другое устройство может быть лучшим для записи другого типа содержимого.</span><span class="sxs-lookup"><span data-stu-id="74ac4-106">Similarly, if a system contains two or more audio-capture endpoint devices, then one device might be best for capturing one type of audio content, and another device might be best for capturing another type of content.</span></span> <span data-ttu-id="74ac4-107">Например, если в системе есть два устройства записи, пользователь может записать динамическую музыку на одном устройстве и использовать другое устройство для работы с голосовыми командами.</span><span class="sxs-lookup"><span data-stu-id="74ac4-107">For example, if a system has two capture devices, the user might choose to record live music on one device and to use the other device for voice commands.</span></span>

<span data-ttu-id="74ac4-108">Устройства могут иметь три роли: консоль, взаимодействие и мультимедиа. в следующей таблице описаны роли устройств, определяемые тремя константами — Еконсоле, Екоммуникатионс и Емултимедиа — в перечислении [**ероле**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) .</span><span class="sxs-lookup"><span data-stu-id="74ac4-108">Devices can have three roles: Console, Communications, and Multimedia.The following table describes the device roles identified by the three constants—eConsole, eCommunications, and eMultimedia—in the [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) enumeration.</span></span>



| <span data-ttu-id="74ac4-109">Константа Ероле</span><span class="sxs-lookup"><span data-stu-id="74ac4-109">ERole constant</span></span>  | <span data-ttu-id="74ac4-110">Роль устройства</span><span class="sxs-lookup"><span data-stu-id="74ac4-110">Device role</span></span>                              | <span data-ttu-id="74ac4-111">Примеры подготовки к просмотру</span><span class="sxs-lookup"><span data-stu-id="74ac4-111">Rendering examples</span></span>             | <span data-ttu-id="74ac4-112">Примеры записи</span><span class="sxs-lookup"><span data-stu-id="74ac4-112">Capture examples</span></span>                   |
|-----------------|------------------------------------------|--------------------------------|------------------------------------|
| <span data-ttu-id="74ac4-113">еконсоле</span><span class="sxs-lookup"><span data-stu-id="74ac4-113">eConsole</span></span>        | <span data-ttu-id="74ac4-114">Взаимодействие с компьютером</span><span class="sxs-lookup"><span data-stu-id="74ac4-114">Interaction with the computer</span></span>            | <span data-ttu-id="74ac4-115">Игры и системные уведомления</span><span class="sxs-lookup"><span data-stu-id="74ac4-115">Games and system notifications</span></span> | <span data-ttu-id="74ac4-116">Команды Voice</span><span class="sxs-lookup"><span data-stu-id="74ac4-116">Voice commands</span></span>                     |
| <span data-ttu-id="74ac4-117">екоммуникатионс</span><span class="sxs-lookup"><span data-stu-id="74ac4-117">eCommunications</span></span> | <span data-ttu-id="74ac4-118">Обмен голосовыми сообщениями с другим лицом</span><span class="sxs-lookup"><span data-stu-id="74ac4-118">Voice communications with another person</span></span> | <span data-ttu-id="74ac4-119">Чат и VoIP</span><span class="sxs-lookup"><span data-stu-id="74ac4-119">Chat and VoIP</span></span>                  | <span data-ttu-id="74ac4-120">Чат и VoIP</span><span class="sxs-lookup"><span data-stu-id="74ac4-120">Chat and VoIP</span></span>                      |
| <span data-ttu-id="74ac4-121">емултимедиа</span><span class="sxs-lookup"><span data-stu-id="74ac4-121">eMultimedia</span></span>     | <span data-ttu-id="74ac4-122">Воспроизведение или запись звукового содержимого</span><span class="sxs-lookup"><span data-stu-id="74ac4-122">Playing or recording audio content</span></span>       | <span data-ttu-id="74ac4-123">Музыка и фильмы</span><span class="sxs-lookup"><span data-stu-id="74ac4-123">Music and movies</span></span>               | <span data-ttu-id="74ac4-124">Речевое сопровождение и запись музыки в реальном времени</span><span class="sxs-lookup"><span data-stu-id="74ac4-124">Narration and live music recording</span></span> |



 

<span data-ttu-id="74ac4-125">Конкретному устройству отрисовки или записи может быть присвоено значение None, одна, часть или все роли в предыдущей таблице.</span><span class="sxs-lookup"><span data-stu-id="74ac4-125">A particular rendering or capture device might be assigned none, one, some, or all of the roles in the preceding table.</span></span> <span data-ttu-id="74ac4-126">В любое время каждая роль в таблице назначается одному (и только одному) устройству отрисовки и только одному (и только одному) устройству записи.</span><span class="sxs-lookup"><span data-stu-id="74ac4-126">At any time, each role in the table is assigned to one (and only one) rendering device and to one (and only one) capture device.</span></span> <span data-ttu-id="74ac4-127">Это значит, что назначение ролей для отрисовки устройств не зависит от назначения ролей для записи устройств.</span><span class="sxs-lookup"><span data-stu-id="74ac4-127">That is, the assignment of roles to rendering devices is independent of the assignment of roles to capture devices.</span></span>

<span data-ttu-id="74ac4-128">Приложение может воспроизводить все свои выходные потоки через одно устройство отрисовки конечной точки, а также записывать все входные потоки из одного устройства записи в конечную точку.</span><span class="sxs-lookup"><span data-stu-id="74ac4-128">An application might choose to play all of its output streams through a single rendering endpoint device, and to record all of its input streams from a single capture endpoint device.</span></span> <span data-ttu-id="74ac4-129">Кроме того, приложение может выбрать воспроизведение некоторых выходных потоков через одно устройство отрисовки и воспроизвести другие выходные потоки через другое устройство визуализации.</span><span class="sxs-lookup"><span data-stu-id="74ac4-129">Alternatively, an application might choose to play some of its output streams through one rendering device and to play other output streams through another rendering device.</span></span> <span data-ttu-id="74ac4-130">Аналогичным образом, он может записывать некоторые входные потоки через одно устройство записи и записывать другие входные потоки через другое устройство записи.</span><span class="sxs-lookup"><span data-stu-id="74ac4-130">Similarly, it might choose to record some of its input streams through one capture device and to record other input streams through another capture device.</span></span> <span data-ttu-id="74ac4-131">Во всех случаях приложение может назначить каждый поток устройству, роль которого наиболее подходит для этого потока.</span><span class="sxs-lookup"><span data-stu-id="74ac4-131">In all cases, the application can assign each stream to the device whose role is most appropriate for that stream.</span></span>

<span data-ttu-id="74ac4-132">Например, приложение VoIP может назначить выходной поток, содержащий уведомление о сопоставлении, на устройство конечной точки отрисовки с ролью Еконсоле.</span><span class="sxs-lookup"><span data-stu-id="74ac4-132">For example, a VoIP application might assign the output stream that contains the ring-in notification to the rendering endpoint device with the eConsole role.</span></span>

## <a name="related-topics"></a><span data-ttu-id="74ac4-133">См. также</span><span class="sxs-lookup"><span data-stu-id="74ac4-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74ac4-134">Устройства конечных точек звука</span><span class="sxs-lookup"><span data-stu-id="74ac4-134">Audio Endpoint Devices</span></span>](audio-endpoint-devices.md)
</dt> <dt>

[<span data-ttu-id="74ac4-135">Работа с ролями устройств</span><span class="sxs-lookup"><span data-stu-id="74ac4-135">Working with Device Roles</span></span>](device-roles-in-windows-vista.md)
</dt> <dt>

[<span data-ttu-id="74ac4-136">Взаимодействие с устаревшими API аудио</span><span class="sxs-lookup"><span data-stu-id="74ac4-136">Interoperability with Legacy Audio APIs</span></span>](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 



