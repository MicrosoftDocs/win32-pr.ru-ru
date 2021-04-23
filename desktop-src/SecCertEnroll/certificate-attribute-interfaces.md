---
description: Для создания атрибутов сертификата можно использовать следующие интерфейсы.
ms.assetid: 3701f9b2-0857-45f0-b3ed-4f1b3db4d6d8
title: Интерфейсы атрибутов сертификата
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 930f427ae6333084c8a180e5d227e4c24daa5426
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647175"
---
# <a name="certificate-attribute-interfaces"></a><span data-ttu-id="b3df2-103">Интерфейсы атрибутов сертификата</span><span class="sxs-lookup"><span data-stu-id="b3df2-103">Certificate Attribute Interfaces</span></span>

<span data-ttu-id="b3df2-104">Для создания атрибутов сертификата можно использовать следующие интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="b3df2-104">The following interfaces can be used to create certificate attributes.</span></span>



| <span data-ttu-id="b3df2-105">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="b3df2-105">Interface</span></span>                                                                    | <span data-ttu-id="b3df2-106">Описание</span><span class="sxs-lookup"><span data-stu-id="b3df2-106">Description</span></span>                                                                                                                                 |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b3df2-107">**икриптаттрибуте**</span><span class="sxs-lookup"><span data-stu-id="b3df2-107">**ICryptAttribute**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute)                                   | <span data-ttu-id="b3df2-108">Представляет криптографический атрибут в запросе на сертификат.</span><span class="sxs-lookup"><span data-stu-id="b3df2-108">Represents a cryptographic attribute in a certificate request.</span></span>                                                                              |
| [<span data-ttu-id="b3df2-109">**икриптаттрибутес**</span><span class="sxs-lookup"><span data-stu-id="b3df2-109">**ICryptAttributes**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)                                 | <span data-ttu-id="b3df2-110">Управляет коллекцией объектов [**икриптаттрибуте**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) .</span><span class="sxs-lookup"><span data-stu-id="b3df2-110">Manages a collection of [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) objects.</span></span>                                                                 |
| [<span data-ttu-id="b3df2-111">**IX509Attribute**</span><span class="sxs-lookup"><span data-stu-id="b3df2-111">**IX509Attribute**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute)                                     | <span data-ttu-id="b3df2-112">Представляет атрибут в \# запросе сертификата PKCS 7, PKCS \# 10 или CMC.</span><span class="sxs-lookup"><span data-stu-id="b3df2-112">Represents an attribute in a PKCS \#7, PKCS \#10, or CMC certificate request.</span></span>                                                               |
| [<span data-ttu-id="b3df2-113">**IX509AttributeClientId**</span><span class="sxs-lookup"><span data-stu-id="b3df2-113">**IX509AttributeClientId**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid)                     | <span data-ttu-id="b3df2-114">Представляет атрибут, который может использоваться для распознавания клиента, создавшего запрос на сертификат.</span><span class="sxs-lookup"><span data-stu-id="b3df2-114">Represents an attribute that can be used to identify the client that generated a certificate request.</span></span>                                       |
| [<span data-ttu-id="b3df2-115">**IX509AttributeExtensions**</span><span class="sxs-lookup"><span data-stu-id="b3df2-115">**IX509AttributeExtensions**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions)                 | <span data-ttu-id="b3df2-116">Представляет расширения сертификата в запросе на сертификат.</span><span class="sxs-lookup"><span data-stu-id="b3df2-116">Represents the certificate extensions in a certificate request.</span></span>                                                                             |
| [<span data-ttu-id="b3df2-117">**IX509AttributeArchiveKey**</span><span class="sxs-lookup"><span data-stu-id="b3df2-117">**IX509AttributeArchiveKey**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekey)                 | <span data-ttu-id="b3df2-118">Представляет атрибут, содержащий зашифрованный закрытый ключ, заархивированный центром сертификации.</span><span class="sxs-lookup"><span data-stu-id="b3df2-118">Represents an attribute that contains an encrypted private key to be archived by a certification authority.</span></span>                                 |
| [<span data-ttu-id="b3df2-119">**IX509AttributeArchiveKeyHash**</span><span class="sxs-lookup"><span data-stu-id="b3df2-119">**IX509AttributeArchiveKeyHash**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekeyhash)         | <span data-ttu-id="b3df2-120">Представляет атрибут, содержащий хэш SHA-1 зашифрованного закрытого ключа, который должен быть архивирован центром сертификации.</span><span class="sxs-lookup"><span data-stu-id="b3df2-120">Represents an attribute that contains a SHA-1 hash of the encrypted private key to be archived by a certification authority.</span></span>                |
| [<span data-ttu-id="b3df2-121">**IX509AttributeCspProvider**</span><span class="sxs-lookup"><span data-stu-id="b3df2-121">**IX509AttributeCspProvider**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributecspprovider)               | <span data-ttu-id="b3df2-122">Представляет атрибут, определяющий поставщик служб шифрования, используемый сущностью, запрашивающей сертификат.</span><span class="sxs-lookup"><span data-stu-id="b3df2-122">Represents an attribute that identifies the cryptographic provider used by the entity requesting the certificate.</span></span>                           |
| [<span data-ttu-id="b3df2-123">**IX509AttributeOSVersion**</span><span class="sxs-lookup"><span data-stu-id="b3df2-123">**IX509AttributeOSVersion**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeosversion)                   | <span data-ttu-id="b3df2-124">Представляет атрибут, содержащий сведения о версии клиентской операционной системы, на которой был создан запрос сертификата.</span><span class="sxs-lookup"><span data-stu-id="b3df2-124">Represents an attribute that contains version information about the client operating system on which the certificate request was generated.</span></span> |
| [<span data-ttu-id="b3df2-125">**IX509AttributeRenewalCertificate**</span><span class="sxs-lookup"><span data-stu-id="b3df2-125">**IX509AttributeRenewalCertificate**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributerenewalcertificate) | <span data-ttu-id="b3df2-126">Представляет атрибут, который содержит обновляемый сертификат.</span><span class="sxs-lookup"><span data-stu-id="b3df2-126">Represents an attribute that contains the certificate being renewed.</span></span>                                                                        |
| [<span data-ttu-id="b3df2-127">**IX509Attributes**</span><span class="sxs-lookup"><span data-stu-id="b3df2-127">**IX509Attributes**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes)                                   | <span data-ttu-id="b3df2-128">Управляет коллекцией объектов [**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute) .</span><span class="sxs-lookup"><span data-stu-id="b3df2-128">Manages a collection of [**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute) objects.</span></span>                                                                   |
| [<span data-ttu-id="b3df2-129">**IX509NameValuePair**</span><span class="sxs-lookup"><span data-stu-id="b3df2-129">**IX509NameValuePair**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair)                             | <span data-ttu-id="b3df2-130">Представляет пару "имя-значение".</span><span class="sxs-lookup"><span data-stu-id="b3df2-130">Represents a generic name-value pair.</span></span>                                                                                                       |
| [<span data-ttu-id="b3df2-131">**IX509NameValuePairs**</span><span class="sxs-lookup"><span data-stu-id="b3df2-131">**IX509NameValuePairs**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs)                           | <span data-ttu-id="b3df2-132">Управляет коллекцией объектов [**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) .</span><span class="sxs-lookup"><span data-stu-id="b3df2-132">Manages a collection of [**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) objects.</span></span>                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="b3df2-133">См. также</span><span class="sxs-lookup"><span data-stu-id="b3df2-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3df2-134">Интерфейсы Цертенролл</span><span class="sxs-lookup"><span data-stu-id="b3df2-134">CertEnroll Interfaces</span></span>](certenroll-interfaces.md)
</dt> </dl>

 

 



