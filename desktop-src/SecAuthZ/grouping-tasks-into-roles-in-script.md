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
# <a name="grouping-tasks-into-roles-in-script"></a>Группирование задач в роли в скрипте

В диспетчере авторизации роль представляет категорию пользователей и задачи, которые эти пользователи имеют право выполнять. Задачи группируются и назначаются в определение роли, которое представляется объектом [**иазтаск**](/windows/desktop/api/Azroles/nn-azroles-iaztask) со свойством [**исроледефинитион**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_isroledefinition) , установленным в **значение true**. Затем определение роли можно назначить объекту [**иазроле**](/windows/desktop/api/Azroles/nn-azroles-iazrole) , после чего пользователи или группы пользователей будут назначены этому объекту. Дополнительные сведения о задачах и ролях см. в разделе [роли](roles.md).

В следующем примере показано, как назначить задачи определению роли, создать объект роли и назначить определение роли объекту Role. В этом примере предполагается, что существует хранилище политик XML с именем MyStore.xml в корневом каталоге диска C, которое содержит приложение с именем расходы и содержит задачи с именем отправка расходов и утверждение расходов.


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



 

 



