---
title: Использование групп безопасности в управлении доступом
description: Идентификатор безопасности (SID) — это идентификатор объекта пользователя или группы безопасности, когда пользователь или группа используются в целях безопасности.
ms.assetid: 3236c51f-21c1-4c07-9b76-2668ae72a42f
ms.tgt_platform: multiple
keywords:
- Использование групп безопасности в управлении доступом
- Управление доступом, группы безопасности, используемые в
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf7096e32c64fe420ca6625378725ce8e4864beb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105654184"
---
# <a name="how-security-groups-are-used-in-access-control"></a><span data-ttu-id="7f142-105">Использование групп безопасности в управлении доступом</span><span class="sxs-lookup"><span data-stu-id="7f142-105">How Security Groups are Used in Access Control</span></span>

<span data-ttu-id="7f142-106">Идентификатор безопасности (SID) — это идентификатор объекта пользователя или группы безопасности, когда пользователь или группа используются в целях безопасности.</span><span class="sxs-lookup"><span data-stu-id="7f142-106">The security identifier (SID) is the object identifier of the user or security group when the user or group is used for security purposes.</span></span> <span data-ttu-id="7f142-107">Имя пользователя или группы не используется в качестве уникального идентификатора в системе.</span><span class="sxs-lookup"><span data-stu-id="7f142-107">The name of the user or group is not used as the unique identifier within the system.</span></span> <span data-ttu-id="7f142-108">Идентификатор безопасности хранится в атрибуте **objectSid** объектов пользователя и объектов группы безопасности.</span><span class="sxs-lookup"><span data-stu-id="7f142-108">The SID is stored in the **objectSid** attribute of user objects and security group objects.</span></span> <span data-ttu-id="7f142-109">Сервер Active Directory создает **objectSid** при создании пользователя или группы.</span><span class="sxs-lookup"><span data-stu-id="7f142-109">The Active Directory server generates the **objectSid** when the user or group is created.</span></span> <span data-ttu-id="7f142-110">Система гарантирует уникальность идентификаторов безопасности в лесу.</span><span class="sxs-lookup"><span data-stu-id="7f142-110">The system ensures that the SIDs are unique across a forest.</span></span> <span data-ttu-id="7f142-111">Имейте в виду, что **objectGuid** — это уникальный идентификатор пользователя, группы или любого другого объекта каталога.</span><span class="sxs-lookup"><span data-stu-id="7f142-111">Be aware that the **objectGuid** is the unique identifier of a user, group, or any other directory object.</span></span> <span data-ttu-id="7f142-112">Идентификатор безопасности изменяется при перемещении пользователя или группы в другой домен. **objectGuid** остается неизменным.</span><span class="sxs-lookup"><span data-stu-id="7f142-112">The SID changes if a user or group is moved to another domain; the **objectGuid** remains the same.</span></span>

<span data-ttu-id="7f142-113">Когда пользователю или группе предоставляется разрешение на доступ к ресурсу, например к принтеру или общей папке, идентификатор безопасности пользователя или группы добавляется в запись контроля доступа (ACE), определяющую предоставленное разрешение в списке управления доступом на уровне пользователей (DACL) ресурса.</span><span class="sxs-lookup"><span data-stu-id="7f142-113">When a user or group is given permission to access a resource, such as a printer or a file share, the SID of the user or group is added to the access control entry (ACE) defining the granted permission in the resource's discretionary access control list (DACL).</span></span> <span data-ttu-id="7f142-114">В службах домен Active Directory Services каждый объект имеет атрибут **нтсекуритидескриптор** , в котором хранится DACL, определяющий доступ к конкретному объекту или атрибутам этого объекта.</span><span class="sxs-lookup"><span data-stu-id="7f142-114">In Active Directory Domain Services, each object has an **nTSecurityDescriptor** attribute that stores a DACL defining the access to that particular object or attributes on that object.</span></span> <span data-ttu-id="7f142-115">Дополнительные сведения о настройке контроля доступа для объектов в службах домен Active Directory см. [в разделе Управление доступом к объектам в службах домен Active Directory](controlling-access-to-objects-in-active-directory-domain-services.md).</span><span class="sxs-lookup"><span data-stu-id="7f142-115">For more information about setting access control on objects in Active Directory Domain Services, see [Controlling Access to Objects in Active Directory Domain Services](controlling-access-to-objects-in-active-directory-domain-services.md).</span></span>

<span data-ttu-id="7f142-116">Когда пользователь входит в домен Windows 2000, операционная система создает маркер доступа.</span><span class="sxs-lookup"><span data-stu-id="7f142-116">When a user logs on to a Windows 2000 domain, the operating system generates an access token.</span></span> <span data-ttu-id="7f142-117">Этот маркер доступа используется для определения ресурсов, к которым может получить доступ пользователь.</span><span class="sxs-lookup"><span data-stu-id="7f142-117">This access token is used to determine which resources the user may access.</span></span> <span data-ttu-id="7f142-118">Маркер доступа пользователя включает следующие данные:</span><span class="sxs-lookup"><span data-stu-id="7f142-118">The user access token includes the following data:</span></span>

-   <span data-ttu-id="7f142-119">Идентификатор безопасности пользователя.</span><span class="sxs-lookup"><span data-stu-id="7f142-119">User SID.</span></span>
-   <span data-ttu-id="7f142-120">Идентификаторы безопасности всех глобальных и универсальных групп безопасности, членом которых является пользователь.</span><span class="sxs-lookup"><span data-stu-id="7f142-120">SIDs of all global and universal security groups that the user is a member of.</span></span>
-   <span data-ttu-id="7f142-121">Идентификаторы безопасности всех вложенных глобальных и универсальных групп безопасности.</span><span class="sxs-lookup"><span data-stu-id="7f142-121">SIDs of all nested global and universal security groups.</span></span>

<span data-ttu-id="7f142-122">Каждый процесс, выполняемый от имени этого пользователя, имеет копию этого маркера доступа.</span><span class="sxs-lookup"><span data-stu-id="7f142-122">Every process executed on behalf of this user has a copy of this access token.</span></span>

<span data-ttu-id="7f142-123">Когда пользователь пытается получить доступ к ресурсам на компьютере, служба, с помощью которой пользователь получает доступ к ресурсу, будет олицетворять пользователя, создавая новый маркер доступа на основе маркера доступа, созданного во время входа пользователя.</span><span class="sxs-lookup"><span data-stu-id="7f142-123">When the user attempts to access resources on a computer, the service through which the user accesses the resource will impersonate the user by creating a new access token based on the access token created at user logon time.</span></span> <span data-ttu-id="7f142-124">Этот новый маркер доступа также будет содержать следующие идентификаторы безопасности:</span><span class="sxs-lookup"><span data-stu-id="7f142-124">This new access token will also contain the following SIDs:</span></span>

-   <span data-ttu-id="7f142-125">Идентификаторы безопасности для всех локальных групп домена в конечном домене, членом которых является пользователь.</span><span class="sxs-lookup"><span data-stu-id="7f142-125">SIDs for all domain local groups in the target domain that the user is a member of.</span></span>
-   <span data-ttu-id="7f142-126">Идентификаторы безопасности для всех локальных групп компьютеров на конечном компьютере, членом которых является пользователь.</span><span class="sxs-lookup"><span data-stu-id="7f142-126">SIDs for all machine local groups on the target computer that the user is a member of.</span></span>

<span data-ttu-id="7f142-127">Служба использует этот новый маркер доступа для вычисления доступа к ресурсу.</span><span class="sxs-lookup"><span data-stu-id="7f142-127">The service uses this new access token to evaluate access to the resource.</span></span> <span data-ttu-id="7f142-128">Если идентификатор безопасности в маркере доступа отображается в любой записи ACE в списке DACL, служба предоставляет пользователю разрешения, указанные в этих элементах управления доступом.</span><span class="sxs-lookup"><span data-stu-id="7f142-128">If a SID in the access token appears in any ACEs in the DACL, the service gives the user the permissions specified in those ACEs.</span></span>

 

 




