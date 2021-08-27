---
description: Чтобы установить клиентский контекст в скрипте, приложение может создать клиентский контекст с дескриптором для маркера, именем домена и пользователя или строковым представлением идентификатора безопасности клиента.
ms.assetid: 94fb79e4-7e9f-4fef-8ca5-b2000a92efab
title: Установка контекста клиента в скрипте
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 05a8ea51efa427c83e78c35806175712b3c6d0d66e0987909f98e23a081415e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118913740"
---
# <a name="establishing-a-client-context-in-script"></a>Установка контекста клиента в скрипте

В диспетчере авторизации приложение определяет, получает ли клиент доступ к операции, вызывая метод [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) объекта [**иазклиентконтекст**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) , который представляет контекст клиента.

Приложение может создать клиентский контекст с маркером, именем домена и пользователя или строковым представлением [*идентификатора безопасности*](/windows/desktop/SecGloss/s-gly) (SID) клиента.

Используйте методы [**инитиализеклиентконтекстфромтокен**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromtoken), [**инитиализеклиентконтекстфромнаме**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromname)и [**инитиализеклиентконтекстфромстрингсид**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromstringsid) объекта [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) для создания контекста клиента.

В следующем примере показано, как создать объект [**иазклиентконтекст**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) на основе имени клиента. В этом примере предполагается, что существует хранилище политик XML с именем MyStore.xml в корневом каталоге диска C и что это хранилище содержит приложение с именем "расходы".


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

%>
```



 

 
