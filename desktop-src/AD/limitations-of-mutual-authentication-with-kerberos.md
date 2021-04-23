---
title: Ограничения взаимной проверки подлинности с помощью Kerberos
description: Учетная запись клиента и учетная запись службы должны находиться в доменах машинного кода Windows 2000 или в смешанном режиме, так как службы Kerberos недоступны в доменах прежних версий.
ms.assetid: 54685e88-b289-4db9-b4cb-f5c22a216a0d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 290bd93050c9cb4c89052ce644b4c588f638f312
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486592"
---
# <a name="limitations-of-mutual-authentication-with-kerberos"></a><span data-ttu-id="0af9d-103">Ограничения взаимной проверки подлинности с помощью Kerberos</span><span class="sxs-lookup"><span data-stu-id="0af9d-103">Limitations of Mutual Authentication with Kerberos</span></span>

<span data-ttu-id="0af9d-104">Учетная запись клиента и учетная запись службы должны находиться в доменах машинного кода Windows 2000 или в смешанном режиме, так как службы Kerberos недоступны в доменах прежних версий.</span><span class="sxs-lookup"><span data-stu-id="0af9d-104">Both the client's account and the service's account must be in Windows 2000 native or mixed-mode domains because Kerberos services are not available in downlevel domains.</span></span> <span data-ttu-id="0af9d-105">Кроме того, учетные записи клиента и службы должны находиться в одном лесу, поскольку KDC клиента использует глобальный каталог для поиска имени субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="0af9d-105">In addition, both client and service accounts must be in the same forest because the client's KDC uses the global catalog to search for the service principal name.</span></span>

<span data-ttu-id="0af9d-106">Служба и клиент должны работать под управлением Windows 2000, в противном случае взаимная проверка подлинности с помощью Kerberos завершится ошибкой, так как более ранние версии Windows не поддерживают Kerberos.</span><span class="sxs-lookup"><span data-stu-id="0af9d-106">Both service and client must be running on Windows 2000, otherwise mutual authentication with Kerberos will fail because earlier versions of Windows do not support Kerberos.</span></span>

<span data-ttu-id="0af9d-107">Имена участников-служб должны включать имя DNS сервера узла, на котором запущена служба.</span><span class="sxs-lookup"><span data-stu-id="0af9d-107">Service principal names must include the DNS name of the host server on which the service is running.</span></span> <span data-ttu-id="0af9d-108">Необходимо использовать DNS-имя.</span><span class="sxs-lookup"><span data-stu-id="0af9d-108">You must use the DNS name.</span></span>

 

 




