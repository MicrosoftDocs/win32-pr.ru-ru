---
description: Группа приложений — это группа пользователей и групп пользователей. Группа приложений может содержать другие группы приложений, поэтому группы пользователей могут быть вложенными. Группа приложений представляется объектом Иазаппликатионграуп.
ms.assetid: 9ec5b55e-3d66-44f6-9b59-a5e66192d8ac
title: Добавление пользователей в группу приложений в скрипте
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6fd92a69a236e6b4d04d5bb0a1a8b961c699d434
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651016"
---
# <a name="adding-users-to-an-application-group-in-script"></a><span data-ttu-id="138c7-105">Добавление пользователей в группу приложений в скрипте</span><span class="sxs-lookup"><span data-stu-id="138c7-105">Adding Users to an Application Group in Script</span></span>

<span data-ttu-id="138c7-106">В диспетчере авторизации группа приложений — это группа пользователей и групп пользователей.</span><span class="sxs-lookup"><span data-stu-id="138c7-106">In Authorization Manager, an application group is a group of users and user groups.</span></span> <span data-ttu-id="138c7-107">Группа приложений может содержать другие группы приложений, поэтому группы пользователей могут быть вложенными.</span><span class="sxs-lookup"><span data-stu-id="138c7-107">An application group can contain other application groups, so groups of users can be nested.</span></span> <span data-ttu-id="138c7-108">Группа приложений представляется объектом [**иазаппликатионграуп**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) .</span><span class="sxs-lookup"><span data-stu-id="138c7-108">An application group is represented by an [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) object.</span></span>

<span data-ttu-id="138c7-109">**Разрешение членам группы приложений выполнять задачу или набор задач**</span><span class="sxs-lookup"><span data-stu-id="138c7-109">**To allow members of an application group to perform a task or set of tasks**</span></span>

-   <span data-ttu-id="138c7-110">Назначьте эту группу приложений роли, которая содержит эти задачи.</span><span class="sxs-lookup"><span data-stu-id="138c7-110">Assign that application group to a role that contains those tasks.</span></span>

    <span data-ttu-id="138c7-111">Роли представлены объектами [**иазроле**](/windows/desktop/api/Azroles/nn-azroles-iazrole) .</span><span class="sxs-lookup"><span data-stu-id="138c7-111">Roles are represented by [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) objects.</span></span>

<span data-ttu-id="138c7-112">В следующем примере показано, как создать группу приложений, добавить пользователя в качестве члена группы приложений и назначить группу приложений существующей роли.</span><span class="sxs-lookup"><span data-stu-id="138c7-112">The following example shows how to create an application group, add a user as a member of the application group, and assign the application group to an existing role.</span></span> <span data-ttu-id="138c7-113">В этом примере предполагается, что существует хранилище политик XML с именем MyStore.xml в корневом каталоге диска C, которое содержит приложение с именем "расходы" и содержит роль с именем "Администратор расходов".</span><span class="sxs-lookup"><span data-stu-id="138c7-113">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C, that this store contains an application named Expense, and that this application contains a role named Expense Administrator.</span></span>


```VB
'  Create the AzAuthorizationStore object.
Dim AzManStore
Set AzManStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the authorization store.
AzManStore.Initialize 2, "msxml://C:\MyStore.xml"

'  Create an application object in the store.
Dim expenseApp
Set expenseApp= AzManStore.OpenApplication("Expense")

'  Create an application group object.
Dim appGroup
Set appGroup = expenseApp.CreateApplicationGroup("Approvers")

'  Add a member to the group.
'  Replace with valid domain and user name.
appGroup.AddMemberName("domain\\username")

'  Save information to the store.
appGroup.Submit

'  Open a role object.
Dim adminRole
Set adminRole = expenseApp.OpenRole("Expense Administrator")

'  Add the group to the role.
adminRole.AddAppMember("Approvers")

'  Save the information to the store.
adminRole.Submit
```



 

 



