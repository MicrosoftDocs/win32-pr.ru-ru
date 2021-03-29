---
description: Хранилище политик авторизации содержит сведения о политике безопасности приложения или группы приложений.
ms.assetid: bce85da8-11de-4bc1-b097-d8efdbd28abf
title: Создание объекта хранилища политики авторизации в скрипте
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: feb02c80408210b663524e2aa914852a853e80ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898017"
---
# <a name="creating-an-authorization-policy-store-object-in-script"></a><span data-ttu-id="66b27-103">Создание объекта хранилища политики авторизации в скрипте</span><span class="sxs-lookup"><span data-stu-id="66b27-103">Creating an Authorization Policy Store Object in Script</span></span>

<span data-ttu-id="66b27-104">Хранилище политик авторизации содержит сведения о политике безопасности приложения или группы приложений.</span><span class="sxs-lookup"><span data-stu-id="66b27-104">An authorization policy store contains information about the security policy of an application or group of applications.</span></span> <span data-ttu-id="66b27-105">Эти сведения включают в себя приложения, операции, задачи, пользователей и группы пользователей, связанных с магазином.</span><span class="sxs-lookup"><span data-stu-id="66b27-105">The information includes the applications, operations, tasks, users, and groups of users associated with the store.</span></span> <span data-ttu-id="66b27-106">При инициализации приложения, использующего Диспетчер авторизации, оно загружает эту информацию из хранилища.</span><span class="sxs-lookup"><span data-stu-id="66b27-106">When an application that uses Authorization Manager initializes, it loads this information from the store.</span></span> <span data-ttu-id="66b27-107">Хранилище политик авторизации должно находиться в доверенной системе, так как администраторы этой системы имеют высокий уровень доступа к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="66b27-107">The authorization policy store must be located on a trusted system because administrators on that system have a high degree of access to the store.</span></span>

<span data-ttu-id="66b27-108">Диспетчер авторизации поддерживает хранение политики авторизации либо в службе каталогов Active Directory, либо в XML-файле, как показано в следующих примерах.</span><span class="sxs-lookup"><span data-stu-id="66b27-108">Authorization Manager supports storing authorization policy either in the Active Directory directory service or in an XML file as shown in the following examples.</span></span> <span data-ttu-id="66b27-109">В API диспетчера авторизации хранилище политик авторизации представлено объектом [**азаусоризатионсторе**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) .</span><span class="sxs-lookup"><span data-stu-id="66b27-109">In the Authorization Manager API, an authorization policy store is represented by an [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) object.</span></span> <span data-ttu-id="66b27-110">В примерах показано, как создать объект **азаусоризатионсторе** для хранилища Active Directory и XML-хранилища.</span><span class="sxs-lookup"><span data-stu-id="66b27-110">The examples show how to create an **AzAuthorizationStore** object for an Active Directory store and an XML store.</span></span>

-   [<span data-ttu-id="66b27-111">Создание хранилища Active Directory</span><span class="sxs-lookup"><span data-stu-id="66b27-111">Creating an Active Directory Store</span></span>](#creating-an-active-directory-store)
-   [<span data-ttu-id="66b27-112">Создание хранилища SQL Server</span><span class="sxs-lookup"><span data-stu-id="66b27-112">Creating a SQL Server Store</span></span>](#creating-a-sql-server-store)
-   [<span data-ttu-id="66b27-113">Создание хранилища XML</span><span class="sxs-lookup"><span data-stu-id="66b27-113">Creating an XML Store</span></span>](#creating-an-xml-store)

## <a name="creating-an-active-directory-store"></a><span data-ttu-id="66b27-114">Создание хранилища Active Directory</span><span class="sxs-lookup"><span data-stu-id="66b27-114">Creating an Active Directory Store</span></span>

<span data-ttu-id="66b27-115">Чтобы использовать Active Directory для хранения политики авторизации, домен должен находиться на функциональном уровне домена **Windows Server 2003** .</span><span class="sxs-lookup"><span data-stu-id="66b27-115">To use Active Directory to store the authorization policy, the domain must be in the **Windows Server 2003** domain functional level.</span></span> <span data-ttu-id="66b27-116">Хранилище политик авторизации не может располагаться в **контексте именования, не являющегося доменом** (также называемого секцией приложения).</span><span class="sxs-lookup"><span data-stu-id="66b27-116">The authorization policy store cannot be located in a **Non-Domain Naming Context** (also called an application partition).</span></span> <span data-ttu-id="66b27-117">Рекомендуется размещать хранилище в контейнере **данных программы** в новом подразделении, созданном специально для хранилища политик авторизации.</span><span class="sxs-lookup"><span data-stu-id="66b27-117">It is recommended that the store be located in the **Program Data** container under a new organizational unit created specifically for the authorization policy store.</span></span> <span data-ttu-id="66b27-118">Также рекомендуется, чтобы хранилище размещалось в той же локальной сети, что и серверы приложений, использующие хранилище.</span><span class="sxs-lookup"><span data-stu-id="66b27-118">It is also recommended that the store be located within the same local area network as application servers that run applications that use the store.</span></span>

<span data-ttu-id="66b27-119">В следующем примере показано, как создать объект [**азаусоризатионсторе**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) , представляющий хранилище политик авторизации в Active Directory.</span><span class="sxs-lookup"><span data-stu-id="66b27-119">The following example shows how to create an [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) object that represents an authorization policy store in Active Directory.</span></span> <span data-ttu-id="66b27-120">В этом примере предполагается, что существует Active Directory подразделение с именем Program Data в домене с именем authmanager.com.</span><span class="sxs-lookup"><span data-stu-id="66b27-120">The example assumes that there is an existing Active Directory organizational unit named Program Data in a domain named authmanager.com.</span></span>


```VB
'  Create the store object.
Dim authStore
Set authStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the store object.
authStore.Initialize 1, _
    "msldap://CN=MyStore, CN=Program Data,DC=authmanager,DC=com"

'  Save the information to the store.
authStore.Submit
```



## <a name="creating-a-sql-server-store"></a><span data-ttu-id="66b27-121">Создание хранилища SQL Server</span><span class="sxs-lookup"><span data-stu-id="66b27-121">Creating a SQL Server Store</span></span>

<span data-ttu-id="66b27-122">Диспетчер авторизации поддерживает создание хранилища политик авторизации на основе Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="66b27-122">Authorization Manager supports creating a Microsoft SQL Server–based authorization policy store.</span></span> <span data-ttu-id="66b27-123">Чтобы создать хранилище данных авторизации на основе SQL Server, используйте URL-адрес, который начинается с префикса **MSSQL://**.</span><span class="sxs-lookup"><span data-stu-id="66b27-123">To create a SQL Server–based authorization store, use a URL that begins with the prefix **MSSQL://**.</span></span> <span data-ttu-id="66b27-124">URL-адрес должен содержать допустимую строку подключения SQL, имя базы данных и имя хранилища политики авторизации: **MSSQL://**_ConnectionString_ *_/_* _DatabaseName_ *_/_* _полицисторенаме_.</span><span class="sxs-lookup"><span data-stu-id="66b27-124">The URL must contain a valid SQL connection string, a database name, and the name of the authorization policy store: **MSSQL://**_ConnectionString_*_/_*_DatabaseName_*_/_*_PolicyStoreName_.</span></span>

<span data-ttu-id="66b27-125">Если экземпляр SQL Server не содержит указанную базу данных диспетчера авторизации, диспетчер авторизации создает новую базу данных с таким именем.</span><span class="sxs-lookup"><span data-stu-id="66b27-125">If the instance of SQL Server does not contain the specified Authorization Manager database, Authorization Manager creates a new database with that name.</span></span>

> [!Note]  
> <span data-ttu-id="66b27-126">Подключения к хранилищу SQL Server не шифруются, если не задано явное шифрование SQL для подключения или не настроено шифрование сетевого трафика, использующего протокол IPsec.</span><span class="sxs-lookup"><span data-stu-id="66b27-126">Connections to a SQL Server store are not encrypted unless you explicitly set up SQL encryption for the connection or set up encryption of the network traffic that uses Internet Protocol Security (IPsec).</span></span>

 

<span data-ttu-id="66b27-127">В следующем примере показано, как создать объект [**азаусоризатионсторе**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) , представляющий хранилище политик авторизации в базе данных SQL Server.</span><span class="sxs-lookup"><span data-stu-id="66b27-127">The following example shows how to create an [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) object that represents an authorization policy store in a SQL Server database.</span></span>


```VB
'  Create the store object.
Dim authStore
Set authStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the store object.
authStore.Initialize 1, _ 
  "MSSQL://Driver={SQL Server};Server={AzServer};/AzDB/MyStore"

'  Save information to the store.
authStore.Submit
```



## <a name="creating-an-xml-store"></a><span data-ttu-id="66b27-128">Создание хранилища XML</span><span class="sxs-lookup"><span data-stu-id="66b27-128">Creating an XML Store</span></span>

<span data-ttu-id="66b27-129">Диспетчер авторизации поддерживает создание хранилища политик авторизации в формате XML.</span><span class="sxs-lookup"><span data-stu-id="66b27-129">Authorization Manager supports creating an authorization policy store in XML format.</span></span> <span data-ttu-id="66b27-130">Хранилище XML может располагаться на том же компьютере, где выполняется приложение, или его можно сохранить удаленно.</span><span class="sxs-lookup"><span data-stu-id="66b27-130">The XML store can be located on the same computer where the application runs, or it can be stored remotely.</span></span> <span data-ttu-id="66b27-131">Непосредственное изменение XML-файла не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="66b27-131">Editing the XML file directly is not supported.</span></span> <span data-ttu-id="66b27-132">Чтобы изменить хранилище политик, используйте оснастку MMC диспетчера авторизации или API диспетчера авторизации.</span><span class="sxs-lookup"><span data-stu-id="66b27-132">Use the Authorization Manager MMC snap-in or the Authorization Manager API to edit the policy store.</span></span>

<span data-ttu-id="66b27-133">Диспетчер авторизации не поддерживает делегирование администрирования хранилища политик XML.</span><span class="sxs-lookup"><span data-stu-id="66b27-133">Authorization Manager does not support delegating administration of an XML policy store.</span></span> <span data-ttu-id="66b27-134">Сведения о делегировании см. [в разделе Делегирование определения разрешений в скрипте](delegating-the-defining-of-permissions-in-script.md).</span><span class="sxs-lookup"><span data-stu-id="66b27-134">For information about delegation, see [Delegating the Defining of Permissions in Script](delegating-the-defining-of-permissions-in-script.md).</span></span>

<span data-ttu-id="66b27-135">В следующем примере показано, как создать объект [**азаусоризатионсторе**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) , представляющий хранилище политики авторизации в XML-файле.</span><span class="sxs-lookup"><span data-stu-id="66b27-135">The following example shows how to create an [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) object that represents an authorization policy store in an XML file.</span></span>


```VB
'  Create the store object.
Dim authStore
Set authStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the store object.
authStore.Initialize 1, "msxml://C:\MyStore.xml"

'  Save information to the store.
authStore.Submit
```



 

 



