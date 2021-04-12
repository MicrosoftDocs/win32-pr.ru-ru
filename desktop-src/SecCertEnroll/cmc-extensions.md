---
description: Расширения включаются в запрос CMC путем добавления их в структуру Тагжедаттрибутес, показанную в следующем примере синтаксиса ASN. 1. Дополнительные сведения см. в разделе атрибуты.
ms.assetid: 3aa9175b-f889-4d5d-8eb2-a8a42f9fe750
title: Расширения CMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b104af2b28470627ea593321627ae5e5076b1e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265636"
---
# <a name="cmc-extensions"></a>Расширения CMC

Расширения включаются в запрос CMC путем добавления их в структуру **тагжедаттрибутес** , показанную в следующем примере синтаксиса ASN. 1. Дополнительные сведения см. в разделе [атрибуты](attributes.md) .

``` syntax
CmcData ::= SEQUENCE 
{
   controlSequence         ControlSequence,
   reqSequence             ReqSequence,
   cmsSequence             CmsSequence,
   otherMsgSequence        OtherMsgSequence
}


ControlSequence  ::=    SEQUENCE OF TaggedAttribute

TaggedAttribute ::= SEQUENCE 
{
   bodyPartID              BodyPartID,
   type                    EncodedObjectID,
   values                  AttributeSetValue
}

BodyPartID ::= INTEGER (0..4294967295)
EncodedObjectID ::= OBJECT IDENTIFIER
AttributeSetValue ::= SET OF ANY
```

Каждая структура в коллекции **тагжедаттрибутес** содержит целочисленный идентификатор, идентификатор объекта ASN. 1 и набор значений. Расширения включаются в запрос путем добавления структуры **кмкаддекстенсионс** в поле **Values** . Синтаксис структуры ASN. 1 показан в следующем примере. Идентификатор объекта — **кскн \_ OID \_ CMC \_ Add \_ Extensions** (1.3.6.1.5.5.7.7.8).

``` syntax
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
```

В следующей процедуре описывается, как использовать API регистрации сертификатов для добавления расширений в запрос сертификата CMC.

**Использование API регистрации сертификатов для добавления расширений в запрос сертификата CMC**

1.  Создайте расширение с помощью любого из доступных интерфейсов, производных от интерфейса [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) , или непосредственно используйте объект **IX509Extension** для создания пользовательских расширений.
2.  Вызовите свойство [**X509Extensions**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_x509extensions) объекта [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) , чтобы получить коллекцию [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) .
3.  Добавьте расширения, созданные на шаге 1, в коллекцию [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) .
4.  Вызовите [**регистрацию**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) , чтобы автоматически выполнить следующие действия:
    -   Извлеките объект [**икриптаттрибутес**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) из объекта [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) .
    -   Создайте и инициализируйте объект [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) с помощью коллекции [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) , полученной на шаге 2.
    -   Создайте коллекцию [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) и добавьте в нее объект [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) .
    -   Используйте коллекцию [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) для инициализации объекта [**икриптаттрибуте**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) .
    -   Добавьте объект [**икриптаттрибуте**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) в коллекцию [**икриптаттрибутес**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) .

## <a name="related-topics"></a>См. также

<dl> <dt>

[Атрибуты](attributes.md)
</dt> <dt>

[Архитектура атрибута](attribute-architecture.md)
</dt> <dt>

[Атрибуты CMC](cmc-attributes.md)
</dt> <dt>

[Расширения](extensions.md)
</dt> </dl>

 

 



