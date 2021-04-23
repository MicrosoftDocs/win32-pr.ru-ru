---
title: Асинхронные каналы
description: Использование параметров канала с асинхронным RPC позволяет передавать данные постепенно, как только оно станет доступным, без привязки клиента и сервера.
ms.assetid: e5c466b8-c0b0-4fa8-8867-d0715fd614b2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be9d6dd5a3e8de7d5c4ad233a577187a49d04ed8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793224"
---
# <a name="asynchronous-pipes"></a><span data-ttu-id="38e24-103">Асинхронные каналы</span><span class="sxs-lookup"><span data-stu-id="38e24-103">Asynchronous Pipes</span></span>

<span data-ttu-id="38e24-104">Использование параметров [канала](/windows/desktop/Midl/pipe) с асинхронным RPC позволяет передавать данные постепенно, как только оно станет доступным, без привязки клиента и сервера.</span><span class="sxs-lookup"><span data-stu-id="38e24-104">Using [pipe](/windows/desktop/Midl/pipe) parameters with asynchronous RPC allows you to transmit data incrementally, as it becomes available, without tying up the client and server.</span></span> <span data-ttu-id="38e24-105">Это особенно полезно при наличии большого объема данных, которые необходимо передавать, в сочетании с замедляют клиент, с сервером или с высокой скоростью сети.</span><span class="sxs-lookup"><span data-stu-id="38e24-105">This is particularly useful when you have a large amount of data to transfer, combined with a slow client, a slow server, or a slow network.</span></span> <span data-ttu-id="38e24-106">При использовании канала в асинхронном вызове функции это, по определению, асинхронный канал.</span><span class="sxs-lookup"><span data-stu-id="38e24-106">If you use a pipe in an asynchronous function call, it is, by definition, an asynchronous pipe.</span></span> <span data-ttu-id="38e24-107">Синхронные каналы не поддерживаются вместе с асинхронными функциями.</span><span class="sxs-lookup"><span data-stu-id="38e24-107">Synchronous pipes are not supported in conjunction with asynchronous functions.</span></span>

<span data-ttu-id="38e24-108">В отличие от обычных (синхронных) каналов, в которых сервер обрабатывает все детали отправки и получения данных канала, асинхронные каналы являются симметричными.</span><span class="sxs-lookup"><span data-stu-id="38e24-108">Unlike conventional (synchronous) pipes where the server handles all the details of sending and receiving pipe data, asynchronous pipes are symmetrical.</span></span> <span data-ttu-id="38e24-109">То есть клиент и сервер могут отправлять и извлекать данные через канал.</span><span class="sxs-lookup"><span data-stu-id="38e24-109">That is, both the client and the server can push and pull data through the pipe.</span></span>

> [!Note]  
> <span data-ttu-id="38e24-110">Параметры канала могут передаваться только по ссылке.</span><span class="sxs-lookup"><span data-stu-id="38e24-110">Pipe parameters can only be passed by reference.</span></span> <span data-ttu-id="38e24-111">Даже если IDL-файл отображает параметры [канала](/windows/desktop/Midl/pipe) , передаваемые по значению, созданные суррогаты будут принимать параметры канала только по ссылке.</span><span class="sxs-lookup"><span data-stu-id="38e24-111">Even if the IDL file shows [pipe](/windows/desktop/Midl/pipe) parameters being passed by value, the generated stubs will accept pipe parameters by reference only.</span></span>

 

<span data-ttu-id="38e24-112">В следующем обсуждении асинхронных каналов предполагается знакомство с конструктором типа канала.</span><span class="sxs-lookup"><span data-stu-id="38e24-112">In the following discussion of asynchronous pipes, familiarity with the pipe type constructor is assumed.</span></span> <span data-ttu-id="38e24-113">Дополнительные сведения о процедурах канала, описанных в этих разделах, см. в разделе [каналы](pipes.md).</span><span class="sxs-lookup"><span data-stu-id="38e24-113">For more information on the pipe procedures described in these topics, see [Pipes](pipes.md).</span></span>

 

 