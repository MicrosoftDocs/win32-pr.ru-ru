---
description: Инструментарий WMI использует стандартные дескрипторы безопасности Windows для контроля и защиты доступа к защищаемым объектам, таким как пространства имен WMI, принтеры, службы и приложения DCOM.
ms.assetid: 5893457d-3fc2-4d64-a6c2-0f410052ce52
ms.tgt_platform: multiple
title: Доступ к защищаемым объектам WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ad4ea78cd45d57856b0909283e7c2624fb26bd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272236"
---
# <a name="access-to-wmi-securable-objects"></a><span data-ttu-id="79f93-103">Доступ к защищаемым объектам WMI</span><span class="sxs-lookup"><span data-stu-id="79f93-103">Access to WMI Securable Objects</span></span>

<span data-ttu-id="79f93-104">Инструментарий WMI использует стандартные [*дескрипторы безопасности*](/windows/desktop/SecGloss/s-gly) Windows для контроля и защиты доступа к защищаемым объектам, таким как пространства имен WMI, принтеры, службы и приложения DCOM.</span><span class="sxs-lookup"><span data-stu-id="79f93-104">WMI relies on standard Windows [*security descriptors*](/windows/desktop/SecGloss/s-gly) to control and protect access to securable objects like WMI namespaces, printers, services, and DCOM applications.</span></span> <span data-ttu-id="79f93-105">Дополнительные сведения см. [в разделе доступ к пространствам имен WMI](access-to-wmi-namespaces.md).</span><span class="sxs-lookup"><span data-stu-id="79f93-105">For more information, see [Access to WMI Namespaces](access-to-wmi-namespaces.md).</span></span>

<span data-ttu-id="79f93-106">В этом разделе рассматриваются следующие вопросы.</span><span class="sxs-lookup"><span data-stu-id="79f93-106">The following topics are discussed in this section:</span></span>

-   [<span data-ttu-id="79f93-107">Дескрипторы безопасности и SID</span><span class="sxs-lookup"><span data-stu-id="79f93-107">Security Descriptors and SIDs</span></span>](#security-descriptors-and-sids)
-   [<span data-ttu-id="79f93-108">Управление доступом</span><span class="sxs-lookup"><span data-stu-id="79f93-108">Access Control</span></span>](#access-control)
-   [<span data-ttu-id="79f93-109">Изменение параметров безопасности доступа</span><span class="sxs-lookup"><span data-stu-id="79f93-109">Changing Access Security</span></span>](#changing-access-security)
-   [<span data-ttu-id="79f93-110">См. также</span><span class="sxs-lookup"><span data-stu-id="79f93-110">Related topics</span></span>](#related-topics)

## <a name="security-descriptors-and-sids"></a><span data-ttu-id="79f93-111">Дескрипторы безопасности и SID</span><span class="sxs-lookup"><span data-stu-id="79f93-111">Security Descriptors and SIDs</span></span>

<span data-ttu-id="79f93-112">WMI обеспечивает безопасность доступа, сравнивая [*маркер доступа*](/windows/desktop/SecGloss/a-gly) пользователя, пытающегося получить доступ к защищаемому объекту, с дескриптором безопасности объекта.</span><span class="sxs-lookup"><span data-stu-id="79f93-112">WMI maintains access security by comparing the [*access token*](/windows/desktop/SecGloss/a-gly) of the user that attempts to access a securable object with the security descriptor of the object.</span></span>

<span data-ttu-id="79f93-113">Когда пользователь или группа создается в системе, учетной записи присваивается [*идентификатор безопасности (SID)*](/windows/desktop/SecGloss/s-gly) , гарантирующий, что учетная запись, созданная с тем же именем, что и ранее удаленная учетная запись, не наследует предыдущие параметры безопасности.</span><span class="sxs-lookup"><span data-stu-id="79f93-113">When a user or group is created on a system, the account is given a [*security identifier (SID)*](/windows/desktop/SecGloss/s-gly) The SID ensures that an account created with the same name as a previously deleted account does not inherit the previous security settings.</span></span> <span data-ttu-id="79f93-114">Маркер доступа создается путем объединения идентификатора безопасности, списка групп, членом которых является пользователь, и списка включенных или отключенных привилегий.</span><span class="sxs-lookup"><span data-stu-id="79f93-114">An access token is created by combining the SID, the list of groups of which the user is a member, and the list of enabled or disabled privileges.</span></span> <span data-ttu-id="79f93-115">Эти маркеры назначаются всем процессам и потокам, принадлежащим пользователю.</span><span class="sxs-lookup"><span data-stu-id="79f93-115">These tokens are assigned to all processes and threads owned by the user.</span></span>

## <a name="access-control"></a><span data-ttu-id="79f93-116">Управление доступом</span><span class="sxs-lookup"><span data-stu-id="79f93-116">Access Control</span></span>

<span data-ttu-id="79f93-117">Когда пользователь хочет использовать защищенный объект, маркер доступа сравнивается со списком управления доступом на [*уровне пользователей (DACL)*](/windows/desktop/SecGloss/d-gly) в дескрипторе безопасности объекта.</span><span class="sxs-lookup"><span data-stu-id="79f93-117">When the user wants to use a secured object, the access token is compared with the [*discretionary access control list (DACL)*](/windows/desktop/SecGloss/d-gly) in the security descriptor on the object.</span></span> <span data-ttu-id="79f93-118">Список DACL содержит разрешения, называемые [*записями управления доступом (ACE)*](/windows/desktop/SecGloss/a-gly).</span><span class="sxs-lookup"><span data-stu-id="79f93-118">The DACL contains permissions called [*access control entries (ACE)*](/windows/desktop/SecGloss/a-gly).</span></span> <span data-ttu-id="79f93-119">[*Системные списки управления доступом (SACL)*](/windows/desktop/SecGloss/s-gly) делают то же самое, что и списки DACL, но могут создавать события аудита безопасности.</span><span class="sxs-lookup"><span data-stu-id="79f93-119">[*System access control lists (SACL)*](/windows/desktop/SecGloss/s-gly) do the same thing as DACLs, but can generate security audit events.</span></span> <span data-ttu-id="79f93-120">Начиная с Windows Vista, Инструментарий WMI может создавать записи аудита в журнале безопасности Windows.</span><span class="sxs-lookup"><span data-stu-id="79f93-120">Starting with Windows Vista, WMI can make auditing entries in the Windows Security Log.</span></span> <span data-ttu-id="79f93-121">Дополнительные сведения об аудите в WMI см. в разделе [доступ к пространствам имен WMI](access-to-wmi-namespaces.md).</span><span class="sxs-lookup"><span data-stu-id="79f93-121">For more information about auditing in WMI, see [Access to WMI Namespaces](access-to-wmi-namespaces.md).</span></span>

<span data-ttu-id="79f93-122">Списки DACL и SACL состоят из списка записей ACE, описывающих, какие пользователи имеют определенные права доступа, включая запись в репозиторий WMI, удаленный доступ и выполнение, а также разрешения на вход.</span><span class="sxs-lookup"><span data-stu-id="79f93-122">Both the DACL and the SACL consist of a list of ACEs that describe which users have specific access rights, including writing to the WMI repository, remote access and execution, and logon permissions.</span></span> <span data-ttu-id="79f93-123">Инструментарий WMI хранит эти списки ACL в репозитории WMI.</span><span class="sxs-lookup"><span data-stu-id="79f93-123">WMI stores these ACLs in the WMI repository.</span></span>

<span data-ttu-id="79f93-124">ACE содержат три типа уровней доступа или разрешения Grant или DENY: разрешить, запретить для DACL и аудит системы (для SACL).</span><span class="sxs-lookup"><span data-stu-id="79f93-124">ACEs hold three types of access levels or grant/deny rights: allow, deny for DACL, and system audit (for SACLs).</span></span> <span data-ttu-id="79f93-125">Запрет записей ACE перед разрешающим доступом ACE в списках DACL или SACL.</span><span class="sxs-lookup"><span data-stu-id="79f93-125">Deny ACEs precede allow ACEs in the DACL or SACL.</span></span> <span data-ttu-id="79f93-126">При проверке прав доступа пользователя Инструментарий WMI последовательно запускается через список управления доступом, пока не обнаружит разрешение ACE, которое применяется к запрашиваемому маркеру доступа.</span><span class="sxs-lookup"><span data-stu-id="79f93-126">When checking the user access rights, WMI runs consecutively through the access control list until it finds an allow ACE that applies to the requesting access token.</span></span> <span data-ttu-id="79f93-127">Остальные записи ACE не проверяются после этой точки.</span><span class="sxs-lookup"><span data-stu-id="79f93-127">The remaining ACEs are not checked after this point.</span></span> <span data-ttu-id="79f93-128">Если соответствующие разрешения ACE не найдены, доступ запрещается.</span><span class="sxs-lookup"><span data-stu-id="79f93-128">If no appropriate allow ACE is found, then access is denied.</span></span> <span data-ttu-id="79f93-129">Дополнительные сведения см. [в разделе порядок элементов ACE в списке DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl) и [Создание списка DACL](/windows/desktop/SecBP/creating-a-dacl).</span><span class="sxs-lookup"><span data-stu-id="79f93-129">For more information, see [Order of ACEs in a DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl) and [Creating a DACL](/windows/desktop/SecBP/creating-a-dacl).</span></span>

## <a name="changing-access-security"></a><span data-ttu-id="79f93-130">Изменение параметров безопасности доступа</span><span class="sxs-lookup"><span data-stu-id="79f93-130">Changing Access Security</span></span>

<span data-ttu-id="79f93-131">С соответствующими разрешениями можно изменить безопасность защищаемого объекта с помощью скрипта или приложения.</span><span class="sxs-lookup"><span data-stu-id="79f93-131">With appropriate permissions, you can change the security on a securable object with a script or application.</span></span> <span data-ttu-id="79f93-132">Параметры безопасности для пространств имен WMI также можно изменить с помощью [*элемента управления WMI*](gloss-w.md) или путем добавления строки на [языке определения дескрипторов безопасности (SDDL)](/windows/desktop/SecAuthZ/security-descriptor-definition-language) в файле [*MOF-файл (MOF)*](gloss-m.md) , который определяет классы для пространства имен.</span><span class="sxs-lookup"><span data-stu-id="79f93-132">You can also change the security settings on WMI namespaces using the [*WMI Control*](gloss-w.md) or by adding a [Security Descriptor Definition Language (SDDL)](/windows/desktop/SecAuthZ/security-descriptor-definition-language) string in the [*Managed Object Format (MOF)*](gloss-m.md) file that defines classes for the namespace.</span></span> <span data-ttu-id="79f93-133">Дополнительные сведения см. в статьях [доступ к пространствам имен WMI](access-to-wmi-namespaces.md), [Защита пространств имен WMI](securing-wmi-namespaces.md)и [изменение параметров безопасности доступа к защищаемым объектам](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="79f93-133">For more information, see [Access to WMI Namespaces](access-to-wmi-namespaces.md), [Securing WMI Namespaces](securing-wmi-namespaces.md), and [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="79f93-134">См. также</span><span class="sxs-lookup"><span data-stu-id="79f93-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79f93-135">Объекты дескрипторов безопасности WMI</span><span class="sxs-lookup"><span data-stu-id="79f93-135">WMI Security Descriptor Objects</span></span>](wmi-security-descriptor-objects.md)
</dt> <dt>

[<span data-ttu-id="79f93-136">Константы безопасности WMI</span><span class="sxs-lookup"><span data-stu-id="79f93-136">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> <dt>

[<span data-ttu-id="79f93-137">Управление учетными записями пользователей и WMI</span><span class="sxs-lookup"><span data-stu-id="79f93-137">User Account Control and WMI</span></span>](user-account-control-and-wmi.md)
</dt> <dt>

[<span data-ttu-id="79f93-138">Объекты дескрипторов безопасности WMI</span><span class="sxs-lookup"><span data-stu-id="79f93-138">WMI Security Descriptor Objects</span></span>](wmi-security-descriptor-objects.md)
</dt> <dt>

[<span data-ttu-id="79f93-139">Доступ к пространствам имен WMI</span><span class="sxs-lookup"><span data-stu-id="79f93-139">Access to WMI Namespaces</span></span>](access-to-wmi-namespaces.md)
</dt> </dl>

 

 
