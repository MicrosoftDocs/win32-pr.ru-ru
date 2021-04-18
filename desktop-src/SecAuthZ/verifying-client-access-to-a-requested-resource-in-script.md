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
# <a name="verifying-client-access-to-requested-resources-in-script"></a>Проверка клиентского доступа к запрошенным ресурсам в скрипте

Вызовите метод [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) объекта [**иазклиентконтекст**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) , чтобы проверить, имеет ли клиент доступ к одной или нескольким операциям. Сведения о создании объекта **иазклиентконтекст** см. в разделе [Установка контекста клиента в скрипте](establishing-a-client-context-in-script.md).

У клиента может быть членство в нескольких ролях, и операция может быть назначена нескольким задачам, поэтому диспетчер авторизации проверяет все роли и задачи. Если любая роль, к которой принадлежит клиент, содержит любую задачу, содержащую операцию, предоставляется доступ к этой операции.

Чтобы проверить доступ только для одной роли, к которой принадлежит клиент, установите свойство [**ролефоракцессчекк**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-get_roleforaccesscheck) объекта [**иазклиентконтекст**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) .

При инициализации хранилища политик авторизации для проверки доступа необходимо передать нуль в качестве значения параметра *лфлагс* метода [**Initialize**](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-initialize) объекта [**азаусоризатионсторе**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) .

Можно также применить бизнес-логику во время выполнения для квалификации доступа. Сведения о том, как получить доступ к бизнес-логике, см. [в разделе Уточнение доступа с помощью бизнес-логики в скрипте](qualifying-access-with-business-logic-in-script.md).

В следующем примере показано, как проверить доступ клиента к операции. В этом примере предполагается, что существует хранилище политик XML с именем MyStore.xml в корневом каталоге диска C и что это хранилище содержит приложение с именем "расходы" и операцию с именем Усеформконтрол.


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



 

 



