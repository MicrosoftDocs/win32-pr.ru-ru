---
title: Получение сведений о системе MCI
description: Получение сведений о системе MCI
ms.assetid: 06175d6e-6d09-4c95-93e9-03af870a2d3f
keywords:
- Команда MCI_SYSINFO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3b5f5d2bf8cc8edd3edf65a9c559b6ec47b0631
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986378"
---
# <a name="obtaining-mci-system-information"></a><span data-ttu-id="b8b01-104">Получение сведений о системе MCI</span><span class="sxs-lookup"><span data-stu-id="b8b01-104">Obtaining MCI System Information</span></span>

<span data-ttu-id="b8b01-105">Команда [сисинфо](sysinfo.md) ([**MCI \_ сисинфо**](mci-sysinfo.md)) получает сведения о системе для устройств MCI.</span><span class="sxs-lookup"><span data-stu-id="b8b01-105">The [sysinfo](sysinfo.md) ([**MCI\_SYSINFO**](mci-sysinfo.md)) command obtains system information about MCI devices.</span></span> <span data-ttu-id="b8b01-106">MCI обрабатывает эту команду без ее пересылки на любое устройство MCI.</span><span class="sxs-lookup"><span data-stu-id="b8b01-106">MCI handles this command without relaying it to any MCI device.</span></span> <span data-ttu-id="b8b01-107">Для интерфейса командной строки MCI возвращает сведения о системе в структуре [**MCI \_ сисинфо \_ пармс**](mci-sysinfo-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="b8b01-107">For the command-message interface, MCI returns the system information in the [**MCI\_SYSINFO\_PARMS**](mci-sysinfo-parms.md) structure.</span></span>

<span data-ttu-id="b8b01-108">Команду **сисинфо** (MCI \_ сисинфо) можно использовать для получения таких сведений, как число устройств MCI в системе, число устройств MCI определенного типа, число открытых устройств MCI и имена устройств.</span><span class="sxs-lookup"><span data-stu-id="b8b01-108">You can use the **sysinfo** (MCI\_SYSINFO) command to retrieve information such as the number of MCI devices on a system, the number of MCI devices of a particular type, the number of open MCI devices, and the names of the devices.</span></span> <span data-ttu-id="b8b01-109">Эта команда часто вызывается более одного раза для получения определенного фрагмента информации.</span><span class="sxs-lookup"><span data-stu-id="b8b01-109">This command is often called more than once to retrieve a particular piece of information.</span></span> <span data-ttu-id="b8b01-110">Например, можно получить число устройств определенного типа при первом вызове, а затем перечислить имена устройств в следующем.</span><span class="sxs-lookup"><span data-stu-id="b8b01-110">For example, you might retrieve the number of devices of a particular type in the first call and then enumerate the names of the devices in the next.</span></span>

 

 




