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
# <a name="adding-users-to-an-application-group-in-script"></a>Добавление пользователей в группу приложений в скрипте

В диспетчере авторизации группа приложений — это группа пользователей и групп пользователей. Группа приложений может содержать другие группы приложений, поэтому группы пользователей могут быть вложенными. Группа приложений представляется объектом [**иазаппликатионграуп**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) .

**Разрешение членам группы приложений выполнять задачу или набор задач**

-   Назначьте эту группу приложений роли, которая содержит эти задачи.

    Роли представлены объектами [**иазроле**](/windows/desktop/api/Azroles/nn-azroles-iazrole) .

В следующем примере показано, как создать группу приложений, добавить пользователя в качестве члена группы приложений и назначить группу приложений существующей роли. В этом примере предполагается, что существует хранилище политик XML с именем MyStore.xml в корневом каталоге диска C, которое содержит приложение с именем "расходы" и содержит роль с именем "Администратор расходов".


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



 

 



