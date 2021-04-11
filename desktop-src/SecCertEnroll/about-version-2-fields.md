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
# <a name="version-2-fields"></a>Поля версии 2

Сертификат X.509 версии 2 содержит основные поля, определенные в версии 1, а также следующие поля.

## <a name="issuer-unique-identifier"></a>Уникальный идентификатор поставщика

Содержит уникальное значение, которое может быть использовано для того, чтобы имя ЦС по стандарту X.500 однозначно идентифицировало этот ЦС при последующем многократном использовании различными объектами.

``` syntax
---------------------------------------------------------------------
-- Issuer Unique identifier
---------------------------------------------------------------------
issuerUniqueIdentifier ::= [1] IMPLICIT UniqueIdentifier OPTIONAL

UniqueIdentifier ::= BITSTRING
```

## <a name="subject-unique-identifier"></a>Уникальный идентификатор субъекта

Содержит уникальное значение, которое может быть использовано для того, чтобы имя субъекта по стандарту X.500 однозначно идентифицировало этот субъект при последующем многократном использовании различными объектами.

``` syntax
---------------------------------------------------------------------
-- Issuer Unique identifier
---------------------------------------------------------------------
subjectUniqueIdentifier ::= [2] IMPLICIT UniqueIdentifier OPTIONAL

UniqueIdentifier ::= BITSTRING
```

## <a name="related-topics"></a>См. также

<dl> <dt>

[Основные поля](about-basic-fields.md)
</dt> <dt>

[Расширения версии 3](about-version-3-extensions.md)
</dt> <dt>

[Сертификаты открытого ключа X. 509](about-x-509-public-key-certificates.md)
</dt> </dl>

 

 



