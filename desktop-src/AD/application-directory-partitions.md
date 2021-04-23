---
title: Разделы каталога приложений
description: В Windows Server 2003 службы домен Active Directory Services поддерживают разделы каталога приложений.
ms.assetid: 55c47803-c1ee-4888-bb19-103374ec9719
ms.tgt_platform: multiple
keywords:
- Разделы каталога приложений AD
- Разделы каталога приложений AD, использование
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63a8e035231aa24569b6fad6d5a7e0e62eaa5a30
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104069819"
---
# <a name="application-directory-partitions"></a><span data-ttu-id="a02a1-105">Разделы каталога приложений</span><span class="sxs-lookup"><span data-stu-id="a02a1-105">Application Directory Partitions</span></span>

<span data-ttu-id="a02a1-106">В Windows Server 2003 службы домен Active Directory Services поддерживают разделы каталога приложений.</span><span class="sxs-lookup"><span data-stu-id="a02a1-106">In Windows Server 2003, Active Directory Domain Services support application directory partitions.</span></span> <span data-ttu-id="a02a1-107">Раздел каталога приложений может содержать иерархию объектов любого типа, за исключением субъектов безопасности, и может быть настроена для репликации на любой набор контроллеров домена в лесу.</span><span class="sxs-lookup"><span data-stu-id="a02a1-107">An application directory partition can contain a hierarchy of any type of objects, except security principals, and can be configured to replicate to any set of domain controllers in the forest.</span></span> <span data-ttu-id="a02a1-108">В отличие от раздела домена, раздел каталога приложений не требуется для репликации на все контроллеры домена в домене, и этот раздел может реплицироваться на контроллеры домена в разных доменах леса.</span><span class="sxs-lookup"><span data-stu-id="a02a1-108">Unlike a domain partition, an application directory partition is not required to replicate to all domain controllers in a domain and the partition can replicate to domain controllers in different domains of the forest.</span></span> <span data-ttu-id="a02a1-109">Дополнительные сведения о разделах каталога приложений см. в разделе [сведения о разделах каталога приложений](about-application-directory-partitions.md).</span><span class="sxs-lookup"><span data-stu-id="a02a1-109">For more information about application directory partitions, see [About Application Directory Partitions](about-application-directory-partitions.md).</span></span>

<span data-ttu-id="a02a1-110">Можно создать раздел каталога приложений.</span><span class="sxs-lookup"><span data-stu-id="a02a1-110">An application directory partition can be created.</span></span> <span data-ttu-id="a02a1-111">изменены и удалены с помощью стандартных операций ADSI, LDAP и [System. DirectoryServices](/dotnet/api/system.directoryservices) .</span><span class="sxs-lookup"><span data-stu-id="a02a1-111">modified and deleted using standard ADSI, LDAP and [System.DirectoryServices](/dotnet/api/system.directoryservices) operations.</span></span> <span data-ttu-id="a02a1-112">Контекст безопасности, необходимый для создания и изменения раздела каталога приложений, такой же, как и для создания раздела домена.</span><span class="sxs-lookup"><span data-stu-id="a02a1-112">The security context required to create and modify an application directory partition is the same as that for creating a domain partition.</span></span>

<span data-ttu-id="a02a1-113">В следующих разделах описывается работа с разделами каталога приложений.</span><span class="sxs-lookup"><span data-stu-id="a02a1-113">The following topics describe how to work with application directory partitions:</span></span>

-   [<span data-ttu-id="a02a1-114">Репликация разделов каталога приложений</span><span class="sxs-lookup"><span data-stu-id="a02a1-114">Application Directory Partition Replication</span></span>](application-directory-partition-replication.md)
-   [<span data-ttu-id="a02a1-115">Безопасность раздела каталога приложений</span><span class="sxs-lookup"><span data-stu-id="a02a1-115">Application Directory Partition Security</span></span>](application-directory-partition-security.md)
-   [<span data-ttu-id="a02a1-116">Создание раздела каталога приложений</span><span class="sxs-lookup"><span data-stu-id="a02a1-116">Creating an Application Directory Partition</span></span>](creating-an-application-directory-partition.md)
-   [<span data-ttu-id="a02a1-117">Удаление раздела каталога приложений</span><span class="sxs-lookup"><span data-stu-id="a02a1-117">Deleting an Application Directory Partition</span></span>](deleting-an-application-directory-partition.md)
-   [<span data-ttu-id="a02a1-118">Перечисление разделов каталога приложений в лесу</span><span class="sxs-lookup"><span data-stu-id="a02a1-118">Enumerating Application Directory Partitions in a Forest</span></span>](enumerating-application-directory-partitions-in-a-forest.md)
-   [<span data-ttu-id="a02a1-119">Поиск сервера узла раздела каталога приложений</span><span class="sxs-lookup"><span data-stu-id="a02a1-119">Locating an Application Directory Partition Host Server</span></span>](locating-an-application-directory-partition-host-server.md)
-   [<span data-ttu-id="a02a1-120">Добавление или удаление реплики раздела каталога приложений</span><span class="sxs-lookup"><span data-stu-id="a02a1-120">Adding or Deleting an Application Directory Partition Replica</span></span>](adding-or-deleting-an-application-directory-partition-replica.md)
-   [<span data-ttu-id="a02a1-121">Перечисление реплик раздела каталога приложений</span><span class="sxs-lookup"><span data-stu-id="a02a1-121">Enumerating Replicas of an Application Directory Partition</span></span>](enumerating-replicas-of-an-application-directory-partition.md)
-   [<span data-ttu-id="a02a1-122">Изменение конфигурации раздела каталога приложений</span><span class="sxs-lookup"><span data-stu-id="a02a1-122">Modifying Application Directory Partition Configuration</span></span>](modifying-application-directory-partition-configuration.md)

 

 