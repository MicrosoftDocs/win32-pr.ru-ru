---
title: О TBS
description: Системная служба, которая обеспечивает прозрачное совместное использование ресурсов доверенный платформенный модуль (TPM) (TPM).
ms.assetid: 5ab3f514-dea9-48f7-97d9-abc774e2a273
keywords:
- TBS базовых служб TPM, сведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a5d40b1fca688676978f274cb976afedb6e6a56
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/20/2020
ms.locfileid: "104260385"
---
# <a name="about-tbs"></a><span data-ttu-id="b11ac-104">О TBS</span><span class="sxs-lookup"><span data-stu-id="b11ac-104">About TBS</span></span>

<span data-ttu-id="b11ac-105">Функция базовых служб TPM (TBS) — это системная служба, которая обеспечивает прозрачное совместное использование ресурсов доверенный платформенный модуль (TPM) (TPM).</span><span class="sxs-lookup"><span data-stu-id="b11ac-105">The TPM Base Services (TBS) feature is a system service that allows transparent sharing of the Trusted Platform Module (TPM) resources.</span></span> <span data-ttu-id="b11ac-106">Он одновременно разделяет ресурсы TPM между несколькими приложениями на одном физическом компьютере, даже если эти приложения работают на разных виртуальных машинах.</span><span class="sxs-lookup"><span data-stu-id="b11ac-106">It simultaneously shares the TPM resources among multiple applications on the same physical machine, even if those applications run on different virtual machines.</span></span> <span data-ttu-id="b11ac-107">Начиная с Windows 8 и Windows Server 2012, TBS поставляется предварительно установленным на всех системах с доверенным платформенным модулем.</span><span class="sxs-lookup"><span data-stu-id="b11ac-107">Starting with Windows 8 and Windows Server 2012, TBS comes pre-installed on all systems with a TPM.</span></span>

<span data-ttu-id="b11ac-108">Организация TCG (TCG) определяет доверенный платформенный модуль (TPM), который предоставляет криптографические функции, предназначенные для обеспечения доверия в платформе.</span><span class="sxs-lookup"><span data-stu-id="b11ac-108">The Trusted Computing Group (TCG) defines a Trusted Platform Module that provides cryptographic functions designed to provide trust in the platform.</span></span> <span data-ttu-id="b11ac-109">Поскольку доверенный платформенный модуль реализован в аппаратном обеспечении, он имеет ограниченные ресурсы.</span><span class="sxs-lookup"><span data-stu-id="b11ac-109">Because the TPM is implemented in hardware, it has finite resources.</span></span> <span data-ttu-id="b11ac-110">TCG также определяет стек программного обеспечения, который использует эти ресурсы для предоставления доверенных операций для программного обеспечения приложения.</span><span class="sxs-lookup"><span data-stu-id="b11ac-110">The TCG also defines a software stack that makes use of these resources to provide trusted operations for application software.</span></span> <span data-ttu-id="b11ac-111">Однако для запуска реализации Тсс параллельно с программным обеспечением операционной системы, которое также может использовать ресурсы доверенного платформенного модуля, не требуется выполнять собственную инициализацию.</span><span class="sxs-lookup"><span data-stu-id="b11ac-111">However, no provision is made for running a TSS implementation side-by-side with operating system software that may also be using TPM resources.</span></span> <span data-ttu-id="b11ac-112">Функция TBS решает эту проблему, позволяя каждому стеку программного обеспечения, взаимодействующему с TBS, использовать ресурсы TPM для проверки любых других программных стеков, которые могут выполняться на компьютере.</span><span class="sxs-lookup"><span data-stu-id="b11ac-112">The TBS feature solves this problem by enabling each software stack that communicates with TBS to use TPM resources checking for any other software stacks that may be running on the machine.</span></span>

<span data-ttu-id="b11ac-113">Спецификация TPM и Спецификация программного стека TCG (ТСС) доступны по адресу [https://www.trustedcomputinggroup.org](https://www.trustedcomputinggroup.org/) .</span><span class="sxs-lookup"><span data-stu-id="b11ac-113">The TPM specification and TCG Software Stack (TSS) specification are available at [https://www.trustedcomputinggroup.org](https://www.trustedcomputinggroup.org/).</span></span>

<span data-ttu-id="b11ac-114">TBS реализуется как служба вне процесса, которая принимает команды, использующие службу RPC.</span><span class="sxs-lookup"><span data-stu-id="b11ac-114">TBS is implemented as an out-of-process service that accepts commands that use an RPC service.</span></span> <span data-ttu-id="b11ac-115">Динамически связанная Библиотека представляет языковой интерфейс C и взаимодействует со службой TBS.</span><span class="sxs-lookup"><span data-stu-id="b11ac-115">A dynamically linked library presents the C language interface and communicates with the TBS service.</span></span>

> [!Note]  
> <span data-ttu-id="b11ac-116">Служба TBS принимает только запросы RPC с локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="b11ac-116">The TBS service only accepts RPC requests from the local machine.</span></span>

 

<span data-ttu-id="b11ac-117">Основные цели TBS:</span><span class="sxs-lookup"><span data-stu-id="b11ac-117">The primary goals of the TBS are to:</span></span>

-   <span data-ttu-id="b11ac-118">Обеспечить эффективный общий доступ к ограниченным ресурсам TPM, таким как слоты ключей, слоты сеансов авторизации и транспортные слоты.</span><span class="sxs-lookup"><span data-stu-id="b11ac-118">Provide efficient sharing of limited TPM resources, such as key slots, authorization sessions slots, and transport slots.</span></span>
-   <span data-ttu-id="b11ac-119">Предоставьте приоритетный и синхронизированный доступ к ресурсам TPM между несколькими экземплярами стеков программного обеспечения TPM.</span><span class="sxs-lookup"><span data-stu-id="b11ac-119">Provide prioritized and synchronized access to TPM resources between multiple instances of TPM software stacks.</span></span>
-   <span data-ttu-id="b11ac-120">Предоставьте соответствующее управление ресурсами доверенного платформенного модуля в различных состояниях электропитания.</span><span class="sxs-lookup"><span data-stu-id="b11ac-120">Provide appropriate management of TPM resources across power states.</span></span>
-   <span data-ttu-id="b11ac-121">Запрещает программным стекам доверенного платформенного модуля доступ к командам доверенного платформенного модуля, которые должны быть ограничены из-за ограничений платформы или административных требований.</span><span class="sxs-lookup"><span data-stu-id="b11ac-121">Prevent TPM software stacks from accessing TPM commands that should be restricted, either because of platform limitations or administrative requirements.</span></span>

<span data-ttu-id="b11ac-122">На следующем рисунке показана связь между TBS и доверенным платформенным модулем.</span><span class="sxs-lookup"><span data-stu-id="b11ac-122">The following illustration shows the relationship of the TBS to the TPM.</span></span>

![связь TBS в пользовательском режиме с доверенным платформенным модулем в режиме ядра](images/tbs-block-diagram-as11601.png)

 

 




