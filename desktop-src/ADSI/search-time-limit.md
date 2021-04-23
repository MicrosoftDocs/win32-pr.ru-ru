---
title: Предельное время поиска
description: При запросе поиска на сервере, находящимся под интенсивной рабочей нагрузкой, может потребоваться указать серверу ограничить поиск до определенного предельного времени.
ms.assetid: 199ac73b-3624-4cd5-a1ee-6db418cd77ba
ms.tgt_platform: multiple
keywords:
- Предельное время поиска (ADSI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e11ff9de38a17fe6ebac4ebb045e2f8b896bc764
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105654105"
---
# <a name="search-time-limit"></a><span data-ttu-id="fabf5-104">Предельное время поиска</span><span class="sxs-lookup"><span data-stu-id="fabf5-104">Search Time Limit</span></span>

<span data-ttu-id="fabf5-105">При запросе поиска на сервере, находящимся под интенсивной рабочей нагрузкой, может потребоваться указать серверу ограничить поиск до определенного предельного времени.</span><span class="sxs-lookup"><span data-stu-id="fabf5-105">When you request a search on a server that is under a heavy workload, you may want to instruct the server to restrict the search to a specified time limit.</span></span> <span data-ttu-id="fabf5-106">Например, чтобы запустить приложение для создания еженедельного отчета на сервере, который работает почти в течение емкости, и избежать увеличения времени ЦП и предотвратить выполнение других заданий, можно задать для времени поиска небольшое значение и повторно запустить приложение позже, если не удается создать отчет.</span><span class="sxs-lookup"><span data-stu-id="fabf5-106">For example, to execute an application to generate a weekly report on a server that is running near capacity, and to avoid maximizing the CPU time and preventing other jobs from running, you can set the search time to a small value and rerun the application later if it fails to generate the report.</span></span>

<span data-ttu-id="fabf5-107">Некоторые серверы могут накладывать собственное административное ограничение по времени.</span><span class="sxs-lookup"><span data-stu-id="fabf5-107">Some servers can impose their own administrative time limit.</span></span> <span data-ttu-id="fabf5-108">В таких случаях при указании предельного времени поиска, превышающего предел времени администратора, сервер игнорирует спецификацию и вместо этого использует внутреннее административное ограничение по времени.</span><span class="sxs-lookup"><span data-stu-id="fabf5-108">In these cases, if you specify a search time limit value greater than the administrative time limit, the server ignores your specification and use its internal administrative time limit instead.</span></span>

<span data-ttu-id="fabf5-109">Дополнительные сведения об использовании параметра предельное время поиска с конкретным интерфейсом поиска см. в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="fabf5-109">For more information about using the search time limit option with a specific search interface, see:</span></span>

-   [<span data-ttu-id="fabf5-110">Ограничение времени сервера на IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="fabf5-110">Server Time Limit with IDirectorySearch</span></span>](server-time-limit-with-idirectorysearch.md)
-   [<span data-ttu-id="fabf5-111">Поиск с помощью объекты данных ActiveX</span><span class="sxs-lookup"><span data-stu-id="fabf5-111">Searching with ActiveX Data Objects</span></span>](searching-with-activex-data-objects-ado.md)
-   [<span data-ttu-id="fabf5-112">Поиск с помощью OLE DB</span><span class="sxs-lookup"><span data-stu-id="fabf5-112">Searching with OLE DB</span></span>](searching-with-ole-db.md)

 

 




