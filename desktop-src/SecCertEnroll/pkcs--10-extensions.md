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
# <a name="pkcs-10-extensions"></a><span data-ttu-id="67913-104">\#Расширения PKCS 10</span><span class="sxs-lookup"><span data-stu-id="67913-104">PKCS \#10 Extensions</span></span>

<span data-ttu-id="67913-105">Расширения включаются в \# запрос сертификата PKCS 10 путем их добавления в поле **Attributes** структуры **CertificationRequestInfo** , как показано в следующем примере синтаксиса ASN. 1.</span><span class="sxs-lookup"><span data-stu-id="67913-105">Extensions are included in a PKCS \#10 certificate request by adding them to the **attributes** field of the **CertificationRequestInfo** structure shown in the following ASN.1 syntax example.</span></span> <span data-ttu-id="67913-106">Дополнительные сведения см. в разделе [атрибуты](attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="67913-106">For more information, see the [Attributes](attributes.md) topic.</span></span>

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

<span data-ttu-id="67913-107">В следующей процедуре описывается, как использовать API регистрации сертификатов для добавления расширений в \# запрос сертификата PKCS 10.</span><span class="sxs-lookup"><span data-stu-id="67913-107">The following procedure discusses how to use the Certificate Enrollment API to add extensions to a PKCS \#10 certificate request:</span></span>

1.  <span data-ttu-id="67913-108">Получите коллекцию [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) , вызвав свойство [**X509Extension**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_x509extensions) объекта [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) .</span><span class="sxs-lookup"><span data-stu-id="67913-108">Retrieve an [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) collection by calling the [**X509Extension**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_x509extensions) property on the [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) object.</span></span>
2.  <span data-ttu-id="67913-109">Создайте расширение с помощью любого из доступных интерфейсов, производных от интерфейса [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) .</span><span class="sxs-lookup"><span data-stu-id="67913-109">Create an extension by using any of the available interfaces that derive from the [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) interface.</span></span>
3.  <span data-ttu-id="67913-110">Добавьте расширения, созданные на шаге 2, в коллекцию [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) , полученную на шаге 1.</span><span class="sxs-lookup"><span data-stu-id="67913-110">Add the extensions created in step 2 to the [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) collection retrieved in step 1.</span></span>

## <a name="related-topics"></a><span data-ttu-id="67913-111">См. также</span><span class="sxs-lookup"><span data-stu-id="67913-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67913-112">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="67913-112">Attributes</span></span>](attributes.md)
</dt> <dt>

[<span data-ttu-id="67913-113">Архитектура атрибута</span><span class="sxs-lookup"><span data-stu-id="67913-113">Attribute Architecture</span></span>](attribute-architecture.md)
</dt> <dt>

[<span data-ttu-id="67913-114">\#АТРИБУТЫ PKCS 10</span><span class="sxs-lookup"><span data-stu-id="67913-114">PKCS \#10 Attributes</span></span>](pkcs--10-attributes.md)
</dt> <dt>

[<span data-ttu-id="67913-115">Расширения</span><span class="sxs-lookup"><span data-stu-id="67913-115">Extensions</span></span>](extensions.md)
</dt> </dl>

 

 



