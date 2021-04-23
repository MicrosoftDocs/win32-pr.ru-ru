---
description: В этом разделе описывается, как проверить, поддерживает ли сертификат конкретный метод подписи.
ms.assetid: c7a23ace-4e9c-4de2-994e-2aa9c70a30b6
title: Убедитесь, что сертификат поддерживает метод подписи.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27da9ae31c3cf0c4e453a5507d93d1505606e859
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912631"
---
# <a name="verify-that-a-certificate-supports-a-signature-method"></a><span data-ttu-id="496b0-103">Убедитесь, что сертификат поддерживает метод подписи.</span><span class="sxs-lookup"><span data-stu-id="496b0-103">Verify That a Certificate Supports a Signature Method</span></span>

<span data-ttu-id="496b0-104">В этом разделе описывается, как проверить, поддерживает ли сертификат конкретный метод подписи.</span><span class="sxs-lookup"><span data-stu-id="496b0-104">This topic describes how to verify that a certificate supports a specific signature method.</span></span>

<span data-ttu-id="496b0-105">**Криптксмленумалгорисминфо** в Microsoft Crypto API перечисляет свойства сертификата и используется в этом примере кода для перечисления методов подписи, поддерживаемых сертификатом.</span><span class="sxs-lookup"><span data-stu-id="496b0-105">The **CryptXmlEnumAlgorithmInfo** in the Microsoft Crypto API enumerates the properties of a certificate and is used in this code example to enumerate the signature methods that the certificate supports.</span></span> <span data-ttu-id="496b0-106">Чтобы использовать **криптксмленумалгорисминфо** для перечисления методов подписи, поддерживаемых сертификатом, вызывающий объект должен предоставить метод обратного вызова и структуру данных в вызове **криптксмленумалгорисминфо**, что позволяет передавать данные в метод обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="496b0-106">To use **CryptXmlEnumAlgorithmInfo** to enumerate the signature methods that the certificate supports, the caller must provide a callback method and a data structure in the call to **CryptXmlEnumAlgorithmInfo**, allowing it to pass data to the callback method.</span></span>

<span data-ttu-id="496b0-107">Структура данных, используемая в следующем примере кода, содержит следующие поля:</span><span class="sxs-lookup"><span data-stu-id="496b0-107">The data structure used in the next code example has the following fields:</span></span>

| <span data-ttu-id="496b0-108">Поле</span><span class="sxs-lookup"><span data-stu-id="496b0-108">Field</span></span>                               | <span data-ttu-id="496b0-109">Описание</span><span class="sxs-lookup"><span data-stu-id="496b0-109">Description</span></span>                                                                                                                               |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="496b0-110">**усерсигнатуреалгорисмточекк**</span><span class="sxs-lookup"><span data-stu-id="496b0-110">**userSignatureAlgorithmToCheck**</span></span>   | <span data-ttu-id="496b0-111">Поле **LPWSTR** , которое указывает на строку, содержащую URI проверяемого алгоритма подписи.</span><span class="sxs-lookup"><span data-stu-id="496b0-111">An **LPWSTR** field that points to the string that contains the URI of the signature algorithm to be checked.</span></span>                             |
| <span data-ttu-id="496b0-112">**цертификатеалгорисминфо**</span><span class="sxs-lookup"><span data-stu-id="496b0-112">**certificateAlgorithmInfo**</span></span>        | <span data-ttu-id="496b0-113">Указатель на **\_ \_ информационную структуру идентификатора OID** , которая содержит сведения о алгоритме подписи, поддерживаемом сертификатом.</span><span class="sxs-lookup"><span data-stu-id="496b0-113">A pointer to a **CRYPT\_OID\_INFO** structure that contains information about a signature algorithm that is supported by the certificate.</span></span> |
| <span data-ttu-id="496b0-114">**усерсигнатуреалгорисмсуппортед**</span><span class="sxs-lookup"><span data-stu-id="496b0-114">**userSignatureAlgorithmSupported**</span></span> | <span data-ttu-id="496b0-115">**Логическое** значение, указывающее, поддерживается ли в сертификате алгоритм подписи.</span><span class="sxs-lookup"><span data-stu-id="496b0-115">A **Boolean** value that indicates whether the signature algorithm is supported by the certificate.</span></span>                                       |



 


```C++
struct SignatureMethodData
{
    LPCWSTR             userSignatureAlgorithmToCheck; 
    PCCRYPT_OID_INFO    certificateAlgorithmInfo; 
    BOOL                userSignatureAlgorithmSupported; 
};
```



<span data-ttu-id="496b0-116">Метод API шифрования, который проверяет сертификат, использует метод обратного вызова для возврата данных вызывающему объекту.</span><span class="sxs-lookup"><span data-stu-id="496b0-116">The Crypto API method that checks the certificate uses a callback method to return data to the caller.</span></span> <span data-ttu-id="496b0-117">**Криптксмленумалгорисминфо** перечисляет методы сигнатуры, поддерживаемые сертификатом, и вызывает метод обратного вызова для каждого метода подписи до тех пор, пока метод обратного вызова не возвратит **значение false** или пока не будут перечислены все методы подписи в сертификате.</span><span class="sxs-lookup"><span data-stu-id="496b0-117">**CryptXmlEnumAlgorithmInfo** enumerates the signature methods that the certificate supports, and calls the callback method for each signature method until the callback method returns **FALSE** or until all signature methods in the certificate have been enumerated.</span></span>

<span data-ttu-id="496b0-118">Метод обратного вызова в следующем примере кода выполняет поиск метода подписи, переданного методом **криптксмленумалгорисминфо** , который соответствует методу подписи, предоставленному вызывающим методом.</span><span class="sxs-lookup"><span data-stu-id="496b0-118">The callback method in the next code example searches for a signature method passed in by **CryptXmlEnumAlgorithmInfo** that matches the signature method provided by the calling method.</span></span> <span data-ttu-id="496b0-119">При обнаружении совпадения метод обратного вызова проверяет, поддерживается ли метод Signature системой.</span><span class="sxs-lookup"><span data-stu-id="496b0-119">When a match is found, the callback method checks whether the signature method is also supported by the system.</span></span> <span data-ttu-id="496b0-120">Если методы подписи совпадают и поддерживаются системой, метод подписи помечается как поддерживаемый системой, а метод обратного вызова возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="496b0-120">If the signature methods match and are supported by the system, the signature method is marked as system-supported and the callback method returns **FALSE**.</span></span>


```C++
BOOL WINAPI 
EnumSignatureMethodCallback (
    __in const CRYPT_XML_ALGORITHM_INFO *certMethodInfo,
    __inout_opt void *userArg
)
{
    // MAX_ALG_ID_LEN is used to set the maximum length of the 
    // algorithm URI in the string comparison. The URI is not 
    // likely to be longer than 128 characters so a fixed-size
    // buffer is used in this example.
    // To make this function more robust, you might consider
    // setting this value dynamically.
    static const size_t MAX_ALG_ID_LEN = 128;
    SignatureMethodData *certificateAlgorithmData = NULL;

    if (NULL != userArg) {
        // Assign user data to local data structure
        certificateAlgorithmData = (SignatureMethodData*)userArg;
    } else {
        // Unable to continue this enumeration 
        //   without data from calling method.
        return FALSE;
    }
    
    // For each algorithm in the enumeration, check to see if the URI 
    //  of the algorithm supported by the certificate matches the URI 
    //  of the algorithm being tested.
    int cmpResult = 0;
    cmpResult = wcsncmp( 
        certMethodInfo->wszAlgorithmURI, 
        certificateAlgorithmData->userSignatureAlgorithmToCheck, 
        MAX_ALG_ID_LEN );
    if ( 0 == cmpResult )
    {
        // This is a match...
        // Check to see if the algorithm supported by the 
        //  certificate matches any of the supported algorithms 
        //  on the system.
        cmpResult = wcsncmp(
            certMethodInfo->wszCNGExtraAlgid, 
            certificateAlgorithmData->certificateAlgorithmInfo->pwszCNGAlgid, 
            MAX_ALG_ID_LEN );
        if ( 0 == cmpResult )
        {
            // This is also a match so set the field in the data structure
            //   provided by the calling method.
            certificateAlgorithmData->userSignatureAlgorithmSupported = TRUE;
            // A match was found so there is no point in continuing 
            //  the enumeration.
            return FALSE;
        }
    }
    // The enumeration stops when the callback method returns FALSE. 
    //   If here, then return TRUE because a matching algorithm has
    //   not been found.
    return TRUE;
}
```



<span data-ttu-id="496b0-121">В следующем примере кода функция проверки переносится в один метод.</span><span class="sxs-lookup"><span data-stu-id="496b0-121">The following code example wraps the validation functionality into a single method.</span></span> <span data-ttu-id="496b0-122">Этот метод возвращает **логическое** значение, указывающее, поддерживает ли сертификат метод подписи и поддерживается ли в системе метод подписи.</span><span class="sxs-lookup"><span data-stu-id="496b0-122">This method returns a **Boolean** value that indicates whether the certificate supports the signature method and whether the signature method is supported by the system.</span></span>


```C++
BOOL 
SupportsSignatureAlgorithm (
    __in LPCWSTR signingMethodToCheck,
    __in PCCERT_CONTEXT certificateToCheck
)
{
    HRESULT     hr = S_OK;

    // Initialize the structure that contains the   
    //  information about the signature algorithm to check
    SignatureMethodData        certificateAlgorithmData;

    certificateAlgorithmData.userSignatureAlgorithmSupported = 
        FALSE;
    certificateAlgorithmData.userSignatureAlgorithmToCheck = 
        signingMethodToCheck;

    // Call the crypt API to get information about the algorithms
    //   that are supported by the certificate and initialize 
    //   certificateAlgorithmData
    certificateAlgorithmData.certificateAlgorithmInfo = CryptFindOIDInfo (
        CRYPT_OID_INFO_OID_KEY,
        certificateToCheck->pCertInfo->SubjectPublicKeyInfo.Algorithm.pszObjId,
        CRYPT_PUBKEY_ALG_OID_GROUP_ID | CRYPT_OID_PREFER_CNG_ALGID_FLAG);

    if (certificateAlgorithmData.certificateAlgorithmInfo != NULL)
    {
        // Enumerate the algorithms that are supported by the 
        //   certificate, and use our callback method to determine if
        //   the user supplied signature algorithm is supported by 
        //     the certificate.
        //
        // Note that CRYPT_XML_GROUP_ID_SIGN is used to enumerate
        //  the signature methods
        hr = CryptXmlEnumAlgorithmInfo(
            CRYPT_XML_GROUP_ID_SIGN,  // NOTE: CRYPT_XML_GROUP_ID_SIGN
            CRYPT_XML_FLAG_DISABLE_EXTENSIONS,
            (void*)&certificateAlgorithmData,
            EnumSignatureMethodCallback);
        // when the enumeration has returned successfully, 
        //  certificateAlgorithmData.userSignatureAlgorithmSupported
        //  will be TRUE if the signing method is supported by
        //  the certificate
    }
    return certificateAlgorithmData.userSignatureAlgorithmSupported;
}
```



## <a name="related-topics"></a><span data-ttu-id="496b0-123">См. также</span><span class="sxs-lookup"><span data-stu-id="496b0-123">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="496b0-124">**Следующие шаги**</span><span class="sxs-lookup"><span data-stu-id="496b0-124">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="496b0-125">Загрузка сертификата из файла</span><span class="sxs-lookup"><span data-stu-id="496b0-125">Load a Certificate from a File</span></span>](load-a-certificate-from-a-file.md)
</dt> <dt>

[<span data-ttu-id="496b0-126">Проверка того, что система поддерживает метод дайджеста</span><span class="sxs-lookup"><span data-stu-id="496b0-126">Verify the System Supports a Digest Method</span></span>](verify-a-certificate-supports-a-digest-method.md)
</dt> <dt>

[<span data-ttu-id="496b0-127">Внедрение цепочек сертификатов в документ</span><span class="sxs-lookup"><span data-stu-id="496b0-127">Embed Certificate Chains in a Document</span></span>](embedding-certificate-trust-chains-in-a-document.md)
</dt> <dt>

<span data-ttu-id="496b0-128">**Используется в этом примере**</span><span class="sxs-lookup"><span data-stu-id="496b0-128">**Used in This Example**</span></span>
</dt> <dt>

[<span data-ttu-id="496b0-129">**криптфиндоидинфо**</span><span class="sxs-lookup"><span data-stu-id="496b0-129">**CryptFindOIDInfo**</span></span>](/windows/desktop/api/wincrypt/nf-wincrypt-cryptfindoidinfo)
</dt> <dt>

[<span data-ttu-id="496b0-130">**\_ \_ сведения о шифровании OID**</span><span class="sxs-lookup"><span data-stu-id="496b0-130">**CRYPT\_OID\_INFO**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-crypt_oid_info)
</dt> <dt>

<span data-ttu-id="496b0-131">**криптксмленумалгорисминфо**</span><span class="sxs-lookup"><span data-stu-id="496b0-131">**CryptXmlEnumAlgorithmInfo**</span></span>
</dt> <dt>

<span data-ttu-id="496b0-132">**Дополнительные сведения**</span><span class="sxs-lookup"><span data-stu-id="496b0-132">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="496b0-133">API шифрования</span><span class="sxs-lookup"><span data-stu-id="496b0-133">Cryptography API</span></span>](/windows/desktop/SecCrypto/cryptography-portal)
</dt> <dt>

[<span data-ttu-id="496b0-134">Криптографические функции</span><span class="sxs-lookup"><span data-stu-id="496b0-134">Cryptography Functions</span></span>](/windows/desktop/SecCrypto/cryptography-functions)
</dt> <dt>

[<span data-ttu-id="496b0-135">Ошибки API цифровой подписи XPS</span><span class="sxs-lookup"><span data-stu-id="496b0-135">XPS Digital Signature API Errors</span></span>](xps-digital-signatures-errors.md)
</dt> <dt>

[<span data-ttu-id="496b0-136">Ошибки документа XPS</span><span class="sxs-lookup"><span data-stu-id="496b0-136">XPS Document Errors</span></span>](xps-document-errors.md)
</dt> <dt>

[<span data-ttu-id="496b0-137">XPS</span><span class="sxs-lookup"><span data-stu-id="496b0-137">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
