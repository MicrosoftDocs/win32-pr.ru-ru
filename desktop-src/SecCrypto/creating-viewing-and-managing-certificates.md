---
description: Сертификаты имеют связанные свойства, такие как отображаемое имя, описание и разрешенные варианты использования, которые можно просматривать и изменять.
ms.assetid: 23faaa03-af3e-4497-8607-4e34f8889368
title: Создание, просмотр и управление сертификатами
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2136f8cd3ea3af1aab95b3c9c89ddd5787b4cefc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662325"
---
# <a name="creating-viewing-and-managing-certificates"></a><span data-ttu-id="5cd78-103">Создание, просмотр и управление сертификатами</span><span class="sxs-lookup"><span data-stu-id="5cd78-103">Creating, Viewing, and Managing Certificates</span></span>

<span data-ttu-id="5cd78-104">[*Сертификаты*](../secgloss/c-gly.md) являются структурами только для чтения.</span><span class="sxs-lookup"><span data-stu-id="5cd78-104">[*Certificates*](../secgloss/c-gly.md) are read-only structures.</span></span> <span data-ttu-id="5cd78-105">Содержимое сертификата можно просмотреть, но нельзя изменить.</span><span class="sxs-lookup"><span data-stu-id="5cd78-105">The contents of a certificate can be viewed but cannot be modified.</span></span> <span data-ttu-id="5cd78-106">Сведения в самом сертификате включают даты допустимости сертификата, издателя, субъекта и открытого ключа.</span><span class="sxs-lookup"><span data-stu-id="5cd78-106">Information in the certificate itself includes the certificate's validity dates, issuer, subject, and the public key.</span></span> <span data-ttu-id="5cd78-107">Однако сертификаты имеют связанные свойства, такие как отображаемое имя, описание и разрешенные варианты использования, которые можно просматривать и изменять.</span><span class="sxs-lookup"><span data-stu-id="5cd78-107">However, certificates have associated properties, such as a display name, description, and allowed uses, that can be viewed and edited.</span></span>

<span data-ttu-id="5cd78-108">В этом разделе демонстрируется создание тестовых сертификатов, Просмотр сертификатов и управление сертификатами и другими объектами безопасности.</span><span class="sxs-lookup"><span data-stu-id="5cd78-108">This section demonstrates creating test certificates, viewing certificates, and managing certificates and other security objects.</span></span> <span data-ttu-id="5cd78-109">Сертификаты и [*сертификаты издателей программного обеспечения*](../secgloss/s-gly.md) (спкс), которые могут быть созданы с помощью Makecert, строго используются исключительно для тестирования.</span><span class="sxs-lookup"><span data-stu-id="5cd78-109">The certificates and [*Software Publisher Certificates*](../secgloss/s-gly.md) (SPCs) that can be created with MakeCert are strictly for test purposes.</span></span> <span data-ttu-id="5cd78-110">Тестовый [*корневой сертификат*](../secgloss/r-gly.md) и корневой [*закрытый ключ*](../secgloss/p-gly.md) предоставляются только для тестирования.</span><span class="sxs-lookup"><span data-stu-id="5cd78-110">A test [*root certificate*](../secgloss/r-gly.md) and a test root [*private key*](../secgloss/p-gly.md) are provided for testing purposes only.</span></span> <span data-ttu-id="5cd78-111">Независимые поставщики программного обеспечения должны получить сертификат от ГТЕ, VeriSign, Inc. или другого [*центра сертификации*](../secgloss/c-gly.md) (CA), чтобы подписать код, который будет распространяться на общедоступный.</span><span class="sxs-lookup"><span data-stu-id="5cd78-111">Independent software vendors must obtain a certificate from GTE, VeriSign, Inc., or other [*certification authority*](../secgloss/c-gly.md) (CA) to sign code that will be distributed to the public.</span></span>

<span data-ttu-id="5cd78-112">Этот раздел содержит следующие подразделы:</span><span class="sxs-lookup"><span data-stu-id="5cd78-112">This section includes the following topics:</span></span>

-   [<span data-ttu-id="5cd78-113">Использование MakeCert</span><span class="sxs-lookup"><span data-stu-id="5cd78-113">Using MakeCert</span></span>](using-makecert.md)
-   [<span data-ttu-id="5cd78-114">Использование Cert2SPC</span><span class="sxs-lookup"><span data-stu-id="5cd78-114">Using Cert2SPC</span></span>](using-cert2spc.md)
-   [<span data-ttu-id="5cd78-115">Использование CertMgr</span><span class="sxs-lookup"><span data-stu-id="5cd78-115">Using CertMgr</span></span>](using-certmgr.md)

 

 
