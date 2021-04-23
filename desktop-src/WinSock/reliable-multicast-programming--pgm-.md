---
description: В этом разделе описывается реализация протокола многоадресной рассылки PGM в Windows, которая часто называется надежной многоадресной рассылкой. Надежная многоадресная рассылка реализуется через сокеты Windows в Windows Server 2003 и более поздних версиях.
ms.assetid: 81c203ed-739f-4a06-99a1-9a99c6164edc
title: Безопасное многоадресное программирование (PGM)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce57fcce7bf2faf471604bed97d345971801ca1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105702101"
---
# <a name="reliable-multicast-programming-pgm"></a><span data-ttu-id="10d2d-104">Безопасное многоадресное программирование (PGM)</span><span class="sxs-lookup"><span data-stu-id="10d2d-104">Reliable Multicast Programming (PGM)</span></span>

<span data-ttu-id="10d2d-105">В этом разделе описывается реализация протокола многоадресной рассылки PGM в Windows, которая часто называется надежной многоадресной рассылкой.</span><span class="sxs-lookup"><span data-stu-id="10d2d-105">This section describes the Pragmatic General Multicast (PGM) multicast protocol implementation in Windows, often referred to as reliable multicast.</span></span> <span data-ttu-id="10d2d-106">Надежная многоадресная рассылка реализуется через сокеты Windows в Windows Server 2003 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="10d2d-106">Reliable multicast is implemented through Windows Sockets in Windows Server 2003 and later.</span></span>

<span data-ttu-id="10d2d-107">**Windows XP:** Протокол PGM поддерживается только в том случае, если установлена служба очередей сообщений Майкрософт (MSMQ) 3,0.</span><span class="sxs-lookup"><span data-stu-id="10d2d-107">**Windows XP:** PGM is only supported when Microsoft Message Queuing (MSMQ) 3.0 is installed.</span></span>

<span data-ttu-id="10d2d-108">PGM — это надежный и масштабируемый протокол многоадресной рассылки, позволяющий получателям обнаруживать потери, запрашивать повторную отправку потерянных данных или уведомлять приложение о неустранимой потере.</span><span class="sxs-lookup"><span data-stu-id="10d2d-108">PGM is a reliable and scalable multicast protocol that enables receivers to detect loss, request retransmission of lost data, or notify an application of unrecoverable loss.</span></span> <span data-ttu-id="10d2d-109">PGM — это надежный протокол, который означает, что получатель отвечает за обеспечение получения всех данных, абсолвинг отправителя за получение.</span><span class="sxs-lookup"><span data-stu-id="10d2d-109">PGM is a receiver-reliable protocol, which means the receiver is responsible for ensuring all data is received, absolving the sender of reception responsibility.</span></span>

<span data-ttu-id="10d2d-110">Протокол PGM подходит для приложений, для которых требуется дублирование данных многоадресной рассылки из нескольких источников в несколько получателей.</span><span class="sxs-lookup"><span data-stu-id="10d2d-110">PGM is appropriate for applications that require duplicate-free multicast data delivery from multiple sources to multiple receivers.</span></span> <span data-ttu-id="10d2d-111">Протокол PGM не поддерживает подтвержденную доставку и не гарантирует упорядочивания пакетов от нескольких отправителей.</span><span class="sxs-lookup"><span data-stu-id="10d2d-111">PGM does not support acknowledged delivery, nor does it guarantee ordering of packets from multiple senders.</span></span>

<span data-ttu-id="10d2d-112">Дополнительные сведения о протоколе PGM см. в документе RFC 3208, доступном по адресу [www.IETF.org](https://www.ietf.org/).</span><span class="sxs-lookup"><span data-stu-id="10d2d-112">For more information about PGM, refer to RFC 3208 available at [www.ietf.org](https://www.ietf.org/).</span></span>

<span data-ttu-id="10d2d-113">В этом разделе описывается использование надежной многоадресной рассылки в Windows.</span><span class="sxs-lookup"><span data-stu-id="10d2d-113">This section describes how to use reliable multicast on Windows.</span></span> <span data-ttu-id="10d2d-114">В следующих разделах объясняются различные аспекты создания надежного многоадресного приложения с помощью сокетов Windows.</span><span class="sxs-lookup"><span data-stu-id="10d2d-114">The following topics explain the various aspects of creating a reliable multicast application using Windows Sockets:</span></span>

-   [<span data-ttu-id="10d2d-115">Отправителей и получателей PGM</span><span class="sxs-lookup"><span data-stu-id="10d2d-115">PGM Senders and Receivers</span></span>](pgm-senders-and-receivers.md)
-   [<span data-ttu-id="10d2d-116">Параметры отправителя PGM</span><span class="sxs-lookup"><span data-stu-id="10d2d-116">PGM Sender Options</span></span>](pgm-sender-options.md)
-   [<span data-ttu-id="10d2d-117">Отправка и получение данных PGM</span><span class="sxs-lookup"><span data-stu-id="10d2d-117">Sending and Receiving PGM Data</span></span>](sending-and-receiving-pgm-data.md)
-   [<span data-ttu-id="10d2d-118">Многосайтовое и PGM</span><span class="sxs-lookup"><span data-stu-id="10d2d-118">Multihoming and PGM</span></span>](multihoming-and-pgm.md)
-   [<span data-ttu-id="10d2d-119">Параметры сокета PGM</span><span class="sxs-lookup"><span data-stu-id="10d2d-119">PGM Socket Options</span></span>](pgm-socket-options.md)

 

 



