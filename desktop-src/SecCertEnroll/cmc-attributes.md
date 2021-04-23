---
description: На практике структура запроса CMC, показанная в следующем синтаксисе, относительно сложна, так как часто содержит вложенные запросы.
ms.assetid: faeee338-bce4-4b35-9be9-72a6568fa259
title: Атрибуты CMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e6778575a9359ad5b8764528fb0351b68efc1e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815785"
---
# <a name="cmc-attributes"></a><span data-ttu-id="4cff0-103">Атрибуты CMC</span><span class="sxs-lookup"><span data-stu-id="4cff0-103">CMC Attributes</span></span>

<span data-ttu-id="4cff0-104">На практике структура запроса CMC, показанная в следующем синтаксисе, относительно сложна, так как часто содержит вложенные запросы.</span><span class="sxs-lookup"><span data-stu-id="4cff0-104">In practice, the structure of a CMC request, shown by the following syntax, is relatively complex because it often contains nested requests.</span></span> <span data-ttu-id="4cff0-105">Например, запрос CMC может содержать ноль или один запрос PKCS \# 10 в последовательности **тагжедрекуест** , а также может содержать ноль или одно \# сообщение PKCS 7 в последовательности **тагжедконтентинфо** .</span><span class="sxs-lookup"><span data-stu-id="4cff0-105">For example, a CMC request can contain zero or one PKCS \#10 requests in a **TaggedRequest** sequence, and it can contain zero or one PKCS \#7 messages in a **TaggedContentInfo** sequence.</span></span> <span data-ttu-id="4cff0-106">Каждое вложенное \# сообщение PKCS 7 может содержать запрос CMC, который, в свою очередь, может содержать больше запросов.</span><span class="sxs-lookup"><span data-stu-id="4cff0-106">Each nested PKCS \#7 message can contain a CMC request which can, in turn, contain more requests.</span></span> <span data-ttu-id="4cff0-107">Число уровней вложенности теоретически не ограничено, но центр сертификации (ЦС) обычно настроен для ограничения размера запроса.</span><span class="sxs-lookup"><span data-stu-id="4cff0-107">The number of nesting levels is theoretically unlimited, but the certification authority (CA) is typically configured to limit the size of a request.</span></span> <span data-ttu-id="4cff0-108">Атрибуты могут применяться к запросу верхнего уровня или к вложенным запросам.</span><span class="sxs-lookup"><span data-stu-id="4cff0-108">Attributes can be applied to the top level request or to the nested requests.</span></span> <span data-ttu-id="4cff0-109">Это описано в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="4cff0-109">This is discussed in the following sections.</span></span>

## <a name="cmcdata-structure"></a><span data-ttu-id="4cff0-110">Структура Кмкдата</span><span class="sxs-lookup"><span data-stu-id="4cff0-110">CMCData Structure</span></span>

<span data-ttu-id="4cff0-111">Запрос CMC содержит последовательности структур **тагжедаттрибуте**, **тагжедрекуест** и **тагжедконтентинфо** ASN. 1.</span><span class="sxs-lookup"><span data-stu-id="4cff0-111">A CMC request contains sequences of **TaggedAttribute**, **TaggedRequest**, and **TaggedContentInfo** ASN.1 structures.</span></span>

``` syntax
CmcData ::= SEQUENCE 
{
   controlSequence         ControlSequence,
   reqSequence             ReqSequence,
   cmsSequence             CmsSequence,
   otherMsgSequence        OtherMsgSequence
}


ControlSequence  ::=    SEQUENCE OF TaggedAttribute
ReqSequence      ::=    SEQUENCE OF TaggedRequest
CmsSequence      ::=    SEQUENCE OF TaggedContentInfo

TaggedAttribute ::= SEQUENCE 
{
   bodyPartID              BodyPartID,
   type                    EncodedObjectID,
   values                  AttributeSetValue
}

TaggedRequest ::= CHOICE 
{
   tcr                     [0] IMPLICIT TaggedCertificationRequest
}

TaggedContentInfo ::= SEQUENCE 
{
   bodyPartID              BodyPartID,
   contentInfo             ANY
}

BodyPartID ::= INTEGER (0..4294967295)
EncodedObjectID ::= OBJECT IDENTIFIER
AttributeSetValue ::= SET OF ANY
```

## <a name="taggedattribute-structure"></a><span data-ttu-id="4cff0-112">Структура Тагжедаттрибуте</span><span class="sxs-lookup"><span data-stu-id="4cff0-112">TaggedAttribute Structure</span></span>

<span data-ttu-id="4cff0-113">Атрибуты включаются в запрос сертификата CMC путем их добавления в коллекцию **тагжедаттрибуте** .</span><span class="sxs-lookup"><span data-stu-id="4cff0-113">Attributes are included in a CMC certificate request by adding them to the **TaggedAttribute** collection.</span></span> <span data-ttu-id="4cff0-114">Каждая структура в коллекции содержит целочисленный идентификатор, идентификатор объекта ASN. 1 и набор значений.</span><span class="sxs-lookup"><span data-stu-id="4cff0-114">Each structure in the collection contains an integer ID, an ASN.1 object identifier (OID), and a set of values.</span></span> <span data-ttu-id="4cff0-115">Возможные значения могут быть любыми из следующих.</span><span class="sxs-lookup"><span data-stu-id="4cff0-115">The possible values can be any of the following.</span></span>

``` syntax
CmcAddAttributes ::= SEQUENCE 
{
   pkiDataReference        BodyPartID,
   certReferences          BodyPartIDSequence,
   attributes              Attributes
}

Attributes ::= SET OF Attribute
Attribute ::= SEQUENCE 
{
   type       EncodedObjectID,
   values     AttributeSetValue
}

CmcAddExtensions ::= SEQUENCE 
{
   pkiDataReference        BodyPartID,
   certReferences          BodyPartIDSequence,
   extensions              Extensions
}

Extensions ::= SEQUENCE OF Extension

Extension ::= SEQUENCE 
{
   extnId              EncodedObjectID,
   critical            BOOLEAN DEFAULT FALSE,
   extnValue           OCTETSTRING
}

SenderNonce ::= OCTET STRING

TransactID ::= OCTET STRING

RegInfo ::= OCTET STRING
```

## <a name="cmcaddattributes"></a><span data-ttu-id="4cff0-116">кмкаддаттрибутес</span><span class="sxs-lookup"><span data-stu-id="4cff0-116">CMCAddAttributes</span></span>

<span data-ttu-id="4cff0-117">Если атрибуты в этой структуре применяются к вложенному запросу PKCS \# 10, поле **цертреференцес** будет содержать **бодипартид** , который идентифицирует запрос.</span><span class="sxs-lookup"><span data-stu-id="4cff0-117">If the attributes in this structure apply to a nested PKCS \#10 request, the **certReferences** field will contain the **BodyPartID** that identifies the request.</span></span> <span data-ttu-id="4cff0-118">Если атрибуты применяются к вложенному запросу CMC, поле **пкидатареференце** будет содержать **бодипартид** запроса.</span><span class="sxs-lookup"><span data-stu-id="4cff0-118">If the attributes apply to a nested CMC request, the **pkiDataReference** field will contain the **BodyPartID** of the request.</span></span> <span data-ttu-id="4cff0-119">В настоящее время только одно из этих полей может быть ненулевым.</span><span class="sxs-lookup"><span data-stu-id="4cff0-119">Currently, only one of these fields can be nonzero.</span></span> <span data-ttu-id="4cff0-120">Атрибуты, которые могут быть включены, перечислены в разделе [Поддерживаемые атрибуты](supported-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="4cff0-120">The attributes that can be included are listed in the [Supported Attributes](supported-attributes.md) topic.</span></span>

## <a name="cmcaddextensions"></a><span data-ttu-id="4cff0-121">кмкаддекстенсионс</span><span class="sxs-lookup"><span data-stu-id="4cff0-121">CmcAddExtensions</span></span>

<span data-ttu-id="4cff0-122">Эта структура может содержать расширения X. 509 версии 3 и расширения, определенные корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="4cff0-122">This structure can contain X.509 version 3 extensions plus extensions defined by Microsoft.</span></span> <span data-ttu-id="4cff0-123">Этот атрибут определяется с помощью интерфейса [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) .</span><span class="sxs-lookup"><span data-stu-id="4cff0-123">This attribute is defined by using the [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) interface.</span></span> <span data-ttu-id="4cff0-124">Если расширения применяются к вложенному запросу PKCS \# 10, поле **цертреференцес** будет содержать **бодипартид** , который идентифицирует запрос.</span><span class="sxs-lookup"><span data-stu-id="4cff0-124">If the extensions apply to a nested PKCS \#10 request, the **certReferences** field will contain the **BodyPartID** that identifies the request.</span></span> <span data-ttu-id="4cff0-125">Если расширения применяются к вложенному запросу CMC, поле **пкидатареференце** будет содержать **бодипартид** запроса.</span><span class="sxs-lookup"><span data-stu-id="4cff0-125">If the extensions apply to a nested CMC request, the **pkiDataReference** field will contain the **BodyPartID** of the request.</span></span> <span data-ttu-id="4cff0-126">В настоящее время только одно из этих полей может быть ненулевым.</span><span class="sxs-lookup"><span data-stu-id="4cff0-126">Currently, only one of these fields can be nonzero.</span></span>

## <a name="sendernonce"></a><span data-ttu-id="4cff0-127">сендернонце</span><span class="sxs-lookup"><span data-stu-id="4cff0-127">SenderNonce</span></span>

<span data-ttu-id="4cff0-128">Nonce — это случайные или псевдо-случайные двоичные данные, которые можно включать в запрос на сертификат и транзакцию ответа, чтобы гарантировать, что ответ или запрос не повторяется в предыдущем сообщении.</span><span class="sxs-lookup"><span data-stu-id="4cff0-128">A nonce is random or pseudo-random binary data that can be included in a certificate request and response transaction to help ensure that the response or request is not a repeat of a previous message.</span></span> <span data-ttu-id="4cff0-129">Дополнительные сведения см. в описании свойства [**сендернонце**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_sendernonce) .</span><span class="sxs-lookup"><span data-stu-id="4cff0-129">For more information, see the [**SenderNonce**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_sendernonce) property.</span></span>

## <a name="transactid"></a><span data-ttu-id="4cff0-130">трансактид</span><span class="sxs-lookup"><span data-stu-id="4cff0-130">TransactID</span></span>

<span data-ttu-id="4cff0-131">Запрос сертификата кругового пути и транзакция ответа могут быть отслеживанием с помощью идентификатора.</span><span class="sxs-lookup"><span data-stu-id="4cff0-131">A round trip certificate request and response transaction can be tracked using an identifier.</span></span> <span data-ttu-id="4cff0-132">Клиент создает идентификатор транзакции и удерживает его до тех пор, пока сертификат или центр регистрации не ответит сообщением, завершающим транзакцию.</span><span class="sxs-lookup"><span data-stu-id="4cff0-132">The client generates a transaction ID and retains it until the certificate or registration authority responds with a message that completes the transaction.</span></span> <span data-ttu-id="4cff0-133">Ответ содержит идентификатор.</span><span class="sxs-lookup"><span data-stu-id="4cff0-133">The response includes the identifier.</span></span> <span data-ttu-id="4cff0-134">Дополнительные сведения см. в описании свойства [**ИД транзакции**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_transactionid) .</span><span class="sxs-lookup"><span data-stu-id="4cff0-134">For more information, see the [**TransactionId**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_transactionid) property.</span></span>

## <a name="reginfo"></a><span data-ttu-id="4cff0-135">регинфо</span><span class="sxs-lookup"><span data-stu-id="4cff0-135">RegInfo</span></span>

<span data-ttu-id="4cff0-136">Этот атрибут может использоваться для хранения сведений о регистрации, которые клиент выбирает для постановки в запрос CMC.</span><span class="sxs-lookup"><span data-stu-id="4cff0-136">This attribute can be used to contain any registration information that the client chooses to put into the CMC request.</span></span> <span data-ttu-id="4cff0-137">Значение атрибута — строка, содержащая объединенные пары "имя-значение".</span><span class="sxs-lookup"><span data-stu-id="4cff0-137">The attribute value is string that contains concatenated name-value pairs.</span></span> <span data-ttu-id="4cff0-138">Дополнительные сведения см. в описании свойства [**намевалуепаирс**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_namevaluepairs) .</span><span class="sxs-lookup"><span data-stu-id="4cff0-138">For more information, see the [**NameValuePairs**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_namevaluepairs) property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4cff0-139">См. также</span><span class="sxs-lookup"><span data-stu-id="4cff0-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4cff0-140">Поддерживаемые атрибуты</span><span class="sxs-lookup"><span data-stu-id="4cff0-140">Supported Attributes</span></span>](supported-attributes.md)
</dt> </dl>

 

 



