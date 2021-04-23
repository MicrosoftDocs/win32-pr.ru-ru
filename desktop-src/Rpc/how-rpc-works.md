---
title: Как работает RPC
description: Средства удаленного вызова процедур делают его пользователям, как будто клиент напрямую вызывает процедуру, расположенную в удаленной серверной программе.
ms.assetid: 265f31b8-9a41-4255-b070-fd50b00b935b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12832d0de4eb972bb1d9d51df0c871191d4d079a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777369"
---
# <a name="how-rpc-works"></a><span data-ttu-id="3aa00-103">Как работает RPC</span><span class="sxs-lookup"><span data-stu-id="3aa00-103">How RPC Works</span></span>

<span data-ttu-id="3aa00-104">Средства удаленного вызова процедур делают его пользователям, как будто клиент напрямую вызывает процедуру, расположенную в удаленной серверной программе.</span><span class="sxs-lookup"><span data-stu-id="3aa00-104">The RPC tools make it appear to users as though a client directly calls a procedure located in a remote server program.</span></span> <span data-ttu-id="3aa00-105">У каждого клиента и сервера есть свои адресные пространства; то есть каждый из них имеет свой собственный ресурс памяти, выделенный для данных, используемых процедурой.</span><span class="sxs-lookup"><span data-stu-id="3aa00-105">The client and server each have their own address spaces; that is, each has its own memory resource allocated to data used by the procedure.</span></span> <span data-ttu-id="3aa00-106">На следующем рисунке показана архитектура RPC.</span><span class="sxs-lookup"><span data-stu-id="3aa00-106">The following figure illustrates the RPC architecture.</span></span>

![Архитектура RPC](images/prog-a11.png)

<span data-ttu-id="3aa00-108">Как показано на рисунке, клиентское приложение вызывает локальную процедуру-заглушку вместо фактического кода, реализующего процедуру.</span><span class="sxs-lookup"><span data-stu-id="3aa00-108">As the illustration shows, the client application calls a local stub procedure instead of the actual code implementing the procedure.</span></span> <span data-ttu-id="3aa00-109">Заглушки компилируются и связываются с клиентским приложением.</span><span class="sxs-lookup"><span data-stu-id="3aa00-109">Stubs are compiled and linked with the client application.</span></span> <span data-ttu-id="3aa00-110">Вместо того, чтобы содержать фактический код, реализующий удаленную процедуру, код заглушки клиента:</span><span class="sxs-lookup"><span data-stu-id="3aa00-110">Instead of containing the actual code that implements the remote procedure, the client stub code:</span></span>

-   <span data-ttu-id="3aa00-111">Извлекает необходимые параметры из адресного пространства клиента.</span><span class="sxs-lookup"><span data-stu-id="3aa00-111">Retrieves the required parameters from the client address space.</span></span>
-   <span data-ttu-id="3aa00-112">Преобразует необходимые параметры в стандартный формат NDR для передачи по сети.</span><span class="sxs-lookup"><span data-stu-id="3aa00-112">Translates the parameters as needed into a standard NDR format for transmission over the network.</span></span>
-   <span data-ttu-id="3aa00-113">Вызывает функции в клиентской библиотеке времени выполнения RPC для отправки запроса и его параметров на сервер.</span><span class="sxs-lookup"><span data-stu-id="3aa00-113">Calls functions in the RPC client run-time library to send the request and its parameters to the server.</span></span>

<span data-ttu-id="3aa00-114">Для вызова удаленной процедуры сервер выполняет следующие действия.</span><span class="sxs-lookup"><span data-stu-id="3aa00-114">The server performs the following steps to call the remote procedure.</span></span>

1.  <span data-ttu-id="3aa00-115">Функции библиотеки времени выполнения RPC сервера принимают запрос и вызывают процедуру заглушки сервера.</span><span class="sxs-lookup"><span data-stu-id="3aa00-115">The server RPC run-time library functions accept the request and call the server stub procedure.</span></span>
2.  <span data-ttu-id="3aa00-116">Заглушка сервера извлекает параметры из сетевого буфера и преобразует их из формата передачи сети в формат, который требуется серверу.</span><span class="sxs-lookup"><span data-stu-id="3aa00-116">The server stub retrieves the parameters from the network buffer and converts them from the network transmission format to the format the server needs.</span></span>
3.  <span data-ttu-id="3aa00-117">Заглушка сервера вызывает фактическую процедуру на сервере.</span><span class="sxs-lookup"><span data-stu-id="3aa00-117">The server stub calls the actual procedure on the server.</span></span>

<span data-ttu-id="3aa00-118">Затем выполняется удаленная процедура, которая, возможно, создает выходные параметры и возвращаемое значение.</span><span class="sxs-lookup"><span data-stu-id="3aa00-118">The remote procedure then runs, possibly generating output parameters and a return value.</span></span> <span data-ttu-id="3aa00-119">После завершения удаленной процедуры аналогичная последовательность действий возвращает клиенту данные.</span><span class="sxs-lookup"><span data-stu-id="3aa00-119">When the remote procedure is complete, a similar sequence of steps returns the data to the client.</span></span>

1.  <span data-ttu-id="3aa00-120">Удаленная процедура возвращает свои данные в заглушку сервера.</span><span class="sxs-lookup"><span data-stu-id="3aa00-120">The remote procedure returns its data to the server stub.</span></span>
2.  <span data-ttu-id="3aa00-121">Заглушка сервера преобразует выходные параметры в формат, необходимый для передачи по сети, и возвращает их в функции библиотеки времени выполнения RPC.</span><span class="sxs-lookup"><span data-stu-id="3aa00-121">The server stub converts output parameters to the format required for transmission over the network and returns them to the RPC run-time library functions.</span></span>
3.  <span data-ttu-id="3aa00-122">Функции библиотеки времени выполнения RPC сервера передают данные в сети клиентскому компьютеру.</span><span class="sxs-lookup"><span data-stu-id="3aa00-122">The server RPC run-time library functions transmit the data on the network to the client computer.</span></span>

<span data-ttu-id="3aa00-123">Клиент завершает процесс, принимая данные по сети и возвращая их вызывающей функции.</span><span class="sxs-lookup"><span data-stu-id="3aa00-123">The client completes the process by accepting the data over the network and returning it to the calling function.</span></span>

1.  <span data-ttu-id="3aa00-124">Библиотека времени выполнения RPC клиента получает возвращаемые из удаленной процедуры значения и возвращает их в клиентскую заглушку.</span><span class="sxs-lookup"><span data-stu-id="3aa00-124">The client RPC run-time library receives the remote-procedure return values and returns them to the client stub.</span></span>
2.  <span data-ttu-id="3aa00-125">Клиентская заглушка преобразует данные из отчета о недоставке в формат, используемый клиентским компьютером.</span><span class="sxs-lookup"><span data-stu-id="3aa00-125">The client stub converts the data from its NDR to the format used by the client computer.</span></span> <span data-ttu-id="3aa00-126">Заглушка записывает данные в память клиента и возвращает результат вызывающей программе на клиенте.</span><span class="sxs-lookup"><span data-stu-id="3aa00-126">The stub writes data into the client memory and returns the result to the calling program on the client.</span></span>
3.  <span data-ttu-id="3aa00-127">Вызывающая процедура продолжится, как если бы процедура была вызвана на том же компьютере.</span><span class="sxs-lookup"><span data-stu-id="3aa00-127">The calling procedure continues as if the procedure had been called on the same computer.</span></span>

<span data-ttu-id="3aa00-128">Библиотеки времени выполнения предоставляются в двух частях: библиотеку импорта, которая связана с приложением и библиотекой времени выполнения RPC, которая реализована как библиотека динамической компоновки (DLL).</span><span class="sxs-lookup"><span data-stu-id="3aa00-128">The run-time libraries are provided in two parts: an import library, which is linked with the application and the RPC run-time library, which is implemented as a dynamic-link library (DLL).</span></span>

<span data-ttu-id="3aa00-129">Серверное приложение содержит вызовы функций библиотеки времени выполнения сервера, которые регистрируют интерфейс сервера и позволяют серверу принимать удаленные вызовы процедур.</span><span class="sxs-lookup"><span data-stu-id="3aa00-129">The server application contains calls to the server run-time library functions which register the server's interface and allow the server to accept remote procedure calls.</span></span> <span data-ttu-id="3aa00-130">Серверное приложение также содержит удаленные процедуры, связанные с конкретным приложением, которые вызываются клиентскими приложениями.</span><span class="sxs-lookup"><span data-stu-id="3aa00-130">The server application also contains the application-specific remote procedures that are called by the client applications.</span></span>

 

 




