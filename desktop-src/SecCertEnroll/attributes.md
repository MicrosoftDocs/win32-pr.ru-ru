---
description: В запрос на сертификат можно добавить атрибуты, чтобы предоставить центр сертификации (ЦС) с дополнительными сведениями, которые он может использовать при создании и выдаче сертификата.
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
ms.openlocfilehash: e7a00c30be8bacf5593d78e21fb420c8a899dc7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811261"
---
# <a name="attributes-certificate-enrollment-api"></a><span data-ttu-id="a7791-103">Атрибуты (API регистрации сертификатов)</span><span class="sxs-lookup"><span data-stu-id="a7791-103">Attributes (Certificate Enrollment API)</span></span>

<span data-ttu-id="a7791-104">В запрос на сертификат можно добавить атрибуты, чтобы предоставить центр сертификации (ЦС) с дополнительными сведениями, которые он может использовать при создании и выдаче сертификата.</span><span class="sxs-lookup"><span data-stu-id="a7791-104">Attributes can be added to a certificate request to provide a certification authority (CA) with additional information that it can use when creating and issuing a certificate.</span></span> <span data-ttu-id="a7791-105">Каждый атрибут представляет собой закодированную в [*distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (Der) [*нотацию абстрактного синтаксиса*](/windows/desktop/SecGloss/a-gly) (ASN. 1), которая содержит идентификатор объекта (OID) и ноль или более значений.</span><span class="sxs-lookup"><span data-stu-id="a7791-105">Each attribute is a [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (DER) encoded [*Abstract Syntax Notation One*](/windows/desktop/SecGloss/a-gly) (ASN.1) structure that contains an object identifier (OID) and zero or more values.</span></span> <span data-ttu-id="a7791-106">Атрибуты определяются с помощью интерфейсов, входящих в API регистрации сертификатов.</span><span class="sxs-lookup"><span data-stu-id="a7791-106">Attributes are defined by using interfaces included with the Certificate Enrollment API.</span></span> <span data-ttu-id="a7791-107">Атрибуты более подробно обсуждаются в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="a7791-107">The following topics discuss attributes in more detail:</span></span>

-   [<span data-ttu-id="a7791-108">Поддерживаемые атрибуты</span><span class="sxs-lookup"><span data-stu-id="a7791-108">Supported Attributes</span></span>](supported-attributes.md)
-   [<span data-ttu-id="a7791-109">Архитектура атрибута</span><span class="sxs-lookup"><span data-stu-id="a7791-109">Attribute Architecture</span></span>](attribute-architecture.md)
-   [<span data-ttu-id="a7791-110">\#АТРИБУТЫ PKCS 7</span><span class="sxs-lookup"><span data-stu-id="a7791-110">PKCS \#7 Attributes</span></span>](pkcs--7-attributes.md)
-   [<span data-ttu-id="a7791-111">\#АТРИБУТЫ PKCS 10</span><span class="sxs-lookup"><span data-stu-id="a7791-111">PKCS \#10 Attributes</span></span>](pkcs--10-attributes.md)
-   [<span data-ttu-id="a7791-112">Атрибуты CMC</span><span class="sxs-lookup"><span data-stu-id="a7791-112">CMC Attributes</span></span>](cmc-attributes.md)

 

 
