---
description: Инфраструктура VSS требует, чтобы инициаторы VSS, такие как приложения резервного копирования, могли функционировать как клиенты COM и как сервер.
ms.assetid: b01145c6-76ba-4a81-bca6-59c4ca488dac
title: Вопросы безопасности для запрашивающих стороны
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d3e989793dbf5a5dd1fac3224cf6f06958564de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345012"
---
# <a name="security-considerations-for-requesters"></a><span data-ttu-id="93593-103">Вопросы безопасности для запрашивающих стороны</span><span class="sxs-lookup"><span data-stu-id="93593-103">Security Considerations for Requesters</span></span>

<span data-ttu-id="93593-104">Инфраструктура VSS требует, чтобы инициаторы VSS, такие как приложения резервного копирования, могли функционировать как клиенты COM и как сервер.</span><span class="sxs-lookup"><span data-stu-id="93593-104">The VSS infrastructure requires VSS requesters, such as backup applications, to be able to function both as COM clients and as a server.</span></span>

<span data-ttu-id="93593-105">При работе в качестве сервера инициатор запроса предоставляет набор интерфейсов обратного вызова COM, которые могут быть вызваны внешними процессами (например, модулями записи или службой VSS).</span><span class="sxs-lookup"><span data-stu-id="93593-105">When acting as a server, a requester exposes a set of COM callback interfaces that can be invoked from external processes (such as writers or the VSS service).</span></span> <span data-ttu-id="93593-106">Таким образом, запрашивающие стороны должны безопасно управлять тем, какие клиенты COM могут выполнять входящие вызовы COM в процесс.</span><span class="sxs-lookup"><span data-stu-id="93593-106">Therefore, requesters need to securely manage which COM clients are able to make incoming COM calls into its process.</span></span>

<span data-ttu-id="93593-107">Аналогичным образом, запрашивающие стороны могут действовать как клиент COM для COM-интерфейсов API, предоставляемых модулем записи VSS или службой VSS.</span><span class="sxs-lookup"><span data-stu-id="93593-107">Similarly, requesters can act as a COM client for the COM APIs supplied by a VSS writer or by the VSS service.</span></span> <span data-ttu-id="93593-108">Параметры безопасности, зависящие от инициатора запроса, должны разрешать исходящим вызовам COM от инициатора запроса к этим другим процессам.</span><span class="sxs-lookup"><span data-stu-id="93593-108">The requester-specific security settings must allow outgoing COM calls from the requester to these other processes.</span></span>

<span data-ttu-id="93593-109">Простейшим механизмом управления проблемами безопасности инициатора запроса является выбор учетной записи пользователя, от имени которой она выполняется.</span><span class="sxs-lookup"><span data-stu-id="93593-109">The simplest mechanism for managing a requester's security issues involves proper selection of the user account under which it runs.</span></span>

<span data-ttu-id="93593-110">Инициатор запроса обычно должен выполняться от имени пользователя, который является членом группы "Администраторы" или "операторы резервного копирования", или выполнять от имени учетной записи локальной системы.</span><span class="sxs-lookup"><span data-stu-id="93593-110">A requester typically needs to run under a user that is a member of either the Administrators group or the Backup Operators group, or run as the Local System account.</span></span>

<span data-ttu-id="93593-111">По умолчанию, когда инициатор запроса выступает в роли клиента COM, если он не выполняется под этими учетными записями, любой вызов COM автоматически отклоняется с помощью **E \_ ACCESSDENIED**, даже не ПОЛУЧАЯ реализацию COM-метода.</span><span class="sxs-lookup"><span data-stu-id="93593-111">By default, when a requester is acting as a COM client, if it does not run under these accounts, any COM call is automatically rejected with **E\_ACCESSDENIED**, without even getting to the COM method implementation.</span></span>

## <a name="disabling-com-exception-handling"></a><span data-ttu-id="93593-112">Отключение обработки исключений COM</span><span class="sxs-lookup"><span data-stu-id="93593-112">Disabling COM Exception Handling</span></span>

<span data-ttu-id="93593-113">При разработке инициатора запроса установите \_ флаг комглб исключения \_ не разграничения \_ обработки глобальных параметров, чтобы отключить обработку исключений COM.</span><span class="sxs-lookup"><span data-stu-id="93593-113">When developing a requester, set the COM COMGLB\_EXCEPTION\_DONOT\_HANDLE global options flag to disable COM exception handling.</span></span> <span data-ttu-id="93593-114">Это важно, поскольку обработка исключений COM может маскировать неустранимые ошибки в приложении VSS.</span><span class="sxs-lookup"><span data-stu-id="93593-114">It is important to do this because COM exception handling can mask fatal errors in a VSS application.</span></span> <span data-ttu-id="93593-115">Ошибка, которая замаскирована, может привести к нестабильной работе и непредсказуемому состоянию, что может приводить к повреждению и зависаниям.</span><span class="sxs-lookup"><span data-stu-id="93593-115">The error that is masked can leave the process in an unstable and unpredictable state, which can lead to corruptions and hangs.</span></span> <span data-ttu-id="93593-116">Дополнительные сведения об этом флаге см. в разделе [иглобалоптионс](/windows/win32/api/objidlbase/nn-objidlbase-iglobaloptions).</span><span class="sxs-lookup"><span data-stu-id="93593-116">For more information about this flag, see [IGlobalOptions](/windows/win32/api/objidlbase/nn-objidlbase-iglobaloptions).</span></span>

## <a name="setting-requester-default-com-access-check-permission"></a><span data-ttu-id="93593-117">Задание разрешения на проверку доступа COM по умолчанию для инициатора запроса</span><span class="sxs-lookup"><span data-stu-id="93593-117">Setting Requester Default COM Access Check Permission</span></span>

<span data-ttu-id="93593-118">Запрашивающие стороны должны иметь в виду, что когда процесс выступает в качестве сервера (например, позволяет авторам изменений изменять документ компонентов резервного копирования), они должны разрешать входящие вызовы от других участников VSS, таких как модули записи или служба VSS.</span><span class="sxs-lookup"><span data-stu-id="93593-118">Requesters need to be aware that when their process acts as a server (for example, allowing writers to modify the Backup Components Document), they must allow incoming calls from other VSS participants, such as writers or the VSS service.</span></span>

<span data-ttu-id="93593-119">Однако по умолчанию процесс Windows разрешает только клиенты COM, которые выполняются в рамках одного сеанса входа в систему (идентификатор безопасности SELF) или выполняются под локальной системной учетной записью.</span><span class="sxs-lookup"><span data-stu-id="93593-119">However, by default, a Windows process will allow only COM clients that are running under the same logon session (the SELF SID) or running under the Local System account.</span></span> <span data-ttu-id="93593-120">Это потенциальная проблема, так как эти значения по умолчанию не подходят для инфраструктуры VSS.</span><span class="sxs-lookup"><span data-stu-id="93593-120">This is a potential problem because these defaults are not adequate for the VSS infrastructure.</span></span> <span data-ttu-id="93593-121">Например, модули записи могут работать как учетная запись пользователя "оператор резервного копирования", которая не находится в том же сеансе входа, что и запрашивающий процесс, или локальная системная учетная запись.</span><span class="sxs-lookup"><span data-stu-id="93593-121">For example, writers might run as a "Backup Operator" user account that is neither in the same logon session as the requester process nor a Local System account.</span></span>

<span data-ttu-id="93593-122">Для решения такого типа проблемы каждый серверный процесс COM может дополнительно контролировать, разрешено ли клиенту RPC или COM выполнять метод COM, реализуемый сервером (в данном случае в данном случае это инициатор запроса), с помощью [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) установить разрешение доступа COM по умолчанию для всего процесса.</span><span class="sxs-lookup"><span data-stu-id="93593-122">To handle this type of problem, every COM server process can exercise further control over whether an RPC or COM client is allowed to perform a COM method implemented by the server (a requester in this case) by using [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) to set a process-wide "Default COM Access Check Permission".</span></span>

<span data-ttu-id="93593-123">Инициаторы запроса могут явным образом выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="93593-123">Requesters can explicitly do the following:</span></span>

-   <span data-ttu-id="93593-124">Разрешение всем процессам доступ для вызова процесса инициатора запроса.</span><span class="sxs-lookup"><span data-stu-id="93593-124">Allow all processes access to call into the requester process.</span></span>

    <span data-ttu-id="93593-125">Этот параметр может быть достаточно для большинства вызывающих запросов и используется другими серверами COM. Например, все службы Windows на основе SVCHOST уже используют этот вариант, как и все службы COM+ по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="93593-125">This option may be adequate for the vast majority of requesters, and is used by other COM servers—for example, all SVCHOST-based Windows services are already using this option, as are all COM+ Services by default.</span></span>

    <span data-ttu-id="93593-126">Разрешение всем процессам выполнять входящие вызовы COM не обязательно является слабостью безопасности.</span><span class="sxs-lookup"><span data-stu-id="93593-126">Allowing all processes to perform incoming COM calls is not necessarily a security weakness.</span></span> <span data-ttu-id="93593-127">Инициатор запроса, действующий как сервер COM, как и все остальные серверы COM, всегда поддерживает возможность авторизации своих клиентов на каждом методе COM, реализованном в его процессе.</span><span class="sxs-lookup"><span data-stu-id="93593-127">A requester acting as a COM server, like all other COM servers, always retains the option to authorize its clients on every COM method implemented in its process.</span></span>

    <span data-ttu-id="93593-128">Обратите внимание, что внутренние обратные вызовы COM, реализованные службой VSS, защищены по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="93593-128">Note that internal COM callbacks implemented by VSS are secured by default.</span></span>

    <span data-ttu-id="93593-129">Чтобы разрешить всем процессам доступ к инициатору запроса через COM, можно передать **нулевой** дескриптор безопасности в качестве первого параметра [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="93593-129">To allow all processes COM access to a requester, you can pass a **NULL** security descriptor as the first parameter of [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="93593-130">(Обратите внимание, что **CoInitializeSecurity** должен вызываться не более одного раза для всего процесса.</span><span class="sxs-lookup"><span data-stu-id="93593-130">(Note that **CoInitializeSecurity** must be called at most once for the entire process.</span></span> <span data-ttu-id="93593-131">Дополнительные сведения о вызовах **CoInitializeSecurity** см. в документации по com или MSDN.)</span><span class="sxs-lookup"><span data-stu-id="93593-131">Please see the COM documentation or MSDN for more information on **CoInitializeSecurity** calls.)</span></span>

    <span data-ttu-id="93593-132">В следующем примере кода показано, как инициатор запроса должен вызвать [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) в Windows 8 и windows Server 2012 и более поздних версий для обеспечения СОВМЕСТИМОСТИ с VSS для удаленных файловых ресурсов (рвсс):</span><span class="sxs-lookup"><span data-stu-id="93593-132">The following code example shows how a requester should call [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) in Windows 8 and Windows Server 2012 and later, in order to be compatible with VSS for remote file shares (RVSS):</span></span>

    ``` syntax
    // Initialize COM security.
       hr = CoInitializeSecurity(
            NULL,                          //  PSECURITY_DESCRIPTOR         pSecDesc,
            -1,                            //  LONG                         cAuthSvc,
            NULL,                          //  SOLE_AUTHENTICATION_SERVICE *asAuthSvc,
            NULL,                          //  void                        *pReserved1,
            RPC_C_AUTHN_LEVEL_PKT_PRIVACY, //  DWORD                        dwAuthnLevel,
            RPC_C_IMP_LEVEL_IMPERSONATE,   //  DWORD                        dwImpLevel,
            NULL,                          //  void                        *pAuthList,
            EOAC_STATIC,                   //  DWORD                        dwCapabilities,
            NULL                           //  void                        *pReserved3
            );
    ```

    <span data-ttu-id="93593-133">При явном задании безопасности на уровне COM инициатора запроса с помощью [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="93593-133">When explicitly setting a requester's COM level security with [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), you should do the following:</span></span>

    -   <span data-ttu-id="93593-134">Установите уровень проверки подлинности по крайней мере на **\_ уровне RPC C \_ AUTHN, \_ \_ \_ целостность PKT**.</span><span class="sxs-lookup"><span data-stu-id="93593-134">Set the authentication level to at least **RPC\_C\_AUTHN\_LEVEL\_PKT\_INTEGRITY**.</span></span> <span data-ttu-id="93593-135">Для повышения безопасности рассмотрите возможность использования **RPC \_ C \_ AUTHN \_ Level \_ PKT \_**.</span><span class="sxs-lookup"><span data-stu-id="93593-135">For better security, consider using **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span>
    -   <span data-ttu-id="93593-136">Задайте уровень олицетворения на **\_ уровне RPC C " \_ \_ \_ impersonate**".</span><span class="sxs-lookup"><span data-stu-id="93593-136">Set the impersonation level to **RPC\_C\_IMP\_LEVEL\_IMPERSONATE**.</span></span>
    -   <span data-ttu-id="93593-137">Установите для функций безопасности маскировку значение **еоак \_ static**.</span><span class="sxs-lookup"><span data-stu-id="93593-137">Set the cloaking security capabilities to **EOAC\_STATIC**.</span></span> <span data-ttu-id="93593-138">Дополнительные сведения о маскировке безопасности см. в разделе [маскировка](../com/cloaking.md).</span><span class="sxs-lookup"><span data-stu-id="93593-138">For more information about cloaking security, see [Cloaking](../com/cloaking.md).</span></span>

    <span data-ttu-id="93593-139">В следующем примере кода показано, как инициатор запроса должен вызвать [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) в Windows 7 и windows Server 2008 R2 и более ранних версиях (или в Windows 8 и windows Server 2012 и более поздних версий, если не требуется совместимость с рвсс):</span><span class="sxs-lookup"><span data-stu-id="93593-139">The following code example shows how a requester should call [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) in Windows 7 and Windows Server 2008 R2 and earlier (or in Windows 8 and Windows Server 2012 and later, if RVSS compatibility is not needed):</span></span>

    ``` syntax
    // Initialize COM security.
       hr = CoInitializeSecurity(
            NULL,                          //  PSECURITY_DESCRIPTOR         pSecDesc,
            -1,                            //  LONG                         cAuthSvc,
            NULL,                          //  SOLE_AUTHENTICATION_SERVICE *asAuthSvc,
            NULL,                          //  void                        *pReserved1,
            RPC_C_AUTHN_LEVEL_PKT_PRIVACY, //  DWORD                        dwAuthnLevel,
            RPC_C_IMP_LEVEL_IDENTIFY,      //  DWORD                        dwImpLevel,
            NULL,                          //  void                        *pAuthList,
            EOAC_NONE,                     //  DWORD                        dwCapabilities,
            NULL                           //  void                        *pReserved3
            );
    ```

    <span data-ttu-id="93593-140">При явном задании безопасности на уровне COM инициатора запроса с помощью [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="93593-140">When explicitly setting a requester's COM level security with [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), you should do the following:</span></span>

    -   <span data-ttu-id="93593-141">Задайте уровень проверки подлинности как минимум **RPC \_ C \_ AUTHN \_ Level \_ Connect**.</span><span class="sxs-lookup"><span data-stu-id="93593-141">Set the authentication level to at least **RPC\_C\_AUTHN\_LEVEL\_CONNECT**.</span></span> <span data-ttu-id="93593-142">Для повышения безопасности рассмотрите возможность использования **RPC \_ C \_ AUTHN \_ Level \_ PKT \_**.</span><span class="sxs-lookup"><span data-stu-id="93593-142">For better security, consider using **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span>
    -   <span data-ttu-id="93593-143">Задайте уровень олицетворения на уровне " **назначение \_ RPC \_ C \_ \_** ", если только процессу инициатора запроса не нужно разрешать олицетворение для конкретных вызовов RPC или COM, которые не связаны с VSS.</span><span class="sxs-lookup"><span data-stu-id="93593-143">Set the impersonation level to **RPC\_C\_IMP\_LEVEL\_IDENTIFY** unless the requester process needs to allow impersonation for specific RPC or COM calls that are unrelated to VSS.</span></span>

-   <span data-ttu-id="93593-144">Разрешить доступ только определенным процессам для вызова процесса инициатора запроса.</span><span class="sxs-lookup"><span data-stu-id="93593-144">Allow only specified processes access to call into the requester process.</span></span>

    <span data-ttu-id="93593-145">COM-сервер (например, инициатор запроса), вызывающий [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) с дескриптором безопасности, отличным от **null** , в качестве первого параметра может использовать дескриптор для настройки, чтобы принимать входящие вызовы только от пользователей, принадлежащих определенному набору учетных записей.</span><span class="sxs-lookup"><span data-stu-id="93593-145">A COM server (such as a requester) that is calling [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) with a non-**NULL** security descriptor as the first parameter can use the descriptor to configure itself to accept incoming calls only from users that belong to a specific set of accounts.</span></span>

    <span data-ttu-id="93593-146">Инициатор запроса должен убедиться, что клиенты COM, работающие с действительными пользователями, имеют право на вызов своего процесса.</span><span class="sxs-lookup"><span data-stu-id="93593-146">A requester must ensure that COM clients running under valid users are authorized to call into its process.</span></span> <span data-ttu-id="93593-147">Инициатор запроса, указывающий дескриптор безопасности в первом параметре, должен предоставить следующим пользователям возможность выполнять входящие вызовы в процессе запроса:</span><span class="sxs-lookup"><span data-stu-id="93593-147">A requester that specifies a Security Descriptor in the first parameter must allow the following users to perform incoming calls into the requester process:</span></span>

    -   <span data-ttu-id="93593-148">Локальная система</span><span class="sxs-lookup"><span data-stu-id="93593-148">Local System</span></span>
    -   <span data-ttu-id="93593-149">Локальная служба.</span><span class="sxs-lookup"><span data-stu-id="93593-149">Local Service</span></span>

        <span data-ttu-id="93593-150">**Windows XP:** Это значение не поддерживается до Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="93593-150">**Windows XP:** This value is not supported until Windows Server 2003.</span></span>

    -   <span data-ttu-id="93593-151">Сетевая служба.</span><span class="sxs-lookup"><span data-stu-id="93593-151">Network Service</span></span>

        <span data-ttu-id="93593-152">**Windows XP:** Это значение не поддерживается до Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="93593-152">**Windows XP:** This value is not supported until Windows Server 2003.</span></span>

    -   <span data-ttu-id="93593-153">Члены локальной группы администраторов</span><span class="sxs-lookup"><span data-stu-id="93593-153">Members of the local Administrators group</span></span>
    -   <span data-ttu-id="93593-154">Члены группы локальных операторов резервного копирования</span><span class="sxs-lookup"><span data-stu-id="93593-154">Members of the local Backup Operators group</span></span>
    -   <span data-ttu-id="93593-155">Специальные пользователи, указанные в расположении реестра ниже, "1" в качестве \_ значения reg DWORD</span><span class="sxs-lookup"><span data-stu-id="93593-155">Special users that are specified in the registry location below, with "1" as their REG\_DWORD value</span></span>

## <a name="explicitly-controlling-user-account-access-to-a-requester"></a><span data-ttu-id="93593-156">Явное управление доступом учетной записи пользователя к инициатору запроса</span><span class="sxs-lookup"><span data-stu-id="93593-156">Explicitly Controlling User Account Access to a Requester</span></span>

<span data-ttu-id="93593-157">Бывают случаи, когда запрещен доступ к инициатору запроса для процессов, работающих в качестве локальной системы, или группы локальных администраторов или локальных операторов резервного копирования, которые могут быть слишком ограниченными.</span><span class="sxs-lookup"><span data-stu-id="93593-157">There are cases where restricting access to a requester to processes running as Local System, or under the local Administrators or local Backup Operators groups, may be too restrictive.</span></span>

<span data-ttu-id="93593-158">Например, указанный процесс инициатора запроса может не требоваться для запуска с учетной записью администратора или оператора резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="93593-158">For example, a specified requester process might not ordinarily need to be run under an Administrator or Backup Operator account.</span></span> <span data-ttu-id="93593-159">По соображениям безопасности лучше не искусственно повышать привилегии процессов для поддержки VSS.</span><span class="sxs-lookup"><span data-stu-id="93593-159">For security reasons, it would be best not to artificially promote the processes privileges to support VSS.</span></span>

<span data-ttu-id="93593-160">В таких случаях **\_ \_** \\  \\  \\ необходимо изменить раздел реестра CurrentControlSet **Services** \\ **VSS** \\ для **вссакцессконтрол** служб, чтобы указать службе VSS, что указанный пользователь может быть защищен для выполнения запрашивающей стороны VSS.</span><span class="sxs-lookup"><span data-stu-id="93593-160">In these cases, the **HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Services**\\**VSS**\\**VssAccessControl** registry key must be modified to instruct VSS that a specified user is safe to run a VSS requester.</span></span>

<span data-ttu-id="93593-161">В этом разделе необходимо создать подраздел с тем же именем, что и у учетной записи, которой должен быть предоставлен или запрещен доступ.</span><span class="sxs-lookup"><span data-stu-id="93593-161">Under this key, you must create a subkey that has the same name as the account that is to be granted or denied access.</span></span> <span data-ttu-id="93593-162">Для этого подраздела необходимо задать одно из значений, приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="93593-162">This subkey must be set to one of the values in the following table.</span></span>

| <span data-ttu-id="93593-163">Значение</span><span class="sxs-lookup"><span data-stu-id="93593-163">Value</span></span> | <span data-ttu-id="93593-164">Значение</span><span class="sxs-lookup"><span data-stu-id="93593-164">Meaning</span></span>                                             |
|-------|-----------------------------------------------------|
| <span data-ttu-id="93593-165">0</span><span class="sxs-lookup"><span data-stu-id="93593-165">0</span></span>     | <span data-ttu-id="93593-166">Запрещает пользователю доступ к модулю записи и инициатору запроса.</span><span class="sxs-lookup"><span data-stu-id="93593-166">Deny the user access to your writer and requester.</span></span>  |
| <span data-ttu-id="93593-167">1</span><span class="sxs-lookup"><span data-stu-id="93593-167">1</span></span>     | <span data-ttu-id="93593-168">Предоставьте пользователю доступ к своему модулю записи.</span><span class="sxs-lookup"><span data-stu-id="93593-168">Grant the user access to your writer.</span></span>               |
| <span data-ttu-id="93593-169">2</span><span class="sxs-lookup"><span data-stu-id="93593-169">2</span></span>     | <span data-ttu-id="93593-170">Предоставьте пользователю доступ к инициатору запроса.</span><span class="sxs-lookup"><span data-stu-id="93593-170">Grant the user access to your requester.</span></span>            |
| <span data-ttu-id="93593-171">3</span><span class="sxs-lookup"><span data-stu-id="93593-171">3</span></span>     | <span data-ttu-id="93593-172">Предоставьте пользователю доступ к своему модулю записи и инициатору запроса.</span><span class="sxs-lookup"><span data-stu-id="93593-172">Grant the user access to your writer and requester.</span></span> |



 

<span data-ttu-id="93593-173">В следующем примере предоставляется доступ к \\ учетной записи "mydomain myuser":</span><span class="sxs-lookup"><span data-stu-id="93593-173">The following example grants access to the "MyDomain\\MyUser" account:</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
            VSS
               VssAccessControl
                  MyDomain\MyUser = 2<dl>
<dt>

                  Data type
</dt>
<dd>                  REG_DWORD</dd>
</dl>
```

<span data-ttu-id="93593-174">Этот механизм также можно использовать, чтобы явно ограничить выполнение инициатора запроса VSS другим разрешенным пользователем.</span><span class="sxs-lookup"><span data-stu-id="93593-174">This mechanism can also be used to explicitly restrict an otherwise permitted user from running a VSS requester.</span></span> <span data-ttu-id="93593-175">В следующем примере ограничение доступа будет ограничено \\ учетной записью администратора сатдомаин:</span><span class="sxs-lookup"><span data-stu-id="93593-175">The following example will restrict access from the "ThatDomain\\Administrator" account:</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
            VSS
               VssAccessControl
                  ThatDomain\Administrator = 0<dl>
<dt>

                  Data type
</dt>
<dd>                  REG_DWORD</dd>
</dl>
```

<span data-ttu-id="93593-176">Администратор Сатдомаин пользователя \\ не сможет запустить инициатор запроса VSS.</span><span class="sxs-lookup"><span data-stu-id="93593-176">The user ThatDomain\\Administrator would not be able to run a VSS requester.</span></span>

## <a name="performing-a-file-backup-of-the-system-state"></a><span data-ttu-id="93593-177">Выполнение резервного копирования файлов состояния системы</span><span class="sxs-lookup"><span data-stu-id="93593-177">Performing a File Backup of the System State</span></span>

<span data-ttu-id="93593-178">Если инициатор запроса выполняет резервное копирование отдельных файлов, а не использует образ тома для резервного копирования, он должен вызвать функции [**финдфирстфиленамев**](/windows/win32/api/fileapi/nf-fileapi-findfirstfilenamew) и [**финднекстфиленамев**](/windows/win32/api/fileapi/nf-fileapi-findnextfilenamew) для перечисления жестких ссылок на файлы, расположенные в следующих каталогах:</span><span class="sxs-lookup"><span data-stu-id="93593-178">If a requester performs system-state backup by backing up individual files instead of using a volume image for the backup, it must call the [**FindFirstFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findfirstfilenamew) and [**FindNextFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findnextfilenamew) functions to enumerate hard links on files that are located in the following directories:</span></span>

-   <span data-ttu-id="93593-179">Windows \\ system32 \\ WDI \\ perftrack</span><span class="sxs-lookup"><span data-stu-id="93593-179">Windows\\system32\\WDI\\perftrack</span></span>\\
-   <span data-ttu-id="93593-180">WINSXS для Windows </span><span class="sxs-lookup"><span data-stu-id="93593-180">Windows\\WINSXS</span></span>\\\\

<span data-ttu-id="93593-181">Доступ к этим каталогам могут получить только члены группы «Администраторы».</span><span class="sxs-lookup"><span data-stu-id="93593-181">These directories can only be accessed by members of the Administrators group.</span></span> <span data-ttu-id="93593-182">По этой причине такой инициатор должен работать под системной учетной записью или с учетной записью пользователя, которая является членом группы "Администраторы".</span><span class="sxs-lookup"><span data-stu-id="93593-182">For this reason, such a requester must run under the system account or a user account that is a member of the Administrators group.</span></span>

<span data-ttu-id="93593-183">**Windows XP и Windows Server 2003:** Функции [**финдфирстфиленамев**](/windows/win32/api/fileapi/nf-fileapi-findfirstfilenamew) и [**финднекстфиленамев**](/windows/win32/api/fileapi/nf-fileapi-findnextfilenamew) не поддерживаются до Windows Vista и Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="93593-183">**Windows XP and Windows Server 2003:** The [**FindFirstFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findfirstfilenamew) and [**FindNextFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findnextfilenamew) functions are not supported until Windows Vista and Windows Server 2008.</span></span>

 

 
