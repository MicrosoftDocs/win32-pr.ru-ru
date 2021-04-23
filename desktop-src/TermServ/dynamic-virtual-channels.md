---
title: Динамические виртуальные каналы
description: Динамические API виртуальных каналов (DVC) расширяют существующие API виртуальных каналов для службы удаленных рабочих столов, называемых статическими интерфейсами API виртуального канала (SVC).
ms.assetid: bddf0048-482d-40f3-a973-9d7bc15be8fa
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe3181c0960b50289846018c3ace773a8351cb20
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410905"
---
# <a name="dynamic-virtual-channels"></a><span data-ttu-id="cbaa9-103">Динамические виртуальные каналы</span><span class="sxs-lookup"><span data-stu-id="cbaa9-103">Dynamic Virtual Channels</span></span>

<span data-ttu-id="cbaa9-104">Динамические API виртуальных каналов (DVC) расширяют существующие API виртуальных каналов для службы удаленных рабочих столов, называемых статическими интерфейсами API виртуального канала (SVC).</span><span class="sxs-lookup"><span data-stu-id="cbaa9-104">Dynamic virtual channel (DVC) APIs extend the existing virtual channel APIs for Remote Desktop Services, known as static virtual channel (SVC) APIs.</span></span> <span data-ttu-id="cbaa9-105">API-интерфейсы DVC разлагаются на несколько ограничений, существовавших в интерфейсах API SVC между клиентом и сервером, например:</span><span class="sxs-lookup"><span data-stu-id="cbaa9-105">DVC APIs address several limitations that existed in SVC APIs between the client and server, such as:</span></span>

-   <span data-ttu-id="cbaa9-106">Ограниченное число каналов</span><span class="sxs-lookup"><span data-stu-id="cbaa9-106">A limited number of channels</span></span>
-   <span data-ttu-id="cbaa9-107">Реконструкция пакетов</span><span class="sxs-lookup"><span data-stu-id="cbaa9-107">Packet reconstruction</span></span>

<span data-ttu-id="cbaa9-108">API-интерфейсы DVC позволяют реализовать модули на стороне сервера и клиента службы удаленных рабочих столов соединения, взаимодействующие друг с другом.</span><span class="sxs-lookup"><span data-stu-id="cbaa9-108">DVC APIs will help you to implement modules on the server and client side of a Remote Desktop Services connection that communicate with each other.</span></span>

<span data-ttu-id="cbaa9-109">Как и многие другие архитектурные клиентские и серверные архитектуры, соединение устанавливается на основе наиболее согласованного фрагмента данных, называемого конечной точкой.</span><span class="sxs-lookup"><span data-stu-id="cbaa9-109">Like many other client/server architectures, a connection is established based on a commonly agreed upon piece of data, referred to as an endpoint.</span></span> <span data-ttu-id="cbaa9-110">Аналогичным примером является TCP/IP, где конечная точка устанавливается через сочетание IP-адреса сервера и имени порта.</span><span class="sxs-lookup"><span data-stu-id="cbaa9-110">A similar example is TCP/IP, where an endpoint is established through a combination of server IP address and the port name.</span></span> <span data-ttu-id="cbaa9-111">Еще один пример — именованные каналы, где конечная точка — это сочетание имени сервера и имени канала.</span><span class="sxs-lookup"><span data-stu-id="cbaa9-111">Another example is named pipes, where an endpoint is a combination of the server name and the pipe name.</span></span> <span data-ttu-id="cbaa9-112">В службы удаленных рабочих столов подключении существует только две стороны.</span><span class="sxs-lookup"><span data-stu-id="cbaa9-112">In a Remote Desktop Services connection there are only two sides involved.</span></span> <span data-ttu-id="cbaa9-113">Таким образом, конечная точка состоит из простой произвольной строки, однозначно идентифицирующей соединение.</span><span class="sxs-lookup"><span data-stu-id="cbaa9-113">Therefore, the endpoint consists of a simple arbitrary string that uniquely identifies the connection.</span></span> <span data-ttu-id="cbaa9-114">Подобно TCP/IP и именованным каналам, несколько подключений могут инициироваться с одного имени конечной точки.</span><span class="sxs-lookup"><span data-stu-id="cbaa9-114">Much like TCP/IP and named pipes, multiple connections can initiate from the same endpoint name.</span></span> <span data-ttu-id="cbaa9-115">В этом смысле у подключений нет имен; просто прослушиватель, ожидающий входящие запросы к конечной точке.</span><span class="sxs-lookup"><span data-stu-id="cbaa9-115">In that sense, connections do not have names; just a listener that waits for incoming requests on the endpoint.</span></span>

<span data-ttu-id="cbaa9-116">API-интерфейсы DVC состоят из следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="cbaa9-116">The DVC APIs consist of the following:</span></span>

-   <span data-ttu-id="cbaa9-117">Интерфейсы API клиента</span><span class="sxs-lookup"><span data-stu-id="cbaa9-117">Client APIs</span></span>

    <span data-ttu-id="cbaa9-118">Эти API-интерфейсы доступны в клиенте подключение к удаленному рабочему столу (RDC) в качестве подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="cbaa9-118">These APIs are available in the Remote Desktop Connection (RDC) client as a plug-in.</span></span> <span data-ttu-id="cbaa9-119">Клиент находится в пассивном режиме, где он прослушивает входящие подключения, но не устанавливает активное соединение.</span><span class="sxs-lookup"><span data-stu-id="cbaa9-119">The client side is in passive mode, where it listens for incoming connections but does not actively establish a connection.</span></span>

-   <span data-ttu-id="cbaa9-120">Серверные API</span><span class="sxs-lookup"><span data-stu-id="cbaa9-120">Server APIs</span></span>

    <span data-ttu-id="cbaa9-121">Эти API активно инициируют подключение.</span><span class="sxs-lookup"><span data-stu-id="cbaa9-121">These APIs actively initiate the connection.</span></span>

<span data-ttu-id="cbaa9-122">Сведения о том, как написать динамический виртуальный канал (DVC), см. в разделе [сведения о реализации DVC](dvc-implementation-details.md).</span><span class="sxs-lookup"><span data-stu-id="cbaa9-122">For information about how to write a dynamic virtual channel (DVC) module, see [DVC Implementation Details](dvc-implementation-details.md).</span></span>

 

 




