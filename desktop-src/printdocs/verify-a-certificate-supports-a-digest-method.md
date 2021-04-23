---
description: В этом разделе описывается, как проверить, поддерживает ли система метод дайджеста.
ms.assetid: dd1b53cd-66b9-46b3-89ad-ee84b4690e1e
title: Проверка того, что система поддерживает метод дайджеста
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9acf3e0c2c7f4927fc6047c88039e443e2db3e71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912632"
---
# <a name="verify-the-system-supports-a-digest-method"></a><span data-ttu-id="f8825-103">Проверка того, что система поддерживает метод дайджеста</span><span class="sxs-lookup"><span data-stu-id="f8825-103">Verify the System Supports a Digest Method</span></span>

<span data-ttu-id="f8825-104">В этом разделе описывается, как проверить, поддерживает ли система метод дайджеста.</span><span class="sxs-lookup"><span data-stu-id="f8825-104">This topic describes how to verify that the system supports a digest method.</span></span>

<span data-ttu-id="f8825-105">Цифровые подписи XPS используют API шифрования, который предоставляет методы для проверки того, что система поддерживает конкретный метод дайджеста.</span><span class="sxs-lookup"><span data-stu-id="f8825-105">XPS Digital Signatures use the Crypto API, which provides methods for verifying that the system supports a specific digest method.</span></span> <span data-ttu-id="f8825-106">Чтобы использовать функцию **КРИПТКСМЛЕНУМАЛГОРИСМИНФО** API шифрования для перечисления методов дайджеста, поддерживаемых системой, вызывающий объект должен предоставить метод обратного вызова и структуру данных.</span><span class="sxs-lookup"><span data-stu-id="f8825-106">To use the Crypto API's **CryptXmlEnumAlgorithmInfo** function to enumerate the digest methods that are supported by the system, the caller must provide a callback method and a data structure.</span></span> <span data-ttu-id="f8825-107">Функция **криптксмленумалгорисминфо** передает данные перечисления обратно вызывающему объекту посредством метода обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="f8825-107">The **CryptXmlEnumAlgorithmInfo** function passes the enumeration data back to the caller by way of the callback method.</span></span>

<span data-ttu-id="f8825-108">Структура данных, используемая в этом примере, показана в следующем примере кода и содержит следующие поля:</span><span class="sxs-lookup"><span data-stu-id="f8825-108">The data structure used in this example is shown in the following code example and contains the following fields:</span></span>

| <span data-ttu-id="f8825-109">Поле</span><span class="sxs-lookup"><span data-stu-id="f8825-109">Field</span></span>                            | <span data-ttu-id="f8825-110">Описание</span><span class="sxs-lookup"><span data-stu-id="f8825-110">Description</span></span>                                                                                                |
|----------------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8825-111">**усердижесталгорисм**</span><span class="sxs-lookup"><span data-stu-id="f8825-111">**userDigestAlgorithm**</span></span>          | <span data-ttu-id="f8825-112">Поле **LPWSTR** , которое указывает на строку, содержащую URI проверяемого алгоритма дайджеста.</span><span class="sxs-lookup"><span data-stu-id="f8825-112">An **LPWSTR** field that points to the string that contains the URI of the digest algorithm to be checked.</span></span> |
| <span data-ttu-id="f8825-113">**усердижесталгорисмсуппортед**</span><span class="sxs-lookup"><span data-stu-id="f8825-113">**userDigestAlgorithmSupported**</span></span> | <span data-ttu-id="f8825-114">**Логическое** значение, указывающее, поддерживается ли в сертификате алгоритм дайджеста.</span><span class="sxs-lookup"><span data-stu-id="f8825-114">A **Boolean** value that indicates whether the digest algorithm is supported by the certificate.</span></span>           |



 


```C++
struct DigestMethodData
{
    LPCWSTR userDigestAlgorithm; 
    BOOL    userDigestAlgorithmSupported;
};
```



<span data-ttu-id="f8825-115">Метод Crypto API, перечисляющий методы дайджеста, использует метод обратного вызова для возврата данных вызывающему объекту.</span><span class="sxs-lookup"><span data-stu-id="f8825-115">The Crypto API method that enumerates the digest methods uses a callback method to return data to the caller.</span></span> <span data-ttu-id="f8825-116">**Криптксмленумалгорисминфо** перечисляет методы дайджеста, поддерживаемые системой, и вызывает метод обратного вызова для каждого перечисленного метода дайджеста, пока метод обратного вызова не возвратит **значение false** или пока не будут перечислены все методы дайджеста, поддерживаемые системой.</span><span class="sxs-lookup"><span data-stu-id="f8825-116">**CryptXmlEnumAlgorithmInfo** enumerates the digest methods that are supported by the system, and it calls the callback method for each digest method that it enumerates, until the callback method returns **FALSE** or until all digest methods supported by the system are enumerated.</span></span> <span data-ttu-id="f8825-117">Метод обратного вызова в этом примере сравнивает метод дайджеста, который передается методом **криптксмленумалгорисминфо** , с помощью метода Digest, предоставленного вызывающим методом.</span><span class="sxs-lookup"><span data-stu-id="f8825-117">The callback method in this example compares the digest method that is passed in by **CryptXmlEnumAlgorithmInfo** with the digest method provided by the calling method.</span></span>


```C++
BOOL WINAPI 
EnumDigestMethodCallback (
    __in   const CRYPT_XML_ALGORITHM_INFO *certMethodInfo,
    __inout_opt  void                     *userArg
)
{
    // MAX_ALG_ID_LEN is used to set the maximum length of the 
    // algorithm URI in the string comparison. The URI is not 
    // likely to be longer than 128 characters so a fixed-size
    // buffer is used in this example.
    // To make this function more robust, consider
    // setting this value dynamically.
    static const  size_t MAX_ALG_ID_LEN = 128;
    DigestMethodData   *certificateAlgorithmData = 
        (DigestMethodData*)userArg;

    if (NULL != userArg) {
        // Assign user data to local data structure
        certificateAlgorithmData = (DigestMethodData*)userArg;
    } else {
        // Unable to continue this enumeration without 
        //  data from calling method.
        return FALSE;
    }
    
    // For each algorithm in the enumeration, check to see 
    //  if the URI of the current supported algorithm matches 
    //  the URI passed in userArg.
    int cmpResult = 0;
    cmpResult = wcsncmp( 
        certMethodInfo->wszAlgorithmURI, 
        certificateAlgorithmData->userDigestAlgorithm, 
        MAX_ALG_ID_LEN );

    if ( 0 == cmpResult )
    {
        // This is a match...
        //  set supported value to true
        certificateAlgorithmData->userDigestAlgorithmSupported = TRUE;
        //  ...and return FALSE to stop any further enumeration
        return FALSE;
    } 
    else
    {
        // no match was found
        // return TRUE to continue enumeration
        return TRUE;
    }
}
```



<span data-ttu-id="f8825-118">В следующем примере кода функция проверки переносится в единый метод, который возвращает **логическое** значение, указывающее, поддерживает ли система метод дайджеста.</span><span class="sxs-lookup"><span data-stu-id="f8825-118">The following code sample wraps the validation functionality into a single method, which returns a **Boolean** value that indicates whether the system supports the digest method.</span></span>


```C++
BOOL 
SupportsDigestAlgorithm (
    __in LPCWSTR digestMethodToCheck
)
{
    HRESULT  hr = S_OK;

    // Initialize the structure that will hold information about the 
    //  digest method to check
    DigestMethodData  certificateAlgorithmData;

    certificateAlgorithmData.userDigestAlgorithmSupported = FALSE;
    certificateAlgorithmData.userDigestAlgorithm = digestMethodToCheck;

    // Enumerate the algorithms that are supported on the system, 
    //  the callback method compares each supported algorithm to the one
    //  passed in digestMethodToCheck and returns true in the
    //  certificateAlgorithmData.userDigestAlgorithmSupported field if
    //  the provided digest algorithm is supported by system.
    //
    // Note that CRYPT_XML_GROUP_ID_HASH is set to enumerate 
    //  digest methods
    hr = CryptXmlEnumAlgorithmInfo(
        CRYPT_XML_GROUP_ID_HASH,       // NOTE: CRYPT_XML_GROUP_ID_HASH
        CRYPT_XML_FLAG_DISABLE_EXTENSIONS,
        (void*)&certificateAlgorithmData,
        EnumDigestMethodCallback);

    return certificateAlgorithmData.userDigestAlgorithmSupported;
}
```



## <a name="related-topics"></a><span data-ttu-id="f8825-119">См. также</span><span class="sxs-lookup"><span data-stu-id="f8825-119">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="f8825-120">**Следующие шаги**</span><span class="sxs-lookup"><span data-stu-id="f8825-120">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="f8825-121">Загрузка сертификата из файла</span><span class="sxs-lookup"><span data-stu-id="f8825-121">Load a Certificate from a File</span></span>](load-a-certificate-from-a-file.md)
</dt> <dt>

[<span data-ttu-id="f8825-122">Убедитесь, что сертификат поддерживает метод подписи.</span><span class="sxs-lookup"><span data-stu-id="f8825-122">Verify That a Certificate Supports a Signature Method</span></span>](verify-a-certificate-supports-a-signature-method.md)
</dt> <dt>

[<span data-ttu-id="f8825-123">Внедрение цепочек сертификатов в документ</span><span class="sxs-lookup"><span data-stu-id="f8825-123">Embed Certificate Chains in a Document</span></span>](embedding-certificate-trust-chains-in-a-document.md)
</dt> <dt>

<span data-ttu-id="f8825-124">**Используется в этом примере**</span><span class="sxs-lookup"><span data-stu-id="f8825-124">**Used in This Example**</span></span>
</dt> <dt>

<span data-ttu-id="f8825-125">**криптксмленумалгорисминфо**</span><span class="sxs-lookup"><span data-stu-id="f8825-125">**CryptXmlEnumAlgorithmInfo**</span></span>
</dt> <dt>

<span data-ttu-id="f8825-126">**Дополнительные сведения**</span><span class="sxs-lookup"><span data-stu-id="f8825-126">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="f8825-127">API шифрования</span><span class="sxs-lookup"><span data-stu-id="f8825-127">Cryptography API</span></span>](/windows/desktop/SecCrypto/cryptography-portal)
</dt> <dt>

[<span data-ttu-id="f8825-128">Криптографические функции</span><span class="sxs-lookup"><span data-stu-id="f8825-128">Cryptography Functions</span></span>](/windows/desktop/SecCrypto/cryptography-functions)
</dt> <dt>

[<span data-ttu-id="f8825-129">Ошибки API цифровой подписи XPS</span><span class="sxs-lookup"><span data-stu-id="f8825-129">XPS Digital Signature API Errors</span></span>](xps-digital-signatures-errors.md)
</dt> <dt>

[<span data-ttu-id="f8825-130">Ошибки документа XPS</span><span class="sxs-lookup"><span data-stu-id="f8825-130">XPS Document Errors</span></span>](xps-document-errors.md)
</dt> <dt>

[<span data-ttu-id="f8825-131">XPS</span><span class="sxs-lookup"><span data-stu-id="f8825-131">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
