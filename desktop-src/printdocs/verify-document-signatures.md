---
description: В этом разделе описывается проверка подписей в документе XPS и проверка сертификатов, связанных с этими подписями.
ms.assetid: fd12abaf-dc0f-4db1-837d-c116627bcc7e
title: Проверка подписей документов и сертификатов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47dfee91437f7cc36e754e8c1f97fa89cd2387af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702911"
---
# <a name="verify-document-signatures-and-certificates"></a>Проверка подписей документов и сертификатов

В этом разделе описывается проверка подписей в документе XPS и проверка сертификатов, связанных с этими подписями.

Прежде чем использовать приведенные ниже примеры кода в программе, ознакомьтесь со сведениями об отказе в [типичных задачах программирования цифровых подписей](basic-digital-signature-programming-tasks.md).

В следующем примере кода выполняется проверка цифровых подписей, найденных в документе XPS.

Чтобы проверить подписи в документе XPS, выполните следующие действия.

1.  Загрузите документ в диспетчер подписей, как описано в разделе [Инициализация диспетчера подписей](initialize-the-signature-manager.md).
2.  Получение коллекции подписей из диспетчера цифровых подписей.
3.  Возвращает количество подписей в коллекции.
4.  Для каждой сигнатуры в коллекции вызовите метод [**Verify**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-verify) , как показано в следующем примере кода.


```C++
HRESULT
VerifyAllDigitalSignaturesAndAuthenticateCertificates(
    IXpsSignatureManager *signatureManager
)
{
    HRESULT                       hr                              = S_OK;
    IXpsSignature                 *signature                      = NULL;
    IXpsSignatureCollection       *signaturesInDocument           = NULL;
    UINT32                        numberOfSignaturesInDocument    = NULL;

    hr = signatureManager->GetSignatures(&signaturesInDocument);
    if (SUCCEEDED(hr)) {
        hr = signaturesInDocument->GetCount(&numberOfSignaturesInDocument);
    }

    if (SUCCEEDED(hr)) {
        // Check each signature in the XPS document that was opened in
        //  the signature manager.
        for (UINT32 index = 0; index < numberOfSignaturesInDocument; index++)
        {
            // Get the signature in the current index of the 
            //  IXpsSignatureCollection object
            hr = signaturesInDocument->GetAt(index, &signature);

            if (SUCCEEDED(hr)) {
                PCCERT_CONTEXT       signingCertificate = NULL;
                XPS_SIGNATURE_STATUS signatureStatus; 

                signatureStatus = XPS_SIGNATURE_STATUS_BROKEN;
                // Verify the signature and authenticate 
                //  its signing certificate
                hr = VerifySignatureAndCertificates (
                        signature,
                        &signingCertificate,
                        &signatureStatus);
                if (FAILED(hr)) {
                    // If a FACILITY_SECURITY error code is returned then 
                    //  the current certificate was not the 
                    //    signing certificate, so continue with 
                    //  the enumeration.
                    if (HRESULT_FACILITY(hr) != FACILITY_SECURITY)
                    {
                        // If the error was not a FACILITY_SECURITY error  
                        //  then exit and return the error
                        break; // out of for loop
                    }
                }
                // release pointers for next loop
                if (NULL != signature) {
                    signature->Release(); 
                    signature = NULL; 
                }
                if (NULL != signingCertificate) {
                    CertFreeCertificateContext (signingCertificate); 
                    signingCertificate = NULL;
                }
            }
        }
    }
    if (NULL != signaturesInDocument) signaturesInDocument->Release();
    
    return hr;
}
```



Чтобы проверить цифровую подпись, сначала проверьте подпись, созданную сертификатом подписи, а затем проверьте сертификат подписи. Метод проверки, используемый в следующем примере кода, кэширует сертификаты во временном хранилище сертификатов, которое используется функциями шифрования API, когда они вызываются далее в этом примере.

Чтобы создать временное хранилище сертификатов, выполните следующие действия.

1.  Создайте временное хранилище сертификатов для хранения сертификатов, используемых сигнатурой.
2.  Выполните итерацию по набору сертификатов подписи и загрузите каждый сертификат во временное хранилище сертификатов.


```C++
HRESULT VerifySignatureAndCertificates (
    IXpsSignature           *signature,
    PCCERT_CONTEXT          *signingCertificate,
    XPS_SIGNATURE_STATUS    *signatureStatus
)
{
    HRESULT                         hr                        = S_OK;
    BOOL                            moreCertificates          = FALSE;
    IOpcCertificateEnumerator       *certificatesInSignature  = NULL;
    
    HCERTSTORE                      signatureCertificateStore = NULL;
    
    // Create a temporary certificate store.  
    signatureCertificateStore = CertOpenStore(
        CERT_STORE_PROV_MEMORY, 
        X509_ASN_ENCODING, 
        NULL, 
        0, 
        NULL);

    // Create a certificate enumerator to store the certificates 
    //  that are associated with the current signature.
    hr = signature->GetCertificateEnumerator(&certificatesInSignature);

    if (SUCCEEDED(hr))
    {
    // We need to call the MoveNext method to initialize the enumerator.
        hr = certificatesInSignature->MoveNext(&moreCertificates);
    }
    if (SUCCEEDED(hr))
    {
        // Iterate through the certificates in the signature, 
        //  and add each one to the temporary certificate store.  
        //  This temporary  certificate store simplifies 
        //  authentication of the signing certificate.
        while (moreCertificates)
        {
            PCCERT_CONTEXT certificate  = NULL;
            hr = certificatesInSignature->GetCurrent(&certificate);
            if (SUCCEEDED(hr))
            {
                // got the next certificate so
                // add the current certificate to the temporary certificate store.
                if (!CertAddCertificateContextToStore(signatureCertificateStore,
                    certificate,
                    CERT_STORE_ADD_REPLACE_EXISTING,
                    NULL))
                {
                    hr = E_FAIL;
                    // ERROR: could not add the certificate to the certificate store
                    break; // out of while loop
                }
                CertFreeCertificateContext (certificate);
            }
            else
            {
                // unable to get the certificate so skip
            }

            // move to next certificate in set
            if (FAILED(hr = certificatesInSignature->MoveNext(&moreCertificates)))
            {
                // ERROR: could not move to the next certificate in the enumerator
                break; // out of while loop
            }
            // moreCertificates == FALSE when the end of the set has been reached.
        }//End while
    }
    if (NULL != certificatesInSignature) certificatesInSignature->Release();

```



Чтобы проверить цифровую подпись и сертификат, используемый для подписания документа, выполните следующие действия.

1.  Найдите сертификат для подписи, просматривая сертификаты, которые используются в сигнатуре.
2.  Протестируйте сертификат, проверив его подпись по сертификату. Сертификат подписи находится в том случае, если метод [**Verify**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-verify) возвращает [**\_ \_ состояние подписи**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_signature_status) XPS, **\_ \_ \_ допустимое состояние подписи XPS** или **\_ \_ состояние подписи \_ XPS**, и не возвращает ошибку **\_ безопасности средства** .


```C++
    // Reset the enumerator
    hr = signature->GetCertificateEnumerator(&certificatesInSignature);
    if (SUCCEEDED (hr))
    {
        moreCertificates = FALSE;
        hr = certificatesInSignature->MoveNext(&moreCertificates);
    }
    if (SUCCEEDED(hr))
    {
        // Iterate through the certificates in the signature,
        //  and call the IXpsSignature.Verify() method
        //  on each certificate.  
        // A signature can include an entire certificate chain, and so 
        //  only one of the certificates found in this enumeration 
        //  is the certificate that was used to sign the package. 
        //  The signing certificate is the one to authenticate.  
        // To find the signing certificate,  iterate through 
        //  the certificates in the signature and select the certificate that 
        //  returns an XPS_SIGNATURE_STATUS of XPS_SIGNATURE_STATUS_VALID
        //  or XPS_SIGNATURE_STATUS_QUESTIONABLE and does not return a
        //  FACILITY_SECURITY error.
        XPS_SIGNATURE_STATUS localSignatureStatus;
        localSignatureStatus = XPS_SIGNATURE_STATUS_INCOMPLIANT;
        do
        {
            PCCERT_CONTEXT certificate = NULL;
            DWORD certificateStatus = NULL;

            if (FAILED(hr = certificatesInSignature->GetCurrent(&certificate)))
            {
                // We will skip corrupted certificates
                // free this one and move to the next
                CertFreeCertificateContext (certificate);
                hr = certificatesInSignature->MoveNext(&moreCertificates);
                if (FAILED(hr))
                {
                    // ERROR: could not move to the next 
                    //  certificate in the enumerator
                    break; // out of do loop with failed hr
                }
                // continue with next loop iteration
                continue;
            }
            
            // Verify that the signature conforms to the XPS signing policy.
            hr = signature->Verify(certificate, &localSignatureStatus);
            if (FAILED(hr))
            {
                // If a FACILITY_SECURITY error code is returned, then the
                //  current certificate was not the signing certificate,
                //  so continue to the next certificate.
                if (HRESULT_FACILITY(hr) == FACILITY_SECURITY)
                {
                    // free this one and move to the next
                    CertFreeCertificateContext (certificate);
                    hr = certificatesInSignature->MoveNext(&moreCertificates);
                    if (FAILED(hr))
                    {
                        // ERROR: could not move to the next certificate 
                        //  in the enumerator
                        break; // out of do loop with failed hr
                    }
                    continue;
                }
                // ERROR: An attempt to verify the signature has failed
                break; // out of do loop with failed hr
            }
            // if verification was successful, localSignatureStatus will
            //  contain the status of the signature.
            //
            // do loop continues in next code example
```



После обнаружения сертификата для подписи выполните следующие действия.

1.  Сохраните возвращенное состояние подписи.
2.  При необходимости обновите локальное состояние, чтобы выполнить последующие проверки сертификатов:
    1.  Если состояние подписи — "успешно", присвойте локальному состоянию значение "вопрос", чтобы проверить сертификаты.
    2.  Если состояние подписи не соответствует требованиям, оставьте локальное состояние несоответствующим.
    3.  Если подпись имеет состояние "нарушена" или "неполная", установите локальное состояние "нарушено".

Состояние подписи " **\_ состояние подписи XPS \_ \_** " означает, что части документа XPS, которые не должны быть подписаны, или части документа XPS, которые должны быть подписаны, не соответствуют. Если [**Проверка**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-verify) возвращает состояние подписи, дальнейшая проверка подписи будет необязательной.


```C++
            // continuing do loop from previous code example
            *signingCertificate = certificate;
            *signatureStatus = localSignatureStatus;
            
            // note that this test should only downgrade the 
            // signature status, it should not upgrade it.
            switch (localSignatureStatus) {
                case XPS_SIGNATURE_STATUS_VALID:
                case XPS_SIGNATURE_STATUS_QUESTIONABLE:
                    // the signature is valid or questionable so
                    // save the actual status and set the new status
                    // to questionable so the certificates will be checked.
                    localSignatureStatus = XPS_SIGNATURE_STATUS_QUESTIONABLE;
                    break;

                case XPS_SIGNATURE_STATUS_INCOMPLIANT:
                    // the signature is not compliant 
                    break;

                case XPS_SIGNATURE_STATUS_INCOMPLETE:
                case XPS_SIGNATURE_STATUS_BROKEN:
                    // The Windows 7 XPS viewer displays incomplete signatures
                    // and broken signatures as broken.
                    *signatureStatus = XPS_SIGNATURE_STATUS_BROKEN;
                    localSignatureStatus = XPS_SIGNATURE_STATUS_BROKEN;
                    break;

                default:
                    // there should be no other possible status values
                    break;
            }
            // do loop continues in next code example
```



Чтобы проверить доверие сертификата, если состояние подписи было допустимым или сомнительным, выполните следующие действия.

1.  Получение состояния доверия сертификата.
2.  Оцените возвращенное состояние доверия сертификата.
3.  Возврат полученного состояния.

Следующий пример кода не проверяет наличие всех возможных состояний доверия сертификатов. Дополнительные сведения о значениях состояния, которые могут быть возвращены, см. в разделе [**\_ \_ состояние доверия сертификатов**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_trust_status).


```C++
            // continuing do loop from previous code example
            //
            // at this point, localSignatureStatus should be less than or 
            // equal to what it was before the test.

            // Check the certificate to see if it is valid
            if ((localSignatureStatus == XPS_SIGNATURE_STATUS_VALID) || 
                (localSignatureStatus == XPS_SIGNATURE_STATUS_QUESTIONABLE))
            {
                // This call builds the certificate trust chain from the 
                //  supplied certificate.  The certificate chain is used to
                //  authenticate the supplied certificate.
                hr = GetCertificateTrustStatus (
                    *signingCertificate, 
                    &signatureCertificateStore,
                    &certificateStatus);
                if (FAILED(hr))
                {
                    // ERROR: An attempt to authenticate the certificate 
                    //  has failed
                    break; // out of do loop with failed hr
                }

                // The Crypt API returns a status that can contain more than
                //  one status value.
                // statusFlagMask is set to test all bits except for the
                //  CERT_TRUST_REVOCATION_STATUS_UNKNOWN
                //  CERT_TRUST_IS_OFFLINE_REVOCATION
                //  CERT_TRUST_IS_NOT_TIME_VALID
                //  values because, for this test, these are not considered
                //  to be error conditions.
                DWORD statusFlagMask = ~(
                    CERT_TRUST_REVOCATION_STATUS_UNKNOWN | 
                    CERT_TRUST_IS_OFFLINE_REVOCATION | 
                    CERT_TRUST_IS_NOT_TIME_VALID);

                if (CERT_TRUST_NO_ERROR == (certificateStatus & statusFlagMask))
                {
                    // If *signatureStatus is already 
                    //    XPS_SIGNATURE_STATUS_VALID then there is no need to 
                    //    change the status as the certificate status has no 
                    //    certificate trust errors.
                    // If *signatureStatus is already 
                    //  XPS_SIGNATURE_STATUS_QUESTIONABLE then we will not
                    //  upgrade the trust status of the signature just 
                    //  because there is no trust issue with the certificate.
                }
                else
                {
                    // If trust errors were detected with the certificate, 
                    //  then this XPS signature is given a status of 
                    //  XPS_SIGNATURE_STATUS_QUESTIONABLE
                    *signatureStatus = XPS_SIGNATURE_STATUS_QUESTIONABLE;
                }

                // Handle additional certificate errors.  
                //  This is not an exhaustive list of possible errors.

                if (certificateStatus & CERT_TRUST_IS_NOT_TIME_VALID)
                {
                    // The XPS Viewer considers signatures with 
                    //  expired certificates as valid.
                }
                if (certificateStatus & CERT_TRUST_IS_PARTIAL_CHAIN)
                {
                    // This test ensures that we only degrade the 
                    //  trust status and never upgrade it
                    if (XPS_SIGNATURE_STATUS_VALID == *signatureStatus)
                    {
                        *signatureStatus = XPS_SIGNATURE_STATUS_QUESTIONABLE;
                    }
                }

                if (certificateStatus & CERT_TRUST_IS_NOT_SIGNATURE_VALID)
                {
                    // This test ensures that we only degrade the 
                    //  trust status and never upgrade it
                    if (XPS_SIGNATURE_STATUS_VALID == *signatureStatus)
                    {
                        *signatureStatus = XPS_SIGNATURE_STATUS_QUESTIONABLE;
                    }
                }

                if (certificateStatus & CERT_TRUST_IS_SELF_SIGNED)
                {
                    // This test ensures that we only degrade the 
                    //  trust status and never upgrade it
                    if (XPS_SIGNATURE_STATUS_VALID == *signatureStatus)
                    {
                        *signatureStatus = XPS_SIGNATURE_STATUS_QUESTIONABLE;
                    }
                }
                
                if (certificateStatus & CERT_TRUST_IS_UNTRUSTED_ROOT)
                {
                    // This test ensures that we only degrade the 
                    //  trust status and never upgrade it
                    if (XPS_SIGNATURE_STATUS_VALID == *signatureStatus)
                    {
                        *signatureStatus = XPS_SIGNATURE_STATUS_QUESTIONABLE;
                    }
                }
            }//End if

            hr = certificatesInSignature->MoveNext(&moreCertificates);
            if (FAILED(hr))
            {
                // ERROR: could not move to the next 
                //  certificate in the enumerator
                break; // out of do loop with failed hr
            }
        } while((*signatureStatus != XPS_SIGNATURE_STATUS_VALID) && 
                    moreCertificates);
    } // end if successful

    if (NULL != certificatesInSignature) certificatesInSignature->Release();

    return hr;
}
```



В следующем примере кода состояние доверия сертификата получается путем вызова метода, показанного в следующем примере кода.


```C++
HRESULT GetCertificateTrustStatus(
    __in PCCERT_CONTEXT certificate,
    __in HCERTSTORE* certificateStore,
    __out DWORD* certificateStatus
)
{
    HRESULT    hr = S_OK;

    // The certificate chain that will be created from 
    //  the PCCERT_CONTEXT object passed in.  
    PCCERT_CHAIN_CONTEXT    certificateChain =    NULL;

    hr = CreateCertificateChain(
        certificate, 
        *certificateStore, 
        &certificateChain);

    if (SUCCEEDED(hr)) { 
        *certificateStatus = 
            certificateChain->TrustStatus.dwErrorStatus;
    }

    return hr;
}
```



Цепочка сертификатов, используемая в предыдущем примере кода, создается путем вызова метода, показанного в следующем примере кода.


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



## <a name="related-topics"></a>См. также

<dl> <dt>

**Используется в этом разделе**
</dt> <dt>

[**\_контекст цепочки сертификатов \_**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context)
</dt> <dt>

[**\_контекст сертификата**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[**\_состояние доверия \_ сертификатов**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_trust_status)
</dt> <dt>

[**цертаддцертификатеконтексттосторе**](/windows/desktop/api/wincrypt/nf-wincrypt-certaddcertificatecontexttostore)
</dt> <dt>

[**цертопенсторе**](/windows/desktop/api/wincrypt/nf-wincrypt-certopenstore)
</dt> <dt>

[**CertGetCertificateChain**](/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain)
</dt> <dt>

[**иопкцертификатинумератор**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopccertificateenumerator)
</dt> <dt>

[**Иопкцертификатинумератор:: OnCurrent**](/previous-versions/windows/desktop/api/msopc/nf-msopc-iopccertificateenumerator-getcurrent)
</dt> <dt>

[**Иопкцертификатинумератор:: MoveNext**](/previous-versions/windows/desktop/api/msopc/nf-msopc-iopccertificateenumerator-movenext)
</dt> <dt>

[**икспссигнатуре**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignature)
</dt> <dt>

[**Икспссигнатуре:: Жетцертификатинумератор**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-getcertificateenumerator)
</dt> <dt>

[**Икспссигнатуре:: Verify**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-verify)
</dt> <dt>

[**икспссигнатуреколлектион**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturecollection)
</dt> <dt>

[**Икспссигнатуреколлектион:: GetAt**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturecollection-getat)
</dt> <dt>

[**Икспссигнатуреколлектион:: NOCOUNT**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturecollection-getcount)
</dt> <dt>

[**икспссигнатуреманажер**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager)
</dt> <dt>

[**Икспссигнатуреманажер:: Signatures**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-getsignatures)
</dt> <dt>

[**\_состояние подписи \_ XPS**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_signature_status)
</dt> <dt>

**Дополнительные сведения**
</dt> <dt>

[Внедрение цепочек сертификатов в документ](embedding-certificate-trust-chains-in-a-document.md)
</dt> <dt>

[Ошибки API цифровой подписи XPS](xps-digital-signatures-errors.md)
</dt> <dt>

[Ошибки документа XPS](xps-document-errors.md)
</dt> <dt>

[XPS](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
