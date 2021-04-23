---
description: Получает пароль учетной записи службы.
ms.assetid: B3D3842F-ACEB-4979-B336-BA3D0143044C
title: Функция Жетсервицеаккаунтпассворд (Secpkg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetServiceAccountPassword
api_type:
- HeaderDef
api_location:
- Secpkg.h
ms.openlocfilehash: 08719fb2b7e4a775df890f20cd640d059cb44475
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683932"
---
# <a name="getserviceaccountpassword-function"></a><span data-ttu-id="1b859-103">Функция Жетсервицеаккаунтпассворд</span><span class="sxs-lookup"><span data-stu-id="1b859-103">GetServiceAccountPassword function</span></span>

<span data-ttu-id="1b859-104">Получает пароль учетной записи службы, доступный для [*поставщиков поддержки безопасности*](/windows/desktop/SecGloss/s-gly) (SSP), таких как Kerberos SSP.</span><span class="sxs-lookup"><span data-stu-id="1b859-104">Retrieves the service account password, available to [*security support providers*](/windows/desktop/SecGloss/s-gly) (SSPs), such as Kerberos SSP.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b859-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1b859-105">Syntax</span></span>


```C++
NTSTATUS NTAPI GetServiceAccountPassword(
  _In_        PUNICODE_STRING AccountName,
  _In_opt_    PUNICODE_STRING DomainName,
  _In_        CRED_FETCH      CredFetch,
  _Inout_opt_ FILETIME        *FileTimeExpiry,
  _Out_       PUNICODE_STRING CurrentPassword,
  _Out_       PUNICODE_STRING PreviousPassword,
  _Out_opt_   FILETIME        *FileTimeCurrPwdValidForOutbound
);
```



## <a name="parameters"></a><span data-ttu-id="1b859-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1b859-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b859-107">*Имя_учетной_записи* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1b859-107">*AccountName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b859-108">Имя учетной записи, заканчивающейся нулем, для учетной записи групповой управляемой учетной записи службы (gMSA).</span><span class="sxs-lookup"><span data-stu-id="1b859-108">Null-terminated account name of the Group Managed Service Account (gMSA) account.</span></span> <span data-ttu-id="1b859-109">Имя пользователя может быть одной из следующих форм:</span><span class="sxs-lookup"><span data-stu-id="1b859-109">The user name can be one of the following forms:</span></span>

-   <span data-ttu-id="1b859-110">Имя учетной записи SAM gMSA.</span><span class="sxs-lookup"><span data-stu-id="1b859-110">SAM account name of the gMSA.</span></span>
-   <span data-ttu-id="1b859-111">Имя пользователя в полном доменном имени (FQDN), например *имя_домена \* **\\** _имя_пользователя_ или **www.** _домен_* _. com \\_ \* _имя_.</span><span class="sxs-lookup"><span data-stu-id="1b859-111">User name in a fully qualified domain name (FQDN), such as *DomainName\***\\**_UserName_ or **www.**_domain_*_.com\\_\*_name_.</span></span> <span data-ttu-id="1b859-112">Имя пользователя должно быть только именем SAM.</span><span class="sxs-lookup"><span data-stu-id="1b859-112">The user name must be a SAM name only.</span></span> <span data-ttu-id="1b859-113">Доменное имя может быть DNS-именем или именем NetBIOS.</span><span class="sxs-lookup"><span data-stu-id="1b859-113">The domain name can be a DNS name or a NetBIOS name.</span></span>
-   <span data-ttu-id="1b859-114">Неявное имя субъекта-пользователя (UPN) для учетной записи gMSA, например *соменаме \* **@** _домен_*_. com_\*, где в соответствии с определением неявного имени участника-пользователя *домен \* \* *. com** — это реальное доменное имя домена.</span><span class="sxs-lookup"><span data-stu-id="1b859-114">Implicit user principal name (UPN) for the gMSA account, for example, *SomeName\***@**_Domain_*_.com_\* where, according to the definition of an implicit UPN, the *Domain\*\*\*.com*\* is the actual domain DNS name.</span></span>

</dd> <dt>

<span data-ttu-id="1b859-115">*Имя_домена* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="1b859-115">*DomainName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1b859-116">Необязательное имя домена, заканчивающееся нулем.</span><span class="sxs-lookup"><span data-stu-id="1b859-116">Optional null-terminated domain name.</span></span> <span data-ttu-id="1b859-117">Это допустимо, только если параметр *AccountName* имеет имя учетной записи SAM.</span><span class="sxs-lookup"><span data-stu-id="1b859-117">This is valid only if the *AccountName* parameter is a SAM account name.</span></span> <span data-ttu-id="1b859-118">Доменное имя может быть только NetBIOS-именем или полным доменным именем (FQDN).</span><span class="sxs-lookup"><span data-stu-id="1b859-118">The domain name can only be a NetBIOS name or a fully qualified domain name (FQDN).</span></span>

</dd> <dt>

<span data-ttu-id="1b859-119">*Кредфетч* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1b859-119">*CredFetch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b859-120">Значение перечисления [**\_ выборки**](cred-fetch.md) , которое указывает, как получить учетные данные.</span><span class="sxs-lookup"><span data-stu-id="1b859-120">A value of the [**CRED\_FETCH**](cred-fetch.md) enumeration that specifies how to retrieve the credential.</span></span>



| <span data-ttu-id="1b859-121">Значение</span><span class="sxs-lookup"><span data-stu-id="1b859-121">Value</span></span>                                                                                                                                                                                                    | <span data-ttu-id="1b859-122">Значение</span><span class="sxs-lookup"><span data-stu-id="1b859-122">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CredFetchDefault"></span><span id="credfetchdefault"></span><span id="CREDFETCHDEFAULT"></span><dl> <span data-ttu-id="1b859-123"><dt>**кредфетчдефаулт**</dt></span><span class="sxs-lookup"><span data-stu-id="1b859-123"><dt>**CredFetchDefault**</dt></span></span> </dl> | <span data-ttu-id="1b859-124">Операционная система сначала пытается получить пароль из локального кэша, если это не время для получения пароля.</span><span class="sxs-lookup"><span data-stu-id="1b859-124">The operating system first attempts to retrieve the password from the local cache if it is not time to fetch the password.</span></span> <span data-ttu-id="1b859-125">Если время получения пароля истекло, операционная система связывается с контроллером домена, в противном случае возвращает все кэшированные пароли со значением status Success.</span><span class="sxs-lookup"><span data-stu-id="1b859-125">If it is time to fetch the password, then the operating system contacts the domain controller, otherwise, return any cached passwords with a status value of success.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="CredFetchDPAPI"></span><span id="credfetchdpapi"></span><span id="CREDFETCHDPAPI"></span><dl> <span data-ttu-id="1b859-126"><dt>**кредфетчдпапи**</dt></span><span class="sxs-lookup"><span data-stu-id="1b859-126"><dt>**CredFetchDPAPI**</dt></span></span> </dl>         | <span data-ttu-id="1b859-127">Возвращает учетные данные локальной DPAPI для вызывающей стороны.</span><span class="sxs-lookup"><span data-stu-id="1b859-127">Returns the local DPAPI credential to the caller.</span></span> <span data-ttu-id="1b859-128">Обычно SSP не требуют использования этого значения.</span><span class="sxs-lookup"><span data-stu-id="1b859-128">SSPs generally would not require use of this value.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="CredFetchForced"></span><span id="credfetchforced"></span><span id="CREDFETCHFORCED"></span><dl> <span data-ttu-id="1b859-129"><dt>**кредфетчфорцед**</dt></span><span class="sxs-lookup"><span data-stu-id="1b859-129"><dt>**CredFetchForced**</dt></span></span> </dl>     | <span data-ttu-id="1b859-130">Заставляет операционную систему попытаться прочитать пароль из контроллера домена.</span><span class="sxs-lookup"><span data-stu-id="1b859-130">Forces the operating system to attempt to read the password from the domain controller.</span></span> <span data-ttu-id="1b859-131">В течение времени смены пароля пароль, возможно, изменился на контроллере домена и на других узлах-членах, но узел участника gMSA распознает пароль так, как если бы он был действителен.</span><span class="sxs-lookup"><span data-stu-id="1b859-131">During the password rollover time, the password may have changed at the domain controller and other member hosts, but the gMSA member host recognizes the password as still valid.</span></span> <span data-ttu-id="1b859-132">Это может произойти из-за проблем с отклонением часов между разными контроллерами домена.</span><span class="sxs-lookup"><span data-stu-id="1b859-132">This can happen due to clock skew issues between different domain controllers.</span></span> <span data-ttu-id="1b859-133">Если указано это значение, операционная система определяет, может ли измениться пароль из-за неравномерного распределения времени, и возвращает пароль.</span><span class="sxs-lookup"><span data-stu-id="1b859-133">When this value is specified, the operating system determines if there could be a possible password change due to clock skew and if so, retrieves the password.</span></span> <span data-ttu-id="1b859-134">В противном случае возвращаются кэшированные учетные данные.</span><span class="sxs-lookup"><span data-stu-id="1b859-134">Otherwise, the cached credential is returned.</span></span> <span data-ttu-id="1b859-135">Если кэшированные учетные данные отсутствуют, операционная система пытается получить его из контроллера домена.</span><span class="sxs-lookup"><span data-stu-id="1b859-135">If there is no cached credential, then the operating system attempts to get one from the domain controller.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="1b859-136">*Филетимикспири* \[ в, out, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="1b859-136">*FileTimeExpiry* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1b859-137">Если это значение не равно NULL и не равно нулю **fileTime**, *филетимикспири* содержит время окончания действия учетных данных учетной записи службы, известное вызывающему объекту.</span><span class="sxs-lookup"><span data-stu-id="1b859-137">On input, if this value is nonnull and is not a zero **FILETIME**, *FileTimeExpiry* contains the expiry time of the service account credentials as known to the caller.</span></span> <span data-ttu-id="1b859-138">Если параметр *филетимикспири* совпадает с одним из текущих учетных данных, этот вызов завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="1b859-138">If the *FileTimeExpiry* parameter is the same as one of the current credentials, this call fails.</span></span> <span data-ttu-id="1b859-139">В выходных данных параметр *филетимикспири* содержит время действия возвращаемых учетных данных.</span><span class="sxs-lookup"><span data-stu-id="1b859-139">On output, the *FileTimeExpiry* parameter contains the expiry time of the credential being returned.</span></span>

</dd> <dt>

<span data-ttu-id="1b859-140">*CurrentPassword* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="1b859-140">*CurrentPassword* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1b859-141">Текущий пароль gMSA.</span><span class="sxs-lookup"><span data-stu-id="1b859-141">The current password of the gMSA.</span></span>

</dd> <dt>

<span data-ttu-id="1b859-142">*Превиауспассворд* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="1b859-142">*PreviousPassword* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1b859-143">Предыдущий пароль gMSA.</span><span class="sxs-lookup"><span data-stu-id="1b859-143">The previous password of the gMSA.</span></span>

</dd> <dt>

<span data-ttu-id="1b859-144">*Филетимекуррпвдвалидфораутбаунд* \[ out, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="1b859-144">*FileTimeCurrPwdValidForOutbound* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1b859-145">Обозначает время, по истечении которого текущий пароль действителен для исходящих запросов.</span><span class="sxs-lookup"><span data-stu-id="1b859-145">Denotes the time after which the current password is valid for outbound requests.</span></span> <span data-ttu-id="1b859-146">Вызывающий объект должен сравнить текущее время с этим значением и использовать текущий пароль, возвращенный только в том случае, если текущее время больше или равно значению, возвращенному этим параметром.</span><span class="sxs-lookup"><span data-stu-id="1b859-146">The caller should compare the current time with this value and use the current password returned only if the current time is greater than or equal to the value returned by this parameter.</span></span> <span data-ttu-id="1b859-147">Использование этого параметра предназначено для вызывающих объектов, которые не имеют повторных попыток в логике исходящего трафика, например NTLM.</span><span class="sxs-lookup"><span data-stu-id="1b859-147">The use of this parameter is designed for callers that do not have retry in the outbound logic, for example, NTLM.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b859-148">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1b859-148">Return value</span></span>

<span data-ttu-id="1b859-149">Если функция завершается успешно, возвращается значение STATUS \_ Success.</span><span class="sxs-lookup"><span data-stu-id="1b859-149">If the function succeeds, the return value is STATUS\_SUCCESS.</span></span>

<span data-ttu-id="1b859-150">Если функция завершается ошибкой, возвращаемое значение является кодом NTSTATUS.</span><span class="sxs-lookup"><span data-stu-id="1b859-150">If the function fails, the return value is an NTSTATUS code.</span></span> <span data-ttu-id="1b859-151">Дополнительные сведения см. в разделе [функция политики LSA: возвращаемые значения](management-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="1b859-151">For more information, see [LSA Policy Function Return Values](management-return-values.md).</span></span>

<span data-ttu-id="1b859-152">Функцию [**лсантстатустовинеррор**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsantstatustowinerror) можно использовать для преобразования кода NTSTATUS в код ошибки Windows.</span><span class="sxs-lookup"><span data-stu-id="1b859-152">You can use the [**LsaNtStatusToWinError**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsantstatustowinerror) function to convert the NTSTATUS code to a Windows error code.</span></span>

<span data-ttu-id="1b859-153">После завершения использования буферов, возвращенных в параметрах *CurrentPassword* и *превиауспассворд* , освободите их, вызвав функцию [**фрилсахеап**](/windows/desktop/api/ntlsa/nc-ntlsa-lsa_free_lsa_heap) .</span><span class="sxs-lookup"><span data-stu-id="1b859-153">When you have finished using the buffers returned in the *CurrentPassword* and *PreviousPassword* parameters, free them by calling the [**FreeLsaHeap**](/windows/desktop/api/ntlsa/nc-ntlsa-lsa_free_lsa_heap) function.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b859-154">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1b859-154">Remarks</span></span>

<span data-ttu-id="1b859-155">Функцию **жетсервицеаккаунтпассворд** можно вызывать в следующих сценариях:</span><span class="sxs-lookup"><span data-stu-id="1b859-155">The **GetServiceAccountPassword** function can be called in the following scenarios:</span></span>

-   <span data-ttu-id="1b859-156">Из функций входа в систему поставщика поддержки безопасности (SSP) поставщик общих служб должен определить, что \_ пароль учетной записи службы \_ используется для входа в сущность и должен проверить наличие у вызывающего пользователя привилегий TCB или сетевой службы.</span><span class="sxs-lookup"><span data-stu-id="1b859-156">From the logon functions of Security Support Providers (SSP), the SSP should detect that the SERVICE\_ACCOUNT\_PASSWORD is being used to log on to the entity and should check that the caller has TCB privilege or is a network service.</span></span> <span data-ttu-id="1b859-157">Затем поставщик общих служб должен разрешить процессу входа в систему, получая последние учетные данные, вызвав функцию **жетсервицеаккаунтпассворд** со значением **кредфетчдефаулт** в перечислении [**\_ выборки**](cred-fetch.md) .</span><span class="sxs-lookup"><span data-stu-id="1b859-157">Then the SSP should allow the log on process to proceed by getting the latest credential by calling the **GetServiceAccountPassword** function with the **CredFetchDefault** value in the [**CRED\_FETCH**](cred-fetch.md) enumeration.</span></span>

-   <span data-ttu-id="1b859-158">От SSP в своих вызовах [**InitializeSecurityContext**](../SecAuthN/initializesecuritycontext--general.md) и [**AcceptSecurityContext**](../SecAuthN/acceptsecuritycontext--general.md) .</span><span class="sxs-lookup"><span data-stu-id="1b859-158">From SSPs in their [**InitializeSecurityContext**](../SecAuthN/initializesecuritycontext--general.md) and [**AcceptSecurityContext**](../SecAuthN/acceptsecuritycontext--general.md) calls.</span></span> <span data-ttu-id="1b859-159">SSP должны определить, что \_ \_ для этих вызовов используется пароль учетной записи службы. Если вызов выполняется для неосновных учетных данных, то поставщик общих служб должен убедиться, что у вызывающего объекта есть права TCB или сетевая служба.</span><span class="sxs-lookup"><span data-stu-id="1b859-159">SSPs should detect that the SERVICE\_ACCOUNT\_PASSWORD is being used for these calls, and if the call is for nonprimary credentials, then the SSP should ensure that the caller has either TCB privilege or is a network service.</span></span> <span data-ttu-id="1b859-160">Затем поставщику общих служб следует вызвать функцию **жетсервицеаккаунтпассворд** со значением **кредфетчдефаулт** в перечислении [**\_ выборки**](cred-fetch.md) и продолжить вызов.</span><span class="sxs-lookup"><span data-stu-id="1b859-160">Then the SSP should call the **GetServiceAccountPassword** function with the **CredFetchDefault** value in the [**CRED\_FETCH**](cred-fetch.md) enumeration and proceed with the call.</span></span> <span data-ttu-id="1b859-161">Если вызовы **InitializeSecurityContext** и **AcceptSecurityContext** вызывают ошибку, то поставщику общих служб следует использовать *филетимикспири* , извлеченный из предыдущего вызова **жетсервицеаккаунтпассворд** , и использовать его в качестве входных данных для вызова **жетсервицеаккаунтпассворд** снова с помощью значения **кредфетчфорцед** в перечислении **\_ выборки** .</span><span class="sxs-lookup"><span data-stu-id="1b859-161">If the **InitializeSecurityContext** and **AcceptSecurityContext** calls fail, then the SSP should use the *FileTimeExpiry* retrieved from the previous call to **GetServiceAccountPassword** and use it as input to calling **GetServiceAccountPassword** again using the **CredFetchForced** value in the **CRED\_FETCH** enumeration.</span></span> <span data-ttu-id="1b859-162">Если доступны новые учетные данные gMSA, второй вызов будет выполнен с новыми учетными данными, после чего поставщик удостоверений должен повторить попытку с новыми учетными данными.</span><span class="sxs-lookup"><span data-stu-id="1b859-162">If a new gMSA credential is available, the second call will succeed with new credentials, and the SSP should then retry with the new credentials.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b859-163">Требования</span><span class="sxs-lookup"><span data-stu-id="1b859-163">Requirements</span></span>



| <span data-ttu-id="1b859-164">Требование</span><span class="sxs-lookup"><span data-stu-id="1b859-164">Requirement</span></span> | <span data-ttu-id="1b859-165">Значение</span><span class="sxs-lookup"><span data-stu-id="1b859-165">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="1b859-166">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1b859-166">Minimum supported client</span></span><br/> | <span data-ttu-id="1b859-167">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="1b859-167">Windows 8 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="1b859-168">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1b859-168">Minimum supported server</span></span><br/> | <span data-ttu-id="1b859-169">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="1b859-169">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="1b859-170">Header</span><span class="sxs-lookup"><span data-stu-id="1b859-170">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b859-171"><dt>Secpkg. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b859-171"><dt>Secpkg.h</dt></span></span> </dl> |



 

