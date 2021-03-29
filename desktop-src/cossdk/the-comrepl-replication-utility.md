---
description: COMREPL — это служебная программа, которая будет выполнять репликацию каталога COM+ с данного исходного компьютера на один или несколько конечных компьютеров.
ms.assetid: 11aa7603-61f1-4af0-b6f9-81f484788052
title: Служебная программа репликации COMREPL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a08ecd77a679b6fc150e7a91fc0214eb829792dd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990718"
---
# <a name="the-comrepl-replication-utility"></a><span data-ttu-id="8a878-103">Служебная программа репликации COMREPL</span><span class="sxs-lookup"><span data-stu-id="8a878-103">The COMREPL Replication Utility</span></span>

<span data-ttu-id="8a878-104">COMREPL — это служебная программа, которая будет выполнять репликацию каталога COM+ с данного исходного компьютера на один или несколько конечных компьютеров.</span><span class="sxs-lookup"><span data-stu-id="8a878-104">COMREPL is a utility that will replicate the COM+ catalog from a given source computer to one or more target computers.</span></span> <span data-ttu-id="8a878-105">Представьте себе исходный компьютер, представляющий "главную конфигурацию".</span><span class="sxs-lookup"><span data-stu-id="8a878-105">Think of the source computer representing a "master configuration."</span></span> <span data-ttu-id="8a878-106">COMREPL используется для репликации этой основной конфигурации, чтобы поддерживать набор одинаково настроенных компьютеров.</span><span class="sxs-lookup"><span data-stu-id="8a878-106">COMREPL is used to replicate this master configuration to maintain a set of identically configured computers.</span></span>

<span data-ttu-id="8a878-107">Единица репликации — это полная конфигурация COM+ на главном компьютере.</span><span class="sxs-lookup"><span data-stu-id="8a878-107">The unit of replication is the entire COM+ configuration on the master computer.</span></span> <span data-ttu-id="8a878-108">Все приложения COM+ на главном компьютере реплицируются на конечные компьютеры. Это все или ничего.</span><span class="sxs-lookup"><span data-stu-id="8a878-108">All COM+ applications on the master are replicated to the target computers; it's all or nothing.</span></span> <span data-ttu-id="8a878-109">Кроме того, все приложения COM+, ранее установленные на конечных компьютерах, за исключением предустановленных приложений COM+, будут удалены в рамках процесса репликации.</span><span class="sxs-lookup"><span data-stu-id="8a878-109">In addition, all COM+ applications previously installed on the target computers, with the exception of the COM+ preinstalled applications, will be deleted as part of the replication process.</span></span>

<span data-ttu-id="8a878-110">COMREPL реплицирует только данные конфигурации COM+.</span><span class="sxs-lookup"><span data-stu-id="8a878-110">COMREPL replicates only COM+ configuration data.</span></span> <span data-ttu-id="8a878-111">К ним относятся приложения COM+ и параметры конкретного компьютера COM+.</span><span class="sxs-lookup"><span data-stu-id="8a878-111">This includes COM+ applications and COM+ specific computer settings.</span></span> <span data-ttu-id="8a878-112">Microsoft службы IIS (IIS) имеет аналогичную служебную программу (Ииссинк), которая использует COMREPL для репликации IIS и конфигурации COM+.</span><span class="sxs-lookup"><span data-stu-id="8a878-112">Microsoft Internet Information Services (IIS) has a similar utility (IISSync), which makes use of COMREPL to replicate IIS and COM+ configuration.</span></span>

<span data-ttu-id="8a878-113">Подробные сведения о запуске и использовании COMREPL см. в следующих подразделах этого раздела:</span><span class="sxs-lookup"><span data-stu-id="8a878-113">For detailed information on launching and using COMREPL, see the following topics in this section:</span></span>

-   [<span data-ttu-id="8a878-114">Использование COMREPL</span><span class="sxs-lookup"><span data-stu-id="8a878-114">Using COMREPL</span></span>](using-comrepl.md)
-   [<span data-ttu-id="8a878-115">Что реплицируется</span><span class="sxs-lookup"><span data-stu-id="8a878-115">What Gets Replicated</span></span>](what-gets-replicated.md)
-   [<span data-ttu-id="8a878-116">Этапы репликации</span><span class="sxs-lookup"><span data-stu-id="8a878-116">Replication Phases</span></span>](replication-phases.md)
-   [<span data-ttu-id="8a878-117">Управление файлами</span><span class="sxs-lookup"><span data-stu-id="8a878-117">File Management</span></span>](file-management.md)
-   [<span data-ttu-id="8a878-118">Ведение журнала и отчеты об ошибках</span><span class="sxs-lookup"><span data-stu-id="8a878-118">Logging and Error Reporting</span></span>](logging-and-error-reporting.md)

## <a name="related-topics"></a><span data-ttu-id="8a878-119">См. также</span><span class="sxs-lookup"><span data-stu-id="8a878-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a878-120">Создание пакетов установки для приложений COM+</span><span class="sxs-lookup"><span data-stu-id="8a878-120">Creating Installation Packages for COM+ Applications</span></span>](creating-installation-packages-for-com--applications.md)
</dt> <dt>

[<span data-ttu-id="8a878-121">Развертывание прокси приложения</span><span class="sxs-lookup"><span data-stu-id="8a878-121">Deploying Application Proxies</span></span>](deploying-application-proxies.md)
</dt> <dt>

[<span data-ttu-id="8a878-122">Каталог COM+</span><span class="sxs-lookup"><span data-stu-id="8a878-122">The COM+ Catalog</span></span>](the-com--catalog.md)
</dt> </dl>

 

 



