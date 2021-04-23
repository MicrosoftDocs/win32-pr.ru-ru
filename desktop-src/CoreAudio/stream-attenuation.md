---
description: Интерфейс Дуккинг по умолчанию
ms.assetid: 2ad9482f-1888-4f19-bc41-9d47a8e0ed15
title: Интерфейс Дуккинг по умолчанию
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d81aa22254ab33ee7396fd4a22d83cc7f5a58041
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807547"
---
# <a name="default-ducking-experience"></a><span data-ttu-id="dfe02-103">Интерфейс Дуккинг по умолчанию</span><span class="sxs-lookup"><span data-stu-id="dfe02-103">Default Ducking Experience</span></span>

<span data-ttu-id="dfe02-104">Рассмотрим ситуацию, когда пользователь получает телефонный звонок во время прослушивания музыки на компьютере.</span><span class="sxs-lookup"><span data-stu-id="dfe02-104">Consider a scenario where a user receives a phone call while listening to music on the computer.</span></span> <span data-ttu-id="dfe02-105">Во время звонка пользователь хочет уменьшить уровень громкости музыки при посещении телефонного звонка и возобновить исходный том после завершения звонка.</span><span class="sxs-lookup"><span data-stu-id="dfe02-105">During the phone call, the user wants to reduce the volume level of the music while attending to the phone call, and resume the original volume after the phone call has ended.</span></span> <span data-ttu-id="dfe02-106">В зависимости от параметров, заданных пользователем на панели управления « **звуки** », операционная система автоматически предоставляет эту функцию через *дуккинг* или *ослабление потоковой* передачи, сокращая интенсивность звукового потока.</span><span class="sxs-lookup"><span data-stu-id="dfe02-106">Depending on the options specified by the user in the **Sounds** control panel, the operating system automatically provides this functionality through *ducking* or *stream attenuation*—reduction in the intensity of an audio stream.</span></span>

<span data-ttu-id="dfe02-107">Режим ослабления по умолчанию зависит от предпочтений пользователя, как указано в параметре **звук** на панели управления.</span><span class="sxs-lookup"><span data-stu-id="dfe02-107">The default attenuation experience depends on the user's preference, as specified in the control panel's **Sound** option.</span></span> <span data-ttu-id="dfe02-108">На вкладке **связи** пользователь может выбрать уровень затухания (значение по умолчанию — 80%), отключить все потоки, не связанные с обменом данными, или отключить интерфейс затухания потока по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="dfe02-108">On the **Communications** tab, the user can choose an attenuation level (default value is 80%), mute all non-communication streams, or disable the default stream attenuation experience.</span></span> <span data-ttu-id="dfe02-109">Система позволяет открывать новые потоки без связи (за исключением новых системных звуков) во время сеанса связи, но новые потоки не раскрываются автоматически.</span><span class="sxs-lookup"><span data-stu-id="dfe02-109">The system allows new non-communication streams (except for new system sounds) to be opened during the communication session but the new streams are not automatically attenuated.</span></span> <span data-ttu-id="dfe02-110">Когда все потоки связи закрыты, система завершает сеанс связи и восстанавливает объем потоков, которые были ослаблены во время сеанса связи.</span><span class="sxs-lookup"><span data-stu-id="dfe02-110">When all of the communication streams are closed, the system ends the communication session and restores the volume of the streams that were attenuated during the communication session.</span></span>

<span data-ttu-id="dfe02-111">Чтобы визуально определить ослабление потока, система изменяет параметры микшера тома в зависимости от предпочтений пользователя.</span><span class="sxs-lookup"><span data-stu-id="dfe02-111">To indicate stream attenuation visually, the system changes the volume mixer settings depending on the user's preference.</span></span> <span data-ttu-id="dfe02-112">Например, если пользователь указывает уровень ослабления, микшер тома понижает ползунок, отображает новый ослабленный том и отображает исходный уровень громкости.</span><span class="sxs-lookup"><span data-stu-id="dfe02-112">For example, if the user specifies an attenuation level, the volume mixer lowers the slider, displays the new attenuated volume, and displays the original volume level.</span></span> <span data-ttu-id="dfe02-113">Этот процесс показан на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="dfe02-113">The following image illustrates this process.</span></span>

![схема поведения по ослаблению потока по умолчанию, предусмотренного в Windows 7](images/stream-aatenuation.jpg)

<span data-ttu-id="dfe02-115">Приложение может переопределить затухание в потоке и реализовать пользовательский интерфейс дуккинг, если он знает, когда начинается и заканчивается сеанс связи.</span><span class="sxs-lookup"><span data-stu-id="dfe02-115">An application can override stream attenuation and implement a custom ducking experience if it knows when the communication session starts and ends.</span></span> <span data-ttu-id="dfe02-116">Дополнительные сведения см. [в разделе предоставление настраиваемого поведения дуккинг](providing-a-custom-ducking-experience.md).</span><span class="sxs-lookup"><span data-stu-id="dfe02-116">For more information, see [Providing a Custom Ducking Behavior](providing-a-custom-ducking-experience.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="dfe02-117">См. также</span><span class="sxs-lookup"><span data-stu-id="dfe02-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dfe02-118">Использование коммуникационного устройства</span><span class="sxs-lookup"><span data-stu-id="dfe02-118">Using a Communication Device</span></span>](using-the-communication-device.md)
</dt> <dt>

[<span data-ttu-id="dfe02-119">Отключение интерфейса Дуккинг по умолчанию</span><span class="sxs-lookup"><span data-stu-id="dfe02-119">Disabling the Default Ducking Experience</span></span>](disabling-the-ducking-experience.md)
</dt> <dt>

[<span data-ttu-id="dfe02-120">Предоставление пользовательского поведения Дуккинг</span><span class="sxs-lookup"><span data-stu-id="dfe02-120">Providing a Custom Ducking Behavior</span></span>](providing-a-custom-ducking-experience.md)
</dt> <dt>

[<span data-ttu-id="dfe02-121">Рекомендации по реализации для уведомлений Дуккинг</span><span class="sxs-lookup"><span data-stu-id="dfe02-121">Implementation Considerations for Ducking Notifications</span></span>](handling-audio-ducking-events-from-communication-devices.md)
</dt> <dt>

[<span data-ttu-id="dfe02-122">Получение событий Дуккинг</span><span class="sxs-lookup"><span data-stu-id="dfe02-122">Getting Ducking Events</span></span>](getting-ducking-events-from-a-communication-device.md)
</dt> </dl>

 

 



