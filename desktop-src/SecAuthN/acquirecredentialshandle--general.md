---
description: Получает маркер для существующих учетных данных субъекта безопасности.
ms.assetid: acda4cf3-39a6-4bd2-91a0-db1f191b57b5
title: Функция AcquireCredentialsHandle (General) (SSPI. h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 9c1202d8b482eee45697cec35ff6a7e8ba6ef354
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105719641"
---
# <a name="acquirecredentialshandle-general-function"></a><span data-ttu-id="df41c-103">Функция AcquireCredentialsHandle (общая)</span><span class="sxs-lookup"><span data-stu-id="df41c-103">AcquireCredentialsHandle (General) function</span></span>

<span data-ttu-id="df41c-104">Функция **AcquireCredentialsHandle (General)** получает маркер для существующих учетных данных [*субъекта безопасности*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="df41c-104">The **AcquireCredentialsHandle (General)** function acquires a handle to preexisting credentials of a [*security principal*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="df41c-105">Этот обработчик необходим для функций [**InitializeSecurityContext (General)**](initializesecuritycontext--general.md) и [**AcceptSecurityContext (General)**](acceptsecuritycontext--general.md) .</span><span class="sxs-lookup"><span data-stu-id="df41c-105">This handle is required by the [**InitializeSecurityContext (General)**](initializesecuritycontext--general.md) and [**AcceptSecurityContext (General)**](acceptsecuritycontext--general.md) functions.</span></span> <span data-ttu-id="df41c-106">Это могут быть либо существовавшие ранее учетные данные, которые устанавливаются с помощью системного входа, не описываемого здесь, либо вызывающая сторона может предоставить альтернативные учетные данные.</span><span class="sxs-lookup"><span data-stu-id="df41c-106">These can be either preexisting credentials, which are established through a system logon that is not described here, or the caller can provide alternative credentials.</span></span>

> [!Note]  
> <span data-ttu-id="df41c-107">Это не «вход в сеть» и не предполагает сбор учетных данных.</span><span class="sxs-lookup"><span data-stu-id="df41c-107">This is not a "log on to the network" and does not imply gathering of credentials.</span></span>

 

<span data-ttu-id="df41c-108">Сведения об использовании этой функции с конкретным [*поставщиком поддержки безопасности*](../secgloss/s-gly.md) (SSP) см. в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="df41c-108">For information about using this function with a specific [*security support provider*](../secgloss/s-gly.md) (SSP), see the following topics.</span></span>



| <span data-ttu-id="df41c-109">Раздел</span><span class="sxs-lookup"><span data-stu-id="df41c-109">Topic</span></span>                                                                                           | <span data-ttu-id="df41c-110">Описание</span><span class="sxs-lookup"><span data-stu-id="df41c-110">Description</span></span>                                                                                                                                   |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="df41c-111">**AcquireCredentialsHandle (CredSSP)**</span><span class="sxs-lookup"><span data-stu-id="df41c-111">**AcquireCredentialsHandle (CredSSP)**</span></span>](acquirecredentialshandle--credssp.md)<br/>     | <span data-ttu-id="df41c-112">Получает маркер для существующих учетных данных субъекта безопасности, использующего поставщик поддержки безопасности учетных данных (CredSSP).</span><span class="sxs-lookup"><span data-stu-id="df41c-112">Acquires a handle to preexisting credentials of a security principal that is using Credential Security Support Provider (CredSSP).</span></span><br/> |
| [<span data-ttu-id="df41c-113">**AcquireCredentialsHandle (дайджест)**</span><span class="sxs-lookup"><span data-stu-id="df41c-113">**AcquireCredentialsHandle (Digest)**</span></span>](acquirecredentialshandle--digest.md)<br/>       | <span data-ttu-id="df41c-114">Получает маркер для существующих учетных данных субъекта безопасности, который использует дайджест.</span><span class="sxs-lookup"><span data-stu-id="df41c-114">Acquires a handle to preexisting credentials of a security principal that is using Digest.</span></span><br/>                                         |
| [<span data-ttu-id="df41c-115">**AcquireCredentialsHandle (Kerberos)**</span><span class="sxs-lookup"><span data-stu-id="df41c-115">**AcquireCredentialsHandle (Kerberos)**</span></span>](acquirecredentialshandle--kerberos.md)<br/>   | <span data-ttu-id="df41c-116">Получает маркер для существующих учетных данных субъекта безопасности, использующего протокол Kerberos.</span><span class="sxs-lookup"><span data-stu-id="df41c-116">Acquires a handle to preexisting credentials of a security principal that is using Kerberos.</span></span><br/>                                       |
| [<span data-ttu-id="df41c-117">**AcquireCredentialsHandle (согласование)**</span><span class="sxs-lookup"><span data-stu-id="df41c-117">**AcquireCredentialsHandle (Negotiate)**</span></span>](acquirecredentialshandle--negotiate.md)<br/> | <span data-ttu-id="df41c-118">Получает маркер для существующих учетных данных субъекта безопасности, использующего Negotiate.</span><span class="sxs-lookup"><span data-stu-id="df41c-118">Acquires a handle to preexisting credentials of a security principal that is using Negotiate.</span></span><br/>                                      |
| [<span data-ttu-id="df41c-119">**AcquireCredentialsHandle (NTLM)**</span><span class="sxs-lookup"><span data-stu-id="df41c-119">**AcquireCredentialsHandle (NTLM)**</span></span>](acquirecredentialshandle--ntlm.md)<br/>           | <span data-ttu-id="df41c-120">Получает маркер для существующих учетных данных субъекта безопасности, использующего NTLM.</span><span class="sxs-lookup"><span data-stu-id="df41c-120">Acquires a handle to preexisting credentials of a security principal that is using NTLM.</span></span><br/>                                           |
| [<span data-ttu-id="df41c-121">**AcquireCredentialsHandle (Schannel)**</span><span class="sxs-lookup"><span data-stu-id="df41c-121">**AcquireCredentialsHandle (Schannel)**</span></span>](acquirecredentialshandle--schannel.md)<br/>   | <span data-ttu-id="df41c-122">Получает маркер для существующих учетных данных субъекта безопасности, использующего SChannel.</span><span class="sxs-lookup"><span data-stu-id="df41c-122">Acquires a handle to preexisting credentials of a security principal that is using Schannel.</span></span><br/>                                       |



 

## <a name="syntax"></a><span data-ttu-id="df41c-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="df41c-123">Syntax</span></span>


```C++
SECURITY_STATUS SEC_Entry AcquireCredentialsHandle(
  _In_  SEC_CHAR       *pszPrincipal,
  _In_  SEC_CHAR       *pszPackage,
  _In_  ULONG          fCredentialUse,
  _In_  PLUID          pvLogonID,
  _In_  PVOID          pAuthData,
  _In_  SEC_GET_KEY_FN pGetKeyFn,
  _In_  PVOID          pvGetKeyArgument,
  _Out_ PCredHandle    phCredential,
  _Out_ PTimeStamp     ptsExpiry
);
```



## <a name="parameters"></a><span data-ttu-id="df41c-124">Параметры</span><span class="sxs-lookup"><span data-stu-id="df41c-124">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df41c-125">*псзпринЦипал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="df41c-125">*pszPrincipal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df41c-126">Указатель на строку, завершающуюся нулем, которая указывает имя участника, учетные данные которого будут ссылаться на этот обработчик.</span><span class="sxs-lookup"><span data-stu-id="df41c-126">A pointer to a null-terminated string that specifies the name of the principal whose credentials the handle will reference.</span></span>

<span data-ttu-id="df41c-127">При использовании дайджест-поставщика общих служб этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="df41c-127">When using the Digest SSP, this parameter is optional.</span></span>

<span data-ttu-id="df41c-128">При использовании поставщика общих служб SChannel этот параметр не используется и должен иметь значение **null**.</span><span class="sxs-lookup"><span data-stu-id="df41c-128">When using the Schannel SSP, this parameter is not used and should be set to **NULL**.</span></span>

> [!Note]  
> <span data-ttu-id="df41c-129">Если процесс, запрашивающий этот обработчик, не имеет доступа к учетным данным, функция возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="df41c-129">If the process that requests the handle does not have access to the credentials, the function returns an error.</span></span> <span data-ttu-id="df41c-130">Строка NULL указывает, что процессу требуется маркер для учетных данных пользователя, от имени которого выполняется [*контекст безопасности*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="df41c-130">A null string indicates that the process requires a handle to the credentials of the user under whose [*security context*](../secgloss/s-gly.md) it is executing.</span></span>

 

</dd> <dt>

<span data-ttu-id="df41c-131">*псзпаккаже* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="df41c-131">*pszPackage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df41c-132">Указатель на строку, завершающуюся нулем, которая указывает имя [*пакета безопасности*](../secgloss/s-gly.md) , с помощью которого будут использоваться эти учетные данные.</span><span class="sxs-lookup"><span data-stu-id="df41c-132">A pointer to a null-terminated string that specifies the name of the [*security package*](../secgloss/s-gly.md) with which these credentials will be used.</span></span> <span data-ttu-id="df41c-133">Это имя [*пакета безопасности*](../secgloss/s-gly.md) , возвращаемое в члене **Name** структуры [**Секпкгинфо**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) , возвращаемой функцией [**енумератесекуритипаккажес**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) .</span><span class="sxs-lookup"><span data-stu-id="df41c-133">This is a [*security package*](../secgloss/s-gly.md) name returned in the **Name** member of a [**SecPkgInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) structure returned by the [**EnumerateSecurityPackages**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) function.</span></span> <span data-ttu-id="df41c-134">После установки контекста [**QueryContextAttributes (Общие)**](querycontextattributes--general.md) можно вызвать с параметром *улаттрибуте* , для которого задано значение SECPKG \_ attr, \_ \_ чтобы вернуть сведения о используемом [*пакете безопасности*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="df41c-134">After a context is established, [**QueryContextAttributes (General)**](querycontextattributes--general.md) can be called with *ulAttribute* set to SECPKG\_ATTR\_PACKAGE\_INFO to return information on the [*security package*](../secgloss/s-gly.md) in use.</span></span>

<span data-ttu-id="df41c-135">При использовании дайджест-поставщика общих служб задайте для этого параметра значение WDIGEST \_ SP \_ Name.</span><span class="sxs-lookup"><span data-stu-id="df41c-135">When using the Digest SSP, set this parameter to WDIGEST\_SP\_NAME.</span></span>

<span data-ttu-id="df41c-136">При использовании поставщика общих служб SChannel присвойте этому параметру \_ имя унисп.</span><span class="sxs-lookup"><span data-stu-id="df41c-136">When using the Schannel SSP, set this parameter to UNISP\_NAME.</span></span>

</dd> <dt>

<span data-ttu-id="df41c-137">*фкредентиалусе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="df41c-137">*fCredentialUse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df41c-138">Флаг, указывающий, как будут использоваться эти учетные данные.</span><span class="sxs-lookup"><span data-stu-id="df41c-138">A flag that indicates how these credentials will be used.</span></span> <span data-ttu-id="df41c-139">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="df41c-139">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="df41c-140">Значение</span><span class="sxs-lookup"><span data-stu-id="df41c-140">Value</span></span>                                                                                                                                                                                                                                                                                    | <span data-ttu-id="df41c-141">Значение</span><span class="sxs-lookup"><span data-stu-id="df41c-141">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SECPKG_CRED_AUTOLOGON_RESTRICTED"></span><span id="secpkg_cred_autologon_restricted"></span><dl> <span data-ttu-id="df41c-142"><dt>**SECPKG \_ Режим \_ автоматического входа в систему с \_ ограничением**</dt> <dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="df41c-142"><dt>**SECPKG\_CRED\_AUTOLOGON\_RESTRICTED**</dt> <dt>0x00000010</dt></span></span> </dl> | <span data-ttu-id="df41c-143">В системе безопасности не используются учетные данные или учетные данные для входа по умолчанию из [диспетчера учетных данных](credential-manager.md).</span><span class="sxs-lookup"><span data-stu-id="df41c-143">The security does not use default logon credentials or credentials from [Credential Manager](credential-manager.md).</span></span><br/> <span data-ttu-id="df41c-144">Это значение поддерживается только [*ограниченным делегированием*](../secgloss/s-gly.md)Negotiate.</span><span class="sxs-lookup"><span data-stu-id="df41c-144">This value is supported only by the Negotiate [*constrained delegation*](../secgloss/s-gly.md).</span></span><br/> <span data-ttu-id="df41c-145">Windows **server 2008, Windows Vista, Windows server 2003 и Windows XP:** Это значение не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="df41c-145">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This value is not supported.</span></span><br/>                                                                                                                                 |
| <span id="SECPKG_CRED_BOTH"></span><span id="secpkg_cred_both"></span><dl> <span data-ttu-id="df41c-146"><dt>**SECPKG \_ cred \_**</dt></span><span class="sxs-lookup"><span data-stu-id="df41c-146"><dt>**SECPKG\_CRED\_BOTH**</dt></span></span> </dl>                                                                                                                  | <span data-ttu-id="df41c-147">Проверка входящих учетных данных или использование локальных учетных данных для подготовки исходящего маркера.</span><span class="sxs-lookup"><span data-stu-id="df41c-147">Validate an incoming credential or use a local credential to prepare an outgoing token.</span></span> <span data-ttu-id="df41c-148">Этот флаг включает и другие флаги.</span><span class="sxs-lookup"><span data-stu-id="df41c-148">This flag enables both other flags.</span></span> <span data-ttu-id="df41c-149">Этот флаг не является допустимым для хэш-правил дайджеста и SChannel.</span><span class="sxs-lookup"><span data-stu-id="df41c-149">This flag is not valid with the Digest and Schannel SSPs.</span></span><br/>                                                                                                                                                                                                                                                                |
| <span id="SECPKG_CRED_INBOUND"></span><span id="secpkg_cred_inbound"></span><dl> <span data-ttu-id="df41c-150"><dt>**SECPKG \_ cred \_ Inbound**</dt></span><span class="sxs-lookup"><span data-stu-id="df41c-150"><dt>**SECPKG\_CRED\_INBOUND**</dt></span></span> </dl>                                                                                                         | <span data-ttu-id="df41c-151">Проверка учетных данных входящего сервера.</span><span class="sxs-lookup"><span data-stu-id="df41c-151">Validate an incoming server credential.</span></span> <span data-ttu-id="df41c-152">Входящие учетные данные могут быть проверены с помощью центра проверки подлинности при вызове [**InitializeSecurityContext (General)**](initializesecuritycontext--general.md) или [**AcceptSecurityContext (General)**](acceptsecuritycontext--general.md) .</span><span class="sxs-lookup"><span data-stu-id="df41c-152">Inbound credentials might be validated by using an authenticating authority when [**InitializeSecurityContext (General)**](initializesecuritycontext--general.md) or [**AcceptSecurityContext (General)**](acceptsecuritycontext--general.md) is called.</span></span> <span data-ttu-id="df41c-153">Если такой центр недоступен, функция завершится ошибкой и возвратит значение, равное, \_ \_ без \_ центра проверки подлинности \_ .</span><span class="sxs-lookup"><span data-stu-id="df41c-153">If such an authority is not available, the function will fail and return SEC\_E\_NO\_AUTHENTICATING\_AUTHORITY.</span></span> <span data-ttu-id="df41c-154">Проверка зависит от пакета.</span><span class="sxs-lookup"><span data-stu-id="df41c-154">Validation is package specific.</span></span><br/> |
| <span id="SECPKG_CRED_OUTBOUND"></span><span id="secpkg_cred_outbound"></span><dl> <span data-ttu-id="df41c-155"><dt>**исходящий SECPKG \_ cred \_**</dt></span><span class="sxs-lookup"><span data-stu-id="df41c-155"><dt>**SECPKG\_CRED\_OUTBOUND**</dt></span></span> </dl>                                                                                                      | <span data-ttu-id="df41c-156">Разрешение учетных данных локального клиента для подготовки исходящего маркера.</span><span class="sxs-lookup"><span data-stu-id="df41c-156">Allow a local client credential to prepare an outgoing token.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="SECPKG_CRED_PROCESS_POLICY_ONLY"></span><span id="secpkg_cred_process_policy_only"></span><dl> <span data-ttu-id="df41c-157"><dt>**SECPKG \_ \_ \_ \_ Только политика процесса CRED**</dt> , <dt>0x00000020</dt></span><span class="sxs-lookup"><span data-stu-id="df41c-157"><dt>**SECPKG\_CRED\_PROCESS\_POLICY\_ONLY**</dt> <dt>0x00000020</dt></span></span> </dl>   | <span data-ttu-id="df41c-158">Функция обрабатывает политику сервера и возвращает данные в секунду, т. **\_ е. \_ не имеет \_ учетных данных**, указывая, что приложение должно запрашивать учетные данные.</span><span class="sxs-lookup"><span data-stu-id="df41c-158">The function processes server policy and returns **SEC\_E\_NO\_CREDENTIALS**, indicating that the application should prompt for credentials.</span></span><br/> <span data-ttu-id="df41c-159">Это значение поддерживается только [*ограниченным делегированием*](../secgloss/s-gly.md)Negotiate.</span><span class="sxs-lookup"><span data-stu-id="df41c-159">This value is supported only by the Negotiate [*constrained delegation*](../secgloss/s-gly.md).</span></span><br/> <span data-ttu-id="df41c-160">Windows **server 2008, Windows Vista, Windows server 2003 и Windows XP:** Это значение не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="df41c-160">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This value is not supported.</span></span><br/>                                                                                                          |



 

</dd> <dt>

<span data-ttu-id="df41c-161">*пвлогонид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="df41c-161">*pvLogonID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df41c-162">Указатель на [*локально уникальный идентификатор*](../secgloss/l-gly.md) (LUID), определяющий пользователя.</span><span class="sxs-lookup"><span data-stu-id="df41c-162">A pointer to a [*locally unique identifier*](../secgloss/l-gly.md) (LUID) that identifies the user.</span></span> <span data-ttu-id="df41c-163">Этот параметр предоставляется для процессов файловой системы, таких как сетевые перенаправления.</span><span class="sxs-lookup"><span data-stu-id="df41c-163">This parameter is provided for file-system processes such as network redirectors.</span></span> <span data-ttu-id="df41c-164">Этот параметр может принимать значение **NULL**.</span><span class="sxs-lookup"><span data-stu-id="df41c-164">This parameter can be **NULL**.</span></span>

<span data-ttu-id="df41c-165">При использовании поставщика общих служб SChannel этот параметр не используется и должен иметь значение **null**.</span><span class="sxs-lookup"><span data-stu-id="df41c-165">When using the Schannel SSP, this parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="df41c-166">*паусдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="df41c-166">*pAuthData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df41c-167">Указатель на данные, зависящие от пакета.</span><span class="sxs-lookup"><span data-stu-id="df41c-167">A pointer to package-specific data.</span></span> <span data-ttu-id="df41c-168">Этот параметр может иметь **значение NULL**, что означает, что необходимо использовать учетные данные по умолчанию для этого [*пакета безопасности*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="df41c-168">This parameter can be **NULL**, which indicates that the default credentials for that [*security package*](../secgloss/s-gly.md) must be used.</span></span> <span data-ttu-id="df41c-169">Чтобы использовать предоставленные учетные данные, передайте в этом параметре структуру [**\_ \_ \_ удостоверений проверки подлинности WinNT (с**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) ).</span><span class="sxs-lookup"><span data-stu-id="df41c-169">To use supplied credentials, pass a [**SEC\_WINNT\_AUTH\_IDENTITY**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) structure that includes those credentials in this parameter.</span></span> <span data-ttu-id="df41c-170">Время выполнения RPC передает все, что было указано в [**рпкбиндингсетаусинфо**](/windows/win32/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo).</span><span class="sxs-lookup"><span data-stu-id="df41c-170">The RPC run time passes whatever was provided in [**RpcBindingSetAuthInfo**](/windows/win32/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo).</span></span>

<span data-ttu-id="df41c-171">При использовании дайджест-поставщика общих служб этот параметр является указателем на [**структуру \_ \_ \_ удостоверения WinNT auth в секунду**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) , которая содержит сведения для проверки подлинности, используемые для нахождение учетных данных.</span><span class="sxs-lookup"><span data-stu-id="df41c-171">When using the Digest SSP, this parameter is a pointer to a [**SEC\_WINNT\_AUTH\_IDENTITY**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) structure that contains authentication information to use to locate the credentials.</span></span>

<span data-ttu-id="df41c-172">При использовании поставщика общих служб SChannel укажите структуру учетных записи [**SChannel \_**](/windows/win32/api/schannel/ns-schannel-schannel_cred) , указывающую используемый протокол, и параметры для различных настраиваемых функций канала.</span><span class="sxs-lookup"><span data-stu-id="df41c-172">When using the Schannel SSP, specify an [**SCHANNEL\_CRED**](/windows/win32/api/schannel/ns-schannel-schannel_cred) structure that indicates the protocol to use and the settings for various customizable channel features.</span></span>

<span data-ttu-id="df41c-173">При использовании пакетов NTLM или Negotiate максимальная длина символов для имени пользователя, пароля и домена составляет 256, 256 и 15 соответственно.</span><span class="sxs-lookup"><span data-stu-id="df41c-173">When using the NTLM or Negotiate packages, the maximum character lengths for user name, password, and domain are 256, 256, and 15, respectively.</span></span>

</dd> <dt>

<span data-ttu-id="df41c-174">*пжеткэйфн* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="df41c-174">*pGetKeyFn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df41c-175">Этот параметр не используется и должен иметь значение **null**.</span><span class="sxs-lookup"><span data-stu-id="df41c-175">This parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="df41c-176">*пвжеткэйаргумент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="df41c-176">*pvGetKeyArgument* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df41c-177">Этот параметр не используется и должен иметь значение **null**.</span><span class="sxs-lookup"><span data-stu-id="df41c-177">This parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="df41c-178">*фкредентиал* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="df41c-178">*phCredential* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="df41c-179">Указатель на структуру [кредхандле](sspi-handles.md) для получения маркера учетных данных.</span><span class="sxs-lookup"><span data-stu-id="df41c-179">A pointer to a [CredHandle](sspi-handles.md) structure to receive the credential handle.</span></span>

</dd> <dt>

<span data-ttu-id="df41c-180">*птсекспири* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="df41c-180">*ptsExpiry* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="df41c-181">Указатель на структуру [**метки времени**](timestamp.md) , которая получает время истечения срока действия возвращенных учетных данных.</span><span class="sxs-lookup"><span data-stu-id="df41c-181">A pointer to a [**TimeStamp**](timestamp.md) structure that receives the time at which the returned credentials expire.</span></span> <span data-ttu-id="df41c-182">Значение, возвращаемое этой структурой **отметок времени** , зависит от [*ограниченного делегирования*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="df41c-182">The value returned in this **TimeStamp** structure depends on the [*constrained delegation*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="df41c-183">[*Пакет безопасности*](../secgloss/s-gly.md) должен вернуть это значение в местное время.</span><span class="sxs-lookup"><span data-stu-id="df41c-183">The [*security package*](../secgloss/s-gly.md) must return this value in local time.</span></span>

<span data-ttu-id="df41c-184">Для этого параметра задается постоянное максимальное время.</span><span class="sxs-lookup"><span data-stu-id="df41c-184">This parameter is set to a constant maximum time.</span></span> <span data-ttu-id="df41c-185">Нет времени истечения срока действия для дайджест- [*контекста безопасности*](../secgloss/s-gly.md)или учетных данных, либо при использовании дайджест-поставщика общих служб.</span><span class="sxs-lookup"><span data-stu-id="df41c-185">There is no expiration time for Digest [*security context*](../secgloss/s-gly.md)s or credentials or when using the Digest SSP.</span></span>

<span data-ttu-id="df41c-186">При использовании поставщика общих служб SChannel этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="df41c-186">When using the Schannel SSP, this parameter is optional.</span></span> <span data-ttu-id="df41c-187">Если учетные данные, используемые для проверки подлинности, являются сертификатом, этот параметр получает срок действия этого сертификата.</span><span class="sxs-lookup"><span data-stu-id="df41c-187">When the credential to be used for authentication is a certificate, this parameter receives the expiration time for that certificate.</span></span> <span data-ttu-id="df41c-188">Если сертификат не указан, возвращается максимальное значение времени.</span><span class="sxs-lookup"><span data-stu-id="df41c-188">If no certificate was supplied, then a maximum time value is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df41c-189">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="df41c-189">Return value</span></span>

<span data-ttu-id="df41c-190">Если функция завершается успешно, функция возвращает значение секунды \_ E \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="df41c-190">If the function succeeds, the function returns SEC\_E\_OK.</span></span>

<span data-ttu-id="df41c-191">Если функция завершается ошибкой, возвращается один из следующих кодов ошибок.</span><span class="sxs-lookup"><span data-stu-id="df41c-191">If the function fails, it returns one of the following error codes.</span></span>



| <span data-ttu-id="df41c-192">Код возврата</span><span class="sxs-lookup"><span data-stu-id="df41c-192">Return code</span></span>                                                                                                 | <span data-ttu-id="df41c-193">Описание</span><span class="sxs-lookup"><span data-stu-id="df41c-193">Description</span></span>                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="df41c-194"><dt>**СЕК \_ . \_ недостаточный \_ объем памяти**</dt></span><span class="sxs-lookup"><span data-stu-id="df41c-194"><dt>**SEC\_E\_INSUFFICIENT\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="df41c-195">Недостаточно доступной памяти для завершения запрошенного действия.</span><span class="sxs-lookup"><span data-stu-id="df41c-195">There is not enough memory available to complete the requested action.</span></span><br/>                                                                  |
| <dl> <span data-ttu-id="df41c-196"><dt>**\_ \_ Внутренняя ошибка E \_ sec**</dt></span><span class="sxs-lookup"><span data-stu-id="df41c-196"><dt>**SEC\_E\_INTERNAL\_ERROR**</dt></span></span> </dl>      | <span data-ttu-id="df41c-197">Произошла ошибка, которая не сопоставлена с кодом ошибки SSPI.</span><span class="sxs-lookup"><span data-stu-id="df41c-197">An error occurred that did not map to an SSPI error code.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="df41c-198"><dt>**с \_ \_ без \_ учетных данных**</dt></span><span class="sxs-lookup"><span data-stu-id="df41c-198"><dt>**SEC\_E\_NO\_CREDENTIALS**</dt></span></span> </dl>      | <span data-ttu-id="df41c-199">Учетные данные недоступны в [*ограниченном делегировании*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="df41c-199">No credentials are available in the [*constrained delegation*](../secgloss/s-gly.md).</span></span><br/> |
| <dl> <span data-ttu-id="df41c-200"><dt>**СЕК. \_ е. \_ не \_ владелец**</dt></span><span class="sxs-lookup"><span data-stu-id="df41c-200"><dt>**SEC\_E\_NOT\_OWNER**</dt></span></span> </dl>           | <span data-ttu-id="df41c-201">Вызывающий объект функции не имеет необходимых учетных данных.</span><span class="sxs-lookup"><span data-stu-id="df41c-201">The caller of the function does not have the necessary credentials.</span></span><br/>                                                                     |
| <dl> <span data-ttu-id="df41c-202"><dt>**с \_ е \_ SECPKG \_ не \_ Найдено**</dt></span><span class="sxs-lookup"><span data-stu-id="df41c-202"><dt>**SEC\_E\_SECPKG\_NOT\_FOUND**</dt></span></span> </dl>   | <span data-ttu-id="df41c-203">Запрошенный [*пакет безопасности*](../secgloss/s-gly.md) не существует.</span><span class="sxs-lookup"><span data-stu-id="df41c-203">The requested [*security package*](../secgloss/s-gly.md) does not exist.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="df41c-204"><dt>**с \_ е \_ неизвестные \_ учетные данные**</dt></span><span class="sxs-lookup"><span data-stu-id="df41c-204"><dt>**SEC\_E\_UNKNOWN\_CREDENTIALS**</dt></span></span> </dl> | <span data-ttu-id="df41c-205">Учетные данные, предоставленные пакету, не распознаны.</span><span class="sxs-lookup"><span data-stu-id="df41c-205">The credentials supplied to the package were not recognized.</span></span><br/>                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="df41c-206">Комментарии</span><span class="sxs-lookup"><span data-stu-id="df41c-206">Remarks</span></span>

<span data-ttu-id="df41c-207">Функция **AcquireCredentialsHandle (General)** возвращает маркер учетных данных участника, например пользователя или клиента, который используется конкретным [*ограниченным делегированием*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="df41c-207">The **AcquireCredentialsHandle (General)** function returns a handle to the credentials of a principal, such as a user or client, as used by a specific [*constrained delegation*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="df41c-208">Это может быть обработчик существующих учетных данных, или функция может создать новый набор учетных данных и вернуть их.</span><span class="sxs-lookup"><span data-stu-id="df41c-208">This can be the handle to preexisting credentials, or the function can create a new set of credentials and return it.</span></span> <span data-ttu-id="df41c-209">Этот маркер можно использовать при последующих вызовах функций [**AcceptSecurityContext (General)**](acceptsecuritycontext--general.md) и [**InitializeSecurityContext (General)**](initializesecuritycontext--general.md) .</span><span class="sxs-lookup"><span data-stu-id="df41c-209">This handle can be used in subsequent calls to the [**AcceptSecurityContext (General)**](acceptsecuritycontext--general.md) and [**InitializeSecurityContext (General)**](initializesecuritycontext--general.md) functions.</span></span>

<span data-ttu-id="df41c-210">Как правило, **AcquireCredentialsHandle (Общие)** не позволяет процессу получить маркер учетных данных других пользователей, выполнивших вход на тот же компьютер.</span><span class="sxs-lookup"><span data-stu-id="df41c-210">In general, **AcquireCredentialsHandle (General)** does not allow a process to obtain a handle to the credentials of other users logged on to the same computer.</span></span> <span data-ttu-id="df41c-211">Однако у вызывающего \_ \_ [*право доступа*](../secgloss/s-gly.md) к имени TCB есть возможность указать [*идентификатор входа*](../secgloss/l-gly.md) (LUID) любого существующего маркера сеанса входа, чтобы получить маркер для учетных данных этого сеанса.</span><span class="sxs-lookup"><span data-stu-id="df41c-211">However, a caller with SE\_TCB\_NAME [*privilege*](../secgloss/s-gly.md) has the option of specifying the [*logon identifier*](../secgloss/l-gly.md) (LUID) of any existing logon session token to get a handle to that session's credentials.</span></span> <span data-ttu-id="df41c-212">Обычно это используется модулями режима ядра, которые должны действовать от имени вошедшего в систему пользователя.</span><span class="sxs-lookup"><span data-stu-id="df41c-212">Typically, this is used by kernel-mode modules that must act on behalf of a logged-on user.</span></span>

<span data-ttu-id="df41c-213">Пакет может вызвать функцию в *пжеткэйфн* , предоставляемую транспортом времени выполнения RPC.</span><span class="sxs-lookup"><span data-stu-id="df41c-213">A package might call the function in *pGetKeyFn* provided by the RPC run-time transport.</span></span> <span data-ttu-id="df41c-214">Если транспорт не поддерживает понятие обратного вызова для получения учетных данных, этот параметр должен иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="df41c-214">If the transport does not support the notion of callback to retrieve credentials, this parameter must be **NULL**.</span></span>

<span data-ttu-id="df41c-215">Для вызывающих объектов в режиме ядра необходимо отметить следующие отличия.</span><span class="sxs-lookup"><span data-stu-id="df41c-215">For kernel mode callers, the following differences must be noted:</span></span>

-   <span data-ttu-id="df41c-216">Два строковых параметра должны быть строками в [*Юникоде*](../secgloss/u-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="df41c-216">The two string parameters must be [*Unicode*](../secgloss/u-gly.md) strings.</span></span>
-   <span data-ttu-id="df41c-217">Значения буфера должны выделяться в виртуальной памяти процесса, а не в пуле.</span><span class="sxs-lookup"><span data-stu-id="df41c-217">The buffer values must be allocated in process virtual memory, not from the pool.</span></span>

<span data-ttu-id="df41c-218">По завершении использования возвращенных учетных данных освободите память, используемую учетными данными, вызвав функцию [**фрикредентиалшандле**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle) .</span><span class="sxs-lookup"><span data-stu-id="df41c-218">When you have finished using the returned credentials, free the memory used by the credentials by calling the [**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="df41c-219">Требования</span><span class="sxs-lookup"><span data-stu-id="df41c-219">Requirements</span></span>



| <span data-ttu-id="df41c-220">Требование</span><span class="sxs-lookup"><span data-stu-id="df41c-220">Requirement</span></span> | <span data-ttu-id="df41c-221">Значение</span><span class="sxs-lookup"><span data-stu-id="df41c-221">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df41c-222">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="df41c-222">Minimum supported client</span></span><br/> | <span data-ttu-id="df41c-223">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="df41c-223">Windows XP \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="df41c-224">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="df41c-224">Minimum supported server</span></span><br/> | <span data-ttu-id="df41c-225">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="df41c-225">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="df41c-226">Header</span><span class="sxs-lookup"><span data-stu-id="df41c-226">Header</span></span><br/>                   | <dl> <span data-ttu-id="df41c-227"><dt>SSPI. h (включая Security. h)</dt></span><span class="sxs-lookup"><span data-stu-id="df41c-227"><dt>Sspi.h (include Security.h)</dt></span></span> </dl> |
| <span data-ttu-id="df41c-228">Библиотека</span><span class="sxs-lookup"><span data-stu-id="df41c-228">Library</span></span><br/>                  | <dl> <span data-ttu-id="df41c-229"><dt>Secur32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="df41c-229"><dt>Secur32.lib</dt></span></span> </dl>                 |
| <span data-ttu-id="df41c-230">DLL</span><span class="sxs-lookup"><span data-stu-id="df41c-230">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df41c-231"><dt>Secur32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df41c-231"><dt>Secur32.dll</dt></span></span> </dl>                 |
| <span data-ttu-id="df41c-232">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="df41c-232">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="df41c-233">**Аккуирекредентиалшандлев** (Юникод) и **аккуирекредентиалшандлеа** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="df41c-233">**AcquireCredentialsHandleW** (Unicode) and **AcquireCredentialsHandleA** (ANSI)</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="df41c-234">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="df41c-234">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df41c-235">Функции SSPI</span><span class="sxs-lookup"><span data-stu-id="df41c-235">SSPI Functions</span></span>](authentication-functions.md#sspi-functions)
</dt> <dt>

[<span data-ttu-id="df41c-236">**AcceptSecurityContext (Общие)**</span><span class="sxs-lookup"><span data-stu-id="df41c-236">**AcceptSecurityContext (General)**</span></span>](acceptsecuritycontext--general.md)
</dt> <dt>

[<span data-ttu-id="df41c-237">**InitializeSecurityContext (Общие)**</span><span class="sxs-lookup"><span data-stu-id="df41c-237">**InitializeSecurityContext (General)**</span></span>](initializesecuritycontext--general.md)
</dt> <dt>

[<span data-ttu-id="df41c-238">**фрикредентиалшандле**</span><span class="sxs-lookup"><span data-stu-id="df41c-238">**FreeCredentialsHandle**</span></span>](/windows/win32/api/sspi/nf-sspi-freecredentialshandle)
</dt> </dl>

 

 
