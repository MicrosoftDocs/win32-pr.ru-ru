---
description: Роли служат двум разным целям в диспетчере авторизации.
ms.assetid: 6d045ecb-432e-4ba6-b5d2-37db82ab1884
title: Роли
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc65d140faa22c72d098c7a4ba2f13e952b2713f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897786"
---
# <a name="roles"></a><span data-ttu-id="7148e-103">Роли</span><span class="sxs-lookup"><span data-stu-id="7148e-103">Roles</span></span>

<span data-ttu-id="7148e-104">Роли служат двум разным целям в диспетчере авторизации.</span><span class="sxs-lookup"><span data-stu-id="7148e-104">Roles serve two different purposes in Authorization Manager.</span></span> <span data-ttu-id="7148e-105">Роль — это набор задач или операций, к которым Категория пользователей требует доступа, а также набор пользователей и групп, которые соответствуют этой категории.</span><span class="sxs-lookup"><span data-stu-id="7148e-105">A role is a set of tasks or operations to which a category of users requires access, and it is also a set of users and groups that fit into that category.</span></span>

-   [<span data-ttu-id="7148e-106">Роли в качестве наборов задач</span><span class="sxs-lookup"><span data-stu-id="7148e-106">Roles as Sets of Tasks</span></span>](#roles-as-sets-of-tasks)
-   [<span data-ttu-id="7148e-107">Роли в качестве наборов пользователей и групп</span><span class="sxs-lookup"><span data-stu-id="7148e-107">Roles as Sets of Users and Groups</span></span>](#roles-as-sets-of-users-and-groups)
-   [<span data-ttu-id="7148e-108">См. также</span><span class="sxs-lookup"><span data-stu-id="7148e-108">Related topics</span></span>](#related-topics)

## <a name="roles-as-sets-of-tasks"></a><span data-ttu-id="7148e-109">Роли в качестве наборов задач</span><span class="sxs-lookup"><span data-stu-id="7148e-109">Roles as Sets of Tasks</span></span>

<span data-ttu-id="7148e-110">Политика авторизации назначает объекты [**иазтаск**](/windows/desktop/api/Azroles/nn-azroles-iaztask) объекту [**иазроле**](/windows/desktop/api/Azroles/nn-azroles-iazrole) для создания наборов задач.</span><span class="sxs-lookup"><span data-stu-id="7148e-110">An authorization policy assigns [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) objects to an [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) object to create sets of tasks.</span></span> <span data-ttu-id="7148e-111">Все пользователи и группы, назначенные этому объекту **иазроле** , имеют разрешение на доступ ко всем операциям, содержащимся в этих объектах **иазтаск** .</span><span class="sxs-lookup"><span data-stu-id="7148e-111">All users and groups assigned to that **IAzRole** object then have permission to access all operations contained by those **IAzTask** objects.</span></span>

<span data-ttu-id="7148e-112">Так как объект [**иазроле**](/windows/desktop/api/Azroles/nn-azroles-iazrole) представляет как набор задач, так и набор пользователей и групп, имеющих доступ к этим задачам, диспетчер авторизации предоставляет способ создания определений ролей, которые могут быть назначены нескольким объектам **иазроле** .</span><span class="sxs-lookup"><span data-stu-id="7148e-112">Because an [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) object represents both a set of tasks and a set of users and groups that have access to those tasks, Authorization Manager provides a way to create role definitions that can be assigned to more than one **IAzRole** object.</span></span> <span data-ttu-id="7148e-113">Объект [**иазтаск**](/windows/desktop/api/Azroles/nn-azroles-iaztask) может содержать другие объекты **иазтаск** .</span><span class="sxs-lookup"><span data-stu-id="7148e-113">An [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) object can contain other **IAzTask** objects.</span></span> <span data-ttu-id="7148e-114">Затем можно использовать этот объект **иазтаск** в качестве определения роли, назначив его одному или нескольким объектам **иазроле** .</span><span class="sxs-lookup"><span data-stu-id="7148e-114">You can then use that **IAzTask** object as a role definition by assigning it to one or more **IAzRole** objects.</span></span> <span data-ttu-id="7148e-115">Задайте для свойства [**исроледефинитион**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_isroledefinition) объекта **иазтаск** **значение true** , чтобы пользовательский интерфейс оснастки MMC **диспетчера авторизации** отображал объект **иазтаск** в качестве роли.</span><span class="sxs-lookup"><span data-stu-id="7148e-115">Set the [**IsRoleDefinition**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_isroledefinition) property of the **IAzTask** object to **TRUE** to cause the **Authorization Manager** MMC snap-in user interface to display the **IAzTask** object as a role.</span></span>

## <a name="roles-as-sets-of-users-and-groups"></a><span data-ttu-id="7148e-116">Роли в качестве наборов пользователей и групп</span><span class="sxs-lookup"><span data-stu-id="7148e-116">Roles as Sets of Users and Groups</span></span>

<span data-ttu-id="7148e-117">Назначьте пользователей и группы объекту [**иазроле**](/windows/desktop/api/Azroles/nn-azroles-iazrole) , чтобы предоставить этим пользователям и группам доступ к задачам, назначенным этому объекту **иазроле** , вызвав метод [**аддмембер**](/windows/desktop/api/Azroles/nf-azroles-iazrole-addmember) или [**аддмембернаме**](/windows/desktop/api/Azroles/nf-azroles-iazrole-addmembername) .</span><span class="sxs-lookup"><span data-stu-id="7148e-117">Assign users and groups to an [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) object to grant those users and groups access to the tasks assigned to that **IAzRole** object by calling the [**AddMember**](/windows/desktop/api/Azroles/nf-azroles-iazrole-addmember) or [**AddMemberName**](/windows/desktop/api/Azroles/nf-azroles-iazrole-addmembername) method.</span></span> <span data-ttu-id="7148e-118">Назначьте существующие группы приложений, представленные объектами [**иазаппликатионграуп**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) , объекту **иазроле** , вызвав метод [**аддаппмембер**](/windows/desktop/api/Azroles/nf-azroles-iazrole-addappmember) .</span><span class="sxs-lookup"><span data-stu-id="7148e-118">Assign existing application groups, represented by [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) objects, to an **IAzRole** object by calling the [**AddAppMember**](/windows/desktop/api/Azroles/nf-azroles-iazrole-addappmember) method.</span></span> <span data-ttu-id="7148e-119">Все пользователи и группы, назначенные объекту **иазроле** , имеют доступ к задачам и операциям, назначенным этой роли.</span><span class="sxs-lookup"><span data-stu-id="7148e-119">All users and groups assigned to the **IAzRole** object have access to the tasks and operations assigned to that role.</span></span> <span data-ttu-id="7148e-120">Дополнительные сведения о группах приложений см. в разделе [Пользователи и группы](users-and-groups.md).</span><span class="sxs-lookup"><span data-stu-id="7148e-120">For more information about application groups, see [Users and Groups](users-and-groups.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7148e-121">См. также</span><span class="sxs-lookup"><span data-stu-id="7148e-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7148e-122">Группирование задач в роли в C++</span><span class="sxs-lookup"><span data-stu-id="7148e-122">Grouping Tasks into Roles in C++</span></span>](grouping-tasks-into-roles-in-c--.md)
</dt> <dt>

[<span data-ttu-id="7148e-123">Определение групп пользователей в C++</span><span class="sxs-lookup"><span data-stu-id="7148e-123">Defining Groups of Users in C++</span></span>](defining-groups-of-users-in-c--.md)
</dt> <dt>

[<span data-ttu-id="7148e-124">Добавление пользователей в группу приложений в C++</span><span class="sxs-lookup"><span data-stu-id="7148e-124">Adding Users to an Application Group in C++</span></span>](adding-users-to-an-application-group-in-c--.md)
</dt> </dl>

 

 



