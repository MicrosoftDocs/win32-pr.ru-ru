---
title: Составление имен участников-служб для службы с SCP
description: В следующем примере кода создается имя субъекта-службы, использующее точку подключения службы (SCP).
ms.assetid: cbaa11ba-d32b-46cf-86a4-9050bb1be3a6
ms.tgt_platform: multiple
keywords:
- Составление имен участников-служб для службы с помощью SCP AD
- Имя субъекта-службы AD, составление имен субъектов-служб для службы с SCP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0a9c44bc603372af35e874acfea4c1e12a2433d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067269"
---
# <a name="composing-the-spns-for-a-service-with-an-scp"></a><span data-ttu-id="c4382-105">Составление имен участников-служб для службы с SCP</span><span class="sxs-lookup"><span data-stu-id="c4382-105">Composing the SPNs for a Service with an SCP</span></span>

<span data-ttu-id="c4382-106">В следующем примере кода создается имя субъекта-службы, использующее точку подключения службы (SCP).</span><span class="sxs-lookup"><span data-stu-id="c4382-106">The following code example composes an SPN for a service that uses a service connection point (SCP).</span></span> <span data-ttu-id="c4382-107">Возвращенное имя субъекта-службы имеет следующий формат.</span><span class="sxs-lookup"><span data-stu-id="c4382-107">The returned SPN has the following format.</span></span>


```C++
<service class>/<host>/<service name>
```



<span data-ttu-id="c4382-108">" &lt; класс службы &gt; " и " &lt; имя службы &gt; " соответствуют параметрам *псзднофскп* и *псзсервицекласс* .</span><span class="sxs-lookup"><span data-stu-id="c4382-108">"&lt;service class&gt;" and "&lt;service name&gt;" correspond to the *pszDNofSCP* and *pszServiceClass* parameters.</span></span> <span data-ttu-id="c4382-109">" &lt; host &gt; " по умолчанию имеет DNS-имя локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="c4382-109">"&lt;host&gt;" defaults to the DNS name of the local computer.</span></span>


```C++
DWORD
SpnCompose(
    TCHAR ***pspn,          // Output: an array of SPNs
    unsigned long *pulSpn,  // Output: the number of SPNs returned
    TCHAR *pszDNofSCP,      // Input: DN of the service's SCP
    TCHAR* pszServiceClass) // Input: the name of the service class
{
DWORD   dwStatus;    
 
dwStatus = DsGetSpn(
    DS_SPN_SERVICE, // Type of SPN to create (enumerated type)
    pszServiceClass, // Service class - a name in this case
    pszDNofSCP, // Service name - DN of the service SCP
    0, // Default: omit port component of SPN
    0, // Number of entries in hostnames and ports arrays
    NULL, // Array of hostnames. Default is local computer
    NULL, // Array of ports. Default omits port component
    pulSpn, // Receives number of SPNs returned in array
    pspn // Receives array of SPN(s)
    );
 
return dwStatus;
}
```



 

 




