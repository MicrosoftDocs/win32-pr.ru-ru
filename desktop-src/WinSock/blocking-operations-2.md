---
description: Понятие блокировки в среде Windows было очень важным.
ms.assetid: bd2ede96-34a4-4912-b9d2-ef11d37d2292
title: Блокирующие операции
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8040865b4c6ededab925279e15d67cb89f7bc6a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692310"
---
# <a name="blocking-operations"></a><span data-ttu-id="09145-103">Блокирующие операции</span><span class="sxs-lookup"><span data-stu-id="09145-103">Blocking Operations</span></span>

<span data-ttu-id="09145-104">Понятие блокировки в среде Windows было очень важным.</span><span class="sxs-lookup"><span data-stu-id="09145-104">The notion of blocking in a Windows environment has historically been a very important one.</span></span> <span data-ttu-id="09145-105">В средах Windows Sockets 1,1 блокирующие вызовы не были бы рекомендуются, так как они были отключены для постоянного взаимодействия с системой.</span><span class="sxs-lookup"><span data-stu-id="09145-105">In Windows Sockets 1.1 environments, blocking calls were discouraged since they tended to disable ongoing interaction with the system.</span></span> <span data-ttu-id="09145-106">Кроме того, они используют псеудоблоккинг методику, которая по различным причинам не всегда работает должным образом.</span><span class="sxs-lookup"><span data-stu-id="09145-106">Additionally, they employ a pseudoblocking technique which, for a variety of reasons, does not always work as intended.</span></span> <span data-ttu-id="09145-107">Однако в запланированных с приоритетами средах Windows, блокирующие вызовы гораздо более осмысленны, могут быть реализованы собственными службами операционной системы и фактически являются предпочтительным механизмом.</span><span class="sxs-lookup"><span data-stu-id="09145-107">However, in preemptively scheduled Windows environments, blocking calls make much more sense, can be implemented by native operating system services, and are in fact a generally preferred mechanism.</span></span> <span data-ttu-id="09145-108">API Winsock 2 больше не поддерживает псуедоблоккинг, но поскольку оболочки совместимости Windows Sockets 1,1 должны продолжать эмуляцию этого поведения, поставщики услуг должны поддерживать это, как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="09145-108">The Winsock 2 API no longer supports psuedoblocking, but because the Windows Sockets 1.1 compatibility shims must continue to emulate this behavior, service providers must support this as described in the following.</span></span>

 

 



