---
description: В этом разделе описывается, как подписать документ XPS.
ms.assetid: fbe64aed-6b07-49de-910c-18be68cb65a2
title: Подписать документ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef544b2c34af19282d697676d22903948355d23e18e1c646df691c720052cc4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119033882"
---
# <a name="sign-a-document"></a>Подписать документ

В этом разделе описывается, как подписать документ XPS.

Прежде чем использовать приведенные ниже примеры кода в программе, ознакомьтесь со сведениями об отказе в [типичных задачах программирования цифровых подписей](basic-digital-signature-programming-tasks.md).

Чтобы подписать XPS-документ, сначала загрузите его в диспетчер подписей, как описано в разделе [Инициализация диспетчера подписей](initialize-the-signature-manager.md).

Чтобы подписать документ, загруженный в диспетчер подписей, выполните следующие действия.

1.  Создайте экземпляр интерфейса [**икспссигнингоптионс**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions) .
2.  Задайте политику подписывания.
3.  Задайте метод подписи. Строковые константы URI метода подписи определены в криптксмл. h. Дополнительные сведения о допустимых значениях метода подписи см. в разделе [**икспссигнингоптионс:: сетсигнатуремесод**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setsignaturemethod).
4.  Задайте метод дайджеста. Строковые константы URI метода дайджеста определены в криптксмл. h. Сведения о допустимых значениях метода дайджеста см. в разделе [**икспссигнингоптионс:: сетдижестмесод**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setdigestmethod).
5.  Загрузите сертификат, как описано в разделе [Загрузка сертификата из файла](load-a-certificate-from-a-file.md).
6.  Убедитесь, что сертификат поддерживает метод подписи, как описано в разделе [Проверка того, что сертификат поддерживает метод подписи](verify-a-certificate-supports-a-signature-method.md).
7.  Убедитесь, что метод дайджеста поддерживается системой, как описано в разделе Проверка того, что [система поддерживает метод дайджеста](verify-a-certificate-supports-a-digest-method.md).
8.  При необходимости внедрите сертификаты из цепочки доверия сертификатов в документ XPS, как описано в статье [встраивание цепочек сертификатов в документ](embedding-certificate-trust-chains-in-a-document.md).
9.  Подпишите документ XPS.

В следующем примере кода показано, как использовать предыдущие шаги в программе.


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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

**Следующие шаги**
</dt> <dt>

[Добавление запроса подписи в документ XPS](add-a-signature-request-to-a-document.md)
</dt> <dt>

[Проверка подписей документов](verify-document-signatures.md)
</dt> <dt>

**Используется в этом разделе**
</dt> <dt>

[**цертфрицертификатеконтекст**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext)
</dt> <dt>

[**икспссигнатуреманажер**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager)
</dt> <dt>

[**Икспссигнатуреманажер:: Креатесигнингоптионс**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-createsigningoptions)
</dt> <dt>

[**Икспссигнатуреманажер:: Sign**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-sign)
</dt> <dt>

[**икспссигнингоптионс**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions)
</dt> <dt>

[**Икспссигнингоптионс:: Сетдижестмесод**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setdigestmethod)
</dt> <dt>

[**Икспссигнингоптионс:: Сетполици**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setpolicy)
</dt> <dt>

[**Икспссигнингоптионс:: Сетсигнатуремесод**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setsignaturemethod)
</dt> <dt>

[**\_Политика подписывания XPS \_**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_policy)
</dt> <dt>

**Дополнительные сведения**
</dt> <dt>

[API шифрования](/windows/desktop/SecCrypto/cryptography-portal)
</dt> <dt>

[Криптографические функции](/windows/desktop/SecCrypto/cryptography-functions)
</dt> <dt>

[Загрузка сертификата из файла](load-a-certificate-from-a-file.md)
</dt> <dt>

[Проверка того, поддерживает ли сертификат метод подписи](verify-a-certificate-supports-a-signature-method.md)
</dt> <dt>

[Проверка того, что система поддерживает метод дайджеста](verify-a-certificate-supports-a-digest-method.md)
</dt> <dt>

[Внедрение цепочек сертификатов в документ](embedding-certificate-trust-chains-in-a-document.md)
</dt> <dt>

[Ошибки API цифровой подписи XPS](xps-digital-signatures-errors.md)
</dt> <dt>

[Ошибки документа XPS](xps-document-errors.md)
</dt> <dt>

[XPS](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
