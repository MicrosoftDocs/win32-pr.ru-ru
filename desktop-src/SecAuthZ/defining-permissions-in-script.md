---
description: Инструкции по использованию API диспетчера авторизации для определения разрешений в скрипте путем создания хранилища политик авторизации.
ms.assetid: 114426e8-03a7-41e2-96c9-e2da91aa7d84
title: Определение разрешений в скрипте
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e16f377ffa669da0b686ac28783e9a370efec94d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999088"
---
# <a name="defining-permissions-in-script"></a><span data-ttu-id="f4ff6-103">Определение разрешений в скрипте</span><span class="sxs-lookup"><span data-stu-id="f4ff6-103">Defining Permissions in Script</span></span>

<span data-ttu-id="f4ff6-104">В диспетчере авторизации вы определяете, какие пользователи имеют доступ к ресурсам приложения, создавая хранилище политик авторизации.</span><span class="sxs-lookup"><span data-stu-id="f4ff6-104">In Authorization Manager, you define which users have access to which application resources by creating an authorization policy store.</span></span>

<span data-ttu-id="f4ff6-105">**Определение разрешений на доступ**</span><span class="sxs-lookup"><span data-stu-id="f4ff6-105">**To define access permissions**</span></span>

1.  <span data-ttu-id="f4ff6-106">Создайте хранилище, в котором определена политика авторизации:</span><span class="sxs-lookup"><span data-stu-id="f4ff6-106">Create the store where the authorization policy is defined:</span></span><dl>

[<span data-ttu-id="f4ff6-107">Создание хранилища политики авторизации в скрипте</span><span class="sxs-lookup"><span data-stu-id="f4ff6-107">Creating an Authorization Policy Store in Script</span></span>](creating-an-authorization-policy-store-object-in-script.md)  
    </dl>
2.  <span data-ttu-id="f4ff6-108">Создайте раздел в хранилище политик авторизации для определенного приложения:</span><span class="sxs-lookup"><span data-stu-id="f4ff6-108">Create a section in the authorization policy store for a specific application:</span></span><dl>

[<span data-ttu-id="f4ff6-109">Создание объекта приложения в скрипте</span><span class="sxs-lookup"><span data-stu-id="f4ff6-109">Creating an Application Object in Script</span></span>](creating-an-application-object-in-script.md)  
    </dl>
3.  <span data-ttu-id="f4ff6-110">Определение операций, реализуемых приложением для доступа к ресурсам и их изменения:</span><span class="sxs-lookup"><span data-stu-id="f4ff6-110">Define operations that the application implements to access and modify resources:</span></span><dl>

[<span data-ttu-id="f4ff6-111">Определение операций в скрипте</span><span class="sxs-lookup"><span data-stu-id="f4ff6-111">Defining Operations in Script</span></span>](defining-operations-in-script.md)  
    </dl>
4.  <span data-ttu-id="f4ff6-112">Сгруппируйте операции по задачам высокого уровня, которые пользователи хотят выполнить:</span><span class="sxs-lookup"><span data-stu-id="f4ff6-112">Group operations into high-level tasks that users want to perform:</span></span><dl>

[<span data-ttu-id="f4ff6-113">Группирование операций в задачи в скрипте</span><span class="sxs-lookup"><span data-stu-id="f4ff6-113">Grouping Operations into Tasks in Script</span></span>](grouping-operations-into-tasks-in-script.md)  
    </dl>
5.  <span data-ttu-id="f4ff6-114">Определите роли, состоящие из групп задач:</span><span class="sxs-lookup"><span data-stu-id="f4ff6-114">Define roles that consist of groups of tasks:</span></span><dl>

[<span data-ttu-id="f4ff6-115">Группирование задач в роли в скрипте</span><span class="sxs-lookup"><span data-stu-id="f4ff6-115">Grouping Tasks into Roles in Script</span></span>](grouping-tasks-into-roles-in-script.md)  
    </dl><span data-ttu-id="f4ff6-116">Пользователь, назначенный роли, имеет разрешение на выполнение любой задачи, назначенной этой роли.</span><span class="sxs-lookup"><span data-stu-id="f4ff6-116">A user that is assigned to a role has permission to perform any task assigned to that role.</span></span>
6.  <span data-ttu-id="f4ff6-117">Создание скриптов для определения доступа к задачам во время выполнения:</span><span class="sxs-lookup"><span data-stu-id="f4ff6-117">Create scripts to qualify access to tasks at run time:</span></span><dl>

[<span data-ttu-id="f4ff6-118">Уточнение доступа с помощью бизнес-логики в скрипте</span><span class="sxs-lookup"><span data-stu-id="f4ff6-118">Qualifying Access with Business Logic in Script</span></span>](qualifying-access-with-business-logic-in-script.md)  
    </dl><span data-ttu-id="f4ff6-119">Это необязательный шаг.</span><span class="sxs-lookup"><span data-stu-id="f4ff6-119">This step is optional.</span></span>
7.  <span data-ttu-id="f4ff6-120">Определите группы пользователей:</span><span class="sxs-lookup"><span data-stu-id="f4ff6-120">Define groups of users:</span></span><dl>

[<span data-ttu-id="f4ff6-121">Определение групп пользователей в сценарии</span><span class="sxs-lookup"><span data-stu-id="f4ff6-121">Defining Groups of Users in Script</span></span>](defining-groups-of-users-in-script.md)  
    </dl><span data-ttu-id="f4ff6-122">Затем эти группы можно назначить ролям, чтобы определить, какие задачи они могут выполнять.</span><span class="sxs-lookup"><span data-stu-id="f4ff6-122">These groups can then be assigned to roles to determine which tasks they can perform.</span></span>
8.  <span data-ttu-id="f4ff6-123">Добавление пользователей в группы пользователей:</span><span class="sxs-lookup"><span data-stu-id="f4ff6-123">Add users to user groups:</span></span><dl>

[<span data-ttu-id="f4ff6-124">Добавление пользователей в группу приложений в скрипте</span><span class="sxs-lookup"><span data-stu-id="f4ff6-124">Adding Users to an Application Group in Script</span></span>](adding-users-to-an-application-group-in-script.md)  
    </dl>

 

 



