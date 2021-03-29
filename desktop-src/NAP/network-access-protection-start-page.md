---
title: Защита доступа к сети
description: Примечание. Платформа защиты доступа к сети недоступна, начиная с Windows 10 Защита доступа к сети (NAP) — это набор компонентов операционной системы, предоставляющий платформу для защищенного доступа к частным сетям.
ms.assetid: f562f5f1-c05a-4e4e-bcd9-a302c61f2a5e
keywords:
- Защита доступа к сети
- Защита доступа к сети, начальная страница
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b99348428a867be5bf846fd40b030b844460cdc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775338"
---
# <a name="network-access-protection"></a><span data-ttu-id="e8ef2-105">Защита доступа к сети</span><span class="sxs-lookup"><span data-stu-id="e8ef2-105">Network Access Protection</span></span>

## <a name="purpose"></a><span data-ttu-id="e8ef2-106">Назначение</span><span class="sxs-lookup"><span data-stu-id="e8ef2-106">Purpose</span></span>

> [!Note]  
> <span data-ttu-id="e8ef2-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="e8ef2-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="e8ef2-108">Защита доступа к сети (NAP) — это набор компонентов операционной системы, предоставляющий платформу для защищенного доступа к частным сетям.</span><span class="sxs-lookup"><span data-stu-id="e8ef2-108">Network Access Protection (NAP) is a set of operating system components that provide a platform for protected access to private networks.</span></span> <span data-ttu-id="e8ef2-109">Платформа NAP предоставляет интегрированный способ оценки состояния работоспособности системы сетевого клиента, который пытается подключиться к сети или связаться с ней и ограничивать доступ к сети, пока не будут выполнены требования политики работоспособности.</span><span class="sxs-lookup"><span data-stu-id="e8ef2-109">The NAP platform provides an integrated way of evaluating the system health state of a network client that is attempting to connect to or communicate on a network and restricting the access of the network client until health policy requirements have been met.</span></span>

<span data-ttu-id="e8ef2-110">NAP — это расширяемая платформа, которая предоставляет инфраструктуру и набор API для добавления компонентов, которые хранят, сообщают, проверяют и исправляет состояние работоспособности системы компьютера.</span><span class="sxs-lookup"><span data-stu-id="e8ef2-110">NAP is an extensible platform that provides an infrastructure and an API set for adding components that store, report, validate, and correct a computer's system health state.</span></span> <span data-ttu-id="e8ef2-111">Сама по себе Платформа NAP не предоставляет компоненты для накопления и оценки атрибутов состояния работоспособности компьютера.</span><span class="sxs-lookup"><span data-stu-id="e8ef2-111">By itself, the NAP platform does not provide components to accumulate and evaluate attributes of a computer's health state.</span></span> <span data-ttu-id="e8ef2-112">Другие компоненты, известные как агенты работоспособности системы (SHA) и средства проверки работоспособности системы (SHV), обеспечивают проверку политики сети и соответствие политике сети.</span><span class="sxs-lookup"><span data-stu-id="e8ef2-112">Other components, known as system health agents (SHAs) and system health validators (SHVs), provide network policy validation and network policy compliance.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="e8ef2-113">Где применимо</span><span class="sxs-lookup"><span data-stu-id="e8ef2-113">Where applicable</span></span>

<span data-ttu-id="e8ef2-114">Защита доступа к сети разработана для расширения.</span><span class="sxs-lookup"><span data-stu-id="e8ef2-114">NAP is designed to be extensible.</span></span> <span data-ttu-id="e8ef2-115">Он может взаимодействовать с любым программным обеспечением поставщика, которое предоставляет SHA и SHV или распознает опубликованный набор API.</span><span class="sxs-lookup"><span data-stu-id="e8ef2-115">It can interoperate with any vendor software that provides SHAs and SHVs or that recognizes its published API set.</span></span> <span data-ttu-id="e8ef2-116">NAP обеспечивает решение для следующих распространенных сценариев:</span><span class="sxs-lookup"><span data-stu-id="e8ef2-116">NAP helps provide a solution for the following common scenarios:</span></span>

-   <span data-ttu-id="e8ef2-117">Проверьте работоспособность и состояние перемещаемых ноутбуков.</span><span class="sxs-lookup"><span data-stu-id="e8ef2-117">Check the health and status of roaming laptops.</span></span>
-   <span data-ttu-id="e8ef2-118">Убедитесь в работоспособности настольных компьютеров.</span><span class="sxs-lookup"><span data-stu-id="e8ef2-118">Ensure the health of desktop computers.</span></span>
-   <span data-ttu-id="e8ef2-119">Проверка соответствия и работоспособности компьютеров в удаленных офисах.</span><span class="sxs-lookup"><span data-stu-id="e8ef2-119">Verify the compliance and health of computers in remote offices.</span></span>
-   <span data-ttu-id="e8ef2-120">Определите работоспособность посещаемых ноутбуков.</span><span class="sxs-lookup"><span data-stu-id="e8ef2-120">Determine the health of visiting laptops.</span></span>
-   <span data-ttu-id="e8ef2-121">Проверьте соответствие и работоспособность неуправляемых домашних компьютеров.</span><span class="sxs-lookup"><span data-stu-id="e8ef2-121">Verify the compliance and health of unmanaged home computers.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="e8ef2-122">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="e8ef2-122">Developer audience</span></span>

<span data-ttu-id="e8ef2-123">API NAP предназначен для разработчиков на C/C++.</span><span class="sxs-lookup"><span data-stu-id="e8ef2-123">The NAP API is designed for C/C++ developers.</span></span> <span data-ttu-id="e8ef2-124">Для методов принудительной защиты доступа к сети программисты должны быть знакомы с сетевыми протоколами и технологиями, такими как служба поддержки пользователей удаленного доступа (RADIUS), протокол DHCP, виртуальные частные сети (VPN), стандарт IEEE 802.1 X для проводного и беспроводного доступа, а также безопасность протокола Интернета (IPsec).</span><span class="sxs-lookup"><span data-stu-id="e8ef2-124">For the NAP enforcement methods, programmers should be familiar with networking protocols and technologies such as Remote Authentication Dial-in User Service (RADIUS), Dynamic Host Configuration Protocol (DHCP), virtual private networks (VPNs), the IEEE 802.1X standard for wired and wireless access, and Internet Protocol security (IPsec).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="e8ef2-125">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="e8ef2-125">Run-time requirements</span></span>

<span data-ttu-id="e8ef2-126">Для платформы NAP требуются серверы инфраструктуры NAP под управлением Windows Server 2008 или более поздней версии и клиенты NAP под управлением Windows XP с пакетом обновления 3 (SP3), Windows Vista или более поздней операционной системой.</span><span class="sxs-lookup"><span data-stu-id="e8ef2-126">The NAP platform requires NAP infrastructure servers running Windows Server 2008 or later and NAP clients running Windows XP with Service Pack 3 (SP3), Windows Vista, or later operating systems.</span></span> <span data-ttu-id="e8ef2-127">Конкретные сведения о том, какие операционные системы поддерживают определенный программный элемент, см. в разделах требования интерфейсов API NAP в справочной документации по NAP.</span><span class="sxs-lookup"><span data-stu-id="e8ef2-127">For specific information about which operating systems support a particular programming element, refer to the Requirements sections of the NAP APIs in the NAP Reference documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="e8ef2-128">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="e8ef2-128">In this section</span></span>



| <span data-ttu-id="e8ef2-129">Раздел</span><span class="sxs-lookup"><span data-stu-id="e8ef2-129">Topic</span></span>                                         | <span data-ttu-id="e8ef2-130">Описание</span><span class="sxs-lookup"><span data-stu-id="e8ef2-130">Description</span></span>                                                                       |
|-----------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="e8ef2-131">О NAP</span><span class="sxs-lookup"><span data-stu-id="e8ef2-131">About NAP</span></span>](about-nap.md)<br/>         | <span data-ttu-id="e8ef2-132">Общие сведения об API NAP.</span><span class="sxs-lookup"><span data-stu-id="e8ef2-132">General information about NAP API.</span></span><br/>                                     |
| [<span data-ttu-id="e8ef2-133">Использование NAP</span><span class="sxs-lookup"><span data-stu-id="e8ef2-133">Using NAP</span></span>](using-nap.md)<br/>         | <span data-ttu-id="e8ef2-134">Примеры использования API защиты доступа к сети.</span><span class="sxs-lookup"><span data-stu-id="e8ef2-134">Usage examples for NAP API.</span></span><br/>                                            |
| [<span data-ttu-id="e8ef2-135">Справочник по NAP</span><span class="sxs-lookup"><span data-stu-id="e8ef2-135">NAP Reference</span></span>](nap-reference.md)<br/> | <span data-ttu-id="e8ef2-136">Документация по интерфейсам NAP, структурам и другим элементам кода.</span><span class="sxs-lookup"><span data-stu-id="e8ef2-136">Documentation for NAP interfaces, structures, and other code elements.</span></span><br/> |



 

 

 





