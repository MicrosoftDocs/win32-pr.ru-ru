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
ms.openlocfilehash: a9569f82271642a610919db8246cc6389daba309
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346555"
---
# <a name="delegating-the-defining-of-permissions-in-script"></a><span data-ttu-id="14ee6-103">Делегирование определения разрешений в скрипте</span><span class="sxs-lookup"><span data-stu-id="14ee6-103">Delegating the Defining of Permissions in Script</span></span>

<span data-ttu-id="14ee6-104">Можно делегировать администрирование хранилищ политик авторизации, которые хранятся в Active Directory.</span><span class="sxs-lookup"><span data-stu-id="14ee6-104">You can delegate the administration of authorization policy stores that are stored in Active Directory.</span></span> <span data-ttu-id="14ee6-105">Администрирование может быть делегировано пользователям и группам на уровне хранилища, приложения или области.</span><span class="sxs-lookup"><span data-stu-id="14ee6-105">Administration can be delegated to users and groups at the store, application, or scope level.</span></span>

<span data-ttu-id="14ee6-106">На каждом уровне имеется список администраторов и читателей.</span><span class="sxs-lookup"><span data-stu-id="14ee6-106">At each level, there is a list of administrators and readers.</span></span> <span data-ttu-id="14ee6-107">Администраторы хранилища, приложения или области могут читать и изменять хранилище политик на делегированном уровне.</span><span class="sxs-lookup"><span data-stu-id="14ee6-107">Administrators of a store, application, or scope can read and modify the policy store at the delegated level.</span></span> <span data-ttu-id="14ee6-108">Читатели могут читать хранилище политик на делегированном уровне, но не изменять хранилище.</span><span class="sxs-lookup"><span data-stu-id="14ee6-108">Readers can read the policy store at the delegated level but cannot modify the store.</span></span>

<span data-ttu-id="14ee6-109">Пользователь или группа, которые являются либо администратором, либо средством чтения приложения, также должны быть добавлены в качестве делегированного пользователя хранилища политик, содержащего это приложение.</span><span class="sxs-lookup"><span data-stu-id="14ee6-109">A user or group that is either an administrator or a reader of an application must also be added as a delegated user of the policy store that contains that application.</span></span> <span data-ttu-id="14ee6-110">Аналогичным образом пользователь или группа, являющиеся администратором или читательом области, должны быть добавлены в качестве делегированного пользователя приложения, содержащего эту область.</span><span class="sxs-lookup"><span data-stu-id="14ee6-110">Similarly, a user or group that is an administrator or a reader of a scope must be added as a delegated user of the application that contains that scope.</span></span>

<span data-ttu-id="14ee6-111">**Делегирование администрирования области**</span><span class="sxs-lookup"><span data-stu-id="14ee6-111">**To delegate administration of a scope**</span></span>

1.  <span data-ttu-id="14ee6-112">Добавьте пользователя или группу в список делегированных пользователей хранилища, содержащего область, вызвав метод [**аддделегатедполициусер**](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-adddelegatedpolicyuser) объекта [**азаусоризатионсторе**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) , содержащего область.</span><span class="sxs-lookup"><span data-stu-id="14ee6-112">Add the user or group to the list of delegated users of the store that contains the scope by calling the [**AddDelegatedPolicyUser**](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-adddelegatedpolicyuser) method of the [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) object that contains the scope.</span></span>
2.  <span data-ttu-id="14ee6-113">Добавьте пользователя или группу в список делегированных пользователей приложения, которое содержит область, вызвав метод [**аддделегатедполициусер**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-adddelegatedpolicyuser) объекта [**иазаппликатион**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) , содержащего область.</span><span class="sxs-lookup"><span data-stu-id="14ee6-113">Add the user or group to the list of delegated users of the application that contains the scope by calling the [**AddDelegatedPolicyUser**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-adddelegatedpolicyuser) method of the [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) object that contains the scope.</span></span>
3.  <span data-ttu-id="14ee6-114">Добавьте пользователя или группу в список администраторов области, вызвав метод [**аддполициадминистратор**](/windows/desktop/api/Azroles/nf-azroles-iazscope-addpolicyadministrator) объекта [**иазскопе**](/windows/desktop/api/Azroles/nn-azroles-iazscope) .</span><span class="sxs-lookup"><span data-stu-id="14ee6-114">Add the user or group to the list of administrators of the scope by calling the [**AddPolicyAdministrator**](/windows/desktop/api/Azroles/nf-azroles-iazscope-addpolicyadministrator) method of the [**IAzScope**](/windows/desktop/api/Azroles/nn-azroles-iazscope) object.</span></span>

> [!Note]  
> <span data-ttu-id="14ee6-115">Хранилища политик на основе XML не поддерживают делегирование на любом уровне.</span><span class="sxs-lookup"><span data-stu-id="14ee6-115">XML-based policy stores do not support delegation at any level.</span></span>

 

<span data-ttu-id="14ee6-116">Если область в хранилище данных авторизации, хранящаяся в Active Directory, содержит определения задач, включающие правила авторизации или определения ролей, включающие правила авторизации, то область не может быть делегирована.</span><span class="sxs-lookup"><span data-stu-id="14ee6-116">If a scope within an authorization store that is stored in Active Directory contains task definitions that include authorization rules or role definitions that include authorization rules, the scope cannot be delegated.</span></span>

<span data-ttu-id="14ee6-117">В следующем примере показано, как делегировать администрирование приложения.</span><span class="sxs-lookup"><span data-stu-id="14ee6-117">The following example shows how to delegate administration of an application.</span></span> <span data-ttu-id="14ee6-118">В этом примере предполагается, что в указанном расположении имеется хранилище политик авторизации Active Directory, которое содержит приложение с именем "расходы" и не содержит задач с сценариями бизнес-правил.</span><span class="sxs-lookup"><span data-stu-id="14ee6-118">The example assumes that there is an existing Active Directory authorization policy store at the specified location, that this policy store contains an application named Expense, and that this application contains no tasks with business rule scripts.</span></span>


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



 

 



