---
title: Общая процедура сборки
description: Страница навигации для процесса создания клиентского или серверного приложения с помощью удаленного вызова процедур (RPC).
ms.assetid: 77fa9f30-c370-4ec2-8c23-6037ec520dc3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b223bf7482cd7cbb65f5b737c90502a6b6dd3de
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067849"
---
# <a name="general-build-procedure"></a><span data-ttu-id="2ba2a-103">Общая процедура сборки</span><span class="sxs-lookup"><span data-stu-id="2ba2a-103">General Build Procedure</span></span>

<span data-ttu-id="2ba2a-104">Процесс создания клиентского или серверного приложения с помощью Microsoft RPC:</span><span class="sxs-lookup"><span data-stu-id="2ba2a-104">The process for creating a client/server application using Microsoft RPC is:</span></span>

-   <span data-ttu-id="2ba2a-105">Разработка интерфейса.</span><span class="sxs-lookup"><span data-stu-id="2ba2a-105">Develop the interface.</span></span>
-   <span data-ttu-id="2ba2a-106">Разработка сервера, реализующего интерфейс.</span><span class="sxs-lookup"><span data-stu-id="2ba2a-106">Develop the server that implements the interface.</span></span>
-   <span data-ttu-id="2ba2a-107">Разработка клиента, использующего интерфейс.</span><span class="sxs-lookup"><span data-stu-id="2ba2a-107">Develop the client that uses the interface.</span></span>

<span data-ttu-id="2ba2a-108">Эти шаги показаны на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="2ba2a-108">The following figure illustrates these steps.</span></span>

![процесс создания приложения "клиент-сервер" с помощью Microsoft RPC](images/appdev.png)

<span data-ttu-id="2ba2a-110">Можно и часто разрабатывать клиентские и серверные приложения параллельно.</span><span class="sxs-lookup"><span data-stu-id="2ba2a-110">It is feasible and common to develop the client and server applications concurrently.</span></span> <span data-ttu-id="2ba2a-111">Так как клиент и серверные программы зависят от интерфейса, интерфейс между ними должен быть разработан до разработки клиента и сервера, как показано на предыдущей схеме.</span><span class="sxs-lookup"><span data-stu-id="2ba2a-111">Since both the client and server programs are dependent on the interface, however, the interface between them must be developed before the client and server are developed, as shown in the preceding diagram.</span></span>

<span data-ttu-id="2ba2a-112">В этом разделе обсуждаются шаги, необходимые для создания приложения клиента/сервера с помощью RPC.</span><span class="sxs-lookup"><span data-stu-id="2ba2a-112">This section discusses the steps required for building a client/server application with RPC.</span></span> <span data-ttu-id="2ba2a-113">Сведения представлены в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="2ba2a-113">The information is presented in the following topics:</span></span>

-   [<span data-ttu-id="2ba2a-114">Разработка интерфейса</span><span class="sxs-lookup"><span data-stu-id="2ba2a-114">Developing the Interface</span></span>](developing-the-interface.md)
-   [<span data-ttu-id="2ba2a-115">Разработка сервера</span><span class="sxs-lookup"><span data-stu-id="2ba2a-115">Developing the Server</span></span>](developing-the-server.md)
-   [<span data-ttu-id="2ba2a-116">Разработка клиента</span><span class="sxs-lookup"><span data-stu-id="2ba2a-116">Developing the Client</span></span>](developing-the-client.md)

 

 




