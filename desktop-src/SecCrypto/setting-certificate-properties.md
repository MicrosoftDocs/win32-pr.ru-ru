---
description: 'Чтобы задать свойства субъекта сертификата, используйте метод Ицертсерверполици:: Сетцертификатепроперти.'
ms.assetid: 93e4b05d-0230-4562-8052-4e118fd92057
title: Настройка свойств сертификата
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f33534792e65c95e24125968a61cf6ac1ad27039
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682392"
---
# <a name="setting-certificate-properties"></a>Настройка свойств сертификата

Чтобы задать свойства субъекта сертификата, используйте метод [**ицертсерверполици:: сетцертификатепроперти**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateproperty) . Свойства субъекта — это свойства, связанные с владельцем сертификата, или лицо, запросившего сертификат. Список свойств субъекта см. в разделе [Свойства имени](name-properties.md).

Можно также использовать метод [**сетцертификатепроперти**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateproperty) для задания свойств сертификата NotBefore и NotAfter. Описание свойств сертификата NotBefore и NotAfter см. в разделе [Свойства сертификата](certificate-properties.md).

Используйте метод [**ицертсерверполици:: сетцертификатикстенсион**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension) , чтобы добавить любое количество расширений в сертификат. Расширения можно использовать для добавления дополнительных сведений о субъекте или использовании в сертификат. Дополнительные сведения см. в разделе [обработчики расширений](extension-handlers.md).

В следующем примере задается свойство сертификата и расширение для сертификата. Методы [**сетцертификатепроперти**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateproperty) и [**сетцертификатикстенсион**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension) вызываются в реализации [**ICertPolicy2:: верифирекуест**](/windows/desktop/api/Certpol/nf-certpol-icertpolicy-verifyrequest) . Пример не является полной реализацией **верифирекуест** ; в примере не показана логика проверки.


```C++
#include <windows.h>
#include <stdio.h>

STDMETHODIMP CCertPolicy::VerifyRequest(
             BSTR const strConfig,
             LONG Context,
             LONG bNewRequest,
             LONG Flags,
             LONG __RPC_FAR *pDisposition)
{
    HRESULT hr = S_OK;
    ICertServerPolicy *pServer = NULL;
    BSTR bstrPropName = NULL;
    VARIANT vPropValue;
    BSTR bstrExtName = NULL;
    VARIANT vExtValue;


    // Retrieve an ICertServerPolicy interface pointer.
    hr = CoCreateInstance( CLSID_CCertServerPolicy,
                           NULL,
                           CLSCTX_INPROC_SERVER,
                           IID_ICertServerPolicy,
                           (void **) &pServer );
    if (FAILED( hr ))
    {
        printf("Failed CoCreateInstance for ICertServerPolicy "
            "- %x\n", hr );
        return hr;
    }

    // Set the context to which this request refers.
    hr = pServer->SetContext(Context);
    if (FAILED( hr ))
    {
        printf("Failed SetContext(%u) - %x\n", Context, hr );
        pServer->Release();
        return hr;
    }

    // Specify the subject property to set on the certificate.
    bstrPropName = SysAllocString(L"Subject.EMail");
    if ( NULL == bstrPropName )
    {
        hr = E_OUTOFMEMORY; 
        printf("Failed SysAllocString for bstrPropName "
            "(no memory)\n" );
        pServer->Release();
        return hr;
    }

    VariantInit( &vPropValue );
    vPropValue.VT_BSTR;
    vPropValue.bstrVal = SysAllocString(L"someone@example.com");
    if ( NULL == vPropValue.bstrVal )
    {
        hr = E_OUTOFMEMORY; 
        printf("Failed SysAllocString for vPropValue "
            "(no memory)\n" );
        SysFreeString(bstrPropName);
        pServer->Release();
        return hr;
    }

    // Set the subject property on the certificate.
    hr = pServer->SetCertificateProperty( bstrPropName,
                                          PROPTYPE_STRING,
                                          &vPropValue );
    SysFreeString(bstrPropName);
    VariantClear(&vPropValue);
    if (FAILED(hr))
    {
        printf("Failed SetCertificateProperty - %x\n", hr);
        pServer->Release();
        return hr;
    }

    // Specify the extension property to set on the certificate.
    bstrExtName = SysAllocString(L"2.29.38.4");
    if ( NULL == bstrExtName )
    {
        hr = E_OUTOFMEMORY; 
        printf("Failed SysAllocString for bstrExtName "
            "(no memory)\n" );
        pServer->Release();
        return hr;
    }

    VariantInit( &vExtValue );
    vExtValue.VT_BSTR;
    vExtValue.bstrVal = SysAllocString
        (L"https://example.microsoft.com");
    if ( NULL == vExtValue.bstrVal )
    {
        hr = E_OUTOFMEMORY; 
        printf("Failed SysAllocString for vExtValue (no memory)\n" );
        SysFreeString(bstrExtName);
        pServer->Release();
        return hr;
    }

    // Set the extension property on the certificate.
    hr = pServer->SetCertificateExtension( bstrExtName,
                                           PROPTYPE_STRING,
                                           EXTENSION_CRITICAL_FLAG,
                                           &vExtValue );
    SysFreeString(bstrExtName);
    VariantClear(&vExtValue);
    if (FAILED(hr))
    {
        printf("Failed SetCertificateExtension - %x\n", hr);
        pServer->Release();
        return hr;
    }

    pServer->Release();
    return(hr);

}
```



 

 



