---
title: Наследование и делегирование администрирования
description: Описывает AD DS поддержку наследования разрешений вниз по дереву объектов, а также наследование для конкретного объекта.
ms.assetid: db9cf8d9-6831-4456-b2a5-9f5b4f3e9100
ms.tgt_platform: multiple
keywords:
- наследование и делегирование администрирования Active Directory
- Active Directory Active Directory, наследование разрешений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d76db80497b54e71c806f3ccff9df549f9b2c1a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104252776"
---
# <a name="inheritance-and-delegation-of-administration"></a><span data-ttu-id="cf572-105">Наследование и делегирование администрирования</span><span class="sxs-lookup"><span data-stu-id="cf572-105">Inheritance and Delegation of Administration</span></span>

<span data-ttu-id="cf572-106">Службы домен Active Directory Services поддерживают наследование разрешений вниз по дереву объектов, чтобы обеспечить выполнение задач администрирования на более высоких уровнях дерева.</span><span class="sxs-lookup"><span data-stu-id="cf572-106">Active Directory Domain Services supports the inheritance of permissions down the object tree to allow administration tasks to be performed at higher levels in the tree.</span></span> <span data-ttu-id="cf572-107">Это позволяет администраторам настраивать наследуемые разрешения на объекты, расположенные в корне, например в домене и подразделениях, и иметь эти разрешения, распределенные по различным объектам в дереве.</span><span class="sxs-lookup"><span data-stu-id="cf572-107">This enables administrators to set up inheritable permissions on objects near the root, such as domain and organizational units, and have those permissions distributed to various objects in the tree.</span></span>

<span data-ttu-id="cf572-108">Наследование может быть задано для отдельных элементов управления доступом.</span><span class="sxs-lookup"><span data-stu-id="cf572-108">Inheritance can be set on a per-ACE basis.</span></span> <span data-ttu-id="cf572-109">В следующей таблице перечислены флаги, которые можно указать в **AceFlags** , чтобы управлять наследованием элемента управления доступом.</span><span class="sxs-lookup"><span data-stu-id="cf572-109">The following table lists flags that can be specified in the **AceFlags** to control inheritance of the ACE.</span></span>



| <span data-ttu-id="cf572-110">Flag</span><span class="sxs-lookup"><span data-stu-id="cf572-110">Flag</span></span>                                                     | <span data-ttu-id="cf572-111">Описание</span><span class="sxs-lookup"><span data-stu-id="cf572-111">Description</span></span>                                                                                                                                     |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf572-112">**ADS \_ ацефлаг \_ наследовать \_ ACE**</span><span class="sxs-lookup"><span data-stu-id="cf572-112">**ADS\_ACEFLAG\_INHERIT\_ACE**</span></span><br/>                | <span data-ttu-id="cf572-113">Приводит к наследованию элемента управления доступом в дереве.</span><span class="sxs-lookup"><span data-stu-id="cf572-113">Causes the ACE to be inherited down in the tree.</span></span><br/>                                                                                     |
| <span data-ttu-id="cf572-114">**ADS \_ ацефлаг \_ без \_ распространения \_ наследования \_ ACE**</span><span class="sxs-lookup"><span data-stu-id="cf572-114">**ADS\_ACEFLAG\_NO\_PROPAGATE\_INHERIT\_ACE**</span></span><br/> | <span data-ttu-id="cf572-115">Приводит к тому, что ACE наследуется только на один уровень в дереве.</span><span class="sxs-lookup"><span data-stu-id="cf572-115">Causes the ACE to be inherited down only one level in the tree.</span></span><br/>                                                                      |
| <span data-ttu-id="cf572-116">**ADS \_ ацефлаг \_ наследует \_ только \_ ACE**</span><span class="sxs-lookup"><span data-stu-id="cf572-116">**ADS\_ACEFLAG\_INHERIT\_ONLY\_ACE**</span></span><br/>          | <span data-ttu-id="cf572-117">Приводит к тому, что ACE игнорируется для объекта, в котором он указан, наследуется только вниз и должен быть эффективным, где он унаследован.</span><span class="sxs-lookup"><span data-stu-id="cf572-117">Causes the ACE to be ignored on the object it is specified on, only be inherited down, and be effective where it has been inherited.</span></span><br/> |



 

<span data-ttu-id="cf572-118">Помимо настройки наследования, службы домен Active Directory Services поддерживают наследование для конкретного объекта.</span><span class="sxs-lookup"><span data-stu-id="cf572-118">In addition to setting inheritance, Active Directory Domain Services supports object-specific inheritance.</span></span> <span data-ttu-id="cf572-119">Это позволяет наследовать наследование ACE вниз по дереву, но оно должно действовать только для определенного типа объекта.</span><span class="sxs-lookup"><span data-stu-id="cf572-119">This allows the inheritable ACEs to be inherited down the tree, but be effective only on a specific type of object.</span></span> <span data-ttu-id="cf572-120">Это чрезвычайно полезно при делегировании администрирования.</span><span class="sxs-lookup"><span data-stu-id="cf572-120">This is extremely useful in delegating administration.</span></span> <span data-ttu-id="cf572-121">Например, это можно использовать для установки наследуемого объекта ACE в подразделении, который позволяет группе иметь полный контроль над всеми объектами-пользователями в подразделении, но ничего другого.</span><span class="sxs-lookup"><span data-stu-id="cf572-121">For example, this can be used to set an object-specific inheritable ACE at an organizational unit that enables a group to have full control on all user objects in the organizational unit, but nothing else.</span></span> <span data-ttu-id="cf572-122">Таким образом, Управление пользователями в этом подразделении становится делегировано пользователям в этой группе.</span><span class="sxs-lookup"><span data-stu-id="cf572-122">Thereby, the management of users in that organizational unit gets delegated to the users in that group.</span></span>

### <a name="delegating-service-administration-with-security-groups"></a><span data-ttu-id="cf572-123">Делегирование администрирования службы с группами безопасности</span><span class="sxs-lookup"><span data-stu-id="cf572-123">Delegating Service Administration with Security Groups</span></span>

<span data-ttu-id="cf572-124">Используйте группы безопасности для определения и делегирования административных ролей, связанных с сервером приложений.</span><span class="sxs-lookup"><span data-stu-id="cf572-124">Use Security groups to define and delegate administrative roles associated with your application server.</span></span> <span data-ttu-id="cf572-125">Например, ваша служба может быть связана с группой администраторов MyService.</span><span class="sxs-lookup"><span data-stu-id="cf572-125">For example, your service may be associated with a group MyService Administrators.</span></span> <span data-ttu-id="cf572-126">Пользователи, которые определены как администраторы MyService, будут добавлены в группу администраторов MyService.</span><span class="sxs-lookup"><span data-stu-id="cf572-126">Users who are identified as the MyService administrators will be added to MyService Administrators group.</span></span> <span data-ttu-id="cf572-127">Программа установки для MyService может установить списки управления доступом в каталоге, чтобы позволить администраторам MyService достаточные разрешения на чтение и запись атрибутов MyService или создание объектов, относящихся к MyService, например.</span><span class="sxs-lookup"><span data-stu-id="cf572-127">The setup program for MyService can set ACLs on the directory to enable MyService Administrators sufficient permissions to read/write MyService-related attributes or create MyService-specific objects for example.</span></span>

### <a name="roles-in-security-groups-for-computers-running-your-service"></a><span data-ttu-id="cf572-128">Роли в группах безопасности для компьютеров, на которых выполняется служба</span><span class="sxs-lookup"><span data-stu-id="cf572-128">Roles in Security Groups for Computers Running Your Service</span></span>

<span data-ttu-id="cf572-129">Используйте группы безопасности, чтобы определить набор компьютеров, которым предоставлен доступ к объектам службы в каталоге.</span><span class="sxs-lookup"><span data-stu-id="cf572-129">Use security groups to define the set of computers that are granted access to your service's objects in the directory.</span></span> <span data-ttu-id="cf572-130">Например, ваша служба может быть связана с серверами группы MyService.</span><span class="sxs-lookup"><span data-stu-id="cf572-130">For example, your service may be associated with a group MyService Servers.</span></span> <span data-ttu-id="cf572-131">Все компьютеры, на которых выполняется сервер MyService, добавляются в группу серверов MyService, и этой группе может быть предоставлен доступ к частям каталога, где серверы MyService должны выполнять чтение и запись данных.</span><span class="sxs-lookup"><span data-stu-id="cf572-131">All computers running the MyService server are added to MyService Servers group and this group can then be given access to parts of the directory where MyService servers need to read/write data.</span></span> <span data-ttu-id="cf572-132">Программа установки MyService может установить списки управления доступом в каталоге, чтобы разрешить серверам MyService достаточные разрешения на чтение и запись атрибутов MyService или создание объектов, связанных с MyService, например.</span><span class="sxs-lookup"><span data-stu-id="cf572-132">The setup program for MyService can set ACLs on the directory to enable MyService Servers sufficient permissions to read/write MyService-related attributes or create MyService-specific objects for example.</span></span>

 

 





