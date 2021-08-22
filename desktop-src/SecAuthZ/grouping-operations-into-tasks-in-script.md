---
description: В диспетчере авторизации задача — это высокоуровневое действие, которое необходимо выполнить пользователям приложения.
ms.assetid: a266dde7-86f8-4537-99a5-be7142e765c6
title: Группирование операций в задачи в скрипте
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 29c7dedb9944a208e5ba128f0341a8cbde3e787056c099d527be8f79260c6f7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118913578"
---
# <a name="grouping-operations-into-tasks-in-script"></a>Группирование операций в задачи в скрипте

В диспетчере авторизации задача — это высокоуровневое действие, которое необходимо выполнить пользователям приложения. Задачи состоят из операций, которые являются функциями низкого уровня и методами приложения. Затем задача назначается ролям, которые должны выполнять эту задачу. Задача представлена объектом [**иазтаск**](/windows/desktop/api/Azroles/nn-azroles-iaztask) . Дополнительные сведения об операциях и задачах см. в разделе [операции и задачи](operations-and-tasks.md).

В следующем примере показано, как группировать операции для создания задачи. В этом примере предполагается, что существует хранилище политик XML с именем MyStore.xml в корневом каталоге диска C, что в этом хранилище содержится приложение с именем "расходы", которое содержит операции, определенные в разделе [Определение операций в скрипте](defining-operations-in-script.md).


```VB
'  Create the AzAuthorizationStore object.
Dim AzManStore
Set AzManStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the authorization store.
AzManStore.Initialize 2, "msxml://C:\MyStore.xml"

'  Create an application object in the store.
Dim expenseApp
Set expenseApp= AzManStore.OpenApplication("Expense")

'  Create a task object.
Dim Task1
Set Task1 = expenseApp.CreateTask("Submit Expense")

'  Add operations to the task.
Task1.AddOperation CStr("RetrieveForm")
Task1.AddOperation CStr("EnqueRequest")
Task1.AddOperation Cstr("UseFormControl")

'  Save the task to the store.
Task1.Submit
```



 

 



