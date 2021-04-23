---
description: Демонстрирует, как запросить архивный сертификат ключа.
ms.assetid: a09f55c1-fb27-41e7-9a2f-617d2360c02f
title: Запрос архивного сертификата ключа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da1f69338ed4a41986700853ef5d46ee08612e8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911268"
---
# <a name="requesting-a-key-archival-certificate"></a><span data-ttu-id="936e0-103">Запрос архивного сертификата ключа</span><span class="sxs-lookup"><span data-stu-id="936e0-103">Requesting a Key Archival Certificate</span></span>

<span data-ttu-id="936e0-104">В следующем примере показано создание и отправка [*запроса на сертификат*](../secgloss/c-gly.md) и получение результирующего архивного сертификата ключа.</span><span class="sxs-lookup"><span data-stu-id="936e0-104">The following example shows creating and submitting a [*certificate request*](../secgloss/c-gly.md) and receiving the resulting key archival certificate.</span></span> <span data-ttu-id="936e0-105">Чтобы выполнить этот пример, [*центр сертификации*](../secgloss/c-gly.md) (ЦС), получающий запрос на сертификат, должен быть настроен для архивирования ключей.</span><span class="sxs-lookup"><span data-stu-id="936e0-105">For this example to succeed, the [*certification authority*](../secgloss/c-gly.md) (CA) that receives the certificate request must be configured for key archival.</span></span>

<span data-ttu-id="936e0-106">Следующие шаги описывают создание и отправку запроса на сертификат.</span><span class="sxs-lookup"><span data-stu-id="936e0-106">The following steps describe how to create and submit a certificate request.</span></span>

<span data-ttu-id="936e0-107">**Создание и отправка запроса на сертификат**</span><span class="sxs-lookup"><span data-stu-id="936e0-107">**To create and submit a certificate request**</span></span>

1.  <span data-ttu-id="936e0-108">Получите сертификат Exchange ЦС с помощью метода [**ICertRequest2:: жеткацертификате**](/windows/desktop/api/Certcli/nf-certcli-icertrequest-getcacertificate) .</span><span class="sxs-lookup"><span data-stu-id="936e0-108">Retrieve the CA's exchange certificate using the [**ICertRequest2::GetCACertificate**](/windows/desktop/api/Certcli/nf-certcli-icertrequest-getcacertificate) method.</span></span>
2.  <span data-ttu-id="936e0-109">Укажите, что полученный сертификат обмена ЦС является сертификатом резервного архива с помощью свойства [**ICEnroll4::P риватекэйарчивецертификате**](/windows/desktop/api/Xenroll/nf-xenroll-icenroll4-get_privatekeyarchivecertificate) .</span><span class="sxs-lookup"><span data-stu-id="936e0-109">Specify that the retrieved CA exchange certificate is the key archive certificate using the [**ICEnroll4::PrivateKeyArchiveCertificate**](/windows/desktop/api/Xenroll/nf-xenroll-icenroll4-get_privatekeyarchivecertificate) property.</span></span>
3.  <span data-ttu-id="936e0-110">Создайте запрос на сертификат CMC с помощью метода [**ICEnroll4:: креатерекуест**](/windows/desktop/api/Xenroll/nf-xenroll-icenroll4-createrequest) .</span><span class="sxs-lookup"><span data-stu-id="936e0-110">Create a CMC certificate request using the [**ICEnroll4::createRequest**](/windows/desktop/api/Xenroll/nf-xenroll-icenroll4-createrequest) method.</span></span>
4.  <span data-ttu-id="936e0-111">Отправьте запрос сертификата в центр сертификации с помощью метода [**ICertRequest2:: submit**](/windows/desktop/api/Certcli/nf-certcli-icertrequest-submit) .</span><span class="sxs-lookup"><span data-stu-id="936e0-111">Submit the certificate request to a CA using the [**ICertRequest2::Submit**](/windows/desktop/api/Certcli/nf-certcli-icertrequest-submit) method.</span></span> <span data-ttu-id="936e0-112">ЦС должен быть настроен для поддержки архивирования ключей.</span><span class="sxs-lookup"><span data-stu-id="936e0-112">The CA must be configured to support key archival.</span></span>

<span data-ttu-id="936e0-113">Следующие шаги описывают, как получить выданный сертификат для архивирования ключей.</span><span class="sxs-lookup"><span data-stu-id="936e0-113">The following steps describe how to retrieve the issued certificate for key archival purposes.</span></span>

<span data-ttu-id="936e0-114">**Получение выданного сертификата для архивирования ключей**</span><span class="sxs-lookup"><span data-stu-id="936e0-114">**To retrieve the issued certificate for key archival purposes**</span></span>

1.  <span data-ttu-id="936e0-115">Получите полный ответ, включая выданный сертификат, с помощью метода [**ICertRequest2:: жетфуллреспонсепроперти**](/windows/desktop/api/Certcli/nf-certcli-icertrequest2-getfullresponseproperty) .</span><span class="sxs-lookup"><span data-stu-id="936e0-115">Retrieve the full response, including the issued certificate, using the [**ICertRequest2::GetFullResponseProperty**](/windows/desktop/api/Certcli/nf-certcli-icertrequest2-getfullresponseproperty) method.</span></span>
2.  <span data-ttu-id="936e0-116">Установите выданный сертификат с помощью метода [**ICEnroll4:: акцептреспонсе**](/windows/desktop/api/Xenroll/nf-xenroll-icenroll4-acceptresponse) .</span><span class="sxs-lookup"><span data-stu-id="936e0-116">Install the issued certificate using the [**ICEnroll4::acceptResponse**](/windows/desktop/api/Xenroll/nf-xenroll-icenroll4-acceptresponse) method.</span></span>

<span data-ttu-id="936e0-117">В следующем примере показано создание и отправка запроса на сертификат и получение результирующего архивного сертификата ключа.</span><span class="sxs-lookup"><span data-stu-id="936e0-117">The following example shows creating and submitting a certificate request and receiving the resulting key archival certificate.</span></span>


```C++
// Pointer to interface objects.
ICEnroll4 * pEnroll = NULL;
ICertRequest2 * pRequest = NULL;

// BSTR variables.
BSTR    bstrCACert = NULL;
BSTR    bstrDN = NULL;
BSTR    bstrCertAuth = NULL;
BSTR    bstrReq = NULL;
BSTR    bstrDispMsg = NULL;
BSTR    bstrErrorMsg = NULL;

VARIANT varFullResp;

LONG    lDisp =0;
LONG    lRequestID = 0;
LONG    lStatus = 0;

HRESULT    hr;

// Initialize COM.
hr = CoInitializeEx( NULL, COINIT_APARTMENTTHREADED );
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
if ( FAILED( hr ) )
{
    printf("Failed CoCreateInstance - pRequest [%x]\n", hr);
    goto error;
}

// Allocate the BSTR that represents the certification authority.
// Note the use of '\\' to produce a single '\' in C++.
bstrCertAuth = SysAllocString(L"Server\\CertAuth");
if (NULL == bstrCertAuth)
{
    printf("Failed SysAllocString\n");
    goto error;
}

// Retrieve the CA's exchange certificate.
hr = pRequest->GetCACertificate(TRUE,
                                bstrCertAuth,
                                CR_OUT_BASE64HEADER,
                                &bstrCACert);
if (FAILED(hr))
{
    printf("Failed GetCACertificate [%x]\n", hr);
    goto error;
}

// Specify the retrieved certificate 
// as the key archive certificate.
hr = pEnroll->put_PrivateKeyArchiveCertificate(bstrCACert);
if (FAILED(hr))
{
    printf("put_PrivateKeyArchiveCertificate [%x]\n", hr);
    goto error;
}

// Create the data for the request.
// A user interface or database retrieval could
// be used instead of this example's hard-coded text.
bstrDN = SysAllocString(L"CN=UserName"    // common name
                        L",OU=UserUnit"   // org unit
                        L",O=UserOrg"     // org
                        L",L=UserCity"    // locality
                        L",S=WA"          // state
                        L",C=US");        // country/region
if (NULL == bstrDN)
{
    printf("Failed SysAllocString\n");
    goto error;
}

// Create the certificate request.
hr = pEnroll->createRequest( XECR_CMC,
                             bstrDN, 
                             NULL,
                             &bstrReq );
if ( FAILED( hr ) )
{
    printf("Failed createRequest - [%x]\n", hr);
    goto error;
}

// Submit the certificate request.
hr = pRequest->Submit( CR_IN_CMC,
                       bstrReq,
                       NULL,
                       bstrCertAuth,
                       &lDisp );
if ( FAILED( hr ) )
{
    
    printf("Failed Submit - [%x]\n", hr);  
    goto error;
}

// Evaluate the disposition of the submitted request.
switch (lDisp)
{
    case CR_DISP_ISSUED:
           printf("Certificate was issued.\n");
           break;

    case CR_DISP_ISSUED_OUT_OF_BAND:
    case CR_DISP_INCOMPLETE:
    case CR_DISP_ERROR:
    case CR_DISP_DENIED:
    case CR_DISP_UNDER_SUBMISSION:
    case CR_DISP_REVOKED:
            printf("Certificate was not issued: %d\n", lDisp);
            break;

    default:
            printf("Unexpected disposition: %d\n", lDisp);
            goto error;
}

// Retrieve the request ID.
hr = pRequest->GetRequestId(&lRequestID);
if ( FAILED(hr) )
{
    printf("Failed GetRequestId - [%x]\n", hr);  
    goto error;
}
printf("The request ID is %d\n", lRequestID);

if (CR_DISP_ISSUED != lDisp)
{
    // Provide information about why a certificate 
    // was not issued.
    
    // Retrieve the last status.
    hr = pRequest->GetLastStatus(&lStatus);
    if ( FAILED(hr) )
    {
        printf("Failed GetLastStatus - [%x]\n", hr);  
        goto error;
    }

    // Retrieve the disposition message.
    hr = pRequest->GetDispositionMessage(&bstrDispMsg);
    if ( FAILED(hr) )
    {
        printf("Failed GetDispositionMessage - [%x]\n", hr);  
        goto error;
    }

    // Retrieve the error message.
    hr = pRequest->GetErrorMessageText(lStatus,
                                       CR_GEMT_HRESULT_STRING,
                                       &bstrErrorMsg);
    if ( FAILED(hr) )
    {
        printf("Failed GetErrorMessageText - [%x]\n", hr);  
        goto error;
    }
    
    // Display the information and exit.
    printf("Request ID: %d\nDisposition: %S\nError: %S\n",
           lRequestID,
           bstrDispMsg,
           bstrErrorMsg);
    goto error;
}

// Retrieve the full response.
VariantInit(&varFullResp);
hr = pRequest->GetFullResponseProperty( FR_PROP_FULLRESPONSE,
                                        0,
                                        PROPTYPE_BINARY,
                                        CR_OUT_BASE64,
                                        &varFullResp );
if ( FAILED( hr ) )
{
    printf("Failed GetFullResponseProperty - [%x]\n", hr);
    goto error;
}

// Accept the response.
hr = pEnroll->acceptResponse(varFullResp.bstrVal);
if ( FAILED( hr ) )
{
    printf("Failed AcceptResponse - [%x]\n", hr);
    goto error;
}
else
{
    printf("Successfully completed processing\n");
}

error:

// Done processing.
// Clean up object resources.
if ( NULL != pEnroll )
    pEnroll->Release();
if ( NULL != pRequest )
    pRequest->Release();

// Free BSTR variables.
if ( NULL != bstrCACert )
    SysFreeString ( bstrCACert );
if ( NULL != bstrDN )
    SysFreeString ( bstrDN );
if ( NULL != bstrCertAuth )
    SysFreeString ( bstrCertAuth );
if ( NULL != bstrReq )
    SysFreeString ( bstrReq );
if ( NULL != bstrDispMsg )
    SysFreeString ( bstrDispMsg );
if ( NULL != bstrErrorMsg )
    SysFreeString ( bstrErrorMsg );

// Clear VARIANTS.
VariantClear(&varFullResp);

// Free COM resources.
CoUninitialize();

return hr;
```



 

 
