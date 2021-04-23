---
description: Получает маркер для существующих учетных данных субъекта безопасности, использующего NTLM.
ms.assetid: 8a51ca50-0e05-4f1e-9dfc-c5d0118f65ed
title: Функция AcquireCredentialsHandle (NTLM) (SSPI. h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 233bfd57c6e3a7471d7c26204157cd1451d7884f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265941"
---
# <a name="acquirecredentialshandle-ntlm-function"></a><span data-ttu-id="fa935-103">Функция AcquireCredentialsHandle (NTLM)</span><span class="sxs-lookup"><span data-stu-id="fa935-103">AcquireCredentialsHandle (NTLM) function</span></span>

<span data-ttu-id="fa935-104">Функция **AcquireCredentialsHandle (NTLM)** получает маркер для существующих учетных данных [*субъекта безопасности*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="fa935-104">The **AcquireCredentialsHandle (NTLM)** function acquires a handle to preexisting credentials of a [*security principal*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="fa935-105">Этот обработчик необходим для функций [**InitializeSecurityContext (NTLM)**](initializesecuritycontext--ntlm.md) и [**AcceptSecurityContext (NTLM)**](acceptsecuritycontext--ntlm.md) .</span><span class="sxs-lookup"><span data-stu-id="fa935-105">This handle is required by the [**InitializeSecurityContext (NTLM)**](initializesecuritycontext--ntlm.md) and [**AcceptSecurityContext (NTLM)**](acceptsecuritycontext--ntlm.md) functions.</span></span> <span data-ttu-id="fa935-106">Это могут быть либо существовавшие ранее *учетные данные*, которые устанавливаются с помощью системного входа, не описываемого здесь, либо вызывающая сторона может предоставить альтернативные учетные данные.</span><span class="sxs-lookup"><span data-stu-id="fa935-106">These can be either preexisting *credentials*, which are established through a system logon that is not described here, or the caller can provide alternative credentials.</span></span>

> [!Note]  
> <span data-ttu-id="fa935-107">Это не «вход в сеть» и не предполагает сбор учетных данных.</span><span class="sxs-lookup"><span data-stu-id="fa935-107">This is not a "log on to the network" and does not imply gathering of credentials.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="fa935-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fa935-108">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="fa935-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="fa935-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa935-110">*псзпринЦипал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fa935-110">*pszPrincipal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa935-111">Указатель на строку, завершающуюся нулем, которая указывает имя участника, учетные данные которого будут ссылаться на этот обработчик.</span><span class="sxs-lookup"><span data-stu-id="fa935-111">A pointer to a null-terminated string that specifies the name of the principal whose credentials the handle will reference.</span></span>

> [!Note]  
> <span data-ttu-id="fa935-112">Если процесс, запрашивающий этот обработчик, не имеет доступа к учетным данным, функция возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="fa935-112">If the process that requests the handle does not have access to the credentials, the function returns an error.</span></span> <span data-ttu-id="fa935-113">Строка NULL указывает, что процессу требуется маркер для учетных данных пользователя, от имени которого выполняется [*контекст безопасности*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="fa935-113">A null string indicates that the process requires a handle to the credentials of the user under whose [*security context*](../secgloss/s-gly.md) it is executing.</span></span>

 

</dd> <dt>

<span data-ttu-id="fa935-114">*псзпаккаже* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fa935-114">*pszPackage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa935-115">Указатель на строку, завершающуюся нулем, которая указывает имя [*пакета безопасности*](../secgloss/s-gly.md) , с помощью которого будут использоваться эти учетные данные.</span><span class="sxs-lookup"><span data-stu-id="fa935-115">A pointer to a null-terminated string that specifies the name of the [*security package*](../secgloss/s-gly.md) with which these credentials will be used.</span></span> <span data-ttu-id="fa935-116">Это имя [*пакета безопасности*](../secgloss/s-gly.md) , возвращаемое в члене **Name** структуры [**Секпкгинфо**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) , возвращаемой функцией [**енумератесекуритипаккажес**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) .</span><span class="sxs-lookup"><span data-stu-id="fa935-116">This is a [*security package*](../secgloss/s-gly.md) name returned in the **Name** member of a [**SecPkgInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) structure returned by the [**EnumerateSecurityPackages**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) function.</span></span> <span data-ttu-id="fa935-117">После установки контекста [**QueryContextAttributes (NTLM)**](querycontextattributes--ntlm.md) можно вызвать с параметром *улаттрибуте* , для которого задано значение SECPKG \_ attr, \_ \_ чтобы вернуть сведения о используемом [*пакете безопасности*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="fa935-117">After a context is established, [**QueryContextAttributes (NTLM)**](querycontextattributes--ntlm.md) can be called with *ulAttribute* set to SECPKG\_ATTR\_PACKAGE\_INFO to return information on the [*security package*](../secgloss/s-gly.md) in use.</span></span>

</dd> <dt>

<span data-ttu-id="fa935-118">*фкредентиалусе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fa935-118">*fCredentialUse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa935-119">Флаг, указывающий, как будут использоваться эти учетные данные.</span><span class="sxs-lookup"><span data-stu-id="fa935-119">A flag that indicates how these credentials will be used.</span></span> <span data-ttu-id="fa935-120">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="fa935-120">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="fa935-121">Значение</span><span class="sxs-lookup"><span data-stu-id="fa935-121">Value</span></span>                                                                                                                                                                               | <span data-ttu-id="fa935-122">Значение</span><span class="sxs-lookup"><span data-stu-id="fa935-122">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SECPKG_CRED_BOTH"></span><span id="secpkg_cred_both"></span><dl> <span data-ttu-id="fa935-123"><dt>**SECPKG \_ cred \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fa935-123"><dt>**SECPKG\_CRED\_BOTH**</dt></span></span> </dl>             | <span data-ttu-id="fa935-124">Проверка входящих учетных данных или использование локальных учетных данных для подготовки исходящего маркера.</span><span class="sxs-lookup"><span data-stu-id="fa935-124">Validate an incoming credential or use a local credential to prepare an outgoing token.</span></span> <span data-ttu-id="fa935-125">Этот флаг включает и другие флаги.</span><span class="sxs-lookup"><span data-stu-id="fa935-125">This flag enables both other flags.</span></span><br/>                                                                                                                                                                                                                                                                                                              |
| <span id="SECPKG_CRED_INBOUND"></span><span id="secpkg_cred_inbound"></span><dl> <span data-ttu-id="fa935-126"><dt>**SECPKG \_ cred \_ Inbound**</dt></span><span class="sxs-lookup"><span data-stu-id="fa935-126"><dt>**SECPKG\_CRED\_INBOUND**</dt></span></span> </dl>    | <span data-ttu-id="fa935-127">Проверка учетных данных входящего сервера.</span><span class="sxs-lookup"><span data-stu-id="fa935-127">Validate an incoming server credential.</span></span> <span data-ttu-id="fa935-128">Входящие учетные данные могут быть проверены с помощью центра проверки подлинности при вызове [**InitializeSecurityContext (NTLM)**](initializesecuritycontext--ntlm.md) или [**AcceptSecurityContext (NTLM)**](acceptsecuritycontext--ntlm.md) .</span><span class="sxs-lookup"><span data-stu-id="fa935-128">Inbound credentials might be validated by using an authenticating authority when [**InitializeSecurityContext (NTLM)**](initializesecuritycontext--ntlm.md) or [**AcceptSecurityContext (NTLM)**](acceptsecuritycontext--ntlm.md) is called.</span></span> <span data-ttu-id="fa935-129">Если такой центр недоступен, функция завершится ошибкой и возвратит значение, равное, \_ \_ без \_ центра проверки подлинности \_ .</span><span class="sxs-lookup"><span data-stu-id="fa935-129">If such an authority is not available, the function will fail and return SEC\_E\_NO\_AUTHENTICATING\_AUTHORITY.</span></span> <span data-ttu-id="fa935-130">Проверка зависит от пакета.</span><span class="sxs-lookup"><span data-stu-id="fa935-130">Validation is package specific.</span></span><br/> |
| <span id="SECPKG_CRED_OUTBOUND"></span><span id="secpkg_cred_outbound"></span><dl> <span data-ttu-id="fa935-131"><dt>**исходящий SECPKG \_ cred \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fa935-131"><dt>**SECPKG\_CRED\_OUTBOUND**</dt></span></span> </dl> | <span data-ttu-id="fa935-132">Разрешение учетных данных локального клиента для подготовки исходящего маркера.</span><span class="sxs-lookup"><span data-stu-id="fa935-132">Allow a local client credential to prepare an outgoing token.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="fa935-133">*пвлогонид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fa935-133">*pvLogonID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa935-134">Указатель на [*локально уникальный идентификатор*](../secgloss/l-gly.md) (LUID), определяющий пользователя.</span><span class="sxs-lookup"><span data-stu-id="fa935-134">A pointer to a [*locally unique identifier*](../secgloss/l-gly.md) (LUID) that identifies the user.</span></span> <span data-ttu-id="fa935-135">Этот параметр предоставляется для процессов файловой системы, таких как сетевые перенаправления.</span><span class="sxs-lookup"><span data-stu-id="fa935-135">This parameter is provided for file-system processes such as network redirectors.</span></span> <span data-ttu-id="fa935-136">Этот параметр может принимать значение **NULL**.</span><span class="sxs-lookup"><span data-stu-id="fa935-136">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="fa935-137">*паусдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fa935-137">*pAuthData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa935-138">Указатель на данные, зависящие от пакета.</span><span class="sxs-lookup"><span data-stu-id="fa935-138">A pointer to package-specific data.</span></span> <span data-ttu-id="fa935-139">Этот параметр может иметь **значение NULL**, что означает, что необходимо использовать учетные данные по умолчанию для этого [*пакета безопасности*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="fa935-139">This parameter can be **NULL**, which indicates that the default credentials for that [*security package*](../secgloss/s-gly.md) must be used.</span></span> <span data-ttu-id="fa935-140">Чтобы использовать предоставленные учетные данные, передайте в этом параметре структуру [**\_ \_ \_ удостоверений проверки подлинности WinNT (с**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) ).</span><span class="sxs-lookup"><span data-stu-id="fa935-140">To use supplied credentials, pass a [**SEC\_WINNT\_AUTH\_IDENTITY**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) structure that includes those credentials in this parameter.</span></span> <span data-ttu-id="fa935-141">Время выполнения RPC передает все, что было указано в [**рпкбиндингсетаусинфо**](/windows/win32/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo).</span><span class="sxs-lookup"><span data-stu-id="fa935-141">The RPC run time passes whatever was provided in [**RpcBindingSetAuthInfo**](/windows/win32/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo).</span></span>

<span data-ttu-id="fa935-142">При использовании пакета NTLM максимальная длина символов для имени пользователя, пароля и домена составляет 256, 256 и 15 соответственно.</span><span class="sxs-lookup"><span data-stu-id="fa935-142">When using the NTLM package, the maximum character lengths for user name, password, and domain are 256, 256, and 15, respectively.</span></span>

</dd> <dt>

<span data-ttu-id="fa935-143">*пжеткэйфн* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fa935-143">*pGetKeyFn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa935-144">Этот параметр не используется и должен иметь значение **null**.</span><span class="sxs-lookup"><span data-stu-id="fa935-144">This parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="fa935-145">*пвжеткэйаргумент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fa935-145">*pvGetKeyArgument* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa935-146">Этот параметр не используется и должен иметь значение **null**.</span><span class="sxs-lookup"><span data-stu-id="fa935-146">This parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="fa935-147">*фкредентиал* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="fa935-147">*phCredential* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fa935-148">Указатель на структуру [кредхандле](sspi-handles.md) для получения маркера учетных данных.</span><span class="sxs-lookup"><span data-stu-id="fa935-148">A pointer to a [CredHandle](sspi-handles.md) structure to receive the credential handle.</span></span>

</dd> <dt>

<span data-ttu-id="fa935-149">*птсекспири* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="fa935-149">*ptsExpiry* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fa935-150">Указатель на структуру [**метки времени**](timestamp.md) , которая получает время истечения срока действия возвращенных учетных данных.</span><span class="sxs-lookup"><span data-stu-id="fa935-150">A pointer to a [**TimeStamp**](timestamp.md) structure that receives the time at which the returned credentials expire.</span></span> <span data-ttu-id="fa935-151">Значение, возвращаемое этой структурой **отметок времени** , зависит от [*ограниченного делегирования*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="fa935-151">The value returned in this **TimeStamp** structure depends on the [*constrained delegation*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="fa935-152">[*Пакет безопасности*](../secgloss/s-gly.md) должен вернуть это значение в местное время.</span><span class="sxs-lookup"><span data-stu-id="fa935-152">The [*security package*](../secgloss/s-gly.md) must return this value in local time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa935-153">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fa935-153">Return value</span></span>

<span data-ttu-id="fa935-154">Если функция завершается успешно, функция возвращает значение секунды \_ E \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="fa935-154">If the function succeeds, the function returns SEC\_E\_OK.</span></span>

<span data-ttu-id="fa935-155">Если функция завершается ошибкой, возвращается один из следующих кодов ошибок.</span><span class="sxs-lookup"><span data-stu-id="fa935-155">If the function fails, it returns one of the following error codes.</span></span>



| <span data-ttu-id="fa935-156">Код возврата</span><span class="sxs-lookup"><span data-stu-id="fa935-156">Return code</span></span>                                                                                                 | <span data-ttu-id="fa935-157">Описание</span><span class="sxs-lookup"><span data-stu-id="fa935-157">Description</span></span>                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fa935-158"><dt>**СЕК \_ . \_ недостаточный \_ объем памяти**</dt></span><span class="sxs-lookup"><span data-stu-id="fa935-158"><dt>**SEC\_E\_INSUFFICIENT\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="fa935-159">Недостаточно доступной памяти для завершения запрошенного действия.</span><span class="sxs-lookup"><span data-stu-id="fa935-159">There is not enough memory available to complete the requested action.</span></span><br/>                                                                  |
| <dl> <span data-ttu-id="fa935-160"><dt>**\_ \_ Внутренняя ошибка E \_ sec**</dt></span><span class="sxs-lookup"><span data-stu-id="fa935-160"><dt>**SEC\_E\_INTERNAL\_ERROR**</dt></span></span> </dl>      | <span data-ttu-id="fa935-161">Произошла ошибка, которая не сопоставлена с кодом ошибки SSPI.</span><span class="sxs-lookup"><span data-stu-id="fa935-161">An error occurred that did not map to an SSPI error code.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="fa935-162"><dt>**с \_ \_ без \_ учетных данных**</dt></span><span class="sxs-lookup"><span data-stu-id="fa935-162"><dt>**SEC\_E\_NO\_CREDENTIALS**</dt></span></span> </dl>      | <span data-ttu-id="fa935-163">Учетные данные недоступны в [*ограниченном делегировании*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="fa935-163">No credentials are available in the [*constrained delegation*](../secgloss/s-gly.md).</span></span><br/> |
| <dl> <span data-ttu-id="fa935-164"><dt>**СЕК. \_ е. \_ не \_ владелец**</dt></span><span class="sxs-lookup"><span data-stu-id="fa935-164"><dt>**SEC\_E\_NOT\_OWNER**</dt></span></span> </dl>           | <span data-ttu-id="fa935-165">Вызывающий объект функции не имеет необходимых учетных данных.</span><span class="sxs-lookup"><span data-stu-id="fa935-165">The caller of the function does not have the necessary credentials.</span></span><br/>                                                                     |
| <dl> <span data-ttu-id="fa935-166"><dt>**с \_ е \_ SECPKG \_ не \_ Найдено**</dt></span><span class="sxs-lookup"><span data-stu-id="fa935-166"><dt>**SEC\_E\_SECPKG\_NOT\_FOUND**</dt></span></span> </dl>   | <span data-ttu-id="fa935-167">Запрошенный [*пакет безопасности*](../secgloss/s-gly.md) не существует.</span><span class="sxs-lookup"><span data-stu-id="fa935-167">The requested [*security package*](../secgloss/s-gly.md) does not exist.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="fa935-168"><dt>**с \_ е \_ неизвестные \_ учетные данные**</dt></span><span class="sxs-lookup"><span data-stu-id="fa935-168"><dt>**SEC\_E\_UNKNOWN\_CREDENTIALS**</dt></span></span> </dl> | <span data-ttu-id="fa935-169">Учетные данные, предоставленные пакету, не распознаны.</span><span class="sxs-lookup"><span data-stu-id="fa935-169">The credentials supplied to the package were not recognized.</span></span><br/>                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="fa935-170">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fa935-170">Remarks</span></span>

<span data-ttu-id="fa935-171">Функция **AcquireCredentialsHandle (NTLM)** возвращает маркер учетных данных участника, например пользователя или клиента, который используется конкретным [*ограниченным делегированием*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="fa935-171">The **AcquireCredentialsHandle (NTLM)** function returns a handle to the credentials of a principal, such as a user or client, as used by a specific [*constrained delegation*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="fa935-172">Это может быть обработчик существующих учетных данных, или функция может создать новый набор учетных данных и вернуть их.</span><span class="sxs-lookup"><span data-stu-id="fa935-172">This can be the handle to preexisting credentials, or the function can create a new set of credentials and return it.</span></span> <span data-ttu-id="fa935-173">Этот маркер можно использовать при последующих вызовах функций [**AcceptSecurityContext (NTLM)**](acceptsecuritycontext--ntlm.md) и [**InitializeSecurityContext (NTLM)**](initializesecuritycontext--ntlm.md) .</span><span class="sxs-lookup"><span data-stu-id="fa935-173">This handle can be used in subsequent calls to the [**AcceptSecurityContext (NTLM)**](acceptsecuritycontext--ntlm.md) and [**InitializeSecurityContext (NTLM)**](initializesecuritycontext--ntlm.md) functions.</span></span>

<span data-ttu-id="fa935-174">В общем случае **AcquireCredentialsHandle (NTLM)** не позволяет процессу получить маркер учетных данных других пользователей, выполнивших вход на тот же компьютер.</span><span class="sxs-lookup"><span data-stu-id="fa935-174">In general, **AcquireCredentialsHandle (NTLM)** does not allow a process to obtain a handle to the credentials of other users logged on to the same computer.</span></span> <span data-ttu-id="fa935-175">Однако у вызывающего \_ \_ [*право доступа*](../secgloss/s-gly.md) к имени TCB есть возможность указать [*идентификатор входа*](../secgloss/l-gly.md) (LUID) любого существующего маркера сеанса входа, чтобы получить маркер для учетных данных этого сеанса.</span><span class="sxs-lookup"><span data-stu-id="fa935-175">However, a caller with SE\_TCB\_NAME [*privilege*](../secgloss/s-gly.md) has the option of specifying the [*logon identifier*](../secgloss/l-gly.md) (LUID) of any existing logon session token to get a handle to that session's credentials.</span></span> <span data-ttu-id="fa935-176">Обычно это используется модулями режима ядра, которые должны действовать от имени вошедшего в систему пользователя.</span><span class="sxs-lookup"><span data-stu-id="fa935-176">Typically, this is used by kernel-mode modules that must act on behalf of a logged-on user.</span></span>

<span data-ttu-id="fa935-177">Пакет может вызвать функцию в *пжеткэйфн* , предоставляемую транспортом времени выполнения RPC.</span><span class="sxs-lookup"><span data-stu-id="fa935-177">A package might call the function in *pGetKeyFn* provided by the RPC run-time transport.</span></span> <span data-ttu-id="fa935-178">Если транспорт не поддерживает понятие обратного вызова для получения учетных данных, этот параметр должен иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="fa935-178">If the transport does not support the notion of callback to retrieve credentials, this parameter must be **NULL**.</span></span>

<span data-ttu-id="fa935-179">Для вызывающих объектов в режиме ядра необходимо отметить следующие отличия.</span><span class="sxs-lookup"><span data-stu-id="fa935-179">For kernel mode callers, the following differences must be noted:</span></span>

-   <span data-ttu-id="fa935-180">Два строковых параметра должны быть строками в [*Юникоде*](../secgloss/u-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="fa935-180">The two string parameters must be [*Unicode*](../secgloss/u-gly.md) strings.</span></span>
-   <span data-ttu-id="fa935-181">Значения буфера должны выделяться в виртуальной памяти процесса, а не в пуле.</span><span class="sxs-lookup"><span data-stu-id="fa935-181">The buffer values must be allocated in process virtual memory, not from the pool.</span></span>

<span data-ttu-id="fa935-182">По завершении использования возвращенных учетных данных освободите память, используемую учетными данными, вызвав функцию [**фрикредентиалшандле**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle) .</span><span class="sxs-lookup"><span data-stu-id="fa935-182">When you have finished using the returned credentials, free the memory used by the credentials by calling the [**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa935-183">Требования</span><span class="sxs-lookup"><span data-stu-id="fa935-183">Requirements</span></span>



| <span data-ttu-id="fa935-184">Требование</span><span class="sxs-lookup"><span data-stu-id="fa935-184">Requirement</span></span> | <span data-ttu-id="fa935-185">Значение</span><span class="sxs-lookup"><span data-stu-id="fa935-185">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa935-186">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fa935-186">Minimum supported client</span></span><br/> | <span data-ttu-id="fa935-187">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="fa935-187">Windows XP \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="fa935-188">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fa935-188">Minimum supported server</span></span><br/> | <span data-ttu-id="fa935-189">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fa935-189">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="fa935-190">Header</span><span class="sxs-lookup"><span data-stu-id="fa935-190">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa935-191"><dt>SSPI. h (включая Security. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fa935-191"><dt>Sspi.h (include Security.h)</dt></span></span> </dl> |
| <span data-ttu-id="fa935-192">Библиотека</span><span class="sxs-lookup"><span data-stu-id="fa935-192">Library</span></span><br/>                  | <dl> <span data-ttu-id="fa935-193"><dt>Secur32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fa935-193"><dt>Secur32.lib</dt></span></span> </dl>                 |
| <span data-ttu-id="fa935-194">DLL</span><span class="sxs-lookup"><span data-stu-id="fa935-194">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa935-195"><dt>Secur32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa935-195"><dt>Secur32.dll</dt></span></span> </dl>                 |
| <span data-ttu-id="fa935-196">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="fa935-196">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="fa935-197">**Аккуирекредентиалшандлев** (Юникод) и **аккуирекредентиалшандлеа** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="fa935-197">**AcquireCredentialsHandleW** (Unicode) and **AcquireCredentialsHandleA** (ANSI)</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="fa935-198">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fa935-198">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa935-199">Функции SSPI</span><span class="sxs-lookup"><span data-stu-id="fa935-199">SSPI Functions</span></span>](authentication-functions.md#sspi-functions)
</dt> <dt>

[<span data-ttu-id="fa935-200">**AcceptSecurityContext (NTLM)**</span><span class="sxs-lookup"><span data-stu-id="fa935-200">**AcceptSecurityContext (NTLM)**</span></span>](acceptsecuritycontext--ntlm.md)
</dt> <dt>

[<span data-ttu-id="fa935-201">**InitializeSecurityContext (NTLM)**</span><span class="sxs-lookup"><span data-stu-id="fa935-201">**InitializeSecurityContext (NTLM)**</span></span>](initializesecuritycontext--ntlm.md)
</dt> <dt>

[<span data-ttu-id="fa935-202">**фрикредентиалшандле**</span><span class="sxs-lookup"><span data-stu-id="fa935-202">**FreeCredentialsHandle**</span></span>](/windows/win32/api/sspi/nf-sspi-freecredentialshandle)
</dt> </dl>

 

 
