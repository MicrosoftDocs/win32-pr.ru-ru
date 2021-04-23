---
description: Для каждого приложения, использующего хранилище политик авторизации, необходимо создать объект Иазаппликатион, а затем сохранить его в хранилище политик.
ms.assetid: 5df964de-e5b6-427e-b859-efb5866f1578
title: Создание объекта приложения в скрипте
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0a4852ef0c06d721f9409c000989895f6767eb9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811272"
---
# <a name="creating-an-application-object-in-script"></a><span data-ttu-id="8905d-103">Создание объекта приложения в скрипте</span><span class="sxs-lookup"><span data-stu-id="8905d-103">Creating an Application Object in Script</span></span>

<span data-ttu-id="8905d-104">Хранилище политик авторизации содержит сведения о политике авторизации для одного или нескольких приложений.</span><span class="sxs-lookup"><span data-stu-id="8905d-104">An authorization policy store contains authorization policy information for one or more applications.</span></span> <span data-ttu-id="8905d-105">Для каждого приложения, использующего хранилище политик авторизации, необходимо создать объект [**иазаппликатион**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) и сохранить его в хранилище политик.</span><span class="sxs-lookup"><span data-stu-id="8905d-105">For each application that uses an authorization policy store, you must create an [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) object and save it to a policy store.</span></span>

<span data-ttu-id="8905d-106">В следующем примере показано, как создать объект [**иазаппликатион**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) , представляющий приложение, и как добавить объект **иазаппликатион** в хранилище политик авторизации, используемое приложением.</span><span class="sxs-lookup"><span data-stu-id="8905d-106">The following example shows how to create an [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) object that represents an application and how to add the **IAzApplication** object to the authorization policy store the application uses.</span></span> <span data-ttu-id="8905d-107">В этом примере предполагается, что существует хранилище политик XML с именем MyStore.xml в корневом каталоге диска C.</span><span class="sxs-lookup"><span data-stu-id="8905d-107">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C.</span></span>


```VB
'  Create the AzAuthorizationStore object.
Dim AzManStore
Set AzManStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the authorization store.
AzManStore.Initialize 2, "msxml://C:\MyStore.xml"

'  Create an application object in the store.
Dim expenseApp
Set expenseApp= AzManStore.CreateApplication("Expense")

'  Save changes to the store.
expenseApp.Submit
```



 

 



