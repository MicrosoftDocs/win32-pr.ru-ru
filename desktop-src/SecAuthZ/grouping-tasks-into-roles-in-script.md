---
description: В диспетчере авторизации роль представляет категорию пользователей и задачи, которые эти пользователи могут выполнять.
ms.assetid: a4981774-0f5c-4032-8a7d-d9ef44c76abe
title: Группирование задач в роли в скрипте
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c84ec45bba8da9d76e2a4fe0b31324429374a74b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999298"
---
# <a name="grouping-tasks-into-roles-in-script"></a><span data-ttu-id="a3b60-103">Группирование задач в роли в скрипте</span><span class="sxs-lookup"><span data-stu-id="a3b60-103">Grouping Tasks into Roles in Script</span></span>

<span data-ttu-id="a3b60-104">В диспетчере авторизации роль представляет категорию пользователей и задачи, которые эти пользователи имеют право выполнять.</span><span class="sxs-lookup"><span data-stu-id="a3b60-104">In Authorization Manager, a role represents a category of users and the tasks those users are authorized to perform.</span></span> <span data-ttu-id="a3b60-105">Задачи группируются и назначаются в определение роли, которое представляется объектом [**иазтаск**](/windows/desktop/api/Azroles/nn-azroles-iaztask) со свойством [**исроледефинитион**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_isroledefinition) , установленным в **значение true**.</span><span class="sxs-lookup"><span data-stu-id="a3b60-105">Tasks are grouped together and assigned to a role definition, which is represented by an [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) object with its [**IsRoleDefinition**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_isroledefinition) property set to **True**.</span></span> <span data-ttu-id="a3b60-106">Затем определение роли можно назначить объекту [**иазроле**](/windows/desktop/api/Azroles/nn-azroles-iazrole) , после чего пользователи или группы пользователей будут назначены этому объекту.</span><span class="sxs-lookup"><span data-stu-id="a3b60-106">The role definition can then be assigned to an [**IAzRole**](/windows/desktop/api/Azroles/nn-azroles-iazrole) object, and users or groups of users are then assigned to that object.</span></span> <span data-ttu-id="a3b60-107">Дополнительные сведения о задачах и ролях см. в разделе [роли](roles.md).</span><span class="sxs-lookup"><span data-stu-id="a3b60-107">For more information about tasks and roles, see [Roles](roles.md).</span></span>

<span data-ttu-id="a3b60-108">В следующем примере показано, как назначить задачи определению роли, создать объект роли и назначить определение роли объекту Role.</span><span class="sxs-lookup"><span data-stu-id="a3b60-108">The following example shows how to assign tasks to a role definition, create a role object, and assign the role definition to the role object.</span></span> <span data-ttu-id="a3b60-109">В этом примере предполагается, что существует хранилище политик XML с именем MyStore.xml в корневом каталоге диска C, которое содержит приложение с именем расходы и содержит задачи с именем отправка расходов и утверждение расходов.</span><span class="sxs-lookup"><span data-stu-id="a3b60-109">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C, that this store contains an application named Expense, and that this application contains tasks named Submit Expense and Approve Expense.</span></span>


```VB
'  Create the AzAuthorizationStore object.
Dim AzManStore
Set AzManStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the authorization store.
AzManStore.Initialize 2, "msxml://C:\MyStore.xml"

'  Create an application object in the store.
Dim expenseApp
Set expenseApp = AzManStore.OpenApplication("Expense")

'  Create a task object to act as a role definition.
Dim roleTask
Set roleTask = expenseApp.CreateTask("Expense Admin")

'  Set the IsRoleDefinition property of roleTask to True.
roleTask.IsRoleDefinition = True

'  Add two tasks to the role definition.
roleTask.AddTask CStr("Submit Expense")
roleTask.AddTask CStr("Approve Expense")

'  Save the role definition to the store.
roleTask.Submit

'  Create a role object.
Dim role1
Set role1 = expenseApp.CreateRole("Expense Administrator")

'  Add the role definition to the role object.
role1.AddTask(roleTask.Name)

'  Save the role object to the store.
role1.Submit
```



 

 



