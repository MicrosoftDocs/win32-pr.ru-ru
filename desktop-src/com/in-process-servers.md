---
title: Серверы In-Process
description: Серверы In-Process
ms.assetid: cc0c4350-fa75-4321-834f-711158776cb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4886932b9669aa2d3cdd49979324f9ccc6e03d44
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104253233"
---
# <a name="in-process-servers"></a><span data-ttu-id="55028-103">Серверы In-Process</span><span class="sxs-lookup"><span data-stu-id="55028-103">In-Process Servers</span></span>

<span data-ttu-id="55028-104">При реализации серверного приложения OLE в качестве внутрипроцессного сервера — DLL-библиотека, запущенная в пространстве процесса приложения-контейнера, а не как локальный сервер — EXE-файл, запущенный в собственном пространстве процесса — взаимодействие между контейнером и сервером является упрощенным, так как взаимодействие между ними может быть вызвано обычными вызовами функций.</span><span class="sxs-lookup"><span data-stu-id="55028-104">If you implement an OLE server application as an in-process server — a DLL running in the process space of the container application — rather than as a local server — an EXE running in its own process space — communication between container and server is simplified because communication between the two can take the form of normal function calls.</span></span> <span data-ttu-id="55028-105">Удаленные вызовы процедур не требуются, так как два приложения выполняются в одном пространстве процесса.</span><span class="sxs-lookup"><span data-stu-id="55028-105">Remote procedure calls are not required because the two applications run in the same process space.</span></span> <span data-ttu-id="55028-106">Как и следовало бы, объекты, управляющие упаковкой параметров, также не нужны, хотя они могут быть объединены в библиотеке DLL, не мешая взаимодействию между контейнером и сервером.</span><span class="sxs-lookup"><span data-stu-id="55028-106">As you would expect, the objects that manage the marshaling of parameters are also unnecessary, although they may be aggregated within the DLL without interfering with the communication between container and server.</span></span>

<span data-ttu-id="55028-107">Если серверное приложение OLE реализовано как внутрипроцессный сервер, отдельный обработчик объекта не требуется, так как сам сервер находится в пространстве процесса клиента.</span><span class="sxs-lookup"><span data-stu-id="55028-107">When an OLE server application is implemented as an in-process server, a separate object handler is not required because the server itself lives in the client's process space.</span></span> <span data-ttu-id="55028-108">Основное различие между процессом внутрипроцессного сервера и обработчика объектов заключается в том, что сервер может управлять объектом в состоянии выполнения, пока обработчик не может.</span><span class="sxs-lookup"><span data-stu-id="55028-108">The main difference between an in-process server and object handler is that the server is able to manage the object in a running state while the handler cannot.</span></span> <span data-ttu-id="55028-109">Одним из следствием этого отличия является то, что сервер должен предоставить пользовательский интерфейс для манипуляции с выполняющимся объектом, а обработчик делегирует это требование серверу объекта.</span><span class="sxs-lookup"><span data-stu-id="55028-109">One consequence of this difference is that a server must provide a user interface for manipulating the running object, while a handler delegates this requirement to the object's server.</span></span> <span data-ttu-id="55028-110">При создании внутрипроцессного сервера можно выполнить статистическую обработку в обработчике OLE по умолчанию, позволяя обрабатывать основные рутинные работы, такие как отображение, хранение и уведомления, при этом реализуются только те службы, которые обработчик не предоставляет или не реализует в соответствии с требуемым образом.</span><span class="sxs-lookup"><span data-stu-id="55028-110">In creating an in-process server, you can aggregate on the OLE default handler, letting it handle basic chores, such as display, storage, and notifications while you implement only those services that the handler either does not provide or does not implement in the way you require.</span></span>

<span data-ttu-id="55028-111">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="55028-111">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="55028-112">Преимущества</span><span class="sxs-lookup"><span data-stu-id="55028-112">Advantages</span></span>](advantages.md)
-   [<span data-ttu-id="55028-113">Недостатки</span><span class="sxs-lookup"><span data-stu-id="55028-113">Disadvantages</span></span>](disadvantages.md)

## <a name="related-topics"></a><span data-ttu-id="55028-114">См. также</span><span class="sxs-lookup"><span data-stu-id="55028-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55028-115">Составные документы</span><span class="sxs-lookup"><span data-stu-id="55028-115">Compound Documents</span></span>](compound-documents.md)
</dt> </dl>

 

 




