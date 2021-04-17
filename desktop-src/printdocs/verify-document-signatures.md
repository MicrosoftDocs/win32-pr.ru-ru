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
# <a name="verify-document-signatures-and-certificates"></a><span data-ttu-id="becfd-103">Проверка подписей документов и сертификатов</span><span class="sxs-lookup"><span data-stu-id="becfd-103">Verify Document Signatures and Certificates</span></span>

<span data-ttu-id="becfd-104">В этом разделе описывается проверка подписей в документе XPS и проверка сертификатов, связанных с этими подписями.</span><span class="sxs-lookup"><span data-stu-id="becfd-104">This topic describes how to verify the signatures in an XPS document and how to verify the certificates that are related to those signatures.</span></span>

<span data-ttu-id="becfd-105">Прежде чем использовать приведенные ниже примеры кода в программе, ознакомьтесь со сведениями об отказе в [типичных задачах программирования цифровых подписей](basic-digital-signature-programming-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="becfd-105">Before using the following code examples in your program, read the disclaimer in [Common Digital Signature Programming Tasks](basic-digital-signature-programming-tasks.md).</span></span>

<span data-ttu-id="becfd-106">В следующем примере кода выполняется проверка цифровых подписей, найденных в документе XPS.</span><span class="sxs-lookup"><span data-stu-id="becfd-106">The following code example checks the digital signatures that are found in an XPS document.</span></span>

<span data-ttu-id="becfd-107">Чтобы проверить подписи в документе XPS, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="becfd-107">To check the signatures in an XPS document, perform the following steps:</span></span>

1.  <span data-ttu-id="becfd-108">Загрузите документ в диспетчер подписей, как описано в разделе [Инициализация диспетчера подписей](initialize-the-signature-manager.md).</span><span class="sxs-lookup"><span data-stu-id="becfd-108">Load the document into a signature manager, as described in [Initialize the Signature Manager](initialize-the-signature-manager.md).</span></span>
2.  <span data-ttu-id="becfd-109">Получение коллекции подписей из диспетчера цифровых подписей.</span><span class="sxs-lookup"><span data-stu-id="becfd-109">Get the collection of signatures from the digital signature manager.</span></span>
3.  <span data-ttu-id="becfd-110">Возвращает количество подписей в коллекции.</span><span class="sxs-lookup"><span data-stu-id="becfd-110">Get the number of signatures in the collection.</span></span>
4.  <span data-ttu-id="becfd-111">Для каждой сигнатуры в коллекции вызовите метод [**Verify**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-verify) , как показано в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="becfd-111">For each signature in the collection, call the [**Verify**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-verify) method as shown in the code example that follows.</span></span>


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



<span data-ttu-id="becfd-112">Чтобы проверить цифровую подпись, сначала проверьте подпись, созданную сертификатом подписи, а затем проверьте сертификат подписи.</span><span class="sxs-lookup"><span data-stu-id="becfd-112">To verify a digital signature, first verify the signature created by the signing certificate, then validate the signing certificate.</span></span> <span data-ttu-id="becfd-113">Метод проверки, используемый в следующем примере кода, кэширует сертификаты во временном хранилище сертификатов, которое используется функциями шифрования API, когда они вызываются далее в этом примере.</span><span class="sxs-lookup"><span data-stu-id="becfd-113">The validation method used in the following code example caches the certificates in a temporary certificate store, which the Crypto API functions use when they are called later in this example.</span></span>

<span data-ttu-id="becfd-114">Чтобы создать временное хранилище сертификатов, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="becfd-114">To create a temporary certificate store, perform the following steps:</span></span>

1.  <span data-ttu-id="becfd-115">Создайте временное хранилище сертификатов для хранения сертификатов, используемых сигнатурой.</span><span class="sxs-lookup"><span data-stu-id="becfd-115">Create a temporary certificate store to hold the certificates used by the signature.</span></span>
2.  <span data-ttu-id="becfd-116">Выполните итерацию по набору сертификатов подписи и загрузите каждый сертификат во временное хранилище сертификатов.</span><span class="sxs-lookup"><span data-stu-id="becfd-116">Iterate through the signature's certificate set, and load each certificate into the temporary certificate store.</span></span>


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



<span data-ttu-id="becfd-117">Чтобы проверить цифровую подпись и сертификат, используемый для подписания документа, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="becfd-117">To verify the digital signature and the certificate used to sign the document, perform the following steps:</span></span>

1.  <span data-ttu-id="becfd-118">Найдите сертификат для подписи, просматривая сертификаты, которые используются в сигнатуре.</span><span class="sxs-lookup"><span data-stu-id="becfd-118">Find the signing certificate by iterating through the certificates that are used by the signature.</span></span>
2.  <span data-ttu-id="becfd-119">Протестируйте сертификат, проверив его подпись по сертификату.</span><span class="sxs-lookup"><span data-stu-id="becfd-119">Test the certificate by verifying the signature against the certificate.</span></span> <span data-ttu-id="becfd-120">Сертификат подписи находится в том случае, если метод [**Verify**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-verify) возвращает [**\_ \_ состояние подписи**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_signature_status) XPS, **\_ \_ \_ допустимое состояние подписи XPS** или **\_ \_ состояние подписи \_ XPS**, и не возвращает ошибку **\_ безопасности средства** .</span><span class="sxs-lookup"><span data-stu-id="becfd-120">The signing certificate is found when the [**Verify**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-verify) method returns an [**XPS\_SIGNATURE\_STATUS**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_signature_status) of **XPS\_SIGNATURE\_STATUS\_VALID** or **XPS\_SIGNATURE\_STATUS\_QUESTIONABLE**, and does not return a **FACILITY\_SECURITY** error.</span></span>


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



<span data-ttu-id="becfd-121">После обнаружения сертификата для подписи выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="becfd-121">When the signing certificate has been found, perform the following steps:</span></span>

1.  <span data-ttu-id="becfd-122">Сохраните возвращенное состояние подписи.</span><span class="sxs-lookup"><span data-stu-id="becfd-122">Save the returned signature status.</span></span>
2.  <span data-ttu-id="becfd-123">При необходимости обновите локальное состояние, чтобы выполнить последующие проверки сертификатов:</span><span class="sxs-lookup"><span data-stu-id="becfd-123">Update the local status, if necessary, to perform subsequent certificate tests:</span></span>
    1.  <span data-ttu-id="becfd-124">Если состояние подписи — "успешно", присвойте локальному состоянию значение "вопрос", чтобы проверить сертификаты.</span><span class="sxs-lookup"><span data-stu-id="becfd-124">If the signature status is successful, set the local status to questionable in order to test the certificates.</span></span>
    2.  <span data-ttu-id="becfd-125">Если состояние подписи не соответствует требованиям, оставьте локальное состояние несоответствующим.</span><span class="sxs-lookup"><span data-stu-id="becfd-125">If the signature status is incompliant, leave the local status as incompliant.</span></span>
    3.  <span data-ttu-id="becfd-126">Если подпись имеет состояние "нарушена" или "неполная", установите локальное состояние "нарушено".</span><span class="sxs-lookup"><span data-stu-id="becfd-126">If the signature status is broken or incomplete, set the local status to broken.</span></span>

<span data-ttu-id="becfd-127">Состояние подписи " **\_ состояние подписи XPS \_ \_** " означает, что части документа XPS, которые не должны быть подписаны, или части документа XPS, которые должны быть подписаны, не соответствуют.</span><span class="sxs-lookup"><span data-stu-id="becfd-127">A signature status of **XPS\_SIGNATURE\_STATUS\_INCOMPLIANT** means that parts of the XPS document that should not have been signed were signed, or parts of the XPS document that should have been signed were not.</span></span> <span data-ttu-id="becfd-128">Если [**Проверка**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-verify) возвращает состояние подписи, дальнейшая проверка подписи будет необязательной.</span><span class="sxs-lookup"><span data-stu-id="becfd-128">If [**Verify**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-verify) returns this signature status, further checking of the signature will be unnecessary.</span></span>


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



<span data-ttu-id="becfd-129">Чтобы проверить доверие сертификата, если состояние подписи было допустимым или сомнительным, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="becfd-129">To verify the certificate trust if the signature status was valid or questionable, perform the following steps:</span></span>

1.  <span data-ttu-id="becfd-130">Получение состояния доверия сертификата.</span><span class="sxs-lookup"><span data-stu-id="becfd-130">Get the certificate trust status.</span></span>
2.  <span data-ttu-id="becfd-131">Оцените возвращенное состояние доверия сертификата.</span><span class="sxs-lookup"><span data-stu-id="becfd-131">Evaluate the returned certificate trust status.</span></span>
3.  <span data-ttu-id="becfd-132">Возврат полученного состояния.</span><span class="sxs-lookup"><span data-stu-id="becfd-132">Return the resulting status.</span></span>

<span data-ttu-id="becfd-133">Следующий пример кода не проверяет наличие всех возможных состояний доверия сертификатов.</span><span class="sxs-lookup"><span data-stu-id="becfd-133">The next code example does not test for every possible certificate trust status.</span></span> <span data-ttu-id="becfd-134">Дополнительные сведения о значениях состояния, которые могут быть возвращены, см. в разделе [**\_ \_ состояние доверия сертификатов**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_trust_status).</span><span class="sxs-lookup"><span data-stu-id="becfd-134">For additional details on the status values that can be returned, see [**CERT\_TRUST\_STATUS**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_trust_status).</span></span>


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



<span data-ttu-id="becfd-135">В следующем примере кода состояние доверия сертификата получается путем вызова метода, показанного в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="becfd-135">In the next code example, the certificate trust status is obtained by calling the method shown in the code example that follows.</span></span>


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



<span data-ttu-id="becfd-136">Цепочка сертификатов, используемая в предыдущем примере кода, создается путем вызова метода, показанного в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="becfd-136">The certificate chain used in the preceding code example is created by calling the method shown in the following code example.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="becfd-137">См. также</span><span class="sxs-lookup"><span data-stu-id="becfd-137">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="becfd-138">**Используется в этом разделе**</span><span class="sxs-lookup"><span data-stu-id="becfd-138">**Used in This Section**</span></span>
</dt> <dt>

[<span data-ttu-id="becfd-139">**\_контекст цепочки сертификатов \_**</span><span class="sxs-lookup"><span data-stu-id="becfd-139">**CERT\_CHAIN\_CONTEXT**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context)
</dt> <dt>

[<span data-ttu-id="becfd-140">**\_контекст сертификата**</span><span class="sxs-lookup"><span data-stu-id="becfd-140">**CERT\_CONTEXT**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[<span data-ttu-id="becfd-141">**\_состояние доверия \_ сертификатов**</span><span class="sxs-lookup"><span data-stu-id="becfd-141">**CERT\_TRUST\_STATUS**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-cert_trust_status)
</dt> <dt>

[<span data-ttu-id="becfd-142">**цертаддцертификатеконтексттосторе**</span><span class="sxs-lookup"><span data-stu-id="becfd-142">**CertAddCertificateContextToStore**</span></span>](/windows/desktop/api/wincrypt/nf-wincrypt-certaddcertificatecontexttostore)
</dt> <dt>

[<span data-ttu-id="becfd-143">**цертопенсторе**</span><span class="sxs-lookup"><span data-stu-id="becfd-143">**CertOpenStore**</span></span>](/windows/desktop/api/wincrypt/nf-wincrypt-certopenstore)
</dt> <dt>

[<span data-ttu-id="becfd-144">**CertGetCertificateChain**</span><span class="sxs-lookup"><span data-stu-id="becfd-144">**CertGetCertificateChain**</span></span>](/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain)
</dt> <dt>

[<span data-ttu-id="becfd-145">**иопкцертификатинумератор**</span><span class="sxs-lookup"><span data-stu-id="becfd-145">**IOpcCertificateEnumerator**</span></span>](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopccertificateenumerator)
</dt> <dt>

[<span data-ttu-id="becfd-146">**Иопкцертификатинумератор:: OnCurrent**</span><span class="sxs-lookup"><span data-stu-id="becfd-146">**IOpcCertificateEnumerator::GetCurrent**</span></span>](/previous-versions/windows/desktop/api/msopc/nf-msopc-iopccertificateenumerator-getcurrent)
</dt> <dt>

[<span data-ttu-id="becfd-147">**Иопкцертификатинумератор:: MoveNext**</span><span class="sxs-lookup"><span data-stu-id="becfd-147">**IOpcCertificateEnumerator::MoveNext**</span></span>](/previous-versions/windows/desktop/api/msopc/nf-msopc-iopccertificateenumerator-movenext)
</dt> <dt>

[<span data-ttu-id="becfd-148">**икспссигнатуре**</span><span class="sxs-lookup"><span data-stu-id="becfd-148">**IXpsSignature**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignature)
</dt> <dt>

[<span data-ttu-id="becfd-149">**Икспссигнатуре:: Жетцертификатинумератор**</span><span class="sxs-lookup"><span data-stu-id="becfd-149">**IXpsSignature::GetCertificateEnumerator**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-getcertificateenumerator)
</dt> <dt>

[<span data-ttu-id="becfd-150">**Икспссигнатуре:: Verify**</span><span class="sxs-lookup"><span data-stu-id="becfd-150">**IXpsSignature::Verify**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-verify)
</dt> <dt>

[<span data-ttu-id="becfd-151">**икспссигнатуреколлектион**</span><span class="sxs-lookup"><span data-stu-id="becfd-151">**IXpsSignatureCollection**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturecollection)
</dt> <dt>

[<span data-ttu-id="becfd-152">**Икспссигнатуреколлектион:: GetAt**</span><span class="sxs-lookup"><span data-stu-id="becfd-152">**IXpsSignatureCollection::GetAt**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturecollection-getat)
</dt> <dt>

[<span data-ttu-id="becfd-153">**Икспссигнатуреколлектион:: NOCOUNT**</span><span class="sxs-lookup"><span data-stu-id="becfd-153">**IXpsSignatureCollection::GetCount**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturecollection-getcount)
</dt> <dt>

[<span data-ttu-id="becfd-154">**икспссигнатуреманажер**</span><span class="sxs-lookup"><span data-stu-id="becfd-154">**IXpsSignatureManager**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager)
</dt> <dt>

[<span data-ttu-id="becfd-155">**Икспссигнатуреманажер:: Signatures**</span><span class="sxs-lookup"><span data-stu-id="becfd-155">**IXpsSignatureManager::GetSignatures**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-getsignatures)
</dt> <dt>

[<span data-ttu-id="becfd-156">**\_состояние подписи \_ XPS**</span><span class="sxs-lookup"><span data-stu-id="becfd-156">**XPS\_SIGNATURE\_STATUS**</span></span>](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_signature_status)
</dt> <dt>

<span data-ttu-id="becfd-157">**Дополнительные сведения**</span><span class="sxs-lookup"><span data-stu-id="becfd-157">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="becfd-158">Внедрение цепочек сертификатов в документ</span><span class="sxs-lookup"><span data-stu-id="becfd-158">Embed Certificate Chains in a Document</span></span>](embedding-certificate-trust-chains-in-a-document.md)
</dt> <dt>

[<span data-ttu-id="becfd-159">Ошибки API цифровой подписи XPS</span><span class="sxs-lookup"><span data-stu-id="becfd-159">XPS Digital Signature API Errors</span></span>](xps-digital-signatures-errors.md)
</dt> <dt>

[<span data-ttu-id="becfd-160">Ошибки документа XPS</span><span class="sxs-lookup"><span data-stu-id="becfd-160">XPS Document Errors</span></span>](xps-document-errors.md)
</dt> <dt>

[<span data-ttu-id="becfd-161">XPS</span><span class="sxs-lookup"><span data-stu-id="becfd-161">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
