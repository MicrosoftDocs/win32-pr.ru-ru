---
description: В этом разделе описывается, как загрузить сертификат из файла сертификата.
ms.assetid: 60cced55-9fcc-4fce-a462-7abf3f4466f0
title: Загрузка сертификата из файла
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c708fb042ccdf4acd43986de1404f9ccb266148
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684483"
---
# <a name="load-a-certificate-from-a-file"></a><span data-ttu-id="576f2-103">Загрузка сертификата из файла</span><span class="sxs-lookup"><span data-stu-id="576f2-103">Load a Certificate from a File</span></span>

<span data-ttu-id="576f2-104">В этом разделе описывается, как загрузить сертификат из файла сертификата.</span><span class="sxs-lookup"><span data-stu-id="576f2-104">This topic describes how to load a certificate from a certificate file.</span></span>

<span data-ttu-id="576f2-105">Загрузка сертификата из файла сертификата</span><span class="sxs-lookup"><span data-stu-id="576f2-105">To load a certificate from a certificate file</span></span>

1.  <span data-ttu-id="576f2-106">Откройте файл сертификата для доступа на чтение.</span><span class="sxs-lookup"><span data-stu-id="576f2-106">Open the certificate file for read access.</span></span>
2.  <span data-ttu-id="576f2-107">Прочтите содержимое файла сертификата в буфер сертификата.</span><span class="sxs-lookup"><span data-stu-id="576f2-107">Read the contents of the certificate file into the certificate buffer.</span></span>
3.  <span data-ttu-id="576f2-108">Создайте сертификат, используя содержимое буфера.</span><span class="sxs-lookup"><span data-stu-id="576f2-108">Create a certificate using the contents of the buffer.</span></span>


```C++
// In the interest of simplicity, this example
//  uses a fixed-length buffer to hold the certificate. 
// A more robust solution would be to query the size
//  of the certificate file and dynamically
//  allocate a buffer of that size or greater.
#define CERTIFICATE_BUFFER_SIZE 1024

HRESULT  hr                  = S_OK;
BYTE     certEncoded[CERTIFICATE_BUFFER_SIZE] = {0};
DWORD    certEncodedSize     = 0L;
HANDLE   certFileHandle      = NULL;
BOOL     result              = FALSE;

// open the certificate file
certFileHandle = CreateFile(certFile, 
    GENERIC_READ, 
    0, 
    NULL, 
    OPEN_EXISTING, 
    FILE_ATTRIBUTE_NORMAL, 
    NULL);
if (INVALID_HANDLE_VALUE == certFileHandle) {
    hr = HRESULT_FROM_WIN32(GetLastError());
}

if (SUCCEEDED(hr)) {
    // if the buffer is large enough
    //  read the certificate file into the buffer
    if (GetFileSize (certFileHandle, NULL) <= CERTIFICATE_BUFFER_SIZE) {
        result = ReadFile(certFileHandle, 
            certEncoded, 
            CERTIFICATE_BUFFER_SIZE, 
            &certEncodedSize, 
            NULL);
        if (!result) {
            // the read failed, return the error as an HRESULT
            hr = HRESULT_FROM_WIN32(GetLastError());
        } else {
            hr = S_OK;
        }
    } else {
        // The certificate file is larger than the allocated buffer.
        //  To handle this error, you could dynamically allocate
        //  the certificate buffer based on the file size returned or 
        //  use a larger static buffer.
        hr = HRESULT_FROM_WIN32(ERROR_MORE_DATA);
    }    
}
if (SUCCEEDED(hr))
{
    // create a certificate from the contents of the buffer
    *cert = CertCreateCertificateContext(X509_ASN_ENCODING, 
        certEncoded, 
        certEncodedSize);
    if (!(*cert)) {
        hr = HRESULT_FROM_WIN32(GetLastError());
        CloseHandle(certFileHandle);
        hr = E_FAIL;
    } else {
        hr = S_OK;
    }
}
// close the certificate file
if (NULL != certFileHandle) CloseHandle(certFileHandle);
```



## <a name="related-topics"></a><span data-ttu-id="576f2-109">См. также</span><span class="sxs-lookup"><span data-stu-id="576f2-109">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="576f2-110">**Следующие шаги**</span><span class="sxs-lookup"><span data-stu-id="576f2-110">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="576f2-111">Проверка того, что система поддерживает метод дайджеста</span><span class="sxs-lookup"><span data-stu-id="576f2-111">Verify the System Supports a Digest Method</span></span>](verify-a-certificate-supports-a-digest-method.md)
</dt> <dt>

[<span data-ttu-id="576f2-112">Убедитесь, что сертификат поддерживает метод подписи.</span><span class="sxs-lookup"><span data-stu-id="576f2-112">Verify That a Certificate Supports a Signature Method</span></span>](verify-a-certificate-supports-a-signature-method.md)
</dt> <dt>

[<span data-ttu-id="576f2-113">Внедрение цепочек сертификатов в документ</span><span class="sxs-lookup"><span data-stu-id="576f2-113">Embed Certificate Chains in a Document</span></span>](embedding-certificate-trust-chains-in-a-document.md)
</dt> <dt>

<span data-ttu-id="576f2-114">**Используется в этом примере**</span><span class="sxs-lookup"><span data-stu-id="576f2-114">**Used in This Example**</span></span>
</dt> <dt>

[<span data-ttu-id="576f2-115">**CreateFile**</span><span class="sxs-lookup"><span data-stu-id="576f2-115">**CreateFile**</span></span>](/windows/desktop/api/fileapi/nf-fileapi-createfilea)
</dt> <dt>

[<span data-ttu-id="576f2-116">**ReadFile**</span><span class="sxs-lookup"><span data-stu-id="576f2-116">**ReadFile**</span></span>](/windows/desktop/api/fileapi/nf-fileapi-readfile)
</dt> <dt>

[<span data-ttu-id="576f2-117">**церткреатецертификатеконтекст**</span><span class="sxs-lookup"><span data-stu-id="576f2-117">**CertCreateCertificateContext**</span></span>](/windows/desktop/api/wincrypt/nf-wincrypt-certcreatecertificatecontext)
</dt> <dt>

<span data-ttu-id="576f2-118">**Дополнительные сведения**</span><span class="sxs-lookup"><span data-stu-id="576f2-118">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="576f2-119">API шифрования</span><span class="sxs-lookup"><span data-stu-id="576f2-119">Cryptography API</span></span>](/windows/desktop/SecCrypto/cryptography-portal)
</dt> <dt>

[<span data-ttu-id="576f2-120">Криптографические функции</span><span class="sxs-lookup"><span data-stu-id="576f2-120">Cryptography Functions</span></span>](/windows/desktop/SecCrypto/cryptography-functions)
</dt> <dt>

[<span data-ttu-id="576f2-121">Ошибки API цифровой подписи XPS</span><span class="sxs-lookup"><span data-stu-id="576f2-121">XPS Digital Signature API Errors</span></span>](xps-digital-signatures-errors.md)
</dt> <dt>

[<span data-ttu-id="576f2-122">Ошибки документа XPS</span><span class="sxs-lookup"><span data-stu-id="576f2-122">XPS Document Errors</span></span>](xps-document-errors.md)
</dt> <dt>

[<span data-ttu-id="576f2-123">XPS</span><span class="sxs-lookup"><span data-stu-id="576f2-123">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
