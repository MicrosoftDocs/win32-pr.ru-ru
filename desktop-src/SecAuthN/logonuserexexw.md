---
description: Функция Логонусерексексв пытается зарегистрировать пользователя на локальном компьютере.
ms.assetid: d90db4c6-a711-4519-8b91-5069cee07738
title: Функция Логонусерексексв (Винбасеп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LogonUserExExW
api_type:
- DllExport
api_location:
- Advapi32.dll
ms.openlocfilehash: 35ec65e7899f45a5222ae12b08992e77ea67f306
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081293"
---
# <a name="logonuserexexw-function"></a><span data-ttu-id="78c4d-103">Функция Логонусерексексв</span><span class="sxs-lookup"><span data-stu-id="78c4d-103">LogonUserExExW function</span></span>

<span data-ttu-id="78c4d-104">Функция **логонусерексексв** пытается зарегистрировать пользователя на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="78c4d-104">The **LogonUserExExW** function attempts to log a user on to the local computer.</span></span> <span data-ttu-id="78c4d-105">Локальный компьютер — это компьютер, с которого был вызван **логонусерексексв** .</span><span class="sxs-lookup"><span data-stu-id="78c4d-105">The local computer is the computer from which **LogonUserExExW** was called.</span></span> <span data-ttu-id="78c4d-106">**Логонусерексексв** нельзя использовать для входа на удаленный компьютер.</span><span class="sxs-lookup"><span data-stu-id="78c4d-106">You cannot use **LogonUserExExW** to log on to a remote computer.</span></span> <span data-ttu-id="78c4d-107">Укажите пользователя, используя имя пользователя и домен, и проверяйте [*подлинность*](../secgloss/a-gly.md) пользователя с помощью пароля в виде открытого текста.</span><span class="sxs-lookup"><span data-stu-id="78c4d-107">Specify the user by using a user name and domain and [*authenticate*](../secgloss/a-gly.md) the user by using a plaintext password.</span></span> <span data-ttu-id="78c4d-108">Если функция выполнена, она получает маркер маркера, который представляет пользователя, выполнившего вход в систему.</span><span class="sxs-lookup"><span data-stu-id="78c4d-108">If the function succeeds, it receives a handle to a token that represents the logged-on user.</span></span> <span data-ttu-id="78c4d-109">Затем этот маркер маркера можно использовать для олицетворения указанного пользователя или, в большинстве случаев, для создания [*процесса*](../secgloss/p-gly.md) , который выполняется в контексте указанного пользователя.</span><span class="sxs-lookup"><span data-stu-id="78c4d-109">You can then use this token handle to impersonate the specified user or, in most cases, to create a [*process*](../secgloss/p-gly.md) that runs in the context of the specified user.</span></span>

<span data-ttu-id="78c4d-110">Эта функция аналогична функции [**логонусерекс**](/windows/desktop/api/Winbase/nf-winbase-logonuserexa) , за исключением того, что она принимает дополнительный параметр *птокенграупс*, который представляет собой набор из одного или нескольких [*идентификаторов безопасности*](../secgloss/s-gly.md) (SID), которые добавляются в маркер, возвращаемый вызывающему объекту при успешном входе.</span><span class="sxs-lookup"><span data-stu-id="78c4d-110">This function is similar to the [**LogonUserEx**](/windows/desktop/api/Winbase/nf-winbase-logonuserexa) function, except that it takes the additional parameter, *pTokenGroups*, which is a set of one or more [*security identifiers*](../secgloss/s-gly.md) (SIDs) that are added to the token returned to the caller when the logon is successful.</span></span>

<span data-ttu-id="78c4d-111">Эта функция не объявлена в общедоступном заголовке и не имеет связанной библиотеки импорта.</span><span class="sxs-lookup"><span data-stu-id="78c4d-111">This function is not declared in a public header and has no associated import library.</span></span> <span data-ttu-id="78c4d-112">Для динамической привязки к Advapi32.dll необходимо использовать функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="78c4d-112">You must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Advapi32.dll.</span></span>

## <a name="syntax"></a><span data-ttu-id="78c4d-113">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="78c4d-113">Syntax</span></span>


```C++
BOOL WINAPI LogonUserExExW(
  _In_      LPTSTR        lpszUsername,
  _In_opt_  LPTSTR        lpszDomain,
  _In_opt_  LPTSTR        lpszPassword,
  _In_      DWORD         dwLogonType,
  _In_      DWORD         dwLogonProvider,
  _In_opt_  PTOKEN_GROUPS pTokenGroups,
  _Out_opt_ PHANDLE       phToken,
  _Out_opt_ PSID          *ppLogonSid,
  _Out_opt_ PVOID         *ppProfileBuffer,
  _Out_opt_ LPDWORD       pdwProfileLength,
  _Out_opt_ PQUOTA_LIMITS pQuotaLimits
);
```



## <a name="parameters"></a><span data-ttu-id="78c4d-114">Параметры</span><span class="sxs-lookup"><span data-stu-id="78c4d-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78c4d-115">*лпсзусернаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="78c4d-115">*lpszUsername* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78c4d-116">Указатель на строку, завершающуюся нулем, которая указывает имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="78c4d-116">A pointer to a null-terminated string that specifies the name of the user.</span></span> <span data-ttu-id="78c4d-117">Это имя учетной записи пользователя для входа в систему.</span><span class="sxs-lookup"><span data-stu-id="78c4d-117">This is the name of the user account to log on to.</span></span> <span data-ttu-id="78c4d-118">Если используется формат [*имени участника-пользователя*](../secgloss/u-gly.md) (UPN), параметр *Лпсздомаин* должен иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="78c4d-118">If you use the [*user principal name*](../secgloss/u-gly.md) (UPN) format, the *lpszDomain* parameter must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="78c4d-119">*лпсздомаин* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="78c4d-119">*lpszDomain* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="78c4d-120">Указатель на строку, завершающуюся нулем, которая указывает имя домена или сервера, база данных учетных записей которого содержит учетную запись *лпсзусернаме* .</span><span class="sxs-lookup"><span data-stu-id="78c4d-120">A pointer to a null-terminated string that specifies the name of the domain or server whose account database contains the *lpszUsername* account.</span></span> <span data-ttu-id="78c4d-121">Если этот параметр имеет **значение NULL**, имя пользователя должно быть указано в формате UPN.</span><span class="sxs-lookup"><span data-stu-id="78c4d-121">If this parameter is **NULL**, the user name must be specified in UPN format.</span></span> <span data-ttu-id="78c4d-122">Если этот параметр имеет значение ".", функция проверяет учетную запись, используя только локальную базу данных учетных записей.</span><span class="sxs-lookup"><span data-stu-id="78c4d-122">If this parameter is ".", the function validates the account by using only the local account database.</span></span>

</dd> <dt>

<span data-ttu-id="78c4d-123">*лпсзпассворд* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="78c4d-123">*lpszPassword* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="78c4d-124">Указатель на строку, завершающуюся нулем, которая указывает пароль в виде открытого текста для учетной записи пользователя, указанной параметром *лпсзусернаме*.</span><span class="sxs-lookup"><span data-stu-id="78c4d-124">A pointer to a null-terminated string that specifies the plaintext password for the user account specified by *lpszUsername*.</span></span> <span data-ttu-id="78c4d-125">Завершив использование пароля, очистите его из памяти, вызвав функцию [**секурезеромемори**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="78c4d-125">When you have finished using the password, clear the password from memory by calling the [**SecureZeroMemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) function.</span></span> <span data-ttu-id="78c4d-126">Дополнительные сведения о защите паролей см. в разделе [обработка паролей](../secbp/handling-passwords.md).</span><span class="sxs-lookup"><span data-stu-id="78c4d-126">For more information about protecting passwords, see [Handling Passwords](../secbp/handling-passwords.md).</span></span>

</dd> <dt>

<span data-ttu-id="78c4d-127">*dwLogonType* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="78c4d-127">*dwLogonType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78c4d-128">Тип выполняемой операции входа.</span><span class="sxs-lookup"><span data-stu-id="78c4d-128">The type of logon operation to perform.</span></span> <span data-ttu-id="78c4d-129">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="78c4d-129">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="78c4d-130">Значение</span><span class="sxs-lookup"><span data-stu-id="78c4d-130">Value</span></span>                                                                                                                                                                                                                                                                        | <span data-ttu-id="78c4d-131">Значение</span><span class="sxs-lookup"><span data-stu-id="78c4d-131">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LOGON32_LOGON_INTERACTIVE"></span><span id="logon32_logon_interactive"></span><dl> <span data-ttu-id="78c4d-132"><dt>**LOGON32 \_ \_Интерактивный вход**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="78c4d-132"><dt>**LOGON32\_LOGON\_INTERACTIVE**</dt> <dt>2</dt></span></span> </dl>                    | <span data-ttu-id="78c4d-133">Этот тип входа предназначен для пользователей, которые будут интерактивно работать с компьютером, например пользователь, вошедший в систему с помощью сервера [*терминалов*](../secgloss/t-gly.md) , удаленной оболочки или аналогичного процесса.</span><span class="sxs-lookup"><span data-stu-id="78c4d-133">This logon type is intended for users who will be interactively using the computer, such as a user being logged on by a [*terminal*](../secgloss/t-gly.md) server, remote shell, or similar process.</span></span> <span data-ttu-id="78c4d-134">Этот тип входа имеет дополнительные затраты на кэширование данных для входа в систему для отключенных операций. Поэтому он не подходит для некоторых клиентских и серверных приложений, таких как почтовый сервер.</span><span class="sxs-lookup"><span data-stu-id="78c4d-134">This logon type has the additional expense of caching logon information for disconnected operations; therefore, it is inappropriate for some client/server applications, such as a mail server.</span></span><br/>                                  |
| <span id="LOGON32_LOGON_NETWORK"></span><span id="logon32_logon_network"></span><dl> <span data-ttu-id="78c4d-135"><dt>**LOGON32 \_ Вход в \_ сеть**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="78c4d-135"><dt>**LOGON32\_LOGON\_NETWORK**</dt> <dt>3</dt></span></span> </dl>                                | <span data-ttu-id="78c4d-136">Этот тип входа предназначен для высокопроизводительных серверов для проверки подлинности паролей в формате обычного текста.</span><span class="sxs-lookup"><span data-stu-id="78c4d-136">This logon type is intended for high performance servers to authenticate plaintext passwords.</span></span> <span data-ttu-id="78c4d-137">Функция **логонусерексексв** не кэширует учетные данные для этого типа входа.</span><span class="sxs-lookup"><span data-stu-id="78c4d-137">The **LogonUserExExW** function does not cache credentials for this logon type.</span></span><br/>                                                                                                                                                                                                                                                                                                 |
| <span id="LOGON32_LOGON_BATCH"></span><span id="logon32_logon_batch"></span><dl> <span data-ttu-id="78c4d-138"><dt>**LOGON32 \_ Вход в \_ пакет**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="78c4d-138"><dt>**LOGON32\_LOGON\_BATCH**</dt> <dt>4</dt></span></span> </dl>                                      | <span data-ttu-id="78c4d-139">Этот тип входа предназначен для пакетных серверов, где процессы могут выполняться от имени пользователя без их прямого вмешательства.</span><span class="sxs-lookup"><span data-stu-id="78c4d-139">This logon type is intended for batch servers, where processes may be executing on behalf of a user without their direct intervention.</span></span> <span data-ttu-id="78c4d-140">Этот тип также используется для более высоких серверов производительности, которые обрабатывают несколько попыток проверки подлинности с открытым текстом в каждый момент времени, таких как почта или веб-серверы.</span><span class="sxs-lookup"><span data-stu-id="78c4d-140">This type is also for higher performance servers that process many plaintext authentication attempts at a time, such as mail or web servers.</span></span> <span data-ttu-id="78c4d-141">Функция **логонусерексексв** не кэширует учетные данные для этого типа входа.</span><span class="sxs-lookup"><span data-stu-id="78c4d-141">The **LogonUserExExW** function does not cache credentials for this logon type.</span></span><br/>                                                                                                           |
| <span id="LOGON32_LOGON_SERVICE"></span><span id="logon32_logon_service"></span><dl> <span data-ttu-id="78c4d-142"><dt>**LOGON32 \_ \_Служба входа**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="78c4d-142"><dt>**LOGON32\_LOGON\_SERVICE**</dt> <dt>5</dt></span></span> </dl>                                | <span data-ttu-id="78c4d-143">Указывает на тип входа в службу.</span><span class="sxs-lookup"><span data-stu-id="78c4d-143">Indicates a service-type logon.</span></span> <span data-ttu-id="78c4d-144">Предоставленная учетная запись должна иметь права на доступ к службе.</span><span class="sxs-lookup"><span data-stu-id="78c4d-144">The account provided must have the service privilege enabled.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="LOGON32_LOGON_UNLOCK"></span><span id="logon32_logon_unlock"></span><dl> <span data-ttu-id="78c4d-145"><dt>**LOGON32 \_ \_Разблокировка входа**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="78c4d-145"><dt>**LOGON32\_LOGON\_UNLOCK**</dt> <dt>7</dt></span></span> </dl>                                   | <span data-ttu-id="78c4d-146">Этот тип входа предназначен для библиотек DLL [*GINA*](../secgloss/g-gly.md) , которые входят в систему пользователей, которые будут интерактивно использовать компьютер.</span><span class="sxs-lookup"><span data-stu-id="78c4d-146">This logon type is for [*GINA*](../secgloss/g-gly.md) DLLs that log on users who will be interactively using the computer.</span></span> <span data-ttu-id="78c4d-147">Этот тип входа может создать уникальную запись аудита, которая показывает, когда Рабочая станция была разблокирована.</span><span class="sxs-lookup"><span data-stu-id="78c4d-147">This logon type can generate a unique audit record that shows when the workstation was unlocked.</span></span><br/>                                                                                                                                                                                                                   |
| <span id="LOGON32_LOGON_NETWORK_CLEARTEXT"></span><span id="logon32_logon_network_cleartext"></span><dl> <span data-ttu-id="78c4d-148"><dt>**LOGON32 \_ Вход в \_ сеть с \_ открытым текстом**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="78c4d-148"><dt>**LOGON32\_LOGON\_NETWORK\_CLEARTEXT**</dt> <dt>8</dt></span></span> </dl> | <span data-ttu-id="78c4d-149">Этот тип входа сохраняет имя и пароль в [*пакете проверки подлинности*](../secgloss/a-gly.md), что позволяет серверу устанавливать соединения с другими сетевыми серверами при олицетворении клиента.</span><span class="sxs-lookup"><span data-stu-id="78c4d-149">This logon type preserves the name and password in the [*authentication package*](../secgloss/a-gly.md), which allows the server to make connections to other network servers while impersonating the client.</span></span> <span data-ttu-id="78c4d-150">Сервер может принимать учетные данные открытого текста от клиента, вызывать **логонусерексексв**, проверять, может ли пользователь получить доступ к системе по сети и по-прежнему взаимодействовать с другими серверами.</span><span class="sxs-lookup"><span data-stu-id="78c4d-150">A server can accept plaintext credentials from a client, call **LogonUserExExW**, verify that the user can access the system across the network, and still communicate with other servers.</span></span> <br/> |
| <span id="LOGON32_LOGON_NEW_CREDENTIALS"></span><span id="logon32_logon_new_credentials"></span><dl> <span data-ttu-id="78c4d-151"><dt>**LOGON32 \_ ВХОД с \_ новыми \_ учетными данными**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="78c4d-151"><dt>**LOGON32\_LOGON\_NEW\_CREDENTIALS**</dt> <dt>9</dt></span></span> </dl>       | <span data-ttu-id="78c4d-152">Этот тип входа позволяет вызывающему объекту клонировать его текущий токен и указывать новые учетные данные для исходящих соединений.</span><span class="sxs-lookup"><span data-stu-id="78c4d-152">This logon type allows the caller to clone its current token and specify new credentials for outbound connections.</span></span> <span data-ttu-id="78c4d-153">Новый сеанс входа имеет тот же локальный идентификатор, но использует другие учетные данные для других сетевых подключений.</span><span class="sxs-lookup"><span data-stu-id="78c4d-153">The new logon session has the same local identifier but uses different credentials for other network connections.</span></span><br/> <span data-ttu-id="78c4d-154">Этот тип входа поддерживается только поставщиком **LOGON32 \_ provider \_ WINNT50** .</span><span class="sxs-lookup"><span data-stu-id="78c4d-154">This logon type is supported only by the **LOGON32\_PROVIDER\_WINNT50** logon provider.</span></span><br/>                                                                                                                                       |



 

</dd> <dt>

<span data-ttu-id="78c4d-155">*двлогонпровидер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="78c4d-155">*dwLogonProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78c4d-156">Поставщик входа в систему.</span><span class="sxs-lookup"><span data-stu-id="78c4d-156">The logon provider.</span></span> <span data-ttu-id="78c4d-157">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="78c4d-157">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="78c4d-158">Значение</span><span class="sxs-lookup"><span data-stu-id="78c4d-158">Value</span></span>                                                                                                                                                                                           | <span data-ttu-id="78c4d-159">Значение</span><span class="sxs-lookup"><span data-stu-id="78c4d-159">Meaning</span></span>                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LOGON32_PROVIDER_DEFAULT"></span><span id="logon32_provider_default"></span><dl> <span data-ttu-id="78c4d-160"><dt>**\_Поставщик LOGON32 \_ по умолчанию**</dt></span><span class="sxs-lookup"><span data-stu-id="78c4d-160"><dt>**LOGON32\_PROVIDER\_DEFAULT**</dt></span></span> </dl> | <span data-ttu-id="78c4d-161">Использовать стандартный поставщик входа в систему.</span><span class="sxs-lookup"><span data-stu-id="78c4d-161">Use the standard logon provider for the system.</span></span> <span data-ttu-id="78c4d-162">По умолчанию используется [*поставщик безопасности*](../secgloss/s-gly.md) NTLM.</span><span class="sxs-lookup"><span data-stu-id="78c4d-162">The default [*security provider*](../secgloss/s-gly.md) is NTLM.</span></span><br/> |
| <span id="LOGON32_PROVIDER_WINNT50"></span><span id="logon32_provider_winnt50"></span><dl> <span data-ttu-id="78c4d-163"><dt>**\_WINNT50 поставщика \_ LOGON32**</dt></span><span class="sxs-lookup"><span data-stu-id="78c4d-163"><dt>**LOGON32\_PROVIDER\_WINNT50**</dt></span></span> </dl> | <span data-ttu-id="78c4d-164">Используйте поставщик согласованного входа в систему.</span><span class="sxs-lookup"><span data-stu-id="78c4d-164">Use the negotiate logon provider.</span></span> <br/>                                                                                                                                                         |
| <span id="LOGON32_PROVIDER_WINNT40"></span><span id="logon32_provider_winnt40"></span><dl> <span data-ttu-id="78c4d-165"><dt>**\_WINNT40 поставщика \_ LOGON32**</dt></span><span class="sxs-lookup"><span data-stu-id="78c4d-165"><dt>**LOGON32\_PROVIDER\_WINNT40**</dt></span></span> </dl> | <span data-ttu-id="78c4d-166">Используйте поставщик входа NTLM.</span><span class="sxs-lookup"><span data-stu-id="78c4d-166">Use the NTLM logon provider.</span></span><br/>                                                                                                                                                               |



 

</dd> <dt>

<span data-ttu-id="78c4d-167">*птокенграупс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="78c4d-167">*pTokenGroups* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="78c4d-168">Указатель на структуру [**\_ групп токенов**](/windows/win32/api/winnt/ns-winnt-token_groups) , указывающий список идентификаторов SID группы, которые добавляются к маркеру, получаемому этой функцией при успешном входе.</span><span class="sxs-lookup"><span data-stu-id="78c4d-168">A pointer to a [**TOKEN\_GROUPS**](/windows/win32/api/winnt/ns-winnt-token_groups) structure that specifies a list of group SIDs that are added to the token that this function receives upon successful logon.</span></span> <span data-ttu-id="78c4d-169">Все идентификаторы SID, добавленные в маркер, также влияют на расширение группы.</span><span class="sxs-lookup"><span data-stu-id="78c4d-169">Any SIDs added to the token also effect group expansion.</span></span> <span data-ttu-id="78c4d-170">Например, если добавленные идентификаторы SID являются членами локальных групп, эти группы также добавляются к полученному маркеру доступа.</span><span class="sxs-lookup"><span data-stu-id="78c4d-170">For example, if the added SIDs are members of local groups, those groups are also added to the received access token.</span></span>

<span data-ttu-id="78c4d-171">Если этот параметр не равен **null**, то вызывающей стороне этой функции должно быть предоставлено и включено право доступа **SE \_ \_** .</span><span class="sxs-lookup"><span data-stu-id="78c4d-171">If this parameter is not **NULL**, the caller of this function must have the **SE\_TCB\_PRIVILEGE** privilege granted and enabled.</span></span>

</dd> <dt>

<span data-ttu-id="78c4d-172">*фтокен* \[ out, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="78c4d-172">*phToken* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="78c4d-173">Указатель на переменную обработчика, которая получает маркер, представляющий указанного пользователя.</span><span class="sxs-lookup"><span data-stu-id="78c4d-173">A pointer to a handle variable that receives a handle to a token that represents the specified user.</span></span>

<span data-ttu-id="78c4d-174">Возвращаемый маркер можно использовать в вызовах функции [**имперсонателогжедонусер**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser) .</span><span class="sxs-lookup"><span data-stu-id="78c4d-174">You can use the returned handle in calls to the [**ImpersonateLoggedOnUser**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser) function.</span></span>

<span data-ttu-id="78c4d-175">В большинстве случаев возвращаемый обработчик является [*основным маркером*](../secgloss/p-gly.md) , который можно использовать в вызовах функции [**параметр CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) .</span><span class="sxs-lookup"><span data-stu-id="78c4d-175">In most cases, the returned handle is a [*primary token*](../secgloss/p-gly.md) that you can use in calls to the [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) function.</span></span> <span data-ttu-id="78c4d-176">Однако при указании \_ \_ флага сети LOGON32 logon **логонусерексексв** возвращает [*маркер олицетворения*](../secgloss/i-gly.md) , который нельзя использовать в **параметр CreateProcessAsUser** , если не был вызван [**дупликатетокенекс**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex) для преобразования токена олицетворения в основной маркер.</span><span class="sxs-lookup"><span data-stu-id="78c4d-176">However, if you specify the LOGON32\_LOGON\_NETWORK flag, **LogonUserExExW** returns an [*impersonation token*](../secgloss/i-gly.md) that you cannot use in **CreateProcessAsUser** unless you call [**DuplicateTokenEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex) to convert the impersonation token to a primary token.</span></span>

<span data-ttu-id="78c4d-177">Если этот обработчик больше не нужен, закройте его, вызвав функцию [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) .</span><span class="sxs-lookup"><span data-stu-id="78c4d-177">When you no longer need this handle, close it by calling the [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) function.</span></span>

</dd> <dt>

<span data-ttu-id="78c4d-178">*пплогонсид* \[ out, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="78c4d-178">*ppLogonSid* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="78c4d-179">Указатель на указатель на идентификатор безопасности, который получает идентификатор безопасности пользователя, вошедшего в систему.</span><span class="sxs-lookup"><span data-stu-id="78c4d-179">A pointer to a pointer to a SID that receives the SID of the user logged on.</span></span>

<span data-ttu-id="78c4d-180">Завершив использование идентификатора безопасности, освободите его, вызвав функцию [**функции LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) .</span><span class="sxs-lookup"><span data-stu-id="78c4d-180">When you have finished using the SID, free it by calling the [**LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) function.</span></span>

</dd> <dt>

<span data-ttu-id="78c4d-181">*пппрофилебуффер* \[ out, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="78c4d-181">*ppProfileBuffer* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="78c4d-182">Указатель на указатель, получающий адрес буфера, который содержит профиль пользователя, вошедшего в систему.</span><span class="sxs-lookup"><span data-stu-id="78c4d-182">A pointer to a pointer that receives the address of a buffer that contains the logged on user's profile.</span></span>

</dd> <dt>

<span data-ttu-id="78c4d-183">*пдвпрофилеленгс* \[ out, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="78c4d-183">*pdwProfileLength* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="78c4d-184">Указатель на **DWORD** , который получает длину буфера профиля.</span><span class="sxs-lookup"><span data-stu-id="78c4d-184">A pointer to a **DWORD** that receives the length of the profile buffer.</span></span>

</dd> <dt>

<span data-ttu-id="78c4d-185">*пкуоталимитс* \[ out, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="78c4d-185">*pQuotaLimits* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="78c4d-186">Указатель на структуру [**\_ ограничений квоты**](/windows/desktop/api/Winnt/ns-winnt-quota_limits) , которая получает сведения о квотах для вошедшего в систему пользователя.</span><span class="sxs-lookup"><span data-stu-id="78c4d-186">A pointer to a [**QUOTA\_LIMITS**](/windows/desktop/api/Winnt/ns-winnt-quota_limits) structure that receives information about the quotas for the logged on user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78c4d-187">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="78c4d-187">Return value</span></span>

<span data-ttu-id="78c4d-188">Если функция завершается с ошибкой, функция возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="78c4d-188">If the function succeeds, the function returns nonzero.</span></span>

<span data-ttu-id="78c4d-189">Если функция завершается ошибкой, она возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="78c4d-189">If the function fails, it returns zero.</span></span> <span data-ttu-id="78c4d-190">Дополнительные сведения об ошибке можно получить, вызвав [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="78c4d-190">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="78c4d-191">Комментарии</span><span class="sxs-lookup"><span data-stu-id="78c4d-191">Remarks</span></span>

<span data-ttu-id="78c4d-192">Тип входа в **\_ \_ сеть LOGON32 logon** — самый быстрый, но он имеет следующие ограничения.</span><span class="sxs-lookup"><span data-stu-id="78c4d-192">The **LOGON32\_LOGON\_NETWORK** logon type is fastest, but it has the following limitations:</span></span>

-   <span data-ttu-id="78c4d-193">Функция возвращает [*маркер олицетворения*](../secgloss/i-gly.md), а не первичный токен.</span><span class="sxs-lookup"><span data-stu-id="78c4d-193">The function returns an [*impersonation token*](../secgloss/i-gly.md), not a primary token.</span></span> <span data-ttu-id="78c4d-194">Этот токен нельзя использовать непосредственно в функции [**параметр CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) .</span><span class="sxs-lookup"><span data-stu-id="78c4d-194">You cannot use this token directly in the [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) function.</span></span> <span data-ttu-id="78c4d-195">Однако можно вызвать функцию [**дупликатетокенекс**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex) для преобразования токена в основной токен, а затем использовать его в **параметр CreateProcessAsUser**.</span><span class="sxs-lookup"><span data-stu-id="78c4d-195">However, you can call the [**DuplicateTokenEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex) function to convert the token to a primary token, and then use it in **CreateProcessAsUser**.</span></span>
-   <span data-ttu-id="78c4d-196">Если вы преобразуете маркер в основной маркер и используете его в [**параметр CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) для запуска процесса, новый процесс не сможет получить доступ к другим сетевым ресурсам, таким как удаленные серверы или принтеры, через перенаправитель.</span><span class="sxs-lookup"><span data-stu-id="78c4d-196">If you convert the token to a primary token and use it in [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) to start a process, the new process cannot access other network resources, such as remote servers or printers, through the redirector.</span></span> <span data-ttu-id="78c4d-197">Исключением является то, что если сетевой ресурс не управляет доступом, новый процесс сможет получить к нему доступ.</span><span class="sxs-lookup"><span data-stu-id="78c4d-197">An exception is that if the network resource is not access controlled, then the new process will be able to access it.</span></span>

<span data-ttu-id="78c4d-198">Учетная запись, указанная параметром *лпсзусернаме* , должна иметь необходимые права учетной записи.</span><span class="sxs-lookup"><span data-stu-id="78c4d-198">The account specified by *lpszUsername* must have the necessary account rights.</span></span> <span data-ttu-id="78c4d-199">Например, чтобы войти в систему пользователя с флагом **\_ \_ интерактивного входа в LOGON32** , пользователь (или группа, к которой принадлежит пользователь) должен иметь право использовать **\_ интерактивное \_ \_ имя для входа в сеть** .</span><span class="sxs-lookup"><span data-stu-id="78c4d-199">For example, to log on a user with the **LOGON32\_LOGON\_INTERACTIVE** flag, the user (or a group to which the user belongs) must have the **SE\_INTERACTIVE\_LOGON\_NAME** account right.</span></span> <span data-ttu-id="78c4d-200">Список прав учетной записи, влияющих на различные операции входа в систему, см. в разделе [права доступа к объектам учетной записи](../secmgmt/account-object-access-rights.md).</span><span class="sxs-lookup"><span data-stu-id="78c4d-200">For a list of the account rights that affect the various logon operations, see [Account Object Access Rights](../secmgmt/account-object-access-rights.md).</span></span>

<span data-ttu-id="78c4d-201">Пользователь считается вошедшим в систему, если существует хотя бы один токен.</span><span class="sxs-lookup"><span data-stu-id="78c4d-201">A user is considered logged on if at least one token exists.</span></span> <span data-ttu-id="78c4d-202">Если вызвать [**параметр CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) и закрыть маркер, пользователь по-прежнему будет входить в систему, пока процесс (и все его дочерние процессы) не будут завершены.</span><span class="sxs-lookup"><span data-stu-id="78c4d-202">If you call [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) and then close the token, the user is still logged on until the process (and all child processes) have ended.</span></span>

<span data-ttu-id="78c4d-203">Если указан необязательный параметр *птокенграупс* , LSA не будет автоматически добавлять локальный SID или SID для входа.</span><span class="sxs-lookup"><span data-stu-id="78c4d-203">If the optional *pTokenGroups* parameter is supplied, LSA will not add either the local SID or the logon SID automatically.</span></span>

## <a name="requirements"></a><span data-ttu-id="78c4d-204">Требования</span><span class="sxs-lookup"><span data-stu-id="78c4d-204">Requirements</span></span>



| <span data-ttu-id="78c4d-205">Требование</span><span class="sxs-lookup"><span data-stu-id="78c4d-205">Requirement</span></span> | <span data-ttu-id="78c4d-206">Значение</span><span class="sxs-lookup"><span data-stu-id="78c4d-206">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78c4d-207">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="78c4d-207">Minimum supported client</span></span><br/> | <span data-ttu-id="78c4d-208">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="78c4d-208">Windows Vista \[desktop apps only\]</span></span><br/>                                                                        |
| <span data-ttu-id="78c4d-209">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="78c4d-209">Minimum supported server</span></span><br/> | <span data-ttu-id="78c4d-210">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="78c4d-210">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                  |
| <span data-ttu-id="78c4d-211">Версия</span><span class="sxs-lookup"><span data-stu-id="78c4d-211">Version</span></span><br/>                  | <span data-ttu-id="78c4d-212">Логонусерексексв также доступен в выпуске Windows Server 2003 или Windows Кспвис для общего распространения.</span><span class="sxs-lookup"><span data-stu-id="78c4d-212">LogonUserExExW is also available onWindows Server 2003 or Windows XPwith the General Distribution Release.</span></span><br/> |
| <span data-ttu-id="78c4d-213">Header</span><span class="sxs-lookup"><span data-stu-id="78c4d-213">Header</span></span><br/>                   | <dl> <span data-ttu-id="78c4d-214"><dt>Винбасеп. h</dt></span><span class="sxs-lookup"><span data-stu-id="78c4d-214"><dt>Winbasep.h</dt></span></span> </dl>                                 |
| <span data-ttu-id="78c4d-215">DLL</span><span class="sxs-lookup"><span data-stu-id="78c4d-215">DLL</span></span><br/>                      | <dl> <span data-ttu-id="78c4d-216"><dt>Advapi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78c4d-216"><dt>Advapi32.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="78c4d-217">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="78c4d-217">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78c4d-218">Управление доступом клиента/сервера</span><span class="sxs-lookup"><span data-stu-id="78c4d-218">Client/Server Access Control</span></span>](../secauthz/client-server-access-control.md)
</dt> <dt>

[<span data-ttu-id="78c4d-219">Функции управления доступом клиента/сервера</span><span class="sxs-lookup"><span data-stu-id="78c4d-219">Client/Server Access Control Functions</span></span>](../secauthz/authorization-functions.md)
</dt> <dt>

[<span data-ttu-id="78c4d-220">**CloseHandle**</span><span class="sxs-lookup"><span data-stu-id="78c4d-220">**CloseHandle**</span></span>](/windows/win32/api/handleapi/nf-handleapi-closehandle)
</dt> <dt>

[<span data-ttu-id="78c4d-221">**Параметр CreateProcessAsUser**</span><span class="sxs-lookup"><span data-stu-id="78c4d-221">**CreateProcessAsUser**</span></span>](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera)
</dt> <dt>

[<span data-ttu-id="78c4d-222">**дупликатетокенекс**</span><span class="sxs-lookup"><span data-stu-id="78c4d-222">**DuplicateTokenEx**</span></span>](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex)
</dt> <dt>

[<span data-ttu-id="78c4d-223">**имперсонателогжедонусер**</span><span class="sxs-lookup"><span data-stu-id="78c4d-223">**ImpersonateLoggedOnUser**</span></span>](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser)
</dt> <dt>

[<span data-ttu-id="78c4d-224">**логонусерекс**</span><span class="sxs-lookup"><span data-stu-id="78c4d-224">**LogonUserEx**</span></span>](/windows/desktop/api/Winbase/nf-winbase-logonuserexa)
</dt> <dt>

[<span data-ttu-id="78c4d-225">**ограничения КВОТы \_**</span><span class="sxs-lookup"><span data-stu-id="78c4d-225">**QUOTA\_LIMITS**</span></span>](/windows/desktop/api/Winnt/ns-winnt-quota_limits)
</dt> </dl>

 

 
