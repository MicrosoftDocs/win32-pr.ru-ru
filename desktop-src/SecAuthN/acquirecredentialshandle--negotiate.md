---
description: Получает маркер для существующих учетных данных субъекта безопасности, использующего Negotiate.
ms.assetid: ff372163-c73b-41bb-afcb-7d5de7720967
title: Функция AcquireCredentialsHandle (Negotiate) (SSPI. h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 80ab4b67866b60831dadb7d8eb9bf9f632c0661c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105719639"
---
# <a name="acquirecredentialshandle-negotiate-function"></a><span data-ttu-id="1968a-103">Функция AcquireCredentialsHandle (Negotiate)</span><span class="sxs-lookup"><span data-stu-id="1968a-103">AcquireCredentialsHandle (Negotiate) function</span></span>

<span data-ttu-id="1968a-104">Функция **AcquireCredentialsHandle (Negotiate)** получает маркер для существующих учетных данных [*субъекта безопасности*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="1968a-104">The **AcquireCredentialsHandle (Negotiate)** function acquires a handle to preexisting credentials of a [*security principal*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="1968a-105">Этот обработчик необходим для функций [**InitializeSecurityContext (Negotiate)**](initializesecuritycontext--negotiate.md) и [**AcceptSecurityContext (Negotiate)**](acceptsecuritycontext--negotiate.md) .</span><span class="sxs-lookup"><span data-stu-id="1968a-105">This handle is required by the [**InitializeSecurityContext (Negotiate)**](initializesecuritycontext--negotiate.md) and [**AcceptSecurityContext (Negotiate)**](acceptsecuritycontext--negotiate.md) functions.</span></span> <span data-ttu-id="1968a-106">Это могут быть либо существовавшие ранее *учетные данные*, которые устанавливаются с помощью системного входа, не описываемого здесь, либо вызывающая сторона может предоставить альтернативные учетные данные.</span><span class="sxs-lookup"><span data-stu-id="1968a-106">These can be either preexisting *credentials*, which are established through a system logon that is not described here, or the caller can provide alternative credentials.</span></span>

> [!Note]  
> <span data-ttu-id="1968a-107">Это не «вход в сеть» и не предполагает сбор учетных данных.</span><span class="sxs-lookup"><span data-stu-id="1968a-107">This is not a "log on to the network" and does not imply gathering of credentials.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="1968a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1968a-108">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="1968a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="1968a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1968a-110">*псзпринЦипал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1968a-110">*pszPrincipal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1968a-111">Указатель на строку, завершающуюся нулем, которая указывает имя участника, учетные данные которого будут ссылаться на этот обработчик.</span><span class="sxs-lookup"><span data-stu-id="1968a-111">A pointer to a null-terminated string that specifies the name of the principal whose credentials the handle will reference.</span></span>

> [!Note]  
> <span data-ttu-id="1968a-112">Если процесс, запрашивающий этот обработчик, не имеет доступа к учетным данным, функция возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="1968a-112">If the process that requests the handle does not have access to the credentials, the function returns an error.</span></span> <span data-ttu-id="1968a-113">Строка NULL указывает, что процессу требуется маркер для учетных данных пользователя, от имени которого выполняется [*контекст безопасности*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="1968a-113">A null string indicates that the process requires a handle to the credentials of the user under whose [*security context*](../secgloss/s-gly.md) it is executing.</span></span>

 

</dd> <dt>

<span data-ttu-id="1968a-114">*псзпаккаже* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1968a-114">*pszPackage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1968a-115">Указатель на строку, завершающуюся нулем, которая указывает имя [*пакета безопасности*](../secgloss/s-gly.md) , с помощью которого будут использоваться эти учетные данные.</span><span class="sxs-lookup"><span data-stu-id="1968a-115">A pointer to a null-terminated string that specifies the name of the [*security package*](../secgloss/s-gly.md) with which these credentials will be used.</span></span> <span data-ttu-id="1968a-116">Это имя [*пакета безопасности*](../secgloss/s-gly.md) , возвращаемое в члене **Name** структуры [**Секпкгинфо**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) , возвращаемой функцией [**енумератесекуритипаккажес**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) .</span><span class="sxs-lookup"><span data-stu-id="1968a-116">This is a [*security package*](../secgloss/s-gly.md) name returned in the **Name** member of a [**SecPkgInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) structure returned by the [**EnumerateSecurityPackages**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) function.</span></span> <span data-ttu-id="1968a-117">После установки контекста [**QueryContextAttributes (Negotiate)**](querycontextattributes--negotiate.md) может быть вызван с параметром *улаттрибуте* , имеющим значение SECPKG \_ attr \_ , \_ для возврата информации о используемом [*пакете безопасности*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="1968a-117">After a context is established, [**QueryContextAttributes (Negotiate)**](querycontextattributes--negotiate.md) can be called with *ulAttribute* set to SECPKG\_ATTR\_PACKAGE\_INFO to return information on the [*security package*](../secgloss/s-gly.md) in use.</span></span>

<span data-ttu-id="1968a-118">Чтобы успешно вызвать эту функцию с помощью поставщика общих служб Negotiate, установите для этого параметра значение "Negotiate".</span><span class="sxs-lookup"><span data-stu-id="1968a-118">To successfully call this function using the Negotiate SSP, set this parameter to "Negotiate".</span></span>

</dd> <dt>

<span data-ttu-id="1968a-119">*фкредентиалусе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1968a-119">*fCredentialUse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1968a-120">Флаг, указывающий, как будут использоваться эти учетные данные.</span><span class="sxs-lookup"><span data-stu-id="1968a-120">A flag that indicates how these credentials will be used.</span></span> <span data-ttu-id="1968a-121">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="1968a-121">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="1968a-122">Значение</span><span class="sxs-lookup"><span data-stu-id="1968a-122">Value</span></span>                                                                                                                                                                                                                                                                                    | <span data-ttu-id="1968a-123">Значение</span><span class="sxs-lookup"><span data-stu-id="1968a-123">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SECPKG_CRED_AUTOLOGON_RESTRICTED"></span><span id="secpkg_cred_autologon_restricted"></span><dl> <span data-ttu-id="1968a-124"><dt>**SECPKG \_ Режим \_ автоматического входа в систему с \_ ограничением**</dt> <dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="1968a-124"><dt>**SECPKG\_CRED\_AUTOLOGON\_RESTRICTED**</dt> <dt>0x00000010</dt></span></span> </dl> | <span data-ttu-id="1968a-125">В системе безопасности не используются учетные данные или учетные данные для входа по умолчанию из [диспетчера учетных данных](credential-manager.md).</span><span class="sxs-lookup"><span data-stu-id="1968a-125">The security does not use default logon credentials or credentials from [Credential Manager](credential-manager.md).</span></span><br/> <span data-ttu-id="1968a-126">Windows **server 2008, Windows Vista, Windows server 2003 и Windows XP:** Это значение не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="1968a-126">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This value is not supported.</span></span><br/>                                                                                                                                                                                                                    |
| <span id="SECPKG_CRED_BOTH"></span><span id="secpkg_cred_both"></span><dl> <span data-ttu-id="1968a-127"><dt>**SECPKG \_ cred \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1968a-127"><dt>**SECPKG\_CRED\_BOTH**</dt></span></span> </dl>                                                                                                                  | <span data-ttu-id="1968a-128">Проверка входящих учетных данных или использование локальных учетных данных для подготовки исходящего маркера.</span><span class="sxs-lookup"><span data-stu-id="1968a-128">Validate an incoming credential or use a local credential to prepare an outgoing token.</span></span> <span data-ttu-id="1968a-129">Этот флаг включает и другие флаги.</span><span class="sxs-lookup"><span data-stu-id="1968a-129">This flag enables both other flags.</span></span><br/>                                                                                                                                                                                                                                                                                                                                  |
| <span id="SECPKG_CRED_INBOUND"></span><span id="secpkg_cred_inbound"></span><dl> <span data-ttu-id="1968a-130"><dt>**SECPKG \_ cred \_ Inbound**</dt></span><span class="sxs-lookup"><span data-stu-id="1968a-130"><dt>**SECPKG\_CRED\_INBOUND**</dt></span></span> </dl>                                                                                                         | <span data-ttu-id="1968a-131">Проверка учетных данных входящего сервера.</span><span class="sxs-lookup"><span data-stu-id="1968a-131">Validate an incoming server credential.</span></span> <span data-ttu-id="1968a-132">Входящие учетные данные могут быть проверены с помощью центра проверки подлинности при вызове [**InitializeSecurityContext (Negotiate)**](initializesecuritycontext--negotiate.md) или [**AcceptSecurityContext (Negotiate)**](acceptsecuritycontext--negotiate.md) .</span><span class="sxs-lookup"><span data-stu-id="1968a-132">Inbound credentials might be validated by using an authenticating authority when [**InitializeSecurityContext (Negotiate)**](initializesecuritycontext--negotiate.md) or [**AcceptSecurityContext (Negotiate)**](acceptsecuritycontext--negotiate.md) is called.</span></span> <span data-ttu-id="1968a-133">Если такой центр недоступен, функция завершится ошибкой и возвратит значение, равное, \_ \_ без \_ центра проверки подлинности \_ .</span><span class="sxs-lookup"><span data-stu-id="1968a-133">If such an authority is not available, the function will fail and return SEC\_E\_NO\_AUTHENTICATING\_AUTHORITY.</span></span> <span data-ttu-id="1968a-134">Проверка зависит от пакета.</span><span class="sxs-lookup"><span data-stu-id="1968a-134">Validation is package specific.</span></span><br/> |
| <span id="SECPKG_CRED_OUTBOUND"></span><span id="secpkg_cred_outbound"></span><dl> <span data-ttu-id="1968a-135"><dt>**исходящий SECPKG \_ cred \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1968a-135"><dt>**SECPKG\_CRED\_OUTBOUND**</dt></span></span> </dl>                                                                                                      | <span data-ttu-id="1968a-136">Разрешение учетных данных локального клиента для подготовки исходящего маркера.</span><span class="sxs-lookup"><span data-stu-id="1968a-136">Allow a local client credential to prepare an outgoing token.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="SECPKG_CRED_PROCESS_POLICY_ONLY"></span><span id="secpkg_cred_process_policy_only"></span><dl> <span data-ttu-id="1968a-137"><dt>**SECPKG \_ \_ \_ \_ Только политика процесса CRED**</dt> , <dt>0x00000020</dt></span><span class="sxs-lookup"><span data-stu-id="1968a-137"><dt>**SECPKG\_CRED\_PROCESS\_POLICY\_ONLY**</dt> <dt>0x00000020</dt></span></span> </dl>   | <span data-ttu-id="1968a-138">Функция обрабатывает политику сервера и возвращает данные в секунду, т. **\_ е. \_ не имеет \_ учетных данных**, указывая, что приложение должно запрашивать учетные данные.</span><span class="sxs-lookup"><span data-stu-id="1968a-138">The function processes server policy and returns **SEC\_E\_NO\_CREDENTIALS**, indicating that the application should prompt for credentials.</span></span><br/> <span data-ttu-id="1968a-139">Windows **server 2008, Windows Vista, Windows server 2003 и Windows XP:** Это значение не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="1968a-139">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This value is not supported.</span></span><br/>                                                                                                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="1968a-140">*пвлогонид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1968a-140">*pvLogonID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1968a-141">Указатель на [*локально уникальный идентификатор*](../secgloss/l-gly.md) (LUID), определяющий пользователя.</span><span class="sxs-lookup"><span data-stu-id="1968a-141">A pointer to a [*locally unique identifier*](../secgloss/l-gly.md) (LUID) that identifies the user.</span></span> <span data-ttu-id="1968a-142">Этот параметр предоставляется для процессов файловой системы, таких как сетевые перенаправления.</span><span class="sxs-lookup"><span data-stu-id="1968a-142">This parameter is provided for file-system processes such as network redirectors.</span></span> <span data-ttu-id="1968a-143">Этот параметр может принимать значение **NULL**.</span><span class="sxs-lookup"><span data-stu-id="1968a-143">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1968a-144">*паусдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1968a-144">*pAuthData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1968a-145">Указатель на данные, зависящие от пакета.</span><span class="sxs-lookup"><span data-stu-id="1968a-145">A pointer to package-specific data.</span></span> <span data-ttu-id="1968a-146">Этот параметр может иметь **значение NULL**, что означает, что необходимо использовать учетные данные по умолчанию для этого [*пакета безопасности*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="1968a-146">This parameter can be **NULL**, which indicates that the default credentials for that [*security package*](../secgloss/s-gly.md) must be used.</span></span> <span data-ttu-id="1968a-147">Чтобы использовать предоставленные учетные данные, передайте **\_ \_ \_ \_ непрозрачную структуру псек WinNT auth Identity** , возвращенную из предыдущего вызова функции [**сспипромптфоркредентиалс**](/windows/win32/api/sspi/nf-sspi-sspipromptforcredentialsa) .</span><span class="sxs-lookup"><span data-stu-id="1968a-147">To use supplied credentials, pass a **PSEC\_WINNT\_AUTH\_IDENTITY\_OPAQUE** structure returned from a previous call to the [**SspiPromptForCredentials**](/windows/win32/api/sspi/nf-sspi-sspipromptforcredentialsa) function.</span></span>

<span data-ttu-id="1968a-148">Windows **server 2008, Windows Vista, Windows server 2003 и Windows XP:** Непрозрачный тип **\_ \_ \_ удостоверения проверки \_ подлинности псек WinNT** и функция [**сспипромптфоркредентиалс**](/windows/win32/api/sspi/nf-sspi-sspipromptforcredentialsa) не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="1968a-148">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** The **PSEC\_WINNT\_AUTH\_IDENTITY\_OPAQUE** type and the [**SspiPromptForCredentials**](/windows/win32/api/sspi/nf-sspi-sspipromptforcredentialsa) function are not supported.</span></span> <span data-ttu-id="1968a-149">Чтобы использовать предоставленные учетные данные, передайте указатель [**на \_ \_ \_ идентификатор проверки подлинности WinNT**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) или с помощью [**\_ команды Winnt \_ AUTH \_ Identity \_ ex**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_ex2) , включающей эти учетные данные.</span><span class="sxs-lookup"><span data-stu-id="1968a-149">To use supplied credentials, pass a pointer to either a [**SEC\_WINNT\_AUTH\_IDENTITY**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) or [**SEC\_WINNT\_AUTH\_IDENTITY\_EX**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_ex2) structure that includes those credentials.</span></span>

<span data-ttu-id="1968a-150">Время выполнения RPC передает все, что было указано в [**рпкбиндингсетаусинфо**](/windows/win32/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo).</span><span class="sxs-lookup"><span data-stu-id="1968a-150">The RPC run time passes whatever was provided in [**RpcBindingSetAuthInfo**](/windows/win32/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo).</span></span>

<span data-ttu-id="1968a-151">При использовании пакета Negotiate максимальная длина символов для имени пользователя, пароля и домена составляет 256, 256 и 15 соответственно.</span><span class="sxs-lookup"><span data-stu-id="1968a-151">When using the Negotiate package, the maximum character lengths for user name, password, and domain are 256, 256, and 15, respectively.</span></span>

</dd> <dt>

<span data-ttu-id="1968a-152">*пжеткэйфн* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1968a-152">*pGetKeyFn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1968a-153">Этот параметр не используется и должен иметь значение **null**.</span><span class="sxs-lookup"><span data-stu-id="1968a-153">This parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1968a-154">*пвжеткэйаргумент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1968a-154">*pvGetKeyArgument* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1968a-155">Этот параметр не используется и должен иметь значение **null**.</span><span class="sxs-lookup"><span data-stu-id="1968a-155">This parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1968a-156">*фкредентиал* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="1968a-156">*phCredential* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1968a-157">Указатель на структуру [кредхандле](sspi-handles.md) для получения маркера учетных данных.</span><span class="sxs-lookup"><span data-stu-id="1968a-157">A pointer to a [CredHandle](sspi-handles.md) structure to receive the credential handle.</span></span>

</dd> <dt>

<span data-ttu-id="1968a-158">*птсекспири* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="1968a-158">*ptsExpiry* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1968a-159">Указатель на структуру [**метки времени**](timestamp.md) , которая получает время истечения срока действия возвращенных учетных данных.</span><span class="sxs-lookup"><span data-stu-id="1968a-159">A pointer to a [**TimeStamp**](timestamp.md) structure that receives the time at which the returned credentials expire.</span></span> <span data-ttu-id="1968a-160">Значение, возвращаемое этой структурой **отметок времени** , зависит от [*ограниченного делегирования*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="1968a-160">The value returned in this **TimeStamp** structure depends on the [*constrained delegation*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="1968a-161">[*Пакет безопасности*](../secgloss/s-gly.md) должен вернуть это значение в местное время.</span><span class="sxs-lookup"><span data-stu-id="1968a-161">The [*security package*](../secgloss/s-gly.md) must return this value in local time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1968a-162">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1968a-162">Return value</span></span>

<span data-ttu-id="1968a-163">Если функция завершается успешно, функция возвращает значение секунды \_ E \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="1968a-163">If the function succeeds, the function returns SEC\_E\_OK.</span></span>

<span data-ttu-id="1968a-164">Если функция завершается ошибкой, возвращается один из следующих кодов ошибок.</span><span class="sxs-lookup"><span data-stu-id="1968a-164">If the function fails, it returns one of the following error codes.</span></span>



| <span data-ttu-id="1968a-165">Код возврата</span><span class="sxs-lookup"><span data-stu-id="1968a-165">Return code</span></span>                                                                                                 | <span data-ttu-id="1968a-166">Описание</span><span class="sxs-lookup"><span data-stu-id="1968a-166">Description</span></span>                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1968a-167"><dt>**СЕК \_ . \_ недостаточный \_ объем памяти**</dt></span><span class="sxs-lookup"><span data-stu-id="1968a-167"><dt>**SEC\_E\_INSUFFICIENT\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="1968a-168">Недостаточно доступной памяти для завершения запрошенного действия.</span><span class="sxs-lookup"><span data-stu-id="1968a-168">There is not enough memory available to complete the requested action.</span></span><br/>                                                                  |
| <dl> <span data-ttu-id="1968a-169"><dt>**\_ \_ Внутренняя ошибка E \_ sec**</dt></span><span class="sxs-lookup"><span data-stu-id="1968a-169"><dt>**SEC\_E\_INTERNAL\_ERROR**</dt></span></span> </dl>      | <span data-ttu-id="1968a-170">Произошла ошибка, которая не сопоставлена с кодом ошибки SSPI.</span><span class="sxs-lookup"><span data-stu-id="1968a-170">An error occurred that did not map to an SSPI error code.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="1968a-171"><dt>**с \_ \_ без \_ учетных данных**</dt></span><span class="sxs-lookup"><span data-stu-id="1968a-171"><dt>**SEC\_E\_NO\_CREDENTIALS**</dt></span></span> </dl>      | <span data-ttu-id="1968a-172">Учетные данные недоступны в [*ограниченном делегировании*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="1968a-172">No credentials are available in the [*constrained delegation*](../secgloss/s-gly.md).</span></span><br/> |
| <dl> <span data-ttu-id="1968a-173"><dt>**СЕК. \_ е. \_ не \_ владелец**</dt></span><span class="sxs-lookup"><span data-stu-id="1968a-173"><dt>**SEC\_E\_NOT\_OWNER**</dt></span></span> </dl>           | <span data-ttu-id="1968a-174">Вызывающий объект функции не имеет необходимых учетных данных.</span><span class="sxs-lookup"><span data-stu-id="1968a-174">The caller of the function does not have the necessary credentials.</span></span><br/>                                                                     |
| <dl> <span data-ttu-id="1968a-175"><dt>**с \_ е \_ SECPKG \_ не \_ Найдено**</dt></span><span class="sxs-lookup"><span data-stu-id="1968a-175"><dt>**SEC\_E\_SECPKG\_NOT\_FOUND**</dt></span></span> </dl>   | <span data-ttu-id="1968a-176">Запрошенный [*пакет безопасности*](../secgloss/s-gly.md) не существует.</span><span class="sxs-lookup"><span data-stu-id="1968a-176">The requested [*security package*](../secgloss/s-gly.md) does not exist.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="1968a-177"><dt>**с \_ е \_ неизвестные \_ учетные данные**</dt></span><span class="sxs-lookup"><span data-stu-id="1968a-177"><dt>**SEC\_E\_UNKNOWN\_CREDENTIALS**</dt></span></span> </dl> | <span data-ttu-id="1968a-178">Учетные данные, предоставленные пакету, не распознаны.</span><span class="sxs-lookup"><span data-stu-id="1968a-178">The credentials supplied to the package were not recognized.</span></span><br/>                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="1968a-179">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1968a-179">Remarks</span></span>

<span data-ttu-id="1968a-180">Функция **AcquireCredentialsHandle (Negotiate)** возвращает маркер учетных данных участника, например пользователя или клиента, который используется конкретным [*ограниченным делегированием*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="1968a-180">The **AcquireCredentialsHandle (Negotiate)** function returns a handle to the credentials of a principal, such as a user or client, as used by a specific [*constrained delegation*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="1968a-181">Это может быть обработчик существующих учетных данных, или функция может создать новый набор учетных данных и вернуть их.</span><span class="sxs-lookup"><span data-stu-id="1968a-181">This can be the handle to preexisting credentials, or the function can create a new set of credentials and return it.</span></span> <span data-ttu-id="1968a-182">Этот маркер можно использовать при последующих вызовах функций [**AcceptSecurityContext (Negotiate)**](acceptsecuritycontext--negotiate.md) и [**InitializeSecurityContext (Negotiate)**](initializesecuritycontext--negotiate.md) .</span><span class="sxs-lookup"><span data-stu-id="1968a-182">This handle can be used in subsequent calls to the [**AcceptSecurityContext (Negotiate)**](acceptsecuritycontext--negotiate.md) and [**InitializeSecurityContext (Negotiate)**](initializesecuritycontext--negotiate.md) functions.</span></span>

<span data-ttu-id="1968a-183">В общем случае **AcquireCredentialsHandle (Negotiate)** не позволяет процессу получить маркер учетных данных других пользователей, выполнивших вход на тот же компьютер.</span><span class="sxs-lookup"><span data-stu-id="1968a-183">In general, **AcquireCredentialsHandle (Negotiate)** does not allow a process to obtain a handle to the credentials of other users logged on to the same computer.</span></span> <span data-ttu-id="1968a-184">Однако у вызывающего \_ \_ [*право доступа*](../secgloss/s-gly.md) к имени TCB есть возможность указать [*идентификатор входа*](../secgloss/l-gly.md) (LUID) любого существующего маркера сеанса входа, чтобы получить маркер для учетных данных этого сеанса.</span><span class="sxs-lookup"><span data-stu-id="1968a-184">However, a caller with SE\_TCB\_NAME [*privilege*](../secgloss/s-gly.md) has the option of specifying the [*logon identifier*](../secgloss/l-gly.md) (LUID) of any existing logon session token to get a handle to that session's credentials.</span></span> <span data-ttu-id="1968a-185">Обычно это используется модулями режима ядра, которые должны действовать от имени вошедшего в систему пользователя.</span><span class="sxs-lookup"><span data-stu-id="1968a-185">Typically, this is used by kernel-mode modules that must act on behalf of a logged-on user.</span></span>

<span data-ttu-id="1968a-186">Пакет может вызвать функцию в *пжеткэйфн* , предоставляемую транспортом времени выполнения RPC.</span><span class="sxs-lookup"><span data-stu-id="1968a-186">A package might call the function in *pGetKeyFn* provided by the RPC run-time transport.</span></span> <span data-ttu-id="1968a-187">Если транспорт не поддерживает понятие обратного вызова для получения учетных данных, этот параметр должен иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="1968a-187">If the transport does not support the notion of callback to retrieve credentials, this parameter must be **NULL**.</span></span>

<span data-ttu-id="1968a-188">Для вызывающих объектов в режиме ядра необходимо отметить следующие отличия.</span><span class="sxs-lookup"><span data-stu-id="1968a-188">For kernel mode callers, the following differences must be noted:</span></span>

-   <span data-ttu-id="1968a-189">Два строковых параметра должны быть строками в [*Юникоде*](../secgloss/u-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="1968a-189">The two string parameters must be [*Unicode*](../secgloss/u-gly.md) strings.</span></span>
-   <span data-ttu-id="1968a-190">Значения буфера должны выделяться в виртуальной памяти процесса, а не в пуле.</span><span class="sxs-lookup"><span data-stu-id="1968a-190">The buffer values must be allocated in process virtual memory, not from the pool.</span></span>

<span data-ttu-id="1968a-191">По завершении использования возвращенных учетных данных освободите память, используемую учетными данными, вызвав функцию [**фрикредентиалшандле**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle) .</span><span class="sxs-lookup"><span data-stu-id="1968a-191">When you have finished using the returned credentials, free the memory used by the credentials by calling the [**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="1968a-192">Требования</span><span class="sxs-lookup"><span data-stu-id="1968a-192">Requirements</span></span>



| <span data-ttu-id="1968a-193">Требование</span><span class="sxs-lookup"><span data-stu-id="1968a-193">Requirement</span></span> | <span data-ttu-id="1968a-194">Значение</span><span class="sxs-lookup"><span data-stu-id="1968a-194">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1968a-195">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1968a-195">Minimum supported client</span></span><br/> | <span data-ttu-id="1968a-196">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="1968a-196">Windows XP \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="1968a-197">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1968a-197">Minimum supported server</span></span><br/> | <span data-ttu-id="1968a-198">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1968a-198">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="1968a-199">Header</span><span class="sxs-lookup"><span data-stu-id="1968a-199">Header</span></span><br/>                   | <dl> <span data-ttu-id="1968a-200"><dt>SSPI. h (включая Security. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1968a-200"><dt>Sspi.h (include Security.h)</dt></span></span> </dl> |
| <span data-ttu-id="1968a-201">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1968a-201">Library</span></span><br/>                  | <dl> <span data-ttu-id="1968a-202"><dt>Secur32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1968a-202"><dt>Secur32.lib</dt></span></span> </dl>                 |
| <span data-ttu-id="1968a-203">DLL</span><span class="sxs-lookup"><span data-stu-id="1968a-203">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1968a-204"><dt>Secur32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1968a-204"><dt>Secur32.dll</dt></span></span> </dl>                 |
| <span data-ttu-id="1968a-205">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="1968a-205">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="1968a-206">**Аккуирекредентиалшандлев** (Юникод) и **аккуирекредентиалшандлеа** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="1968a-206">**AcquireCredentialsHandleW** (Unicode) and **AcquireCredentialsHandleA** (ANSI)</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="1968a-207">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1968a-207">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1968a-208">Функции SSPI</span><span class="sxs-lookup"><span data-stu-id="1968a-208">SSPI Functions</span></span>](authentication-functions.md#sspi-functions)
</dt> <dt>

[<span data-ttu-id="1968a-209">**AcceptSecurityContext (согласование)**</span><span class="sxs-lookup"><span data-stu-id="1968a-209">**AcceptSecurityContext (Negotiate)**</span></span>](acceptsecuritycontext--negotiate.md)
</dt> <dt>

[<span data-ttu-id="1968a-210">**InitializeSecurityContext (согласование)**</span><span class="sxs-lookup"><span data-stu-id="1968a-210">**InitializeSecurityContext (Negotiate)**</span></span>](initializesecuritycontext--negotiate.md)
</dt> <dt>

[<span data-ttu-id="1968a-211">**фрикредентиалшандле**</span><span class="sxs-lookup"><span data-stu-id="1968a-211">**FreeCredentialsHandle**</span></span>](/windows/win32/api/sspi/nf-sspi-freecredentialshandle)
</dt> </dl>

 

 
