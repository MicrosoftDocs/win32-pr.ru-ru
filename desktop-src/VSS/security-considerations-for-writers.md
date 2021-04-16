---
description: Инфраструктура VSS требует, чтобы процессы модуля записи могли функционировать как клиенты COM и как серверы.
ms.assetid: 59bb7a86-e874-45ce-abd6-cafd18802c4d
title: Вопросы безопасности для модулей записи
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea6f88243adbd62d928170a86ed57b91cbebe134
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692878"
---
# <a name="security-considerations-for-writers"></a><span data-ttu-id="daed0-103">Вопросы безопасности для модулей записи</span><span class="sxs-lookup"><span data-stu-id="daed0-103">Security Considerations for Writers</span></span>

<span data-ttu-id="daed0-104">Инфраструктура VSS требует, чтобы процессы модуля записи могли функционировать как клиенты COM и как серверы.</span><span class="sxs-lookup"><span data-stu-id="daed0-104">The VSS infrastructure requires writer processes to be able to function both as COM clients and as servers.</span></span>

<span data-ttu-id="daed0-105">При работе в качестве серверов модули записи VSS предоставляют интерфейсы COM (например, обработчики событий VSS, такие как [**квссвритер:: onidentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify)) и получают входящие вызовы COM из процессов VSS (например, запрашивающих и службы VSS) или вызовы RPC из процессов, которые являются внешними по отношению к VSS, обычно когда эти процессы создают события VSS (например, когда инициатор запроса вызывает [**Ивссбаккупкомпонентс:: гасервритерметадата**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)).</span><span class="sxs-lookup"><span data-stu-id="daed0-105">When acting as servers, VSS writers expose COM interfaces (for example, the VSS event handlers such as [**CVssWriter::OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify)) and receive incoming COM calls from VSS processes (such as requesters and the VSS service) or RPC calls from processes that are external to VSS, typically when these processes generate VSS events (for example, when a requester calls [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)).</span></span> <span data-ttu-id="daed0-106">Таким образом, модуль записи VSS должен безопасно управлять тем, какие клиенты COM могут выполнять входящие вызовы COM в процесс.</span><span class="sxs-lookup"><span data-stu-id="daed0-106">Therefore, a VSS writer needs to securely manage which COM clients are able to make incoming COM calls into its process.</span></span>

<span data-ttu-id="daed0-107">Аналогично, модули записи VSS также могут действовать как клиенты COM, делая исходящие вызовы COM обратными вызовами, предоставляемыми инфраструктурой VSS, или вызовы RPC к процессам, которые являются внешними по отношению к VSS.</span><span class="sxs-lookup"><span data-stu-id="daed0-107">Similarly, VSS writers may also act as COM clients, making outgoing COM calls to callbacks supplied by the VSS infrastructure or RPC calls to processes that are external to VSS.</span></span> <span data-ttu-id="daed0-108">Эти обратные вызовы, предоставляемые приложением резервного копирования или службой VSS, позволяют модулю записи выполнять такие задачи, как обновление документа компонента резервного копирования через интерфейс [**ивсскомпонент**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) .</span><span class="sxs-lookup"><span data-stu-id="daed0-108">These callbacks that are provided either by a backup application or by the VSS service allow the writer to perform tasks such as updating the Backup Components Document through the [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) interface.</span></span> <span data-ttu-id="daed0-109">Поэтому параметры безопасности VSS должны разрешать потокам записи исключать исходящие вызовы COM в другие процессы VSS.</span><span class="sxs-lookup"><span data-stu-id="daed0-109">Therefore, VSS security settings must allow writers to make outgoing COM calls into other VSS processes.</span></span>

<span data-ttu-id="daed0-110">Самым простым механизмом управления проблемами безопасности модуля записи является правильная выбор учетной записи пользователя, от имени которой она выполняется.</span><span class="sxs-lookup"><span data-stu-id="daed0-110">The simplest mechanism for managing writer security issues involves the proper selection of the user account under which it runs.</span></span> <span data-ttu-id="daed0-111">Модуль записи обычно должен выполняться от имени пользователя, который является членом группы "Администраторы" или "операторы резервного копирования", либо должен запускаться как локальная системная учетная запись.</span><span class="sxs-lookup"><span data-stu-id="daed0-111">A writer typically needs to run under a user who is a member of either the Administrators group or the Backup Operators group, or it needs to run as the Local System account.</span></span>

<span data-ttu-id="daed0-112">По умолчанию, когда модуль записи выступает в качестве клиента COM, если он не выполняется под этими учетными записями, любой вызов COM, который он делает, автоматически отклоняется с помощью **E \_ ACCESSDENIED** , не ПОЛУЧАЯ реализацию COM-метода.</span><span class="sxs-lookup"><span data-stu-id="daed0-112">By default, when a writer is acting as a COM client, if it does not run under these accounts, any COM call it makes is automatically rejected with **E\_ACCESSDENIED** without even getting to the COM method implementation.</span></span>

## <a name="disabling-com-exception-handling"></a><span data-ttu-id="daed0-113">Отключение обработки исключений COM</span><span class="sxs-lookup"><span data-stu-id="daed0-113">Disabling COM Exception Handling</span></span>

<span data-ttu-id="daed0-114">При разработке модуля записи установите \_ \_ флаг глобального параметра com комглб Exception не разграничения \_ Handle, чтобы отключить обработку исключений COM.</span><span class="sxs-lookup"><span data-stu-id="daed0-114">When developing a writer, set the COM COMGLB\_EXCEPTION\_DONOT\_HANDLE global options flag to disable COM exception handling.</span></span> <span data-ttu-id="daed0-115">Это важно, поскольку обработка исключений COM может маскировать неустранимые ошибки в приложении VSS.</span><span class="sxs-lookup"><span data-stu-id="daed0-115">It is important to do this because COM exception handling can mask fatal errors in a VSS application.</span></span> <span data-ttu-id="daed0-116">Ошибка, которая замаскирована, может привести к нестабильной работе и непредсказуемому состоянию, что может приводить к повреждению и зависаниям.</span><span class="sxs-lookup"><span data-stu-id="daed0-116">The error that is masked can leave the process in an unstable and unpredictable state, which can lead to corruptions and hangs.</span></span> <span data-ttu-id="daed0-117">Дополнительные сведения об этом флаге см. в разделе [иглобалоптионс](/windows/win32/api/objidlbase/nn-objidlbase-iglobaloptions).</span><span class="sxs-lookup"><span data-stu-id="daed0-117">For more information about this flag, see [IGlobalOptions](/windows/win32/api/objidlbase/nn-objidlbase-iglobaloptions).</span></span>

## <a name="setting-writer-default-com-access-check-permission"></a><span data-ttu-id="daed0-118">Задание разрешения на проверку доступа COM по умолчанию для модуля записи</span><span class="sxs-lookup"><span data-stu-id="daed0-118">Setting Writer Default COM Access Check Permission</span></span>

<span data-ttu-id="daed0-119">Модули записи должны знать, что, когда их процессы работают в качестве сервера (например, для обработки событий VSS), они должны разрешать входящие вызовы от других участников VSS, таких как инициаторы запроса или служба VSS.</span><span class="sxs-lookup"><span data-stu-id="daed0-119">Writers need to be aware that when their processes act as a server (for example, to handle VSS events), they must allow incoming calls from other VSS participants, such as requesters or the VSS service.</span></span>

<span data-ttu-id="daed0-120">Однако по умолчанию процесс разрешается только клиентам COM, которые выполняются в одном сеансе входа в систему, идентификатором безопасности SELF) или выполняются под локальной системной учетной записью.</span><span class="sxs-lookup"><span data-stu-id="daed0-120">However, by default, a process will allow only COM clients that are running under the same logon session the SELF SID) or running under the Local System account.</span></span> <span data-ttu-id="daed0-121">Это потенциальная проблема, так как эти значения по умолчанию недостаточно для поддержки инфраструктуры VSS.</span><span class="sxs-lookup"><span data-stu-id="daed0-121">This is a potential problem because these defaults are not sufficient to support the VSS infrastructure.</span></span> <span data-ttu-id="daed0-122">Например, инициаторы запроса могут работать как учетная запись пользователя "оператор резервного копирования", которая не находится в том же сеансе входа, что и процесс записи или локальная системная учетная запись.</span><span class="sxs-lookup"><span data-stu-id="daed0-122">For example, requesters may run as a "Backup Operator" user account that is neither in the same logon session as the writer process nor a Local System account.</span></span>

<span data-ttu-id="daed0-123">Для решения такого типа проблемы каждый серверный процесс COM может дополнительно контролировать, разрешено ли клиенту RPC или COM выполнять COM-метод, используемый сервером (в данном случае это средство записи), с помощью [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) , чтобы установить разрешение на доступ по умолчанию для проверки доступа COM на уровне процесса.</span><span class="sxs-lookup"><span data-stu-id="daed0-123">To handle this type of problem, every COM server process can exercise further control over whether an RPC or COM client is allowed to perform a COM method the server (a writer in this case) implements by using [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) to set a process-wide default COM access check permission.</span></span>

<span data-ttu-id="daed0-124">Модули записи могут явно выполнять следующие действия:</span><span class="sxs-lookup"><span data-stu-id="daed0-124">Writers can explicitly do the following:</span></span>

-   <span data-ttu-id="daed0-125">Разрешить всем процессам доступ для вызова процесса записи.</span><span class="sxs-lookup"><span data-stu-id="daed0-125">Allow all processes access to call into the writer process.</span></span>

    <span data-ttu-id="daed0-126">Этот параметр может быть достаточно для многих модулей записи и используется другими серверами COM — например, все службы Windows на основе SVCHOST уже используют этот вариант, как и все службы COM+ по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="daed0-126">This option may be adequate for many writers, and is used by other COM servers—for example, all SVCHOST-based Windows services are already using this option, as are all COM+ Services by default.</span></span>

    <span data-ttu-id="daed0-127">Разрешение всем процессам выполнять входящие вызовы COM не обязательно является слабостью безопасности.</span><span class="sxs-lookup"><span data-stu-id="daed0-127">Allowing all processes to perform incoming COM calls is not necessarily a security weakness.</span></span> <span data-ttu-id="daed0-128">Модуль записи, действующий как сервер COM, как и все остальные серверы COM, всегда поддерживает возможность авторизации своих клиентов на каждом методе COM, реализованном в его процессе.</span><span class="sxs-lookup"><span data-stu-id="daed0-128">A writer acting as a COM server, like all other COM servers, always retains the option of authorizing its clients on every COM method implemented in its process.</span></span>

    <span data-ttu-id="daed0-129">Чтобы разрешить всем процессам доступ к модулю записи через COM, можно передать **нулевой** дескриптор безопасности в качестве первого параметра [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="daed0-129">To allow all processes COM access to a writer, you can pass a **NULL** security descriptor as the first parameter of [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="daed0-130">(Обратите внимание, что **CoInitializeSecurity** должен вызываться не более одного раза для всего процесса.</span><span class="sxs-lookup"><span data-stu-id="daed0-130">(Note that **CoInitializeSecurity** must be called at most once for the entire process.</span></span> <span data-ttu-id="daed0-131">Дополнительные сведения о **CoInitializeSecurity** см. в документации по com.)</span><span class="sxs-lookup"><span data-stu-id="daed0-131">Please see the COM documentation for more details on **CoInitializeSecurity**.)</span></span>

    <span data-ttu-id="daed0-132">Ниже приведен пример кода, который включает вызов [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity):</span><span class="sxs-lookup"><span data-stu-id="daed0-132">The following is a code example that includes a call to [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity):</span></span>

    ``` syntax
    // Initialize COM security.
    hr = CoInitializeSecurity(
           NULL,                          // PSECURITY_DESCRIPTOR          pSecDesc,
           -1,                            // LONG                          cAuthSvc,
           NULL,                          // SOLE_AUTHENTICATION_SERVICE  *asAuthSvc,
           NULL,                          // void                         *pReserved1,
           RPC_C_AUTHN_LEVEL_PKT_PRIVACY, // DWORD                         dwAuthnLevel,
           RPC_C_IMP_LEVEL_IDENTIFY,      // DWORD                         dwImpLevel,
           NULL,                          // void                         *pAuthList,
           EOAC_NONE,                     // DWORD                         dwCapabilities,
           NULL                           // void                         *pReserved3
        );
    ```

    <span data-ttu-id="daed0-133">При явном задании безопасности на уровне COM модуля записи с помощью [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="daed0-133">When explicitly setting a writer's COM-level security with [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), you should do the following:</span></span>

    -   <span data-ttu-id="daed0-134">Задайте уровень проверки подлинности как минимум **RPC \_ C \_ AUTHN \_ Level \_ Connect**.</span><span class="sxs-lookup"><span data-stu-id="daed0-134">Set the authentication level to at least **RPC\_C\_AUTHN\_LEVEL\_CONNECT**.</span></span>

        <span data-ttu-id="daed0-135">Для повышения безопасности рассмотрите возможность использования **RPC \_ C \_ AUTHN \_ Level \_ PKT \_**.</span><span class="sxs-lookup"><span data-stu-id="daed0-135">For better security, consider using **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span>

    -   <span data-ttu-id="daed0-136">Установите уровень олицетворения **RPC \_ C на \_ \_ уровне Imp \_** , если процессу записи не нужно разрешать олицетворение для конкретных вызовов RPC или COM, которые не связаны с VSS.</span><span class="sxs-lookup"><span data-stu-id="daed0-136">Set the impersonation level to **RPC\_C\_IMP\_LEVEL\_IDENTIFY** unless the writer process needs to allow impersonation for specific RPC or COM calls that are unrelated to VSS.</span></span>

-   <span data-ttu-id="daed0-137">Разрешить доступ только указанным процессам для вызова процесса записи.</span><span class="sxs-lookup"><span data-stu-id="daed0-137">Allow only specified processes access to call into the writer process.</span></span>

    <span data-ttu-id="daed0-138">COM-сервер (например, модуль записи), вызывающий [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) с дескриптором безопасности, не **равным NULL** , может использовать дескриптор для собственной настройки, чтобы принимать входящие вызовы только от пользователей, принадлежащих к определенному набору учетных записей.</span><span class="sxs-lookup"><span data-stu-id="daed0-138">A COM server (such as a writer) that is calling [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) with a non-**NULL** security descriptor can use the descriptor to configure itself to accept incoming calls only from users that belong to a specific set of accounts.</span></span>

    <span data-ttu-id="daed0-139">Модуль записи должен гарантировать, что клиенты COM, работающие с действительными пользователями, смогут обращаться к его процессу.</span><span class="sxs-lookup"><span data-stu-id="daed0-139">A writer must ensure that COM clients running under valid users are authorized to call into its process.</span></span> <span data-ttu-id="daed0-140">Модуль записи, указывающий дескриптор безопасности в первом параметре, должен предоставить следующим пользователям возможность выполнять входящие вызовы в процессе запроса:</span><span class="sxs-lookup"><span data-stu-id="daed0-140">A writer that specifies a Security Descriptor in the first parameter must allow the following users to perform incoming calls into the requester process:</span></span>

    -   <span data-ttu-id="daed0-141">Локальная система</span><span class="sxs-lookup"><span data-stu-id="daed0-141">Local System</span></span>
    -   <span data-ttu-id="daed0-142">Члены локальной группы администраторов</span><span class="sxs-lookup"><span data-stu-id="daed0-142">Members of the local Administrators group</span></span>
    -   <span data-ttu-id="daed0-143">Члены группы локальных операторов резервного копирования</span><span class="sxs-lookup"><span data-stu-id="daed0-143">Members of the local Backup Operators group</span></span>
    -   <span data-ttu-id="daed0-144">Учетная запись, под которой выполняется модуль записи</span><span class="sxs-lookup"><span data-stu-id="daed0-144">The account under which the writer is running</span></span>

## <a name="explicitly-controlling-user-account-access-to-a-writer"></a><span data-ttu-id="daed0-145">Явное управление доступом учетной записи пользователя к модулю записи</span><span class="sxs-lookup"><span data-stu-id="daed0-145">Explicitly Controlling User Account Access to a Writer</span></span>

<span data-ttu-id="daed0-146">Бывают случаи, когда доступ к модулю записи для выполнения процессов от имени локальной системы или локальных администраторов или локальных операторов резервного копирования может быть слишком ограниченным.</span><span class="sxs-lookup"><span data-stu-id="daed0-146">There are cases where restricting access to a writer to processes running as Local System, or under the local Administrators or local Backup Operators local groups, may be too restrictive.</span></span>

<span data-ttu-id="daed0-147">Например, процесс записи (возможно, не являющийся системным модулем записи) обычно не требуется запускать с учетной записью администратора или оператора резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="daed0-147">For example, a writer process (perhaps a third-party non-system writer) might not ordinarily need to be run under an Administrator or Backup Operator account.</span></span> <span data-ttu-id="daed0-148">По соображениям безопасности лучше не искусственно повышать привилегии процесса для поддержки VSS.</span><span class="sxs-lookup"><span data-stu-id="daed0-148">For security reasons, it would be best not to artificially promote the process's privileges to support VSS.</span></span>

<span data-ttu-id="daed0-149">В таких случаях **\_ \_** \\  \\  \\ необходимо изменить раздел реестра CurrentControlSet **Services** \\ **VSS** \\ для **вссакцессконтрол** служб, чтобы указать службе VSS, что указанный пользователь может быть защищен для выполнения модуля записи VSS.</span><span class="sxs-lookup"><span data-stu-id="daed0-149">In these cases, the **HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Services**\\**VSS**\\**VssAccessControl** registry key must be modified to instruct VSS that a specified user is safe to run a VSS writer.</span></span>

<span data-ttu-id="daed0-150">В этом разделе необходимо создать подраздел с тем же именем, что и у учетной записи, которой должен быть предоставлен или запрещен доступ.</span><span class="sxs-lookup"><span data-stu-id="daed0-150">Under this key, you must create a subkey that has the same name as the account that is to be granted or denied access.</span></span> <span data-ttu-id="daed0-151">Для этого подраздела необходимо задать одно из значений, приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="daed0-151">This subkey must be set to one of the values in the following table.</span></span>

| <span data-ttu-id="daed0-152">Значение</span><span class="sxs-lookup"><span data-stu-id="daed0-152">Value</span></span> | <span data-ttu-id="daed0-153">Значение</span><span class="sxs-lookup"><span data-stu-id="daed0-153">Meaning</span></span>                                             |
|-------|-----------------------------------------------------|
| <span data-ttu-id="daed0-154">0</span><span class="sxs-lookup"><span data-stu-id="daed0-154">0</span></span>     | <span data-ttu-id="daed0-155">Запрещает пользователю доступ к модулю записи и инициатору запроса.</span><span class="sxs-lookup"><span data-stu-id="daed0-155">Deny the user access to your writer and requester.</span></span>  |
| <span data-ttu-id="daed0-156">1</span><span class="sxs-lookup"><span data-stu-id="daed0-156">1</span></span>     | <span data-ttu-id="daed0-157">Предоставьте пользователю доступ к своему модулю записи.</span><span class="sxs-lookup"><span data-stu-id="daed0-157">Grant the user access to your writer.</span></span>               |
| <span data-ttu-id="daed0-158">2</span><span class="sxs-lookup"><span data-stu-id="daed0-158">2</span></span>     | <span data-ttu-id="daed0-159">Предоставьте пользователю доступ к инициатору запроса.</span><span class="sxs-lookup"><span data-stu-id="daed0-159">Grant the user access to your requester.</span></span>            |
| <span data-ttu-id="daed0-160">3</span><span class="sxs-lookup"><span data-stu-id="daed0-160">3</span></span>     | <span data-ttu-id="daed0-161">Предоставьте пользователю доступ к своему модулю записи и инициатору запроса.</span><span class="sxs-lookup"><span data-stu-id="daed0-161">Grant the user access to your writer and requester.</span></span> |



 

<span data-ttu-id="daed0-162">В следующем примере предоставляется доступ к \\ учетной записи "mydomain myuser":</span><span class="sxs-lookup"><span data-stu-id="daed0-162">The following example grants access to the "MyDomain\\MyUser" account:</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
            VSS
               VssAccessControl
                  MyDomain\MyUser = 1<dl>
<dt>

                  Data type
</dt>
<dd>                  REG_DWORD</dd>
</dl>
```

<span data-ttu-id="daed0-163">Этот механизм также можно использовать для явного ограничения выполнения модуля записи VSS другим разрешенным пользователем.</span><span class="sxs-lookup"><span data-stu-id="daed0-163">This mechanism can also be used to explicitly restrict an otherwise permitted user from running a VSS writer.</span></span> <span data-ttu-id="daed0-164">В следующем примере ограничение доступа будет ограничено \\ учетной записью администратора сатдомаин:</span><span class="sxs-lookup"><span data-stu-id="daed0-164">The following example will restrict access from the "ThatDomain\\Administrator" account:</span></span>

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

<span data-ttu-id="daed0-165">Администратор Сатдомаин пользователя \\ не сможет запустить модуль записи VSS.</span><span class="sxs-lookup"><span data-stu-id="daed0-165">The user ThatDomain\\Administrator would not be able to run a VSS writer.</span></span>

 

 
