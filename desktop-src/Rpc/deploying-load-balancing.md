---
title: Развертывание балансировки нагрузки
description: Развертывание балансировки нагрузки
ms.assetid: d80b8999-16c9-4fc8-a1cb-35a65f434884
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc00430e8e93334c04dc74c57fc8b50db7d3c899
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104253064"
---
# <a name="deploying-load-balancing"></a><span data-ttu-id="d839e-103">Развертывание балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="d839e-103">Deploying Load Balancing</span></span>

<span data-ttu-id="d839e-104">Ниже показана типичная среда развертывания и вариант использования, в которых используется балансировщик нагрузки RPC.</span><span class="sxs-lookup"><span data-stu-id="d839e-104">The typical deployment environment and use case is which the RPC Load balancer is utilized is shown below:</span></span>![Балансировка нагрузки RPC](images/rpc-load-balancing.png)

1.  <span data-ttu-id="d839e-106">RPC-клиент выполняет подключение RPC/HTTP к ферме серверов.</span><span class="sxs-lookup"><span data-stu-id="d839e-106">The RPC client makes an RPC/HTTP connection to the server farm.</span></span>
2.  <span data-ttu-id="d839e-107">Подключение перенаправляется по сети в балансировщик нагрузки внешнего интерфейса</span><span class="sxs-lookup"><span data-stu-id="d839e-107">The connection is forwarded through the network to a front end load balancer</span></span>
3.  <span data-ttu-id="d839e-108">Подсистема балансировки нагрузки внешнего интерфейса выбирает сервер для обслуживания запроса.</span><span class="sxs-lookup"><span data-stu-id="d839e-108">The front end load balancer chooses a server to service the request.</span></span> <span data-ttu-id="d839e-109">В этом примере балансировщик нагрузки внешнего интерфейса перенаправляет соединение на сервер 1.</span><span class="sxs-lookup"><span data-stu-id="d839e-109">In this example, the front end load balancer forwards the connection to Server 1.</span></span>
4.  <span data-ttu-id="d839e-110">Служба балансировщика нагрузки RPC единолично соединение.</span><span class="sxs-lookup"><span data-stu-id="d839e-110">The RPC Load balancer service arbitrates the connection.</span></span> <span data-ttu-id="d839e-111">Он определяет, что это первое подключение клиента, и связывает соединение с локальным сервером, сервером 1.</span><span class="sxs-lookup"><span data-stu-id="d839e-111">It determines that this is the first connection from the client and associates the connection with the local server, Server 1.</span></span>
5.  <span data-ttu-id="d839e-112">Клиент выполняет второй запрос RPC/HTTP.</span><span class="sxs-lookup"><span data-stu-id="d839e-112">The client makes a second RPC/HTTP request.</span></span>
6.  <span data-ttu-id="d839e-113">Запрос перенаправляется по сети в балансировщик нагрузки переднего плана.</span><span class="sxs-lookup"><span data-stu-id="d839e-113">The request is forwarded through the network to the front end load balancer.</span></span>
7.  <span data-ttu-id="d839e-114">Подсистема балансировки нагрузки внешнего интерфейса выбирает сервер для обслуживания запроса.</span><span class="sxs-lookup"><span data-stu-id="d839e-114">The front end load balancer chooses a server to service the request.</span></span> <span data-ttu-id="d839e-115">В этом случае балансировщик нагрузки внешнего интерфейса выбирает сервер 2 для обслуживания запроса.</span><span class="sxs-lookup"><span data-stu-id="d839e-115">In this case, the front end load balancer chooses Server 2 to service the request.</span></span>
8.  <span data-ttu-id="d839e-116">Служба RPC Load Balancer, единолично соединение.</span><span class="sxs-lookup"><span data-stu-id="d839e-116">The RPC Load Balancer service arbitrates the connection.</span></span> <span data-ttu-id="d839e-117">Он определяет, что подключения от этого клиента обслуживаются сервером 1.</span><span class="sxs-lookup"><span data-stu-id="d839e-117">It recognizes that connections from this client is being serviced by Server 1.</span></span>
9.  <span data-ttu-id="d839e-118">Соединение перенаправляется на сервер 1.</span><span class="sxs-lookup"><span data-stu-id="d839e-118">The connection is forwarded to Server 1.</span></span>

 

 




