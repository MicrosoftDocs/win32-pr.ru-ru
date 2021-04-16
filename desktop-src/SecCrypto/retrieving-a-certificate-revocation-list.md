---
description: Демонстрирует получение списка отзыва сертификатов.
ms.assetid: b8fbffae-d968-453d-81f0-af9d60be5fa9
title: Получение списка отзыва сертификатов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e9c7933ac5762c9367d7bdff150da011f789835
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664389"
---
# <a name="retrieving-a-certificate-revocation-list"></a>Получение списка отзыва сертификатов

[*Центр сертификации*](../secgloss/c-gly.md) (ЦС) отвечает за публикацию [*списка отзыва сертификатов*](../secgloss/c-gly.md) (CRL). Текущий список отзыва сертификатов можно получить с помощью метода [**ICertAdmin2:: жеткрл**](/windows/desktop/api/Certadm/nf-certadm-icertadmin-getcrl) . В случае продления сертификата ЦС может потребоваться получить списки отзыва сертификатов для предыдущих сертификатов ЦС. Сведения об обновлении ЦС см. в разделе [продление центра сертификации](certification-authority-renewal.md). Кроме того, ЦС может публиковать разностные CRL. Чтобы получить CRL для обновленных сертификатов ЦС или разностных CRL, используйте методы [**ICertAdmin2:: жеткапроперти**](/windows/desktop/api/Certadm/nf-certadm-icertadmin2-getcaproperty) или [**ICertRequest2:: жеткапроперти**](/windows/desktop/api/Certcli/nf-certcli-icertrequest2-getcaproperty) .

В следующем примере показано получение текущего списка отзыва сертификатов.


```C++
    ICertAdmin2 * pCertAdmin2 = NULL;  // pointer to interface object
    BSTR bstrCA = NULL;  // variable for computer\CAname
    BSTR bstrCRL = NULL;  // variable to contain the retrieved CRL
    HRESULT hr;

    // Initialize COM.
    hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
    if (FAILED(hr))
    {
        printf("Failed CoInitializeEx [%x]\n", hr);
        goto error;
    }

    // Create the CertAdmin object,
    // and get a pointer to its ICertAdmin interface.
    hr = CoCreateInstance( CLSID_CCertAdmin,
                           NULL,
                           CLSCTX_INPROC_SERVER,
                           IID_ICertAdmin2,
                           (void **)&pCertAdmin2;);
    if (FAILED(hr))
    {
        printf("Failed CoCreateInstance pCertAdmin2 [%x]\n", hr);
        goto error;
    }

    // Note the use of two '\' in C++ to produce one '\'.
    bstrCA = SysAllocString(L"<COMPUTERNAMEHERE>\\<CANAMEHERE>");
    if (FAILED(hr))
    {
        printf("Failed to allocate memory for bstrCA\n");
        goto error;
    }

    // Retrieve the CRL.
    hr = pCertAdmin2->GetCRL( bstrCA, CR_OUT_BINARY, &bstrCRL );
    if (FAILED(hr))
    {
        printf("Failed GetCRL [%x]\n", hr);
        goto error;
    }
    else
        printf("CRL retrieved successfully\n");
        // Use the CRL as needed...

    // Processing is finished.

error:

    // Free BSTR values.
    if (NULL != bstrCA)
        SysFreeString(bstrCA);

    if (NULL != bstrCRL)
        SysFreeString(bstrCRL);

    // Clean up object resources.
    if (NULL != pCertAdmin2)
        pCertAdmin2->Release();

    // Free COM resources.
    CoUninitialize();
```



В следующем примере показано получение базового и разностного списка отзыва сертификатов, включая те, которые были обновлены сертификатами ЦС. В примере используется [**ICertAdmin2:: жеткапроперти**](/windows/desktop/api/Certadm/nf-certadm-icertadmin2-getcaproperty), хотя [**ICertRequest2:: жеткапроперти**](/windows/desktop/api/Certcli/nf-certcli-icertrequest2-getcaproperty) предоставляет аналогичные функциональные возможности.


```C++
    LONG nCACertCount, nIndex, nCRLState;
    VARIANT    variant;

    VariantInit(&variant);
    // Determine the number of CA certificates.
    hr = pCertAdmin2->GetCAProperty(bstrCA, 
                                CR_PROP_CASIGCERTCOUNT,
                                0,
                                PROPTYPE_LONG, 
                                CR_OUT_BINARY, 
                                &variant);
    if (FAILED(hr))
    {
        printf("Failed call to GetCAProperty - "
            "CR_PROP_CASIGCERTCOUNT\n");
        goto error;
    }
    nCACertCount = variant.lVal;

    for (nIndex = 0; nIndex < nCACertCount; nIndex++)
    {
           // Determine the CRL state for each certificate index.
           pCertAdmin2->GetCAProperty(bstrCA, 
                               CR_PROP_CRLSTATE, 
                               nIndex, 
                               PROPTYPE_LONG, 
                               CR_OUT_BINARY, 
                               &variant);
        if (FAILED(hr))
        {
            printf("Failed call to GetCAProperty - "
                "CR_PROP_CRLSTATE\n");
            goto error;
        }
        nCRLState = variant.lVal;

        // Process certificate indices only when 
        // the CRL state is valid.
        if (CA_DISP_VALID == nCRLState)
        {
           // Retrieve the base CRL.
           hr = pCertAdmin2->GetCAProperty(bstrCA,
                                   CR_PROP_BASECRL, 
                                   nIndex, 
                                   PROPTYPE_BINARY,
                                   CR_OUT_BINARY, 
                                   &variant);
           if (FAILED(hr))
           {
               printf("Failed call to GetCAProperty - "
                   "CR_PROP_BASECRL\n");
               goto error;
           }

           // Use the base CRL as needed (not shown).
           // ...

           // Retrieve the delta CRL.
           hr = pCertAdmin2->GetCAProperty(bstrCA, 
                                   CR_PROP_DELTACRL, 
                                   nIndex, 
                                   PROPTYPE_BINARY, 
                                   CR_OUT_BINARY, 
                                   &variant);
           if (FAILED(hr))
           {
               printf("Failed call to GetCAProperty - "
                   "CR_PROP_DELTACRL\n");
               goto error;
           }

           // Use the delta CRL as needed (not shown).
           // ...

       }        
    }
    
    // Processing is finished.

error:

    // Clean up object resources.
    if ( NULL != pCertAdmin2 )
        pCertAdmin2->Release();

    // Free BSTR variables.
    if ( NULL != bstrCA )
        SysFreeString ( bstrCA );

    // Clear the variant.
    VariantClear(&variant);
```



 

 
