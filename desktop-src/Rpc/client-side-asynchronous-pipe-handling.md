---
title: Асинхронная обработка канала на стороне клиента
description: Перед выполнением асинхронного удаленного вызова клиент должен сначала инициализировать асинхронный обработчик.
ms.assetid: 3d54b233-d8b0-45d1-b759-0d2d24c1e247
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11ff503f80c77b2403d683c2b644d89836365956
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888923"
---
# <a name="client-side-asynchronous-pipe-handling"></a><span data-ttu-id="b6e33-103">Асинхронная обработка канала на стороне клиента</span><span class="sxs-lookup"><span data-stu-id="b6e33-103">Client-side Asynchronous Pipe Handling</span></span>

<span data-ttu-id="b6e33-104">Перед выполнением асинхронного удаленного вызова клиент должен сначала инициализировать асинхронный обработчик.</span><span class="sxs-lookup"><span data-stu-id="b6e33-104">Before making an asynchronous remote call, the client must first initialize the asynchronous handle.</span></span> <span data-ttu-id="b6e33-105">Как и в случае с неконвейерными процедурами, клиент вызывает асинхронную функцию с асинхронным маркером в качестве первого параметра и использует асинхронный обработчик для отправки и получения данных канала, запроса состояния вызова и получения ответа.</span><span class="sxs-lookup"><span data-stu-id="b6e33-105">As with nonpipe procedures, the client calls an asynchronous function with the asynchronous handle as the first parameter and uses the asynchronous handle to send and receive pipe data, query the status of the call, and receive the reply.</span></span>

<span data-ttu-id="b6e33-106">Клиент выполняет асинхронный вызов удаленной процедуры с асинхронным маркером в качестве первого параметра.</span><span class="sxs-lookup"><span data-stu-id="b6e33-106">The client makes the asynchronous remote procedure call with the asynchronous handle as the first parameter.</span></span> <span data-ttu-id="b6e33-107">Клиент может использовать этот обработчик для запроса состояния вызова и получения ответа.</span><span class="sxs-lookup"><span data-stu-id="b6e33-107">The client can use this handle to query the status of the call and to receive the reply.</span></span> <span data-ttu-id="b6e33-108">Модель асинхронных каналов является симметричной.</span><span class="sxs-lookup"><span data-stu-id="b6e33-108">The asynchronous pipe model is symmetric.</span></span> <span data-ttu-id="b6e33-109">Клиентские и серверные приложения отправляют и получают данные канала активно (в отличие от синхронного RPC, в котором данные канала отправляются и получаются в пассивном режиме).</span><span class="sxs-lookup"><span data-stu-id="b6e33-109">Both client and server applications send and receive pipe data actively (as opposed to synchronous RPC, where the pipe data is sent and received passively).</span></span>

<span data-ttu-id="b6e33-110">Клиент отправляет асинхронные данные канала, вызывая функцию **Push** в соответствующем асинхронном канале с переменной состояния канала в качестве первого параметра.</span><span class="sxs-lookup"><span data-stu-id="b6e33-110">The client sends asynchronous pipe data by calling the **push** function on the appropriate asynchronous pipe, with the pipe's state variable as the first parameter.</span></span> <span data-ttu-id="b6e33-111">Когда функция **Push** возвращает, клиент может изменить или освободить буфер отправки.</span><span class="sxs-lookup"><span data-stu-id="b6e33-111">When the **push** function returns, the client can modify or free the send buffer.</span></span>

<span data-ttu-id="b6e33-112">Если в \_ \_ \_ \_ \_ асинхронном обработчике установлен флаг RPC Async notify for Send Complete, и если в качестве механизма уведомления используются APC, то протокол APC помещается в очередь при завершении отправки канала.</span><span class="sxs-lookup"><span data-stu-id="b6e33-112">If the RPC\_ASYNC\_NOTIFY\_ON\_SEND\_COMPLETE flag is set in the asynchronous handle, and if APCs are used as the notification mechanism, an APC is queued when the pipe send is actually complete.</span></span> <span data-ttu-id="b6e33-113">Можно воспользоваться преимуществами этого механизма для реализации управления потоком.</span><span class="sxs-lookup"><span data-stu-id="b6e33-113">You can take advantage of this mechanism to implement flow control.</span></span> <span data-ttu-id="b6e33-114">Однако обратите внимание, что если клиент отправляет другой буфер до завершения предыдущей отправки, клиент может, в зависимости от скорости операции передачи, получать только одно уведомление об отправке, а не одно уведомление для каждого буфера или операции **принудительной** отправки.</span><span class="sxs-lookup"><span data-stu-id="b6e33-114">Note, however, that if the client pushes another buffer before the previous push is complete, the client may, depending on the speed of the transfer operation, receive only one send-complete notification, rather than one notification for each buffer or each **push** operation.</span></span> <span data-ttu-id="b6e33-115">Когда клиент отправил все данные канала, он выполняет один окончательный вызов **Push** с числом элементов, равным 0.</span><span class="sxs-lookup"><span data-stu-id="b6e33-115">When the client has sent all of the pipe data, it makes one final **push** call with the number of elements set to 0.</span></span>

<span data-ttu-id="b6e33-116">Клиентская программа получает асинхронные данные канала, вызывая функцию **Pull** в соответствующем асинхронном канале с переменной состояния канала в качестве первого параметра.</span><span class="sxs-lookup"><span data-stu-id="b6e33-116">The client program receives asynchronous pipe data by calling the **pull** function on the appropriate asynchronous pipe, with the pipe's state variable as the first parameter.</span></span> <span data-ttu-id="b6e33-117">Если данные канала недоступны, функция **Pull** возвращает \_ \_ \_ ожидающий асинхронный вызов RPC S \_ .</span><span class="sxs-lookup"><span data-stu-id="b6e33-117">If no pipe data is available, the **pull** function returns RPC\_S\_ASYNC\_CALL\_PENDING.</span></span>

<span data-ttu-id="b6e33-118">Если механизм уведомления имеет значение APC и сервер вернул \_ \_ асинхронный вызов RPC S \_ \_ , клиент должен дождаться получения **рпкрецеивекомплете** APC из среды выполнения перед повторным вызовом **Pull** .</span><span class="sxs-lookup"><span data-stu-id="b6e33-118">If the notification mechanism is APC, and the server returned RPC\_S\_ASYNC\_CALL\_PENDING, the client must wait until it receives the **RpcReceiveComplete** APC from run-time before calling **pull** again.</span></span>

 

 




