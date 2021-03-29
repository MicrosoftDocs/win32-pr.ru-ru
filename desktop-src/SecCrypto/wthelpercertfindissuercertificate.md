---
description: Находит сертификат издателя из указанных хранилищ сертификатов, который соответствует указанному сертификату субъекта.
ms.assetid: c724f602-fc73-4857-941f-0f22a9e472d1
title: Функция Вселперцертфиндиссуерцертификате
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WTHelperCertFindIssuerCertificate
api_type:
- DllExport
api_location:
- Wintrust.dll
ms.openlocfilehash: 99135ac22509b288726732ca4a16248b304f294b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264676"
---
# <a name="wthelpercertfindissuercertificate-function"></a><span data-ttu-id="e41e3-103">Функция Вселперцертфиндиссуерцертификате</span><span class="sxs-lookup"><span data-stu-id="e41e3-103">WTHelperCertFindIssuerCertificate function</span></span>

<span data-ttu-id="e41e3-104">\[Функция **вселперцертфиндиссуерцертификате** доступна для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="e41e3-104">\[The **WTHelperCertFindIssuerCertificate** function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e41e3-105">В последующих версиях он может быть изменен или недоступен.\]</span><span class="sxs-lookup"><span data-stu-id="e41e3-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="e41e3-106">Функция **вселперцертфиндиссуерцертификате** находит сертификат издателя из указанных хранилищ сертификатов, который соответствует указанному сертификату субъекта.</span><span class="sxs-lookup"><span data-stu-id="e41e3-106">The **WTHelperCertFindIssuerCertificate** function finds an issuer certificate from the specified certificate stores that matches the specified subject certificate.</span></span>

> [!Note]  
> <span data-ttu-id="e41e3-107">Эта функция не имеет связанной библиотеки импорта.</span><span class="sxs-lookup"><span data-stu-id="e41e3-107">This function has no associated import library.</span></span> <span data-ttu-id="e41e3-108">Для динамической привязки к Wintrust.dll необходимо использовать функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="e41e3-108">You must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Wintrust.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="e41e3-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e41e3-109">Syntax</span></span>


```C++
PCCERT_CONTEXT WINAPI WTHelperCertFindIssuerCertificate(
  _In_      PCCERT_CONTEXT pChildContext,
  _In_      DWORD          chStores,
  _In_      HCERTSTORE     *pahStores,
  _In_      FILETIME       *psftVerifyAsOf,
  _In_      DWORD          dwEncoding,
  _Out_opt_ DWORD          *pdwConfidence,
  _Out_     DWORD          *dwError
);
```



## <a name="parameters"></a><span data-ttu-id="e41e3-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="e41e3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e41e3-111">*пчилдконтекст* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e41e3-111">*pChildContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e41e3-112">Сертификат субъекта, для которого необходимо найти соответствующий сертификат издателя.</span><span class="sxs-lookup"><span data-stu-id="e41e3-112">The subject certificate for which to find a matching issuer certificate.</span></span>

</dd> <dt>

<span data-ttu-id="e41e3-113">*чсторес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e41e3-113">*chStores* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e41e3-114">Число элементов в массиве *пахсторес* .</span><span class="sxs-lookup"><span data-stu-id="e41e3-114">The number of elements in the *pahStores* array.</span></span>

</dd> <dt>

<span data-ttu-id="e41e3-115">*пахсторес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e41e3-115">*pahStores* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e41e3-116">Массив хранилищ сертификатов, в котором выполняется поиск.</span><span class="sxs-lookup"><span data-stu-id="e41e3-116">An array of certificate stores in which to search.</span></span>

</dd> <dt>

<span data-ttu-id="e41e3-117">*псфтверифясоф* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e41e3-117">*psftVerifyAsOf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e41e3-118">Время проверки.</span><span class="sxs-lookup"><span data-stu-id="e41e3-118">The time of verification.</span></span>

</dd> <dt>

<span data-ttu-id="e41e3-119">*двенкодинг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e41e3-119">*dwEncoding* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e41e3-120">Значение **типа DWORD** , указывающее типы кодировки проверяемого сертификата.</span><span class="sxs-lookup"><span data-stu-id="e41e3-120">A **DWORD** value that specifies the encoding types of the certificate to check.</span></span> <span data-ttu-id="e41e3-121">Дополнительные сведения о возможных типах кодировок см. в разделе [типы кодирования сертификатов и сообщений](certificate-and-message-encoding-types.md).</span><span class="sxs-lookup"><span data-stu-id="e41e3-121">For information about possible encoding types, see [Certificate and Message Encoding Types](certificate-and-message-encoding-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="e41e3-122">*пдвконфиденце* \[ out, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="e41e3-122">*pdwConfidence* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e41e3-123">Этот параметр может быть побитовой комбинацией из следующих значений достоверности, равных нулю или более.</span><span class="sxs-lookup"><span data-stu-id="e41e3-123">This parameter can be a bitwise combination of zero or more of the following confidence values.</span></span>



| <span data-ttu-id="e41e3-124">Значение</span><span class="sxs-lookup"><span data-stu-id="e41e3-124">Value</span></span>                                                                                                                                                                                                                                                                 | <span data-ttu-id="e41e3-125">Значение</span><span class="sxs-lookup"><span data-stu-id="e41e3-125">Meaning</span></span>                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="CERT_CONFIDENCE_SIG"></span><span id="cert_confidence_sig"></span><dl> <span data-ttu-id="e41e3-126"><dt>**Сертификат \_ \_Подпись достоверности**</dt> <dt> 0x10000000</dt></span><span class="sxs-lookup"><span data-stu-id="e41e3-126"><dt>**CERT\_CONFIDENCE\_SIG**</dt> <dt> 0x10000000</dt></span></span> </dl>                     | <span data-ttu-id="e41e3-127">Подпись сертификата действительна.</span><span class="sxs-lookup"><span data-stu-id="e41e3-127">The signature of the certificate is valid.</span></span><br/>                                           |
| <span id="CERT_CONFIDENCE_TIME"></span><span id="cert_confidence_time"></span><dl> <span data-ttu-id="e41e3-128"><dt>**Сертификат \_ ДОСТОВЕРНОсть \_ времени**</dt> <dt> 0x01000000</dt></span><span class="sxs-lookup"><span data-stu-id="e41e3-128"><dt>**CERT\_CONFIDENCE\_TIME**</dt> <dt> 0x01000000</dt></span></span> </dl>                  | <span data-ttu-id="e41e3-129">Допустимое время издателя сертификата.</span><span class="sxs-lookup"><span data-stu-id="e41e3-129">The time of the certificate issuer is valid.</span></span><br/>                                         |
| <span id="_CERT_CONFIDENCE_TIMENEST"></span><span id="_cert_confidence_timenest"></span><dl> <span data-ttu-id="e41e3-130"><dt> **\_ Достоверность сертификата \_ тименест**</dt> <dt>0x00100000</dt></span><span class="sxs-lookup"><span data-stu-id="e41e3-130"><dt> **CERT\_CONFIDENCE\_TIMENEST**</dt> <dt>0x00100000</dt></span></span> </dl>    | <span data-ttu-id="e41e3-131">Срок действия сертификата действителен.</span><span class="sxs-lookup"><span data-stu-id="e41e3-131">The time of the certificate is valid.</span></span><br/>                                                |
| <span id="_CERT_CONFIDENCE_AUTHIDEXT"></span><span id="_cert_confidence_authidext"></span><dl> <span data-ttu-id="e41e3-132"><dt> **\_ Достоверность сертификата \_ аусидекст**</dt> <dt>0x00010000</dt></span><span class="sxs-lookup"><span data-stu-id="e41e3-132"><dt> **CERT\_CONFIDENCE\_AUTHIDEXT**</dt> <dt>0x00010000</dt></span></span> </dl> | <span data-ttu-id="e41e3-133">Расширение идентификатора центра сертификации является допустимым.</span><span class="sxs-lookup"><span data-stu-id="e41e3-133">The authority ID extension is valid.</span></span><br/>                                                 |
| <span id="_CERT_CONFIDENCE_HYGIENE"></span><span id="_cert_confidence_hygiene"></span><dl> <span data-ttu-id="e41e3-134"><dt> **\_ Достоверность сертификата \_ санации**</dt> <dt>0x00001000</dt></span><span class="sxs-lookup"><span data-stu-id="e41e3-134"><dt> **CERT\_CONFIDENCE\_HYGIENE**</dt> <dt>0x00001000</dt></span></span> </dl>       | <span data-ttu-id="e41e3-135">Как минимум, подпись сертификата и расширения центра сертификации действительна.</span><span class="sxs-lookup"><span data-stu-id="e41e3-135">At a minimum, the signature of the certificate and authority ID extension are valid.</span></span><br/> |
| <span id="_CERT_CONFIDENCE_HIGHEST"></span><span id="_cert_confidence_highest"></span><dl> <span data-ttu-id="e41e3-136"><dt> **\_ Достоверность \_ сертификата — самый**</dt> <dt>0x11111000</dt></span><span class="sxs-lookup"><span data-stu-id="e41e3-136"><dt> **CERT\_CONFIDENCE\_HIGHEST**</dt> <dt>0x11111000</dt></span></span> </dl>       | <span data-ttu-id="e41e3-137">Сочетание всех других значений достоверности.</span><span class="sxs-lookup"><span data-stu-id="e41e3-137">A combination of all of the other confidence values.</span></span><br/>                                 |



 

</dd> <dt>

<span data-ttu-id="e41e3-138">*дверрор* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e41e3-138">*dwError* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e41e3-139">Указатель на переменную **типа DWORD** , которая содержит значение ошибки для этого сертификата, если применимо.</span><span class="sxs-lookup"><span data-stu-id="e41e3-139">A pointer to a **DWORD** variable that contains the error value for this certificate, if applicable.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e41e3-140">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e41e3-140">Return value</span></span>

<span data-ttu-id="e41e3-141">Сертификат издателя, соответствующий сертификату субъекта, указанному параметром *пчилдконтекст* .</span><span class="sxs-lookup"><span data-stu-id="e41e3-141">An issuer certificate that matches the subject certificate specified by the *pChildContext* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="e41e3-142">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e41e3-142">Remarks</span></span>

<span data-ttu-id="e41e3-143">Для успешного поиска соответствующего сертификата издателя должны выполняться следующие требования.</span><span class="sxs-lookup"><span data-stu-id="e41e3-143">To successfully find a matching issuer certificate, the following requirements must be met:</span></span>

-   <span data-ttu-id="e41e3-144">Подпись сертификата субъекта, указанного параметром *пчилдконтекст* , должна быть допустимой.</span><span class="sxs-lookup"><span data-stu-id="e41e3-144">The signature of the subject certificate specified by the *pChildContext* parameter must be valid.</span></span>
-   <span data-ttu-id="e41e3-145">Член **ржекстенсион** элемента **пцертинфо** в параметре *пчилдконтекст* должен содержать структуру [**\_ \_ \_ \_ сведений об идентификаторе ключа центра сертификации**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_authority_key_id_info) .</span><span class="sxs-lookup"><span data-stu-id="e41e3-145">The **rgExtension** member of the **pCertInfo** member of the *pChildContext* parameter must contain a [**CERT\_AUTHORITY\_KEY\_ID\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_authority_key_id_info) structure.</span></span> <span data-ttu-id="e41e3-146">Члены этой структуры, **цертиссуер** и **цертсериалмембер** , значительно соответствуют соответствующим элементам для сертификата издателя.</span><span class="sxs-lookup"><span data-stu-id="e41e3-146">The **CertIssuer** and **CertSerialMember** members of this structure much match the corresponding members for the issuer certificate.</span></span>
-   <span data-ttu-id="e41e3-147">Значение параметра *псфтверифясоф* должно быть в пределах срока действия сертификата субъекта.</span><span class="sxs-lookup"><span data-stu-id="e41e3-147">The value of the *psftVerifyAsOf* parameter must be within the period of validity of the subject certificate.</span></span>
-   <span data-ttu-id="e41e3-148">Срок действия сертификата субъекта должен быть в пределах срока действия сертификата издателя.</span><span class="sxs-lookup"><span data-stu-id="e41e3-148">The period of validity of the subject certificate must be within the period of validity of the issuer certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="e41e3-149">Требования</span><span class="sxs-lookup"><span data-stu-id="e41e3-149">Requirements</span></span>



| <span data-ttu-id="e41e3-150">Требование</span><span class="sxs-lookup"><span data-stu-id="e41e3-150">Requirement</span></span> | <span data-ttu-id="e41e3-151">Значение</span><span class="sxs-lookup"><span data-stu-id="e41e3-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e41e3-152">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e41e3-152">Minimum supported client</span></span><br/> | <span data-ttu-id="e41e3-153">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e41e3-153">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="e41e3-154">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e41e3-154">Minimum supported server</span></span><br/> | <span data-ttu-id="e41e3-155">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e41e3-155">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e41e3-156">DLL</span><span class="sxs-lookup"><span data-stu-id="e41e3-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e41e3-157"><dt>Wintrust.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e41e3-157"><dt>Wintrust.dll</dt></span></span> </dl> |



 

 
