---
description: Инструкции по использованию API диспетчера авторизации для определения разрешений в C++ путем создания хранилища политик авторизации.
ms.assetid: 8a3bf625-7973-4905-a63c-e42e6682b7c2
title: Определение разрешений в C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc398d811f44b69dbde8d30f135fd4f30a552bbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651208"
---
# <a name="defining-permissions-in-c"></a><span data-ttu-id="525c0-103">Определение разрешений в C++</span><span class="sxs-lookup"><span data-stu-id="525c0-103">Defining Permissions in C++</span></span>

<span data-ttu-id="525c0-104">В диспетчере авторизации вы определяете, какие пользователи имеют доступ к ресурсам приложения, создавая хранилище политик авторизации.</span><span class="sxs-lookup"><span data-stu-id="525c0-104">In Authorization Manager, you define which users have access to which application resources by creating an authorization policy store.</span></span>

<span data-ttu-id="525c0-105">Дополнительные сведения об определении разрешений с помощью списков управления доступом см. [в разделе Определение разрешений с помощью ACL в C++](defining-permissions-with-acls-in-c--.md).</span><span class="sxs-lookup"><span data-stu-id="525c0-105">For information about defining permissions with ACLs, see [Defining Permissions with ACLs in C++](defining-permissions-with-acls-in-c--.md).</span></span>

<span data-ttu-id="525c0-106">**Определение разрешений на доступ**</span><span class="sxs-lookup"><span data-stu-id="525c0-106">**To define access permissions**</span></span>

1.  <span data-ttu-id="525c0-107">Создайте хранилище, в котором определена политика авторизации:</span><span class="sxs-lookup"><span data-stu-id="525c0-107">Create the store where the authorization policy is defined:</span></span><dl>

[<span data-ttu-id="525c0-108">Создание объекта хранилища политики авторизации в C++</span><span class="sxs-lookup"><span data-stu-id="525c0-108">Creating an Authorization Policy Store Object in C++</span></span>](creating-an-authorization-policy-store-object-in-c--.md)  
    </dl>
2.  <span data-ttu-id="525c0-109">Создайте раздел в хранилище политик авторизации для определенного приложения:</span><span class="sxs-lookup"><span data-stu-id="525c0-109">Create a section in the authorization policy store for a specific application:</span></span><dl>

[<span data-ttu-id="525c0-110">Создание объекта приложения на C++</span><span class="sxs-lookup"><span data-stu-id="525c0-110">Creating an Application Object in C++</span></span>](creating-an-application-object-in-c--.md)  
    </dl>
3.  <span data-ttu-id="525c0-111">Определение операций, реализуемых приложением для доступа к ресурсам и их изменения:</span><span class="sxs-lookup"><span data-stu-id="525c0-111">Define operations that the application implements to access and modify resources:</span></span><dl>

[<span data-ttu-id="525c0-112">Определение операций в C++</span><span class="sxs-lookup"><span data-stu-id="525c0-112">Defining Operations in C++</span></span>](defining-operations-in-c--.md)  
    </dl>
4.  <span data-ttu-id="525c0-113">Сгруппируйте операции по задачам высокого уровня, которые пользователи хотят выполнить:</span><span class="sxs-lookup"><span data-stu-id="525c0-113">Group operations into high-level tasks that users want to perform:</span></span><dl>

[<span data-ttu-id="525c0-114">Группирование операций в задачи на C++</span><span class="sxs-lookup"><span data-stu-id="525c0-114">Grouping Operations into Tasks in C++</span></span>](grouping-operations-into-tasks-in-c--.md)  
    </dl>
5.  <span data-ttu-id="525c0-115">Определите роли, состоящие из групп задач:</span><span class="sxs-lookup"><span data-stu-id="525c0-115">Define roles that consist of groups of tasks:</span></span><dl>

[<span data-ttu-id="525c0-116">Группирование задач в роли в C++</span><span class="sxs-lookup"><span data-stu-id="525c0-116">Grouping Tasks into Roles in C++</span></span>](grouping-tasks-into-roles-in-c--.md)  
    </dl><span data-ttu-id="525c0-117">Пользователь, назначенный роли, имеет разрешение на выполнение любой задачи, назначенной этой роли.</span><span class="sxs-lookup"><span data-stu-id="525c0-117">A user that is assigned to a role has permission to perform any task assigned to that role.</span></span>
6.  <span data-ttu-id="525c0-118">Создание скриптов для определения доступа к задачам во время выполнения:</span><span class="sxs-lookup"><span data-stu-id="525c0-118">Create scripts to qualify access to tasks at run time:</span></span><dl>

[<span data-ttu-id="525c0-119">Квалификация доступа с помощью бизнес-логики в C++</span><span class="sxs-lookup"><span data-stu-id="525c0-119">Qualifying Access with Business Logic in C++</span></span>](qualifying-access-with-business-logic-in-c--.md)  
    </dl><span data-ttu-id="525c0-120">Это необязательный шаг.</span><span class="sxs-lookup"><span data-stu-id="525c0-120">This step is optional.</span></span>
7.  <span data-ttu-id="525c0-121">Определите группы пользователей:</span><span class="sxs-lookup"><span data-stu-id="525c0-121">Define groups of users:</span></span><dl>

[<span data-ttu-id="525c0-122">Определение групп пользователей в C++</span><span class="sxs-lookup"><span data-stu-id="525c0-122">Defining Groups of Users in C++</span></span>](defining-groups-of-users-in-c--.md)  
    </dl><span data-ttu-id="525c0-123">Затем эти группы можно назначить ролям, чтобы определить, какие задачи они могут выполнять.</span><span class="sxs-lookup"><span data-stu-id="525c0-123">These groups can then be assigned to roles to determine which tasks they can perform.</span></span>
8.  <span data-ttu-id="525c0-124">Добавление пользователей в группы пользователей:</span><span class="sxs-lookup"><span data-stu-id="525c0-124">Add users to user groups:</span></span><dl>

[<span data-ttu-id="525c0-125">Добавление пользователей в группу приложений в C++</span><span class="sxs-lookup"><span data-stu-id="525c0-125">Adding Users to an Application Group in C++</span></span>](adding-users-to-an-application-group-in-c--.md)  
    </dl>

 

 



