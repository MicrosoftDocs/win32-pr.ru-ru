---
title: Получение асинхронного ответа
description: После получения уведомления о том, что сервер отправил ответ, клиент вызывает Рпкасинккомплетекалл с асинхронным обработчиком, чтобы он мог получить ответ.
ms.assetid: 48fb3777-d90a-474b-a1fa-9d034b5791e5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9143daaf1f276f784086e2ec17efb47dfd1fb6e4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413538"
---
# <a name="receiving-the-asynchronous-reply"></a><span data-ttu-id="46340-103">Получение асинхронного ответа</span><span class="sxs-lookup"><span data-stu-id="46340-103">Receiving the Asynchronous Reply</span></span>

<span data-ttu-id="46340-104">После получения уведомления о том, что сервер отправил ответ, клиент вызывает [**рпкасинккомплетекалл**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) с асинхронным обработчиком, чтобы он мог получить ответ.</span><span class="sxs-lookup"><span data-stu-id="46340-104">After it is notified that the server has sent a reply, the client calls [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) with the asynchronous handle so that it can receive the reply.</span></span> <span data-ttu-id="46340-105">После успешного завершения **рпкасинккомплетекалл** параметр *Reply* указывает на буфер, содержащий возвращаемое значение удаленной функции.</span><span class="sxs-lookup"><span data-stu-id="46340-105">When **RpcAsyncCompleteCall** has completed successfully, the *Reply* parameter points to a buffer that contains the return value of the remote function.</span></span> <span data-ttu-id="46340-106">Любые буферы, предоставляемые клиентской программой как \[ [**out**](/windows/desktop/Midl/out-idl) \] или \[ [**in**](/windows/desktop/Midl/in), параметры **out** \] для асинхронной удаленной функции содержат допустимые данные.</span><span class="sxs-lookup"><span data-stu-id="46340-106">Any buffers supplied by the client program as \[[**out**](/windows/desktop/Midl/out-idl)\] or \[[**in**](/windows/desktop/Midl/in), **out**\] parameters to the asynchronous remote function contain valid data.</span></span> <span data-ttu-id="46340-107">Если клиент вызывает **рпкасинккомплетекалл** до того, как сервер отправил ответ, этот вызов завершится ошибкой и возвратит значение \_ \_ \_ ожидающего асинхронного вызова RPC S \_ .</span><span class="sxs-lookup"><span data-stu-id="46340-107">If the client calls **RpcAsyncCompleteCall** before the server has sent the reply, that call will fail and return a value of RPC\_S\_ASYNC\_CALL\_PENDING.</span></span>

<span data-ttu-id="46340-108">Если клиентская программа использует порты завершения ввода-вывода или события для уведомления, она должна вызвать функцию [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) для освобождения порта или обработчика, когда они больше не нужны.</span><span class="sxs-lookup"><span data-stu-id="46340-108">If your client program uses I/O completion ports or events for notification, it must call [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) to release the port or handle when it no longer needs them.</span></span>

 

 