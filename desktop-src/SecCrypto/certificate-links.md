---
description: Функции Цертаддцертификателинктосторе, Цертаддкрллинктосторе и Цертаддктллинктосторе добавляют ссылки на существующие контексты в хранилища сертификатов, а не добавляют копии этих контекстов.
ms.assetid: 482fb11e-eb59-4de2-a2ad-c1960617e64b
title: Ссылки на сертификаты
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2954c52bcc7b2d98ab5ebb8d732abcbc8f0dea81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156291"
---
# <a name="certificate-links"></a><span data-ttu-id="4974c-103">Ссылки на сертификаты</span><span class="sxs-lookup"><span data-stu-id="4974c-103">Certificate Links</span></span>

<span data-ttu-id="4974c-104">Функции [**цертаддцертификателинктосторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatelinktostore), [**цертаддкрллинктосторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcrllinktostore)и [**цертаддктллинктосторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddctllinktostore) добавляют ссылки на существующие контексты в [*хранилища сертификатов*](../secgloss/c-gly.md) , а не добавляют копии этих контекстов.</span><span class="sxs-lookup"><span data-stu-id="4974c-104">The functions [**CertAddCertificateLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatelinktostore), [**CertAddCRLLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcrllinktostore), and [**CertAddCTLLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddctllinktostore) add links to existing contexts into [*certificate stores*](../secgloss/c-gly.md) rather than adding copies of those contexts.</span></span> <span data-ttu-id="4974c-105">При добавлении ссылок на хранилища один и тот же физический [*сертификат*](../secgloss/c-gly.md), [*список отзыва*](../secgloss/c-gly.md)сертификатов или [*список доверия*](../secgloss/c-gly.md) сертификатов будет доступен в нескольких разных магазинах.</span><span class="sxs-lookup"><span data-stu-id="4974c-105">Adding links to stores makes the same physical [*certificate*](../secgloss/c-gly.md), [*CRL*](../secgloss/c-gly.md), or [*CTL*](../secgloss/c-gly.md) available through several different stores.</span></span> <span data-ttu-id="4974c-106">Изменения, внесенные в расширенные свойства [*контекста*](../secgloss/c-gly.md) из хранилища исходного контекста или из хранилища, в котором хранится ссылка на этот контекст, доступны в хранилище, содержащем исходный контекст и во всех других магазинах, которые имеют ссылки на этот контекст.</span><span class="sxs-lookup"><span data-stu-id="4974c-106">Changes made to the extended properties of a [*context*](../secgloss/c-gly.md) from the store of the original context, or from a store where a link to that context is stored, are available in the store that holds the original context and in all other stores that have links to that context.</span></span>

<span data-ttu-id="4974c-107">Пример использования [**цертаддцертификателинктосторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatelinktostore)см. в разделе [Пример программы C: операции с хранилищем сертификатов](example-c-program-certificate-store-operations.md).</span><span class="sxs-lookup"><span data-stu-id="4974c-107">For an example that uses [**CertAddCertificateLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatelinktostore), see [Example C Program: Certificate Store Operations](example-c-program-certificate-store-operations.md).</span></span>

![ссылки на сертификаты](images/mancert1.png)

<span data-ttu-id="4974c-109">Предположим, что сертификаты A. 1, A. 2, A. 3 и A. 4 изначально находятся в хранилище A, а сертификаты B. 1, B. 2, B. 3 и B. 4 изначально находятся в магазине B.</span><span class="sxs-lookup"><span data-stu-id="4974c-109">Assume that certificates A.1, A.2, A.3, and A.4 are originally in store A, and certificates B.1, B.2, B.3, and B.4 are originally in store B.</span></span>

-   <span data-ttu-id="4974c-110">На схеме показана ссылка, добавленная в хранилище B в сертификат A. 2, и ссылка, добавленная в Store A в сертификат B. 2.</span><span class="sxs-lookup"><span data-stu-id="4974c-110">The diagram shows a link added in store B to certificate A.2 and a link added in store A to certificate B.2.</span></span>
-   <span data-ttu-id="4974c-111">Оригинал сертификата A. 2 все еще находится в хранилище A. Исходный объект B. 2 все еще находится в хранилище B.</span><span class="sxs-lookup"><span data-stu-id="4974c-111">The original of certificate A.2 is still in store A. The original of B.2 is still in store B.</span></span>
-   <span data-ttu-id="4974c-112">Любые изменения, внесенные в расширенные свойства сертификата A. 2 или сертификата B. 2 из магазина A или магазина B, будут доступны обоим магазинам.</span><span class="sxs-lookup"><span data-stu-id="4974c-112">Any changes made to the extended properties of certificate A.2 or certificate B.2 from either store A or store B will be available to both stores.</span></span>
-   <span data-ttu-id="4974c-113">Если копия сертификата A. 3 была сделана и сохранена в хранилище B, любые изменения в расширенных свойствах исходного сертификата A. 3, созданного из хранилища A, не будут отображаться в новой копии в хранилище B. Если в расширенные свойства копии сертификата A. 3 в хранилище B были внесены изменения, эти изменения не повлияют на содержимое исходного сертификата A. 3 и не будут видны из хранилища.</span><span class="sxs-lookup"><span data-stu-id="4974c-113">If a copy of certificate A.3 were made and stored in store B, any changes to the extended properties of the original A.3 certificate made from store A would not be visible in the new copy in store B. If changes were made to the extended properties of the copy of certificate A.3 in store B, those changes would not affect the contents of the original A.3 certificate and would not be visible from store A.</span></span>

 

 
