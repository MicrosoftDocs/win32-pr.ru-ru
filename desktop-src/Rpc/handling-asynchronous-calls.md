---
title: Обработка асинхронных вызовов
description: Подпрограммы диспетчера асинхронной функции всегда получают асинхронный обработчик в качестве первого параметра. Сервер должен отследить этот обработчик и использовать его для отправки ответа при завершении асинхронного вызова удаленной процедуры.
ms.assetid: 4f38b68b-0bea-4fa7-8c7e-dd09e7daf8bf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e04dc7feed0d7bee47f6fa51583cf8de3a8e42f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411061"
---
# <a name="handling-asynchronous-calls"></a><span data-ttu-id="47dda-104">Обработка асинхронных вызовов</span><span class="sxs-lookup"><span data-stu-id="47dda-104">Handling Asynchronous Calls</span></span>

<span data-ttu-id="47dda-105">Подпрограммы диспетчера асинхронной функции всегда получают асинхронный обработчик в качестве первого параметра.</span><span class="sxs-lookup"><span data-stu-id="47dda-105">The manager routine of an asynchronous function always receives the asynchronous handle as the first parameter.</span></span> <span data-ttu-id="47dda-106">Сервер должен отследить этот обработчик и использовать его для отправки ответа при завершении асинхронного вызова удаленной процедуры.</span><span class="sxs-lookup"><span data-stu-id="47dda-106">The server must keep track of this handle and use it to send the reply when the asynchronous remote procedure call finishes.</span></span>

<span data-ttu-id="47dda-107">Если серверу необходимо прервать асинхронную RPC, он вызывает [**рпкасинкаборткалл**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall).</span><span class="sxs-lookup"><span data-stu-id="47dda-107">If the server needs to abort an asynchronous RPC, it calls [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall).</span></span> <span data-ttu-id="47dda-108">Эта функция выполняет ту же очистку на стороне сервера, что и [**рпкасинккомплетекалл**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) , и распространяет код исключения (предоставленный серверным приложением) обратно клиенту, за исключением того, что он не выполняет упаковку аргументов out.</span><span class="sxs-lookup"><span data-stu-id="47dda-108">This function performs the same server-side cleanup as [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) and propagates an exception code (provided by the server application) back to the client, except that it does not perform marshalling of the out arguments.</span></span>

<span data-ttu-id="47dda-109">Пример асинхронной процедуры см. [в разделе Отправка асинхронного ответа](sending-the-asynchronous-reply.md).</span><span class="sxs-lookup"><span data-stu-id="47dda-109">For an example of an asynchronous procedure, see [Sending the Asynchronous Reply](sending-the-asynchronous-reply.md).</span></span>

 

 




