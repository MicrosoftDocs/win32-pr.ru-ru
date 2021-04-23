---
description: Список экспортируемых библиотек DLL, которые должны быть реализованы для создания диспетчера учетных данных.
ms.assetid: 8b176dd6-0e0b-4330-8889-f87384977ceb
title: Реализация диспетчера учетных данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0bbd42f4ade57b754c6f7a067519d7df2711cfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912480"
---
# <a name="implementing-a-credential-manager"></a><span data-ttu-id="1b5c8-103">Реализация диспетчера учетных данных</span><span class="sxs-lookup"><span data-stu-id="1b5c8-103">Implementing a Credential Manager</span></span>

<span data-ttu-id="1b5c8-104">Чтобы создать диспетчер учетных данных, необходимо создать библиотеку DLL, которая экспортирует следующие функции:</span><span class="sxs-lookup"><span data-stu-id="1b5c8-104">To create a credential manager, you must create a DLL that exports the following functions:</span></span>

-   [<span data-ttu-id="1b5c8-105">**нплогоннотифи**</span><span class="sxs-lookup"><span data-stu-id="1b5c8-105">**NPLogonNotify**</span></span>](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify)
-   [<span data-ttu-id="1b5c8-106">**нппассвордчанженотифи**</span><span class="sxs-lookup"><span data-stu-id="1b5c8-106">**NPPasswordChangeNotify**</span></span>](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify)

<span data-ttu-id="1b5c8-107">Чтобы восстановить уведомления в функциях [**нплогоннотифи**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify) и [**нппассвордчанженотифи**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify) для входа со смарт-картой, создайте запись реестра с именем **смарткардлогоннотифи** в виде **DWORD** и задайте для нее значение 1:</span><span class="sxs-lookup"><span data-stu-id="1b5c8-107">To restore notifications to the [**NPLogonNotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify) and [**NPPasswordChangeNotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify) functions for smart card logon, create a registry entry called **SmartCardLogonNotify** as a **DWORD**, and set it to 1:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
   Microsoft
   Windows NT
   CurrentVersion
      Winlogon
         Notify
            SmartCardLogonNotify = 1
```

<span data-ttu-id="1b5c8-108">**Windows Server 2003 и Windows XP:** Запись реестра **смарткардлогоннотифи** не требуется.</span><span class="sxs-lookup"><span data-stu-id="1b5c8-108">**Windows Server 2003 and Windows XP:** The **SmartCardLogonNotify** registry entry is not required.</span></span>

<span data-ttu-id="1b5c8-109">Кроме того, диспетчеры учетных данных также должны поддерживать функцию [**нпжеткапс**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) для \_ запуска вннк (поддержка других индексов для диспетчеров учетных данных не требуется).</span><span class="sxs-lookup"><span data-stu-id="1b5c8-109">In addition, credential managers should also support the [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) function for WNNC\_START (supporting other indexes is not required for credential managers).</span></span> <span data-ttu-id="1b5c8-110">Это говорит о том, что будет запущен диспетчер учетных данных.</span><span class="sxs-lookup"><span data-stu-id="1b5c8-110">This tells MPR when a credential manager will start.</span></span> <span data-ttu-id="1b5c8-111">При вызове **нпжеткапс** с параметром *ниндекс* , для которого задано значение вннк \_ Start, многопротокольный маршрутизатор получает время ожидания перед вызовом функций точки входа управления учетными данными поставщика.</span><span class="sxs-lookup"><span data-stu-id="1b5c8-111">By calling **NPGetCaps** with the *nIndex* parameter set to WNNC\_START, the MPR gets the time to wait before calling the provider's credential management entry point functions.</span></span> <span data-ttu-id="1b5c8-112">И если многопротокольный маршрутизатор имеет эти сведения, он может переслать его диспетчеру учетных данных, установив время ожидания.</span><span class="sxs-lookup"><span data-stu-id="1b5c8-112">And if the MPR has this information, it can forward it to the credential manager, setting the time out.</span></span>

 

 



