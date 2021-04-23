---
title: Неправильные обратные вызовы предупреждений интерфейса
description: После того как сервер пересылки ядра получает данные многоадресной рассылки из определенного источника на неправильном интерфейсе, он уведомляет Диспетчер групп многоадресной рассылки.
ms.assetid: 7b20625e-286b-4c4f-8452-4d21563fd030
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d12906d836ca994e90347ea78cf22e50f8f2f00d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779448"
---
# <a name="wrong-interface-alert-callbacks"></a><span data-ttu-id="85fd1-103">Неправильные обратные вызовы предупреждений интерфейса</span><span class="sxs-lookup"><span data-stu-id="85fd1-103">Wrong Interface Alert Callbacks</span></span>

<span data-ttu-id="85fd1-104">После того как сервер пересылки ядра получает данные многоадресной рассылки из определенного источника на неправильном интерфейсе, он уведомляет Диспетчер групп многоадресной рассылки.</span><span class="sxs-lookup"><span data-stu-id="85fd1-104">After the kernel forwarder receives multicast data from a specific source on the wrong interface, it notifies the multicast group manager.</span></span> <span data-ttu-id="85fd1-105">Затем Диспетчер групп многоадресной рассылки вызывает [**ошибку пмгм, если обратный вызов \_ \_ \_ обратного вызова**](/windows/desktop/api/Mgm/nc-mgm-pmgm_wrong_if_callback) к протоколу маршрутизации, владеющему интерфейсом, в котором данные были ошибочно получены.</span><span class="sxs-lookup"><span data-stu-id="85fd1-105">The multicast group manager then invokes the [**PMGM\_WRONG\_IF\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_wrong_if_callback) callback to the routing protocol that owns the interface on which the data incorrectly arrived.</span></span>

> [!Note]  
> <span data-ttu-id="85fd1-106">Этот обратный вызов в настоящее время не реализован в этой версии API МГМ.</span><span class="sxs-lookup"><span data-stu-id="85fd1-106">This callback is not currently implemented in this version of the MGM API.</span></span>

 

 

 




