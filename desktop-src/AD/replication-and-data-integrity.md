---
title: Репликация и целостность данных
description: Домен Active Directory Services обеспечивают обновление нескольких хозяев.
ms.assetid: 99d35e16-9d1e-40d9-b1b0-600966165e45
ms.tgt_platform: multiple
keywords:
- Active Directory, использование, репликация и целостность данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 499f7e2c3193a280d009f53521e7a94fa3b89c5e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105654173"
---
# <a name="replication-and-data-integrity"></a><span data-ttu-id="2d5b9-104">Репликация и целостность данных</span><span class="sxs-lookup"><span data-stu-id="2d5b9-104">Replication and Data Integrity</span></span>

<span data-ttu-id="2d5b9-105">Домен Active Directory Services обеспечивают *Обновление нескольких хозяев*.</span><span class="sxs-lookup"><span data-stu-id="2d5b9-105">Active Directory Domain Services provide *multi-master update*.</span></span> <span data-ttu-id="2d5b9-106">Обновление с несколькими хозяевами означает, что все полные реплики данного раздела доступны для записи (частичные реплики на серверах глобального каталога недоступны для записи). Обновление с несколькими хозяевами означает, что обновления не блокируются даже в том случае, если некоторые реплики неработоспособны.</span><span class="sxs-lookup"><span data-stu-id="2d5b9-106">Multi-master update means that all full replicas of a given partition are writable (the partial replicas on global catalog servers are not writable.) Multi-master update means that updates are not blocked even when some replicas are inoperable.</span></span> <span data-ttu-id="2d5b9-107">Сервер Active Directory распространяет изменения из обновленной реплики на все остальные реплики.</span><span class="sxs-lookup"><span data-stu-id="2d5b9-107">The Active Directory server propagates the changes from the updated replica to all other replicas.</span></span> <span data-ttu-id="2d5b9-108">Репликация является автоматической и прозрачной.</span><span class="sxs-lookup"><span data-stu-id="2d5b9-108">Replication is automatic and transparent.</span></span>

<span data-ttu-id="2d5b9-109">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="2d5b9-109">For more information, see the following topics.</span></span>

-   [<span data-ttu-id="2d5b9-110">Модель репликации в службах домен Active Directory</span><span class="sxs-lookup"><span data-stu-id="2d5b9-110">The Replication Model in Active Directory Domain Services</span></span>](replication-model-in-active-directory-domain-services.md)
-   [<span data-ttu-id="2d5b9-111">Поведение репликации в службах домен Active Directory Services</span><span class="sxs-lookup"><span data-stu-id="2d5b9-111">Replication Behavior in Active Directory Domain Services</span></span>](replication-behavior-in-active-directory-domain-services.md)
-   [<span data-ttu-id="2d5b9-112">Обнаружение и предотвращение задержки репликации</span><span class="sxs-lookup"><span data-stu-id="2d5b9-112">Detecting and Avoiding Replication Latency</span></span>](detecting-and-avoiding-replication-latency.md)

 

 




