---
title: Очередь сообщений RPC
description: Служба очередей сообщений (MSMQ) позволяет пользователям обмениваться данными между сетями и системами независимо от текущего состояния взаимодействующих приложений и систем.
ms.assetid: f1c8665b-3754-4c2e-b3ac-bba1f4b329e1
keywords:
- Удаленный вызов процедур RPC, описание, очередь сообщений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b72e9e35ec2aa1cc440c0d0356c681c4fe8548c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068388"
---
# <a name="rpc-message-queuing"></a><span data-ttu-id="e2602-104">Очередь сообщений RPC</span><span class="sxs-lookup"><span data-stu-id="e2602-104">RPC Message Queuing</span></span>

<span data-ttu-id="e2602-105">Служба очередей сообщений (MSMQ) позволяет пользователям обмениваться данными между сетями и системами независимо от текущего состояния взаимодействующих приложений и систем.</span><span class="sxs-lookup"><span data-stu-id="e2602-105">Message Queuing (MSMQ) lets users communicate across networks and systems regardless of the current state of the communicating applications and systems.</span></span> <span data-ttu-id="e2602-106">Приложения отправляют и получают сообщения через очереди сообщений, которые поддерживаются службой MSMQ.</span><span class="sxs-lookup"><span data-stu-id="e2602-106">Applications send and receive messages through message queues that MSMQ maintains.</span></span> <span data-ttu-id="e2602-107">Очереди сообщений продолжают работать, даже если клиентское или серверное приложение не работает.</span><span class="sxs-lookup"><span data-stu-id="e2602-107">The message queues continue to function even when the client or server application is not running.</span></span> <span data-ttu-id="e2602-108">Служба очереди сообщений предоставляет следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="e2602-108">Message queuing provides:</span></span>

-   <span data-ttu-id="e2602-109">**Асинхронный обмен сообщениями.**</span><span class="sxs-lookup"><span data-stu-id="e2602-109">**Asynchronous messaging.**</span></span> <span data-ttu-id="e2602-110">При асинхронном обмене сообщениями MSMQ клиентское приложение может отправить сообщение на сервер и вернуться немедленно, даже если целевой компьютер или серверная программа не отвечают.</span><span class="sxs-lookup"><span data-stu-id="e2602-110">With MSMQ asynchronous messaging, a client application can send a message to a server and return immediately, even if the target computer or server program is not responding.</span></span>
-   <span data-ttu-id="e2602-111">**Гарантированная доставка сообщений.**</span><span class="sxs-lookup"><span data-stu-id="e2602-111">**Guaranteed message delivery.**</span></span> <span data-ttu-id="e2602-112">Когда приложение отправляет сообщение через MSMQ, сообщение будет достигать места назначения, даже если целевое приложение не выполняется одновременно, а сети и системы не находятся в автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="e2602-112">When an application sends a message through MSMQ, the message will reach its destination even if the destination application is not running at the same time or the networks and systems are offline.</span></span>
-   <span data-ttu-id="e2602-113">**Маршрутизация и динамическая конфигурация.**</span><span class="sxs-lookup"><span data-stu-id="e2602-113">**Routing and dynamic configuration.**</span></span> <span data-ttu-id="e2602-114">MSMQ обеспечивает гибкую маршрутизацию по разнородным сетям.</span><span class="sxs-lookup"><span data-stu-id="e2602-114">MSMQ provides flexible routing over heterogeneous networks.</span></span> <span data-ttu-id="e2602-115">Конфигурацию таких сетей можно динамически изменить, не внося существенных изменений в системы и сети.</span><span class="sxs-lookup"><span data-stu-id="e2602-115">The configuration of such networks can be changed dynamically without any major changes to systems and networks themselves.</span></span>
-   <span data-ttu-id="e2602-116">**Обмен сообщениями без подключения.**</span><span class="sxs-lookup"><span data-stu-id="e2602-116">**Connectionless messaging.**</span></span> <span data-ttu-id="e2602-117">Приложениям, использующим MSMQ, не нужно настраивать прямые сеансы с целевыми приложениями.</span><span class="sxs-lookup"><span data-stu-id="e2602-117">Applications using MSMQ do not need to set up direct sessions with target applications.</span></span>
-   <span data-ttu-id="e2602-118">[Безопасность](security.md).</span><span class="sxs-lookup"><span data-stu-id="e2602-118">[Security](security.md).</span></span> <span data-ttu-id="e2602-119">Служба MSMQ обеспечивает безопасную связь на основе безопасности Windows и API шифрования (CryptoAPI) для шифрования и цифровых подписей.</span><span class="sxs-lookup"><span data-stu-id="e2602-119">MSMQ provides secure communication based on Windows security and the Cryptographic API (CryptoAPI) for encryption and digital signatures.</span></span>
-   <span data-ttu-id="e2602-120">**Приоритет обмена сообщениями.**</span><span class="sxs-lookup"><span data-stu-id="e2602-120">**Prioritized Messaging.**</span></span> <span data-ttu-id="e2602-121">MSMQ передает сообщения по сетям в зависимости от приоритета, что обеспечивает более быстрое взаимодействие для критически важных приложений.</span><span class="sxs-lookup"><span data-stu-id="e2602-121">MSMQ transfers messages across networks based on priority, allowing faster communication for critical applications.</span></span>

<span data-ttu-id="e2602-122">Microsoft RPC расширяет модель Open Software Foundation Data Communications (использование-DCE) для удаленных вызовов процедур, позволяя распределенным приложениям использовать MSMQ в качестве транспорта и управлять многими его функциями.</span><span class="sxs-lookup"><span data-stu-id="e2602-122">Microsoft RPC extends the Open Software Foundation–Data Communications Equipment (OSF-DCE) model for remote procedure calls by allowing distributed applications to use MSMQ as a transport and to control many of its features.</span></span> <span data-ttu-id="e2602-123">Эта функция доступна как для обычных приложений RPC, так и через интерфейс **ирпкоптионс** для COM-приложений.</span><span class="sxs-lookup"><span data-stu-id="e2602-123">This functionality is available both to conventional RPC applications and, through the **IRPCOptions** interface, to COM applications.</span></span>

> [!Note]  
> <span data-ttu-id="e2602-124">Очередь сообщений RPC доступна только в Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="e2602-124">RPC message queuing is available only on Windows 2000.</span></span> <span data-ttu-id="e2602-125">Более поздние версии Windows не поддерживают очередь сообщений RPC.</span><span class="sxs-lookup"><span data-stu-id="e2602-125">Later versions of Windows do not support RPC message queuing.</span></span>

 

<span data-ttu-id="e2602-126">В следующих разделах приводятся общие сведения об очереди сообщений.</span><span class="sxs-lookup"><span data-stu-id="e2602-126">The following topics provide an overview of message queuing:</span></span>

-   [<span data-ttu-id="e2602-127">Обзор архитектуры служб очереди сообщений</span><span class="sxs-lookup"><span data-stu-id="e2602-127">Overview of Message Queuing Services Architecture</span></span>](overview-of-message-queuing-services-architecture.md)
-   [<span data-ttu-id="e2602-128">Свойства очереди сообщений и сообщений</span><span class="sxs-lookup"><span data-stu-id="e2602-128">Message and Message Queue Properties</span></span>](message-and-message-queue-properties.md)
-   [<span data-ttu-id="e2602-129">Использование MSMQ в качестве транспорта RPC</span><span class="sxs-lookup"><span data-stu-id="e2602-129">Using MSMQ as an RPC Transport</span></span>](using-msmq-as-an-rpc-transport.md)
-   [<span data-ttu-id="e2602-130">Требования к системе для \_ приложений очереди сообщений RPC</span><span class="sxs-lookup"><span data-stu-id="e2602-130">System Requirements for RPC-Message\_Queuing Applications</span></span>](system-requirements-for-rpc-message-queuing-applications.md)
-   [<span data-ttu-id="e2602-131">Разработка приложений RPC-Message Queuing</span><span class="sxs-lookup"><span data-stu-id="e2602-131">Developing RPC-Message Queuing Applications</span></span>](developing-rpc-message-queuing-applications.md)
-   [<span data-ttu-id="e2602-132">Службы безопасности MSMQ</span><span class="sxs-lookup"><span data-stu-id="e2602-132">MSMQ Security Services</span></span>](msmq-security-services.md)

 

 




