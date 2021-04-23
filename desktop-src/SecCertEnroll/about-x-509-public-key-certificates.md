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
# <a name="x509-public-key-certificates"></a><span data-ttu-id="667fc-103">Сертификаты открытого ключа X. 509</span><span class="sxs-lookup"><span data-stu-id="667fc-103">X.509 Public Key Certificates</span></span>

<span data-ttu-id="667fc-104">Для шифрования и расшифровки содержимого шифрование с открытым ключом использует пару из открытого и закрытого ключей.</span><span class="sxs-lookup"><span data-stu-id="667fc-104">Public key cryptography relies on a public and private key pair to encrypt and decrypt content.</span></span> <span data-ttu-id="667fc-105">Ключи математически связаны, и содержимое, зашифрованное с помощью одного из ключей, можно расшифровать только с помощью другого.</span><span class="sxs-lookup"><span data-stu-id="667fc-105">The keys are mathematically related, and content encrypted by using one of the keys can only be decrypted by using the other.</span></span> <span data-ttu-id="667fc-106">Закрытый ключ сохраняется в секрете.</span><span class="sxs-lookup"><span data-stu-id="667fc-106">The private key is kept secret.</span></span> <span data-ttu-id="667fc-107">Открытый ключ обычно внедряется в двоичный сертификат, и сертификат публикуется в базе данных, к которой могут обращаться все полномочные пользователи.</span><span class="sxs-lookup"><span data-stu-id="667fc-107">The public key is typically embedded in a binary certificate, and the certificate is published to a database that can be reached by all authorized users.</span></span>

<span data-ttu-id="667fc-108">Стандарт инфраструктуры открытых ключей X. 509 (PKI) определяет требования к надежным сертификатам открытого ключа.</span><span class="sxs-lookup"><span data-stu-id="667fc-108">The X.509 public key infrastructure (PKI) standard identifies the requirements for robust public key certificates.</span></span> <span data-ttu-id="667fc-109">Сертификат — это подписанная структура данных, которая связывает открытый ключ с лицом, компьютером или организацией.</span><span class="sxs-lookup"><span data-stu-id="667fc-109">A certificate is a signed data structure that binds a public key to a person, computer, or organization.</span></span> <span data-ttu-id="667fc-110">Сертификаты выдаются [*центрами сертификации*](/windows/desktop/SecGloss/c-gly) (CAS).</span><span class="sxs-lookup"><span data-stu-id="667fc-110">Certificates are issued by [*certification authorities*](/windows/desktop/SecGloss/c-gly) (CAs).</span></span> <span data-ttu-id="667fc-111">Все, кто является субъектом для защиты обмена данными, которые используют открытый ключ, используют центр сертификации для адекватной проверки подлинности лиц, систем или сущностей, на которые он выдает сертификаты.</span><span class="sxs-lookup"><span data-stu-id="667fc-111">All who are party to secure communications that make use of a public key rely on the CA to adequately verify the identities of the individuals, systems, or entities to which it issues certificates.</span></span> <span data-ttu-id="667fc-112">Уровень проверки обычно зависит от уровня безопасности, необходимого для транзакции.</span><span class="sxs-lookup"><span data-stu-id="667fc-112">The level of verification typically depends on the level of security required for the transaction.</span></span> <span data-ttu-id="667fc-113">Если ЦС может соответствующим образом проверить удостоверение инициатора запроса, он подписывает (шифрует), кодирует и выдает сертификат.</span><span class="sxs-lookup"><span data-stu-id="667fc-113">If the CA can suitably verify the identity of the requester, it signs (encrypts), encodes, and issues the certificate.</span></span>

<span data-ttu-id="667fc-114">Сертификат — это подписанная структура данных, которая связывает открытый ключ с сущностью.</span><span class="sxs-lookup"><span data-stu-id="667fc-114">A certificate is a signed data structure that binds a public key to an entity.</span></span> <span data-ttu-id="667fc-115">В следующем примере показана синтаксическая [*нотация*](/windows/desktop/SecGloss/a-gly) с синтаксисом (ASN. 1) для сертификата версии 3 [*X. 509*](/windows/desktop/SecGloss/x-gly) .</span><span class="sxs-lookup"><span data-stu-id="667fc-115">The [*Abstract Syntax Notation One*](/windows/desktop/SecGloss/a-gly) (ASN.1) syntax for the version 3 [*X.509*](/windows/desktop/SecGloss/x-gly) certificate is shown in the following example.</span></span>

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

<span data-ttu-id="667fc-116">С момента своего порождения в 1998 три версии стандарта сертификата открытого ключа X. 509 были изменены.</span><span class="sxs-lookup"><span data-stu-id="667fc-116">Since its inception in 1998, three versions of the X.509 public key certificate standard have evolved.</span></span> <span data-ttu-id="667fc-117">Как показано на следующем рисунке, каждая последующая версия структуры данных сохранила поля, существовавшие в предыдущих версиях, и добавила еще больше.</span><span class="sxs-lookup"><span data-stu-id="667fc-117">As shown by the following illustration, each successive version of the data structure has retained the fields that existed in the previous versions and added more.</span></span>

![сертификаты x. 509 версии 1, 2 и 3](images/x509certificateversions.png)

<span data-ttu-id="667fc-119">В следующих разделах более подробно рассматриваются доступные поля:</span><span class="sxs-lookup"><span data-stu-id="667fc-119">The following topics discuss the available fields in more detail:</span></span>

-   [<span data-ttu-id="667fc-120">Основные поля</span><span class="sxs-lookup"><span data-stu-id="667fc-120">Basic Fields</span></span>](about-basic-fields.md)
-   [<span data-ttu-id="667fc-121">Поля версии 2</span><span class="sxs-lookup"><span data-stu-id="667fc-121">Version 2 Fields</span></span>](about-version-2-fields.md)
-   [<span data-ttu-id="667fc-122">Расширения версии 3</span><span class="sxs-lookup"><span data-stu-id="667fc-122">Version 3 Extensions</span></span>](about-version-3-extensions.md)

## <a name="related-topics"></a><span data-ttu-id="667fc-123">См. также</span><span class="sxs-lookup"><span data-stu-id="667fc-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="667fc-124">Инфраструктура открытых ключей</span><span class="sxs-lookup"><span data-stu-id="667fc-124">Public Key Infrastructure</span></span>](public-key-infrastructure.md)
</dt> </dl>

 

 
