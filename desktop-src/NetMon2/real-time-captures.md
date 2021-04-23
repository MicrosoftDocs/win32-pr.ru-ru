---
description: Мониторы получают захваченные кадры сети в режиме реального времени. Кадры фиксируются поставщиком сетевых пакетов (НПП) с помощью COM-интерфейса ИРТК Providers и передаются монитору в одном из мониторов двух потоков выполнения.
ms.assetid: 50aa9da2-3a8a-4514-9b1b-9c8364d074d0
title: Записи Real-Time
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24bdf5bc451173a98d1c4428674d308f8b3b8d79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913651"
---
# <a name="real-time-captures"></a><span data-ttu-id="41f88-104">Записи Real-Time</span><span class="sxs-lookup"><span data-stu-id="41f88-104">Real-Time Captures</span></span>

<span data-ttu-id="41f88-105">Мониторы получают захваченные кадры сети в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="41f88-105">Monitors receive captured network frames in real-time mode.</span></span> <span data-ttu-id="41f88-106">Кадры фиксируются [*поставщиком сетевых пакетов*](n.md) (НПП) с помощью COM-интерфейса [ИРТК](irtc.md) поставщика и передаются монитору в одном из двух потоков выполнения монитора.</span><span class="sxs-lookup"><span data-stu-id="41f88-106">The frames are captured by a [*network packet provider*](n.md) (NPP) using the provider's [IRTC](irtc.md) COM interface, and passed on to the monitor in one of the monitor's two execution threads.</span></span>

<span data-ttu-id="41f88-107">Мониторы могут ограничивать количество кадров, которые они должны обработать, передавая [*фильтр записи*](c.md) НПП, который предоставляет кадры.</span><span class="sxs-lookup"><span data-stu-id="41f88-107">Monitors can limit the number of frames they have to process by passing a [*capture filter*](c.md) to the NPP that is supplying the frames.</span></span> <span data-ttu-id="41f88-108">Как правило, конкретный монитор предназначен для наблюдения за конкретными типами трафика, такими как HTTP, RIPX или SMB.</span><span class="sxs-lookup"><span data-stu-id="41f88-108">Typically, a specific monitor is designed to watch for specific types of traffic, such as HTTP, RIPX, or SMB.</span></span> <span data-ttu-id="41f88-109">В отличие от экспертов, которые используют сложные средства синтаксического анализа для выбора анализируемых данных, монитор должен изучить каждый кадр на предмет условий, которые он был предназначен для обнаружения.</span><span class="sxs-lookup"><span data-stu-id="41f88-109">Unlike experts, which use sophisticated parsers to select the information to be analyzed, a monitor must examine each frame for the conditions it was designed to detect.</span></span> <span data-ttu-id="41f88-110">Причина этого подхода в кадрах заключается в производительности.</span><span class="sxs-lookup"><span data-stu-id="41f88-110">The reason behind this frame-by-frame approach is performance.</span></span> <span data-ttu-id="41f88-111">Монитор должен быстро обрабатывать свои кадры, чтобы он не выпадал за пределы драйвера, предоставляя кадры НПП.</span><span class="sxs-lookup"><span data-stu-id="41f88-111">A monitor must process its frames quickly enough so that it does not fall behind the driver supplying the frames to the NPP.</span></span> <span data-ttu-id="41f88-112">В противном случае данные будут потеряны.</span><span class="sxs-lookup"><span data-stu-id="41f88-112">Otherwise, data will be lost.</span></span>

 

 



