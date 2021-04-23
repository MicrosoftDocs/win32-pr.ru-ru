---
title: Убедитесь, что сервер требует утверждения
description: Лучше использовать взаимную проверку подлинности и, таким образом, проверять удостоверение сервера.
ms.assetid: 6636a865-0e3b-4e52-81bb-0df48285e928
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d3e16ae6a87134a9fbc783d35216a1c4df56ce2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776112"
---
# <a name="verify-the-server-is-who-it-claims-to-be"></a><span data-ttu-id="e505b-103">Убедитесь, что сервер требует утверждения</span><span class="sxs-lookup"><span data-stu-id="e505b-103">Verify the Server is Who it Claims to Be</span></span>

<span data-ttu-id="e505b-104">Лучше использовать взаимную проверку подлинности и, таким образом, проверять удостоверение сервера.</span><span class="sxs-lookup"><span data-stu-id="e505b-104">It is best to use mutual authentication, and thereby verify the identity of the server.</span></span> <span data-ttu-id="e505b-105">Примером распространенной ошибки, которую не удается сделать, являются приложения, которые имеют локальную службу, в которую клиент вызывает.</span><span class="sxs-lookup"><span data-stu-id="e505b-105">An example of a common mistake that fails to do this is applications that have a local service into which clients call.</span></span> <span data-ttu-id="e505b-106">В некоторых конфигурациях администратор может решить, что системная служба не является действительно полезной и ее можно отключить.</span><span class="sxs-lookup"><span data-stu-id="e505b-106">In some configurations an administrator may decide that the system service is not really useful and may chose to stop it.</span></span> <span data-ttu-id="e505b-107">На компьютере сервера терминалов может быть запущен процесс, который прослушивает ту же конечную точку, и когда клиент подключается к конечной точке, разрешая олицетворение на сервере без взаимной проверки подлинности сервера, злоумышленник может олицетворять клиента и получать доступ к данным клиента, а также выполнять сетевые вызовы от имени клиента.</span><span class="sxs-lookup"><span data-stu-id="e505b-107">An inventive attacker on a terminal server computer may launch a process that listens on the same endpoint, and when a client connects to an endpoint, allowing impersonation on the server without mutually authenticating the server, the attacker can impersonate the client and access the client's data, or make network calls on behalf of the client.</span></span> <span data-ttu-id="e505b-108">Большинство системных служб работает под хорошо известной учетной записью, например Локалсисем, LocalService или NetworkService, которую можно проверить с помощью взаимной проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="e505b-108">Most system services run under a well-known account, such as LocalSysyem, LocalService, or NetworkService, which can be verified using mutual authentication.</span></span>

 

 




