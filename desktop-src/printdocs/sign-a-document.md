---
description: В этом разделе описывается, как подписать документ XPS.
ms.assetid: fbe64aed-6b07-49de-910c-18be68cb65a2
title: Подписать документ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a4ad07323a26d21f9010c3fd54c708880b90173
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909364"
---
# <a name="sign-a-document"></a><span data-ttu-id="8de2f-103">Подписать документ</span><span class="sxs-lookup"><span data-stu-id="8de2f-103">Sign a Document</span></span>

<span data-ttu-id="8de2f-104">В этом разделе описывается, как подписать документ XPS.</span><span class="sxs-lookup"><span data-stu-id="8de2f-104">This topic describes how to sign an XPS document.</span></span>

<span data-ttu-id="8de2f-105">Прежде чем использовать приведенные ниже примеры кода в программе, ознакомьтесь со сведениями об отказе в [типичных задачах программирования цифровых подписей](basic-digital-signature-programming-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="8de2f-105">Before using the following code examples in your program, read the disclaimer in [Common Digital Signature Programming Tasks](basic-digital-signature-programming-tasks.md).</span></span>

<span data-ttu-id="8de2f-106">Чтобы подписать XPS-документ, сначала загрузите его в диспетчер подписей, как описано в разделе [Инициализация диспетчера подписей](initialize-the-signature-manager.md).</span><span class="sxs-lookup"><span data-stu-id="8de2f-106">To sign an XPS document, first load it into a signature manager as described in [Initialize the Signature Manager](initialize-the-signature-manager.md).</span></span>

<span data-ttu-id="8de2f-107">Чтобы подписать документ, загруженный в диспетчер подписей, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="8de2f-107">To sign a document that has been loaded into a signature manager:</span></span>

1.  <span data-ttu-id="8de2f-108">Создайте экземпляр интерфейса [**икспссигнингоптионс**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions) .</span><span class="sxs-lookup"><span data-stu-id="8de2f-108">Instantiate an [**IXpsSigningOptions**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions) interface.</span></span>
2.  <span data-ttu-id="8de2f-109">Задайте политику подписывания.</span><span class="sxs-lookup"><span data-stu-id="8de2f-109">Set the signing policy.</span></span>
3.  <span data-ttu-id="8de2f-110">Задайте метод подписи.</span><span class="sxs-lookup"><span data-stu-id="8de2f-110">Set the signature method.</span></span> <span data-ttu-id="8de2f-111">Строковые константы URI метода подписи определены в криптксмл. h.</span><span class="sxs-lookup"><span data-stu-id="8de2f-111">Signature method URI string constants are defined in cryptxml.h.</span></span> <span data-ttu-id="8de2f-112">Дополнительные сведения о допустимых значениях метода подписи см. в разделе [**икспссигнингоптионс:: сетсигнатуремесод**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setsignaturemethod).</span><span class="sxs-lookup"><span data-stu-id="8de2f-112">For more information about valid signature method values, see [**IXpsSigningOptions::SetSignatureMethod**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setsignaturemethod).</span></span>
4.  <span data-ttu-id="8de2f-113">Задайте метод дайджеста.</span><span class="sxs-lookup"><span data-stu-id="8de2f-113">Set the digest method.</span></span> <span data-ttu-id="8de2f-114">Строковые константы URI метода дайджеста определены в криптксмл. h.</span><span class="sxs-lookup"><span data-stu-id="8de2f-114">Digest method URI string constants are defined in cryptxml.h.</span></span> <span data-ttu-id="8de2f-115">Сведения о допустимых значениях метода дайджеста см. в разделе [**икспссигнингоптионс:: сетдижестмесод**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setdigestmethod).</span><span class="sxs-lookup"><span data-stu-id="8de2f-115">For information about valid digest method values, see [**IXpsSigningOptions::SetDigestMethod**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setdigestmethod).</span></span>
5.  <span data-ttu-id="8de2f-116">Загрузите сертификат, как описано в разделе [Загрузка сертификата из файла](load-a-certificate-from-a-file.md).</span><span class="sxs-lookup"><span data-stu-id="8de2f-116">Load the certificate as described in [Load a Certificate From a File](load-a-certificate-from-a-file.md).</span></span>
6.  <span data-ttu-id="8de2f-117">Убедитесь, что сертификат поддерживает метод подписи, как описано в разделе [Проверка того, что сертификат поддерживает метод подписи](verify-a-certificate-supports-a-signature-method.md).</span><span class="sxs-lookup"><span data-stu-id="8de2f-117">Verify that the certificate supports the signature method, as described in [Verify That a Certificate Supports a Signature Method](verify-a-certificate-supports-a-signature-method.md).</span></span>
7.  <span data-ttu-id="8de2f-118">Убедитесь, что метод дайджеста поддерживается системой, как описано в разделе Проверка того, что [система поддерживает метод дайджеста](verify-a-certificate-supports-a-digest-method.md).</span><span class="sxs-lookup"><span data-stu-id="8de2f-118">Verify that the digest method is supported by the system, as described in [Verify the System Supports a Digest Method](verify-a-certificate-supports-a-digest-method.md).</span></span>
8.  <span data-ttu-id="8de2f-119">При необходимости внедрите сертификаты из цепочки доверия сертификатов в документ XPS, как описано в статье [встраивание цепочек сертификатов в документ](embedding-certificate-trust-chains-in-a-document.md).</span><span class="sxs-lookup"><span data-stu-id="8de2f-119">If required, embed the certificates of the certificate trust chain in the XPS document as described in [Embed Certificate Chains in a Document](embedding-certificate-trust-chains-in-a-document.md).</span></span>
9.  <span data-ttu-id="8de2f-120">Подпишите документ XPS.</span><span class="sxs-lookup"><span data-stu-id="8de2f-120">Sign the XPS document.</span></span>

<span data-ttu-id="8de2f-121">В следующем примере кода показано, как использовать предыдущие шаги в программе.</span><span class="sxs-lookup"><span data-stu-id="8de2f-121">The following code example illustrates how to use the preceding steps in a program.</span></span>


```C++
    // this example requires:
    //        cryptxml.h
    // and refers to local methods that are described
    // in other topics

    HRESULT                hr               = S_OK;
    BOOL                   supported        = FALSE;
    BOOL                   succeeded        = FALSE;
    IXpsSigningOptions     *signingOptions  = NULL;
    IXpsSignature          *signature       = NULL;
    PCCERT_CONTEXT         certificate      = NULL;
    
    // Instantiate an IXpsSigningOptions interface.
    hr = signatureManager->CreateSigningOptions (&signingOptions);
    
    if (SUCCEEDED(hr)) {
        // Set the signing policy to indicate the document parts 
        //  to sign.
        hr = signingOptions->SetPolicy (XPS_SIGN_POLICY_CORE_PROPERTIES);
    }

    if (SUCCEEDED(hr)) {
        // Set the digital signature method to use to generate the 
        //    signature hash value. 
        //
        // The signature method used in this example is 
        //    defined in cryptxml.h.
        hr = signingOptions->SetSignatureMethod (
            wszURI_XMLNS_DIGSIG_RSA_SHA1);
    }

    if (SUCCEEDED(hr)) {
        // Set the digest method to use.
        //
        // The digest method used in this example is 
        //    defined in cryptxml.h.
        hr = signingOptions->SetDigestMethod (wszURI_XMLNS_DIGSIG_SHA1);
    }

    if (SUCCEEDED(hr)) {
        // Load a certificate from a certificate file
        hr = LoadCertificateFromFile (signingCertificate, &certificate);
    }

    if (SUCCEEDED(hr)) {
        // Verify the certificate supports the digest method
        supported = SupportsDigestAlgorithm (
            wszURI_XMLNS_DIGSIG_SHA1);
        if (!supported) hr = E_FAIL;
    }

    if (SUCCEEDED(hr)) {
        // Verify the signature method is supported by the certificate
        //  and the system
        supported = SupportsSignatureAlgorithm(
            wszURI_XMLNS_DIGSIG_RSA_SHA1, certificate);
        if (!supported) hr = E_FAIL;
    }

    if (SUCCEEDED(hr)) {
        // Embed the certificate trust chain in the XPS package (optional).
        hr = EmbedCertificateChainInXpsPackage (signingOptions, certificate);
    }

    if (SUCCEEDED(hr)) {
        // Sign the XPS document
        hr = signatureManager->Sign (signingOptions, certificate, &signature);
    }

 //<Free the certificate context
    if (NULL != certificate) CertFreeCertificateContext (certificate);

    if (NULL != signingOptions) signingOptions->Release();
    if (NULL != signature) signature->Release();
```



## <a name="related-topics"></a><span data-ttu-id="8de2f-122">См. также</span><span class="sxs-lookup"><span data-stu-id="8de2f-122">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="8de2f-123">**Следующие шаги**</span><span class="sxs-lookup"><span data-stu-id="8de2f-123">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="8de2f-124">Добавление запроса подписи в документ XPS</span><span class="sxs-lookup"><span data-stu-id="8de2f-124">Add a Signature Request to an XPS Document</span></span>](add-a-signature-request-to-a-document.md)
</dt> <dt>

[<span data-ttu-id="8de2f-125">Проверка подписей документов</span><span class="sxs-lookup"><span data-stu-id="8de2f-125">Verify Document Signatures</span></span>](verify-document-signatures.md)
</dt> <dt>

<span data-ttu-id="8de2f-126">**Используется в этом разделе**</span><span class="sxs-lookup"><span data-stu-id="8de2f-126">**Used in This Section**</span></span>
</dt> <dt>

[<span data-ttu-id="8de2f-127">**цертфрицертификатеконтекст**</span><span class="sxs-lookup"><span data-stu-id="8de2f-127">**CertFreeCertificateContext**</span></span>](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext)
</dt> <dt>

[<span data-ttu-id="8de2f-128">**икспссигнатуреманажер**</span><span class="sxs-lookup"><span data-stu-id="8de2f-128">**IXpsSignatureManager**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager)
</dt> <dt>

[<span data-ttu-id="8de2f-129">**Икспссигнатуреманажер:: Креатесигнингоптионс**</span><span class="sxs-lookup"><span data-stu-id="8de2f-129">**IXpsSignatureManager::CreateSigningOptions**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-createsigningoptions)
</dt> <dt>

[<span data-ttu-id="8de2f-130">**Икспссигнатуреманажер:: Sign**</span><span class="sxs-lookup"><span data-stu-id="8de2f-130">**IXpsSignatureManager::Sign**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-sign)
</dt> <dt>

[<span data-ttu-id="8de2f-131">**икспссигнингоптионс**</span><span class="sxs-lookup"><span data-stu-id="8de2f-131">**IXpsSigningOptions**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions)
</dt> <dt>

[<span data-ttu-id="8de2f-132">**Икспссигнингоптионс:: Сетдижестмесод**</span><span class="sxs-lookup"><span data-stu-id="8de2f-132">**IXpsSigningOptions::SetDigestMethod**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setdigestmethod)
</dt> <dt>

[<span data-ttu-id="8de2f-133">**Икспссигнингоптионс:: Сетполици**</span><span class="sxs-lookup"><span data-stu-id="8de2f-133">**IXpsSigningOptions::SetPolicy**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setpolicy)
</dt> <dt>

[<span data-ttu-id="8de2f-134">**Икспссигнингоптионс:: Сетсигнатуремесод**</span><span class="sxs-lookup"><span data-stu-id="8de2f-134">**IXpsSigningOptions::SetSignatureMethod**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setsignaturemethod)
</dt> <dt>

[<span data-ttu-id="8de2f-135">**\_Политика подписывания XPS \_**</span><span class="sxs-lookup"><span data-stu-id="8de2f-135">**XPS\_SIGN\_POLICY**</span></span>](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_policy)
</dt> <dt>

<span data-ttu-id="8de2f-136">**Дополнительные сведения**</span><span class="sxs-lookup"><span data-stu-id="8de2f-136">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="8de2f-137">API шифрования</span><span class="sxs-lookup"><span data-stu-id="8de2f-137">Cryptography API</span></span>](/windows/desktop/SecCrypto/cryptography-portal)
</dt> <dt>

[<span data-ttu-id="8de2f-138">Криптографические функции</span><span class="sxs-lookup"><span data-stu-id="8de2f-138">Cryptography Functions</span></span>](/windows/desktop/SecCrypto/cryptography-functions)
</dt> <dt>

[<span data-ttu-id="8de2f-139">Загрузка сертификата из файла</span><span class="sxs-lookup"><span data-stu-id="8de2f-139">Load a Certificate From a File</span></span>](load-a-certificate-from-a-file.md)
</dt> <dt>

[<span data-ttu-id="8de2f-140">Проверка того, поддерживает ли сертификат метод подписи</span><span class="sxs-lookup"><span data-stu-id="8de2f-140">Verify a Certificate Supports a Signature Method</span></span>](verify-a-certificate-supports-a-signature-method.md)
</dt> <dt>

[<span data-ttu-id="8de2f-141">Проверка того, что система поддерживает метод дайджеста</span><span class="sxs-lookup"><span data-stu-id="8de2f-141">Verify the System Supports a Digest Method</span></span>](verify-a-certificate-supports-a-digest-method.md)
</dt> <dt>

[<span data-ttu-id="8de2f-142">Внедрение цепочек сертификатов в документ</span><span class="sxs-lookup"><span data-stu-id="8de2f-142">Embed Certificate Chains in a Document</span></span>](embedding-certificate-trust-chains-in-a-document.md)
</dt> <dt>

[<span data-ttu-id="8de2f-143">Ошибки API цифровой подписи XPS</span><span class="sxs-lookup"><span data-stu-id="8de2f-143">XPS Digital Signature API Errors</span></span>](xps-digital-signatures-errors.md)
</dt> <dt>

[<span data-ttu-id="8de2f-144">Ошибки документа XPS</span><span class="sxs-lookup"><span data-stu-id="8de2f-144">XPS Document Errors</span></span>](xps-document-errors.md)
</dt> <dt>

[<span data-ttu-id="8de2f-145">XPS</span><span class="sxs-lookup"><span data-stu-id="8de2f-145">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
