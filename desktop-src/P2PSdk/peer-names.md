---
description: Одноранговые имена используются протоколом PNRP, одноранговым диспетчером удостоверений и инфраструктурой однорангового группирования.
ms.assetid: b0d78b17-6f48-4294-b8a2-8fcc1a7f8ef1
title: Имена одноранговых узлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b18774939d5e0e9bad208999fbc6ca1e5f624300
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663305"
---
# <a name="peer-names"></a><span data-ttu-id="e379e-103">Имена одноранговых узлов</span><span class="sxs-lookup"><span data-stu-id="e379e-103">Peer Names</span></span>

<span data-ttu-id="e379e-104">Одноранговые имена используются протоколом PNRP, одноранговым диспетчером удостоверений и инфраструктурой однорангового группирования.</span><span class="sxs-lookup"><span data-stu-id="e379e-104">Peer names are used by Peer Name Resolution Protocol (PNRP), the Peer Identity Manager, and the Peer Grouping Infrastructure.</span></span> <span data-ttu-id="e379e-105">Одноранговые имена — это стабильные имена для таких ресурсов, как компьютеры, пользователи, группы или службы.</span><span class="sxs-lookup"><span data-stu-id="e379e-105">Peer names are stable names for resources such as computers, users, groups, or services.</span></span> <span data-ttu-id="e379e-106">PNRP использует одноранговые имена для обнаружения узлов в одноранговой сети.</span><span class="sxs-lookup"><span data-stu-id="e379e-106">PNRP uses peer names to identify nodes in a peer network.</span></span>

> [!Note]  
> <span data-ttu-id="e379e-107">Конечная точка, используемая одноранговой инфраструктурой, на самом деле является кортежем, состоящим из адреса IPv4 или IPv6, порта и протокола (TCP или UDP).</span><span class="sxs-lookup"><span data-stu-id="e379e-107">An endpoint that the Peer Infrastructure uses is actually a tuple that consists of an IPv4 or IPv6 address, port, and protocol (either TCP or UDP).</span></span> <span data-ttu-id="e379e-108">Одно имя однорангового узла может иметь более одного кортежа.</span><span class="sxs-lookup"><span data-stu-id="e379e-108">One peer name can have more than one tuple.</span></span>

 

<span data-ttu-id="e379e-109">Имя однорангового узла — это текстовая строка, имеющая следующий формат:</span><span class="sxs-lookup"><span data-stu-id="e379e-109">A peer name is a text string that has the following format:</span></span>

-   <span data-ttu-id="e379e-110">"Authority. классификатор"</span><span class="sxs-lookup"><span data-stu-id="e379e-110">"Authority.Classifier"</span></span>

<span data-ttu-id="e379e-111">Значение центра зависит от того, является ли имя безопасным или незащищенным.</span><span class="sxs-lookup"><span data-stu-id="e379e-111">The value of an Authority depends on whether the name is secure or unsecured.</span></span> <span data-ttu-id="e379e-112">Классификатор имени однорангового узла — это строка.</span><span class="sxs-lookup"><span data-stu-id="e379e-112">The Classifier of a peer name is a string.</span></span> <span data-ttu-id="e379e-113">Классификатор может быть любым именем, содержащим не более 150 символов Юникода.</span><span class="sxs-lookup"><span data-stu-id="e379e-113">A Classifier can be any name that contains 150 or less UNICODE characters.</span></span> <span data-ttu-id="e379e-114">Имена одноранговых узлов чувствительны к регистру и могут быть зарегистрированы как безопасные или незащищенные.</span><span class="sxs-lookup"><span data-stu-id="e379e-114">Peer names are case-sensitive and can be registered as secured or unsecured.</span></span> <span data-ttu-id="e379e-115">В следующем списке приведены некоторые примеры имен одноранговых узлов.</span><span class="sxs-lookup"><span data-stu-id="e379e-115">The following list identifies some examples of peer names:</span></span>

-   <span data-ttu-id="e379e-116">"0. Мюнсекуредпирнаме"</span><span class="sxs-lookup"><span data-stu-id="e379e-116">"0.MyUnsecuredPeerName"</span></span>
-   <span data-ttu-id="e379e-117">"0. JohnDoe. Games"</span><span class="sxs-lookup"><span data-stu-id="e379e-117">"0.JohnDoe.Games"</span></span>
-   <span data-ttu-id="e379e-118">"6520c005f63fc1864b7d8f3cabebd4916ae7f33d. JohnDoe</span><span class="sxs-lookup"><span data-stu-id="e379e-118">"6520c005f63fc1864b7d8f3cabebd4916ae7f33d.JohnDoe"</span></span>

## <a name="secure-peer-names"></a><span data-ttu-id="e379e-119">Безопасные имена одноранговых узлов</span><span class="sxs-lookup"><span data-stu-id="e379e-119">Secure Peer Names</span></span>

<span data-ttu-id="e379e-120">Для безопасного имени центр — это хэш SHA открытого ключа имени однорангового узла, который приводит к побайтовой шестнадцатеричной строке 40.</span><span class="sxs-lookup"><span data-stu-id="e379e-120">For a secure name, the Authority is the Secure Hash Algorithm (SHA) hash of the public key of the peer name, and results in a 40 character hexadecimal string.</span></span> <span data-ttu-id="e379e-121">Безопасное имя однорангового узла может быть зарегистрировано только в протоколе PNRP владельцем или делегатом владельца имени однорангового узла.</span><span class="sxs-lookup"><span data-stu-id="e379e-121">A secure peer name can only be registered with PNRP by the owner or delegate of the peer name owner.</span></span> <span data-ttu-id="e379e-122">Безопасное имя однорангового узла должно быть создано путем вызова [**пиркреатепирнаме**](/windows/desktop/api/P2P/nf-p2p-peercreatepeername).</span><span class="sxs-lookup"><span data-stu-id="e379e-122">A secured peer name must be created by calling [**PeerCreatePeerName**](/windows/desktop/api/P2P/nf-p2p-peercreatepeername).</span></span>

## <a name="unsecured-peer-names"></a><span data-ttu-id="e379e-123">Небезопасные имена одноранговых узлов</span><span class="sxs-lookup"><span data-stu-id="e379e-123">Unsecured Peer Names</span></span>

<span data-ttu-id="e379e-124">Для незащищенного имени центр равен нулю (0), а классификатор является единственной важной частью имени однорангового узла, который создает небезопасное имя однорангового узла без связанного [удостоверения](identity-manager-api.md).</span><span class="sxs-lookup"><span data-stu-id="e379e-124">For an unsecured name, the Authority is zero (0), and the Classifier is the only significant part of the peer name, which creates an unsecured peer name without an associated [identity](identity-manager-api.md).</span></span> <span data-ttu-id="e379e-125">Небезопасные имена одноранговых узлов используются в регистрации и разрешении имен PNRP.</span><span class="sxs-lookup"><span data-stu-id="e379e-125">Unsecured peer names are used in PNRP name registration and resolution.</span></span> <span data-ttu-id="e379e-126">Небезопасные имена одноранговых узлов предоставляют удобный способ регистрации и разрешения ресурсов, которые не нуждаются в безопасном разрешении имен.</span><span class="sxs-lookup"><span data-stu-id="e379e-126">Unsecured peer names provide a useful way to register and resolve resources that do not require secure name resolution.</span></span> <span data-ttu-id="e379e-127">Однако любой узел может опубликовать любое незащищенное имя.</span><span class="sxs-lookup"><span data-stu-id="e379e-127">However, any node can publish any unsecured name.</span></span> <span data-ttu-id="e379e-128">Приложения, связанные с безопасностью, должны обеспечивать надежность и безопасность при использовании незащищенных имен одноранговых узлов.</span><span class="sxs-lookup"><span data-stu-id="e379e-128">Applications concerned with security must ensure that they are robust and secure in their consumption of unsecured peer names.</span></span>

> [!Note]  
> <span data-ttu-id="e379e-129">Любой пользователь может зарегистрировать незащищенное имя однорангового узла с помощью PNRP.</span><span class="sxs-lookup"><span data-stu-id="e379e-129">Anyone can register an unsecured peer name with PNRP.</span></span>

 

## <a name="pnrp-and-the-nearest-peer-name-instance"></a><span data-ttu-id="e379e-130">PNRP и ближайший экземпляр имени однорангового узла</span><span class="sxs-lookup"><span data-stu-id="e379e-130">PNRP and the Nearest Peer Name Instance</span></span>

<span data-ttu-id="e379e-131">Может существовать более одного экземпляра однорангового имени.</span><span class="sxs-lookup"><span data-stu-id="e379e-131">There can be more than one instance of a peer name.</span></span> <span data-ttu-id="e379e-132">При использовании протокола [PNRP](pnrp-namespace-provider-api.md) для разрешения имени однорангового узла существует понятие **ближайшего** экземпляра имени однорангового узла. Это означает, что имя службы имеет расположение, ближайшее к элементу **Сахинт** , указанному в [**пнрпинфо \_ v1**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) или [**пнрпинфо \_ v2**](/previous-versions/windows/desktop/legacy/aa371671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e379e-132">When using [PNRP](pnrp-namespace-provider-api.md) to resolve a peer name, there is a concept of a **nearest** peer name instance, which means that the name has a service location closest to the **saHint** member specified in [**PNRPINFO\_V1**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) or [**PNRPINFO\_V2**](/previous-versions/windows/desktop/legacy/aa371671(v=vs.85)).</span></span> <span data-ttu-id="e379e-133">Если подсказка не указана, ближайший к одному из локальных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="e379e-133">If no hint is supplied, closest to one of the local IP addresses.</span></span>

 

 
