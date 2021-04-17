---
description: В этом разделе обсуждаются конкретные вопросы программирования при использовании одноранговой инфраструктуры.
ms.assetid: 525b0625-ec13-4aba-a741-dbacff3587f9
title: Вопросы программирования (одноранговые)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89956cbdbbc8d2ed89226a490bbae505862ab18f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663291"
---
# <a name="programming-considerations-peer-to-peer"></a><span data-ttu-id="e3657-103">Вопросы программирования (одноранговые)</span><span class="sxs-lookup"><span data-stu-id="e3657-103">Programming Considerations (Peer-to-Peer)</span></span>

<span data-ttu-id="e3657-104">В этом разделе обсуждаются конкретные вопросы программирования при использовании одноранговой инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="e3657-104">This topic discusses specific programming considerations when using the Peer Infrastructure.</span></span>

<span data-ttu-id="e3657-105">При использовании одноранговой инфраструктуры для разработки одноранговых приложений следует учитывать следующие аспекты программирования:</span><span class="sxs-lookup"><span data-stu-id="e3657-105">When using the Peer Infrastructure to develop peer applications, you must take the following programming considerations into account:</span></span>

-   <span data-ttu-id="e3657-106">IPv6;</span><span class="sxs-lookup"><span data-stu-id="e3657-106">IPv6</span></span>

    <span data-ttu-id="e3657-107">Одноранговая инфраструктура требует установки IPv6 и запуска приложений для работы с одноранговой сетью.</span><span class="sxs-lookup"><span data-stu-id="e3657-107">The Peer Infrastructure requires that IPv6 be installed and started to enable peer networking applications to function.</span></span>

-   <span data-ttu-id="e3657-108">Порты брандмауэра</span><span class="sxs-lookup"><span data-stu-id="e3657-108">Firewall Ports</span></span>

    <span data-ttu-id="e3657-109">При использовании брандмауэра в сети (например, в брандмауэре подключения к Интернету IPv6) необходимо открыть определенные порты, чтобы обеспечить функционирование одноранговой инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="e3657-109">When a firewall is being used on a network (such as the IPv6 Internet Connection firewall), specific ports must be opened to allow the Peer Infrastructure to function.</span></span> <span data-ttu-id="e3657-110">Должны быть открыты следующие порты:</span><span class="sxs-lookup"><span data-stu-id="e3657-110">The following ports must be open:</span></span>

    <span data-ttu-id="e3657-111">TCP-порт 3587 для инфраструктуры однорангового группирования.</span><span class="sxs-lookup"><span data-stu-id="e3657-111">TCP port 3587 for the Peer Grouping Infrastructure.</span></span>

    <span data-ttu-id="e3657-112">UDP-порт 3540 для инфраструктуры одноранговых диаграмм.</span><span class="sxs-lookup"><span data-stu-id="e3657-112">UDP port 3540 for the Peer Graphing Infrastructure.</span></span>

    > [!Note]  
    > <span data-ttu-id="e3657-113">Приложения, использующие одноранговую инфраструктуру диаграмм по протоколу TCP, выбирают собственный TCP-порт при вызове [**пирграфлистен**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten).</span><span class="sxs-lookup"><span data-stu-id="e3657-113">Applications that use the Peer Graphing Infrastructure over TCP choose their own TCP port when calling [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten).</span></span>

     

-   <span data-ttu-id="e3657-114">Параметр сокета</span><span class="sxs-lookup"><span data-stu-id="e3657-114">Socket Option</span></span>

    <span data-ttu-id="e3657-115">При попытке прямого подключения к другим одноранговым узлам IPv6 (без использования одноранговой инфраструктуры) убедитесь, что для параметра сокета IPV6 установлен уровень \_ \_ **защиты не \_ \_ ограничено**.</span><span class="sxs-lookup"><span data-stu-id="e3657-115">When attempting to connect to other IPv6 peer nodes directly (without using the Peer Infrastructure), ensure that the socket option IPV6\_PROTECTION\_LEVEL is set to **PROTECTION\_LEVEL\_UNRESTRICTED**.</span></span>

-   <span data-ttu-id="e3657-116">Пропускная способность</span><span class="sxs-lookup"><span data-stu-id="e3657-116">Bandwidth</span></span>

    <span data-ttu-id="e3657-117">При использовании PNRP приложение может опубликовать одно или несколько [одноранговых имен](peer-names.md) , которые можно разрешить.</span><span class="sxs-lookup"><span data-stu-id="e3657-117">When using PNRP, an application can publish one or more [peer names](peer-names.md) that can be resolved.</span></span> <span data-ttu-id="e3657-118">Для каждого имени однорангового узла, зарегистрированного в PNRP, существует увеличение пропускной способности сети, используемой протоколом PNRP для публикации имени однорангового узла, и обеспечение его доступности для разрешения другими узлами.</span><span class="sxs-lookup"><span data-stu-id="e3657-118">For each peer name registered with PNRP, there is an increase in the network bandwidth that PNRP uses to publish the peer name, and keep it available to be resolved by other nodes.</span></span>

    <span data-ttu-id="e3657-119">Чтобы избежать чрезмерного использования пропускной способности, приложения должны избегать регистрации большого количества одноранговых имен на компьютере.</span><span class="sxs-lookup"><span data-stu-id="e3657-119">To prevent using too much bandwidth, applications should avoid registering large numbers of peer names on a computer.</span></span> <span data-ttu-id="e3657-120">Например, приложение, которое публикует рисунки, не должно создавать имя однорангового узла для каждого изображения, но должно создать одно имя однорангового узла для службы, которое публикует изображения, и использовать другой протокол для клиентов, чтобы запросить службу для конкретных изображений.</span><span class="sxs-lookup"><span data-stu-id="e3657-120">For example, an application that publishes pictures should not create a peer name for each picture, but should create one peer name for the service that publishes pictures, and use a different protocol for clients to query the service for specific pictures.</span></span>

-   <span data-ttu-id="e3657-121">Регистрация имени однорангового узла</span><span class="sxs-lookup"><span data-stu-id="e3657-121">Peer Name Registration</span></span>

    <span data-ttu-id="e3657-122">Некоторым приложениям может потребоваться зарегистрировать одно и то же [имя однорангового узла](peer-names.md) на нескольких компьютерах.</span><span class="sxs-lookup"><span data-stu-id="e3657-122">Some applications may be required to register the same [peer name](peer-names.md) on more than one computer.</span></span> <span data-ttu-id="e3657-123">Как правило, это происходит, если имя однорангового узла связано с пользователем, использующим более одного компьютера.</span><span class="sxs-lookup"><span data-stu-id="e3657-123">Typically, this happens if a peer name is associated with a person who uses more than one computer.</span></span> <span data-ttu-id="e3657-124">Одним из способов, с помощью которых можно зарегистрировать одно и то же имя однорангового узла на нескольких компьютерах, является создание одноранговой группы для пользователя и подключение к этой группе со всех компьютеров.</span><span class="sxs-lookup"><span data-stu-id="e3657-124">One method that you can use to register the same peer name on multiple computers is to create a peer group for the person, and connect to that group from all computers.</span></span> <span data-ttu-id="e3657-125">Другой способ — создать одноранговый идентификатор и одноранговое имя на одном компьютере, экспортировать удостоверение однорангового узла с этого компьютера и импортировать его на другие компьютеры.</span><span class="sxs-lookup"><span data-stu-id="e3657-125">Another method is to create a peer identity and peer name on one computer, export the peer identity from that computer, and import it on other computers.</span></span> <span data-ttu-id="e3657-126">Это позволяет создать одно и то же безопасное имя однорангового узла на всех компьютерах, которые импортировали одноранговый идентификатор.</span><span class="sxs-lookup"><span data-stu-id="e3657-126">This allows the same secure peer name to be created on all the computers that have imported the peer identity.</span></span>

 

 



