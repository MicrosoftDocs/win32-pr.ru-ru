---
title: Получение сведений об устройстве
description: Получение сведений об устройстве
ms.assetid: d038d3fb-43d0-4d9d-836c-205f6d8c98e3
keywords:
- Команда MCI_GETDEVCAPS
- Команда MCI_STATUS
- Команда MCI_INFO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10acb53fa1a961fe7a70042350f8d889d9fdf572
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986798"
---
# <a name="retrieving-information-about-a-device"></a><span data-ttu-id="77dc0-106">Получение сведений об устройстве</span><span class="sxs-lookup"><span data-stu-id="77dc0-106">Retrieving Information About a Device</span></span>

<span data-ttu-id="77dc0-107">Каждое устройство реагирует на [**возможности**](capability.md) ([**MCI \_ жетдевкапс**](mci-getdevcaps.md)), [**состояние**](status.md) ([**\_ состояние MCI**](mci-status.md)) и [**сведения**](info.md) ([**\_ сведения о MCI**](mci-info.md)).</span><span class="sxs-lookup"><span data-stu-id="77dc0-107">Every device responds to the [**capability**](capability.md) ([**MCI\_GETDEVCAPS**](mci-getdevcaps.md)), [**status**](status.md) ([**MCI\_STATUS**](mci-status.md)), and [**info**](info.md) ([**MCI\_INFO**](mci-info.md)) commands.</span></span> <span data-ttu-id="77dc0-108">Эти команды получают сведения об устройстве.</span><span class="sxs-lookup"><span data-stu-id="77dc0-108">These commands obtain information about the device.</span></span> <span data-ttu-id="77dc0-109">Например, следующая команда возвращает значение true, если устройство **кдаудио** может извлечь диск:</span><span class="sxs-lookup"><span data-stu-id="77dc0-109">For example, the following command returns "true" if a **cdaudio** device can eject the disc:</span></span>


```C++
mciSendString(
    "capability cdaudio can eject", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
```



<span data-ttu-id="77dc0-110">Флаги, перечисленные для обязательных и основных команд, предоставляют минимальный объем сведений об устройстве.</span><span class="sxs-lookup"><span data-stu-id="77dc0-110">The flags listed for the required and basic commands provide a minimum amount of information about a device.</span></span> <span data-ttu-id="77dc0-111">Многие устройства дополняют необходимые и базовые команды с расширенными флагами для предоставления дополнительных сведений об устройстве.</span><span class="sxs-lookup"><span data-stu-id="77dc0-111">Many devices supplement the required and basic commands with extended flags to provide additional information about the device.</span></span>

 

 




