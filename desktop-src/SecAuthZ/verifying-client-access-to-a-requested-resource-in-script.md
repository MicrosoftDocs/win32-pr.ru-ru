---
description: 'Вызовите метод Иазклиентконтекст:: AccessCheck, чтобы проверить, имеет ли клиент доступ к одной или нескольким операциям.'
ms.assetid: cf1070fe-3737-4ae6-a8ef-f0782418a1d5
title: Проверка клиентского доступа к запрошенным ресурсам в скрипте
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6d5c3940e38d8a9a8befa00b85ac9c3cd406c292
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663637"
---
# <a name="verifying-client-access-to-requested-resources-in-script"></a><span data-ttu-id="1ac7d-103">Проверка клиентского доступа к запрошенным ресурсам в скрипте</span><span class="sxs-lookup"><span data-stu-id="1ac7d-103">Verifying Client Access to Requested Resources in Script</span></span>

<span data-ttu-id="1ac7d-104">Вызовите метод [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) объекта [**иазклиентконтекст**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) , чтобы проверить, имеет ли клиент доступ к одной или нескольким операциям.</span><span class="sxs-lookup"><span data-stu-id="1ac7d-104">Call the [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) method of an [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) object to check whether the client has access to one or more operations.</span></span> <span data-ttu-id="1ac7d-105">Сведения о создании объекта **иазклиентконтекст** см. в разделе [Установка контекста клиента в скрипте](establishing-a-client-context-in-script.md).</span><span class="sxs-lookup"><span data-stu-id="1ac7d-105">For information about creating an **IAzClientContext** object, see [Establishing a Client Context in Script](establishing-a-client-context-in-script.md).</span></span>

<span data-ttu-id="1ac7d-106">У клиента может быть членство в нескольких ролях, и операция может быть назначена нескольким задачам, поэтому диспетчер авторизации проверяет все роли и задачи.</span><span class="sxs-lookup"><span data-stu-id="1ac7d-106">A client might have membership in more than one role, and an operation might be assigned to more than one task, so Authorization Manager checks for all roles and tasks.</span></span> <span data-ttu-id="1ac7d-107">Если любая роль, к которой принадлежит клиент, содержит любую задачу, содержащую операцию, предоставляется доступ к этой операции.</span><span class="sxs-lookup"><span data-stu-id="1ac7d-107">If any role to which the client belongs contains any task that contains an operation, access to that operation is granted.</span></span>

<span data-ttu-id="1ac7d-108">Чтобы проверить доступ только для одной роли, к которой принадлежит клиент, установите свойство [**ролефоракцессчекк**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-get_roleforaccesscheck) объекта [**иазклиентконтекст**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) .</span><span class="sxs-lookup"><span data-stu-id="1ac7d-108">To check access for only a single role to which the client belongs, set the [**RoleForAccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-get_roleforaccesscheck) property of the [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) object.</span></span>

<span data-ttu-id="1ac7d-109">При инициализации хранилища политик авторизации для проверки доступа необходимо передать нуль в качестве значения параметра *лфлагс* метода [**Initialize**](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-initialize) объекта [**азаусоризатионсторе**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) .</span><span class="sxs-lookup"><span data-stu-id="1ac7d-109">When initializing the authorization policy store for access check, you must pass zero as the value of the *lFlags* parameter of the [**Initialize**](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-initialize) method of the [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) object.</span></span>

<span data-ttu-id="1ac7d-110">Можно также применить бизнес-логику во время выполнения для квалификации доступа.</span><span class="sxs-lookup"><span data-stu-id="1ac7d-110">It is also possible to apply business logic at run time to qualify access.</span></span> <span data-ttu-id="1ac7d-111">Сведения о том, как получить доступ к бизнес-логике, см. [в разделе Уточнение доступа с помощью бизнес-логики в скрипте](qualifying-access-with-business-logic-in-script.md).</span><span class="sxs-lookup"><span data-stu-id="1ac7d-111">For information about qualifying access with business logic, see [Qualifying Access with Business Logic in Script](qualifying-access-with-business-logic-in-script.md).</span></span>

<span data-ttu-id="1ac7d-112">В следующем примере показано, как проверить доступ клиента к операции.</span><span class="sxs-lookup"><span data-stu-id="1ac7d-112">The following example shows how to check a client's access to an operation.</span></span> <span data-ttu-id="1ac7d-113">В этом примере предполагается, что существует хранилище политик XML с именем MyStore.xml в корневом каталоге диска C и что это хранилище содержит приложение с именем "расходы" и операцию с именем Усеформконтрол.</span><span class="sxs-lookup"><span data-stu-id="1ac7d-113">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C, and that this store contains an application named Expense and an operation named UseFormControl.</span></span>


```VB
<%@ Language=VBScript %>
<%
'  Create the AzAuthorizationStore object.
Dim AzManStore
Set AzManStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the authorization store.
AzManStore.Initialize 0, "msxml://C:\MyStore.xml"

'  Open the application object in the store.
Dim expenseApp
Set expenseApp = AzManStore.OpenApplication("Expense")

'  Create a client context.
Dim clientName
clientName = Request.ServerVariables("LOGON_USER")
Dim clientContext
Set clientContext = _
    expenseApp.InitializeClientContextFromName(clientName)

'  Open the operation to check.
Dim formOperation
Set formOperation = expenseApp.OpenOperation("UseFormControl")

'  Get the ID of the operation.
Dim operationID
operationID = formOperation.OperationID

'  Check access.
Dim Operations(1)
Operations(0) = operationID
Dim Results

Results = _
    clientContext.AccessCheck("UseFormControl", Empty, Operations)

%>
```



 

 



