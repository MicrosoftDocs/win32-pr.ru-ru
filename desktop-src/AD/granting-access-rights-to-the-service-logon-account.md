---
title: Предоставление прав доступа учетной записи входа в службу
description: Основное внимание в установке экземпляра службы заключается в том, чтобы установленная служба могла получить доступ к необходимым ресурсам.
ms.assetid: 5b756318-f621-4fce-af2b-71ccccbb4e3c
ms.tgt_platform: multiple
keywords:
- Предоставление прав доступа учетной записи входа в службу AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22f4ea5b85e6158109338b881eeb3f59d74a3910
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "105654292"
---
# <a name="granting-access-rights-to-the-service-logon-account"></a><span data-ttu-id="4f514-104">Предоставление прав доступа учетной записи входа в службу</span><span class="sxs-lookup"><span data-stu-id="4f514-104">Granting Access Rights to the Service Logon Account</span></span>

<span data-ttu-id="4f514-105">Основное внимание в установке экземпляра службы заключается в том, чтобы установленная служба могла получить доступ к необходимым ресурсам.</span><span class="sxs-lookup"><span data-stu-id="4f514-105">A primary consideration of installing a service instance is to ensure that the installed service can access the necessary resources.</span></span> <span data-ttu-id="4f514-106">Для этого следует задать ACE в дескрипторах безопасности объектов, к которым служба должна обращаться.</span><span class="sxs-lookup"><span data-stu-id="4f514-106">To do this, set ACEs in the security descriptors of objects that the service must access.</span></span> <span data-ttu-id="4f514-107">ACE может предоставлять или запрещать права доступа для указанного субъекта безопасности, например учетной записи пользователя службы или учетной записи компьютера для службы LocalSystem, или группы, к которой принадлежит учетная запись службы.</span><span class="sxs-lookup"><span data-stu-id="4f514-107">An ACE can grant or deny access rights to a specified security principal, such as the service user account, or the computer account for a LocalSystem service, or a group to which the service's account belongs.</span></span> <span data-ttu-id="4f514-108">Дополнительные сведения об элементах управления доступом, дескрипторах безопасности и управлении доступом см. [в разделе Управление доступом к объектам в домен Active Directory служб](controlling-access-to-objects-in-active-directory-domain-services.md) и [управлении доступом](/windows/desktop/SecAuthZ/access-control).</span><span class="sxs-lookup"><span data-stu-id="4f514-108">For more information about ACEs, security descriptors, and access control, see [Controlling Access to objects in Active Directory Domain Services](controlling-access-to-objects-in-active-directory-domain-services.md) and [Access Control](/windows/desktop/SecAuthZ/access-control).</span></span>

<span data-ttu-id="4f514-109">Дополнительные сведения и пример кода, который можно использовать для настройки записи ACE, которая позволяет службе изменять точку подключения службы, см. в разделе [Включение учетной записью службы для доступа к свойствам SCP](enabling-service-account-to-access-scp-properties.md).</span><span class="sxs-lookup"><span data-stu-id="4f514-109">For more information and a code example that can be used to set an ACE that enables the service to modify its service connection point, see [Enabling Service Account to Access SCP Properties](enabling-service-account-to-access-scp-properties.md).</span></span>

<span data-ttu-id="4f514-110">В некоторых случаях учетную запись пользователя службы необходимо добавить в состав одной или нескольких групп безопасности.</span><span class="sxs-lookup"><span data-stu-id="4f514-110">In some cases, you must add your service user account as a member of one or more security groups.</span></span> <span data-ttu-id="4f514-111">Например, если вы создаете группу администраторов для службы, вы можете сделать ее членом группы.</span><span class="sxs-lookup"><span data-stu-id="4f514-111">For example, if you create an administrators group for your service, you might make the service a member of the group.</span></span> <span data-ttu-id="4f514-112">После этого можно предоставить группе права доступа, а не предоставлять их явным образом учетной записи службы.</span><span class="sxs-lookup"><span data-stu-id="4f514-112">You can then grant access rights to the group rather than granting them explicitly to the service account.</span></span> <span data-ttu-id="4f514-113">Дополнительные сведения о группах безопасности см. в разделе [Управление группами](managing-groups.md).</span><span class="sxs-lookup"><span data-stu-id="4f514-113">For more information about security groups, see [Managing Groups](managing-groups.md).</span></span>

 

 