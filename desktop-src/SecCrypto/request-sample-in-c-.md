---
description: В следующем примере показано, как можно использовать элемент управления регистрации сертификатов с объектом интерфейса ICertRequest для создания и отправки запроса на сертификат.
ms.assetid: 2816e1f8-c4be-4905-b070-6e67255811d4
title: Пример запроса в C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43dbcaea567ed6d6427ab17cf1b99c0a41807651
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104423957"
---
# <a name="request-sample-in-c"></a><span data-ttu-id="a5c82-103">Пример запроса в C++</span><span class="sxs-lookup"><span data-stu-id="a5c82-103">Request Sample in C++</span></span>

<span data-ttu-id="a5c82-104">В следующем примере показано, как можно использовать элемент управления регистрации сертификатов с объектом [**интерфейса ICertRequest**](/windows/desktop/api/Certcli/nn-certcli-icertrequest) для создания и отправки запроса на сертификат.</span><span class="sxs-lookup"><span data-stu-id="a5c82-104">The following example shows how the Certificate Enrollment Control can be used with the [**ICertRequest**](/windows/desktop/api/Certcli/nn-certcli-icertrequest) object to create and submit a certificate request.</span></span>


```C++
// Copyright (C) Microsoft.  All rights reserved.
// Example for Certificate Enrollment Control
// used with ICertRequest in C++
// 

#include <stdio.h>
#include <Certsrv.h> // for ICertRequest object
#include <xenroll.h>
#include <windows.h>

HRESULT __cdecl main()
{

    // Pointer to interface objects.
    ICEnroll4 * pEnroll = NULL;
    ICertRequest2 * pRequest = NULL;

    // BSTR variables.
    BSTR    bstrDN = NULL;
    BSTR    bstrOID = NULL;
    BSTR    bstrCertAuth = NULL;
    BSTR    bstrReq = NULL;
    BSTR    bstrAttrib = NULL;

    // Request disposition variable.
    long    nDisp;

    // Variable for return value.
    HRESULT    hr;

    // Initialize COM.
    hr = CoInitializeEx( NULL, COINIT_APARTMENTTHREADED );

    // Check status.
    if ( FAILED( hr ) )
    {
        printf("Failed CoInitializeEx - [%x]\n", hr);
        goto error;
    }

    // Create an instance of the Certificate Enrollment object.
    hr = CoCreateInstance( CLSID_CEnroll,
                           NULL,
                           CLSCTX_INPROC_SERVER,
                           IID_ICEnroll4,
                           (void **)&pEnroll);
    // Check status.
    if ( FAILED( hr ) )
    {
        printf("Failed CoCreateInstance - pEnroll [%x]\n", hr);
        goto error;
    }

    // Create an instance of the Certificate Request object.
    hr = CoCreateInstance( CLSID_CCertRequest,
                           NULL,
                           CLSCTX_INPROC_SERVER,
                           IID_ICertRequest2,
                           (void **)&pRequest);
    // Check status.
    if ( FAILED( hr ) )
    {
        printf("Failed CoCreateInstance - pRequest [%x]\n", hr);
        goto error;
    }

    // Create the data for the request.
    // A user interface or database retrieval could
    // be used instead of this sample's hard-coded text.
    bstrDN = SysAllocString(L"CN=UserName"    // Common Name
                            L",OU=UserUnit"   // Org Unit
                            L",O=UserOrg"     // Org
                            L",L=UserCity"    // Locality
                            L",S=WA"          // State
                            L",C=US");        // Country/Region
    if (NULL == bstrDN)
    {
        printf("Failed SysAllocString\n");
        goto error;
    }

    // Allocate the BSTR representing the certification authority.
    // Note the use of '\\' to produce a single '\' in C++.
    bstrCertAuth = SysAllocString(L"Server\\CertAuth");
    if (NULL == bstrCertAuth)
    {
        printf("Failed SysAllocString\n");
        goto error;
    }

    // Allocate the BSTR for the certificate usage.
    bstrOID = SysAllocString(L"1.3.6.1.4.1.311.2.1.21");
    if (NULL == bstrOID)
    {
        printf("Failed SysAllocString\n");
        goto error;
    }

    // Allocate the BSTR for the attributes.
    // In this case, no attribute is specified.
    bstrAttrib = SysAllocString(L"");
    if (NULL == bstrAttrib)
    {
        printf("Failed SysAllocString\n");
        goto error;
    }

    // Create the PKCS #10.
    hr = pEnroll->createPKCS10( bstrDN, bstrOID, &bstrReq );
    // check status
    if ( FAILED( hr ) )
    {
        printf("Failed createPKCS10 - [%x]\n", hr);
        goto error;
    }

    // Submit the certificate request.
    hr = pRequest->Submit( CR_IN_BASE64 | CR_IN_PKCS10,
                           bstrReq,
                           bstrAttrib,
                           bstrCertAuth,
                           &nDisp );
    // Check status.
    if ( FAILED( hr ) )
    {
        printf("Failed Request Submit - [%x]\n", hr);
        goto error;
    }
    else
        printf("Request submitted; disposition = %d\n", nDisp );

error:

    // Done processing.
    // Clean up object resources.
    if ( NULL != pEnroll )
        pEnroll->Release();
    if ( NULL != pRequest )
        pRequest->Release();

    // Free BSTR variables.
    if ( NULL != bstrDN )
        SysFreeString ( bstrDN );
    if ( NULL != bstrOID )
        SysFreeString ( bstrOID );
    if ( NULL != bstrCertAuth )
        SysFreeString ( bstrCertAuth );
    if ( NULL != bstrReq )
        SysFreeString ( bstrReq );
    if ( NULL != bstrAttrib )
        SysFreeString ( bstrAttrib );

    // Free COM resources.
    CoUninitialize();

    return hr;
}
```



 

 



