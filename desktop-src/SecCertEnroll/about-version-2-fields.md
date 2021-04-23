---
description: Сертификат X.509 версии 2 содержит основные поля, определенные в версии 1, а также следующие поля.
ms.assetid: 533d43d7-0c49-4461-8ba8-368c103feb4f
title: Поля версии 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48e66d66d9c5d92f7c3a0436ae828b60d285edce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262852"
---
# <a name="version-2-fields"></a><span data-ttu-id="4e21c-103">Поля версии 2</span><span class="sxs-lookup"><span data-stu-id="4e21c-103">Version 2 Fields</span></span>

<span data-ttu-id="4e21c-104">Сертификат X.509 версии 2 содержит основные поля, определенные в версии 1, а также следующие поля.</span><span class="sxs-lookup"><span data-stu-id="4e21c-104">An X.509 version 2 certificate contains the basic fields defined in version 1 and adds the following fields.</span></span>

## <a name="issuer-unique-identifier"></a><span data-ttu-id="4e21c-105">Уникальный идентификатор поставщика</span><span class="sxs-lookup"><span data-stu-id="4e21c-105">Issuer Unique Identifier</span></span>

<span data-ttu-id="4e21c-106">Содержит уникальное значение, которое может быть использовано для того, чтобы имя ЦС по стандарту X.500 однозначно идентифицировало этот ЦС при последующем многократном использовании различными объектами.</span><span class="sxs-lookup"><span data-stu-id="4e21c-106">Contains a unique value that can be used to make the X.500 name of the CA unambiguous when reused by different entities over time.</span></span>

``` syntax
---------------------------------------------------------------------
-- Issuer Unique identifier
---------------------------------------------------------------------
issuerUniqueIdentifier ::= [1] IMPLICIT UniqueIdentifier OPTIONAL

UniqueIdentifier ::= BITSTRING
```

## <a name="subject-unique-identifier"></a><span data-ttu-id="4e21c-107">Уникальный идентификатор субъекта</span><span class="sxs-lookup"><span data-stu-id="4e21c-107">Subject Unique Identifier</span></span>

<span data-ttu-id="4e21c-108">Содержит уникальное значение, которое может быть использовано для того, чтобы имя субъекта по стандарту X.500 однозначно идентифицировало этот субъект при последующем многократном использовании различными объектами.</span><span class="sxs-lookup"><span data-stu-id="4e21c-108">Contains a unique value that can be used to make the X.500 name of the certificate subject unambiguous when reused by different entities over time.</span></span>

``` syntax
---------------------------------------------------------------------
-- Issuer Unique identifier
---------------------------------------------------------------------
subjectUniqueIdentifier ::= [2] IMPLICIT UniqueIdentifier OPTIONAL

UniqueIdentifier ::= BITSTRING
```

## <a name="related-topics"></a><span data-ttu-id="4e21c-109">См. также</span><span class="sxs-lookup"><span data-stu-id="4e21c-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e21c-110">Основные поля</span><span class="sxs-lookup"><span data-stu-id="4e21c-110">Basic Fields</span></span>](about-basic-fields.md)
</dt> <dt>

[<span data-ttu-id="4e21c-111">Расширения версии 3</span><span class="sxs-lookup"><span data-stu-id="4e21c-111">Version 3 Extensions</span></span>](about-version-3-extensions.md)
</dt> <dt>

[<span data-ttu-id="4e21c-112">Сертификаты открытого ключа X. 509</span><span class="sxs-lookup"><span data-stu-id="4e21c-112">X.509 Public Key Certificates</span></span>](about-x-509-public-key-certificates.md)
</dt> </dl>

 

 



