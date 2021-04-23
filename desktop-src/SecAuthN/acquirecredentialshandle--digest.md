---
description: Получает маркер для существующих учетных данных субъекта безопасности, который использует дайджест.
ms.assetid: 79f49240-e394-4584-8db7-ef721672ba6b
title: Функция AcquireCredentialsHandle (Digest) (SSPI. h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 1474eef8ad5f5a30fe7d930431185a8ff70f7dfc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265942"
---
# <a name="acquirecredentialshandle-digest-function"></a><span data-ttu-id="50637-103">Функция AcquireCredentialsHandle (Digest)</span><span class="sxs-lookup"><span data-stu-id="50637-103">AcquireCredentialsHandle (Digest) function</span></span>

<span data-ttu-id="50637-104">Функция **AcquireCredentialsHandle (Digest)** получает маркер для существующих учетных данных [*субъекта безопасности*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="50637-104">The **AcquireCredentialsHandle (Digest)** function acquires a handle to preexisting credentials of a [*security principal*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="50637-105">Этот обработчик необходим для функций [**AcceptSecurityContext (Digest)**](acceptsecuritycontext--digest.md) и [**InitializeSecurityContext (Digest)**](initializesecuritycontext--digest.md) .</span><span class="sxs-lookup"><span data-stu-id="50637-105">This handle is required by the [**AcceptSecurityContext (Digest)**](acceptsecuritycontext--digest.md) and [**InitializeSecurityContext (Digest)**](initializesecuritycontext--digest.md) functions.</span></span> <span data-ttu-id="50637-106">Это могут быть либо существовавшие ранее *учетные данные*, которые устанавливаются с помощью системного входа, не описываемого здесь, либо вызывающая сторона может предоставить альтернативные учетные данные.</span><span class="sxs-lookup"><span data-stu-id="50637-106">These can be either preexisting *credentials*, which are established through a system logon that is not described here, or the caller can provide alternative credentials.</span></span>

> [!Note]  
> <span data-ttu-id="50637-107">Это не «вход в сеть» и не предполагает сбор учетных данных.</span><span class="sxs-lookup"><span data-stu-id="50637-107">This is not a "log on to the network" and does not imply gathering of credentials.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="50637-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="50637-108">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="50637-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="50637-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50637-110">*псзпринЦипал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="50637-110">*pszPrincipal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50637-111">Указатель на строку, завершающуюся нулем, которая указывает имя участника, учетные данные которого будут ссылаться на этот обработчик.</span><span class="sxs-lookup"><span data-stu-id="50637-111">A pointer to a null-terminated string that specifies the name of the principal whose credentials the handle will reference.</span></span>

<span data-ttu-id="50637-112">При использовании дайджест-поставщика общих служб этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="50637-112">When using the Digest SSP, this parameter is optional.</span></span>

> [!Note]  
> <span data-ttu-id="50637-113">Если процесс, запрашивающий этот обработчик, не имеет доступа к учетным данным, функция возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="50637-113">If the process that requests the handle does not have access to the credentials, the function returns an error.</span></span> <span data-ttu-id="50637-114">Строка NULL указывает, что процессу требуется маркер для учетных данных пользователя, от имени которого выполняется [*контекст безопасности*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="50637-114">A null string indicates that the process requires a handle to the credentials of the user under whose [*security context*](../secgloss/s-gly.md) it is executing.</span></span>

 

</dd> <dt>

<span data-ttu-id="50637-115">*псзпаккаже* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="50637-115">*pszPackage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50637-116">Указатель на строку, завершающуюся нулем, которая указывает имя [*пакета безопасности*](../secgloss/s-gly.md) , с помощью которого будут использоваться эти учетные данные.</span><span class="sxs-lookup"><span data-stu-id="50637-116">A pointer to a null-terminated string that specifies the name of the [*security package*](../secgloss/s-gly.md) with which these credentials will be used.</span></span> <span data-ttu-id="50637-117">Это имя [*пакета безопасности*](../secgloss/s-gly.md) , возвращаемое в члене **Name** структуры [**Секпкгинфо**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) , возвращаемой функцией [**енумератесекуритипаккажес**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) .</span><span class="sxs-lookup"><span data-stu-id="50637-117">This is a [*security package*](../secgloss/s-gly.md) name returned in the **Name** member of a [**SecPkgInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) structure returned by the [**EnumerateSecurityPackages**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) function.</span></span> <span data-ttu-id="50637-118">После установки контекста можно вызвать [**QueryContextAttributes (Digest)**](querycontextattributes--digest.md) с параметром *улаттрибуте* , имеющим значение SECPKG \_ attr, \_ \_ для возврата информации о используемом [*пакете безопасности*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="50637-118">After a context is established, [**QueryContextAttributes (Digest)**](querycontextattributes--digest.md) can be called with *ulAttribute* set to SECPKG\_ATTR\_PACKAGE\_INFO to return information on the [*security package*](../secgloss/s-gly.md) in use.</span></span>

<span data-ttu-id="50637-119">При использовании дайджест-поставщика общих служб задайте для этого параметра значение WDIGEST \_ SP \_ Name.</span><span class="sxs-lookup"><span data-stu-id="50637-119">When using the Digest SSP, set this parameter to WDIGEST\_SP\_NAME.</span></span>

</dd> <dt>

<span data-ttu-id="50637-120">*фкредентиалусе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="50637-120">*fCredentialUse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50637-121">Флаг, указывающий, как будут использоваться эти учетные данные.</span><span class="sxs-lookup"><span data-stu-id="50637-121">A flag that indicates how these credentials will be used.</span></span> <span data-ttu-id="50637-122">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="50637-122">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="50637-123">Значение</span><span class="sxs-lookup"><span data-stu-id="50637-123">Value</span></span>                                                                                                                                                                               | <span data-ttu-id="50637-124">Значение</span><span class="sxs-lookup"><span data-stu-id="50637-124">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SECPKG_CRED_INBOUND"></span><span id="secpkg_cred_inbound"></span><dl> <span data-ttu-id="50637-125"><dt>**SECPKG \_ cred \_ Inbound**</dt></span><span class="sxs-lookup"><span data-stu-id="50637-125"><dt>**SECPKG\_CRED\_INBOUND**</dt></span></span> </dl>    | <span data-ttu-id="50637-126">Проверка учетных данных входящего сервера.</span><span class="sxs-lookup"><span data-stu-id="50637-126">Validate an incoming server credential.</span></span> <span data-ttu-id="50637-127">Входящие учетные данные могут быть проверены с помощью центра проверки подлинности при вызове [**InitializeSecurityContext (Digest)**](initializesecuritycontext--digest.md) или [**AcceptSecurityContext (Digest)**](acceptsecuritycontext--digest.md) .</span><span class="sxs-lookup"><span data-stu-id="50637-127">Inbound credentials might be validated by using an authenticating authority when [**InitializeSecurityContext (Digest)**](initializesecuritycontext--digest.md) or [**AcceptSecurityContext (Digest)**](acceptsecuritycontext--digest.md) is called.</span></span> <span data-ttu-id="50637-128">Если такой центр недоступен, функция завершится ошибкой и возвратит значение, равное, \_ \_ без \_ центра проверки подлинности \_ .</span><span class="sxs-lookup"><span data-stu-id="50637-128">If such an authority is not available, the function will fail and return SEC\_E\_NO\_AUTHENTICATING\_AUTHORITY.</span></span> <span data-ttu-id="50637-129">Проверка зависит от пакета.</span><span class="sxs-lookup"><span data-stu-id="50637-129">Validation is package specific.</span></span><br/> |
| <span id="SECPKG_CRED_OUTBOUND"></span><span id="secpkg_cred_outbound"></span><dl> <span data-ttu-id="50637-130"><dt>**исходящий SECPKG \_ cred \_**</dt></span><span class="sxs-lookup"><span data-stu-id="50637-130"><dt>**SECPKG\_CRED\_OUTBOUND**</dt></span></span> </dl> | <span data-ttu-id="50637-131">Разрешение учетных данных локального клиента для подготовки исходящего маркера.</span><span class="sxs-lookup"><span data-stu-id="50637-131">Allow a local client credential to prepare an outgoing token.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                    |



 

</dd> <dt>

<span data-ttu-id="50637-132">*пвлогонид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="50637-132">*pvLogonID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50637-133">Указатель на [*локально уникальный идентификатор*](../secgloss/l-gly.md) (LUID), определяющий пользователя.</span><span class="sxs-lookup"><span data-stu-id="50637-133">A pointer to a [*locally unique identifier*](../secgloss/l-gly.md) (LUID) that identifies the user.</span></span> <span data-ttu-id="50637-134">Этот параметр предоставляется для процессов файловой системы, таких как сетевые перенаправления.</span><span class="sxs-lookup"><span data-stu-id="50637-134">This parameter is provided for file-system processes such as network redirectors.</span></span> <span data-ttu-id="50637-135">Этот параметр может принимать значение **NULL**.</span><span class="sxs-lookup"><span data-stu-id="50637-135">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="50637-136">*паусдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="50637-136">*pAuthData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50637-137">Указатель на данные, зависящие от пакета.</span><span class="sxs-lookup"><span data-stu-id="50637-137">A pointer to package-specific data.</span></span> <span data-ttu-id="50637-138">Этот параметр может иметь **значение NULL**, что означает, что необходимо использовать учетные данные по умолчанию для этого [*пакета безопасности*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="50637-138">This parameter can be **NULL**, which indicates that the default credentials for that [*security package*](../secgloss/s-gly.md) must be used.</span></span> <span data-ttu-id="50637-139">Чтобы использовать предоставленные учетные данные, передайте в этом параметре структуру [**\_ \_ \_ удостоверений проверки подлинности WinNT (с**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) ).</span><span class="sxs-lookup"><span data-stu-id="50637-139">To use supplied credentials, pass a [**SEC\_WINNT\_AUTH\_IDENTITY**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) structure that includes those credentials in this parameter.</span></span> <span data-ttu-id="50637-140">Время выполнения RPC передает все, что было указано в [**рпкбиндингсетаусинфо**](/windows/win32/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo).</span><span class="sxs-lookup"><span data-stu-id="50637-140">The RPC run time passes whatever was provided in [**RpcBindingSetAuthInfo**](/windows/win32/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo).</span></span>

<span data-ttu-id="50637-141">При использовании дайджест-поставщика общих служб этот параметр является указателем на [**структуру \_ \_ \_ удостоверения WinNT auth в секунду**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) , которая содержит сведения для проверки подлинности, используемые для нахождение учетных данных.</span><span class="sxs-lookup"><span data-stu-id="50637-141">When using the Digest SSP, this parameter is a pointer to a [**SEC\_WINNT\_AUTH\_IDENTITY**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) structure that contains authentication information to use to locate the credentials.</span></span>

</dd> <dt>

<span data-ttu-id="50637-142">*пжеткэйфн* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="50637-142">*pGetKeyFn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50637-143">Этот параметр не используется и должен иметь значение **null**.</span><span class="sxs-lookup"><span data-stu-id="50637-143">This parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="50637-144">*пвжеткэйаргумент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="50637-144">*pvGetKeyArgument* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50637-145">Этот параметр не используется и должен иметь значение **null**.</span><span class="sxs-lookup"><span data-stu-id="50637-145">This parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="50637-146">*фкредентиал* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="50637-146">*phCredential* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="50637-147">Указатель на структуру [кредхандле](sspi-handles.md) для получения маркера учетных данных.</span><span class="sxs-lookup"><span data-stu-id="50637-147">A pointer to a [CredHandle](sspi-handles.md) structure to receive the credential handle.</span></span>

</dd> <dt>

<span data-ttu-id="50637-148">*птсекспири* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="50637-148">*ptsExpiry* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="50637-149">Указатель на структуру [**метки времени**](timestamp.md) , которая получает время истечения срока действия возвращенных учетных данных.</span><span class="sxs-lookup"><span data-stu-id="50637-149">A pointer to a [**TimeStamp**](timestamp.md) structure that receives the time at which the returned credentials expire.</span></span> <span data-ttu-id="50637-150">Значение, возвращаемое этой структурой **отметок времени** , зависит от [*ограниченного делегирования*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="50637-150">The value returned in this **TimeStamp** structure depends on the [*constrained delegation*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="50637-151">[*Пакет безопасности*](../secgloss/s-gly.md) должен вернуть это значение в местное время.</span><span class="sxs-lookup"><span data-stu-id="50637-151">The [*security package*](../secgloss/s-gly.md) must return this value in local time.</span></span>

<span data-ttu-id="50637-152">Для этого параметра задается постоянное максимальное время.</span><span class="sxs-lookup"><span data-stu-id="50637-152">This parameter is set to a constant maximum time.</span></span> <span data-ttu-id="50637-153">Нет времени истечения срока действия для дайджест- [*контекста безопасности*](../secgloss/s-gly.md)или учетных данных, либо при использовании дайджест-поставщика общих служб.</span><span class="sxs-lookup"><span data-stu-id="50637-153">There is no expiration time for Digest [*security context*](../secgloss/s-gly.md)s or credentials or when using the Digest SSP.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50637-154">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="50637-154">Return value</span></span>

<span data-ttu-id="50637-155">Если функция завершается успешно, функция возвращает значение секунды \_ E \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="50637-155">If the function succeeds, the function returns SEC\_E\_OK.</span></span>

<span data-ttu-id="50637-156">Если функция завершается ошибкой, возвращается один из следующих кодов ошибок.</span><span class="sxs-lookup"><span data-stu-id="50637-156">If the function fails, it returns one of the following error codes.</span></span>



| <span data-ttu-id="50637-157">Код возврата</span><span class="sxs-lookup"><span data-stu-id="50637-157">Return code</span></span>                                                                                                 | <span data-ttu-id="50637-158">Описание</span><span class="sxs-lookup"><span data-stu-id="50637-158">Description</span></span>                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="50637-159"><dt>**СЕК \_ . \_ недостаточный \_ объем памяти**</dt></span><span class="sxs-lookup"><span data-stu-id="50637-159"><dt>**SEC\_E\_INSUFFICIENT\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="50637-160">Недостаточно доступной памяти для завершения запрошенного действия.</span><span class="sxs-lookup"><span data-stu-id="50637-160">There is not enough memory available to complete the requested action.</span></span><br/>                                                                  |
| <dl> <span data-ttu-id="50637-161"><dt>**\_ \_ Внутренняя ошибка E \_ sec**</dt></span><span class="sxs-lookup"><span data-stu-id="50637-161"><dt>**SEC\_E\_INTERNAL\_ERROR**</dt></span></span> </dl>      | <span data-ttu-id="50637-162">Произошла ошибка, которая не сопоставлена с кодом ошибки SSPI.</span><span class="sxs-lookup"><span data-stu-id="50637-162">An error occurred that did not map to an SSPI error code.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="50637-163"><dt>**с \_ \_ без \_ учетных данных**</dt></span><span class="sxs-lookup"><span data-stu-id="50637-163"><dt>**SEC\_E\_NO\_CREDENTIALS**</dt></span></span> </dl>      | <span data-ttu-id="50637-164">Учетные данные недоступны в [*ограниченном делегировании*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="50637-164">No credentials are available in the [*constrained delegation*](../secgloss/s-gly.md).</span></span><br/> |
| <dl> <span data-ttu-id="50637-165"><dt>**СЕК. \_ е. \_ не \_ владелец**</dt></span><span class="sxs-lookup"><span data-stu-id="50637-165"><dt>**SEC\_E\_NOT\_OWNER**</dt></span></span> </dl>           | <span data-ttu-id="50637-166">Вызывающий объект функции не имеет необходимых учетных данных.</span><span class="sxs-lookup"><span data-stu-id="50637-166">The caller of the function does not have the necessary credentials.</span></span><br/>                                                                     |
| <dl> <span data-ttu-id="50637-167"><dt>**с \_ е \_ SECPKG \_ не \_ Найдено**</dt></span><span class="sxs-lookup"><span data-stu-id="50637-167"><dt>**SEC\_E\_SECPKG\_NOT\_FOUND**</dt></span></span> </dl>   | <span data-ttu-id="50637-168">Запрошенный [*пакет безопасности*](../secgloss/s-gly.md) не существует.</span><span class="sxs-lookup"><span data-stu-id="50637-168">The requested [*security package*](../secgloss/s-gly.md) does not exist.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="50637-169"><dt>**с \_ е \_ неизвестные \_ учетные данные**</dt></span><span class="sxs-lookup"><span data-stu-id="50637-169"><dt>**SEC\_E\_UNKNOWN\_CREDENTIALS**</dt></span></span> </dl> | <span data-ttu-id="50637-170">Учетные данные, предоставленные пакету, не распознаны.</span><span class="sxs-lookup"><span data-stu-id="50637-170">The credentials supplied to the package were not recognized.</span></span><br/>                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="50637-171">Комментарии</span><span class="sxs-lookup"><span data-stu-id="50637-171">Remarks</span></span>

<span data-ttu-id="50637-172">Функция **AcquireCredentialsHandle (Digest)** возвращает маркер учетных данных участника, например пользователя или клиента, который используется конкретным [*ограниченным делегированием*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="50637-172">The **AcquireCredentialsHandle (Digest)** function returns a handle to the credentials of a principal, such as a user or client, as used by a specific [*constrained delegation*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="50637-173">Это может быть обработчик существующих учетных данных, или функция может создать новый набор учетных данных и вернуть их.</span><span class="sxs-lookup"><span data-stu-id="50637-173">This can be the handle to preexisting credentials, or the function can create a new set of credentials and return it.</span></span> <span data-ttu-id="50637-174">Этот маркер можно использовать при последующих вызовах функций [**AcceptSecurityContext (Digest)**](acceptsecuritycontext--digest.md) и [**InitializeSecurityContext (Digest)**](initializesecuritycontext--digest.md) .</span><span class="sxs-lookup"><span data-stu-id="50637-174">This handle can be used in subsequent calls to the [**AcceptSecurityContext (Digest)**](acceptsecuritycontext--digest.md) and [**InitializeSecurityContext (Digest)**](initializesecuritycontext--digest.md) functions.</span></span>

<span data-ttu-id="50637-175">В общем случае **AcquireCredentialsHandle (дайджест)** не позволяет процессу получить маркер учетных данных других пользователей, выполнивших вход на тот же компьютер.</span><span class="sxs-lookup"><span data-stu-id="50637-175">In general, **AcquireCredentialsHandle (Digest)** does not allow a process to obtain a handle to the credentials of other users logged on to the same computer.</span></span> <span data-ttu-id="50637-176">Однако у вызывающего \_ \_ [*право доступа*](../secgloss/s-gly.md) к имени TCB есть возможность указать [*идентификатор входа*](../secgloss/l-gly.md) (LUID) любого существующего маркера сеанса входа, чтобы получить маркер для учетных данных этого сеанса.</span><span class="sxs-lookup"><span data-stu-id="50637-176">However, a caller with SE\_TCB\_NAME [*privilege*](../secgloss/s-gly.md) has the option of specifying the [*logon identifier*](../secgloss/l-gly.md) (LUID) of any existing logon session token to get a handle to that session's credentials.</span></span> <span data-ttu-id="50637-177">Обычно это используется модулями режима ядра, которые должны действовать от имени вошедшего в систему пользователя.</span><span class="sxs-lookup"><span data-stu-id="50637-177">Typically, this is used by kernel-mode modules that must act on behalf of a logged-on user.</span></span>

<span data-ttu-id="50637-178">Пакет может вызвать функцию в *пжеткэйфн* , предоставляемую транспортом времени выполнения RPC.</span><span class="sxs-lookup"><span data-stu-id="50637-178">A package might call the function in *pGetKeyFn* provided by the RPC run-time transport.</span></span> <span data-ttu-id="50637-179">Если транспорт не поддерживает понятие обратного вызова для получения учетных данных, этот параметр должен иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="50637-179">If the transport does not support the notion of callback to retrieve credentials, this parameter must be **NULL**.</span></span>

<span data-ttu-id="50637-180">Для вызывающих объектов в режиме ядра необходимо отметить следующие отличия.</span><span class="sxs-lookup"><span data-stu-id="50637-180">For kernel mode callers, the following differences must be noted:</span></span>

-   <span data-ttu-id="50637-181">Два строковых параметра должны быть строками в [*Юникоде*](../secgloss/u-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="50637-181">The two string parameters must be [*Unicode*](../secgloss/u-gly.md) strings.</span></span>
-   <span data-ttu-id="50637-182">Значения буфера должны выделяться в виртуальной памяти процесса, а не в пуле.</span><span class="sxs-lookup"><span data-stu-id="50637-182">The buffer values must be allocated in process virtual memory, not from the pool.</span></span>

<span data-ttu-id="50637-183">По завершении использования возвращенных учетных данных освободите память, используемую учетными данными, вызвав функцию [**фрикредентиалшандле**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle) .</span><span class="sxs-lookup"><span data-stu-id="50637-183">When you have finished using the returned credentials, free the memory used by the credentials by calling the [**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="50637-184">Требования</span><span class="sxs-lookup"><span data-stu-id="50637-184">Requirements</span></span>



| <span data-ttu-id="50637-185">Требование</span><span class="sxs-lookup"><span data-stu-id="50637-185">Requirement</span></span> | <span data-ttu-id="50637-186">Значение</span><span class="sxs-lookup"><span data-stu-id="50637-186">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50637-187">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="50637-187">Minimum supported client</span></span><br/> | <span data-ttu-id="50637-188">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="50637-188">Windows XP \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="50637-189">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="50637-189">Minimum supported server</span></span><br/> | <span data-ttu-id="50637-190">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="50637-190">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="50637-191">Header</span><span class="sxs-lookup"><span data-stu-id="50637-191">Header</span></span><br/>                   | <dl> <span data-ttu-id="50637-192"><dt>SSPI. h (включая Security. h)</dt></span><span class="sxs-lookup"><span data-stu-id="50637-192"><dt>Sspi.h (include Security.h)</dt></span></span> </dl> |
| <span data-ttu-id="50637-193">Библиотека</span><span class="sxs-lookup"><span data-stu-id="50637-193">Library</span></span><br/>                  | <dl> <span data-ttu-id="50637-194"><dt>Secur32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="50637-194"><dt>Secur32.lib</dt></span></span> </dl>                 |
| <span data-ttu-id="50637-195">DLL</span><span class="sxs-lookup"><span data-stu-id="50637-195">DLL</span></span><br/>                      | <dl> <span data-ttu-id="50637-196"><dt>Secur32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50637-196"><dt>Secur32.dll</dt></span></span> </dl>                 |
| <span data-ttu-id="50637-197">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="50637-197">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="50637-198">**Аккуирекредентиалшандлев** (Юникод) и **аккуирекредентиалшандлеа** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="50637-198">**AcquireCredentialsHandleW** (Unicode) and **AcquireCredentialsHandleA** (ANSI)</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="50637-199">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="50637-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50637-200">Функции SSPI</span><span class="sxs-lookup"><span data-stu-id="50637-200">SSPI Functions</span></span>](authentication-functions.md#sspi-functions)
</dt> <dt>

[<span data-ttu-id="50637-201">**AcceptSecurityContext (дайджест)**</span><span class="sxs-lookup"><span data-stu-id="50637-201">**AcceptSecurityContext (Digest)**</span></span>](acceptsecuritycontext--digest.md)
</dt> <dt>

[<span data-ttu-id="50637-202">**InitializeSecurityContext (дайджест)**</span><span class="sxs-lookup"><span data-stu-id="50637-202">**InitializeSecurityContext (Digest)**</span></span>](initializesecuritycontext--digest.md)
</dt> <dt>

[<span data-ttu-id="50637-203">**фрикредентиалшандле**</span><span class="sxs-lookup"><span data-stu-id="50637-203">**FreeCredentialsHandle**</span></span>](/windows/win32/api/sspi/nf-sspi-freecredentialshandle)
</dt> </dl>

 

 
