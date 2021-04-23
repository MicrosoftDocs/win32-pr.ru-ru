---
title: Влияние безопасности на операции в службах домен Active Directory Services
description: Домен Active Directory Services используют управление доступом для предоставления или запрета доступа к объектам, свойствам и операциям на основе удостоверения пользователя, выполняющего попытку доступа.
ms.assetid: d5d53354-fa97-4e46-9632-20ac49f7db5a
ms.tgt_platform: multiple
keywords:
- Эффекты безопасности в службах домен Active Directory Services Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3be628acd1709985aeaa9539bfa527de674732ef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103887659"
---
# <a name="how-security-affects-operations-in-active-directory-domain-services"></a><span data-ttu-id="d3e06-104">Влияние безопасности на операции в службах домен Active Directory Services</span><span class="sxs-lookup"><span data-stu-id="d3e06-104">How Security Affects Operations in Active Directory Domain Services</span></span>

<span data-ttu-id="d3e06-105">Домен Active Directory Services используют управление доступом для предоставления или запрета доступа к объектам, свойствам и операциям на основе удостоверения пользователя, выполняющего попытку доступа.</span><span class="sxs-lookup"><span data-stu-id="d3e06-105">Active Directory Domain Services use access control to grant or deny access to objects, properties, and operations based on the identity of the user performing the access attempt.</span></span> <span data-ttu-id="d3e06-106">Когда приложение привязывается к каталогу, оно связывается с конкретными учетными данными пользователя.</span><span class="sxs-lookup"><span data-stu-id="d3e06-106">When your application binds to the directory, it binds with specific user credentials.</span></span> <span data-ttu-id="d3e06-107">При проверке подлинности эти учетные данные определяют контекст безопасности приложения.</span><span class="sxs-lookup"><span data-stu-id="d3e06-107">When authenticated, these credentials determine your application's security context.</span></span> <span data-ttu-id="d3e06-108">Независимо от того, являются ли учетные данные вошедшим в систему пользователем, указанным пользователем, учетной записью службы, учетной записью компьютера или пользователем, не прошедшим проверку подлинности (гостевой или все), Active Directory сервер проверяет права пользователя на доступ к объекту до выполнения каких-либо операций с этим объектом.</span><span class="sxs-lookup"><span data-stu-id="d3e06-108">Regardless of whether the credentials are those of the logged-on user, a specified user, a service account, a computer account, or an unauthenticated user (Guest/Everyone), the Active Directory server verifies the user's right to access an object before any operation is performed on that object.</span></span> <span data-ttu-id="d3e06-109">Пользователь может или не иметь доступа к определенному объекту, его дочерним элементам, его свойствам или операциям на этом объекте, что означает, что приложение должно справиться с возможными ошибками, вызванными отказом в доступе.</span><span class="sxs-lookup"><span data-stu-id="d3e06-109">The user may, or may not, have access to a particular object, its children, its properties, or operations on that object, which means that your application must handle the potential errors caused by denied access.</span></span>

<span data-ttu-id="d3e06-110">Дополнительные сведения о контекстах безопасности и влиянии контроля доступа на различные операции см. в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="d3e06-110">For more information about security contexts and the effects of access control on various operations, see:</span></span>

-   [<span data-ttu-id="d3e06-111">Операции контроля доступа и чтения</span><span class="sxs-lookup"><span data-stu-id="d3e06-111">Access Control and Read Operations</span></span>](access-control-and-read-operations.md)
-   [<span data-ttu-id="d3e06-112">Операции управления доступом и записи</span><span class="sxs-lookup"><span data-stu-id="d3e06-112">Access Control and Write Operations</span></span>](access-control-and-write-operations.md)
-   [<span data-ttu-id="d3e06-113">Управление доступом и создание объектов</span><span class="sxs-lookup"><span data-stu-id="d3e06-113">Access Control and Object Creation</span></span>](access-control-and-object-creation.md)
-   [<span data-ttu-id="d3e06-114">Управление доступом и удаление объектов</span><span class="sxs-lookup"><span data-stu-id="d3e06-114">Access Control and Object Deletion</span></span>](access-control-and-object-deletion.md)

 

 




