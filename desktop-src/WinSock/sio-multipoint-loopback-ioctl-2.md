---
description: Использование \_ \_ командного кода для обратной передачи SIO MultiPoint для включения или отключения замыкания на себя трафика MultiPoint.
ms.assetid: 7e11932b-ce9a-4500-888f-8a08ab67b46c
title: SIO_MULTIPOINT_LOOPBACK ioctl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c9f0c7527c8c8b8b32b872eccbbbcdc9a3a2c35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105702007"
---
# <a name="sio_multipoint_loopback-ioctl"></a><span data-ttu-id="7fb47-103">\_Ioctl MULTIPOINT с \_ замыканием на себя</span><span class="sxs-lookup"><span data-stu-id="7fb47-103">SIO\_MULTIPOINT\_LOOPBACK Ioctl</span></span>

<span data-ttu-id="7fb47-104">При \_ использовании d конечных сокетов в некорневой плоскости данных, как правило, желательно иметь возможность контролировать, будет ли отправленный трафик также получен обратно на тот же сокет.</span><span class="sxs-lookup"><span data-stu-id="7fb47-104">When d\_leaf sockets are used in a nonrooted data plane, it is generally desirable to be able to control whether traffic sent out is also received back on the same socket.</span></span> <span data-ttu-id="7fb47-105">Для \_ \_ включения или отключения замыкания на себя трафика MultiPoint используется код команды замыкания на себя для [**вспиоктл**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="7fb47-105">The SIO\_MULTIPOINT\_LOOPBACK command code for [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) is used to enable or disable loopback of multipoint traffic.</span></span>

 

 
