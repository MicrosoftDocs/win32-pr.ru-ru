---
title: Управление зоны DNS
description: Зона DNS — это база данных записей RR, которая соответствует части иерархического пространства имен DNS. Зоны DNS используются для определения того, какие DNS-серверы являются полномочными для разрешения запросов разрешения имен для определенного раздела иерархии DNS.
ms.assetid: d4aa94e0-36f7-4b97-8a0a-c677c8a826a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58c4cc991821f88076d3c3e9b2bfcbddc3ab662d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777960"
---
# <a name="managing-dns-zones"></a><span data-ttu-id="3ad20-104">Управление зоны DNS</span><span class="sxs-lookup"><span data-stu-id="3ad20-104">Managing DNS Zones</span></span>

<span data-ttu-id="3ad20-105">Зона DNS — это база данных записей RR, которая соответствует части иерархического пространства имен DNS.</span><span class="sxs-lookup"><span data-stu-id="3ad20-105">A DNS zone is a database of RR entries that corresponds to part of the DNS hierarchical name space.</span></span> <span data-ttu-id="3ad20-106">Зоны DNS используются для определения того, какие DNS-серверы являются полномочными для разрешения запросов разрешения имен для определенного раздела иерархии DNS.</span><span class="sxs-lookup"><span data-stu-id="3ad20-106">DNS zones are used to delineate which DNS Servers are authoritative for resolving name-resolution queries for a given section of the DNS hierarchy.</span></span>

## <a name="administration-steps"></a><span data-ttu-id="3ad20-107">Шаги администрирования</span><span class="sxs-lookup"><span data-stu-id="3ad20-107">Administration Steps</span></span>

<span data-ttu-id="3ad20-108">Поставщик WMI для DNS позволяет администрировать зоны DNS с самого полномочного DNS-сервера или с удаленных узлов.</span><span class="sxs-lookup"><span data-stu-id="3ad20-108">The DNS WMI Provider enables the administration of DNS zones from the authoritative DNS Server itself, or from remote hosts.</span></span> <span data-ttu-id="3ad20-109">Общие шаги, необходимые для администрирования зоны с помощью поставщика WMI DNS:</span><span class="sxs-lookup"><span data-stu-id="3ad20-109">The general steps necessary to administer a zone using the DNS WMI Provider are:</span></span>

-   <span data-ttu-id="3ad20-110">Подключение к поставщику WMI DNS</span><span class="sxs-lookup"><span data-stu-id="3ad20-110">Connecting to the DNS WMI Provider</span></span>
-   <span data-ttu-id="3ad20-111">Получение экземпляра зоны</span><span class="sxs-lookup"><span data-stu-id="3ad20-111">Getting a zone instance</span></span>
-   <span data-ttu-id="3ad20-112">Перечисление или изменение свойства зоны или с помощью метода</span><span class="sxs-lookup"><span data-stu-id="3ad20-112">Listing or modifying a zone property, or using a method</span></span>

<span data-ttu-id="3ad20-113">Следующие задачи связаны со связанными образцами сценариев:</span><span class="sxs-lookup"><span data-stu-id="3ad20-113">The following tasks are linked to their associated scripting samples:</span></span>

-   [<span data-ttu-id="3ad20-114">Создание зоны DNS</span><span class="sxs-lookup"><span data-stu-id="3ad20-114">Creating a DNS Zone</span></span>](dns-wmi-provider-samples-managing-dns-zones.md)
-   [<span data-ttu-id="3ad20-115">Изменение зоны DNS</span><span class="sxs-lookup"><span data-stu-id="3ad20-115">Modifying a DNS Zone</span></span>](dns-wmi-provider-samples-managing-dns-zones.md)
-   [<span data-ttu-id="3ad20-116">Удаление зоны DNS</span><span class="sxs-lookup"><span data-stu-id="3ad20-116">Deleting a DNS Zone</span></span>](dns-wmi-provider-samples-managing-dns-zones.md)
-   [<span data-ttu-id="3ad20-117">Добавление IP-адреса зоны</span><span class="sxs-lookup"><span data-stu-id="3ad20-117">Adding a Zone IP Address</span></span>](dns-wmi-provider-samples-managing-dns-zones.md)
-   [<span data-ttu-id="3ad20-118">Удаление IP-адреса зоны</span><span class="sxs-lookup"><span data-stu-id="3ad20-118">Deleting a Zone IP Address</span></span>](dns-wmi-provider-samples-managing-dns-zones.md)
-   [<span data-ttu-id="3ad20-119">Приостановка зоны</span><span class="sxs-lookup"><span data-stu-id="3ad20-119">Pausing a Zone</span></span>](dns-wmi-provider-samples-managing-dns-zones.md)
-   [<span data-ttu-id="3ad20-120">Возобновление зоны</span><span class="sxs-lookup"><span data-stu-id="3ad20-120">Resuming a Zone</span></span>](dns-wmi-provider-samples-managing-dns-zones.md)
-   [<span data-ttu-id="3ad20-121">Обновление зоны</span><span class="sxs-lookup"><span data-stu-id="3ad20-121">Updating a Zone</span></span>](dns-wmi-provider-samples-managing-dns-zones.md)
-   [<span data-ttu-id="3ad20-122">Перезагрузка зоны</span><span class="sxs-lookup"><span data-stu-id="3ad20-122">Reloading a Zone</span></span>](dns-wmi-provider-samples-managing-dns-zones.md)
-   [<span data-ttu-id="3ad20-123">Обновление зоны</span><span class="sxs-lookup"><span data-stu-id="3ad20-123">Refreshing a Zone</span></span>](dns-wmi-provider-samples-managing-dns-zones.md)

 

 




