---
description: Службы сертификатов, работающие в операционной системе Windows Server, получают запросы на новые цифровые сертификаты через транспорты, такие как RPC или HTTP.
ms.assetid: 4c0098be-6b1b-4ce0-b3a0-942c1290b5b4
title: Службы сертификатов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1a3f25972f98a79a208719eb2bcb08de07d7894
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684005"
---
# <a name="certificate-services"></a><span data-ttu-id="b27fa-103">Службы сертификатов</span><span class="sxs-lookup"><span data-stu-id="b27fa-103">Certificate Services</span></span>

<span data-ttu-id="b27fa-104">[*Службы сертификатов*](../secgloss/c-gly.md), работающие в операционной системе Windows Server, получают запросы на новые цифровые сертификаты через транспорты, такие как RPC или HTTP.</span><span class="sxs-lookup"><span data-stu-id="b27fa-104">[*Certificate Services*](../secgloss/c-gly.md), a service running on a Windows server operating system, receives requests for new digital certificates over transports such as RPC or HTTP.</span></span> <span data-ttu-id="b27fa-105">Он проверяет каждый запрос на соответствие настраиваемым или особым политикам для конкретного сайта, устанавливает дополнительные свойства для выдаваемого сертификата и выдает сертификат.</span><span class="sxs-lookup"><span data-stu-id="b27fa-105">It checks each request against custom or site-specific policies, sets optional properties for a certificate to be issued, and issues the certificate.</span></span> <span data-ttu-id="b27fa-106">Службы сертификации позволяют администраторам добавлять элементы в [*список отзыва сертификатов*](../secgloss/c-gly.md) (CRL) и регулярно публиковать подписанные списки CRL.</span><span class="sxs-lookup"><span data-stu-id="b27fa-106">Certificate Services allows administrators to add elements to a [*certificate revocation list*](../secgloss/c-gly.md) (CRL), and to publish signed CRLs on a regular basis.</span></span>

<span data-ttu-id="b27fa-107">Службы сертификатов включают программируемые интерфейсы для создания поддержки дополнительных транспортов, политик и свойств сертификатов и форматов.</span><span class="sxs-lookup"><span data-stu-id="b27fa-107">Certificate services include programmable interfaces for creating support for additional transports, policies, and certificate properties and formats.</span></span>

<span data-ttu-id="b27fa-108">В Windows Server 2003 службы сертификатов 2,0 можно установить из **панели управления** , щелкнув элемент **Установка и удаление программ** , а затем выбрав пункт **Установка и удаление компонентов Windows** , чтобы установить или удалить службы сертификатов.</span><span class="sxs-lookup"><span data-stu-id="b27fa-108">In Windows Server 2003, Certificate Services 2.0 can be installed from **Control Panel** by clicking **Add or Remove Programs** and then clicking **Add/Remove Windows Components** to install or uninstall Certificate Services.</span></span>

<span data-ttu-id="b27fa-109">Основные понятия служб сертификации подробно описаны в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="b27fa-109">Certificate Services concepts are detailed in the following sections.</span></span> <span data-ttu-id="b27fa-110">Содержимое предназначено для помощи в разработке приложений, которые будут взаимодействовать со службами сертификатов.</span><span class="sxs-lookup"><span data-stu-id="b27fa-110">The content is intended to help you develop applications that will interact with Certificate Services.</span></span>



| <span data-ttu-id="b27fa-111">Содержимое</span><span class="sxs-lookup"><span data-stu-id="b27fa-111">Content</span></span>                                                                                                                                                           | <span data-ttu-id="b27fa-112">Section</span><span class="sxs-lookup"><span data-stu-id="b27fa-112">Section</span></span>                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="b27fa-113">Описание функций служб сертификации</span><span class="sxs-lookup"><span data-stu-id="b27fa-113">Description of the features of Certificate Services</span></span>                                                                                                               | [<span data-ttu-id="b27fa-114">Функции служб сертификатов</span><span class="sxs-lookup"><span data-stu-id="b27fa-114">Certificate Services Features</span></span>](certificate-services-features.md)         |
| <span data-ttu-id="b27fa-115">Обзор архитектуры служб сертификации</span><span class="sxs-lookup"><span data-stu-id="b27fa-115">Overview of Certificate Services architecture</span></span>                                                                                                                     | [<span data-ttu-id="b27fa-116">Архитектура служб сертификатов</span><span class="sxs-lookup"><span data-stu-id="b27fa-116">Certificate Services Architecture</span></span>](certificate-services-architecture.md) |
| <span data-ttu-id="b27fa-117">Отношение между сертификатом, субъектом сертификата и [ *открытым ключом* субъекта](../secgloss/p-gly.md)</span><span class="sxs-lookup"><span data-stu-id="b27fa-117">Relationship between a certificate, the certificate's subject, and the subject's [*public key*](../secgloss/p-gly.md)</span></span> | [<span data-ttu-id="b27fa-118">Сертификаты и открытые ключи</span><span class="sxs-lookup"><span data-stu-id="b27fa-118">Certificates and Public Keys</span></span>](certificates-and-public-keys.md)           |
| <span data-ttu-id="b27fa-119">Сведения о свойствах запроса сертификата</span><span class="sxs-lookup"><span data-stu-id="b27fa-119">Information about the Certificate Request properties</span></span>                                                                                                              | [<span data-ttu-id="b27fa-120">Рекомендации по запросам сертификатов</span><span class="sxs-lookup"><span data-stu-id="b27fa-120">Certificate Request Guidelines</span></span>](certificate-request-guidelines.md)       |
| <span data-ttu-id="b27fa-121">Сведения о том, как сертификат обрабатывается службами сертификации</span><span class="sxs-lookup"><span data-stu-id="b27fa-121">Details of how a certificate is processed by Certificate Services</span></span>                                                                                                 | [<span data-ttu-id="b27fa-122">О сертификатах</span><span class="sxs-lookup"><span data-stu-id="b27fa-122">About Certificates</span></span>](about-certificates.md)                               |
| <span data-ttu-id="b27fa-123">Описание процесса продления [*центра сертификации*](../secgloss/c-gly.md)</span><span class="sxs-lookup"><span data-stu-id="b27fa-123">Description of the [*certification authority*](../secgloss/c-gly.md) renewal process</span></span>        | [<span data-ttu-id="b27fa-124">Продление центра сертификации</span><span class="sxs-lookup"><span data-stu-id="b27fa-124">Certification Authority Renewal</span></span>](certification-authority-renewal.md)     |



 

<span data-ttu-id="b27fa-125">Также включены следующие дополнительные полезные темы.</span><span class="sxs-lookup"><span data-stu-id="b27fa-125">The following additional useful topics are also included.</span></span>



| <span data-ttu-id="b27fa-126">Содержимое</span><span class="sxs-lookup"><span data-stu-id="b27fa-126">Content</span></span>                                                                                                                                             | <span data-ttu-id="b27fa-127">Section</span><span class="sxs-lookup"><span data-stu-id="b27fa-127">Section</span></span>                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <span data-ttu-id="b27fa-128">Документация по управлению регистрацией сертификатов, которая предоставляет службы для создания запросов сертификатов, включая запросы для пользователей смарт-карт.</span><span class="sxs-lookup"><span data-stu-id="b27fa-128">Documentation on Certificate Enrollment Control, which provides services for creating certificate requests including requests for smart card users.</span></span> | [<span data-ttu-id="b27fa-129">Управление регистрацией сертификатов</span><span class="sxs-lookup"><span data-stu-id="b27fa-129">Certificate Enrollment Control</span></span>](certificate-enrollment-control.md) |
| <span data-ttu-id="b27fa-130">Документация по интерфейсу прикладного программирования Microsoft Cryptography, предоставляющему службы безопасности на основе шифрования.</span><span class="sxs-lookup"><span data-stu-id="b27fa-130">Documentation on the Microsoft Cryptographic Application Programming Interface, which provides cryptography-based security services.</span></span>                | [<span data-ttu-id="b27fa-131">Основы криптографии</span><span class="sxs-lookup"><span data-stu-id="b27fa-131">Cryptography Essentials</span></span>](cryptography-essentials.md)               |
| <span data-ttu-id="b27fa-132">Документация по смарт-карте, которая предоставляет службы для разработки и использования систем со смарт-картами.</span><span class="sxs-lookup"><span data-stu-id="b27fa-132">Documentation on Smart Card, which provides services for developing and using smart card systems.</span></span>                                                   | [<span data-ttu-id="b27fa-133">Смарт-карта</span><span class="sxs-lookup"><span data-stu-id="b27fa-133">Smart Card</span></span>](../secauthn/smart-card-authentication.md)                     |
| <span data-ttu-id="b27fa-134">Имя свойства сертификатов и запросов сертификатов.</span><span class="sxs-lookup"><span data-stu-id="b27fa-134">Name properties of certificates and certificate requests.</span></span>                                                                                           | [<span data-ttu-id="b27fa-135">Свойства имени</span><span class="sxs-lookup"><span data-stu-id="b27fa-135">Name Properties</span></span>](name-properties.md)                               |
| <span data-ttu-id="b27fa-136">Список и описания свойств сертификата [*X. 509*](../secgloss/x-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="b27fa-136">List and descriptions of [*X.509*](../secgloss/x-gly.md) certificate properties.</span></span>                                  | [<span data-ttu-id="b27fa-137">Свойства сертификата</span><span class="sxs-lookup"><span data-stu-id="b27fa-137">Certificate Properties</span></span>](certificate-properties.md)                 |



 

 

 
