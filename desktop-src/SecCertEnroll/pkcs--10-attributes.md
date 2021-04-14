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
# <a name="pkcs-10-attributes"></a><span data-ttu-id="ed520-103">\#АТРИБУТЫ PKCS 10</span><span class="sxs-lookup"><span data-stu-id="ed520-103">PKCS \#10 Attributes</span></span>

<span data-ttu-id="ed520-104">Атрибуты включаются в \# запрос сертификата PKCS 10 путем их добавления в структуру **CertificationRequestInfo** , показанную в следующем примере синтаксиса ASN. 1.</span><span class="sxs-lookup"><span data-stu-id="ed520-104">Attributes are included in a PKCS \#10 certificate request by adding them to the **CertificationRequestInfo** structure shown in the following ASN.1 syntax example.</span></span> <span data-ttu-id="ed520-105">Дополнительные сведения о том, как можно добавить атрибуты в запрос, см. в разделе об [архитектуре атрибута](attribute-architecture.md) .</span><span class="sxs-lookup"><span data-stu-id="ed520-105">For more information about how you can add attributes to a request, see the [Attribute Architecture](attribute-architecture.md) topic.</span></span>

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

<span data-ttu-id="ed520-106">Атрибут, наиболее часто добавляемый в \# запрос PKCS 10, представляет собой коллекцию расширений версии 3, определенных объектом [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) .</span><span class="sxs-lookup"><span data-stu-id="ed520-106">The attribute most commonly added to a PKCS \#10 request is a collection of version 3 extensions defined by an [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) object.</span></span> <span data-ttu-id="ed520-107">Поскольку запрос PKCS \# 10 не содержит поле, к которому можно напрямую добавить расширения, они должны быть добавлены в качестве атрибута.</span><span class="sxs-lookup"><span data-stu-id="ed520-107">Because a PKCS \#10 request does not contain a field to which the extensions can be directly added, they must be added as an attribute.</span></span> <span data-ttu-id="ed520-108">Атрибуты **ClientID**, **ксппровидер**, **OSVersion** и **реневалцертификате** также можно добавить в файл PKCS.</span><span class="sxs-lookup"><span data-stu-id="ed520-108">The **ClientId**, **CspProvider**, **OSVersion**, and **RenewalCertificate** attributes can also be added to a PKCS ) topic.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ed520-109">См. также</span><span class="sxs-lookup"><span data-stu-id="ed520-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed520-110">Поддерживаемые атрибуты</span><span class="sxs-lookup"><span data-stu-id="ed520-110">Supported Attributes</span></span>](supported-attributes.md)
</dt> </dl>

 

 



