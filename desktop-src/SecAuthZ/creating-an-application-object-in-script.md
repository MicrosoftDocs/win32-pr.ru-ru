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
ms.openlocfilehash: 02a5ada4a8a79244cc454d9efc88e69a5d9a205241119b5dda371699f0c86552
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117782550"
---
# <a name="creating-an-application-object-in-script"></a>Создание объекта приложения в скрипте

Хранилище политик авторизации содержит сведения о политике авторизации для одного или нескольких приложений. Для каждого приложения, использующего хранилище политик авторизации, необходимо создать объект [**иазаппликатион**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) и сохранить его в хранилище политик.

В следующем примере показано, как создать объект [**иазаппликатион**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) , представляющий приложение, и как добавить объект **иазаппликатион** в хранилище политик авторизации, используемое приложением. В этом примере предполагается, что существует хранилище политик XML с именем MyStore.xml в корневом каталоге диска C.


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



 

 



