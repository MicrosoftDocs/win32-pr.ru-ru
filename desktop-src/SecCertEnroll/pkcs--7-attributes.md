---
description: PKCS \# 7 — это стандартный синтаксис криптографического сообщения.
ms.assetid: fd4e2a13-f257-4ba9-a11d-35f49c5a6c00
title: '\#АТРИБУТЫ PKCS 7'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24436a918afe2d9bd85d7c28ae330b8c022bd4e3d34d30e58aae7b9c57c4963a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117774589"
---
# <a name="pkcs-7-attributes"></a>\#АТРИБУТЫ PKCS 7

PKCS \# 7 — это стандартный синтаксис криптографического сообщения. Сообщение PKCS \# 7 само по себе не является запросом на сертификат, но может инкапсулировать \# запрос PKCS 10 или CMC в структуре **контентинфо** ASN. 1 с помощью одного из следующих типов содержимого. Инкапсуляция позволяет добавлять дополнительные функции, например несколько подписей, которые в других случаях недоступны.

-   **Данные**
-   **сигнеддата**
-   **енвелопеддата**
-   **сигнеданденвелопеддата**
-   **дижестеддата**
-   **EncryptedData**

Атрибуты можно добавить в поля **аусентикатедаттрибутес** и **Унаусентикатедаттрибутес** типа содержимого **сигнеддата** .

``` syntax
SignedData ::= SEQUENCE 
{
   version             INTEGER,
   digestAlgorithms    DigestAlgorithmIdentifiers,
   contentInfo         ContentInfo,
   certificates        [0] IMPLICIT Certificates OPTIONAL,
   crls                [1] IMPLICIT CertificateRevocationLists OPTIONAL,
   signerInfos         SignerInfos
}

SignerInfos ::= SET OF SignerInfo

SignerInfo ::= SEQUENCE 
{
    version                     INTEGER,
    sid                         CertIdentifier,
    digestAlgorithm             DigestAlgorithmIdentifier,
    authenticatedAttributes     [0] IMPLICIT Attributes OPTIONAL,
    digestEncryptionAlgorithm   DigestEncryptionAlgId,
    encryptedDigest             EncryptedDigest,
    unauthenticatedAttributes   [1] IMPLICIT Attributes
}

Attributes ::= SET OF Attribute

Attribute ::= SEQUENCE 
{
   type       EncodedObjectID,
   values     AttributeSetValue
}
```

Процесс, необходимый для архивации закрытого ключа клиента в центре сертификации (ЦС), предоставляет исчерпывающий пример того, как можно использовать атрибуты с проверкой подлинности (подписанный) и непроверенные атрибуты.

-   Клиент создает объект [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) и добавляет соответствующие данные для типа запрашиваемого сертификата.
-   Клиент использует \# запрос PKCS 10 для инициализации объекта [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) . Запрос PKCS \# 10 помещается в структуру **тагжедрекуест** в запросе CMC. Дополнительные сведения см. в разделе [атрибуты CMC](cmc-attributes.md).
-   Клиент шифрует закрытый ключ и использует его для инициализации объекта [**IX509AttributeArchiveKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekey) . Новый атрибут **арчивекэй** инкапсулируется в структуре **енвелопеддата** .

    ``` syntax
    EnvelopedData ::= SEQUENCE 
    {
        version                 INTEGER,
        recipientInfos          RecipientInfos,
        encryptedContentInfo    EncryptedContentInfo
    } 

    RecipientInfos ::= SET OF RecipientInfo

    EncryptedContentInfo ::= SEQUENCE 
    {
        contentType                 ContentType,
        contentEncryptionAlgorithm  ContentEncryptionAlgId,
        encryptedContent            [0] IMPLICIT EncryptedContent OPTIONAL
    } 

    EncryptedContent ::= OCTET STRING

    RecipientInfo ::= SEQUENCE 
    {
        version                 INTEGER,
        issuerAndSerialNumber   IssuerAndSerialNumber,
        keyEncryptionAlgorithm  KeyEncryptionAlgId,
        encryptedKey            EncryptedKey
    } 
    ```

-   Клиент создает хэш SHA-1 зашифрованного ключа и использует его для инициализации объекта [**IX509AttributeArchiveKeyHash**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekeyhash) .
-   Клиент получает коллекцию [**криптаттрибутес**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_cryptattributes) из запроса CMC и добавляет к ней атрибуты **арчивекэй** и **арчивекэйхаш** . Атрибуты помещаются в структуру **тагжедаттрибутес** запроса CMC.
-   Клиент использует запрос CMC для инициализации объекта [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) . Это помещает запрос CMC в поле **контентинфо** \# структуры PKCS 7 **сигнеддата** .
-   Атрибут **арчивекэйхаш** подписывается и помещается в последовательность **аусентикатедаттрибутес** структуры **SignerInfo** .
-   Атрибут **арчивекэй** помещается в последовательность **унаусентикатедаттрибутес** структуры **SignerInfo** , связанной с основным подписавшим \# сообщения PKCS 7.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Поддерживаемые атрибуты](supported-attributes.md)
</dt> </dl>

 

 



