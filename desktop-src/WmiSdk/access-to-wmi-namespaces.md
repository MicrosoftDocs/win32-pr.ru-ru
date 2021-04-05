---
description: Инструментарий WMI использует стандартный дескриптор безопасности Windows для управления доступом к пространствам имен WMI.
ms.assetid: 5cf9886c-04fa-480e-889f-b64a6a70d053
ms.tgt_platform: multiple
title: Доступ к пространствам имен WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6eaebe5370e97dcb42ddcf79018015ceff9147f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999381"
---
# <a name="access-to-wmi-namespaces"></a><span data-ttu-id="f4dcf-103">Доступ к пространствам имен WMI</span><span class="sxs-lookup"><span data-stu-id="f4dcf-103">Access to WMI Namespaces</span></span>

<span data-ttu-id="f4dcf-104">Инструментарий WMI использует стандартный *дескриптор безопасности* Windows для управления доступом к пространствам имен WMI.</span><span class="sxs-lookup"><span data-stu-id="f4dcf-104">WMI uses a standard Windows *security descriptor* to control access to WMI namespaces.</span></span> <span data-ttu-id="f4dcf-105">При подключении к WMI с помощью моникера WMI "винмгмтс" или вызова [**ивбемлокатор:: коннектсервер**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) или [**SWbemLocator. коннектсервер**](swbemlocator-connectserver.md)вы подключаетесь к определенному пространству имен.</span><span class="sxs-lookup"><span data-stu-id="f4dcf-105">When you connect to WMI, either through the WMI "winmgmts" moniker or a call to [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) or [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md), you connect to a specific namespace.</span></span>

<span data-ttu-id="f4dcf-106">В этом разделе рассматриваются следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="f4dcf-106">The following information is discussed in this topic:</span></span>

-   [<span data-ttu-id="f4dcf-107">Безопасность пространства имен WMI</span><span class="sxs-lookup"><span data-stu-id="f4dcf-107">WMI Namespace Security</span></span>](#wmi-namespace-security)
-   [<span data-ttu-id="f4dcf-108">Аудит пространства имен WMI</span><span class="sxs-lookup"><span data-stu-id="f4dcf-108">WMI Namespace Auditing</span></span>](#wmi-namespace-auditing)
-   [<span data-ttu-id="f4dcf-109">Типы событий пространства имен</span><span class="sxs-lookup"><span data-stu-id="f4dcf-109">Types of Namespace Events</span></span>](#types-of-namespace-events)
-   [<span data-ttu-id="f4dcf-110">Параметры доступа к пространству имен</span><span class="sxs-lookup"><span data-stu-id="f4dcf-110">Namespace Access Settings</span></span>](#namespace-access-settings)
-   [<span data-ttu-id="f4dcf-111">Разрешения по умолчанию для пространств имен WMI</span><span class="sxs-lookup"><span data-stu-id="f4dcf-111">Default Permissions on WMI Namespaces</span></span>](#default-permissions-on-wmi-namespaces)
-   [<span data-ttu-id="f4dcf-112">См. также</span><span class="sxs-lookup"><span data-stu-id="f4dcf-112">Related topics</span></span>](#related-topics)

## <a name="wmi-namespace-security"></a><span data-ttu-id="f4dcf-113">Безопасность пространства имен WMI</span><span class="sxs-lookup"><span data-stu-id="f4dcf-113">WMI Namespace Security</span></span>

<span data-ttu-id="f4dcf-114">WMI обеспечивает безопасность пространства имен, сравнивая [*маркер доступа*](/windows/desktop/SecGloss/a-gly) пользователя, подключающегося к пространству имен, с [*дескриптором безопасности*](/windows/desktop/SecGloss/s-gly) пространства имен.</span><span class="sxs-lookup"><span data-stu-id="f4dcf-114">WMI maintains namespace security by comparing the [*access token*](/windows/desktop/SecGloss/a-gly) of the user connecting to the namespace with the [*security descriptor*](/windows/desktop/SecGloss/s-gly) of the namespace.</span></span> <span data-ttu-id="f4dcf-115">Дополнительные сведения о безопасности Windows см. [в разделе доступ к защищаемым ОБЪЕКТАМ WMI](access-to-wmi-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="f4dcf-115">For more information about Windows security, see [Access to WMI Securable Objects](access-to-wmi-securable-objects.md).</span></span>

<span data-ttu-id="f4dcf-116">Имейте в виду, что начиная с Windows Vista [Управление учетными записями пользователей (UAC)](https://www.microsoft.com/technet/windowsvista/security/uac.mspx) влияет на доступ к данным WMI и что может быть настроено с помощью [*элемента управления WMI*](gloss-w.md).</span><span class="sxs-lookup"><span data-stu-id="f4dcf-116">Be aware that, starting with Windows Vista, [User Account Control (UAC)](https://www.microsoft.com/technet/windowsvista/security/uac.mspx) affects access to WMI data and what can be configured with the [*WMI Control*](gloss-w.md).</span></span> <span data-ttu-id="f4dcf-117">Дополнительные сведения см. [в разделе разрешения по умолчанию для пространств имен WMI](#default-permissions-on-wmi-namespaces) и [Управление учетными записями пользователей и WMI](user-account-control-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="f4dcf-117">For more information, see [Default Permissions on WMI Namespaces](#default-permissions-on-wmi-namespaces) and [User Account Control and WMI](user-account-control-and-wmi.md).</span></span>

<span data-ttu-id="f4dcf-118">Доступ к пространствам имен WMI также влияет на подключение к удаленному компьютеру.</span><span class="sxs-lookup"><span data-stu-id="f4dcf-118">Access to WMI namespaces is also affected when the connection is from a remote computer.</span></span> <span data-ttu-id="f4dcf-119">Дополнительные сведения см. в статьях [Подключение к WMI на удаленном компьютере](connecting-to-wmi-on-a-remote-computer.md), [Защита удаленного WMI-подключения](securing-a-remote-wmi-connection.md)и [подключение через брандмауэр Windows](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista).</span><span class="sxs-lookup"><span data-stu-id="f4dcf-119">For more information, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md), [Securing a Remote WMI Connection](securing-a-remote-wmi-connection.md), and [Connecting Through Windows Firewall](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista).</span></span>

<span data-ttu-id="f4dcf-120">Чтобы определить, должен ли клиентский скрипт или приложение принимать данные, поставщики должны использовать параметр олицетворения.</span><span class="sxs-lookup"><span data-stu-id="f4dcf-120">Providers must rely on the impersonation setting for the connection to determine if the client script or application should receive data.</span></span> <span data-ttu-id="f4dcf-121">Дополнительные сведения о скриптах и клиентских приложениях см. в разделе [Установка параметров безопасности процессов для клиентских приложений](setting-client-application-process-security.md).</span><span class="sxs-lookup"><span data-stu-id="f4dcf-121">For more information about script and client applications, see [Setting Client Application Process Security](setting-client-application-process-security.md).</span></span> <span data-ttu-id="f4dcf-122">Дополнительные сведения об олицетворении [*поставщика*](gloss-p.md) см. в разделе [Разработка поставщика WMI](developing-a-wmi-provider.md).</span><span class="sxs-lookup"><span data-stu-id="f4dcf-122">For more information about [*provider*](gloss-p.md) impersonation, see [Developing a WMI Provider](developing-a-wmi-provider.md).</span></span>

## <a name="wmi-namespace-auditing"></a><span data-ttu-id="f4dcf-123">Аудит пространства имен WMI</span><span class="sxs-lookup"><span data-stu-id="f4dcf-123">WMI Namespace Auditing</span></span>

<span data-ttu-id="f4dcf-124">Инструментарий WMI использует [*системные списки управления доступом (SACL)*](/windows/desktop/SecGloss/s-gly) пространства имен для аудита действий пространства имен.</span><span class="sxs-lookup"><span data-stu-id="f4dcf-124">WMI uses the namespace [*System access control lists (SACL)*](/windows/desktop/SecGloss/s-gly) to audit namespace activity.</span></span> <span data-ttu-id="f4dcf-125">Чтобы включить аудит пространств имен WMI, используйте вкладку **Безопасность** в [*элементе управления WMI*](gloss-w.md) , чтобы изменить параметры аудита для пространства имен.</span><span class="sxs-lookup"><span data-stu-id="f4dcf-125">To enable auditing of WMI namespaces, use the **Security** tab on the [*WMI Control*](gloss-w.md) to change the auditing settings for the namespace.</span></span>

<span data-ttu-id="f4dcf-126">Аудит не включен во время установки операционной системы.</span><span class="sxs-lookup"><span data-stu-id="f4dcf-126">Auditing is not enabled during the installation of the operating system.</span></span> <span data-ttu-id="f4dcf-127">Чтобы включить аудит, перейдите на вкладку **Аудит** в окне Стандартная **Безопасность** .</span><span class="sxs-lookup"><span data-stu-id="f4dcf-127">To enable auditing, click the **Auditing** tab in the standard **Security** window.</span></span> <span data-ttu-id="f4dcf-128">Затем можно добавить запись аудита.</span><span class="sxs-lookup"><span data-stu-id="f4dcf-128">Then you can add an auditing entry.</span></span>

<span data-ttu-id="f4dcf-129">Групповая политика для локального компьютера должно быть настроено для разрешения аудита.</span><span class="sxs-lookup"><span data-stu-id="f4dcf-129">Group Policy for the local computer must be set to allow auditing.</span></span> <span data-ttu-id="f4dcf-130">Аудит можно включить, запустив оснастку MMC gpedit. msc и настроив **доступ к объектам аудита** в разделе **Конфигурация компьютера** Настройка  >  **Windows параметры**  >  **безопасности**  >  **Локальные политики**  >  **аудит политика**.</span><span class="sxs-lookup"><span data-stu-id="f4dcf-130">You can enable auditing by running the Gpedit.msc MMC snap-in and setting **Audit Object Access** under **Computer Configuration** > **Windows Settings** > **Security Settings** > **Local Policies** > **Audit Policy**.</span></span>

<span data-ttu-id="f4dcf-131">Запись аудита изменяет список SACL пространства имен.</span><span class="sxs-lookup"><span data-stu-id="f4dcf-131">An auditing entry edits the SACL of the namespace.</span></span> <span data-ttu-id="f4dcf-132">При добавлении записи аудита это может быть пользователь, группа, компьютер или встроенный субъект безопасности.</span><span class="sxs-lookup"><span data-stu-id="f4dcf-132">When you add an auditing entry, it is either a user, group, computer, or built-in security principal.</span></span> <span data-ttu-id="f4dcf-133">После добавления записи можно задать операции доступа, которые приводят к событиям журнала безопасности.</span><span class="sxs-lookup"><span data-stu-id="f4dcf-133">After adding the entry, you can set the access operations that result in Security Log events.</span></span> <span data-ttu-id="f4dcf-134">Например, для пользователей, прошедших проверку подлинности группы, можно нажать кнопку выполнить методы.</span><span class="sxs-lookup"><span data-stu-id="f4dcf-134">For example, for the group Authenticated Users, you can click Execute Methods.</span></span> <span data-ttu-id="f4dcf-135">Этот параметр приводит к возникновению событий журнала безопасности каждый раз, когда член группы «Пользователи, прошедшие проверку подлинности» выполняет метод в этом пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="f4dcf-135">This setting results in Security Log events whenever a member of the Authenticated Users group executes a method in that namespace.</span></span> <span data-ttu-id="f4dcf-136">Идентификатор события для событий WMI — 4662.</span><span class="sxs-lookup"><span data-stu-id="f4dcf-136">The Event ID for WMI events is 4662.</span></span>

<span data-ttu-id="f4dcf-137">Чтобы изменить параметры аудита, ваша учетная запись должна быть в группе администраторов и запущена с повышенными привилегиями.</span><span class="sxs-lookup"><span data-stu-id="f4dcf-137">Your account must be in the Administrators group and running under elevated privilege to change the auditing settings.</span></span> <span data-ttu-id="f4dcf-138">Встроенная учетная запись администратора также может изменить безопасность или аудит пространства имен.</span><span class="sxs-lookup"><span data-stu-id="f4dcf-138">The built-in Administrator account can also change the security or auditing for a namespace.</span></span> <span data-ttu-id="f4dcf-139">Дополнительные сведения о работе в режиме с повышенными правами см. в разделе [Управление учетными записями пользователей и инструментарий WMI](user-account-control-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="f4dcf-139">For more information about running in elevated mode, see [User Account Control and WMI](user-account-control-and-wmi.md).</span></span>

<span data-ttu-id="f4dcf-140">Аудит WMI создает события успешных или неудачных попыток доступа к пространствам имен WMI.</span><span class="sxs-lookup"><span data-stu-id="f4dcf-140">WMI auditing generates success or failure events for attempts to access WMI namespaces.</span></span> <span data-ttu-id="f4dcf-141">Служба не выполняет аудит успешных или неудачных операций поставщика.</span><span class="sxs-lookup"><span data-stu-id="f4dcf-141">The service does not audit the success or failure of provider operations.</span></span> <span data-ttu-id="f4dcf-142">Например, при подключении сценария к WMI и пространству имен может произойти сбой, так как учетная запись, под которой выполняется сценарий, не имеет доступа к этому пространству имен или может пытаться выполнить операцию, например изменение списка DACL, которое не предоставлено.</span><span class="sxs-lookup"><span data-stu-id="f4dcf-142">For example, when a script connects to WMI and a namespace, it may fail because the account under which the script is running does not have access to that the namespace or may attempt an operation, such as editing the DACL, that is not granted.</span></span>

<span data-ttu-id="f4dcf-143">Если вы используете учетную запись в группе "Администраторы", то можете просмотреть события аудита пространства имен в **Просмотр событий** пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="f4dcf-143">If you are running under an account in the Administrators group, you can view the namespace auditing events in the **Event Viewer** user interface.</span></span>

## <a name="types-of-namespace-events"></a><span data-ttu-id="f4dcf-144">Типы событий пространства имен</span><span class="sxs-lookup"><span data-stu-id="f4dcf-144">Types of Namespace Events</span></span>

<span data-ttu-id="f4dcf-145">Инструментарий WMI отслеживает в журнале событий безопасности следующие типы событий:</span><span class="sxs-lookup"><span data-stu-id="f4dcf-145">WMI traces the following types of events in the Security Event Log:</span></span>

-   <span data-ttu-id="f4dcf-146">Аудит выполнен успешно</span><span class="sxs-lookup"><span data-stu-id="f4dcf-146">Audit Success</span></span>

    <span data-ttu-id="f4dcf-147">Операция должна успешно завершить два шага для успешного выполнения аудита.</span><span class="sxs-lookup"><span data-stu-id="f4dcf-147">The operation must successfully complete two steps for an Audit Success.</span></span> <span data-ttu-id="f4dcf-148">Во первых, WMI предоставляет доступ к клиентскому приложению или скрипту на основе идентификатора безопасности клиента и DACL пространства имен.</span><span class="sxs-lookup"><span data-stu-id="f4dcf-148">First, WMI grants access to the client application or script based on the client SID and the namespace DACL.</span></span> <span data-ttu-id="f4dcf-149">Во вторых, запрошенная операция соответствует правам доступа в списке SACL пространства имен для этого пользователя или группы.</span><span class="sxs-lookup"><span data-stu-id="f4dcf-149">Second, the requested operation matches the access rights in the namespace SACL for that user or group.</span></span>

-   <span data-ttu-id="f4dcf-150">Сбой аудита</span><span class="sxs-lookup"><span data-stu-id="f4dcf-150">Audit Failure</span></span>

    <span data-ttu-id="f4dcf-151">Инструментарий WMI запрещает доступ к пространству имен, но запрошенная операция соответствует правам доступа в списке SACL пространства имен для этого пользователя или группы.</span><span class="sxs-lookup"><span data-stu-id="f4dcf-151">WMI denies access to the namespace, but the requested operation matches the access rights in the namespace SACL for that user or group.</span></span>

## <a name="namespace-access-settings"></a><span data-ttu-id="f4dcf-152">Параметры доступа к пространству имен</span><span class="sxs-lookup"><span data-stu-id="f4dcf-152">Namespace Access Settings</span></span>

<span data-ttu-id="f4dcf-153">Вы можете просмотреть права доступа к пространству имен для различных учетных записей в элементе управления WMI.</span><span class="sxs-lookup"><span data-stu-id="f4dcf-153">You can view the namespace access rights for various accounts on the WMI Control.</span></span> <span data-ttu-id="f4dcf-154">Эти константы описаны в статье [**константы прав доступа к пространству имен**](namespace-access-rights-constants.md).</span><span class="sxs-lookup"><span data-stu-id="f4dcf-154">These constants are described in [**Namespace Access Rights Constants**](namespace-access-rights-constants.md).</span></span> <span data-ttu-id="f4dcf-155">Доступ к пространству имен WMI можно изменить с помощью элемента управления WMI или программно.</span><span class="sxs-lookup"><span data-stu-id="f4dcf-155">You can change the access to a WMI namespace using the WMI Control or programmatically.</span></span> <span data-ttu-id="f4dcf-156">Дополнительные сведения см. [в разделе Изменение параметров безопасности доступа к защищаемым объектам](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="f4dcf-156">For more information, see [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

<span data-ttu-id="f4dcf-157">WMI выполняет аудит изменений во всех разрешениях на доступ, перечисленных в следующем списке, за исключением разрешения на удаленную включение.</span><span class="sxs-lookup"><span data-stu-id="f4dcf-157">WMI audits changes in all of the access permissions listed in the following list except for the Remote Enable permission.</span></span> <span data-ttu-id="f4dcf-158">Изменения регистрируются при успешном аудите или сбое, соответствующем разрешению на изменение безопасности.</span><span class="sxs-lookup"><span data-stu-id="f4dcf-158">The changes are logged as audit success or failure corresponding to the Edit Security permission.</span></span>

<dl> <dt>

<span data-ttu-id="f4dcf-159"><span id="Execute_Methods"></span><span id="execute_methods"></span><span id="EXECUTE_METHODS"></span>Выполнение методов</span><span class="sxs-lookup"><span data-stu-id="f4dcf-159"><span id="Execute_Methods"></span><span id="execute_methods"></span><span id="EXECUTE_METHODS"></span>Execute Methods</span></span>
</dt> <dd>

<span data-ttu-id="f4dcf-160">Разрешает пользователю выполнять методы, определенные в классах WMI.</span><span class="sxs-lookup"><span data-stu-id="f4dcf-160">Permits the user to execute methods defined on WMI classes.</span></span> <span data-ttu-id="f4dcf-161">Соответствует константе разрешения на **\_ \_ выполнение метода WBEM** .</span><span class="sxs-lookup"><span data-stu-id="f4dcf-161">Corresponds to the **WBEM\_METHOD\_EXECUTE** access permission constant.</span></span>

</dd> <dt>

<span data-ttu-id="f4dcf-162"><span id="Full_Write"></span><span id="full_write"></span><span id="FULL_WRITE"></span>Полная запись</span><span class="sxs-lookup"><span data-stu-id="f4dcf-162"><span id="Full_Write"></span><span id="full_write"></span><span id="FULL_WRITE"></span>Full Write</span></span>
</dt> <dd>

<span data-ttu-id="f4dcf-163">Разрешает полный доступ для чтения, записи и удаления к классам и экземплярам классов WMI, как статическим, так и динамическим.</span><span class="sxs-lookup"><span data-stu-id="f4dcf-163">Permits full read, write, and delete access to WMI classes and class instances, both static and dynamic.</span></span> <span data-ttu-id="f4dcf-164">Соответствует константе разрешения на доступ **\_ \_ \_ представителя полной записи** .</span><span class="sxs-lookup"><span data-stu-id="f4dcf-164">Corresponds to the **WBEM\_FULL\_WRITE\_REP** access permission constant.</span></span>

</dd> <dt>

<span data-ttu-id="f4dcf-165"><span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>Частичная запись</span><span class="sxs-lookup"><span data-stu-id="f4dcf-165"><span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>Partial Write</span></span>
</dt> <dd>

<span data-ttu-id="f4dcf-166">Разрешает доступ на запись к статическим экземплярам классов WMI.</span><span class="sxs-lookup"><span data-stu-id="f4dcf-166">Permits write access to static WMI class instances.</span></span> <span data-ttu-id="f4dcf-167">Соответствует константе разрешения на доступ для **\_ частичной \_ записи \_ для WBEM** .</span><span class="sxs-lookup"><span data-stu-id="f4dcf-167">Corresponds to the **WBEM\_PARTIAL\_WRITE\_REP** access permission constant.</span></span>

</dd> <dt>

<span data-ttu-id="f4dcf-168"><span id="Provider_Write"></span><span id="provider_write"></span><span id="PROVIDER_WRITE"></span>Запись поставщика</span><span class="sxs-lookup"><span data-stu-id="f4dcf-168"><span id="Provider_Write"></span><span id="provider_write"></span><span id="PROVIDER_WRITE"></span>Provider Write</span></span>
</dt> <dd>

<span data-ttu-id="f4dcf-169">Разрешает доступ на запись к динамическим экземплярам классов WMI.</span><span class="sxs-lookup"><span data-stu-id="f4dcf-169">Permits write access to dynamic WMI class instances.</span></span> <span data-ttu-id="f4dcf-170">Соответствует константе разрешения доступа к **\_ \_ поставщику записи WBEM** .</span><span class="sxs-lookup"><span data-stu-id="f4dcf-170">Corresponds to the **WBEM\_WRITE\_PROVIDER** access permission constant.</span></span>

</dd> <dt>

<span data-ttu-id="f4dcf-171"><span id="Enable_Account"></span><span id="enable_account"></span><span id="ENABLE_ACCOUNT"></span>Включить учетную запись</span><span class="sxs-lookup"><span data-stu-id="f4dcf-171"><span id="Enable_Account"></span><span id="enable_account"></span><span id="ENABLE_ACCOUNT"></span>Enable Account</span></span>
</dt> <dd>

<span data-ttu-id="f4dcf-172">Разрешает доступ на чтение к экземплярам класса WMI.</span><span class="sxs-lookup"><span data-stu-id="f4dcf-172">Permits read access to WMI class instances.</span></span> <span data-ttu-id="f4dcf-173">Соответствует константе **WBEM \_** для разрешения доступа.</span><span class="sxs-lookup"><span data-stu-id="f4dcf-173">Corresponds to the **WBEM\_ENABLE** access permission constant.</span></span>

</dd> <dt>

<span data-ttu-id="f4dcf-174"><span id="Remote_Enable"></span><span id="remote_enable"></span><span id="REMOTE_ENABLE"></span>Включить удаленно</span><span class="sxs-lookup"><span data-stu-id="f4dcf-174"><span id="Remote_Enable"></span><span id="remote_enable"></span><span id="REMOTE_ENABLE"></span>Remote Enable</span></span>
</dt> <dd>

<span data-ttu-id="f4dcf-175">Разрешает доступ к пространству имен с удаленных компьютеров.</span><span class="sxs-lookup"><span data-stu-id="f4dcf-175">Permits access to the namespace by remote computers.</span></span> <span data-ttu-id="f4dcf-176">Соответствует константе разрешения на доступ для **\_ удаленного \_ доступа WBEM** .</span><span class="sxs-lookup"><span data-stu-id="f4dcf-176">Corresponds to the **WBEM\_REMOTE\_ACCESS** access permission constant.</span></span>

</dd> <dt>

<span data-ttu-id="f4dcf-177"><span id="Read_Security"></span><span id="read_security"></span><span id="READ_SECURITY"></span>Чтение безопасности</span><span class="sxs-lookup"><span data-stu-id="f4dcf-177"><span id="Read_Security"></span><span id="read_security"></span><span id="READ_SECURITY"></span>Read Security</span></span>
</dt> <dd>

<span data-ttu-id="f4dcf-178">Разрешает доступ только для чтения к параметрам DACL.</span><span class="sxs-lookup"><span data-stu-id="f4dcf-178">Permits read-only access to DACL settings.</span></span> <span data-ttu-id="f4dcf-179">Соответствует константе разрешения на **\_ Управление** доступом на чтение.</span><span class="sxs-lookup"><span data-stu-id="f4dcf-179">Corresponds to the **READ\_CONTROL** access permission constant.</span></span>

</dd> <dt>

<span data-ttu-id="f4dcf-180"><span id="Edit_Security"></span><span id="edit_security"></span><span id="EDIT_SECURITY"></span>Изменить безопасность</span><span class="sxs-lookup"><span data-stu-id="f4dcf-180"><span id="Edit_Security"></span><span id="edit_security"></span><span id="EDIT_SECURITY"></span>Edit Security</span></span>
</dt> <dd>

<span data-ttu-id="f4dcf-181">Разрешает доступ на запись к параметрам DACL.</span><span class="sxs-lookup"><span data-stu-id="f4dcf-181">Permits write access to DACL settings.</span></span> <span data-ttu-id="f4dcf-182">Соответствует константе разрешения на доступ для **записи \_ DAC** .</span><span class="sxs-lookup"><span data-stu-id="f4dcf-182">Corresponds to the **WRITE\_DAC** access permission constant.</span></span>

</dd> </dl>

## <a name="default-permissions-on-wmi-namespaces"></a><span data-ttu-id="f4dcf-183">Разрешения по умолчанию для пространств имен WMI</span><span class="sxs-lookup"><span data-stu-id="f4dcf-183">Default Permissions on WMI Namespaces</span></span>

<span data-ttu-id="f4dcf-184">Группы безопасности по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="f4dcf-184">The default security groups are:</span></span>

-   <span data-ttu-id="f4dcf-185">Прошедшие проверку пользователи</span><span class="sxs-lookup"><span data-stu-id="f4dcf-185">Authenticated Users</span></span>
-   <span data-ttu-id="f4dcf-186">LOCAL SERVICE</span><span class="sxs-lookup"><span data-stu-id="f4dcf-186">LOCAL SERVICE</span></span>
-   <span data-ttu-id="f4dcf-187">СЕТЕВАЯ СЛУЖБА</span><span class="sxs-lookup"><span data-stu-id="f4dcf-187">NETWORK SERVICE</span></span>
-   <span data-ttu-id="f4dcf-188">Администраторы (на локальном компьютере)</span><span class="sxs-lookup"><span data-stu-id="f4dcf-188">Administrators (on the local computer)</span></span>

<span data-ttu-id="f4dcf-189">Разрешения на доступ по умолчанию для пользователей, прошедших проверку подлинности, ЛОКАЛЬную службу и СЕТЕВую службу:</span><span class="sxs-lookup"><span data-stu-id="f4dcf-189">The default access permissions for the Authenticated Users, LOCAL SERVICE, and NETWORK SERVICE are:</span></span>

-   <span data-ttu-id="f4dcf-190">Выполнение методов</span><span class="sxs-lookup"><span data-stu-id="f4dcf-190">Execute Methods</span></span>
-   <span data-ttu-id="f4dcf-191">Полная запись</span><span class="sxs-lookup"><span data-stu-id="f4dcf-191">Full Write</span></span>
-   <span data-ttu-id="f4dcf-192">Включить учетную запись</span><span class="sxs-lookup"><span data-stu-id="f4dcf-192">Enable Account</span></span>

<span data-ttu-id="f4dcf-193">Учетные записи в группе "Администраторы" имеют все доступные права, включая изменение дескрипторов безопасности.</span><span class="sxs-lookup"><span data-stu-id="f4dcf-193">Accounts in the Administrators group have all rights available to them, including editing security descriptors.</span></span> <span data-ttu-id="f4dcf-194">Однако из-за контроля учетных записей (UAC) элемент управления WMI или скрипт должен работать с повышенной безопасностью.</span><span class="sxs-lookup"><span data-stu-id="f4dcf-194">However, because of User Account Control (UAC), the WMI Control or the script must be running at elevated security.</span></span> <span data-ttu-id="f4dcf-195">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](user-account-control-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="f4dcf-195">For more information, see [User Account Control and WMI](user-account-control-and-wmi.md).</span></span>

<span data-ttu-id="f4dcf-196">Иногда скрипт или приложение должны включать права администратора, например **SeSecurityPrivilege**, для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="f4dcf-196">Sometimes a script or application must enable an administrator privilege, such as **SeSecurityPrivilege**, to carry out an operation.</span></span> <span data-ttu-id="f4dcf-197">Например, сценарий может выполнить метод [**жетсекуритидескриптор**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-printer) класса [**\_ принтера Win32**](/windows/desktop/CIMWin32Prov/win32-printer) без **SeSecurityPrivilege** и получить сведения о безопасности в [*списке управления доступом на уровне пользователей (DACL)*](/windows/desktop/SecGloss/d-gly) [*дескриптора безопасности*](/windows/desktop/SecGloss/s-gly)объекта принтера.</span><span class="sxs-lookup"><span data-stu-id="f4dcf-197">For example, a script can execute the [**GetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-printer) method of the [**Win32\_Printer**](/windows/desktop/CIMWin32Prov/win32-printer) class without **SeSecurityPrivilege** and get the security information in the [*discretionary access control list (DACL)*](/windows/desktop/SecGloss/d-gly) of the printer object [*security descriptor*](/windows/desktop/SecGloss/s-gly).</span></span> <span data-ttu-id="f4dcf-198">Однако сведения о SACL не возвращаются в скрипт, если только привилегии **SeSecurityPrivilege** недоступны и не включены для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="f4dcf-198">However, the SACL information is not returned to the script unless the **SeSecurityPrivilege** privilege is available and enabled for the account.</span></span> <span data-ttu-id="f4dcf-199">Если у учетной записи нет доступных привилегий, ее нельзя включить.</span><span class="sxs-lookup"><span data-stu-id="f4dcf-199">If the account does not have the privilege available, then it cannot be enabled.</span></span> <span data-ttu-id="f4dcf-200">Дополнительные сведения см. в разделе [выполнение привилегированных операций](executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="f4dcf-200">For more information, see [Executing Privileged Operations](executing-privileged-operations.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f4dcf-201">См. также</span><span class="sxs-lookup"><span data-stu-id="f4dcf-201">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4dcf-202">Сведения об инструментарии WMI</span><span class="sxs-lookup"><span data-stu-id="f4dcf-202">About WMI</span></span>](about-wmi.md)
</dt> </dl>

 

 
