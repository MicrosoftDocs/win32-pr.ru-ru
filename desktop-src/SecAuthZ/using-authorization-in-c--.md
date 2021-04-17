---
description: Использование API диспетчера авторизации для управления доступом к ресурсам приложения.
ms.assetid: 2485056c-b860-4247-9e7b-0157ca85d05d
title: Использование авторизации в C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b6771d16748d3c04680b545a83e382fa3d5ce78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663953"
---
# <a name="using-authorization-in-c"></a><span data-ttu-id="1a9a2-103">Использование авторизации в C++</span><span class="sxs-lookup"><span data-stu-id="1a9a2-103">Using Authorization in C++</span></span>

<span data-ttu-id="1a9a2-104">API диспетчера авторизации можно использовать для управления доступом к ресурсам приложения.</span><span class="sxs-lookup"><span data-stu-id="1a9a2-104">You can use the Authorization Manager API to control access to application resources.</span></span>

<span data-ttu-id="1a9a2-105">Если у вас есть решение по управлению доступом на основе [*списков управления доступом*](/windows/desktop/SecGloss/a-gly) (ACL) и вы хотите избежать преобразования этого решения для использования диспетчера авторизации, можно продолжать использовать списки управления доступом для управления доступом к ресурсам.</span><span class="sxs-lookup"><span data-stu-id="1a9a2-105">If you have an existing access control solution based on [*access control lists*](/windows/desktop/SecGloss/a-gly) (ACLs) and want to avoid converting this solution to use Authorization Manager, you can continue to use ACLs to control access to resources.</span></span> <span data-ttu-id="1a9a2-106">Сведения об управлении доступом к ресурсам с помощью списков управления доступом см. в статьях [Определение разрешений с использованием ACL в c++](defining-permissions-with-acls-in-c--.md), [Установка контекста клиента из идентификатора SID в C++](establishing-a-client-context-from-a-sid-in-c--.md)и [Проверка клиентского доступа с помощью ACL в c++](verifying-client-access-with-acls-in-c--.md).</span><span class="sxs-lookup"><span data-stu-id="1a9a2-106">For information about controlling access to resources using ACLs, see [Defining Permissions with ACLs in C++](defining-permissions-with-acls-in-c--.md), [Establishing a Client Context from a SID in C++](establishing-a-client-context-from-a-sid-in-c--.md), and [Verifying Client Access with ACLs in C++](verifying-client-access-with-acls-in-c--.md).</span></span>

> [!Note]  
> <span data-ttu-id="1a9a2-107">Для крупных предприятий существует компромисс между административными издержками и производительностью.</span><span class="sxs-lookup"><span data-stu-id="1a9a2-107">For large enterprises, there is a trade-off between administrative overhead and performance.</span></span> <span data-ttu-id="1a9a2-108">По мере роста количества защищенных ресурсов и пользователей Администрирование списков управления доступом становится более сложным.</span><span class="sxs-lookup"><span data-stu-id="1a9a2-108">As the number of secured resources and users increases, the administration of ACLs becomes more complicated.</span></span> <span data-ttu-id="1a9a2-109">Производительность не затрагивается, поскольку все необходимые сведения о правах доступа распространяются на защищенные ресурсы.</span><span class="sxs-lookup"><span data-stu-id="1a9a2-109">Performance is not affected because all required information about access rights is distributed to the secured resources.</span></span> <span data-ttu-id="1a9a2-110">Масштабирование влияет на производительность диспетчера авторизации.</span><span class="sxs-lookup"><span data-stu-id="1a9a2-110">The performance of Authorization Manager is affected by scaling.</span></span>

 

<span data-ttu-id="1a9a2-111">Сведения о других задачах авторизации см. [в разделе Поддержка задач для авторизации в C++](supporting-tasks-for-authorization-in-c--.md).</span><span class="sxs-lookup"><span data-stu-id="1a9a2-111">For information about other authorization tasks, see [Supporting Tasks for Authorization in C++](supporting-tasks-for-authorization-in-c--.md).</span></span>



| <span data-ttu-id="1a9a2-112">Раздел</span><span class="sxs-lookup"><span data-stu-id="1a9a2-112">Topic</span></span>                                                                                                                | <span data-ttu-id="1a9a2-113">Описание</span><span class="sxs-lookup"><span data-stu-id="1a9a2-113">Description</span></span>                                                                                              |
|----------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1a9a2-114">Определение разрешений в C++</span><span class="sxs-lookup"><span data-stu-id="1a9a2-114">Defining Permissions in C++</span></span>](defining-permissions-in-c--.md)                                                       | <span data-ttu-id="1a9a2-115">Определите, какие пользователи имеют доступ к ресурсам приложения, создав хранилище политик авторизации.</span><span class="sxs-lookup"><span data-stu-id="1a9a2-115">Define which users have access to which application resources by creating an authorization policy store.</span></span> |
| [<span data-ttu-id="1a9a2-116">Проверка клиентского доступа к запрошенному ресурсу в C++</span><span class="sxs-lookup"><span data-stu-id="1a9a2-116">Verifying Client Access to a Requested Resource in C++</span></span>](verifying-client-access-to-a-requested-resource-in-c--.md) | <span data-ttu-id="1a9a2-117">Проверьте, имеет ли клиент доступ к одной или нескольким операциям.</span><span class="sxs-lookup"><span data-stu-id="1a9a2-117">Check whether the client has access to one or more operations.</span></span>                                           |
| [<span data-ttu-id="1a9a2-118">Делегирование определения разрешений в C++</span><span class="sxs-lookup"><span data-stu-id="1a9a2-118">Delegating the Defining of Permissions in C++</span></span>](delegating-the-defining-of-permissions-in-c--.md)                   | <span data-ttu-id="1a9a2-119">Делегирование администрирования хранилищ политик авторизации, которые хранятся в Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1a9a2-119">Delegate the administration of authorization policy stores that are stored in Active Directory.</span></span>          |



 

 

 
