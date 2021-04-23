---
title: Как сервер готовится к подключению
description: Когда серверная программа начинает выполнение, она должна сначала зарегистрировать интерфейс или интерфейсы, которые он содержит, в библиотеке времени выполнения RPC.
ms.assetid: 3e78e095-f4a4-4ce7-b4a9-936a6c10316b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9787cc0f4a10da99f1401843450a6e00073e135b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330624"
---
# <a name="how-the-server-prepares-for-a-connection"></a><span data-ttu-id="7e5b1-103">Как сервер готовится к подключению</span><span class="sxs-lookup"><span data-stu-id="7e5b1-103">How the Server Prepares for a Connection</span></span>

<span data-ttu-id="7e5b1-104">Когда серверная программа начинает выполнение, она должна сначала зарегистрировать интерфейс или интерфейсы, которые он содержит, в библиотеке времени выполнения RPC.</span><span class="sxs-lookup"><span data-stu-id="7e5b1-104">When a server program begins execution, it must first register the interface or interfaces it contains with the RPC run-time library.</span></span> <span data-ttu-id="7e5b1-105">Затем он создает необходимые сведения о привязке.</span><span class="sxs-lookup"><span data-stu-id="7e5b1-105">It then creates the necessary binding information.</span></span> <span data-ttu-id="7e5b1-106">Серверная программа также должна зарегистрировать конечную точку или конечные точки, которые он прослушивает.</span><span class="sxs-lookup"><span data-stu-id="7e5b1-106">The server program must also register the endpoint or endpoints it listens to.</span></span> <span data-ttu-id="7e5b1-107">Затем он может начать прослушивание клиентских вызовов.</span><span class="sxs-lookup"><span data-stu-id="7e5b1-107">It can then begin listening for client calls.</span></span> <span data-ttu-id="7e5b1-108">Этот процесс показан на следующей схеме.</span><span class="sxs-lookup"><span data-stu-id="7e5b1-108">This process is illustrated in the following diagram.</span></span>

![серверное приложение RPC подготавливается к подключениям клиентов](images/srvrcon.png)

<span data-ttu-id="7e5b1-110">В зависимости от выбранной структуры, серверное приложение может выбрать другой набор действий. в предыдущем примере и иллюстрации представлен один из способов.</span><span class="sxs-lookup"><span data-stu-id="7e5b1-110">Depending on the design chosen, a server application may choose a different set of steps; the previous example and illustration provides one approach.</span></span>

<span data-ttu-id="7e5b1-111">В этом разделе представлены сведения о шагах, которые должен выполнить серверный процесс для подготовки к подключению.</span><span class="sxs-lookup"><span data-stu-id="7e5b1-111">This section presents information on the steps that a server process must take to prepare for a connection.</span></span> <span data-ttu-id="7e5b1-112">Обсуждение состоит из следующих разделов:</span><span class="sxs-lookup"><span data-stu-id="7e5b1-112">The discussion is divided into the following sections:</span></span>

-   [<span data-ttu-id="7e5b1-113">Регистрация интерфейса</span><span class="sxs-lookup"><span data-stu-id="7e5b1-113">Registering the Interface</span></span>](registering-the-interface.md)
-   [<span data-ttu-id="7e5b1-114">Обеспечение доступности сервера в сети</span><span class="sxs-lookup"><span data-stu-id="7e5b1-114">Making the Server Available on the Network</span></span>](making-the-server-available-on-the-network.md)
-   [<span data-ttu-id="7e5b1-115">Регистрация конечных точек</span><span class="sxs-lookup"><span data-stu-id="7e5b1-115">Registering Endpoints</span></span>](registering-endpoints.md)
-   [<span data-ttu-id="7e5b1-116">Ожидание вызовов клиента</span><span class="sxs-lookup"><span data-stu-id="7e5b1-116">Listening for Client Calls</span></span>](listening-for-client-calls.md)

 

 




