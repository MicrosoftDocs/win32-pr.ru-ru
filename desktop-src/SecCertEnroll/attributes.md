---
description: Атрибуты (API регистрации сертификатов) — атрибуты можно добавить в запрос на сертификат, чтобы предоставить центр сертификации (ЦС) с дополнительными сведениями, которые могут использоваться при создании и выдаче сертификата.
ms.assetid: 6116e61e-3ec5-4992-90ab-e3c7ced291b6
title: Атрибуты (API регистрации сертификатов)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 93414156c7fa6e46fe80995d8d01eadc28796ec2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118432"
---
# <a name="attributes-certificate-enrollment-api"></a><span data-ttu-id="19659-103">Атрибуты (API регистрации сертификатов)</span><span class="sxs-lookup"><span data-stu-id="19659-103">Attributes (Certificate Enrollment API)</span></span>

<span data-ttu-id="19659-104">В запрос на сертификат можно добавить атрибуты, чтобы предоставить центр сертификации (ЦС) с дополнительными сведениями, которые он может использовать при создании и выдаче сертификата.</span><span class="sxs-lookup"><span data-stu-id="19659-104">Attributes can be added to a certificate request to provide a certification authority (CA) with additional information that it can use when creating and issuing a certificate.</span></span> <span data-ttu-id="19659-105">Каждый атрибут представляет собой закодированную в [*distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (Der) [*нотацию абстрактного синтаксиса*](/windows/desktop/SecGloss/a-gly) (ASN. 1), которая содержит идентификатор объекта (OID) и ноль или более значений.</span><span class="sxs-lookup"><span data-stu-id="19659-105">Each attribute is a [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (DER) encoded [*Abstract Syntax Notation One*](/windows/desktop/SecGloss/a-gly) (ASN.1) structure that contains an object identifier (OID) and zero or more values.</span></span> <span data-ttu-id="19659-106">Атрибуты определяются с помощью интерфейсов, входящих в API регистрации сертификатов.</span><span class="sxs-lookup"><span data-stu-id="19659-106">Attributes are defined by using interfaces included with the Certificate Enrollment API.</span></span> <span data-ttu-id="19659-107">Атрибуты более подробно обсуждаются в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="19659-107">The following topics discuss attributes in more detail:</span></span>

-   [<span data-ttu-id="19659-108">Поддерживаемые атрибуты</span><span class="sxs-lookup"><span data-stu-id="19659-108">Supported Attributes</span></span>](supported-attributes.md)
-   [<span data-ttu-id="19659-109">Архитектура атрибута</span><span class="sxs-lookup"><span data-stu-id="19659-109">Attribute Architecture</span></span>](attribute-architecture.md)
-   [<span data-ttu-id="19659-110">\#АТРИБУТЫ PKCS 7</span><span class="sxs-lookup"><span data-stu-id="19659-110">PKCS \#7 Attributes</span></span>](pkcs--7-attributes.md)
-   [<span data-ttu-id="19659-111">\#АТРИБУТЫ PKCS 10</span><span class="sxs-lookup"><span data-stu-id="19659-111">PKCS \#10 Attributes</span></span>](pkcs--10-attributes.md)
-   [<span data-ttu-id="19659-112">Атрибуты CMC</span><span class="sxs-lookup"><span data-stu-id="19659-112">CMC Attributes</span></span>](cmc-attributes.md)

 

 
