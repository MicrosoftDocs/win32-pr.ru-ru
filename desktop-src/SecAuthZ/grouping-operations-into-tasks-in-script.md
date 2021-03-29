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
ms.openlocfilehash: fb7fc1d4a84cd42dc0ae48af4fcbf02412b93337
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912448"
---
# <a name="grouping-operations-into-tasks-in-script"></a><span data-ttu-id="dd428-103">Группирование операций в задачи в скрипте</span><span class="sxs-lookup"><span data-stu-id="dd428-103">Grouping Operations into Tasks in Script</span></span>

<span data-ttu-id="dd428-104">В диспетчере авторизации задача — это высокоуровневое действие, которое необходимо выполнить пользователям приложения.</span><span class="sxs-lookup"><span data-stu-id="dd428-104">In Authorization Manager, a task is a high-level action that users of an application need to complete.</span></span> <span data-ttu-id="dd428-105">Задачи состоят из операций, которые являются функциями низкого уровня и методами приложения.</span><span class="sxs-lookup"><span data-stu-id="dd428-105">Tasks are made up of operations, which are low-level functions and methods of the application.</span></span> <span data-ttu-id="dd428-106">Затем задача назначается ролям, которые должны выполнять эту задачу.</span><span class="sxs-lookup"><span data-stu-id="dd428-106">A task is then assigned to those roles that must perform that task.</span></span> <span data-ttu-id="dd428-107">Задача представлена объектом [**иазтаск**](/windows/desktop/api/Azroles/nn-azroles-iaztask) .</span><span class="sxs-lookup"><span data-stu-id="dd428-107">A task is represented by an [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) object.</span></span> <span data-ttu-id="dd428-108">Дополнительные сведения об операциях и задачах см. в разделе [операции и задачи](operations-and-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="dd428-108">For more information about operations and tasks, see [Operations and Tasks](operations-and-tasks.md).</span></span>

<span data-ttu-id="dd428-109">В следующем примере показано, как группировать операции для создания задачи.</span><span class="sxs-lookup"><span data-stu-id="dd428-109">The following example shows how to group operations to create a task.</span></span> <span data-ttu-id="dd428-110">В этом примере предполагается, что существует хранилище политик XML с именем MyStore.xml в корневом каталоге диска C, что в этом хранилище содержится приложение с именем "расходы", которое содержит операции, определенные в разделе [Определение операций в скрипте](defining-operations-in-script.md).</span><span class="sxs-lookup"><span data-stu-id="dd428-110">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C, that this store contains an application named Expense, and that this application contains operations defined in the topic [Defining Operations in Script](defining-operations-in-script.md).</span></span>


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



 

 



