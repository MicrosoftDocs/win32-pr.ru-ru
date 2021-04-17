---
description: Для шифрования и расшифровки содержимого шифрование с открытым ключом использует пару из открытого и закрытого ключей.
ms.assetid: a85ec2bc-a413-41a6-b3d2-5fa81a9e7bb6
title: Сертификаты открытого ключа X. 509
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1acd602e9b47cb7825f6d75df0fb74399b914db3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104567720"
---
# <a name="x509-public-key-certificates"></a>Сертификаты открытого ключа X. 509

Для шифрования и расшифровки содержимого шифрование с открытым ключом использует пару из открытого и закрытого ключей. Ключи математически связаны, и содержимое, зашифрованное с помощью одного из ключей, можно расшифровать только с помощью другого. Закрытый ключ сохраняется в секрете. Открытый ключ обычно внедряется в двоичный сертификат, и сертификат публикуется в базе данных, к которой могут обращаться все полномочные пользователи.

Стандарт инфраструктуры открытых ключей X. 509 (PKI) определяет требования к надежным сертификатам открытого ключа. Сертификат — это подписанная структура данных, которая связывает открытый ключ с лицом, компьютером или организацией. Сертификаты выдаются [*центрами сертификации*](/windows/desktop/SecGloss/c-gly) (CAS). Все, кто является субъектом для защиты обмена данными, которые используют открытый ключ, используют центр сертификации для адекватной проверки подлинности лиц, систем или сущностей, на которые он выдает сертификаты. Уровень проверки обычно зависит от уровня безопасности, необходимого для транзакции. Если ЦС может соответствующим образом проверить удостоверение инициатора запроса, он подписывает (шифрует), кодирует и выдает сертификат.

Сертификат — это подписанная структура данных, которая связывает открытый ключ с сущностью. В следующем примере показана синтаксическая [*нотация*](/windows/desktop/SecGloss/a-gly) с синтаксисом (ASN. 1) для сертификата версии 3 [*X. 509*](/windows/desktop/SecGloss/x-gly) .

``` syntax
-- X.509 signed certificate 

SignedContent ::= SEQUENCE 
{
  certificate         CertificateToBeSigned,
  algorithm           Object Identifier,
  signature           BITSTRING
}
 
-- X.509 certificate to be signed

CertificateToBeSigned ::= SEQUENCE 
{
  version                 [0] CertificateVersion DEFAULT v1,
  serialNumber            CertificateSerialNumber,
  signature               AlgorithmIdentifier,
  issuer                  Name
  validity                Validity,
  subject                 Name
  subjectPublicKeyInfo    SubjectPublicKeyInfo,
  issuerUniqueIdentifier  [1] IMPLICIT UniqueIdentifier OPTIONAL,
  subjectUniqueIdentifier [2] IMPLICIT UniqueIdentifier OPTIONAL,
  extensions              [3] Extensions OPTIONAL
}
```

С момента своего порождения в 1998 три версии стандарта сертификата открытого ключа X. 509 были изменены. Как показано на следующем рисунке, каждая последующая версия структуры данных сохранила поля, существовавшие в предыдущих версиях, и добавила еще больше.

![сертификаты x. 509 версии 1, 2 и 3](images/x509certificateversions.png)

В следующих разделах более подробно рассматриваются доступные поля:

-   [Основные поля](about-basic-fields.md)
-   [Поля версии 2](about-version-2-fields.md)
-   [Расширения версии 3](about-version-3-extensions.md)

## <a name="related-topics"></a>См. также

<dl> <dt>

[Инфраструктура открытых ключей](public-key-infrastructure.md)
</dt> </dl>

 

 
