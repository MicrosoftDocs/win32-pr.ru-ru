---
title: Предоставление прав на вход в качестве службы на главном компьютере
description: При установке службы для запуска от имени учетной записи пользователя домена учетная запись должна иметь право на вход в качестве службы на локальном компьютере.
ms.assetid: 1b217650-4397-4e28-b53e-8b03f3caf903
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95ef2bb87c3cf461e67cb7da20f36d9ac07fb362
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773148"
---
# <a name="granting-logon-as-service-right-on-the-host-computer"></a><span data-ttu-id="66fc5-103">Предоставление прав на вход в качестве службы на главном компьютере</span><span class="sxs-lookup"><span data-stu-id="66fc5-103">Granting Logon as Service Right on the Host Computer</span></span>

<span data-ttu-id="66fc5-104">При установке службы для запуска от имени учетной записи пользователя домена учетная запись должна иметь право на вход в качестве службы на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="66fc5-104">When installing a service to run under a domain user account, the account must have the right to logon as a service on the local computer.</span></span> <span data-ttu-id="66fc5-105">Имейте в виду, что это право входа применяется только к локальному компьютеру и должно быть предоставлено в локальной политике LSA каждого главного компьютера.</span><span class="sxs-lookup"><span data-stu-id="66fc5-105">Be aware that this logon right applies only to the local computer and must be granted in the local LSA policy of each host computer.</span></span> <span data-ttu-id="66fc5-106">Этот шаг не требуется, если служба выполняется как LocalSystem, которая по умолчанию предоставляет это право.</span><span class="sxs-lookup"><span data-stu-id="66fc5-106">This step is not required if your service runs as LocalSystem, which, by default, is granted this right.</span></span>

<span data-ttu-id="66fc5-107">Дополнительные сведения о том, как программно предоставить право на вход в качестве службы, см. в [примере кода лсапривс](https://www.google.com/#q=LSAPrivs).</span><span class="sxs-lookup"><span data-stu-id="66fc5-107">For more information on how to programmatically grant logon as a service right, see the [LSAPrivs sample code](https://www.google.com/#q=LSAPrivs).</span></span>

 

 




