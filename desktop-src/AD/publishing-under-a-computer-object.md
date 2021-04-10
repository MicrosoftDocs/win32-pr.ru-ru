---
title: Публикация в объекте компьютера
description: Как правило, службы на основе узла создают запрашивая в объекте Computer для главного компьютера. Службы на основе узлов тесно связаны с одним ведущим компьютером.
ms.assetid: ecd7d8bc-4714-408a-856c-7cab8360bf81
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77fe382001910f3b78b4461c622e94b14c54fb59
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "103890387"
---
# <a name="publishing-under-a-computer-object"></a><span data-ttu-id="3ad4d-104">Публикация в объекте компьютера</span><span class="sxs-lookup"><span data-stu-id="3ad4d-104">Publishing Under a Computer Object</span></span>

<span data-ttu-id="3ad4d-105">Как правило, службы на основе узла создают запрашивая в объекте Computer для главного компьютера.</span><span class="sxs-lookup"><span data-stu-id="3ad4d-105">Typically, host-based services create SCPs under the computer object for the host computer.</span></span> <span data-ttu-id="3ad4d-106">Службы на основе узлов тесно связаны с одним ведущим компьютером.</span><span class="sxs-lookup"><span data-stu-id="3ad4d-106">Host-based services are services closely tied to a single host computer.</span></span>

<span data-ttu-id="3ad4d-107">**Создание запрашивая в объекте Computer**</span><span class="sxs-lookup"><span data-stu-id="3ad4d-107">**To create SCPs under a computer object**</span></span>

1.  <span data-ttu-id="3ad4d-108">Вызовите функцию [**жеткомпутеробжектнаме**](/windows/desktop/api/secext/nf-secext-getcomputerobjectnamea) , чтобы получить различающееся имя (DN) в каталоге объекта компьютера для локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="3ad4d-108">Call the [**GetComputerObjectName**](/windows/desktop/api/secext/nf-secext-getcomputerobjectnamea) function to get the distinguished name (DN) in the directory of the computer object for the local computer.</span></span>
2.  <span data-ttu-id="3ad4d-109">Используйте это различающееся имя для привязки к объекту Computer и создания точки подключения службы.</span><span class="sxs-lookup"><span data-stu-id="3ad4d-109">Use that DN to bind to the computer object and create the SCP.</span></span>

<span data-ttu-id="3ad4d-110">Дополнительные сведения и пример кода см. в разделе [как клиенты находят и используют точку подключения службы](how-clients-find-and-use-a-service-connection-point.md).</span><span class="sxs-lookup"><span data-stu-id="3ad4d-110">For more information and a code example, see [How Clients Find and Use a Service Connection Point](how-clients-find-and-use-a-service-connection-point.md).</span></span>

<span data-ttu-id="3ad4d-111">Имейте в виду, что только компьютеры, являющиеся членами домена, имеют допустимые объекты компьютеров в каталоге.</span><span class="sxs-lookup"><span data-stu-id="3ad4d-111">Be aware that only domain-member computers have valid computer objects in the directory.</span></span>

<span data-ttu-id="3ad4d-112">Чтобы получить имя DNS или NetBIOS локального компьютера, вызовите функцию [**предполагался сбой getcomputernameex**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) .</span><span class="sxs-lookup"><span data-stu-id="3ad4d-112">To get the DNS or NetBIOS name of the local computer, call the [**GetComputerNameEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) function.</span></span>

 

 