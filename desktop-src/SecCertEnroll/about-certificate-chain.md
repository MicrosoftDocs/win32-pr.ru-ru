---
description: Цепочка сертификатов — это иерархическая коллекция сертификатов, которая ведет от конечного пользователя или компьютера к корню доверия, обычно корневому центру сертификации (ЦС) Организации.
ms.assetid: 53701ede-269c-4949-b839-3f2b64cb5510
title: Цепочка сертификатов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e7509adb164c98cf07912af00af0d91c27ab8df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664647"
---
# <a name="certificate-chain"></a><span data-ttu-id="408b1-103">Цепочка сертификатов</span><span class="sxs-lookup"><span data-stu-id="408b1-103">Certificate Chain</span></span>

<span data-ttu-id="408b1-104">Цепочка сертификатов — это иерархическая коллекция сертификатов, которая ведет от конечного пользователя или компьютера к корню доверия, обычно корневому центру сертификации (ЦС) Организации.</span><span class="sxs-lookup"><span data-stu-id="408b1-104">A certificate chain is a hierarchal collection of certificates that leads from the end user or computer back to a root of trust, typically the root certification authority (CA) of an organization.</span></span> <span data-ttu-id="408b1-105">Так как все стороны предположительно доверяют корневому сертификату, сторона может получить доверие в сертификате конечного субъекта, проверив цепочку сертификатов.</span><span class="sxs-lookup"><span data-stu-id="408b1-105">Because all parties presumably trust the root certificate, a party can gain trust in an end-entity certificate by verifying the certificate chain.</span></span> <span data-ttu-id="408b1-106">Проверка обычно требует установки каждого сертификата в цепочке:</span><span class="sxs-lookup"><span data-stu-id="408b1-106">Verification typically requires establishing that each certificate in the chain:</span></span>

-   <span data-ttu-id="408b1-107">Подписывается открытым ключом в предыдущем сертификате.</span><span class="sxs-lookup"><span data-stu-id="408b1-107">Is signed by the public key in the prior certificate.</span></span>
-   <span data-ttu-id="408b1-108">Срок действия не истек.</span><span class="sxs-lookup"><span data-stu-id="408b1-108">Has not expired.</span></span>
-   <span data-ttu-id="408b1-109">Не отозван.</span><span class="sxs-lookup"><span data-stu-id="408b1-109">Has not been revoked.</span></span>
-   <span data-ttu-id="408b1-110">Соответствует политикам, заданным в предыдущих сертификатах.</span><span class="sxs-lookup"><span data-stu-id="408b1-110">Conforms to the policies specified by prior certificates.</span></span>

## <a name="related-topics"></a><span data-ttu-id="408b1-111">См. также</span><span class="sxs-lookup"><span data-stu-id="408b1-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="408b1-112">Иерархия сертификатов</span><span class="sxs-lookup"><span data-stu-id="408b1-112">Certificate Hierarchy</span></span>](about-certificate-hierarchy.md)
</dt> <dt>

[<span data-ttu-id="408b1-113">Перекрестная сертификация</span><span class="sxs-lookup"><span data-stu-id="408b1-113">Cross Certification</span></span>](about-cross-certification.md)
</dt> <dt>

[<span data-ttu-id="408b1-114">Модели доверия</span><span class="sxs-lookup"><span data-stu-id="408b1-114">Trust Models</span></span>](about-trust-models.md)
</dt> </dl>

 

 



