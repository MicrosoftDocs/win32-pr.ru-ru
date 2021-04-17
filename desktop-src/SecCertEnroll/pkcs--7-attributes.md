---
description: PKCS \# 7 — это стандартный синтаксис криптографического сообщения.
ms.assetid: fd4e2a13-f257-4ba9-a11d-35f49c5a6c00
title: '\#АТРИБУТЫ PKCS 7'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce0c7bc9b991a6625cae36ae9857275a9d86786a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684166"
---
# <a name="pkcs-7-attributes"></a><span data-ttu-id="70477-103">\#АТРИБУТЫ PKCS 7</span><span class="sxs-lookup"><span data-stu-id="70477-103">PKCS \#7 Attributes</span></span>

<span data-ttu-id="70477-104">PKCS \# 7 — это стандартный синтаксис криптографического сообщения.</span><span class="sxs-lookup"><span data-stu-id="70477-104">PKCS \#7 is a cryptographic message syntax standard.</span></span> <span data-ttu-id="70477-105">Сообщение PKCS \# 7 само по себе не является запросом на сертификат, но может инкапсулировать \# запрос PKCS 10 или CMC в структуре **контентинфо** ASN. 1 с помощью одного из следующих типов содержимого.</span><span class="sxs-lookup"><span data-stu-id="70477-105">A PKCS \#7 message does not, by itself, constitute a certificate request, but it can encapsulate a PKCS \#10 or CMC request in a **ContentInfo** ASN.1 structure by using one of the following content types.</span></span> <span data-ttu-id="70477-106">Инкапсуляция позволяет добавлять дополнительные функции, например несколько подписей, которые в других случаях недоступны.</span><span class="sxs-lookup"><span data-stu-id="70477-106">Encapsulation enables you to add extra functionality, such as multiple signatures, that is not otherwise available.</span></span>

-   <span data-ttu-id="70477-107">**Data**</span><span class="sxs-lookup"><span data-stu-id="70477-107">**Data**</span></span>
-   <span data-ttu-id="70477-108">**сигнеддата**</span><span class="sxs-lookup"><span data-stu-id="70477-108">**SignedData**</span></span>
-   <span data-ttu-id="70477-109">**енвелопеддата**</span><span class="sxs-lookup"><span data-stu-id="70477-109">**EnvelopedData**</span></span>
-   <span data-ttu-id="70477-110">**сигнеданденвелопеддата**</span><span class="sxs-lookup"><span data-stu-id="70477-110">**SignedAndEnvelopedData**</span></span>
-   <span data-ttu-id="70477-111">**дижестеддата**</span><span class="sxs-lookup"><span data-stu-id="70477-111">**DigestedData**</span></span>
-   <span data-ttu-id="70477-112">**EncryptedData**</span><span class="sxs-lookup"><span data-stu-id="70477-112">**EncryptedData**</span></span>

<span data-ttu-id="70477-113">Атрибуты можно добавить в поля **аусентикатедаттрибутес** и **Унаусентикатедаттрибутес** типа содержимого **сигнеддата** .</span><span class="sxs-lookup"><span data-stu-id="70477-113">Attributes can be added to the **authenticatedAttributes** and **unauthenticatedAttributes** fields of the **SignedData** content type.</span></span>

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

<span data-ttu-id="70477-114">Процесс, необходимый для архивации закрытого ключа клиента в центре сертификации (ЦС), предоставляет исчерпывающий пример того, как можно использовать атрибуты с проверкой подлинности (подписанный) и непроверенные атрибуты.</span><span class="sxs-lookup"><span data-stu-id="70477-114">The process required to archive a client's private key on a certification authority (CA) provides a comprehensive example of how authenticated (signed) attributes and the unauthenticated attributes can be used:</span></span>

-   <span data-ttu-id="70477-115">Клиент создает объект [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) и добавляет соответствующие данные для типа запрашиваемого сертификата.</span><span class="sxs-lookup"><span data-stu-id="70477-115">The client creates an [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) object and adds appropriate data for the type of certificate being requested.</span></span>
-   <span data-ttu-id="70477-116">Клиент использует \# запрос PKCS 10 для инициализации объекта [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) .</span><span class="sxs-lookup"><span data-stu-id="70477-116">The client uses the PKCS \#10 request to initialize an [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) object.</span></span> <span data-ttu-id="70477-117">Запрос PKCS \# 10 помещается в структуру **тагжедрекуест** в запросе CMC.</span><span class="sxs-lookup"><span data-stu-id="70477-117">The PKCS \#10 request is placed into the **TaggedRequest** structure in the CMC request.</span></span> <span data-ttu-id="70477-118">Дополнительные сведения см. в разделе [атрибуты CMC](cmc-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="70477-118">For more information, see [CMC Attributes](cmc-attributes.md).</span></span>
-   <span data-ttu-id="70477-119">Клиент шифрует закрытый ключ и использует его для инициализации объекта [**IX509AttributeArchiveKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekey) .</span><span class="sxs-lookup"><span data-stu-id="70477-119">The client encrypts a private key and uses it to initialize an [**IX509AttributeArchiveKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekey) object.</span></span> <span data-ttu-id="70477-120">Новый атрибут **арчивекэй** инкапсулируется в структуре **енвелопеддата** .</span><span class="sxs-lookup"><span data-stu-id="70477-120">The new **ArchiveKey** attribute is encapsulated in an **EnvelopedData** structure.</span></span>

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

-   <span data-ttu-id="70477-121">Клиент создает хэш SHA-1 зашифрованного ключа и использует его для инициализации объекта [**IX509AttributeArchiveKeyHash**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekeyhash) .</span><span class="sxs-lookup"><span data-stu-id="70477-121">The client creates a SHA-1 hash of the encrypted key and uses it to initialize an [**IX509AttributeArchiveKeyHash**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekeyhash) object.</span></span>
-   <span data-ttu-id="70477-122">Клиент получает коллекцию [**криптаттрибутес**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_cryptattributes) из запроса CMC и добавляет к ней атрибуты **арчивекэй** и **арчивекэйхаш** .</span><span class="sxs-lookup"><span data-stu-id="70477-122">The client retrieves the [**CryptAttributes**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_cryptattributes) collection from the CMC request and adds the **ArchiveKey** and the **ArchiveKeyHash** attributes to it.</span></span> <span data-ttu-id="70477-123">Атрибуты помещаются в структуру **тагжедаттрибутес** запроса CMC.</span><span class="sxs-lookup"><span data-stu-id="70477-123">The attributes are placed into the **TaggedAttributes** structure of the CMC request.</span></span>
-   <span data-ttu-id="70477-124">Клиент использует запрос CMC для инициализации объекта [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) .</span><span class="sxs-lookup"><span data-stu-id="70477-124">The client uses the CMC request to initialize an [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) object.</span></span> <span data-ttu-id="70477-125">Это помещает запрос CMC в поле **контентинфо** \# структуры PKCS 7 **сигнеддата** .</span><span class="sxs-lookup"><span data-stu-id="70477-125">This places the CMC request into the **contentInfo** field of the PKCS \#7 **SignedData** structure.</span></span>
-   <span data-ttu-id="70477-126">Атрибут **арчивекэйхаш** подписывается и помещается в последовательность **аусентикатедаттрибутес** структуры **SignerInfo** .</span><span class="sxs-lookup"><span data-stu-id="70477-126">The **ArchiveKeyHash** attribute is signed and placed in the **authenticatedAttributes** sequence of the **SignerInfo** structure.</span></span>
-   <span data-ttu-id="70477-127">Атрибут **арчивекэй** помещается в последовательность **унаусентикатедаттрибутес** структуры **SignerInfo** , связанной с основным подписавшим \# сообщения PKCS 7.</span><span class="sxs-lookup"><span data-stu-id="70477-127">The **ArchiveKey** attribute is placed in the **unauthenticatedAttributes** sequence of the **SignerInfo** structure associated with the primary signer of the PKCS \#7 message.</span></span>

## <a name="related-topics"></a><span data-ttu-id="70477-128">См. также</span><span class="sxs-lookup"><span data-stu-id="70477-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="70477-129">Поддерживаемые атрибуты</span><span class="sxs-lookup"><span data-stu-id="70477-129">Supported Attributes</span></span>](supported-attributes.md)
</dt> </dl>

 

 



