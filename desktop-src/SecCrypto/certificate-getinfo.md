---
description: Извлекает сведения из сертификата.
ms.assetid: 57f1c6f9-f06d-4ac7-9070-2a2e6afe93d2
title: 'Метод ICertificate2:: info'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.GetInfo
- ICertificate2.GetInfo
- ICertificate.GetInfo
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 41b3cb6cde796f64ee3a5953ed848d105a10bc5e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665317"
---
# <a name="icertificate2getinfo-method"></a><span data-ttu-id="c3ddd-103">Метод ICertificate2:: info</span><span class="sxs-lookup"><span data-stu-id="c3ddd-103">ICertificate2::GetInfo method</span></span>

<span data-ttu-id="c3ddd-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c3ddd-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="c3ddd-105">Вместо этого используйте [**класс X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="c3ddd-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="c3ddd-106">Метод " **info** " извлекает сведения из [*сертификата*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="c3ddd-106">The **GetInfo** method retrieves information from the [*certificate*](../secgloss/c-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c3ddd-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c3ddd-107">Syntax</span></span>


```VB
Certificate.GetInfo( _
  ByVal InfoType _
)
```



## <a name="parameters"></a><span data-ttu-id="c3ddd-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c3ddd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3ddd-109">*Инфотипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c3ddd-109">*InfoType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3ddd-110">Значение перечисления [**\_ \_ \_ типа CAPICOM CERT info**](capicom-cert-info-type.md) , указывающее тип данных, извлекаемых из сертификата.</span><span class="sxs-lookup"><span data-stu-id="c3ddd-110">A value of the [**CAPICOM\_CERT\_INFO\_TYPE**](capicom-cert-info-type.md) enumeration that specifies what type of data is retrieved from the certificate.</span></span> <span data-ttu-id="c3ddd-111">В следующей таблице приводятся возможные значения.</span><span class="sxs-lookup"><span data-stu-id="c3ddd-111">The following table shows the possible values.</span></span>



| <span data-ttu-id="c3ddd-112">Значение</span><span class="sxs-lookup"><span data-stu-id="c3ddd-112">Value</span></span>                                                                                                                                                                                                                                     | <span data-ttu-id="c3ddd-113">Значение</span><span class="sxs-lookup"><span data-stu-id="c3ddd-113">Meaning</span></span>                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERT_INFO_SUBJECT_SIMPLE_NAME"></span><span id="capicom_cert_info_subject_simple_name"></span><dl> <span data-ttu-id="c3ddd-114"><dt>**\_ \_ \_ имя субъекта сведений об CAPICOM \_ CERT \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c3ddd-114"><dt>**CAPICOM\_CERT\_INFO\_SUBJECT\_SIMPLE\_NAME**</dt></span></span> </dl> | <span data-ttu-id="c3ddd-115">Возвращает отображаемое имя из субъекта сертификата.</span><span class="sxs-lookup"><span data-stu-id="c3ddd-115">Returns the display name from the certificate subject.</span></span><br/>                            |
| <span id="CAPICOM_CERT_INFO_ISSUER_SIMPLE_NAME"></span><span id="capicom_cert_info_issuer_simple_name"></span><dl> <span data-ttu-id="c3ddd-116"><dt>**\_ \_ \_ \_ необычное имя поставщика сведений CAPICOM CERT \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c3ddd-116"><dt>**CAPICOM\_CERT\_INFO\_ISSUER\_SIMPLE\_NAME**</dt></span></span> </dl>    | <span data-ttu-id="c3ddd-117">Возвращает отображаемое имя издателя сертификата.</span><span class="sxs-lookup"><span data-stu-id="c3ddd-117">Returns the display name of the issuer of the certificate.</span></span><br/>                        |
| <span id="CAPICOM_CERT_INFO_SUBJECT_EMAIL_NAME"></span><span id="capicom_cert_info_subject_email_name"></span><dl> <span data-ttu-id="c3ddd-118"><dt>**\_ \_ \_ \_ имя электронной почты субъекта сведений об CAPICOM CERT \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c3ddd-118"><dt>**CAPICOM\_CERT\_INFO\_SUBJECT\_EMAIL\_NAME**</dt></span></span> </dl>    | <span data-ttu-id="c3ddd-119">Возвращает адрес электронной почты субъекта сертификата.</span><span class="sxs-lookup"><span data-stu-id="c3ddd-119">Returns the email address of the certificate subject.</span></span><br/>                             |
| <span id="CAPICOM_CERT_INFO_ISSUER_EMAIL_NAME"></span><span id="capicom_cert_info_issuer_email_name"></span><dl> <span data-ttu-id="c3ddd-120"><dt>**CAPICOM \_ CERT \_ info \_ \_ имя электронной почты поставщика \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c3ddd-120"><dt>**CAPICOM\_CERT\_INFO\_ISSUER\_EMAIL\_NAME**</dt></span></span> </dl>       | <span data-ttu-id="c3ddd-121">Возвращает адрес электронной почты издателя сертификата.</span><span class="sxs-lookup"><span data-stu-id="c3ddd-121">Returns the email address of the issuer of the certificate.</span></span><br/>                       |
| <span id="CAPICOM_CERT_INFO_SUBJECT_UPN"></span><span id="capicom_cert_info_subject_upn"></span><dl> <span data-ttu-id="c3ddd-122"><dt>**CAPICOM \_ \_ сведения о сертификате \_ субъект \_ имени участника-пользователя**</dt></span><span class="sxs-lookup"><span data-stu-id="c3ddd-122"><dt>**CAPICOM\_CERT\_INFO\_SUBJECT\_UPN**</dt></span></span> </dl>                          | <span data-ttu-id="c3ddd-123">Возвращает имя участника-пользователя для субъекта сертификата.</span><span class="sxs-lookup"><span data-stu-id="c3ddd-123">Returns the UPN of the certificate subject.</span></span> <span data-ttu-id="c3ddd-124">Представлено в CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="c3ddd-124">Introduced in CAPICOM 2.0.</span></span><br/>            |
| <span id="CAPICOM_CERT_INFO_ISSUER_UPN"></span><span id="capicom_cert_info_issuer_upn"></span><dl> <span data-ttu-id="c3ddd-125"><dt>**\_ \_ \_ имя участника-пользователя для заверителя сертификата \_ CAPICOM**</dt></span><span class="sxs-lookup"><span data-stu-id="c3ddd-125"><dt>**CAPICOM\_CERT\_INFO\_ISSUER\_UPN**</dt></span></span> </dl>                             | <span data-ttu-id="c3ddd-126">Возвращает имя участника-пользователя (UPN) издателя сертификата.</span><span class="sxs-lookup"><span data-stu-id="c3ddd-126">Returns the UPN of the issuer of the certificate.</span></span> <span data-ttu-id="c3ddd-127">Представлено в CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="c3ddd-127">Introduced in CAPICOM 2.0.</span></span><br/>      |
| <span id="CAPICOM_CERT_INFO_SUBJECT_DNS_NAME"></span><span id="capicom_cert_info_subject_dns_name"></span><dl> <span data-ttu-id="c3ddd-128"><dt>**\_ \_ \_ имя DNS субъекта сведений об \_ CAPICOM CERT \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c3ddd-128"><dt>**CAPICOM\_CERT\_INFO\_SUBJECT\_DNS\_NAME**</dt></span></span> </dl>          | <span data-ttu-id="c3ddd-129">Возвращает DNS-имя субъекта сертификата.</span><span class="sxs-lookup"><span data-stu-id="c3ddd-129">Returns the DNS name of the certificate subject.</span></span> <span data-ttu-id="c3ddd-130">Представлено в CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="c3ddd-130">Introduced in CAPICOM 2.0.</span></span><br/>       |
| <span id="CAPICOM_CERT_INFO_ISSUER_DNS_NAME"></span><span id="capicom_cert_info_issuer_dns_name"></span><dl> <span data-ttu-id="c3ddd-131"><dt>**\_ \_ \_ \_ имя DNS-сервера поставщика сведений CAPICOM CERT \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c3ddd-131"><dt>**CAPICOM\_CERT\_INFO\_ISSUER\_DNS\_NAME**</dt></span></span> </dl>             | <span data-ttu-id="c3ddd-132">Возвращает DNS-имя издателя сертификата.</span><span class="sxs-lookup"><span data-stu-id="c3ddd-132">Returns the DNS name of the issuer of the certificate.</span></span> <span data-ttu-id="c3ddd-133">Представлено в CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="c3ddd-133">Introduced in CAPICOM 2.0.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3ddd-134">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c3ddd-134">Return value</span></span>

<span data-ttu-id="c3ddd-135">Строка, содержащая запрошенные сведения.</span><span class="sxs-lookup"><span data-stu-id="c3ddd-135">A string that contains the requested information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3ddd-136">Требования</span><span class="sxs-lookup"><span data-stu-id="c3ddd-136">Requirements</span></span>



| <span data-ttu-id="c3ddd-137">Требование</span><span class="sxs-lookup"><span data-stu-id="c3ddd-137">Requirement</span></span> | <span data-ttu-id="c3ddd-138">Значение</span><span class="sxs-lookup"><span data-stu-id="c3ddd-138">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c3ddd-139">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="c3ddd-139">End of client support</span></span><br/> | <span data-ttu-id="c3ddd-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c3ddd-140">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="c3ddd-141">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="c3ddd-141">End of server support</span></span><br/> | <span data-ttu-id="c3ddd-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c3ddd-142">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="c3ddd-143">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="c3ddd-143">Redistributable</span></span><br/>       | <span data-ttu-id="c3ddd-144">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="c3ddd-144">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="c3ddd-145">DLL</span><span class="sxs-lookup"><span data-stu-id="c3ddd-145">DLL</span></span><br/>                   | <dl> <span data-ttu-id="c3ddd-146"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c3ddd-146"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3ddd-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c3ddd-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3ddd-148">Криптографические объекты</span><span class="sxs-lookup"><span data-stu-id="c3ddd-148">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="c3ddd-149">**Certificate**</span><span class="sxs-lookup"><span data-stu-id="c3ddd-149">**Certificate**</span></span>](certificate.md)
</dt> </dl>

 

 
