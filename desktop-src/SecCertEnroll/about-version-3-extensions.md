---
description: Сертификат X.509 версии 3 содержит основные поля, определенные в версии 1 и в версии 2, а также следующие расширения сертификата. В следующем примере показан синтаксис ASN. 1 расширений сертификата.
ms.assetid: ca8df7a4-caa4-4fe7-81a8-8fce372454f4
title: Расширения версии 3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee23ce35ba7031a1a9f7a2c9caa79fd955ccbe2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264478"
---
# <a name="version-3-extensions"></a><span data-ttu-id="21fea-104">Расширения версии 3</span><span class="sxs-lookup"><span data-stu-id="21fea-104">Version 3 Extensions</span></span>

<span data-ttu-id="21fea-105">Сертификат X.509 версии 3 содержит основные поля, определенные в версии 1 и в версии 2, а также следующие расширения сертификата.</span><span class="sxs-lookup"><span data-stu-id="21fea-105">An X.509 version 3 certificate contains the fields defined in version 1 and version 2 and adds certificate extensions.</span></span> <span data-ttu-id="21fea-106">В следующем примере показан синтаксис ASN. 1 расширений сертификата.</span><span class="sxs-lookup"><span data-stu-id="21fea-106">The ASN.1 syntax of certificate extensions is shown in the following example.</span></span>

``` syntax
---------------------------------------------------------------------
-- Extensions (beginning with version 3).
---------------------------------------------------------------------
Extensions ::= SEQUENCE OF Extension

Extension ::= SEQUENCE 
{
  Id                  OBJECT IDENTIFIER,
  critical            BOOLEAN DEFAULT FALSE,
  extnValue           OCTET STRING
}
```

<span data-ttu-id="21fea-107">В следующей таблице перечислены расширения Standard версии 3 и их идентификаторы объектов (OID).</span><span class="sxs-lookup"><span data-stu-id="21fea-107">The standard version 3 extensions and their object identifiers (OIDs) are listed in the following table.</span></span> <span data-ttu-id="21fea-108">Корпорация Майкрософт поддерживает их и включает дополнительные пользовательские расширения.</span><span class="sxs-lookup"><span data-stu-id="21fea-108">Microsoft supports these and includes additional custom extensions.</span></span> <span data-ttu-id="21fea-109">Дополнительные сведения см. в разделе [Extensions](extensions.md).</span><span class="sxs-lookup"><span data-stu-id="21fea-109">For more information, see [Extensions](extensions.md).</span></span>

| <span data-ttu-id="21fea-110">Расширение</span><span class="sxs-lookup"><span data-stu-id="21fea-110">Extension</span></span>                                         | <span data-ttu-id="21fea-111">Описание</span><span class="sxs-lookup"><span data-stu-id="21fea-111">Description</span></span>                                                                                                                                                                                              |
|---------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21fea-112">Идентификатор ключа центра (2.5.29.19)</span><span class="sxs-lookup"><span data-stu-id="21fea-112">Authority Key Identifier(2.5.29.19)</span></span><br/>    | <span data-ttu-id="21fea-113">Идентифицирует открытый ключ центра сертификатов (ЦС), соответствующий закрытому ключу ЦС, который используется для подписания данного сертификата.</span><span class="sxs-lookup"><span data-stu-id="21fea-113">Identifies the certification authority (CA) public key that corresponds to the CA private key used to sign the certificate.</span></span>                                                                              |
| <span data-ttu-id="21fea-114">Базовые ограничения (2.5.29.35)</span><span class="sxs-lookup"><span data-stu-id="21fea-114">Basic Constraints(2.5.29.35)</span></span><br/>           | <span data-ttu-id="21fea-115">Определяет, может ли объект использоваться в качестве ЦС, и, если может, номера подчиненных ЦС, которые могут присутствовать в нисходящей цепочке сертификатов.</span><span class="sxs-lookup"><span data-stu-id="21fea-115">Specifies whether the entity can be used as a CA and, if so, the number of subordinate CAs that can exist beneath it in the certificate chain.</span></span>                                                           |
| <span data-ttu-id="21fea-116">Политики сертификатов (2.5.29.32)</span><span class="sxs-lookup"><span data-stu-id="21fea-116">Certificate Policies(2.5.29.32)</span></span><br/>        | <span data-ttu-id="21fea-117">Определяет политики, регулирующие выдачу сертификата, и возможные цели его использования.</span><span class="sxs-lookup"><span data-stu-id="21fea-117">Specifies the policies under which the certificate has been issued and the purposes for which it can be used.</span></span>                                                                                            |
| <span data-ttu-id="21fea-118">Точки распространения списков отзыва сертификатов (2.5.29.31)</span><span class="sxs-lookup"><span data-stu-id="21fea-118">CRL Distribution Points(2.5.29.31)</span></span><br/>     | <span data-ttu-id="21fea-119">Содержит URI базового [*списка отзыва сертификатов*](/windows/desktop/SecGloss/c-gly) (CRL).</span><span class="sxs-lookup"><span data-stu-id="21fea-119">Contains the URI of the base [*certificate revocation list*](/windows/desktop/SecGloss/c-gly) (CRL).</span></span>                                  |
| <span data-ttu-id="21fea-120">Расширенное использование ключа (2.5.29.46)</span><span class="sxs-lookup"><span data-stu-id="21fea-120">Enhanced Key Usage(2.5.29.46)</span></span><br/>          | <span data-ttu-id="21fea-121">Указывает механизм использования открытого ключа, содержащегося в данном сертификате.</span><span class="sxs-lookup"><span data-stu-id="21fea-121">Specifies the manner in which the public key contained in the certificate can be used.</span></span>                                                                                                                   |
| <span data-ttu-id="21fea-122">Альтернативное имя поставщика (2.5.29.8)</span><span class="sxs-lookup"><span data-stu-id="21fea-122">Issuer Alternative Name(2.5.29.8)</span></span><br/>      | <span data-ttu-id="21fea-123">Определяет одну (или более одной) дополнительную форму имени для поставщика запроса сертификата.</span><span class="sxs-lookup"><span data-stu-id="21fea-123">Specifies one or more alternative name forms for the issuer of the certificate request.</span></span>                                                                                                                  |
| <span data-ttu-id="21fea-124">Использование ключа (2.5.29.15)</span><span class="sxs-lookup"><span data-stu-id="21fea-124">Key Usage(2.5.29.15)</span></span><br/>                   | <span data-ttu-id="21fea-125">Определяет ограничения для операций, которые могут выполняться с использованием открытого ключа, содержащегося в данном сертификате.</span><span class="sxs-lookup"><span data-stu-id="21fea-125">Specifies restrictions on the operations that can be performed by the public key contained in the certificate.</span></span>                                                                                           |
| <span data-ttu-id="21fea-126">Ограничения имен (2.5.29.30)</span><span class="sxs-lookup"><span data-stu-id="21fea-126">Name Constraints(2.5.29.30)</span></span><br/>            | <span data-ttu-id="21fea-127">Определяет пространство имен, в котором должны быть размещены все имена субъектов в иерархии сертификата. </span><span class="sxs-lookup"><span data-stu-id="21fea-127">Specifies the namespace within which all subject names in a certificate hierarchy must be located.</span></span> <span data-ttu-id="21fea-128">Это расширение используется только в сертификате ЦС.</span><span class="sxs-lookup"><span data-stu-id="21fea-128">The extension is used only in a CA certificate.</span></span>                                                       |
| <span data-ttu-id="21fea-129">Ограничения политики (2.5.29.36)</span><span class="sxs-lookup"><span data-stu-id="21fea-129">Policy Constraints(2.5.29.36)</span></span><br/>          | <span data-ttu-id="21fea-130">Ограничивает проверку пути при помощи запрещения сопоставлений политики или требования, чтобы каждый сертификат в данной иерархии содержал допустимый идентификатор политики.</span><span class="sxs-lookup"><span data-stu-id="21fea-130">Constrains path validation by prohibiting policy mapping or by requiring that each certificate in the hierarchy contain an acceptable policy identifier.</span></span> <span data-ttu-id="21fea-131">Это расширение используется только в сертификате ЦС.</span><span class="sxs-lookup"><span data-stu-id="21fea-131">The extension is used only in a CA certificate.</span></span> |
| <span data-ttu-id="21fea-132">Сопоставления политик (2.5.29.33)</span><span class="sxs-lookup"><span data-stu-id="21fea-132">Policy Mappings(2.5.29.33)</span></span><br/>             | <span data-ttu-id="21fea-133">Указывает, какие политики в подчиненном ЦС соответствуют политикам в выдающем ЦС.</span><span class="sxs-lookup"><span data-stu-id="21fea-133">Specifies the policies in a subordinate CA that correspond to policies in the issuing CA.</span></span>                                                                                                                |
| <span data-ttu-id="21fea-134">Период использования закрытого ключа (2.5.29.16)</span><span class="sxs-lookup"><span data-stu-id="21fea-134">Private Key Usage Period(2.5.29.16)</span></span><br/>    | <span data-ttu-id="21fea-135">Указывает срок действия закрытого ключа, отличающийся от срока действия сертификата, с которым связан этот закрытый ключ.</span><span class="sxs-lookup"><span data-stu-id="21fea-135">Specifies a different validity period for the private key than for the certificate with which the private key is associated.</span></span>                                                                             |
| <span data-ttu-id="21fea-136">Альтернативное имя субъекта (2.5.29.17)</span><span class="sxs-lookup"><span data-stu-id="21fea-136">Subject Alternative Name(2.5.29.17)</span></span><br/>    | <span data-ttu-id="21fea-137">Определяет одну (или более одной) дополнительную форму имени для субъекта запроса сертификата.</span><span class="sxs-lookup"><span data-stu-id="21fea-137">Specifies one or more alternative name forms for the subject of the certificate request.</span></span> <span data-ttu-id="21fea-138">Примеры дополнительных форм могут включать адреса электронной почты, DNS-имена, IP-адреса и URI.</span><span class="sxs-lookup"><span data-stu-id="21fea-138">Example alternative forms include email addresses, DNS names, IP addresses, and URIs.</span></span>                           |
| <span data-ttu-id="21fea-139">Атрибуты каталога субъекта (2.5.29.9)</span><span class="sxs-lookup"><span data-stu-id="21fea-139">Subject Directory Attributes(2.5.29.9)</span></span><br/> | <span data-ttu-id="21fea-140">Сообщает атрибуты идентификации, например национальную принадлежность субъекта сертификата.</span><span class="sxs-lookup"><span data-stu-id="21fea-140">Conveys identification attributes such as the nationality of the certificate subject.</span></span> <span data-ttu-id="21fea-141">Значением расширения является последовательность пар значений кодов объекта (OID)</span><span class="sxs-lookup"><span data-stu-id="21fea-141">The extension value is a sequence of OID-value pairs.</span></span>                                                              |
| <span data-ttu-id="21fea-142">Идентификатор ключа субъекта (2.5.29.14)</span><span class="sxs-lookup"><span data-stu-id="21fea-142">Subject Key Identifier(2.5.29.14)</span></span><br/>      | <span data-ttu-id="21fea-143">Служит для разделения нескольких открытых ключей, держателем которых является субъект сертификата.</span><span class="sxs-lookup"><span data-stu-id="21fea-143">Differentiates between multiple public keys held by the certificate subject.</span></span> <span data-ttu-id="21fea-144">Значением расширения обычно является хэш SHA-1 ключа.</span><span class="sxs-lookup"><span data-stu-id="21fea-144">The extension value is typically a SHA-1 hash of the key.</span></span>                                                                   |



 

## <a name="related-topics"></a><span data-ttu-id="21fea-145">См. также</span><span class="sxs-lookup"><span data-stu-id="21fea-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="21fea-146">Основные поля</span><span class="sxs-lookup"><span data-stu-id="21fea-146">Basic Fields</span></span>](about-basic-fields.md)
</dt> <dt>

[<span data-ttu-id="21fea-147">Поля версии 2</span><span class="sxs-lookup"><span data-stu-id="21fea-147">Version 2 Fields</span></span>](about-version-2-fields.md)
</dt> <dt>

[<span data-ttu-id="21fea-148">Сертификаты открытого ключа X. 509</span><span class="sxs-lookup"><span data-stu-id="21fea-148">X.509 Public Key Certificates</span></span>](about-x-509-public-key-certificates.md)
</dt> </dl>

 

