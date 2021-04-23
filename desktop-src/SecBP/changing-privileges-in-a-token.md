---
description: Объясняет, как изменить привилегии в токене с помощью функций AdjustTokenPrivileges и CreateRestrictedToken.
ms.assetid: b8e47d04-07c1-4d57-8209-6b0c397476e5
title: Изменение привилегий в токене
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a8b77d966acf90db101269b77a767550bcae3ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664410"
---
# <a name="changing-privileges-in-a-token"></a><span data-ttu-id="ba631-103">Изменение привилегий в токене</span><span class="sxs-lookup"><span data-stu-id="ba631-103">Changing Privileges in a Token</span></span>

<span data-ttu-id="ba631-104">Вы можете изменить привилегии в первичном или токене олицетворения двумя способами:</span><span class="sxs-lookup"><span data-stu-id="ba631-104">You can change the privileges in either a primary or an impersonation token in two ways:</span></span>

-   <span data-ttu-id="ba631-105">Включите или отключите привилегии с помощью функции [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) .</span><span class="sxs-lookup"><span data-stu-id="ba631-105">Enable or disable privileges by using the [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) function.</span></span>
-   <span data-ttu-id="ba631-106">Ограничьте или удалите привилегии с помощью функции [**CreateRestrictedToken**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) .</span><span class="sxs-lookup"><span data-stu-id="ba631-106">Restrict or remove privileges by using the [**CreateRestrictedToken**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) function.</span></span>

<span data-ttu-id="ba631-107">[**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) не может добавлять или удалять привилегии из токена.</span><span class="sxs-lookup"><span data-stu-id="ba631-107">[**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) cannot add or remove privileges from the token.</span></span> <span data-ttu-id="ba631-108">Он может включать только существующие привилегии, которые в настоящее время отключены, или отключать существующие привилегии, которые в настоящее время включены.</span><span class="sxs-lookup"><span data-stu-id="ba631-108">It can only enable existing privileges that are currently disabled or disable existing privileges that are currently enabled.</span></span> <span data-ttu-id="ba631-109">Примеры см. [в разделе Включение и отключение привилегий в C++](/windows/desktop/SecAuthZ/enabling-and-disabling-privileges-in-c--).</span><span class="sxs-lookup"><span data-stu-id="ba631-109">For examples, see [Enabling and Disabling Privileges in C++](/windows/desktop/SecAuthZ/enabling-and-disabling-privileges-in-c--).</span></span>

<span data-ttu-id="ba631-110">Чтобы назначить привилегии учетной записи пользователя, см. раздел [назначение привилегий учетной записи](assigning-privileges-to-an-account.md).</span><span class="sxs-lookup"><span data-stu-id="ba631-110">To assign privileges to a user account, see [Assigning Privileges to an Account](assigning-privileges-to-an-account.md).</span></span>

<span data-ttu-id="ba631-111">[**CreateRestrictedToken**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) обладает более широкими возможностями, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="ba631-111">[**CreateRestrictedToken**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) has more extensive capabilities as follows:</span></span>

-   <span data-ttu-id="ba631-112">Удаление привилегий.</span><span class="sxs-lookup"><span data-stu-id="ba631-112">Removing a privilege.</span></span> <span data-ttu-id="ba631-113">Обратите внимание, что удаление привилегий не так же, как и при ее отключении.</span><span class="sxs-lookup"><span data-stu-id="ba631-113">Note that removing a privilege is not the same as disabling one.</span></span> <span data-ttu-id="ba631-114">После удаления привилегий из токена ее нельзя вернуть обратно.</span><span class="sxs-lookup"><span data-stu-id="ba631-114">After a privilege is removed from a token, it cannot be put back.</span></span>
-   <span data-ttu-id="ba631-115">Присоединение атрибута Deny-only к идентификаторам безопасности в токене.</span><span class="sxs-lookup"><span data-stu-id="ba631-115">Attaching the deny-only attribute to SIDs in the token.</span></span> <span data-ttu-id="ba631-116">Это позволяет запретить доступ к определенному файлу для определенных групп или учетных записей, например для запрета доступа к группе Everyone.</span><span class="sxs-lookup"><span data-stu-id="ba631-116">This has the effect of disallowing specific groups or accounts, for example, denying the Everyone group delete access to a particular file.</span></span> <span data-ttu-id="ba631-117">Дополнительные сведения о том, как ограничивать идентификаторы безопасности, см. [в разделе атрибуты SID в маркере доступа](/windows/desktop/SecAuthZ/sid-attributes-in-an-access-token).</span><span class="sxs-lookup"><span data-stu-id="ba631-117">For more information on restricting SIDs, see [SID Attributes in an Access Token](/windows/desktop/SecAuthZ/sid-attributes-in-an-access-token).</span></span>
-   <span data-ttu-id="ba631-118">Указание списка запрещенных идентификаторов безопасности в токене.</span><span class="sxs-lookup"><span data-stu-id="ba631-118">Specifying a list of restricting SIDs in the token.</span></span> <span data-ttu-id="ba631-119">Дополнительные сведения об ограничении идентификаторов безопасности см. в разделе [ограничения токенов](/windows/desktop/SecAuthZ/restricted-tokens).</span><span class="sxs-lookup"><span data-stu-id="ba631-119">For information about restricting SIDs, see [Restricted Tokens](/windows/desktop/SecAuthZ/restricted-tokens).</span></span>

 

 
