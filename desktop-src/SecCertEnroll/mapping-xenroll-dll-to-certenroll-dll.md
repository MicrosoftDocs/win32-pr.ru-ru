---
description: Библиотека Xenroll.dll была удалена из операционной системы и заменена CertEnroll.dll.
ms.assetid: ec28fbdc-9198-472a-8976-7b5db09069a6
title: Сопоставление Xenroll.dll CertEnroll.dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1fcaec56967f4c694b85d454bd21407c3af9029
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815769"
---
# <a name="mapping-xenrolldll-to-certenrolldll"></a><span data-ttu-id="e680a-103">Сопоставление Xenroll.dll CertEnroll.dll</span><span class="sxs-lookup"><span data-stu-id="e680a-103">Mapping Xenroll.dll to CertEnroll.dll</span></span>

<span data-ttu-id="e680a-104">До выхода Windows Vista Управление регистрацией сертификатов было реализовано в Xenroll.dll.</span><span class="sxs-lookup"><span data-stu-id="e680a-104">Prior to Windows Vista, the Certificate Enrollment Control was implemented in Xenroll.dll.</span></span> <span data-ttu-id="e680a-105">Библиотека Xenroll.dll была удалена из операционной системы и заменена CertEnroll.dll.</span><span class="sxs-lookup"><span data-stu-id="e680a-105">The Xenroll.dll library has been removed from the operating system and replaced by CertEnroll.dll.</span></span>

<span data-ttu-id="e680a-106">Xenroll попытался реализовать два параллельных набора интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="e680a-106">Xenroll attempted to implement two parallel sets of interfaces.</span></span> <span data-ttu-id="e680a-107">[**Иценролл**](/windows/desktop/api/xenroll/nn-xenroll-icenroll), [**ICEnroll2**](/windows/desktop/api/xenroll/nn-xenroll-icenroll2), [**ICEnroll3**](/windows/desktop/api/xenroll/nn-xenroll-icenroll3)и [**ICEnroll4**](/windows/desktop/api/xenroll/nn-xenroll-icenroll4) были совместимы с автоматизацией и совместимы с языками сценариев.</span><span class="sxs-lookup"><span data-stu-id="e680a-107">[**ICEnroll**](/windows/desktop/api/xenroll/nn-xenroll-icenroll), [**ICEnroll2**](/windows/desktop/api/xenroll/nn-xenroll-icenroll2), [**ICEnroll3**](/windows/desktop/api/xenroll/nn-xenroll-icenroll3), and [**ICEnroll4**](/windows/desktop/api/xenroll/nn-xenroll-icenroll4) were Automation-compliant and compatible with scripting languages.</span></span> <span data-ttu-id="e680a-108">Соответствующие интерфейсы —[**иенролл**](/windows/desktop/api/xenroll/nn-xenroll-ienroll), [**IEnroll2**](/windows/desktop/api/xenroll/nn-xenroll-ienroll2)и [**IEnroll4**](/windows/desktop/api/xenroll/nn-xenroll-ienroll4)— не могут быть внесены в скрипт, но более удобны для программистов C++.</span><span class="sxs-lookup"><span data-stu-id="e680a-108">The corresponding interfaces—[**IEnroll**](/windows/desktop/api/xenroll/nn-xenroll-ienroll), [**IEnroll2**](/windows/desktop/api/xenroll/nn-xenroll-ienroll2), and [**IEnroll4**](/windows/desktop/api/xenroll/nn-xenroll-ienroll4)—could not be scripted but were more convenient for C++ programmers.</span></span> <span data-ttu-id="e680a-109">По мере их развития два набора интерфейсов не сохранились синхронизированными.</span><span class="sxs-lookup"><span data-stu-id="e680a-109">As they evolved, the two sets of interfaces did not remain synchronized.</span></span> <span data-ttu-id="e680a-110">В частности, набор сдвоенных интерфейсов, которые в последнее время представляются **ICEnroll4** , определяет только подмножество функций, определенных **IEnroll4**.</span><span class="sxs-lookup"><span data-stu-id="e680a-110">In particular, the set of dual interfaces represented most recently by **ICEnroll4** defines only a subset of the functionality defined by **IEnroll4**.</span></span>

<span data-ttu-id="e680a-111">CertEnroll.dll реализует более широкий и структурированный набор совместимых с автоматизацией COM-интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="e680a-111">CertEnroll.dll implements a larger and more structured set of Automation-compliant COM interfaces.</span></span> <span data-ttu-id="e680a-112">В следующих разделах описывается, как Xenroll.dll сопоставляется CertEnroll.dll для различных типов функций.</span><span class="sxs-lookup"><span data-stu-id="e680a-112">The following topics discuss how Xenroll.dll maps to CertEnroll.dll for different types of functionality.</span></span>

-   [<span data-ttu-id="e680a-113">Функции запроса сертификата</span><span class="sxs-lookup"><span data-stu-id="e680a-113">Certificate Request Functions</span></span>](certificate-request-functions.md)
-   [<span data-ttu-id="e680a-114">Функции ответа на сертификат</span><span class="sxs-lookup"><span data-stu-id="e680a-114">Certificate Response Functions</span></span>](certificate-response-functions.md)
-   [<span data-ttu-id="e680a-115">Функции атрибутов</span><span class="sxs-lookup"><span data-stu-id="e680a-115">Attribute Functions</span></span>](attribute-functions.md)
-   [<span data-ttu-id="e680a-116">Функции расширения</span><span class="sxs-lookup"><span data-stu-id="e680a-116">Extension Functions</span></span>](extension-functions.md)
-   [<span data-ttu-id="e680a-117">Функции внешних свойств</span><span class="sxs-lookup"><span data-stu-id="e680a-117">External Property Functions</span></span>](external-property-functions.md)
-   [<span data-ttu-id="e680a-118">Функции закрытых и открытых ключей</span><span class="sxs-lookup"><span data-stu-id="e680a-118">Private and Public Key Functions</span></span>](private-and-public-key-functions.md)
-   [<span data-ttu-id="e680a-119">Функции поставщика служб шифрования</span><span class="sxs-lookup"><span data-stu-id="e680a-119">Cryptographic Service Provider Functions</span></span>](cryptographic-service-provider-functions.md)
-   [<span data-ttu-id="e680a-120">Функции хранилища сертификатов</span><span class="sxs-lookup"><span data-stu-id="e680a-120">Certificate Store Functions</span></span>](certificate-store-functions.md)
-   [<span data-ttu-id="e680a-121">Функции обмена личной информацией</span><span class="sxs-lookup"><span data-stu-id="e680a-121">Personal Information Exchange Functions</span></span>](personal-information-exchange-functions.md)
-   [<span data-ttu-id="e680a-122">Вспомогательные функции</span><span class="sxs-lookup"><span data-stu-id="e680a-122">Helper Functions</span></span>](helper-functions.md)

## <a name="related-topics"></a><span data-ttu-id="e680a-123">См. также</span><span class="sxs-lookup"><span data-stu-id="e680a-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e680a-124">Использование API регистрации сертификатов</span><span class="sxs-lookup"><span data-stu-id="e680a-124">Using the Certificate Enrollment API</span></span>](about-the-certificate-enrollment-api.md)
</dt> </dl>

 

 
