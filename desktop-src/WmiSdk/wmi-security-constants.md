---
description: WMI проверяет права доступа для приложений и скриптов.
ms.assetid: f6808f50-a1fd-434f-8a42-efa3afbe7871
ms.tgt_platform: multiple
title: Константы безопасности WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d360aa57c12c958db95c4b94f2b06327a3f70dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272429"
---
# <a name="wmi-security-constants"></a><span data-ttu-id="cf6bb-103">Константы безопасности WMI</span><span class="sxs-lookup"><span data-stu-id="cf6bb-103">WMI Security Constants</span></span>

<span data-ttu-id="cf6bb-104">WMI проверяет права доступа для приложений и скриптов для таких объектов, как пространства имен WMI, принтер, службы, приложения DCOM, файлы, общие папки и другие защищаемые объекты.</span><span class="sxs-lookup"><span data-stu-id="cf6bb-104">WMI checks access rights for applications and scripts for objects such as WMI namespaces, printer, services, DCOM applications, files, shares, and other securable objects.</span></span> <span data-ttu-id="cf6bb-105">Доступ к этим защищаемым объектам контролируется записями управления доступом (ACE).</span><span class="sxs-lookup"><span data-stu-id="cf6bb-105">Access to theses securable objects is controlled by access control entries (ACE).</span></span> <span data-ttu-id="cf6bb-106">Каждый элемент ACE содержит списки, которые определяют, к каким группам или пользователям имеет доступ.</span><span class="sxs-lookup"><span data-stu-id="cf6bb-106">Each ACE contains lists that designate which groups or users have access.</span></span> <span data-ttu-id="cf6bb-107">Дополнительные сведения о списках управления доступом и безопасности (ACL, DACL и SACL) см. в разделе [списки управления доступом (ACL)](/windows/desktop/SecAuthZ/access-control-lists) и [дескрипторы безопасности](/windows/desktop/SecAuthZ/security-descriptors).</span><span class="sxs-lookup"><span data-stu-id="cf6bb-107">For more information about security and access control lists (ACLs, DACLs, or SACLs), see [Access Control Lists (ACLs)](/windows/desktop/SecAuthZ/access-control-lists) and [Security Descriptors](/windows/desktop/SecAuthZ/security-descriptors).</span></span>

<span data-ttu-id="cf6bb-108">Многие методы поставщика в WMI, которые влияют на защищаемые объекты, требуют, чтобы администратор включил определенные привилегии.</span><span class="sxs-lookup"><span data-stu-id="cf6bb-108">Many provider methods in WMI that affect securable objects require the administrator to enable certain privileges.</span></span> <span data-ttu-id="cf6bb-109">Какая версия привилегий, которую вы используете, зависит от языка программирования, как показано в [**константах прав**](privilege-constants.md).</span><span class="sxs-lookup"><span data-stu-id="cf6bb-109">Which version of the privilege you use depends on the programming language, as shown in [**Privilege Constants**](privilege-constants.md).</span></span>

<span data-ttu-id="cf6bb-110">Константы безопасности определяются в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="cf6bb-110">The security constants are defined in the following topics:</span></span>

-   [<span data-ttu-id="cf6bb-111">**Константы безопасности событий**</span><span class="sxs-lookup"><span data-stu-id="cf6bb-111">**Event Security Constants**</span></span>](event-security-constants.md)
-   [<span data-ttu-id="cf6bb-112">**Константы прав доступа к файлам и каталогам**</span><span class="sxs-lookup"><span data-stu-id="cf6bb-112">**File and Directory Access Rights Constants**</span></span>](file-and-directory-access-rights-constants.md)
-   [<span data-ttu-id="cf6bb-113">**Константы прав доступа к пространству имен**</span><span class="sxs-lookup"><span data-stu-id="cf6bb-113">**Namespace Access Rights Constants**</span></span>](namespace-access-rights-constants.md)
-   [<span data-ttu-id="cf6bb-114">**Константы флагов пространства имен ACE**</span><span class="sxs-lookup"><span data-stu-id="cf6bb-114">**Namespace ACE Flag Constants**</span></span>](namespace-ace-flag-constants.md)
-   [<span data-ttu-id="cf6bb-115">**Константы типа ACE пространства имен**</span><span class="sxs-lookup"><span data-stu-id="cf6bb-115">**Namespace ACE Type Constants**</span></span>](namespace-ace-type-constants.md)
-   [<span data-ttu-id="cf6bb-116">**Константы прав доступа**</span><span class="sxs-lookup"><span data-stu-id="cf6bb-116">**Privilege Constants**</span></span>](privilege-constants.md)

 

 
