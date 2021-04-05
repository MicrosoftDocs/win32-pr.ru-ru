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
ms.openlocfilehash: 63c0381834a42d10a03b02ee949f8fe4bf7560bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911840"
---
# <a name="establishing-a-client-context-in-script"></a><span data-ttu-id="39720-103">Установка контекста клиента в скрипте</span><span class="sxs-lookup"><span data-stu-id="39720-103">Establishing a Client Context in Script</span></span>

<span data-ttu-id="39720-104">В диспетчере авторизации приложение определяет, получает ли клиент доступ к операции, вызывая метод [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) объекта [**иазклиентконтекст**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) , который представляет контекст клиента.</span><span class="sxs-lookup"><span data-stu-id="39720-104">In Authorization Manager, an application determines whether a client is given access to an operation by calling the [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) method of an [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) object, which represents a client context.</span></span>

<span data-ttu-id="39720-105">Приложение может создать клиентский контекст с маркером, именем домена и пользователя или строковым представлением [*идентификатора безопасности*](/windows/desktop/SecGloss/s-gly) (SID) клиента.</span><span class="sxs-lookup"><span data-stu-id="39720-105">An application can create a client context with a handle to a token, a domain and user name, or a string representation of the [*security identifier*](/windows/desktop/SecGloss/s-gly) (SID) of the client.</span></span>

<span data-ttu-id="39720-106">Используйте методы [**инитиализеклиентконтекстфромтокен**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromtoken), [**инитиализеклиентконтекстфромнаме**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromname)и [**инитиализеклиентконтекстфромстрингсид**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromstringsid) объекта [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) для создания контекста клиента.</span><span class="sxs-lookup"><span data-stu-id="39720-106">Use the [**InitializeClientContextFromToken**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromtoken), [**InitializeClientContextFromName**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromname), and [**InitializeClientContextFromStringSid**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromstringsid) methods of an [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) object to create a client context.</span></span>

<span data-ttu-id="39720-107">В следующем примере показано, как создать объект [**иазклиентконтекст**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) на основе имени клиента.</span><span class="sxs-lookup"><span data-stu-id="39720-107">The following example shows how to create an [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) object from a client name.</span></span> <span data-ttu-id="39720-108">В этом примере предполагается, что существует хранилище политик XML с именем MyStore.xml в корневом каталоге диска C и что это хранилище содержит приложение с именем "расходы".</span><span class="sxs-lookup"><span data-stu-id="39720-108">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C, and that this store contains an application named Expense.</span></span>


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



 

 
