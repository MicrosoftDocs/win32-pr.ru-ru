---
description: Получает маркер для существующих учетных данных субъекта безопасности, использующего протокол Kerberos.
ms.assetid: 2612bbe9-856b-4a81-bffb-6c761035883d
title: Функция AcquireCredentialsHandle (Kerberos) (SSPI. h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 05a4dd885712e89b812896684f73d60df610e41d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105719640"
---
# <a name="acquirecredentialshandle-kerberos-function"></a><span data-ttu-id="b8275-103">Функция AcquireCredentialsHandle (Kerberos)</span><span class="sxs-lookup"><span data-stu-id="b8275-103">AcquireCredentialsHandle (Kerberos) function</span></span>

<span data-ttu-id="b8275-104">Функция **AcquireCredentialsHandle (Kerberos)** получает маркер для существующих учетных данных [*субъекта безопасности*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="b8275-104">The **AcquireCredentialsHandle (Kerberos)** function acquires a handle to preexisting credentials of a [*security principal*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="b8275-105">Этот обработчик необходим для функций [**InitializeSecurityContext (Kerberos)**](initializesecuritycontext--kerberos.md) и [**AcceptSecurityContext (Kerberos)**](acceptsecuritycontext--kerberos.md) .</span><span class="sxs-lookup"><span data-stu-id="b8275-105">This handle is required by the [**InitializeSecurityContext (Kerberos)**](initializesecuritycontext--kerberos.md) and [**AcceptSecurityContext (Kerberos)**](acceptsecuritycontext--kerberos.md) functions.</span></span> <span data-ttu-id="b8275-106">Это могут быть либо существовавшие ранее *учетные данные*, которые устанавливаются с помощью системного входа, не описываемого здесь, либо вызывающая сторона может предоставить альтернативные учетные данные.</span><span class="sxs-lookup"><span data-stu-id="b8275-106">These can be either preexisting *credentials*, which are established through a system logon that is not described here, or the caller can provide alternative credentials.</span></span>

> [!Note]  
> <span data-ttu-id="b8275-107">Это не «вход в сеть» и не предполагает сбор учетных данных.</span><span class="sxs-lookup"><span data-stu-id="b8275-107">This is not a "log on to the network" and does not imply gathering of credentials.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="b8275-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b8275-108">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="b8275-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="b8275-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8275-110">*псзпринЦипал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b8275-110">*pszPrincipal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8275-111">Указатель на строку, завершающуюся нулем, которая указывает имя участника, учетные данные которого будут ссылаться на этот обработчик.</span><span class="sxs-lookup"><span data-stu-id="b8275-111">A pointer to a null-terminated string that specifies the name of the principal whose credentials the handle will reference.</span></span>

> [!Note]  
> <span data-ttu-id="b8275-112">Если процесс, запрашивающий этот обработчик, не имеет доступа к учетным данным, функция возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="b8275-112">If the process that requests the handle does not have access to the credentials, the function returns an error.</span></span> <span data-ttu-id="b8275-113">Строка NULL указывает, что процессу требуется маркер для учетных данных пользователя, от имени которого выполняется [*контекст безопасности*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="b8275-113">A null string indicates that the process requires a handle to the credentials of the user under whose [*security context*](../secgloss/s-gly.md) it is executing.</span></span>

 

</dd> <dt>

<span data-ttu-id="b8275-114">*псзпаккаже* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b8275-114">*pszPackage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8275-115">Указатель на строку, завершающуюся нулем, которая указывает имя [*пакета безопасности*](../secgloss/s-gly.md) , с помощью которого будут использоваться эти учетные данные.</span><span class="sxs-lookup"><span data-stu-id="b8275-115">A pointer to a null-terminated string that specifies the name of the [*security package*](../secgloss/s-gly.md) with which these credentials will be used.</span></span> <span data-ttu-id="b8275-116">Это имя [*пакета безопасности*](../secgloss/s-gly.md) , возвращаемое в члене **Name** структуры [**Секпкгинфо**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) , возвращаемой функцией [**енумератесекуритипаккажес**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) .</span><span class="sxs-lookup"><span data-stu-id="b8275-116">This is a [*security package*](../secgloss/s-gly.md) name returned in the **Name** member of a [**SecPkgInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) structure returned by the [**EnumerateSecurityPackages**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) function.</span></span> <span data-ttu-id="b8275-117">После установки контекста [**QueryContextAttributes (Kerberos)**](querycontextattributes--kerberos.md) может быть вызван с параметром *улаттрибуте* , имеющим значение SECPKG \_ attr \_ , \_ для возврата информации о используемом [*пакете безопасности*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="b8275-117">After a context is established, [**QueryContextAttributes (Kerberos)**](querycontextattributes--kerberos.md) can be called with *ulAttribute* set to SECPKG\_ATTR\_PACKAGE\_INFO to return information on the [*security package*](../secgloss/s-gly.md) in use.</span></span>

</dd> <dt>

<span data-ttu-id="b8275-118">*фкредентиалусе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b8275-118">*fCredentialUse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8275-119">Флаг, указывающий, как будут использоваться эти учетные данные.</span><span class="sxs-lookup"><span data-stu-id="b8275-119">A flag that indicates how these credentials will be used.</span></span> <span data-ttu-id="b8275-120">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="b8275-120">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="b8275-121">Значение</span><span class="sxs-lookup"><span data-stu-id="b8275-121">Value</span></span>                                                                                                                                                                               | <span data-ttu-id="b8275-122">Значение</span><span class="sxs-lookup"><span data-stu-id="b8275-122">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SECPKG_CRED_BOTH"></span><span id="secpkg_cred_both"></span><dl> <span data-ttu-id="b8275-123"><dt>**SECPKG \_ cred \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b8275-123"><dt>**SECPKG\_CRED\_BOTH**</dt></span></span> </dl>             | <span data-ttu-id="b8275-124">Проверка входящих учетных данных или использование локальных учетных данных для подготовки исходящего маркера.</span><span class="sxs-lookup"><span data-stu-id="b8275-124">Validate an incoming credential or use a local credential to prepare an outgoing token.</span></span> <span data-ttu-id="b8275-125">Этот флаг включает и другие флаги.</span><span class="sxs-lookup"><span data-stu-id="b8275-125">This flag enables both other flags.</span></span><br/>                                                                                                                                                                                                                                                                                                                              |
| <span id="SECPKG_CRED_INBOUND"></span><span id="secpkg_cred_inbound"></span><dl> <span data-ttu-id="b8275-126"><dt>**SECPKG \_ cred \_ Inbound**</dt></span><span class="sxs-lookup"><span data-stu-id="b8275-126"><dt>**SECPKG\_CRED\_INBOUND**</dt></span></span> </dl>    | <span data-ttu-id="b8275-127">Проверка учетных данных входящего сервера.</span><span class="sxs-lookup"><span data-stu-id="b8275-127">Validate an incoming server credential.</span></span> <span data-ttu-id="b8275-128">Входящие учетные данные могут быть проверены с помощью центра проверки подлинности при вызове [**InitializeSecurityContext (Kerberos)**](initializesecuritycontext--kerberos.md) или [**AcceptSecurityContext (Kerberos)**](acceptsecuritycontext--kerberos.md) .</span><span class="sxs-lookup"><span data-stu-id="b8275-128">Inbound credentials might be validated by using an authenticating authority when [**InitializeSecurityContext (Kerberos)**](initializesecuritycontext--kerberos.md) or [**AcceptSecurityContext (Kerberos)**](acceptsecuritycontext--kerberos.md) is called.</span></span> <span data-ttu-id="b8275-129">Если такой центр недоступен, функция завершится ошибкой и возвратит значение, равное, \_ \_ без \_ центра проверки подлинности \_ .</span><span class="sxs-lookup"><span data-stu-id="b8275-129">If such an authority is not available, the function will fail and return SEC\_E\_NO\_AUTHENTICATING\_AUTHORITY.</span></span> <span data-ttu-id="b8275-130">Проверка зависит от пакета.</span><span class="sxs-lookup"><span data-stu-id="b8275-130">Validation is package specific.</span></span><br/> |
| <span id="SECPKG_CRED_OUTBOUND"></span><span id="secpkg_cred_outbound"></span><dl> <span data-ttu-id="b8275-131"><dt>**исходящий SECPKG \_ cred \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b8275-131"><dt>**SECPKG\_CRED\_OUTBOUND**</dt></span></span> </dl> | <span data-ttu-id="b8275-132">Разрешение учетных данных локального клиента для подготовки исходящего маркера.</span><span class="sxs-lookup"><span data-stu-id="b8275-132">Allow a local client credential to prepare an outgoing token.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="b8275-133">*пвлогонид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b8275-133">*pvLogonID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8275-134">Указатель на [*локально уникальный идентификатор*](../secgloss/l-gly.md) (LUID), определяющий пользователя.</span><span class="sxs-lookup"><span data-stu-id="b8275-134">A pointer to a [*locally unique identifier*](../secgloss/l-gly.md) (LUID) that identifies the user.</span></span> <span data-ttu-id="b8275-135">Этот параметр предоставляется для процессов файловой системы, таких как сетевые перенаправления.</span><span class="sxs-lookup"><span data-stu-id="b8275-135">This parameter is provided for file-system processes such as network redirectors.</span></span> <span data-ttu-id="b8275-136">Этот параметр может принимать значение **NULL**.</span><span class="sxs-lookup"><span data-stu-id="b8275-136">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b8275-137">*паусдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b8275-137">*pAuthData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8275-138">Указатель на данные, зависящие от пакета.</span><span class="sxs-lookup"><span data-stu-id="b8275-138">A pointer to package-specific data.</span></span> <span data-ttu-id="b8275-139">Этот параметр может иметь **значение NULL**, что означает, что необходимо использовать учетные данные по умолчанию для этого [*пакета безопасности*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="b8275-139">This parameter can be **NULL**, which indicates that the default credentials for that [*security package*](../secgloss/s-gly.md) must be used.</span></span> <span data-ttu-id="b8275-140">Чтобы использовать предоставленные учетные данные, передайте в этом параметре структуру [**\_ \_ \_ удостоверений проверки подлинности WinNT (с**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) ).</span><span class="sxs-lookup"><span data-stu-id="b8275-140">To use supplied credentials, pass a [**SEC\_WINNT\_AUTH\_IDENTITY**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) structure that includes those credentials in this parameter.</span></span> <span data-ttu-id="b8275-141">Время выполнения RPC передает все, что было указано в [**рпкбиндингсетаусинфо**](/windows/win32/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo).</span><span class="sxs-lookup"><span data-stu-id="b8275-141">The RPC run time passes whatever was provided in [**RpcBindingSetAuthInfo**](/windows/win32/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo).</span></span>

</dd> <dt>

<span data-ttu-id="b8275-142">*пжеткэйфн* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b8275-142">*pGetKeyFn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8275-143">Этот параметр не используется и должен иметь значение **null**.</span><span class="sxs-lookup"><span data-stu-id="b8275-143">This parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b8275-144">*пвжеткэйаргумент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b8275-144">*pvGetKeyArgument* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8275-145">Этот параметр не используется и должен иметь значение **null**.</span><span class="sxs-lookup"><span data-stu-id="b8275-145">This parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b8275-146">*фкредентиал* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b8275-146">*phCredential* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b8275-147">Указатель на структуру [кредхандле](sspi-handles.md) для получения маркера учетных данных.</span><span class="sxs-lookup"><span data-stu-id="b8275-147">A pointer to a [CredHandle](sspi-handles.md) structure to receive the credential handle.</span></span>

</dd> <dt>

<span data-ttu-id="b8275-148">*птсекспири* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b8275-148">*ptsExpiry* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b8275-149">Указатель на структуру [**метки времени**](timestamp.md) , которая получает время истечения срока действия возвращенных учетных данных.</span><span class="sxs-lookup"><span data-stu-id="b8275-149">A pointer to a [**TimeStamp**](timestamp.md) structure that receives the time at which the returned credentials expire.</span></span> <span data-ttu-id="b8275-150">Значение, возвращаемое этой структурой **отметок времени** , зависит от [*ограниченного делегирования*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="b8275-150">The value returned in this **TimeStamp** structure depends on the [*constrained delegation*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="b8275-151">[*Пакет безопасности*](../secgloss/s-gly.md) должен вернуть это значение в местное время.</span><span class="sxs-lookup"><span data-stu-id="b8275-151">The [*security package*](../secgloss/s-gly.md) must return this value in local time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8275-152">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b8275-152">Return value</span></span>

<span data-ttu-id="b8275-153">Если функция завершается успешно, функция возвращает значение секунды \_ E \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="b8275-153">If the function succeeds, the function returns SEC\_E\_OK.</span></span>

<span data-ttu-id="b8275-154">Если функция завершается ошибкой, возвращается один из следующих кодов ошибок.</span><span class="sxs-lookup"><span data-stu-id="b8275-154">If the function fails, it returns one of the following error codes.</span></span>



| <span data-ttu-id="b8275-155">Код возврата</span><span class="sxs-lookup"><span data-stu-id="b8275-155">Return code</span></span>                                                                                                 | <span data-ttu-id="b8275-156">Описание</span><span class="sxs-lookup"><span data-stu-id="b8275-156">Description</span></span>                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b8275-157"><dt>**СЕК \_ . \_ недостаточный \_ объем памяти**</dt></span><span class="sxs-lookup"><span data-stu-id="b8275-157"><dt>**SEC\_E\_INSUFFICIENT\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="b8275-158">Недостаточно доступной памяти для завершения запрошенного действия.</span><span class="sxs-lookup"><span data-stu-id="b8275-158">There is not enough memory available to complete the requested action.</span></span><br/>                                                                  |
| <dl> <span data-ttu-id="b8275-159"><dt>**\_ \_ Внутренняя ошибка E \_ sec**</dt></span><span class="sxs-lookup"><span data-stu-id="b8275-159"><dt>**SEC\_E\_INTERNAL\_ERROR**</dt></span></span> </dl>      | <span data-ttu-id="b8275-160">Произошла ошибка, которая не сопоставлена с кодом ошибки SSPI.</span><span class="sxs-lookup"><span data-stu-id="b8275-160">An error occurred that did not map to an SSPI error code.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="b8275-161"><dt>**с \_ \_ без \_ учетных данных**</dt></span><span class="sxs-lookup"><span data-stu-id="b8275-161"><dt>**SEC\_E\_NO\_CREDENTIALS**</dt></span></span> </dl>      | <span data-ttu-id="b8275-162">Учетные данные недоступны в [*ограниченном делегировании*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="b8275-162">No credentials are available in the [*constrained delegation*](../secgloss/s-gly.md).</span></span><br/> |
| <dl> <span data-ttu-id="b8275-163"><dt>**СЕК. \_ е. \_ не \_ владелец**</dt></span><span class="sxs-lookup"><span data-stu-id="b8275-163"><dt>**SEC\_E\_NOT\_OWNER**</dt></span></span> </dl>           | <span data-ttu-id="b8275-164">Вызывающий объект функции не имеет необходимых учетных данных.</span><span class="sxs-lookup"><span data-stu-id="b8275-164">The caller of the function does not have the necessary credentials.</span></span><br/>                                                                     |
| <dl> <span data-ttu-id="b8275-165"><dt>**с \_ е \_ SECPKG \_ не \_ Найдено**</dt></span><span class="sxs-lookup"><span data-stu-id="b8275-165"><dt>**SEC\_E\_SECPKG\_NOT\_FOUND**</dt></span></span> </dl>   | <span data-ttu-id="b8275-166">Запрошенный [*пакет безопасности*](../secgloss/s-gly.md) не существует.</span><span class="sxs-lookup"><span data-stu-id="b8275-166">The requested [*security package*](../secgloss/s-gly.md) does not exist.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="b8275-167"><dt>**с \_ е \_ неизвестные \_ учетные данные**</dt></span><span class="sxs-lookup"><span data-stu-id="b8275-167"><dt>**SEC\_E\_UNKNOWN\_CREDENTIALS**</dt></span></span> </dl> | <span data-ttu-id="b8275-168">Учетные данные, предоставленные пакету, не распознаны.</span><span class="sxs-lookup"><span data-stu-id="b8275-168">The credentials supplied to the package were not recognized.</span></span><br/>                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="b8275-169">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b8275-169">Remarks</span></span>

<span data-ttu-id="b8275-170">Функция **AcquireCredentialsHandle (Kerberos)** возвращает маркер учетных данных участника, например пользователя или клиента, который используется конкретным [*ограниченным делегированием*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="b8275-170">The **AcquireCredentialsHandle (Kerberos)** function returns a handle to the credentials of a principal, such as a user or client, as used by a specific [*constrained delegation*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="b8275-171">Это может быть обработчик существующих учетных данных, или функция может создать новый набор учетных данных и вернуть их.</span><span class="sxs-lookup"><span data-stu-id="b8275-171">This can be the handle to preexisting credentials, or the function can create a new set of credentials and return it.</span></span> <span data-ttu-id="b8275-172">Этот маркер можно использовать при последующих вызовах функций [**AcceptSecurityContext (Kerberos)**](acceptsecuritycontext--kerberos.md) и [**InitializeSecurityContext (Kerberos)**](initializesecuritycontext--kerberos.md) .</span><span class="sxs-lookup"><span data-stu-id="b8275-172">This handle can be used in subsequent calls to the [**AcceptSecurityContext (Kerberos)**](acceptsecuritycontext--kerberos.md) and [**InitializeSecurityContext (Kerberos)**](initializesecuritycontext--kerberos.md) functions.</span></span>

<span data-ttu-id="b8275-173">В общем случае **AcquireCredentialsHandle (Kerberos)** не позволяет процессу получить маркер учетных данных других пользователей, выполнивших вход на тот же компьютер.</span><span class="sxs-lookup"><span data-stu-id="b8275-173">In general, **AcquireCredentialsHandle (Kerberos)** does not allow a process to obtain a handle to the credentials of other users logged on to the same computer.</span></span> <span data-ttu-id="b8275-174">Однако у вызывающего \_ \_ [*право доступа*](../secgloss/s-gly.md) к имени TCB есть возможность указать [*идентификатор входа*](../secgloss/l-gly.md) (LUID) любого существующего маркера сеанса входа, чтобы получить маркер для учетных данных этого сеанса.</span><span class="sxs-lookup"><span data-stu-id="b8275-174">However, a caller with SE\_TCB\_NAME [*privilege*](../secgloss/s-gly.md) has the option of specifying the [*logon identifier*](../secgloss/l-gly.md) (LUID) of any existing logon session token to get a handle to that session's credentials.</span></span> <span data-ttu-id="b8275-175">Обычно это используется модулями режима ядра, которые должны действовать от имени вошедшего в систему пользователя.</span><span class="sxs-lookup"><span data-stu-id="b8275-175">Typically, this is used by kernel-mode modules that must act on behalf of a logged-on user.</span></span>

<span data-ttu-id="b8275-176">Пакет может вызвать функцию в *пжеткэйфн* , предоставляемую транспортом времени выполнения RPC.</span><span class="sxs-lookup"><span data-stu-id="b8275-176">A package might call the function in *pGetKeyFn* provided by the RPC run-time transport.</span></span> <span data-ttu-id="b8275-177">Если транспорт не поддерживает понятие обратного вызова для получения учетных данных, этот параметр должен иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="b8275-177">If the transport does not support the notion of callback to retrieve credentials, this parameter must be **NULL**.</span></span>

<span data-ttu-id="b8275-178">Для вызывающих объектов в режиме ядра необходимо отметить следующие отличия.</span><span class="sxs-lookup"><span data-stu-id="b8275-178">For kernel mode callers, the following differences must be noted:</span></span>

-   <span data-ttu-id="b8275-179">Два строковых параметра должны быть строками в [*Юникоде*](../secgloss/u-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="b8275-179">The two string parameters must be [*Unicode*](../secgloss/u-gly.md) strings.</span></span>
-   <span data-ttu-id="b8275-180">Значения буфера должны выделяться в виртуальной памяти процесса, а не в пуле.</span><span class="sxs-lookup"><span data-stu-id="b8275-180">The buffer values must be allocated in process virtual memory, not from the pool.</span></span>

<span data-ttu-id="b8275-181">По завершении использования возвращенных учетных данных освободите память, используемую учетными данными, вызвав функцию [**фрикредентиалшандле**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle) .</span><span class="sxs-lookup"><span data-stu-id="b8275-181">When you have finished using the returned credentials, free the memory used by the credentials by calling the [**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8275-182">Требования</span><span class="sxs-lookup"><span data-stu-id="b8275-182">Requirements</span></span>



| <span data-ttu-id="b8275-183">Требование</span><span class="sxs-lookup"><span data-stu-id="b8275-183">Requirement</span></span> | <span data-ttu-id="b8275-184">Значение</span><span class="sxs-lookup"><span data-stu-id="b8275-184">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8275-185">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b8275-185">Minimum supported client</span></span><br/> | <span data-ttu-id="b8275-186">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b8275-186">Windows XP \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="b8275-187">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b8275-187">Minimum supported server</span></span><br/> | <span data-ttu-id="b8275-188">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b8275-188">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="b8275-189">Header</span><span class="sxs-lookup"><span data-stu-id="b8275-189">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8275-190"><dt>SSPI. h (включая Security. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b8275-190"><dt>Sspi.h (include Security.h)</dt></span></span> </dl> |
| <span data-ttu-id="b8275-191">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b8275-191">Library</span></span><br/>                  | <dl> <span data-ttu-id="b8275-192"><dt>Secur32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b8275-192"><dt>Secur32.lib</dt></span></span> </dl>                 |
| <span data-ttu-id="b8275-193">DLL</span><span class="sxs-lookup"><span data-stu-id="b8275-193">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8275-194"><dt>Secur32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8275-194"><dt>Secur32.dll</dt></span></span> </dl>                 |
| <span data-ttu-id="b8275-195">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="b8275-195">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="b8275-196">**Аккуирекредентиалшандлев** (Юникод) и **аккуирекредентиалшандлеа** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="b8275-196">**AcquireCredentialsHandleW** (Unicode) and **AcquireCredentialsHandleA** (ANSI)</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="b8275-197">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b8275-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8275-198">Функции SSPI</span><span class="sxs-lookup"><span data-stu-id="b8275-198">SSPI Functions</span></span>](authentication-functions.md#sspi-functions)
</dt> <dt>

[<span data-ttu-id="b8275-199">**AcceptSecurityContext (Kerberos)**</span><span class="sxs-lookup"><span data-stu-id="b8275-199">**AcceptSecurityContext (Kerberos)**</span></span>](acceptsecuritycontext--kerberos.md)
</dt> <dt>

[<span data-ttu-id="b8275-200">**InitializeSecurityContext (Kerberos)**</span><span class="sxs-lookup"><span data-stu-id="b8275-200">**InitializeSecurityContext (Kerberos)**</span></span>](initializesecuritycontext--kerberos.md)
</dt> <dt>

[<span data-ttu-id="b8275-201">**фрикредентиалшандле**</span><span class="sxs-lookup"><span data-stu-id="b8275-201">**FreeCredentialsHandle**</span></span>](/windows/win32/api/sspi/nf-sspi-freecredentialshandle)
</dt> </dl>

 

 
