---
description: На практике структура запроса CMC, показанная в следующем синтаксисе, относительно сложна, так как часто содержит вложенные запросы.
ms.assetid: faeee338-bce4-4b35-9be9-72a6568fa259
title: Атрибуты CMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b98e30c257234ebee864a1749ceecee7b79e25a9e11c9f1f190c60f3154ef64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118902067"
---
# <a name="cmc-attributes"></a>Атрибуты CMC

На практике структура запроса CMC, показанная в следующем синтаксисе, относительно сложна, так как часто содержит вложенные запросы. Например, запрос CMC может содержать ноль или один запрос PKCS \# 10 в последовательности **тагжедрекуест** , а также может содержать ноль или одно \# сообщение PKCS 7 в последовательности **тагжедконтентинфо** . Каждое вложенное \# сообщение PKCS 7 может содержать запрос CMC, который, в свою очередь, может содержать больше запросов. Число уровней вложенности теоретически не ограничено, но центр сертификации (ЦС) обычно настроен для ограничения размера запроса. Атрибуты могут применяться к запросу верхнего уровня или к вложенным запросам. Это описано в следующих разделах.

## <a name="cmcdata-structure"></a>Структура Кмкдата

Запрос CMC содержит последовательности структур **тагжедаттрибуте**, **тагжедрекуест** и **тагжедконтентинфо** ASN. 1.

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

## <a name="taggedattribute-structure"></a>Структура Тагжедаттрибуте

Атрибуты включаются в запрос сертификата CMC путем их добавления в коллекцию **тагжедаттрибуте** . Каждая структура в коллекции содержит целочисленный идентификатор, идентификатор объекта ASN. 1 и набор значений. Возможные значения могут быть любыми из следующих.

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

## <a name="cmcaddattributes"></a>кмкаддаттрибутес

Если атрибуты в этой структуре применяются к вложенному запросу PKCS \# 10, поле **цертреференцес** будет содержать **бодипартид** , который идентифицирует запрос. Если атрибуты применяются к вложенному запросу CMC, поле **пкидатареференце** будет содержать **бодипартид** запроса. В настоящее время только одно из этих полей может быть ненулевым. Атрибуты, которые могут быть включены, перечислены в разделе [Поддерживаемые атрибуты](supported-attributes.md) .

## <a name="cmcaddextensions"></a>кмкаддекстенсионс

Эта структура может содержать расширения X. 509 версии 3 и расширения, определенные корпорацией Майкрософт. Этот атрибут определяется с помощью интерфейса [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) . Если расширения применяются к вложенному запросу PKCS \# 10, поле **цертреференцес** будет содержать **бодипартид** , который идентифицирует запрос. Если расширения применяются к вложенному запросу CMC, поле **пкидатареференце** будет содержать **бодипартид** запроса. В настоящее время только одно из этих полей может быть ненулевым.

## <a name="sendernonce"></a>сендернонце

Nonce — это случайные или псевдо-случайные двоичные данные, которые можно включать в запрос на сертификат и транзакцию ответа, чтобы гарантировать, что ответ или запрос не повторяется в предыдущем сообщении. Дополнительные сведения см. в описании свойства [**сендернонце**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_sendernonce) .

## <a name="transactid"></a>трансактид

Запрос сертификата кругового пути и транзакция ответа могут быть отслеживанием с помощью идентификатора. Клиент создает идентификатор транзакции и удерживает его до тех пор, пока сертификат или центр регистрации не ответит сообщением, завершающим транзакцию. Ответ содержит идентификатор. Дополнительные сведения см. в описании свойства [**ИД транзакции**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_transactionid) .

## <a name="reginfo"></a>регинфо

Этот атрибут может использоваться для хранения сведений о регистрации, которые клиент выбирает для постановки в запрос CMC. Значение атрибута — строка, содержащая объединенные пары "имя-значение". Дополнительные сведения см. в описании свойства [**намевалуепаирс**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_namevaluepairs) .

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Поддерживаемые атрибуты](supported-attributes.md)
</dt> </dl>

 

 



