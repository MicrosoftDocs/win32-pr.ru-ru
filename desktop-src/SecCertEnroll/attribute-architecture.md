---
description: Используется для добавления атрибутов в запрос сертификата.
ms.assetid: 7007c751-f1a4-4ddc-a66e-d3edefc6ed97
title: Архитектура атрибута
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64d83171985c062fd2d8d4ae968c2ef4d36a29ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344952"
---
# <a name="attribute-architecture"></a>Архитектура атрибута

Для добавления атрибутов в запрос сертификата используются следующие интерфейсы:

-   [**икриптаттрибуте**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute)
-   [**икриптаттрибутес**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)
-   [**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute)
-   [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes)

Ниже приведена архитектура, определенная в модуле ASN. 1 \# синтаксиса запроса на сертификацию PKCS 10.

``` syntax
CertificationRequestInfo ::= SEQUENCE 
{
   version                 CertificationRequestInfoVersion,
   subject                 ANY,
   subjectPublicKeyInfo    SubjectPublicKeyInfo,
   attributes              [0] IMPLICIT Attributes
}

Attributes ::= SET OF Attribute

Attribute ::= SEQUENCE 
{
   type       EncodedObjectID,
   values     AttributeSetValue
}
```

Коллекция [**икриптаттрибутес**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) соответствует полю **Attributes** , а каждый объект [**Икриптаттрибуте**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) в коллекции соответствует структуре **атрибута** ASN. 1.

Каждый **атрибут** состоит из идентификатора объекта (OID) и от нуля или более значений, связанных с OID. Одна пара OID-значение представляется интерфейсом [**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute) . Вы можете использовать коллекцию [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) для инициализации объекта [**икриптаттрибуте**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) , но каждый атрибут в коллекции должен быть связан с одним и тем же идентификатором OID. Как правило, атрибут имеет только одно значение.

Для создания одной пары атрибутов OID/значение можно использовать любой из следующих интерфейсов, которые являются производными от [**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute).

-   [**IX509AttributeClientId**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid)
-   [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions)
-   [**IX509AttributeArchiveKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekey)
-   [**IX509AttributeArchiveKeyHash**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekeyhash)
-   [**IX509AttributeCspProvider**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributecspprovider)
-   [**IX509AttributeOSVersion**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeosversion)
-   [**IX509AttributeRenewalCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributerenewalcertificate)

Например, в следующей процедуре показано, как создать атрибут **ClientID** .

**Создание атрибута **ClientID****

1.  Получите объект [**икриптаттрибутес**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) из объекта [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) или [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) .
2.  Создание и инициализация объекта [**IX509AttributeClientId**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid) .
3.  Создайте коллекцию [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) и добавьте объект [**IX509AttributeClientId**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid) .
4.  Используйте коллекцию [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) для инициализации объекта [**икриптаттрибуте**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) .
5.  Добавьте объект [**икриптаттрибуте**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) в коллекцию, полученную на шаге 1.

В следующем примере показаны выходные данные ASN. 1 атрибута **ClientID** . Атрибут содержит DNS-имя компьютера, на котором был создан запрос (test3d.jdomcsc.nttest.microsoft.com), имя SAM пользователя ( \\ Администратор ждомкск) и имя приложения, создавшего запрос (certreq).

``` syntax
0136: 30 57; SEQUENCE (57 Bytes)
0138: |  06 09                            ; OBJECT_ID (9 Bytes)
013a: |  |  2b 06 01 04 01 82 37 15  14
      |  |     ; 1.3.6.1.4.1.311.21.20 Client Information
0143: |  |  31 4a                         ; SET (4a Bytes)
0145: |  |     30 48                      ; SEQUENCE (48 Bytes)
0147: |  |        02 01                   ; INTEGER (1 Bytes)
0149: |  |        |  09
014a: |  |        0c 23                   ; UTF8_STRING (23 Bytes)
014c: |  |        |  74 65 73 74 33 64 2e 6a  64 6f 6d 63 73 63 2e 6e 
015c: |  |        |  74 74 65 73 74 2e 6d 69  63 72 6f 73 6f 66 74 2e 
016c: |  |        |  63 6f 6d                                         
      |  |        |     ; "test3d.jdomcsc.nttest.microsoft.com"
016f: |  |        0c 15                   ; UTF8_STRING (15 Bytes)
0171: |  |        |  4a 44 4f 4d 43 53 43 5c  61 64 6d 69 6e 69 73 74 
0181: |  |        |  72 61 74 6f 72                                   
      |  |        |     ; "JDOMCSC\administrator"
0186: |  |        0c 07                   ; UTF8_STRING (7 Bytes)
0188: |  |           63 65 72 74 72 65 71                             
      |  |              ; "certreq"
```

## <a name="related-topics"></a>См. также

<dl> <dt>

[**икриптаттрибуте**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute)
</dt> <dt>

[**икриптаттрибутес**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)
</dt> <dt>

[**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute)
</dt> <dt>

[**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes)
</dt> </dl>

 

 



