---
title: Рекомендации для приложений и служб
description: Чтобы сократить число перезапусков системы при установке и обслуживании приложений в Windows Vista или Windows Server 2008, необходимо следовать приведенным ниже рекомендациям, чтобы обеспечить корректное завершение работы приложения или службы.
ms.assetid: d0b9344f-05c6-4054-90b9-86942df50b3d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaf2963c03432a8b016f01316b79b387754f1459
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105650270"
---
# <a name="guidelines-for-applications-and-services"></a><span data-ttu-id="e4403-103">Рекомендации для приложений и служб</span><span class="sxs-lookup"><span data-stu-id="e4403-103">Guidelines for Applications and Services</span></span>

<span data-ttu-id="e4403-104">Чтобы сократить число перезапусков системы при установке и обслуживании приложений в Windows Vista или Windows Server 2008, необходимо следовать приведенным ниже рекомендациям, чтобы обеспечить корректное завершение работы приложения или службы.</span><span class="sxs-lookup"><span data-stu-id="e4403-104">To reduce the number of system restarts when installing and servicing applications on Windows Vista or Windows Server 2008, you should observe the following guidelines to enable your application or service to be shut down cleanly and restarted.</span></span>

-   <span data-ttu-id="e4403-105">Приложения и службы должны быть готовы к завершению работы и перезапускаются системой, если это необходимо для установки обновления.</span><span class="sxs-lookup"><span data-stu-id="e4403-105">Your applications and services should be prepared to be shut down and restarted by the system when this is necessary to install an update.</span></span> <span data-ttu-id="e4403-106">Как правило, при установке обновления необходимо завершить работу приложения или службы, поскольку в настоящее время используется затронутый файл.</span><span class="sxs-lookup"><span data-stu-id="e4403-106">Typically, when an update is installed, an application or service needs to be shut down because it currently holds an affected file in use.</span></span> <span data-ttu-id="e4403-107">Все приложения или службы, которые могут хранить файл, используемый во время обновления, должны быть готовы к завершению работы.</span><span class="sxs-lookup"><span data-stu-id="e4403-107">All applications or services that can hold a file in use during an update should be prepared to shut down cleanly.</span></span>
-   <span data-ttu-id="e4403-108">Приложения должны сохранять данные пользователя и сведения о состоянии, необходимые после перезагрузки, и следовать рекомендациям, описанным в разделе [рекомендации для приложений](guidelines-for-applications.md).</span><span class="sxs-lookup"><span data-stu-id="e4403-108">Your applications should save user data and state information that are needed after a restart and should adhere to the guidelines that are described in the section [Guidelines for Applications](guidelines-for-applications.md).</span></span>
-   <span data-ttu-id="e4403-109">Службы должны соблюдать рекомендации, описанные в разделе [рекомендации по службам](guidelines-for-services.md).</span><span class="sxs-lookup"><span data-stu-id="e4403-109">Your services should adhere to the guidelines that are described in the section [Guidelines for Services](guidelines-for-services.md).</span></span>
-   <span data-ttu-id="e4403-110">Диспетчер перезапуска не завершает работу [критических системных служб](critical-system-services.md); Таким образом, эти службы должны ограничивать количество библиотек DLL, от которых они зависят.</span><span class="sxs-lookup"><span data-stu-id="e4403-110">Restart Manager does not shut down [critical system services](critical-system-services.md); therefore, these services should limit the number of DLLs they depend on.</span></span>

 

 




