---
description: Можно делегировать администрирование хранилищ политик авторизации, которые хранятся в Active Directory.
ms.assetid: a7b43dfe-f03e-4795-bbd3-746eb3449fd0
title: Делегирование определения разрешений в скрипте
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 69cf0793a48a572ec4b37cbf3634f65b04ff3565f3205bf0380c68914abb4530
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117782068"
---
# <a name="delegating-the-defining-of-permissions-in-script"></a>Делегирование определения разрешений в скрипте

Можно делегировать администрирование хранилищ политик авторизации, которые хранятся в Active Directory. Администрирование может быть делегировано пользователям и группам на уровне хранилища, приложения или области.

На каждом уровне имеется список администраторов и читателей. Администраторы хранилища, приложения или области могут читать и изменять хранилище политик на делегированном уровне. Читатели могут читать хранилище политик на делегированном уровне, но не изменять хранилище.

Пользователь или группа, которые являются либо администратором, либо средством чтения приложения, также должны быть добавлены в качестве делегированного пользователя хранилища политик, содержащего это приложение. Аналогичным образом пользователь или группа, являющиеся администратором или читательом области, должны быть добавлены в качестве делегированного пользователя приложения, содержащего эту область.

**Делегирование администрирования области**

1.  Добавьте пользователя или группу в список делегированных пользователей хранилища, содержащего область, вызвав метод [**аддделегатедполициусер**](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-adddelegatedpolicyuser) объекта [**азаусоризатионсторе**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) , содержащего область.
2.  Добавьте пользователя или группу в список делегированных пользователей приложения, которое содержит область, вызвав метод [**аддделегатедполициусер**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-adddelegatedpolicyuser) объекта [**иазаппликатион**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) , содержащего область.
3.  Добавьте пользователя или группу в список администраторов области, вызвав метод [**аддполициадминистратор**](/windows/desktop/api/Azroles/nf-azroles-iazscope-addpolicyadministrator) объекта [**иазскопе**](/windows/desktop/api/Azroles/nn-azroles-iazscope) .

> [!Note]  
> Хранилища политик на основе XML не поддерживают делегирование на любом уровне.

 

Если область в хранилище данных авторизации, хранящаяся в Active Directory, содержит определения задач, включающие правила авторизации или определения ролей, включающие правила авторизации, то область не может быть делегирована.

В следующем примере показано, как делегировать администрирование приложения. В этом примере предполагается, что в указанном расположении имеется хранилище политик авторизации Active Directory, которое содержит приложение с именем "расходы" и не содержит задач с сценариями бизнес-правил.


```VB
'  Create the AzAuthorizationStore object.
Dim AzManStore
Set AzManStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the authorization store.
AzManStore.Initialize 2, _
    "msldap://CN=MyStore,CN=Program Data,DC=authmanager,DC=com"

'  Create an application object in the store.
Dim expenseApp
Set expenseApp= AzManStore.OpenApplication("Expense")

'  Add a delegated policy user to the store.
AzManStore.AddDelegatedPolicyUserName("ExampleDomain\\UserName")

'  Add the user as an administrator of the application.
expenseApp.AddPolicyAdministratorName("ExampleDomain\\UserName")

'  Save changes to the store.
AzManStore.Submit
```



 

 



