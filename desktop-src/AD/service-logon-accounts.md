---
title: Учетные записи входа в службу
description: Служба, как и любой процесс, имеет основное удостоверение безопасности, определяющее предоставленные права доступа и привилегии для локальных и сетевых ресурсов.
ms.assetid: c2345967-8415-4cc0-96d3-12c48e74028e
ms.tgt_platform: multiple
keywords:
- Active Directory, использование службы, вход в службу
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9340fe7eebc95ec4c7ea3091c96a2539cb08dee4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103887619"
---
# <a name="service-logon-accounts"></a><span data-ttu-id="2b60d-104">Учетные записи входа в службу</span><span class="sxs-lookup"><span data-stu-id="2b60d-104">Service Logon Accounts</span></span>

<span data-ttu-id="2b60d-105">Служба, как и любой процесс, имеет основное удостоверение безопасности, определяющее предоставленные права доступа и привилегии для локальных и сетевых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2b60d-105">A service, like any process, has a primary security identity that determines the granted access rights and privileges for local and network resources.</span></span> <span data-ttu-id="2b60d-106">Это удостоверение безопасности, или контекст безопасности, также определяет потенциальную службу для повреждения локальных и сетевых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2b60d-106">This security identity, or security context, also determines the potential the service has for damaging local and network resources.</span></span>

<span data-ttu-id="2b60d-107">Контекст безопасности для службы Microsoft Win32 определяется учетной записью входа, используемой для запуска службы.</span><span class="sxs-lookup"><span data-stu-id="2b60d-107">The security context for a Microsoft Win32 service is determined by the logon account that is used to start the service.</span></span> <span data-ttu-id="2b60d-108">В этом разделе рассматриваются вопросы программирования и рекомендации по использованию учетной записи входа в службу, используемой службами Win32, и основное внимание уделяется службам, поддерживающим каталог.</span><span class="sxs-lookup"><span data-stu-id="2b60d-108">This section discusses programming issues and best practices relating to the service logon account used by Win32 services, with a focus on directory-enabled services.</span></span> <span data-ttu-id="2b60d-109">Этот раздел содержит следующие подразделы:</span><span class="sxs-lookup"><span data-stu-id="2b60d-109">This section includes the following topics:</span></span>

-   <span data-ttu-id="2b60d-110">[О учетных записях входа](about-service-logon-accounts.md)в службу — обзор учетных записей входа в службу и проблем программирования контекста безопасности для службы Win32.</span><span class="sxs-lookup"><span data-stu-id="2b60d-110">[About Service Logon Accounts](about-service-logon-accounts.md)—An overview of service logon accounts and security context programming issues for a Win32 service.</span></span>
-   <span data-ttu-id="2b60d-111">[Рекомендации по выбору учетной записи входа службы](guidelines-for-selecting-a-service-logon-account.md) для службы Win32.</span><span class="sxs-lookup"><span data-stu-id="2b60d-111">[Guidelines for Selecting a Service Logon Account](guidelines-for-selecting-a-service-logon-account.md) for a Win32 service.</span></span>
-   <span data-ttu-id="2b60d-112">[Настройка учетной записи пользователя службы](setting-up-a-serviceampaposs-user-account.md).</span><span class="sxs-lookup"><span data-stu-id="2b60d-112">[Setting up a Service's User Account](setting-up-a-serviceampaposs-user-account.md).</span></span>
-   <span data-ttu-id="2b60d-113">[Установка службы на главном компьютере](installing-a-service-on-a-host-computer.md) и указание учетной записи входа в службу.</span><span class="sxs-lookup"><span data-stu-id="2b60d-113">[Installing a Service on a Host Computer](installing-a-service-on-a-host-computer.md) and specifying the service logon account.</span></span>
-   <span data-ttu-id="2b60d-114">Предоставление учетной записи для [входа в качестве службы непосредственно на главном компьютере](granting-logon-as-service-right-on-the-host-computer.md), предоставляющая вход пользователя службы в качестве службы непосредственно на главном компьютере.</span><span class="sxs-lookup"><span data-stu-id="2b60d-114">[Granting Logon as Service Right on the Host Computer](granting-logon-as-service-right-on-the-host-computer.md)—Granting the service's user account the logon as a service right on the host computer.</span></span>
-   <span data-ttu-id="2b60d-115">[Проверка работы на контроллере домена](testing-whether-running-on-a-domain-controller.md)— обнаружение во время установки экземпляра службы, установленного на контроллере домена.</span><span class="sxs-lookup"><span data-stu-id="2b60d-115">[Testing Whether Running on a Domain Controller](testing-whether-running-on-a-domain-controller.md)—Detecting at installation time whether the service instance is being installed on a domain controller.</span></span>
-   <span data-ttu-id="2b60d-116">[Предоставление прав доступа учетной записи входа в службу](granting-access-rights-to-the-service-logon-account.md)— Настройка и обслуживание записей ACE и членства в группах, чтобы гарантировать, что система предоставит работающей службе доступ к необходимым локальным и сетевым ресурсам.</span><span class="sxs-lookup"><span data-stu-id="2b60d-116">[Granting Access Rights to the Service Logon Account](granting-access-rights-to-the-service-logon-account.md)—Setting and maintaining ACEs and group memberships to ensure that the system will grant the running service access to the necessary local and network resources.</span></span>
-   <span data-ttu-id="2b60d-117">[Изменение пароля учетной записи пользователя службы](changing-the-password-on-a-serviceampaposs-user-account.md)— изменение пароля для учетной записи пользователя службы и одновременное обновление пароля, зарегистрированного диспетчером управления службами на каждом сервере узла, на котором установлена служба.</span><span class="sxs-lookup"><span data-stu-id="2b60d-117">[Changing the Password on a Service's User Account](changing-the-password-on-a-serviceampaposs-user-account.md)—Changing the password on a service's user account, and at the same time updating the password registered with the service control manager on each host server on which the service is installed.</span></span>
-   <span data-ttu-id="2b60d-118">[Взаимная проверка подлинности с помощью Kerberos](mutual-authentication-using-kerberos.md)— регистрация имени участника-службы (SPN) для объекта каталога, связанного с учетной записью входа каждого экземпляра службы.</span><span class="sxs-lookup"><span data-stu-id="2b60d-118">[Mutual Authentication Using Kerberos](mutual-authentication-using-kerberos.md)—Maintaining service principal name (SPN) registration on the directory object associated with the logon account of each instance of your service.</span></span> <span data-ttu-id="2b60d-119">Имена участников-служб позволяют клиентам проверять подлинность службы с помощью взаимной проверки подлинности Kerberos.</span><span class="sxs-lookup"><span data-stu-id="2b60d-119">SPNs enable clients to authenticate a service using Kerberos mutual authentication.</span></span>
-   <span data-ttu-id="2b60d-120">[Преобразование форматов имен учетных записей домена](converting-domain-account-name-formats.md)— например, преобразование различающегося имени в *Формат ***\\*** имени пользователя домена* и наоборот.</span><span class="sxs-lookup"><span data-stu-id="2b60d-120">[Converting Domain Account Name Formats](converting-domain-account-name-formats.md)—For example, converting a distinguished name to *Domain ***\\*** UserName* format, and vice versa.</span></span>

 

 




