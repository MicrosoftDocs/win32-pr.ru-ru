---
description: Диспетчер ресурсов запускается как доверенная служба в одном процессе. Все запросы на доступ к смарт-карте выполняются в диспетчере ресурсов, который направляет их в средство чтения, содержащее целевую карту.
ms.assetid: 4a62588a-14d9-43dc-9572-25a9cbcd0efd
title: Реализация диспетчер ресурсов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04ec653f999b74bb9851893b11e1fa49120a7bd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650764"
---
# <a name="resource-manager-implementation"></a><span data-ttu-id="bd008-104">Реализация диспетчер ресурсов</span><span class="sxs-lookup"><span data-stu-id="bd008-104">Resource Manager Implementation</span></span>

<span data-ttu-id="bd008-105">[*Диспетчер ресурсов*](../secgloss/r-gly.md) запускается как доверенная служба в одном процессе.</span><span class="sxs-lookup"><span data-stu-id="bd008-105">The [*resource manager*](../secgloss/r-gly.md) runs as a trusted service in a single process.</span></span> <span data-ttu-id="bd008-106">Все запросы на доступ к [*смарт-карте*](../secgloss/s-gly.md) выполняются в диспетчере ресурсов, который направляет их в [*средство чтения*](../secgloss/r-gly.md) , содержащее целевую карту.</span><span class="sxs-lookup"><span data-stu-id="bd008-106">All requests for [*smart card*](../secgloss/s-gly.md) access are made to the resource manager, which routes them to the [*reader*](../secgloss/r-gly.md) that contains the targeted card.</span></span>

<span data-ttu-id="bd008-107">Смарт-карты часто используются совместно с безопасностью и личной конфиденциальностью.</span><span class="sxs-lookup"><span data-stu-id="bd008-107">Smart cards are often used in conjunction with security and personal privacy.</span></span> <span data-ttu-id="bd008-108">Там, где это возможно, диспетчер ресурсов использует механизмы безопасности, существующие в базовой операционной системе, при доступе к модулю чтения или смарт-карте.</span><span class="sxs-lookup"><span data-stu-id="bd008-108">Wherever possible, the resource manager uses the security mechanisms existing within the underlying operating system when accessing a reader or smart card.</span></span>

 

 
