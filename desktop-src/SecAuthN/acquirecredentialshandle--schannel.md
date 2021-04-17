---
description: Получает маркер для существующих учетных данных субъекта безопасности, использующего SChannel.
ms.assetid: 0f006670-a1e5-47ed-baf5-ed55bd42b468
title: Функция AcquireCredentialsHandle (Schannel) (SSPI. h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 5b7de49e76cf5b09611790a12826f1a13fc38e62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105719638"
---
# <a name="acquirecredentialshandle-schannel-function"></a><span data-ttu-id="182b4-103">Функция AcquireCredentialsHandle (Schannel)</span><span class="sxs-lookup"><span data-stu-id="182b4-103">AcquireCredentialsHandle (Schannel) function</span></span>

<span data-ttu-id="182b4-104">Функция **AcquireCredentialsHandle (Schannel)** получает маркер для существующих учетных данных [*субъекта безопасности*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="182b4-104">The **AcquireCredentialsHandle (Schannel)** function acquires a handle to preexisting credentials of a [*security principal*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="182b4-105">Этот обработчик необходим для функций [**InitializeSecurityContext (Schannel)**](initializesecuritycontext--schannel.md) и [**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md) .</span><span class="sxs-lookup"><span data-stu-id="182b4-105">This handle is required by the [**InitializeSecurityContext (Schannel)**](initializesecuritycontext--schannel.md) and [**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md) functions.</span></span> <span data-ttu-id="182b4-106">Это могут быть либо существовавшие ранее *учетные данные*, которые устанавливаются с помощью системного входа, не описываемого здесь, либо вызывающая сторона может предоставить альтернативные учетные данные.</span><span class="sxs-lookup"><span data-stu-id="182b4-106">These can be either preexisting *credentials*, which are established through a system logon that is not described here, or the caller can provide alternative credentials.</span></span>

> [!Note]  
> <span data-ttu-id="182b4-107">Это не «вход в сеть» и не предполагает сбор учетных данных.</span><span class="sxs-lookup"><span data-stu-id="182b4-107">This is not a "log on to the network" and does not imply gathering of credentials.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="182b4-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="182b4-108">Syntax</span></span>


```C++
SECURITY_STATUS SEC_Entry AcquireCredentialsHandle(
  _In_opt_  SEC_CHAR       *pszPrincipal,
  _In_      SEC_CHAR       *pszPackage,
  _In_      ULONG          fCredentialUse,
  _In_opt_  PLUID          pvLogonID,
  _In_opt_  PVOID          pAuthData,
  _In_opt_  SEC_GET_KEY_FN pGetKeyFn,
  _In_opt_  PVOID          pvGetKeyArgument,
  _Out_     PCredHandle    phCredential,
  _Out_opt_ PTimeStamp     ptsExpiry
);
```



## <a name="parameters"></a><span data-ttu-id="182b4-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="182b4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="182b4-110">*псзпринЦипал* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="182b4-110">*pszPrincipal* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="182b4-111">Указатель на строку, завершающуюся нулем, которая указывает имя участника, учетные данные которого будут ссылаться на этот обработчик.</span><span class="sxs-lookup"><span data-stu-id="182b4-111">A pointer to a null-terminated string that specifies the name of the principal whose credentials the handle will reference.</span></span>

<span data-ttu-id="182b4-112">При использовании поставщика общих служб SChannel этот параметр не используется и должен иметь значение **null**.</span><span class="sxs-lookup"><span data-stu-id="182b4-112">When using the Schannel SSP, this parameter is not used and should be set to **NULL**.</span></span>

> [!Note]  
> <span data-ttu-id="182b4-113">Если процесс, запрашивающий этот обработчик, не имеет доступа к учетным данным, функция возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="182b4-113">If the process that requests the handle does not have access to the credentials, the function returns an error.</span></span> <span data-ttu-id="182b4-114">Строка NULL указывает, что процессу требуется маркер для учетных данных пользователя, от имени которого выполняется [*контекст безопасности*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="182b4-114">A null string indicates that the process requires a handle to the credentials of the user under whose [*security context*](../secgloss/s-gly.md) it is executing.</span></span>

 

</dd> <dt>

<span data-ttu-id="182b4-115">*псзпаккаже* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="182b4-115">*pszPackage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="182b4-116">Указатель на строку, завершающуюся нулем, которая указывает имя [*пакета безопасности*](../secgloss/s-gly.md) , с помощью которого будут использоваться эти учетные данные.</span><span class="sxs-lookup"><span data-stu-id="182b4-116">A pointer to a null-terminated string that specifies the name of the [*security package*](../secgloss/s-gly.md) with which these credentials will be used.</span></span> <span data-ttu-id="182b4-117">Это имя [*пакета безопасности*](../secgloss/s-gly.md) , возвращаемое в члене **Name** структуры [**Секпкгинфо**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) , возвращаемой функцией [**енумератесекуритипаккажес**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) .</span><span class="sxs-lookup"><span data-stu-id="182b4-117">This is a [*security package*](../secgloss/s-gly.md) name returned in the **Name** member of a [**SecPkgInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) structure returned by the [**EnumerateSecurityPackages**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) function.</span></span> <span data-ttu-id="182b4-118">После установки контекста [**QueryContextAttributes (Schannel)**](querycontextattributes--schannel.md) может быть вызван с параметром *улаттрибуте* , имеющим значение SECPKG \_ attr \_ , \_ для возврата информации о используемом [*пакете безопасности*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="182b4-118">After a context is established, [**QueryContextAttributes (Schannel)**](querycontextattributes--schannel.md) can be called with *ulAttribute* set to SECPKG\_ATTR\_PACKAGE\_INFO to return information on the [*security package*](../secgloss/s-gly.md) in use.</span></span>

<span data-ttu-id="182b4-119">При использовании поставщика общих служб SChannel присвойте этому параметру \_ имя унисп.</span><span class="sxs-lookup"><span data-stu-id="182b4-119">When using the Schannel SSP, set this parameter to UNISP\_NAME.</span></span>

</dd> <dt>

<span data-ttu-id="182b4-120">*фкредентиалусе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="182b4-120">*fCredentialUse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="182b4-121">Флаг, указывающий, как будут использоваться эти учетные данные.</span><span class="sxs-lookup"><span data-stu-id="182b4-121">A flag that indicates how these credentials will be used.</span></span> <span data-ttu-id="182b4-122">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="182b4-122">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="182b4-123">Значение</span><span class="sxs-lookup"><span data-stu-id="182b4-123">Value</span></span>                                                                                                                                                                               | <span data-ttu-id="182b4-124">Значение</span><span class="sxs-lookup"><span data-stu-id="182b4-124">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SECPKG_CRED_INBOUND"></span><span id="secpkg_cred_inbound"></span><dl> <span data-ttu-id="182b4-125"><dt>**SECPKG \_ cred \_ Inbound**</dt></span><span class="sxs-lookup"><span data-stu-id="182b4-125"><dt>**SECPKG\_CRED\_INBOUND**</dt></span></span> </dl>    | <span data-ttu-id="182b4-126">Проверка учетных данных входящего сервера.</span><span class="sxs-lookup"><span data-stu-id="182b4-126">Validate an incoming server credential.</span></span> <span data-ttu-id="182b4-127">Входящие учетные данные могут быть проверены с помощью центра проверки подлинности при вызове [**InitializeSecurityContext (Schannel)**](initializesecuritycontext--schannel.md) или [**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md) .</span><span class="sxs-lookup"><span data-stu-id="182b4-127">Inbound credentials might be validated by using an authenticating authority when [**InitializeSecurityContext (Schannel)**](initializesecuritycontext--schannel.md) or [**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md) is called.</span></span> <span data-ttu-id="182b4-128">Если такой центр недоступен, функция завершится ошибкой и возвратит значение, равное, \_ \_ без \_ центра проверки подлинности \_ .</span><span class="sxs-lookup"><span data-stu-id="182b4-128">If such an authority is not available, the function will fail and return SEC\_E\_NO\_AUTHENTICATING\_AUTHORITY.</span></span> <span data-ttu-id="182b4-129">Проверка зависит от пакета.</span><span class="sxs-lookup"><span data-stu-id="182b4-129">Validation is package specific.</span></span><br/> |
| <span id="SECPKG_CRED_OUTBOUND"></span><span id="secpkg_cred_outbound"></span><dl> <span data-ttu-id="182b4-130"><dt>**исходящий SECPKG \_ cred \_**</dt></span><span class="sxs-lookup"><span data-stu-id="182b4-130"><dt>**SECPKG\_CRED\_OUTBOUND**</dt></span></span> </dl> | <span data-ttu-id="182b4-131">Разрешение учетных данных локального клиента для подготовки исходящего маркера.</span><span class="sxs-lookup"><span data-stu-id="182b4-131">Allow a local client credential to prepare an outgoing token.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="182b4-132">*пвлогонид* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="182b4-132">*pvLogonID* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="182b4-133">Указатель на [*локально уникальный идентификатор*](../secgloss/l-gly.md) (LUID), определяющий пользователя.</span><span class="sxs-lookup"><span data-stu-id="182b4-133">A pointer to a [*locally unique identifier*](../secgloss/l-gly.md) (LUID) that identifies the user.</span></span> <span data-ttu-id="182b4-134">Этот параметр предоставляется для процессов файловой системы, таких как сетевые перенаправления.</span><span class="sxs-lookup"><span data-stu-id="182b4-134">This parameter is provided for file-system processes such as network redirectors.</span></span> <span data-ttu-id="182b4-135">Этот параметр может принимать значение **NULL**.</span><span class="sxs-lookup"><span data-stu-id="182b4-135">This parameter can be **NULL**.</span></span>

<span data-ttu-id="182b4-136">При использовании поставщика общих служб SChannel этот параметр не используется и должен иметь значение **null**.</span><span class="sxs-lookup"><span data-stu-id="182b4-136">When using the Schannel SSP, this parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="182b4-137">*паусдата* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="182b4-137">*pAuthData* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="182b4-138">Указатель на данные, зависящие от пакета.</span><span class="sxs-lookup"><span data-stu-id="182b4-138">A pointer to package-specific data.</span></span> <span data-ttu-id="182b4-139">Этот параметр может иметь **значение NULL**, что означает, что необходимо использовать учетные данные по умолчанию для этого [*пакета безопасности*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="182b4-139">This parameter can be **NULL**, which indicates that the default credentials for that [*security package*](../secgloss/s-gly.md) must be used.</span></span> <span data-ttu-id="182b4-140">Чтобы использовать предоставленные учетные данные, передайте в этом параметре структуру [**\_ \_ \_ удостоверений проверки подлинности WinNT (с**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) ).</span><span class="sxs-lookup"><span data-stu-id="182b4-140">To use supplied credentials, pass a [**SEC\_WINNT\_AUTH\_IDENTITY**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) structure that includes those credentials in this parameter.</span></span> <span data-ttu-id="182b4-141">Время выполнения RPC передает все, что было указано в [**рпкбиндингсетаусинфо**](/windows/win32/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo).</span><span class="sxs-lookup"><span data-stu-id="182b4-141">The RPC run time passes whatever was provided in [**RpcBindingSetAuthInfo**](/windows/win32/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo).</span></span>

<span data-ttu-id="182b4-142">При использовании поставщика общих служб SChannel укажите структуру [**SCH_CREDENTIALS**](/windows/win32/api/schannel/ns-schannel-sch_credentials) , указывающую используемый протокол, и параметры для различных настраиваемых функций канала.</span><span class="sxs-lookup"><span data-stu-id="182b4-142">When using the Schannel SSP, specify an [**SCH_CREDENTIALS**](/windows/win32/api/schannel/ns-schannel-sch_credentials) structure that indicates the protocol to use and the settings for various customizable channel features.</span></span>

</dd> <dt>

<span data-ttu-id="182b4-143">*пжеткэйфн* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="182b4-143">*pGetKeyFn* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="182b4-144">Этот параметр не используется и должен иметь значение **null**.</span><span class="sxs-lookup"><span data-stu-id="182b4-144">This parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="182b4-145">*пвжеткэйаргумент* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="182b4-145">*pvGetKeyArgument* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="182b4-146">Этот параметр не используется и должен иметь значение **null**.</span><span class="sxs-lookup"><span data-stu-id="182b4-146">This parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="182b4-147">*фкредентиал* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="182b4-147">*phCredential* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="182b4-148">Указатель на структуру [кредхандле](sspi-handles.md) для получения маркера учетных данных.</span><span class="sxs-lookup"><span data-stu-id="182b4-148">A pointer to a [CredHandle](sspi-handles.md) structure to receive the credential handle.</span></span>

</dd> <dt>

<span data-ttu-id="182b4-149">*птсекспири* \[ out, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="182b4-149">*ptsExpiry* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="182b4-150">Указатель на структуру [**метки времени**](timestamp.md) , которая получает время истечения срока действия возвращенных учетных данных.</span><span class="sxs-lookup"><span data-stu-id="182b4-150">A pointer to a [**TimeStamp**](timestamp.md) structure that receives the time at which the returned credentials expire.</span></span> <span data-ttu-id="182b4-151">Значение, возвращаемое этой структурой **отметок времени** , зависит от [*ограниченного делегирования*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="182b4-151">The value returned in this **TimeStamp** structure depends on the [*constrained delegation*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="182b4-152">[*Пакет безопасности*](../secgloss/s-gly.md) должен вернуть это значение в местное время.</span><span class="sxs-lookup"><span data-stu-id="182b4-152">The [*security package*](../secgloss/s-gly.md) must return this value in local time.</span></span>

<span data-ttu-id="182b4-153">При использовании поставщика общих служб SChannel этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="182b4-153">When using the Schannel SSP, this parameter is optional.</span></span> <span data-ttu-id="182b4-154">Если учетные данные, используемые для проверки подлинности, являются сертификатом, этот параметр получает срок действия этого сертификата.</span><span class="sxs-lookup"><span data-stu-id="182b4-154">When the credential to be used for authentication is a certificate, this parameter receives the expiration time for that certificate.</span></span> <span data-ttu-id="182b4-155">Если сертификат не указан, возвращается максимальное значение времени.</span><span class="sxs-lookup"><span data-stu-id="182b4-155">If no certificate was supplied, then a maximum time value is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="182b4-156">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="182b4-156">Return value</span></span>

<span data-ttu-id="182b4-157">Если функция завершается успешно, функция возвращает значение секунды \_ E \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="182b4-157">If the function succeeds, the function returns SEC\_E\_OK.</span></span>

<span data-ttu-id="182b4-158">Если функция завершается ошибкой, возвращается один из следующих кодов ошибок.</span><span class="sxs-lookup"><span data-stu-id="182b4-158">If the function fails, it returns one of the following error codes.</span></span>



| <span data-ttu-id="182b4-159">Код возврата</span><span class="sxs-lookup"><span data-stu-id="182b4-159">Return code</span></span>                                                                                                 | <span data-ttu-id="182b4-160">Описание</span><span class="sxs-lookup"><span data-stu-id="182b4-160">Description</span></span>                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="182b4-161"><dt>**СЕК \_ . \_ недостаточный \_ объем памяти**</dt></span><span class="sxs-lookup"><span data-stu-id="182b4-161"><dt>**SEC\_E\_INSUFFICIENT\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="182b4-162">Недостаточно доступной памяти для завершения запрошенного действия.</span><span class="sxs-lookup"><span data-stu-id="182b4-162">There is not enough memory available to complete the requested action.</span></span><br/>                                                                  |
| <dl> <span data-ttu-id="182b4-163"><dt>**\_ \_ Внутренняя ошибка E \_ sec**</dt></span><span class="sxs-lookup"><span data-stu-id="182b4-163"><dt>**SEC\_E\_INTERNAL\_ERROR**</dt></span></span> </dl>      | <span data-ttu-id="182b4-164">Произошла ошибка, которая не сопоставлена с кодом ошибки SSPI.</span><span class="sxs-lookup"><span data-stu-id="182b4-164">An error occurred that did not map to an SSPI error code.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="182b4-165"><dt>**с \_ \_ без \_ учетных данных**</dt></span><span class="sxs-lookup"><span data-stu-id="182b4-165"><dt>**SEC\_E\_NO\_CREDENTIALS**</dt></span></span> </dl>      | <span data-ttu-id="182b4-166">Учетные данные недоступны в [*ограниченном делегировании*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="182b4-166">No credentials are available in the [*constrained delegation*](../secgloss/s-gly.md).</span></span><br/> |
| <dl> <span data-ttu-id="182b4-167"><dt>**СЕК. \_ е. \_ не \_ владелец**</dt></span><span class="sxs-lookup"><span data-stu-id="182b4-167"><dt>**SEC\_E\_NOT\_OWNER**</dt></span></span> </dl>           | <span data-ttu-id="182b4-168">Вызывающий объект функции не имеет необходимых учетных данных.</span><span class="sxs-lookup"><span data-stu-id="182b4-168">The caller of the function does not have the necessary credentials.</span></span><br/>                                                                     |
| <dl> <span data-ttu-id="182b4-169"><dt>**с \_ е \_ SECPKG \_ не \_ Найдено**</dt></span><span class="sxs-lookup"><span data-stu-id="182b4-169"><dt>**SEC\_E\_SECPKG\_NOT\_FOUND**</dt></span></span> </dl>   | <span data-ttu-id="182b4-170">Запрошенный [*пакет безопасности*](../secgloss/s-gly.md) не существует.</span><span class="sxs-lookup"><span data-stu-id="182b4-170">The requested [*security package*](../secgloss/s-gly.md) does not exist.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="182b4-171"><dt>**с \_ е \_ неизвестные \_ учетные данные**</dt></span><span class="sxs-lookup"><span data-stu-id="182b4-171"><dt>**SEC\_E\_UNKNOWN\_CREDENTIALS**</dt></span></span> </dl> | <span data-ttu-id="182b4-172">Учетные данные, предоставленные пакету, не распознаны.</span><span class="sxs-lookup"><span data-stu-id="182b4-172">The credentials supplied to the package were not recognized.</span></span><br/>                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="182b4-173">Комментарии</span><span class="sxs-lookup"><span data-stu-id="182b4-173">Remarks</span></span>

<span data-ttu-id="182b4-174">Функция **AcquireCredentialsHandle (Schannel)** возвращает маркер учетных данных участника, например пользователя или клиента, который используется конкретным [*ограниченным делегированием*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="182b4-174">The **AcquireCredentialsHandle (Schannel)** function returns a handle to the credentials of a principal, such as a user or client, as used by a specific [*constrained delegation*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="182b4-175">Это может быть обработчик существующих учетных данных, или функция может создать новый набор учетных данных и вернуть их.</span><span class="sxs-lookup"><span data-stu-id="182b4-175">This can be the handle to preexisting credentials, or the function can create a new set of credentials and return it.</span></span> <span data-ttu-id="182b4-176">Этот маркер можно использовать при последующих вызовах функций [**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md) и [**InitializeSecurityContext (Schannel)**](initializesecuritycontext--schannel.md) .</span><span class="sxs-lookup"><span data-stu-id="182b4-176">This handle can be used in subsequent calls to the [**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md) and [**InitializeSecurityContext (Schannel)**](initializesecuritycontext--schannel.md) functions.</span></span>

<span data-ttu-id="182b4-177">В общем случае **AcquireCredentialsHandle (Schannel)** не позволяет процессу получить маркер учетных данных других пользователей, выполнивших вход на тот же компьютер.</span><span class="sxs-lookup"><span data-stu-id="182b4-177">In general, **AcquireCredentialsHandle (Schannel)** does not allow a process to obtain a handle to the credentials of other users logged on to the same computer.</span></span> <span data-ttu-id="182b4-178">Однако у вызывающего \_ \_ [*право доступа*](../secgloss/s-gly.md) к имени TCB есть возможность указать [*идентификатор входа*](../secgloss/l-gly.md) (LUID) любого существующего маркера сеанса входа, чтобы получить маркер для учетных данных этого сеанса.</span><span class="sxs-lookup"><span data-stu-id="182b4-178">However, a caller with SE\_TCB\_NAME [*privilege*](../secgloss/s-gly.md) has the option of specifying the [*logon identifier*](../secgloss/l-gly.md) (LUID) of any existing logon session token to get a handle to that session's credentials.</span></span> <span data-ttu-id="182b4-179">Обычно это используется модулями режима ядра, которые должны действовать от имени вошедшего в систему пользователя.</span><span class="sxs-lookup"><span data-stu-id="182b4-179">Typically, this is used by kernel-mode modules that must act on behalf of a logged-on user.</span></span>

<span data-ttu-id="182b4-180">Пакет может вызвать функцию в *пжеткэйфн* , предоставляемую транспортом времени выполнения RPC.</span><span class="sxs-lookup"><span data-stu-id="182b4-180">A package might call the function in *pGetKeyFn* provided by the RPC run-time transport.</span></span> <span data-ttu-id="182b4-181">Если транспорт не поддерживает понятие обратного вызова для получения учетных данных, этот параметр должен иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="182b4-181">If the transport does not support the notion of callback to retrieve credentials, this parameter must be **NULL**.</span></span>

<span data-ttu-id="182b4-182">Для вызывающих объектов в режиме ядра необходимо отметить следующие отличия.</span><span class="sxs-lookup"><span data-stu-id="182b4-182">For kernel mode callers, the following differences must be noted:</span></span>

-   <span data-ttu-id="182b4-183">Два строковых параметра должны быть строками в [*Юникоде*](../secgloss/u-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="182b4-183">The two string parameters must be [*Unicode*](../secgloss/u-gly.md) strings.</span></span>
-   <span data-ttu-id="182b4-184">Значения буфера должны выделяться в виртуальной памяти процесса, а не в пуле.</span><span class="sxs-lookup"><span data-stu-id="182b4-184">The buffer values must be allocated in process virtual memory, not from the pool.</span></span>

<span data-ttu-id="182b4-185">По завершении использования возвращенных учетных данных освободите память, используемую учетными данными, вызвав функцию [**фрикредентиалшандле**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle) .</span><span class="sxs-lookup"><span data-stu-id="182b4-185">When you have finished using the returned credentials, free the memory used by the credentials by calling the [**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="182b4-186">Требования</span><span class="sxs-lookup"><span data-stu-id="182b4-186">Requirements</span></span>



| <span data-ttu-id="182b4-187">Требование</span><span class="sxs-lookup"><span data-stu-id="182b4-187">Requirement</span></span> | <span data-ttu-id="182b4-188">Значение</span><span class="sxs-lookup"><span data-stu-id="182b4-188">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="182b4-189">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="182b4-189">Minimum supported client</span></span><br/> | <span data-ttu-id="182b4-190">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="182b4-190">Windows XP \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="182b4-191">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="182b4-191">Minimum supported server</span></span><br/> | <span data-ttu-id="182b4-192">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="182b4-192">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="182b4-193">Header</span><span class="sxs-lookup"><span data-stu-id="182b4-193">Header</span></span><br/>                   | <dl> <span data-ttu-id="182b4-194"><dt>SSPI. h (включая Security. h)</dt></span><span class="sxs-lookup"><span data-stu-id="182b4-194"><dt>Sspi.h (include Security.h)</dt></span></span> </dl> |
| <span data-ttu-id="182b4-195">Библиотека</span><span class="sxs-lookup"><span data-stu-id="182b4-195">Library</span></span><br/>                  | <dl> <span data-ttu-id="182b4-196"><dt>Secur32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="182b4-196"><dt>Secur32.lib</dt></span></span> </dl>                 |
| <span data-ttu-id="182b4-197">DLL</span><span class="sxs-lookup"><span data-stu-id="182b4-197">DLL</span></span><br/>                      | <dl> <span data-ttu-id="182b4-198"><dt>Secur32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="182b4-198"><dt>Secur32.dll</dt></span></span> </dl>                 |
| <span data-ttu-id="182b4-199">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="182b4-199">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="182b4-200">**Аккуирекредентиалшандлев** (Юникод) и **аккуирекредентиалшандлеа** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="182b4-200">**AcquireCredentialsHandleW** (Unicode) and **AcquireCredentialsHandleA** (ANSI)</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="182b4-201">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="182b4-201">See also</span></span>

<dl> <dt>

[<span data-ttu-id="182b4-202">**AcceptSecurityContext (Schannel)**</span><span class="sxs-lookup"><span data-stu-id="182b4-202">**AcceptSecurityContext (Schannel)**</span></span>](acceptsecuritycontext--schannel.md)
</dt> <dt>

[<span data-ttu-id="182b4-203">**фрикредентиалшандле**</span><span class="sxs-lookup"><span data-stu-id="182b4-203">**FreeCredentialsHandle**</span></span>](/windows/win32/api/sspi/nf-sspi-freecredentialshandle)
</dt> </dl>

[<span data-ttu-id="182b4-204">**InitializeSecurityContext (Schannel)**</span><span class="sxs-lookup"><span data-stu-id="182b4-204">**InitializeSecurityContext (Schannel)**</span></span>](initializesecuritycontext--schannel.md)
</dt> <dt>

[<span data-ttu-id="182b4-205">**SCH_CREDENTIALS**</span><span class="sxs-lookup"><span data-stu-id="182b4-205">**SCH_CREDENTIALS**</span></span>](/windows/win32/api/schannel/ns-schannel-sch_credentials)
</dt> <dt>

[<span data-ttu-id="182b4-206">**Функции SSPI**</span><span class="sxs-lookup"><span data-stu-id="182b4-206">**SSPI Functions**</span></span>](authentication-functions.md#sspi-functions)
</dt> <dt>
 

 
