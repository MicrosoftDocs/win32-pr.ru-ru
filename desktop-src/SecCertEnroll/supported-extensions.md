---
description: Для определения произвольного расширения можно использовать интерфейс IX509Extension.
ms.assetid: 025447f4-98d0-4cb8-b546-4797b7e60722
title: Поддерживаемые расширения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd55886b03cdea5783f918182c84382910510918
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810271"
---
# <a name="supported-extensions"></a><span data-ttu-id="f6721-103">Поддерживаемые расширения</span><span class="sxs-lookup"><span data-stu-id="f6721-103">Supported Extensions</span></span>

<span data-ttu-id="f6721-104">Для определения произвольного расширения можно использовать интерфейс [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) .</span><span class="sxs-lookup"><span data-stu-id="f6721-104">You can use the [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) interface to define an arbitrary extension.</span></span> <span data-ttu-id="f6721-105">API регистрации сертификатов также предоставляет интерфейсы, производные от **IX509Extension** , что позволяет легко создавать любые из наиболее распространенных расширений.</span><span class="sxs-lookup"><span data-stu-id="f6721-105">The Certificate Enrollment API also provides interfaces derived from **IX509Extension** to enable you to easily create any of the most common extensions.</span></span> <span data-ttu-id="f6721-106">В следующем списке перечислены общие расширения, поддерживаемые центрами сертификации Майкрософт, а также идентификаторы объектов и интерфейсы, которые можно использовать для их создания.</span><span class="sxs-lookup"><span data-stu-id="f6721-106">The following list identifies the common extensions supported by Microsoft certification authorities, and the object identifiers and interfaces that you can use to create them.</span></span>

## <a name="alternativenames"></a><span data-ttu-id="f6721-107">алтернативенамес</span><span class="sxs-lookup"><span data-stu-id="f6721-107">AlternativeNames</span></span>

<span data-ttu-id="f6721-108">Расширение альтернативных имен можно использовать для определения одной или нескольких альтернативных форм имен для субъекта запроса на сертификат.</span><span class="sxs-lookup"><span data-stu-id="f6721-108">The alternative names extension can be used to define one or more alternative name forms for the subject of the certificate request.</span></span> <span data-ttu-id="f6721-109">Примеры дополнительных форм могут включать адреса электронной почты, DNS-имена, IP-адреса и URI.</span><span class="sxs-lookup"><span data-stu-id="f6721-109">Example alternative forms include email addresses, DNS names, IP addresses, and URIs.</span></span>

<span data-ttu-id="f6721-110">**Интерфейс:** [ **IX509ExtensionAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionalternativenames)</span><span class="sxs-lookup"><span data-stu-id="f6721-110">**Interface:** [**IX509ExtensionAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionalternativenames)</span></span>

<span data-ttu-id="f6721-111">**Идентификатор объекта:** КСКН \_ OID \_ субъекта \_ Alt \_ имя2 (2.5.29.17)</span><span class="sxs-lookup"><span data-stu-id="f6721-111">**OID:** XCN\_OID\_SUBJECT\_ALT\_NAME2 (2.5.29.17)</span></span>

## <a name="authorityinformationaccess"></a><span data-ttu-id="f6721-112">аусоритинформатионакцесс</span><span class="sxs-lookup"><span data-stu-id="f6721-112">AuthorityInformationAccess</span></span>

<span data-ttu-id="f6721-113">Расширение доступа к информации о центрах сертификации определяет, как получить доступ к информации и службам ЦС.</span><span class="sxs-lookup"><span data-stu-id="f6721-113">The authority information access extension identifies how to access CA information and services.</span></span> <span data-ttu-id="f6721-114">Значение расширения содержит последовательность URI.</span><span class="sxs-lookup"><span data-stu-id="f6721-114">The extension value contains a sequence of URIs.</span></span>

<span data-ttu-id="f6721-115">**Интерфейс:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span><span class="sxs-lookup"><span data-stu-id="f6721-115">**Interface:** [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span></span>

<span data-ttu-id="f6721-116">**Идентификатор объекта:** \_ \_ \_ Доступ к сведениям о центре OID кскн \_ (1.3.6.1.5.5.7.1.1)</span><span class="sxs-lookup"><span data-stu-id="f6721-116">**OID:** XCN\_OID\_AUTHORITY\_INFO\_ACCESS (1.3.6.1.5.5.7.1.1)</span></span>

## <a name="authoritykeyidentifier"></a><span data-ttu-id="f6721-117">аусоритикэйидентифиер</span><span class="sxs-lookup"><span data-stu-id="f6721-117">AuthorityKeyIdentifier</span></span>

<span data-ttu-id="f6721-118">Расширение идентификатора ключа центра сертификации позволяет идентифицировать открытый ключ ЦС, соответствующий закрытому ключу ЦС, который подписал выданный сертификат.</span><span class="sxs-lookup"><span data-stu-id="f6721-118">The authority key identifier extension enables identification of the CA public key that corresponds to the CA private key that signed an issued certificate.</span></span> <span data-ttu-id="f6721-119">Он используется путем создания программного обеспечения на сервере Windows Server для поиска сертификата ЦС.</span><span class="sxs-lookup"><span data-stu-id="f6721-119">It is used by certificate path building software on a Windows server to find the CA certificate.</span></span> <span data-ttu-id="f6721-120">Когда ЦС выдает сертификат, значение расширения устанавливается равным расширению **субжекткэйидентифиер** в сертификате подписи ЦС.</span><span class="sxs-lookup"><span data-stu-id="f6721-120">When a CA issues a certificate, the extension value is set equal to the **SubjectKeyIdentifier** extension in the CA signing certificate.</span></span> <span data-ttu-id="f6721-121">Значение обычно представляет собой хэш SHA-1 открытого ключа.</span><span class="sxs-lookup"><span data-stu-id="f6721-121">The value is typically a SHA-1 hash of the public key.</span></span>

<span data-ttu-id="f6721-122">**Интерфейс:** [ **IX509ExtensionAuthorityKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionauthoritykeyidentifier)</span><span class="sxs-lookup"><span data-stu-id="f6721-122">**Interface:** [**IX509ExtensionAuthorityKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionauthoritykeyidentifier)</span></span>

<span data-ttu-id="f6721-123">**Идентификатор объекта:** КСКН \_ \_ \_ ключ идентификатор2 центра OID \_ (2.5.29.35)</span><span class="sxs-lookup"><span data-stu-id="f6721-123">**OID:** XCN\_OID\_AUTHORITY\_KEY\_IDENTIFIER2 (2.5.29.35)</span></span>

## <a name="basicconstraints"></a><span data-ttu-id="f6721-124">басикконстраинтс</span><span class="sxs-lookup"><span data-stu-id="f6721-124">BasicConstraints</span></span>

<span data-ttu-id="f6721-125">Расширение основных ограничений можно использовать для того, чтобы определить, может ли сущность использоваться в качестве центра сертификации (CA), и, если это так, количество подчиненных ЦС, которые могут существовать под ним в цепочке сертификатов.</span><span class="sxs-lookup"><span data-stu-id="f6721-125">The basic constraints extension can be used to identify whether the entity can be used as a certification authority (CA) and, if so, the number of subordinate CAs that can exist beneath it in the certificate chain.</span></span>

<span data-ttu-id="f6721-126">**Интерфейс:** [ **IX509ExtensionBasicConstraints**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionbasicconstraints)</span><span class="sxs-lookup"><span data-stu-id="f6721-126">**Interface:** [**IX509ExtensionBasicConstraints**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionbasicconstraints)</span></span>

<span data-ttu-id="f6721-127">**Идентификатор объекта:** КСКН \_ OID \_ Basic \_ CONSTRAINTS2 (2.5.29.19)</span><span class="sxs-lookup"><span data-stu-id="f6721-127">**OID:** XCN\_OID\_BASIC\_CONSTRAINTS2 (2.5.29.19)</span></span>

## <a name="certificatepolicies"></a><span data-ttu-id="f6721-128">цертификатеполиЦиес</span><span class="sxs-lookup"><span data-stu-id="f6721-128">CertificatePolicies</span></span>

<span data-ttu-id="f6721-129">Расширение политик сертификатов можно использовать для идентификации политик, в которых был выдан сертификат, и для него можно использовать его цели.</span><span class="sxs-lookup"><span data-stu-id="f6721-129">The certificate policies extension can be used to identify the policies under which the certificate has been issued and the purposes for it can be used.</span></span> <span data-ttu-id="f6721-130">Они определяются коллекцией идентификаторов объектов (OID).</span><span class="sxs-lookup"><span data-stu-id="f6721-130">These are identified by a collection of object identifiers (OIDs).</span></span> <span data-ttu-id="f6721-131">Политики настраиваются для требований Организации.</span><span class="sxs-lookup"><span data-stu-id="f6721-131">Policies are customized for the requirements of an organization.</span></span>

<span data-ttu-id="f6721-132">**Интерфейс:** [ **IX509ExtensionCertificatePolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensioncertificatepolicies)</span><span class="sxs-lookup"><span data-stu-id="f6721-132">**Interface:** [**IX509ExtensionCertificatePolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensioncertificatepolicies)</span></span>

<span data-ttu-id="f6721-133">**Идентификатор объекта:** \_ \_ Политики сертификата кскн OID \_ (2.5.29.32)</span><span class="sxs-lookup"><span data-stu-id="f6721-133">**OID:** XCN\_OID\_CERT\_POLICIES (2.5.29.32)</span></span>

## <a name="crldistributionpoints"></a><span data-ttu-id="f6721-134">крлдистрибутионпоинтс</span><span class="sxs-lookup"><span data-stu-id="f6721-134">CrlDistributionPoints</span></span>

<span data-ttu-id="f6721-135">Расширение точек распространения списка отзыва сертификатов (CRL) содержит URI базового списка отзыва сертификатов (CRL).</span><span class="sxs-lookup"><span data-stu-id="f6721-135">The certificate revocation list (CRL) distribution points extension contains the URI of the base certificate revocation list (CRL).</span></span>

<span data-ttu-id="f6721-136">**Интерфейс:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span><span class="sxs-lookup"><span data-stu-id="f6721-136">**Interface:** [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span></span>

<span data-ttu-id="f6721-137">**Идентификатор объекта:** Точки распространения CRL для КСКН \_ OID \_ \_ \_ (2.5.29.31)</span><span class="sxs-lookup"><span data-stu-id="f6721-137">**OID:** XCN\_OID\_CRL\_DIST\_POINTS (2.5.29.31)</span></span>

## <a name="enhancedkeyusage"></a><span data-ttu-id="f6721-138">енханцедкэйусаже</span><span class="sxs-lookup"><span data-stu-id="f6721-138">EnhancedKeyUsage</span></span>

<span data-ttu-id="f6721-139">Расширение расширенного использования ключа можно использовать для определения одного или нескольких применений открытого ключа, содержащегося в сертификате.</span><span class="sxs-lookup"><span data-stu-id="f6721-139">The enhanced key usage extension can be used to define one or more uses of the public key contained in the certificate.</span></span>

<span data-ttu-id="f6721-140">**Интерфейс:** [ **IX509ExtensionEnhancedKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage)</span><span class="sxs-lookup"><span data-stu-id="f6721-140">**Interface:** [**IX509ExtensionEnhancedKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage)</span></span>

<span data-ttu-id="f6721-141">**Идентификатор объекта:** \_ \_ Расширенное \_ Использование ключа кскн OID \_ (2.5.29.37)</span><span class="sxs-lookup"><span data-stu-id="f6721-141">**OID:** XCN\_OID\_ENHANCED\_KEY\_USAGE (2.5.29.37)</span></span>

## <a name="freshestcrl"></a><span data-ttu-id="f6721-142">фрешесткрл</span><span class="sxs-lookup"><span data-stu-id="f6721-142">FreshestCRL</span></span>

<span data-ttu-id="f6721-143">Самое свежее расширение списка отзыва сертификатов содержит URI разностного CRL.</span><span class="sxs-lookup"><span data-stu-id="f6721-143">The freshest CRL extension contains the URI of the delta CRL.</span></span> <span data-ttu-id="f6721-144">Для этого расширения и расширения **крлдистрибутионпоинтс** используется один и тот же синтаксис ASN. 1.</span><span class="sxs-lookup"><span data-stu-id="f6721-144">The same ASN.1 syntax is used for this extension and the **CrlDistributionPoints** extension.</span></span>

<span data-ttu-id="f6721-145">**Интерфейс:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span><span class="sxs-lookup"><span data-stu-id="f6721-145">**Interface:** [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span></span>

<span data-ttu-id="f6721-146">**Идентификатор объекта:** \_ \_ Актуальный CRL кскн \_ OID (2.5.29.46)</span><span class="sxs-lookup"><span data-stu-id="f6721-146">**OID:** XCN\_OID\_FRESHEST\_CRL (2.5.29.46)</span></span>

## <a name="keyusage"></a><span data-ttu-id="f6721-147">кэйусаже</span><span class="sxs-lookup"><span data-stu-id="f6721-147">KeyUsage</span></span>

<span data-ttu-id="f6721-148">Расширение использования ключа можно использовать для определения ограничений на операции, которые могут быть выполнены с помощью открытого ключа, содержащегося в сертификате.</span><span class="sxs-lookup"><span data-stu-id="f6721-148">The key usage extension can be used to define restrictions on the operations that can be performed by the public key contained in the certificate.</span></span> <span data-ttu-id="f6721-149">Например, можно указать, что открытый ключ должен использоваться только для создания цифровой подписи, подписывания списка отзыва сертификатов (CRL) или шифрования другого ключа.</span><span class="sxs-lookup"><span data-stu-id="f6721-149">For example, you can specify that the public key be used only to create a digital signature, sign a certificate revocation list (CRL), or encrypt another key.</span></span>

<span data-ttu-id="f6721-150">**Интерфейс:** [ **IX509ExtensionKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionkeyusage)</span><span class="sxs-lookup"><span data-stu-id="f6721-150">**Interface:** [**IX509ExtensionKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionkeyusage)</span></span>

<span data-ttu-id="f6721-151">**Идентификатор объекта:** \_ \_ Использование ключа OID кскн \_ (2.5.29.15)</span><span class="sxs-lookup"><span data-stu-id="f6721-151">**OID:** XCN\_OID\_KEY\_USAGE (2.5.29.15)</span></span>

## <a name="msapplicationpolicies"></a><span data-ttu-id="f6721-152">мсаппликатионполиЦиес</span><span class="sxs-lookup"><span data-stu-id="f6721-152">MSApplicationPolicies</span></span>

<span data-ttu-id="f6721-153">Расширение политик приложений Майкрософт может использоваться приложением для фильтрации сертификатов на основе разрешенного использования.</span><span class="sxs-lookup"><span data-stu-id="f6721-153">The Microsoft application policies extension can be used by an application to filter certificates on the basis of permitted use.</span></span> <span data-ttu-id="f6721-154">Разрешенные варианты использования идентифицируются по OID.</span><span class="sxs-lookup"><span data-stu-id="f6721-154">Permitted uses are identified by OIDs.</span></span> <span data-ttu-id="f6721-155">Это расширение похоже на расширение **енханцедкэйусаже** , но с более тщательной семантикой, примененной к родительскому ЦС.</span><span class="sxs-lookup"><span data-stu-id="f6721-155">This extension is similar to the **EnhancedKeyUsage** extension but with stricter semantics applied to the parent CA.</span></span> <span data-ttu-id="f6721-156">Расширение зависит от корпорации Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="f6721-156">The extension is Microsoft specific.</span></span>

<span data-ttu-id="f6721-157">**Интерфейс:** [ **IX509ExtensionMSApplicationPolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionmsapplicationpolicies)</span><span class="sxs-lookup"><span data-stu-id="f6721-157">**Interface:** [**IX509ExtensionMSApplicationPolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionmsapplicationpolicies)</span></span>

<span data-ttu-id="f6721-158">**Идентификатор объекта:** \_ \_ Политики сертификата приложения кскн OID \_ \_ (1.3.6.1.4.1.311.21.10)</span><span class="sxs-lookup"><span data-stu-id="f6721-158">**OID:** XCN\_OID\_APPLICATION\_CERT\_POLICIES (1.3.6.1.4.1.311.21.10)</span></span>

## <a name="nameconstraints"></a><span data-ttu-id="f6721-159">намеконстраинтс</span><span class="sxs-lookup"><span data-stu-id="f6721-159">NameConstraints</span></span>

<span data-ttu-id="f6721-160">Расширение ограничений имен используется для указания пространства имен, в котором должны располагаться все имена субъектов сертификатов в иерархии сертификатов.</span><span class="sxs-lookup"><span data-stu-id="f6721-160">The name constraints extension is used to identify the namespace within which all subject names of certificates in a certificate hierarchy must be located.</span></span> <span data-ttu-id="f6721-161">Это расширение используется только в сертификате ЦС.</span><span class="sxs-lookup"><span data-stu-id="f6721-161">The extension is used only in a CA certificate.</span></span>

<span data-ttu-id="f6721-162">**Интерфейс:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span><span class="sxs-lookup"><span data-stu-id="f6721-162">**Interface:** [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span></span>

<span data-ttu-id="f6721-163">**Идентификатор объекта:** \_ \_ Ограничения имен OID кскн \_ (2.5.29.30)</span><span class="sxs-lookup"><span data-stu-id="f6721-163">**OID:** XCN\_OID\_NAME\_CONSTRAINTS (2.5.29.30)</span></span>

## <a name="policyconstraints"></a><span data-ttu-id="f6721-164">полициконстраинтс</span><span class="sxs-lookup"><span data-stu-id="f6721-164">PolicyConstraints</span></span>

<span data-ttu-id="f6721-165">Расширение ограничений политики добавляется к сертификатам ЦС, чтобы ограничить проверку пути, запрещая сопоставление политик или, запрашивая, что каждый сертификат в иерархии содержит допустимый идентификатор политики.</span><span class="sxs-lookup"><span data-stu-id="f6721-165">The policy constraints extension is added to CA certificates to constrain path validation by prohibiting policy mapping or by requiring that each certificate in the hierarchy contain an acceptable policy identifier.</span></span>

<span data-ttu-id="f6721-166">**Интерфейс:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span><span class="sxs-lookup"><span data-stu-id="f6721-166">**Interface:** [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span></span>

<span data-ttu-id="f6721-167">**Идентификатор объекта:** \_ \_ Ограничения политики OID кскн \_ (2.5.29.36)</span><span class="sxs-lookup"><span data-stu-id="f6721-167">**OID:** XCN\_OID\_POLICY\_CONSTRAINTS (2.5.29.36)</span></span>

## <a name="policymappings"></a><span data-ttu-id="f6721-168">полицимаппингс</span><span class="sxs-lookup"><span data-stu-id="f6721-168">PolicyMappings</span></span>

<span data-ttu-id="f6721-169">Расширение сопоставления политик используется для обнаружения политик в подчиненном ЦС, соответствующих политикам в выдающем ЦС.</span><span class="sxs-lookup"><span data-stu-id="f6721-169">The policy mappings extension is used to identify the policies in a subordinate CA that correspond to policies in the issuing CA.</span></span> <span data-ttu-id="f6721-170">Значение расширения содержит последовательность выдачи ЦС и сопоставления политик подчиненного ЦС, представленные идентификаторами объектов.</span><span class="sxs-lookup"><span data-stu-id="f6721-170">The extension value contains a sequence of issuing CA and subordinate CA policy mappings represented by object identifiers.</span></span>

<span data-ttu-id="f6721-171">**Интерфейс:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span><span class="sxs-lookup"><span data-stu-id="f6721-171">**Interface:** [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span></span>

<span data-ttu-id="f6721-172">**Идентификатор объекта:** \_ \_ Сопоставления политики OID кскн \_ (2.5.29.33)</span><span class="sxs-lookup"><span data-stu-id="f6721-172">**OID:** XCN\_OID\_POLICY\_MAPPINGS (2.5.29.33)</span></span>

## <a name="privatekeyusageperiod"></a><span data-ttu-id="f6721-173">приватекэйусажепериод</span><span class="sxs-lookup"><span data-stu-id="f6721-173">PrivateKeyUsagePeriod</span></span>

<span data-ttu-id="f6721-174">Расширение периода использования закрытого ключа используется для указания другого срока действия закрытого ключа, отличного от сертификата, с которым связан ключ.</span><span class="sxs-lookup"><span data-stu-id="f6721-174">The private key usage period extension is used to specify a different validity period for the private key than for the certificate with which the key is associated.</span></span>

<span data-ttu-id="f6721-175">**Интерфейс:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span><span class="sxs-lookup"><span data-stu-id="f6721-175">**Interface:** [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span></span>

<span data-ttu-id="f6721-176">**Идентификатор объекта:** \_ \_ Период использования кскн OID PRIVATEKEY \_ \_ (2.5.29.16)</span><span class="sxs-lookup"><span data-stu-id="f6721-176">**OID:** XCN\_OID\_PRIVATEKEY\_USAGE\_PERIOD (2.5.29.16)</span></span>

## <a name="smimecapabilities"></a><span data-ttu-id="f6721-177">смимекапабилитиес</span><span class="sxs-lookup"><span data-stu-id="f6721-177">SmimeCapabilities</span></span>

<span data-ttu-id="f6721-178">Расширение возможностей SSL/MIME можно использовать для отправки сообщений электронной почты отправителю сообщения электронной почты, чтобы отправитель мог выбрать наиболее безопасный алгоритм шифрования, поддерживаемый обеими сторонами.</span><span class="sxs-lookup"><span data-stu-id="f6721-178">The Secure/Multipurpose Internet Mail Extensions (S/MIME) capabilities extension can be used to report an email recipient's decryption capabilities to the sender of the email message so that the sender can choose the most secure encryption algorithm supported by both parties.</span></span> <span data-ttu-id="f6721-179">Значение расширения содержит набор идентификаторов OID алгоритма симметричного шифрования и дополнительную стойкость шифрования для каждого из них.</span><span class="sxs-lookup"><span data-stu-id="f6721-179">The extension value contains a collection of symmetric encryption algorithm OIDs and an optional encryption strength for each.</span></span>

<span data-ttu-id="f6721-180">**Интерфейс:** [ **IX509ExtensionSmimeCapabilities**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsmimecapabilities)</span><span class="sxs-lookup"><span data-stu-id="f6721-180">**Interface:** [**IX509ExtensionSmimeCapabilities**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsmimecapabilities)</span></span>

<span data-ttu-id="f6721-181">**Идентификатор объекта:** КСКН \_ OID \_ RSA \_ смимекапабилитиес (1.2.840.113549.1.9.15)</span><span class="sxs-lookup"><span data-stu-id="f6721-181">**OID:** XCN\_OID\_RSA\_SMIMECapabilities (1.2.840.113549.1.9.15)</span></span>

## <a name="subjectdirectoryattributes"></a><span data-ttu-id="f6721-182">субжектдиректоряттрибутес</span><span class="sxs-lookup"><span data-stu-id="f6721-182">SubjectDirectoryAttributes</span></span>

<span data-ttu-id="f6721-183">Расширение атрибутов каталога субъекта можно использовать для передачи атрибутов идентификации, таких как натионалити субъекта сертификата.</span><span class="sxs-lookup"><span data-stu-id="f6721-183">The subject directory attributes extension can be used to convey identification attributes such as the nationality of the certificate subject.</span></span> <span data-ttu-id="f6721-184">Значением расширения является последовательность пар значений кодов объекта (OID)</span><span class="sxs-lookup"><span data-stu-id="f6721-184">The extension value is a sequence of OID-value pairs.</span></span>

<span data-ttu-id="f6721-185">**Интерфейс:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span><span class="sxs-lookup"><span data-stu-id="f6721-185">**Interface:** [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span></span>

<span data-ttu-id="f6721-186">**Идентификатор объекта:** КСКН \_ OID \_ субъекта \_ dir \_ (2.5.29.9)</span><span class="sxs-lookup"><span data-stu-id="f6721-186">**OID:** XCN\_OID\_SUBJECT\_DIR\_ATTRS (2.5.29.9)</span></span>

## <a name="subjectkeyidentifier"></a><span data-ttu-id="f6721-187">SubjectKeyIdentifier</span><span class="sxs-lookup"><span data-stu-id="f6721-187">SubjectKeyIdentifier</span></span>

<span data-ttu-id="f6721-188">Расширение идентификатора ключа субъекта можно использовать для различения нескольких открытых ключей, удерживаемых субъектом сертификата.</span><span class="sxs-lookup"><span data-stu-id="f6721-188">The subject key identifier extension can be used to differentiate between multiple public keys held by the certificate subject.</span></span> <span data-ttu-id="f6721-189">Значением расширения обычно является хэш SHA-1 ключа.</span><span class="sxs-lookup"><span data-stu-id="f6721-189">The extension value is typically a SHA-1 hash of the key.</span></span>

<span data-ttu-id="f6721-190">**Интерфейс:** [ **IX509ExtensionSubjectKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsubjectkeyidentifier)</span><span class="sxs-lookup"><span data-stu-id="f6721-190">**Interface:** [**IX509ExtensionSubjectKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsubjectkeyidentifier)</span></span>

<span data-ttu-id="f6721-191">**Идентификатор объекта:** \_ \_ Идентификатор ключа субъекта OID кскн \_ \_ (2.5.29.14)</span><span class="sxs-lookup"><span data-stu-id="f6721-191">**OID:** XCN\_OID\_SUBJECT\_KEY\_IDENTIFIER (2.5.29.14)</span></span>

## <a name="template"></a><span data-ttu-id="f6721-192">Шаблон</span><span class="sxs-lookup"><span data-stu-id="f6721-192">Template</span></span>

<span data-ttu-id="f6721-193">Расширение шаблона можно использовать для обнаружения шаблона версии 2, используемого при выдаче или обновлении сертификата.</span><span class="sxs-lookup"><span data-stu-id="f6721-193">The template extension can be used to identify the version 2 template to use when issuing or renewing a certificate.</span></span> <span data-ttu-id="f6721-194">Значение расширения содержит шаблон OID и дополнительные сведения о версии.</span><span class="sxs-lookup"><span data-stu-id="f6721-194">The extension value contains the template OID and optional version information.</span></span> <span data-ttu-id="f6721-195">Расширение зависит от корпорации Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="f6721-195">The extension is Microsoft specific.</span></span>

<span data-ttu-id="f6721-196">**Интерфейс:** [ **IX509ExtensionTemplate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplate)</span><span class="sxs-lookup"><span data-stu-id="f6721-196">**Interface:** [**IX509ExtensionTemplate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplate)</span></span>

<span data-ttu-id="f6721-197">**Идентификатор объекта:** \_ \_ Шаблон сертификата кскн OID \_ (1.3.6.1.4.1.311.21.7)</span><span class="sxs-lookup"><span data-stu-id="f6721-197">**OID:** XCN\_OID\_CERTIFICATE\_TEMPLATE (1.3.6.1.4.1.311.21.7)</span></span>

## <a name="templatename"></a><span data-ttu-id="f6721-198">TemplateName</span><span class="sxs-lookup"><span data-stu-id="f6721-198">TemplateName</span></span>

<span data-ttu-id="f6721-199">Расширение имени шаблона можно использовать для поиска шаблона версии 1, используемого при выдаче или обновлении сертификата.</span><span class="sxs-lookup"><span data-stu-id="f6721-199">The template name extension can be used to identify the version 1 template to use when issuing or renewing a certificate.</span></span> <span data-ttu-id="f6721-200">Значение расширения содержит имя шаблона.</span><span class="sxs-lookup"><span data-stu-id="f6721-200">The extension value contains the name of the template.</span></span> <span data-ttu-id="f6721-201">Расширение зависит от корпорации Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="f6721-201">The extension is Microsoft specific.</span></span>

<span data-ttu-id="f6721-202">**Интерфейс:** [ **IX509ExtensionTemplateName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplatename)</span><span class="sxs-lookup"><span data-stu-id="f6721-202">**Interface:** [**IX509ExtensionTemplateName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplatename)</span></span>

<span data-ttu-id="f6721-203">**Идентификатор объекта:** КСКН \_ OID \_ Регистрация \_ \_ расширения типом (1.3.6.1.4.1.311.20.2)</span><span class="sxs-lookup"><span data-stu-id="f6721-203">**OID:** XCN\_OID\_ENROLL\_CERTTYPE\_EXTENSION (1.3.6.1.4.1.311.20.2)</span></span>

## <a name="related-topics"></a><span data-ttu-id="f6721-204">См. также</span><span class="sxs-lookup"><span data-stu-id="f6721-204">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6721-205">Расширения</span><span class="sxs-lookup"><span data-stu-id="f6721-205">Extensions</span></span>](extensions.md)
</dt> </dl>

 

 



