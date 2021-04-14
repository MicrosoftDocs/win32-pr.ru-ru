---
description: Атрибуты включаются в \# запрос сертификата PKCS 10 путем их добавления в структуру CertificationRequestInfo, показанную в следующем примере синтаксиса ASN. 1.
ms.assetid: 5f00f638-9edb-474b-a7e4-f6f7b62c89a4
title: '\#АТРИБУТЫ PKCS 10'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6c69260fa09b99c4d91fa1f8bcdafeb4b0da285
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350185"
---
# <a name="pkcs-10-attributes"></a>\#АТРИБУТЫ PKCS 10

Атрибуты включаются в \# запрос сертификата PKCS 10 путем их добавления в структуру **CertificationRequestInfo** , показанную в следующем примере синтаксиса ASN. 1. Дополнительные сведения о том, как можно добавить атрибуты в запрос, см. в разделе об [архитектуре атрибута](attribute-architecture.md) .

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

Атрибут, наиболее часто добавляемый в \# запрос PKCS 10, представляет собой коллекцию расширений версии 3, определенных объектом [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) . Поскольку запрос PKCS \# 10 не содержит поле, к которому можно напрямую добавить расширения, они должны быть добавлены в качестве атрибута. Атрибуты **ClientID**, **ксппровидер**, **OSVersion** и **реневалцертификате** также можно добавить в файл PKCS.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Поддерживаемые атрибуты](supported-attributes.md)
</dt> </dl>

 

 



