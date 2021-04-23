---
description: API регистрации сертификатов поддерживает следующие атрибуты. Можно создать отдельный атрибут, используя соответствующий интерфейс, определенный в каждом из следующих разделов.
ms.assetid: e14fd472-1974-4ad2-b35a-3ab58ba0d707
title: Поддерживаемые атрибуты
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3bfff5785a0b891e98e6d78d59b4688e2d5c11a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682782"
---
# <a name="supported-attributes"></a><span data-ttu-id="eaeb6-104">Поддерживаемые атрибуты</span><span class="sxs-lookup"><span data-stu-id="eaeb6-104">Supported Attributes</span></span>

<span data-ttu-id="eaeb6-105">API регистрации сертификатов поддерживает следующие атрибуты.</span><span class="sxs-lookup"><span data-stu-id="eaeb6-105">The Certificate Enrollment API supports the following attributes.</span></span> <span data-ttu-id="eaeb6-106">Можно создать отдельный атрибут, используя соответствующий интерфейс, определенный в каждом из следующих разделов.</span><span class="sxs-lookup"><span data-stu-id="eaeb6-106">You can create an individual attribute by using the corresponding interface identified in each of the following sections.</span></span>

## <a name="clientid"></a><span data-ttu-id="eaeb6-107">ClientId</span><span class="sxs-lookup"><span data-stu-id="eaeb6-107">ClientId</span></span>

<span data-ttu-id="eaeb6-108">Интерфейс [**IX509AttributeClientId**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid) можно использовать для определения атрибута, содержащего сведения о клиентском компьютере, который отправил запрос на сертификат.</span><span class="sxs-lookup"><span data-stu-id="eaeb6-108">The [**IX509AttributeClientId**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid) interface can be used to define an attribute that contains information about the client computer that sent the certificate request.</span></span> <span data-ttu-id="eaeb6-109">Эти сведения можно использовать для диагностики.</span><span class="sxs-lookup"><span data-stu-id="eaeb6-109">The information can be used for diagnostics.</span></span>

<span data-ttu-id="eaeb6-110">**Применимо к:** \#Запрос PKCS 10 или CMC.</span><span class="sxs-lookup"><span data-stu-id="eaeb6-110">**Applies To:** PKCS \#10 or CMC request.</span></span>

<span data-ttu-id="eaeb6-111">**Идентификатор объекта:** \_ \_ \_ Сведения о клиенте запроса OID кскн \_ (1.3.6.1.4.1.311.21.20)</span><span class="sxs-lookup"><span data-stu-id="eaeb6-111">**OID:** XCN\_OID\_REQUEST\_CLIENT\_INFO (1.3.6.1.4.1.311.21.20)</span></span>

## <a name="extensions"></a><span data-ttu-id="eaeb6-112">Модули</span><span class="sxs-lookup"><span data-stu-id="eaeb6-112">Extensions</span></span>

<span data-ttu-id="eaeb6-113">Интерфейс [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) можно использовать для определения набора расширений сертификатов X. 509 версии 3.</span><span class="sxs-lookup"><span data-stu-id="eaeb6-113">The [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) interface can be used to define a set of X.509 version 3 certificate extensions.</span></span> <span data-ttu-id="eaeb6-114">Поддерживаются следующие расширения.</span><span class="sxs-lookup"><span data-stu-id="eaeb6-114">The following extensions are supported.</span></span> <span data-ttu-id="eaeb6-115">Дополнительные сведения см. в разделе интерфейсы расширений.</span><span class="sxs-lookup"><span data-stu-id="eaeb6-115">For more information, see the Extension Interfaces topic.</span></span>



| <span data-ttu-id="eaeb6-116">Расширение</span><span class="sxs-lookup"><span data-stu-id="eaeb6-116">Extension</span></span>              | <span data-ttu-id="eaeb6-117">Описание</span><span class="sxs-lookup"><span data-stu-id="eaeb6-117">Description</span></span>                                                                                                                                                                                                                      |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eaeb6-118">алтернативенамес</span><span class="sxs-lookup"><span data-stu-id="eaeb6-118">AlternativeNames</span></span>       | <span data-ttu-id="eaeb6-119">Содержит одну или несколько альтернативных форм имени издателя, связанного с сертификатом.</span><span class="sxs-lookup"><span data-stu-id="eaeb6-119">Contains one or more alternative name forms of the issuer associated with the certificate.</span></span>                                                                                                                                       |
| <span data-ttu-id="eaeb6-120">аусоритикэйидентифиер</span><span class="sxs-lookup"><span data-stu-id="eaeb6-120">AuthorityKeyIdentifier</span></span> | <span data-ttu-id="eaeb6-121">Содержит уникальный идентификатор ключа для различения нескольких ключей подписи сертификатов в [*центре сертификации*](/windows/desktop/SecGloss/c-gly) (ЦС).</span><span class="sxs-lookup"><span data-stu-id="eaeb6-121">Contains a unique key identifier to differentiate between multiple certificate signing keys of the [*certification authority*](/windows/desktop/SecGloss/c-gly) (CA).</span></span> |
| <span data-ttu-id="eaeb6-122">басикконстраинтс</span><span class="sxs-lookup"><span data-stu-id="eaeb6-122">BasicConstraints</span></span>       | <span data-ttu-id="eaeb6-123">Указывает, может ли субъект действовать как ЦС.</span><span class="sxs-lookup"><span data-stu-id="eaeb6-123">Indicates whether the subject can act as a CA.</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="eaeb6-124">цертификатеполиЦиес</span><span class="sxs-lookup"><span data-stu-id="eaeb6-124">CertificatePolicies</span></span>    | <span data-ttu-id="eaeb6-125">Определяет политики и сведения о необязательном квалификаторе, связанные с сертификатом.</span><span class="sxs-lookup"><span data-stu-id="eaeb6-125">Identifies the policies and optional qualifier information associated with the certificate.</span></span>                                                                                                                                      |
| <span data-ttu-id="eaeb6-126">мсаппликатионполиЦиес</span><span class="sxs-lookup"><span data-stu-id="eaeb6-126">MSApplicationPolicies</span></span>  | <span data-ttu-id="eaeb6-127">Определяет одно или несколько применений сертификата.</span><span class="sxs-lookup"><span data-stu-id="eaeb6-127">Identifies one or more uses for the certificate.</span></span> <span data-ttu-id="eaeb6-128">Это расширение похоже на расширение Енханцедкэйусаже, но определено корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="eaeb6-128">This extension is similar to the EnhancedKeyUsage extension but is Microsoft-defined.</span></span>                                                                                           |
| <span data-ttu-id="eaeb6-129">енханцедкэйусаже</span><span class="sxs-lookup"><span data-stu-id="eaeb6-129">EnhancedKeyUsage</span></span>       | <span data-ttu-id="eaeb6-130">Определяет одно или несколько применений открытого ключа, содержащегося в сертификате.</span><span class="sxs-lookup"><span data-stu-id="eaeb6-130">Identifies one or more uses of the public key contained in the certificate.</span></span> <span data-ttu-id="eaeb6-131">Расширение расширенного использования ключа можно использовать в дополнение к расширению использования ключа или вместо него.</span><span class="sxs-lookup"><span data-stu-id="eaeb6-131">The enhanced key usage extension can be used in addition to or in place of the key usage extension.</span></span>                                                  |
| <span data-ttu-id="eaeb6-132">кэйусаже</span><span class="sxs-lookup"><span data-stu-id="eaeb6-132">KeyUsage</span></span>               | <span data-ttu-id="eaeb6-133">Определяет ограничения на операции, которые могут быть выполнены с помощью открытого ключа, содержащегося в сертификате.</span><span class="sxs-lookup"><span data-stu-id="eaeb6-133">Identifies restrictions on the operations that can be performed by the public key contained in the certificate.</span></span>                                                                                                                  |
| <span data-ttu-id="eaeb6-134">смимекапабилитиес</span><span class="sxs-lookup"><span data-stu-id="eaeb6-134">SmimeCapabilities</span></span>      | <span data-ttu-id="eaeb6-135">Сообщает о возможностях расшифровки получателя сообщения электронной почты, чтобы предоставить отправителю возможность выбора наиболее безопасного симметричного алгоритма, поддерживаемого обеими сторонами.</span><span class="sxs-lookup"><span data-stu-id="eaeb6-135">Reports the decryption capabilities of an email recipient to the email sender to enable the sender to choose the most secure symmetric algorithm supported by both parties.</span></span>                                                      |
| <span data-ttu-id="eaeb6-136">SubjectKeyIdentifier</span><span class="sxs-lookup"><span data-stu-id="eaeb6-136">SubjectKeyIdentifier</span></span>   | <span data-ttu-id="eaeb6-137">Содержит уникальный идентификатор ключа, который можно использовать для различения нескольких ключей подписывания, связанных с владельцем сертификата.</span><span class="sxs-lookup"><span data-stu-id="eaeb6-137">Contains a unique key identifier that can be used to differentiate between multiple signing keys associated with the certificate owner.</span></span>                                                                                          |
| <span data-ttu-id="eaeb6-138">Шаблон</span><span class="sxs-lookup"><span data-stu-id="eaeb6-138">Template</span></span>               | <span data-ttu-id="eaeb6-139">Определяет шаблон, используемый при выдаче или обновлении сертификата.</span><span class="sxs-lookup"><span data-stu-id="eaeb6-139">Identifies the template to use when issuing or renewing a certificate.</span></span> <span data-ttu-id="eaeb6-140">Расширение содержит идентификатор объекта (OID) шаблона.</span><span class="sxs-lookup"><span data-stu-id="eaeb6-140">The extension contains the object identifier (OID) of the template.</span></span>                                                                                       |
| <span data-ttu-id="eaeb6-141">TemplateName</span><span class="sxs-lookup"><span data-stu-id="eaeb6-141">TemplateName</span></span>           | <span data-ttu-id="eaeb6-142">Определяет шаблон, используемый при выдаче или обновлении сертификата.</span><span class="sxs-lookup"><span data-stu-id="eaeb6-142">Identifies the template to use when issuing or renewing a certificate.</span></span> <span data-ttu-id="eaeb6-143">Расширение содержит имя шаблона.</span><span class="sxs-lookup"><span data-stu-id="eaeb6-143">The extension contains the name of the template.</span></span>                                                                                                          |



 

<span data-ttu-id="eaeb6-144">**Применимо к:** \#Запрос PKCS 10.</span><span class="sxs-lookup"><span data-stu-id="eaeb6-144">**Applies To:** PKCS \#10 request.</span></span>

<span data-ttu-id="eaeb6-145">**Идентификатор объекта:** КСКН \_ OID \_ RSA \_ цертекстенсионс (1.2.840.113549.1.9.14)</span><span class="sxs-lookup"><span data-stu-id="eaeb6-145">**OID:** XCN\_OID\_RSA\_certExtensions (1.2.840.113549.1.9.14)</span></span>

## <a name="archivekey"></a><span data-ttu-id="eaeb6-146">арчивекэй</span><span class="sxs-lookup"><span data-stu-id="eaeb6-146">ArchiveKey</span></span>

<span data-ttu-id="eaeb6-147">Интерфейс [**IX509AttributeArchiveKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekey) можно использовать для определения атрибута, содержащего зашифрованный закрытый ключ, отправленный в ЦС для архивирования.</span><span class="sxs-lookup"><span data-stu-id="eaeb6-147">The [**IX509AttributeArchiveKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekey) interface can be used to define an attribute that contains an encrypted private key submitted to a CA for archiving.</span></span>

<span data-ttu-id="eaeb6-148">**Применимо к:** Запрос CMC.</span><span class="sxs-lookup"><span data-stu-id="eaeb6-148">**Applies To:** CMC request.</span></span>

<span data-ttu-id="eaeb6-149">**Идентификатор объекта:** Атрибут \_ ключевого атрибута кскн OID \_ \_ \_ (1.3.6.1.4.1.311.21.13)</span><span class="sxs-lookup"><span data-stu-id="eaeb6-149">**OID:** XCN\_OID\_ARCHIVED\_KEY\_ATTR (1.3.6.1.4.1.311.21.13)</span></span>

## <a name="archivekeyhash"></a><span data-ttu-id="eaeb6-150">арчивекэйхаш</span><span class="sxs-lookup"><span data-stu-id="eaeb6-150">ArchiveKeyHash</span></span>

<span data-ttu-id="eaeb6-151">Интерфейс [**IX509AttributeArchiveKeyHash**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekeyhash) можно использовать для определения хэша закрытого ключа, содержащегося в атрибуте **арчивекэй** .</span><span class="sxs-lookup"><span data-stu-id="eaeb6-151">The [**IX509AttributeArchiveKeyHash**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekeyhash) interface can be used to define a hash of the private key contained in the **ArchiveKey** attribute.</span></span>

<span data-ttu-id="eaeb6-152">**Применимо к:** Запрос CMC.</span><span class="sxs-lookup"><span data-stu-id="eaeb6-152">**Applies To:** CMC request.</span></span>

<span data-ttu-id="eaeb6-153">**Идентификатор объекта:** \_ \_ Хэш зашифрованного \_ ключа кскн OID \_ (1.3.6.1.4.1.311.21.21)</span><span class="sxs-lookup"><span data-stu-id="eaeb6-153">**OID:** XCN\_OID\_ENCRYPTED\_KEY\_HASH (1.3.6.1.4.1.311.21.21)</span></span>

## <a name="cspprovider"></a><span data-ttu-id="eaeb6-154">ксппровидер</span><span class="sxs-lookup"><span data-stu-id="eaeb6-154">CspProvider</span></span>

<span data-ttu-id="eaeb6-155">Интерфейс [**IX509AttributeCspProvider**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributecspprovider) можно использовать для определения атрибута, который содержит сведения о [*поставщике служб шифрования*](/windows/desktop/SecGloss/c-gly) (CSP), используемом инициатором запроса для криптографических операций.</span><span class="sxs-lookup"><span data-stu-id="eaeb6-155">The [**IX509AttributeCspProvider**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributecspprovider) interface can be used to define an attribute that contains information about the [*cryptographic service provider*](/windows/desktop/SecGloss/c-gly) (CSP) used by the requester for cryptographic operations.</span></span>

<span data-ttu-id="eaeb6-156">**Применимо к:** \#Запрос PKCS 10.</span><span class="sxs-lookup"><span data-stu-id="eaeb6-156">**Applies To:** PKCS \#10 request.</span></span> <span data-ttu-id="eaeb6-157">Этот атрибут создается автоматически при создании объекта [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) .</span><span class="sxs-lookup"><span data-stu-id="eaeb6-157">This attribute is automatically created when you create an [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) object.</span></span>

<span data-ttu-id="eaeb6-158">**Идентификатор объекта:** \_ \_ Поставщик CSP регистрации кскн \_ OID \_ (1.3.6.1.4.1.311.13.2.2)</span><span class="sxs-lookup"><span data-stu-id="eaeb6-158">**OID:** XCN\_OID\_ENROLLMENT\_CSP\_PROVIDER (1.3.6.1.4.1.311.13.2.2)</span></span>

## <a name="osversion"></a><span data-ttu-id="eaeb6-159">OSVersion</span><span class="sxs-lookup"><span data-stu-id="eaeb6-159">OSVersion</span></span>

<span data-ttu-id="eaeb6-160">Интерфейс [**IX509AttributeOSVersion**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeosversion) можно использовать для создания атрибута, содержащего сведения о версии клиентской операционной системы.</span><span class="sxs-lookup"><span data-stu-id="eaeb6-160">The [**IX509AttributeOSVersion**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeosversion) interface can be used to create an attribute that contains version information about the client operating system.</span></span> <span data-ttu-id="eaeb6-161">Эти сведения могут использоваться ЦС для определения типа обработки, применяемой при создании сертификата.</span><span class="sxs-lookup"><span data-stu-id="eaeb6-161">The information can be used by the CA to determine the type of processing to apply when creating the certificate.</span></span>

<span data-ttu-id="eaeb6-162">**Применимо к:** \#Запрос PKCS 10 или CMC.</span><span class="sxs-lookup"><span data-stu-id="eaeb6-162">**Applies To:** PKCS \#10 or CMC request.</span></span>

<span data-ttu-id="eaeb6-163">**Идентификатор объекта:** \_ \_ Версия ОС OID кскн \_ (1.3.6.1.4.1.311.13.2.3)</span><span class="sxs-lookup"><span data-stu-id="eaeb6-163">**OID:** XCN\_OID\_OS\_VERSION (1.3.6.1.4.1.311.13.2.3)</span></span>

## <a name="renewalcertificate"></a><span data-ttu-id="eaeb6-164">реневалцертификате</span><span class="sxs-lookup"><span data-stu-id="eaeb6-164">RenewalCertificate</span></span>

<span data-ttu-id="eaeb6-165">Интерфейс [**IX509AttributeRenewalCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributerenewalcertificate) можно использовать для создания атрибута, содержащего обновляемый сертификат.</span><span class="sxs-lookup"><span data-stu-id="eaeb6-165">The [**IX509AttributeRenewalCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributerenewalcertificate) interface can be used to create an attribute that contains the certificate being renewed.</span></span>

<span data-ttu-id="eaeb6-166">**Применимо к:** \#Запрос PKCS 10.</span><span class="sxs-lookup"><span data-stu-id="eaeb6-166">**Applies To:** PKCS \#10 request.</span></span> <span data-ttu-id="eaeb6-167">Этот атрибут создается автоматически, если вы создаете \# запрос PKCS 10, инициируя его с помощью возобновляемого сертификата.</span><span class="sxs-lookup"><span data-stu-id="eaeb6-167">This attribute is automatically created if you create a PKCS \#10 request by initiating it with the certificate being renewed.</span></span>

<span data-ttu-id="eaeb6-168">**Идентификатор объекта:** \_ \_ Сертификат продления OID кскн \_ (1.3.6.1.4.1.311.13.1)</span><span class="sxs-lookup"><span data-stu-id="eaeb6-168">**OID:** XCN\_OID\_RENEWAL\_CERTIFICATE (1.3.6.1.4.1.311.13.1)</span></span>

 

 
