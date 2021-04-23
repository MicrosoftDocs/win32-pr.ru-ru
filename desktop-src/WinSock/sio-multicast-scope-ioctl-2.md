---
description: Использование \_ кода команды многоадресной \_ области ввода/вывода для указания области, в которой должно выполняться многоадресная рассылка.
ms.assetid: 3acec987-9cb4-446c-af6e-ea0e6a96e70c
title: SIO_MULTICAST_SCOPE ioctl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90d1fd6f2bea76d095ea88d66c0ac029fb9168ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693392"
---
# <a name="sio_multicast_scope-ioctl"></a><span data-ttu-id="f13ce-103">\_Многоадресная \_ область действия ioctl</span><span class="sxs-lookup"><span data-stu-id="f13ce-103">SIO\_MULTICAST\_SCOPE Ioctl</span></span>

<span data-ttu-id="f13ce-104">При использовании многоадресной рассылки обычно необходимо указать область, в которой должна выполняться многоадресная рассылка.</span><span class="sxs-lookup"><span data-stu-id="f13ce-104">When multicasting is employed, it is usually necessary to specify the scope over which the multicast should occur.</span></span> <span data-ttu-id="f13ce-105">Здесь область определяется как количество сегментов маршрутизируемых сетей, подпадающих под действие.</span><span class="sxs-lookup"><span data-stu-id="f13ce-105">Here scope is defined to be the number of routed network segments to be covered.</span></span> <span data-ttu-id="f13ce-106">\_ \_ Для управления этим используется код команды многоадресной области SIO для [**вспиоктл**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="f13ce-106">The SIO\_MULTICAST\_SCOPE command code for [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) is used to control this.</span></span> <span data-ttu-id="f13ce-107">Нулевая область означает, что многоадресная передача не будет помещаться в сеть, но может быть распределена между сокетами на локальном узле.</span><span class="sxs-lookup"><span data-stu-id="f13ce-107">A scope of zero would indicate that the multicast transmission would not be placed on the wire but could be disseminated across sockets within the local host.</span></span> <span data-ttu-id="f13ce-108">Значение области, равное единице (по умолчанию), указывает, что передача будет размещена на канале передачи, но не будет пересекать маршрутизаторы.</span><span class="sxs-lookup"><span data-stu-id="f13ce-108">A scope value of one (the default) indicates that the transmission will be placed on the wire, but will not cross any routers.</span></span> <span data-ttu-id="f13ce-109">Более высокие значения области определяют количество маршрутизаторов, которые могут быть перепутаны.</span><span class="sxs-lookup"><span data-stu-id="f13ce-109">Higher scope values determine the number of routers that may be crossed.</span></span> <span data-ttu-id="f13ce-110">Обратите внимание, что это соответствует параметру срока жизни (TTL) в многоадресной IP-рассылке.</span><span class="sxs-lookup"><span data-stu-id="f13ce-110">Note that this corresponds to the time-to-live (TTL) parameter in IP multicasting.</span></span>

 

 
