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
# <a name="verify-the-system-supports-a-digest-method"></a>Проверка того, что система поддерживает метод дайджеста

В этом разделе описывается, как проверить, поддерживает ли система метод дайджеста.

Цифровые подписи XPS используют API шифрования, который предоставляет методы для проверки того, что система поддерживает конкретный метод дайджеста. Чтобы использовать функцию **КРИПТКСМЛЕНУМАЛГОРИСМИНФО** API шифрования для перечисления методов дайджеста, поддерживаемых системой, вызывающий объект должен предоставить метод обратного вызова и структуру данных. Функция **криптксмленумалгорисминфо** передает данные перечисления обратно вызывающему объекту посредством метода обратного вызова.

Структура данных, используемая в этом примере, показана в следующем примере кода и содержит следующие поля:

| Поле                            | Описание                                                                                                |
|----------------------------------|------------------------------------------------------------------------------------------------------------|
| **усердижесталгорисм**          | Поле **LPWSTR** , которое указывает на строку, содержащую URI проверяемого алгоритма дайджеста. |
| **усердижесталгорисмсуппортед** | **Логическое** значение, указывающее, поддерживается ли в сертификате алгоритм дайджеста.           |



 


```C++
struct DigestMethodData
{
    LPCWSTR userDigestAlgorithm; 
    BOOL    userDigestAlgorithmSupported;
};
```



Метод Crypto API, перечисляющий методы дайджеста, использует метод обратного вызова для возврата данных вызывающему объекту. **Криптксмленумалгорисминфо** перечисляет методы дайджеста, поддерживаемые системой, и вызывает метод обратного вызова для каждого перечисленного метода дайджеста, пока метод обратного вызова не возвратит **значение false** или пока не будут перечислены все методы дайджеста, поддерживаемые системой. Метод обратного вызова в этом примере сравнивает метод дайджеста, который передается методом **криптксмленумалгорисминфо** , с помощью метода Digest, предоставленного вызывающим методом.


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



В следующем примере кода функция проверки переносится в единый метод, который возвращает **логическое** значение, указывающее, поддерживает ли система метод дайджеста.


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



## <a name="related-topics"></a>См. также

<dl> <dt>

**Следующие шаги**
</dt> <dt>

[Загрузка сертификата из файла](load-a-certificate-from-a-file.md)
</dt> <dt>

[Убедитесь, что сертификат поддерживает метод подписи.](verify-a-certificate-supports-a-signature-method.md)
</dt> <dt>

[Внедрение цепочек сертификатов в документ](embedding-certificate-trust-chains-in-a-document.md)
</dt> <dt>

**Используется в этом примере**
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

 

 
