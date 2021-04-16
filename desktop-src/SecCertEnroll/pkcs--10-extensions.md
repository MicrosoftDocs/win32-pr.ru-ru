---
description: Расширения включаются в \# запрос сертификата PKCS 10 путем их добавления в поле Attributes структуры CertificationRequestInfo, как показано в следующем примере синтаксиса ASN. 1. Дополнительные сведения см. в разделе атрибуты.
ms.assetid: 26fa8476-a0ad-4114-a1e7-ed3d4fc9d30e
title: '\#Расширения PKCS 10'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ba71f0a24f50503fd92b3b9670b787dea3b9ad2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664640"
---
# <a name="pkcs-10-extensions"></a>\#Расширения PKCS 10

Расширения включаются в \# запрос сертификата PKCS 10 путем их добавления в поле **Attributes** структуры **CertificationRequestInfo** , как показано в следующем примере синтаксиса ASN. 1. Дополнительные сведения см. в разделе [атрибуты](attributes.md) .

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

В следующей процедуре описывается, как использовать API регистрации сертификатов для добавления расширений в \# запрос сертификата PKCS 10.

1.  Получите коллекцию [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) , вызвав свойство [**X509Extension**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_x509extensions) объекта [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) .
2.  Создайте расширение с помощью любого из доступных интерфейсов, производных от интерфейса [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) .
3.  Добавьте расширения, созданные на шаге 2, в коллекцию [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) , полученную на шаге 1.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Атрибуты](attributes.md)
</dt> <dt>

[Архитектура атрибута](attribute-architecture.md)
</dt> <dt>

[\#АТРИБУТЫ PKCS 10](pkcs--10-attributes.md)
</dt> <dt>

[Расширения](extensions.md)
</dt> </dl>

 

 



