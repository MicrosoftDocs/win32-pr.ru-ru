---
description: В этом разделе описывается, как проверить, поддерживает ли сертификат конкретный метод подписи.
ms.assetid: c7a23ace-4e9c-4de2-994e-2aa9c70a30b6
title: Убедитесь, что сертификат поддерживает метод подписи.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 177859dd78d30ee9f9147cee7ca01311ed95c0733115cd939dde8aa6ec70f5b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119098716"
---
# <a name="verify-that-a-certificate-supports-a-signature-method"></a>Убедитесь, что сертификат поддерживает метод подписи.

В этом разделе описывается, как проверить, поддерживает ли сертификат конкретный метод подписи.

**Криптксмленумалгорисминфо** в Microsoft Crypto API перечисляет свойства сертификата и используется в этом примере кода для перечисления методов подписи, поддерживаемых сертификатом. Чтобы использовать **криптксмленумалгорисминфо** для перечисления методов подписи, поддерживаемых сертификатом, вызывающий объект должен предоставить метод обратного вызова и структуру данных в вызове **криптксмленумалгорисминфо**, что позволяет передавать данные в метод обратного вызова.

Структура данных, используемая в следующем примере кода, содержит следующие поля:

| Поле                               | Описание                                                                                                                               |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| **усерсигнатуреалгорисмточекк**   | Поле **LPWSTR** , которое указывает на строку, содержащую URI проверяемого алгоритма подписи.                             |
| **цертификатеалгорисминфо**        | Указатель на **\_ \_ информационную структуру идентификатора OID** , которая содержит сведения о алгоритме подписи, поддерживаемом сертификатом. |
| **усерсигнатуреалгорисмсуппортед** | **Логическое** значение, указывающее, поддерживается ли в сертификате алгоритм подписи.                                       |



 


```C++
struct SignatureMethodData
{
    LPCWSTR             userSignatureAlgorithmToCheck; 
    PCCRYPT_OID_INFO    certificateAlgorithmInfo; 
    BOOL                userSignatureAlgorithmSupported; 
};
```



Метод API шифрования, который проверяет сертификат, использует метод обратного вызова для возврата данных вызывающему объекту. **Криптксмленумалгорисминфо** перечисляет методы сигнатуры, поддерживаемые сертификатом, и вызывает метод обратного вызова для каждого метода подписи до тех пор, пока метод обратного вызова не возвратит **значение false** или пока не будут перечислены все методы подписи в сертификате.

Метод обратного вызова в следующем примере кода выполняет поиск метода подписи, переданного методом **криптксмленумалгорисминфо** , который соответствует методу подписи, предоставленному вызывающим методом. При обнаружении совпадения метод обратного вызова проверяет, поддерживается ли метод Signature системой. Если методы подписи совпадают и поддерживаются системой, метод подписи помечается как поддерживаемый системой, а метод обратного вызова возвращает **значение false**.


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



В следующем примере кода функция проверки переносится в один метод. Этот метод возвращает **логическое** значение, указывающее, поддерживает ли сертификат метод подписи и поддерживается ли в системе метод подписи.


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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

**Следующие шаги**
</dt> <dt>

[Загрузка сертификата из файла](load-a-certificate-from-a-file.md)
</dt> <dt>

[Проверка того, что система поддерживает метод дайджеста](verify-a-certificate-supports-a-digest-method.md)
</dt> <dt>

[Внедрение цепочек сертификатов в документ](embedding-certificate-trust-chains-in-a-document.md)
</dt> <dt>

**Используется в этом примере**
</dt> <dt>

[**криптфиндоидинфо**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptfindoidinfo)
</dt> <dt>

[**\_ \_ сведения о шифровании OID**](/windows/desktop/api/wincrypt/ns-wincrypt-crypt_oid_info)
</dt> <dt>

**криптксмленумалгорисминфо**
</dt> <dt>

**Дополнительные сведения**
</dt> <dt>

[API шифрования](/windows/desktop/SecCrypto/cryptography-portal)
</dt> <dt>

[Криптографические функции](/windows/desktop/SecCrypto/cryptography-functions)
</dt> <dt>

[Ошибки API цифровой подписи XPS](xps-digital-signatures-errors.md)
</dt> <dt>

[Ошибки документа XPS](xps-document-errors.md)
</dt> <dt>

[XPS](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
