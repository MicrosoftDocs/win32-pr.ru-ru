---
description: Модель, описывающая громкость ориентированного звука.
ms.assetid: 15252358-d932-22f4-f13a-8e4b8487dd86
title: Звук конес
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 215659ab08c33066abfade2faf206f6360a51051
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703032"
---
# <a name="sound-cones"></a><span data-ttu-id="0b0a8-103">Звук конес</span><span class="sxs-lookup"><span data-stu-id="0b0a8-103">Sound Cones</span></span>

<span data-ttu-id="0b0a8-104">Модель, описывающая громкость ориентированного звука.</span><span class="sxs-lookup"><span data-stu-id="0b0a8-104">A model that describes the loudness of oriented sound.</span></span>

<span data-ttu-id="0b0a8-105">Звук без ориентации имеет тот же амплитуд на заданном расстоянии во всех направлениях.</span><span class="sxs-lookup"><span data-stu-id="0b0a8-105">A sound with no orientation has the same amplitude at a given distance in all directions.</span></span> <span data-ttu-id="0b0a8-106">Звук с ориентацией имеет громкое направление в направлении ориентации.</span><span class="sxs-lookup"><span data-stu-id="0b0a8-106">A sound with an orientation is loudest in the direction of orientation.</span></span> <span data-ttu-id="0b0a8-107">Модель, описывающая громкость ориентированного звука, называется звуковой конусом.</span><span class="sxs-lookup"><span data-stu-id="0b0a8-107">The model that describes the loudness of the oriented sound is called a sound cone.</span></span> <span data-ttu-id="0b0a8-108">Звуковые конес состоят из внутренней (или внутренней) конуса, а также внешнего (или наружного) конуса.</span><span class="sxs-lookup"><span data-stu-id="0b0a8-108">Sound cones are made up of an inside (or inner) cone and an outside (or outer) cone.</span></span> <span data-ttu-id="0b0a8-109">Угол снаружи конуса должен всегда быть больше или равен внутреннему уголу конуса.</span><span class="sxs-lookup"><span data-stu-id="0b0a8-109">The outside cone angle must always be equal to or greater than the inside cone angle.</span></span>

<span data-ttu-id="0b0a8-110">В любом углу внутреннего конуса громкость звука устанавливается равным внутреннему цилиндру.</span><span class="sxs-lookup"><span data-stu-id="0b0a8-110">At any angle within the inner cone, the volume of the sound is set to the inner cone volume.</span></span> <span data-ttu-id="0b0a8-111">В этом случае учитывается базовый объем буфера, расстояние от прослушивателя, ориентация прослушивателя, если прослушиватель имеет собственный конус и т. д.</span><span class="sxs-lookup"><span data-stu-id="0b0a8-111">This takes into account the basic volume of the buffer, the distance from the listener, the listener's orientation if the listener has its own cone, and so on.</span></span>

<span data-ttu-id="0b0a8-112">С любого угла за пределами внешнего конуса нормальный том помещается в степень, заданную приложением.</span><span class="sxs-lookup"><span data-stu-id="0b0a8-112">At any angle outside the outer cone, the normal volume is attenuated by a factor set by the application.</span></span> <span data-ttu-id="0b0a8-113">Внешний уровень громкости конусов выражается в линейном масштабировании амплитуды: 1,0 f не означает никакого затухания, применяемого к исходному сигналу, 0,5 f обозначает затухание 6 dB, а 0,0 f приводит к бездействиям.</span><span class="sxs-lookup"><span data-stu-id="0b0a8-113">The outside cone volume level is expressed as a linear amplitude scaler: 1.0 f represents no attenuation applied to the original signal, 0.5 f denotes an attenuation of 6 dB, and 0.0 f results in silence.</span></span> <span data-ttu-id="0b0a8-114">Усиление (Volume > 1,0 f) также разрешено и не находится в виде фиксации.</span><span class="sxs-lookup"><span data-stu-id="0b0a8-114">Amplification (volume > 1.0 f) is also allowed, and is not clamped.</span></span> <span data-ttu-id="0b0a8-115">Допустимый диапазон томов — от 0,0 f до 2,0 f.</span><span class="sxs-lookup"><span data-stu-id="0b0a8-115">The valid volume range is actually 0.0 f to 2.0 f.</span></span>

<span data-ttu-id="0b0a8-116">Между внутренним и внешним конес — это зона перехода с внутреннего тома на внешний.</span><span class="sxs-lookup"><span data-stu-id="0b0a8-116">Between the inner and outer cones is a zone of transition from the inside volume to the outside volume.</span></span> <span data-ttu-id="0b0a8-117">Том приближается к внешнему тому конуса по мере увеличения угла.</span><span class="sxs-lookup"><span data-stu-id="0b0a8-117">The volume approaches the cone's outer volume as the angle increases.</span></span>

<span data-ttu-id="0b0a8-118">Конес может влиять на параметры, отличные от Volume.</span><span class="sxs-lookup"><span data-stu-id="0b0a8-118">Cones can affect parameters other than volume.</span></span> <span data-ttu-id="0b0a8-119">Также может затронуть низкий уровень фильтрации и отправки переглаголов, что делает эту методику еще более значительной.</span><span class="sxs-lookup"><span data-stu-id="0b0a8-119">Low pass filter and reverb send level may also be affected, making the technique even more dramatic.</span></span> <span data-ttu-id="0b0a8-120">Например, с конусом на прослушиватель можно указать, что все звуки за прослушивателем получают немного муффлед и имеют несколько более высоких данных о переглаголе на прямую.</span><span class="sxs-lookup"><span data-stu-id="0b0a8-120">For example, with a cone on the listener, one can specify all sounds behind the listener get a bit muffled, and have slightly higher reverb-to-direct ratio content.</span></span> <span data-ttu-id="0b0a8-121">Они предоставляют больше подсказок о том, что звук находится за пользователем.</span><span class="sxs-lookup"><span data-stu-id="0b0a8-121">These provide more cues that the sound is behind the user.</span></span> <span data-ttu-id="0b0a8-122">Это улучшает реальные возможности.</span><span class="sxs-lookup"><span data-stu-id="0b0a8-122">This enhances realism.</span></span>

<span data-ttu-id="0b0a8-123">На следующем рисунке показана концепция Sound конес.</span><span class="sxs-lookup"><span data-stu-id="0b0a8-123">The following illustration shows the concept of sound cones.</span></span>

![звук конес](images/common-audio-concepts-sound-cones.png)

<span data-ttu-id="0b0a8-125">Правильная разработка звуковых конес может значительно повысить эффект приложения.</span><span class="sxs-lookup"><span data-stu-id="0b0a8-125">Designing sound cones properly can add dramatic effects to your application.</span></span> <span data-ttu-id="0b0a8-126">Например, можно разместить звуковый источник в центре комнаты, установив его ориентацию в сторону открытой дверцы в коридора.</span><span class="sxs-lookup"><span data-stu-id="0b0a8-126">For example, you could position a sound source in the center of a room, setting its orientation toward an open door in a hallway.</span></span> <span data-ttu-id="0b0a8-127">Затем установите угол внутри конуса таким образом, чтобы он был увеличен до ширины двери, сделайте внешний конус более широким и, наконец, установите для внешнего конуса значение неразборчиво.</span><span class="sxs-lookup"><span data-stu-id="0b0a8-127">Then set the angle of the inside cone so that it extends to the width of the doorway, make the outside cone a bit wider, and finally set the outside cone volume to inaudible.</span></span> <span data-ttu-id="0b0a8-128">Прослушиватель, перемещающийся по коридора, начнет слышать звук только при приближении к двери.</span><span class="sxs-lookup"><span data-stu-id="0b0a8-128">A listener moving along the hallway will begin to hear the sound only when near the doorway.</span></span> <span data-ttu-id="0b0a8-129">Звук будет громкее, так как прослушиватель проходит перед открытой дверцей.</span><span class="sxs-lookup"><span data-stu-id="0b0a8-129">The sound will be loudest as the listener passes in front of the open door.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0b0a8-130">См. также</span><span class="sxs-lookup"><span data-stu-id="0b0a8-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b0a8-131">Общие концепции аудио</span><span class="sxs-lookup"><span data-stu-id="0b0a8-131">Common Audio Concepts</span></span>](common-audio-concepts.md)
</dt> <dt>

[<span data-ttu-id="0b0a8-132">X3DAudio</span><span class="sxs-lookup"><span data-stu-id="0b0a8-132">X3DAudio</span></span>](x3daudio-overview.md)
</dt> <dt>

[<span data-ttu-id="0b0a8-133">**X3DAUDIO \_ конус**</span><span class="sxs-lookup"><span data-stu-id="0b0a8-133">**X3DAUDIO\_CONE**</span></span>](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_cone)
</dt> </dl>

 

 



