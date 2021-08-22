---
description: В этом разделе описывается внедрение сертификатов, образующих цепочку сертификатов, в документ XPS.
ms.assetid: c6aae8ff-2e1e-43de-9105-171e4187d193
title: Внедрение цепочек сертификатов в документ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e23e47b4cd0d140d7200fb8aa01642ea5fbb731e49dcc289f596a054b0accbf3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119447584"
---
# <a name="embed-certificate-chains-in-a-document"></a>Внедрение цепочек сертификатов в документ

В этом разделе описывается внедрение сертификатов, образующих цепочку сертификатов, в документ XPS. Цепочка сертификатов состоит из всех сертификатов, за исключением корневого сертификата, необходимого для сертификации субъекта, идентифицируемого конечным сертификатом.

Чтобы внедрить цепочку сертификатов в документ XPS, сначала создайте цепочку сертификатов, как показано в следующем примере кода.

Метод **креатецертификатечаин** в примере кода принимает *certificateStore* в качестве параметра, который является значением **хцертсторе** . Если это значение равно **null**, сертификаты будут получены с сервера сертификатов клиентского компьютера. Если значение является маркером хранилища сертификатов, сертификаты будут извлечены из хранилища, на который ссылаются *certificateStore* , а также с сервера сертификатов клиентского компьютера.


```C++
HRESULT 
CreateCertificateChain (
    __in PCCERT_CONTEXT            certificate,
    __in HCERTSTORE                certificateStore,
    __out PCCERT_CHAIN_CONTEXT* certificateChain
)
{
    HRESULT  hr = S_OK;

    CERT_CHAIN_PARA certificateChainParameters = {0};

    certificateChainParameters.cbSize = sizeof(CERT_CHAIN_PARA);
    certificateChainParameters.RequestedUsage.dwType = USAGE_MATCH_TYPE_AND;

    // CertGetCertificateChain builds a certificate chain that starts 
    //  from the PCCERT_CONTEXT structure provided by the caller.
    //  After the certificate chain has been successfully created, 
    //  then the authenticity of the certificate can be determined 
    //  by examining the errors, if any, that occurred while the chain
    //  was created.
    BOOL successCreatingCertChain = CertGetCertificateChain (
        NULL,
        certificate,
        NULL,
        certificateStore,
        &certificateChainParameters,
        CERT_CHAIN_REVOCATION_CHECK_CHAIN_EXCLUDE_ROOT,
        NULL,
        certificateChain);

    if (!successCreatingCertChain)
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
    }
    return hr;
}
```



В следующем примере кода создается цепочка сертификатов на основе сертификатов, а затем эти сертификаты добавляются в документ XPS. Обратите внимание, что [**CertGetCertificateChain**](/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain) создает цепочку сертификатов, в которой первый сертификат подписи является первым, а корневой сертификат — последним. В этом примере сертификат подписи и корневой сертификат не добавляются. Сертификаты подписи будут добавлены с вызовом метода [**икспссигнатуреманажер:: Sign**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-sign) , который должен быть последним методом подписи, вызванным в документе. Корневой сертификат не добавляется, когда документ подписан, так как он должен быть предоставлен сервером сертификатов клиентского компьютера при проверке подписи.


```C++
HRESULT
EmbedCertificateChainInXpsPackage (
    __in IXpsSigningOptions *signingOptions,
    __in PCCERT_CONTEXT signingCertificate
)
{
    HRESULT                 hr                           = S_OK;
    PCCERT_CHAIN_CONTEXT    certificateChainContext      = NULL;
    IOpcCertificateSet      *certificateSetToUpdate      = NULL;
    DWORD                   certificateChainContextIndex = 0;

    // Create the entire certificate chain that originates 
    //  from the certificate that is used to sign the XPS document.
    hr = CreateCertificateChain(
        signingCertificate, 
        NULL, 
        &certificateChainContext);

    if (SUCCEEDED(hr))
    {
        // The signing options of an XPS document contain a pointer to 
        //  an IOpcCertificateSet interface that can be retrieved by 
        //  calling the GetCertificateSet method.
        hr = signingOptions->GetCertificateSet(&certificateSetToUpdate);
    }
    if (SUCCEEDED(hr))
    {
        // for each certificate chain context in this certificate...
        for (certificateChainContextIndex = 0; 
             certificateChainContextIndex < certificateChainContext->cChain; 
             certificateChainContextIndex++)
        {
            // inside a certificate chain context, 
            DWORD adjustedSimpleChainStartIndex = 0;
            DWORD adjustedSimpleChainEndIndex = 0;
            DWORD simpleCertChainIndex = 0;
            CERT_SIMPLE_CHAIN  *simpleCertificateChainWithinContext = NULL;

            // get the information about the certificate chain
            //  set the first item in the certificate chain to load
            //  Ignore the first PCCERT_CONTEXT in the first CERT_SIMPLE_CHAIN
            //  because this is the certificate that was used to build
            //  the chain and is already loaded in the document
            if (certificateChainContextIndex == 0)
            {
                adjustedSimpleChainStartIndex = 1;
            }
            else
            {
                adjustedSimpleChainStartIndex = 0;
            }
                    
            //  get the last item in the certificate chain
            simpleCertificateChainWithinContext = 
                certificateChainContext->rgpChain[certificateChainContextIndex];
            adjustedSimpleChainEndIndex = 
                simpleCertificateChainWithinContext->cElement;

            // Ignore the last PCCERT_CONTEXT in the last CERT_SIMPLE_CHAIN
            //  because this is the root certificate that must be retrieved
            //  from the client computer's certificate server.
            if (certificateChainContextIndex == certificateChainContext->cChain - 1)
            {
                if (adjustedSimpleChainEndIndex != 0)
                {
                    adjustedSimpleChainEndIndex = adjustedSimpleChainEndIndex - 1;
                }
            }

            // for each certificate chain in this context...
            for (simpleCertChainIndex = adjustedSimpleChainStartIndex; 
                 simpleCertChainIndex < adjustedSimpleChainEndIndex;
                 simpleCertChainIndex++)
            {
                // Add the certificate to the XPS document.
                PCCERT_CONTEXT certificateToEmbed = 
                    simpleCertificateChainWithinContext->rgpElement[simpleCertChainIndex]->pCertContext;
                if (FAILED(hr = certificateSetToUpdate->Add(certificateToEmbed)))
                {
                    break; // out of for loop with failed hr
                }
            }
        }
    }
    return hr;
}
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

**Следующие шаги**
</dt> <dt>

[Загрузка сертификата из файла](load-a-certificate-from-a-file.md)
</dt> <dt>

[Убедитесь, что сертификат поддерживает метод подписи.](verify-a-certificate-supports-a-signature-method.md)
</dt> <dt>

[Проверка того, что система поддерживает метод дайджеста](verify-a-certificate-supports-a-digest-method.md)
</dt> <dt>

**Используется в этом примере**
</dt> <dt>

[**\_контекст сертификата**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[**CertGetCertificateChain**](/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain)
</dt> <dt>

[**\_ \_ сведения о шифровании OID**](/windows/desktop/api/wincrypt/ns-wincrypt-crypt_oid_info)
</dt> <dt>

[**иопкцертификатесет**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopccertificateset)
</dt> <dt>

[**икспссигнингоптионс**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions)
</dt> <dt>

**Дополнительные сведения**
</dt> <dt>

[API шифрования](/windows/desktop/SecCrypto/cryptography-portal)
</dt> <dt>

[Криптографические функции](/windows/desktop/SecCrypto/cryptography-functions)
</dt> <dt>

[Цифровые сертификаты](/windows/desktop/SecCrypto/digital-certificates)
</dt> <dt>

[Цепочки сертификатов](/windows/desktop/SecCrypto/certificate-chains)
</dt> <dt>

[Проверка доверия сертификата](/windows/desktop/SecCrypto/certificate-trust-verification)
</dt> <dt>

[Ошибки API цифровой подписи XPS](xps-digital-signatures-errors.md)
</dt> <dt>

[Ошибки документа XPS](xps-document-errors.md)
</dt> <dt>

[XPS](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
