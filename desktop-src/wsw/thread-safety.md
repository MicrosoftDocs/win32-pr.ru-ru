---
title: Потокобезопасность
description: Все функции в этом API можно вызывать параллельно из разных потоков. Однако каждый объект, переданный в качестве параметра в функции, имеет определенное поведение потоков, как описано ниже.
ms.assetid: 712d6750-884e-421a-8ecf-efcd4ec9b21d
keywords:
- Веб-службы безопасности потоков для Windows
- ввсапи
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fed84cac9634148742c92f1b0d4b4ecdb905ac42
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "103797287"
---
# <a name="thread-safety"></a><span data-ttu-id="98d43-107">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="98d43-107">Thread Safety</span></span>

<span data-ttu-id="98d43-108">Все функции в этом API можно вызывать параллельно из разных потоков.</span><span class="sxs-lookup"><span data-stu-id="98d43-108">All functions in this API are safe to call concurrently from different threads.</span></span> <span data-ttu-id="98d43-109">Однако каждый объект, переданный в качестве параметра в функции, имеет определенное поведение потоков, как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="98d43-109">However, each object passed as a parameter to the functions have specific threading behavior, as described below.</span></span>


<span data-ttu-id="98d43-110">Следующие дескрипторы являются однопотоковыми и не поддерживают параллельные операции для конкретного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="98d43-110">The following handles are single threaded and do not support concurrent operations for a particular instance:</span></span>

-   [<span data-ttu-id="98d43-111">\_куча WS</span><span class="sxs-lookup"><span data-stu-id="98d43-111">WS\_HEAP</span></span>](ws-heap.md)
-   [<span data-ttu-id="98d43-112">\_сообщение WS</span><span class="sxs-lookup"><span data-stu-id="98d43-112">WS\_MESSAGE</span></span>](ws-message.md)
-   [<span data-ttu-id="98d43-113">\_XML- \_ буфер WS</span><span class="sxs-lookup"><span data-stu-id="98d43-113">WS\_XML\_BUFFER</span></span>](ws-xml-buffer.md)
-   [<span data-ttu-id="98d43-114">\_ \_ модуль чтения XML WS</span><span class="sxs-lookup"><span data-stu-id="98d43-114">WS\_XML\_READER</span></span>](ws-xml-reader.md)
-   [<span data-ttu-id="98d43-115">\_ \_ модуль записи XML WS</span><span class="sxs-lookup"><span data-stu-id="98d43-115">WS\_XML\_WRITER</span></span>](ws-xml-writer.md)
-   [<span data-ttu-id="98d43-116">\_Ошибка WS</span><span class="sxs-lookup"><span data-stu-id="98d43-116">WS\_ERROR</span></span>](ws-error.md)
-   [<span data-ttu-id="98d43-117">\_контекст операции \_ WS</span><span class="sxs-lookup"><span data-stu-id="98d43-117">WS\_OPERATION\_CONTEXT</span></span>](ws-operation-context.md)
-   [<span data-ttu-id="98d43-118">\_политика WS</span><span class="sxs-lookup"><span data-stu-id="98d43-118">WS\_POLICY</span></span>](ws-policy.md)
-   [<span data-ttu-id="98d43-119">\_метаданные WS</span><span class="sxs-lookup"><span data-stu-id="98d43-119">WS\_METADATA</span></span>](ws-metadata.md)
-   [<span data-ttu-id="98d43-120">\_токен безопасности \_ WS</span><span class="sxs-lookup"><span data-stu-id="98d43-120">WS\_SECURITY\_TOKEN</span></span>](ws-security-token.md)
-   [<span data-ttu-id="98d43-121">\_контекст безопасности \_ WS</span><span class="sxs-lookup"><span data-stu-id="98d43-121">WS\_SECURITY\_CONTEXT</span></span>](ws-security-context.md)

<span data-ttu-id="98d43-122">Следующие дескрипторы являются свободными потоками и поддерживают параллельные операции для конкретного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="98d43-122">The following handles are free threaded and do support concurrent operations for a particular instance:</span></span>

-   [<span data-ttu-id="98d43-123">\_канал WS</span><span class="sxs-lookup"><span data-stu-id="98d43-123">WS\_CHANNEL</span></span>](ws-channel.md)
-   [<span data-ttu-id="98d43-124">\_прослушиватель WS</span><span class="sxs-lookup"><span data-stu-id="98d43-124">WS\_LISTENER</span></span>](ws-listener.md)
-   [<span data-ttu-id="98d43-125">\_узел службы \_ WS</span><span class="sxs-lookup"><span data-stu-id="98d43-125">WS\_SERVICE\_HOST</span></span>](ws-service-host.md)
-   [<span data-ttu-id="98d43-126">\_ \_ прокси-сервер службы WS</span><span class="sxs-lookup"><span data-stu-id="98d43-126">WS\_SERVICE\_PROXY</span></span>](ws-service-proxy.md)

<span data-ttu-id="98d43-127">Для всех этих дескрипторов определение потоков определяется с точки зрения операций (не вызовов функций).</span><span class="sxs-lookup"><span data-stu-id="98d43-127">For all these handles, threading is defined in terms of operations (not function calls).</span></span> <span data-ttu-id="98d43-128">Операция определена по-разному для функций, синхронно вызванных по сравнению с функциями, которые вызываются асинхронно:</span><span class="sxs-lookup"><span data-stu-id="98d43-128">An operation is defined differently for functions invoked synchronously versus functions invoked asynchronously:</span></span>

-   <span data-ttu-id="98d43-129">Для функций, вызванных синхронно, операция находится в состоянии ожидания во время выполнения функции.</span><span class="sxs-lookup"><span data-stu-id="98d43-129">For functions invoked synchronously, the operation is pending during the execution of the function.</span></span>
-   <span data-ttu-id="98d43-130">Для функций, вызываемых асинхронно, если функция возвращает код возврата, отличный **от \_ WS \_ S** , то ожидание операции во время выполнения функции.</span><span class="sxs-lookup"><span data-stu-id="98d43-130">For functions invoked asynchronously, if the function returns a return code other than **WS\_S\_ASYNC** the operation is pending during the execution of the function.</span></span> <span data-ttu-id="98d43-131">Однако, если функция возвращает **WS \_ S \_ асинхронно** , операция ожидает, пока не будет [**вызван \_ асинхронный \_ обратный вызов WS**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback) .</span><span class="sxs-lookup"><span data-stu-id="98d43-131">If the function returns **WS\_S\_ASYNC** , however, the operation is pending until the [**WS\_ASYNC\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback) is invoked.</span></span> <span data-ttu-id="98d43-132">Дополнительные сведения о асинхронном вызове функций см. в разделе [асинхронная модель](asynchronous-model.md) .</span><span class="sxs-lookup"><span data-stu-id="98d43-132">For more information about invoking functions asynchronously, see the [Asynchronous Model](asynchronous-model.md) topic.</span></span> <span data-ttu-id="98d43-133">Коды ошибок см. в статье [возвращаемые значения веб-служб Windows](windows-web-services-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="98d43-133">For error codes, see [Windows Web Services Return Values](windows-web-services-return-values.md).</span></span>

<span data-ttu-id="98d43-134">Несоблюдение контракта потоковой обработки для объекта приведет к неопределенному поведению.</span><span class="sxs-lookup"><span data-stu-id="98d43-134">Failure to follow the threading contract for an object will result in undefined behavior.</span></span>

 

 




